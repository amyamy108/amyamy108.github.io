---
layout: post
title:  "CLI -mbing Scone Mountain"
date:   2017-09-26 03:40:57 +0000
---


Terrible puns aside, for some reason this CLI Greetings lab really tripped me up, essentially because I didn't understand how the directories were designed to interact. Their purposes are easy to confuse - what makes the code and contents of the bin directory "executable" and what does it mean for the lib directory to "define"? Even the subsequent definitions seemed pretty vague. For me, at least, the only way to learn was to work through the lab. 

The best metaphor I can come up with to better understand their relationship is that of baking scones. Especially topical, since I botched a batch just the other day. God knows if it was subconscious guilt that made me craft this example, but in essence, the thought process behind baking scones goes like this:

Input |         "I think I'd like to make scones. What sweet nibblings do I have on hand?" 
Variables|     dried cherries, dark chocolate
Retrieve |     Great Gran's recipe and commence with the bake!  

Though it is probably obvious to you, dear reader, what each part of the process represents, let's break it down. The bin directory is represented by the executable logic (i.e. "let's bake!" and setting the parameters of that action), the #gets method is represented by the ingredients on hand  (a.k.a. the terms/ variables you can't control, which are typed by a contributing party), and lib directory is represented by the defined recipe which can be executed with those ingredients. The execution of this entire endeavor was set forth by an overarching action (a.k.a. the bin directory) but that specific recipe is defined in a completely different directory, a.k.a. a cookbook. Still essential for pulling-off the plan, but located in a different place. 

Other helpful observations - the bin files (for now) are simple - lines of puts, defined variables, and calls to particular methods. The Lib files contain examples of the work we've been doing up to this point. 

*Why* defining a method *must* go in the lib and can't be combined within the bin is still a mystery to me. Dear reader, feel free to set me straight, but I'll shall continue my quest for an easily digestible answer! 

Okay, puns are over now. 
_________________

In other "climbing the mountain" news, I am setting an outrageous goal for myself: I am going to finish Intro to Ruby Development by Sunday of this week. October 2 seems just as good a day as any to graduate from Intro, and though I'm balancing three jobs, let's peddle to the metal! HERE WE GO.

- A.K. 
