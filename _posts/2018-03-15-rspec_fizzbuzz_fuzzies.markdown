---
layout: post
title:      "Rspec Fizzbuzz Fuzzies"
date:       2018-03-15 04:00:52 +0000
permalink:  rspec_fizzbuzz_fuzzies
---


Who knew this exercise would so heavily rely on my first-grade logic! Let's dive in. 

First, I loved learning about booleans and conditional logic. It ran in a way that made sense, and proved a fun challenge in organizing the coding process. That, and who doesn't love a good foray into TDD? 

The problem arose in Rspec Fizzbuzz. There was excellent literature on how rspec and learn run differently, require different file paths, explanations of way, and when it came time to create the actual code in root file fizzbuzz.rb, I was REH-DEE. 

First time around, this is what I had: 

```
> def fizzbuzz(int)
>   if int % 3 == 0
>      "Fizz"
>   elsif int % 5 == 0 
>      "Buzz"
>   elsif int % 3 && 5 == 0
>      "FizzBuzz"
>   else
>      "nil"
>   end
> end
```

And then an hour passed as I continued to struggle UNBELIEVABLY with those last two troublesome returns. I tried:

elsif int % 3, 5 == 0

elsif int % 3  % 5 == 0 

elsif int % (3 && 5) == 0

and all kinds of formats in between. Whats worse, I knew they were wrong. The computer was reading some of these as int % 3 (true), % 5 == 0 (false) (which, since we used the && operation, makes the entire statement false), and I had trouble getting my head out of the sand. Time to ask another brain.

Enter Sophia, and thank GOODNESS for it. Here is where the first-grader logic came into play. First, read those errors closely! I would have discovered that since the code reads everything line by line, any integer that was divisible by 3 would *stop* at the first conditional, returning Fizz, instead of continuing to the second else conditional. Same with any integer that was divisible by 5. A number like 15 wouldn't even make it to FizzBuzz! 

With that in mind, we could use the same structure to ensure that our variable returned what we wanted. We had to make sure that whatever was divisible by 3 was also definitively not divisible by 5, and while I was tempted to write something like:

```
if int % 3 == 0 && int !(...)
```

Sophia reminded me that we already had the tools to craft a more elegant solution. The final thing to fix was getting rid of those quotes around nil (for reasons I am still trying to figure out, come back Sophia I need you!) 

```
def fizzbuzz(int)
  if int % 3 == 0 && int % 5 != 0
     "Fizz"
  elsif int % 5 == 0 && int % 3 != 0
     "Buzz"
  elsif int % 3 == 0 && int % 5 == 0
     "FizzBuzz"
  else
     nil
  end
end
```

Let that be a lesson to you. Don't be embarrassed, and once you get it, you get it. 

Happy Pi Day! 

A. K. Young

