---
layout: post
title:  "A Note for New Practitioners "
date:   2017-09-04 17:48:38 -0400
---


There's an old adage that claims "life is what happens when you're busy making other plans." That job offer falls through, for instance. Your cat gets put down. You find a rat nest in your room, there's a shooting on your block, and then two job offers come through. These things happen. That's life. Screw your plans, and your coding bootcamp be damned! 

There's another adage that I think is more valuable: The grass is greener where you water it. The most important aspect of it, however, is not assigning blame or manifesting disappointment in yourself, that you really couldn't do it all. Sometimes you have to take time away. It's not great, and there are costs doing so, but online learning is a bit like meditation. The point of meditation is not the perfectly focused mind, but the practice of coming back to the exercise. Monkey mind takes over, but the most important (and productive) part of practice is refocusing on your practice.

Case in point: I had WAY over thought the Tic-Tac-Toe board exercise. I'd just learned about arrays but none of my code seemed to satisfy my lab. When I tried to tap other ruby communities for answers to the coding conundrum (aka take a detrimental shortcut) an anonymous contributor noted that each space had to have a special designation, so the computer would understand which "X" or "O" would go in each space. 

At this point, I'm two hours into the same dang lab. I've worked myself into a lather, feeling like an idiot for failing this lab, and ended up with this (published here at the risk of serious embarassment down the road): 

```
> def display_board
> puts "[a1] | [a2] | [a3]"
> puts "[b1] | [b2] | [b3]"
> puts "[c1] | [c2] | [c3]" 
> end
```


It was at this point that "life" happened. I'll skip all that, to the most important part where I came back to the exercise with absolutely not idea how I'd reached my previous conclusion. I reviewed the previous lessons in hopes I'd figure it out, yet continued to struggle. The IDE wouldn't launch properly, I was stuck in irb, the end/ exit command wouldn't work ... clearly I'd met my match.

Enter Michael D., who was at once incredibly kind, empowering, and informative - one of the many reasons I am so happy to be part of have joined this community. 

First, he set me straight about irb. Fun fact, if you execute "end" and see either - 

2.3.1 :024"> exit

or

2.3.1 :003?> end

 - there is a missing or expected element in your previous irb code. Go back over your code, figure it out, and then you'll be BACK IN THE GAME.

Then, Michael informed me that "you can't puts an array." *game changer*  Strings are the only class/ data type that can follow puts/ print commands. I did not know that, and that certainly makes things more clear cut.

Finally, he told me there was no need to assign each space a designated ID. For now, we were sticking with straight ASCII. 

From there, it was pretty easy sailing. I won't post the answer here lest I take a learning opportunity from someone else, but Michael was a wonderful help and I am certainly excited to get past that deceptively simple lab. 


TL, DR;

1. Don't get upset with yourself if you have to take time away from coding. The most important part is that you do come back to your practice.
2. Seriously, don't be afraid to ask for help. The coaches are incredible, knowledgeable, and just want to see you succeed.

and *if,* like me, you let life take the wheel and need a short refresher on the first few Ruby lessons, I'll post my notes in subsequent blog posts. 

TTFN, 

- AK 


 
