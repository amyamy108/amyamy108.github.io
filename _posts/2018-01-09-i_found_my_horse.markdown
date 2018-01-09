---
layout: post
title:      "I Found My Horse"
date:       2018-01-09 05:20:33 +0000
permalink:  i_found_my_horse
---

This is what happens after a little bit of humble pie, when you've stepped away from coding for an **embarrassing** amount of time, and decide to jump straight back into CLI. In other words, this is how to relearn everything you unlearned in Learn.co 

Let's start slow. Not like there was any other option, but still. 

This is how you get to the correct directory in IDE:

1. type `pwd` into your terminal to see where you even are, because you keep typing 'learn' to try and relearned what you've apparently not learned and the terminal returns "You don't appear to be in a Learn lesson's directory. Please `cd` to an appropriate directory." So as I said, you type in `pwd` which returns */home/amykristenyoung-30210/code*.  Discover you are certainly not where you should be. Ask for help. 

2. Follow the suggestion of a very nice person named Sam, who suggests you type `ls` for some reason. The terminal returns the word 'labs' .


3. Sam says AHA, type `cd labs` so that is what you do. you've always been good at taking direction, good on you! `pwd` now returns */home/amykristenyoung-30210/code/labs* We are getting somewhere. memory is starting to thaw ... 


4. Enter `cd ttt-5-move-rb-v-000`, then `pwd` to return 
*/home/amykristenyoung-30210/code/labs/ttt-5-move-rb-v-000* . Run 'learn' . Completely ignore "Could not find coderay-1.1.0 in any of the sources    Run `bundle install` to install missing gems." and continue forward needlessly. 

5. Enter `cd lib` and enter `pwd` to return /*home/amykristenyoung-30210/code/labs/ttt-5-move-rb-v-000/lib* and get flummoxed as to why you again don't seem to be in Learn's directory. 


6. Sam informs you of your error, but only five seconds after you embarrassingly figure it out yourself. To go back, type `cd ..` which returns you to your previous step. run `bundle install` which will reinstall the missing gems, like the program mentioned the first time. enter 'learn' , and realize you still have a solid amount of work to do, but be pleased that you will never again have to ask how it's done because you took really great notes this time. 


This is how you figure out #index_to_input 

1. Read the directions many, many times over. remember this is an edge case and spaces are going to be important. 
2. Get very confused when this bit of code doesn't work: 

```
> def input_to_index('user_input')
>   'user_input'.to_i - 1
> end
```

(How exciting, reader, can you spot the error yourself?)

3. Listen to your Slack-mate who is ever so kindly assisting you. He says: "so when you write a method, whatever you put in between the parenthesis is just a variable, a stand-in for whatever is going to be passed into the method. So since its a variable, it isn't a string. once it is passed in by the user on the command line, that variable will have the value of a string. but the variable name will be user_input  which will point to a string. in this case a string of whichever number they input." Assess, correct, victory! The bit of code now reads:

```
> def input_to_index(user_input)
>   'user_input'.to_i - 1
> end
```

 But our tests are still returning one failure. Try many other amalgamations which are certainly not correct. here is my most embarassing favorte:
 
 ```
> def input_to_index('user_input')
>   'user_input'.to_i 
>   user_input- 1
> end
```


4. Point this out to your Slack-mate upon which he points this out to you:  "right...now that you have a proper argument being passed in, you'll need to use that argument. right now you are still using 'user_input'.  remember I said, one thing to fix in two places?" I fix it, and now everything is green. It feels like Christmas. Well done. Only 2 other methods and lots of other failed tests to go. 

This is how you figured out #move method: 

1. Realize you've already been up for 20 hours today, and you've spent an hour and half on this today, and while that may be paltry to some (and paltry compared to your efforts in the future) it is a step in the right direction.  I found my horse. And I'm on it now, entirely because of this community. Thanks Flatiron! See you tomorrow. 

- A. K. Young


