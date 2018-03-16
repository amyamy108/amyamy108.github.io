---
layout: post
title:      "Tic Tac Toe: Valid Move, Valid Question"
date:       2018-03-16 12:41:33 -0400
permalink:  tic_tac_toe_valid_move_valid_question
---


As of yesterday, I decided the easiest way to keep up with this blog would be to document every lab and the troubleshooting that followed, since I'm trying to average at least one lab a day. Like some of my other *brilliant* ideas, I promptly forgot and finished "Tic Tac Toe Position Taken" without taking too many notes. So, there's my first problem. This is my second. 

When creating #valid_move? , I was more comfortable with test driven development and thought I had it down. I figured out how to get #between to work no sweat (not that big a deal in the long run, but regardless a nice endorphin bump) - but, here came the stumper. My previous #position_taken? was invalidating my #valid_move? After running a few tests, heres what we had: 

```
1 > def valid_move?(board, index)
2 >   if index.between?(0,8)
3 >     true
4 >   elsif index >= 9
5 >     false
6 >   elsif position_taken?
7 >     false
8 >   else
9 >     true
10>   end
11> end
12> 
13> def position_taken? (board, index)
14>   if board[index] == "" || board[index] == " "
15>     false
16>   elsif board[index] == nil
17>     false
18>   else board[index] == "X" || board[index] == "O"
19>     true
20>   end
21> end
```

Here is the error it returned: 

  1) ./lib/valid_move.rb returns nil or false for an occupied position
     Failure/Error: expect(valid_move?(board, index)).to be_falsey
       expected: falsey value
            got: true
      ./spec/valid_move_spec.rb:20:in `block (2 levels) in <top (required)>'

> rspec ./spec/valid_move_spec.rb:16 # ./lib/valid_move.rb returns nil or false for an occupied position 

So far, it seemed my problem was clearly with my 16th line of code:  a.k.a., code that had previously, apparently, tested fine. (I also don't know why this thing is still highlighted, so bear with me). Extra confusing, still, since I'd worked with a study group the day before and got the green light.

First, I recognized that the order for #valid_move? if/else statements needed to be rearranged. As I'd learned in the previous labs, if the input passes the first if statement as a truthey, then the operation stops regardless of whether or not the input also returns truthy for other elsif statements. Since the first input would have validated anything between 0 - 8 *regardless* of whether the position was already taken, I decided to move anything that I wanted to return "true" to the end of the method def.

Second, the nil problem. The code has passed previously, with some help from a study session from the previous day, so the instructor at least agreed that this method definition was functional, if not the correct answer. Time to tinker. My first thought: Change #position_taken?. One of the (many) iterations was: 

def position_taken? (board, index)
  if board[index] == "" || board[index] == " " || nil
    false
  else board[index] == "X" || board[index] == "O"
    true
  end
end

Which wouldn't work - the booleans lead to muddled logic. I tinkered more. I should have written all of the trial and errors down (and I will in the future), but, finally, I received an error message that clarified things: 

     ArgumentError:
       wrong number of arguments (given 0, expected 2)
			 
This specifically applied to the code on line 6, and I realized that the same array and variables originally expressed in def #position_taken? had to be passed into the body of def #valid_move? for the method to work. In the end, this is the code that passed the test: 

def valid_move?(board, index)
  if index >= 9
    false
  elsif position_taken?(board, index)
    false
  elsif index.between?(0,8)
    true
  else board[index] != "X" || board[index] != "O"
    true
  end
end

def position_taken? (board, index)
  if board[index] == "" || board[index] == " "
    false
  elsif board[index] == nil
    false
  else board[index] == "X" || board[index] == "O"
    true
  end
end

This code is not perfect: I feel like one of the rspec tests came out truthy by default, that all of our preemptive if/else statements are not met, and " else board[index] != "X" || board[index] != "O" " was rigged to try and meet the "it 'returns true for a valid position on a non-empty board" qualification - it might be redundant. 

While I get this checked (and I'll report back if there is better code out there) I'll be at least a little pleased. 

This lab was a bit of a milestone: I solved it without help from an outside party. Granted, I could not have done it without clarifying issues in previous labs with excellent Flatiron Fellows, but to all those that are tempted to reach out at the first for fifth sign of trouble- keep going. Iterate at least 10 times before seeking help, and explicitly lay out your thought process when you do so that (a) your terminology can be corrected if need be, and (b) you learn more by "rubber ducking" than by being told the right answer.

Lastly, write it all down. I'll write it all down, too.

Happy Friday, all! And happy coding! 

UPDATE: After getting it checked, the #valid_move? can be simpified further! See below:

def valid_move?(board, index)
  if position_taken?(board, index)
    false
  elsif index.between?(0,8)
    true
  end
end


- A. K. Young
