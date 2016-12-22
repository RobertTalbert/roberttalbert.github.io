---
layout: post
title:  "The value of keeping your mouth shut"
date:   2015-09-21 15:30:21   
author: Robert Talbert
tags: 	"IBL" 
---
_It's been a while since I have posted on the blog, but with this post I am starting a personal challenge: To write one post here on the blog each weekday for one month. The idea is to build a habit of posting so that going a day without posting will feel weird and off-schedule. Most likely the posts will be short but "greater than zero" is the idea. Here we go!_

It's hard to believe, but we are in week 4 of the Fall semester already, almost 1/4 of the way through. I'm teaching Discrete Structures for Computer Science this fall, which is a two-semester sequence, and I have two sections of the first semester and one section of the second semester. After my experiences at the RL Moore conference this summer and being around guys like Dana Ernst and T.J. Hitchman, I decided to design the course in an inquiry-based learning (IBL) style in which most of the time in the class is spent with students working in groups on problems and then presenting them at the board. 

I haven't gotten IBL completely figured out yet. The last time I tried IBL was about ten years ago in an abstract algebra course and it was an unmitigated disaster, mainly my fault for a number of reasons but I've been gun-shy about going the IBL route ever since. Until now, and boy, am I glad I did it. Let me relate an experience from this morning's Discrete Structures 1 course, which was an introductory unit on basic combinatorics. Students were working out solutions to several problems on the rule of products when, out of nowhere, two of those problems became a lot more interesting than I intended. 

__Problem 1: How many integers are there between 100 and 999 that do not use the number 7 in their digits?__ I figured this one would be trivial for the students, who through their Guided Practice work on this in a previous session showed strong mastery of basic counting before coming to class. The "textbook" solution would say: There are 648 such integers because there are 8 choices for the hundreds digit (can't use 0 or 7), 9 for the tens digit (can't use 7), and 9 for the ones digit (likewise); and using the rule of products we get $$8 \times 9 \times 9 = 648$$. 

But as I worked with groups around the room, I ended up with five different answers to this questions (648 being one of them), _all with plausible explanations_. Normally I assign eight problems for daily homework because we have 32 students in groups of 4, and each group gets a problem; this time I had each group with differing answers for this problem go to the board to explain their work. 

+ One group gave the explanation above. 
+ Another group gave this explanation: There are $$999-100 = 899$$ integers to choose from. Between 100 and 199 there are 19 integers that have a 7 in them (10 with a 7 in the ones place and 10 more with a 7 in the tens place, and then we counted 177 twice). The same is true for 200-299, 300-399, and so on except for 700-799 in which every integer has a 7. So that's $$100 + 8 \times 19 = 252$$ integers in all, and the ones that _don't_ have a 7 are the leftovers, of which there are $$899 - 252 = 647$$. 
+ The other solutions offered up by the class were variations on the "subtraction" idea in the second solution. Some came out to 648 and some didn't (due to missed assumptions or arithmetic errors). 

As the instructor, hanging out away from the front/center of the action and just listening to the students present, I spotted the error in the second solution immediately -- and I had a choice to make. Either bring it up, or keep my mouth shut. I _really_ wanted to bring it up because that's what mathematicians are trained to do. But I chose silence -- because this is not my show, it's the students'. 

Eventually one team caught the other team's error -- by starting with $$999-100$$ we undercount the number of integers that are in range by 1 -- and the whole class had an "aha" moment. Eventually I did step in, but only to provide perspective. _How many of you have ever written a program before that involved indexing an array, and the index went out of bounds?_ (This is a class of about 85% computer science majors.) Some knowing chuckles and then another "aha" moment as the students made a connection between this silly  problem and something they do as programmers that happens all the time. 

__Problem 2: A frozen yogurt store claims to offer over 1000 flavor combinations. They have strawberry and chocolate flavored froyo. How many toppings do they need to have available in order to make good on their advertising?__ This also sparked considerable discussion. Lots of people wanted to use binomial coefficients and factorials because, well, isn't that what you're supposed to use when you hear the word "combination"? But eventually they made a connection back to an earlier problem: Suppose you have a true-false test with 10 items. How many ways are there to answer (if you are not allowed to give blank response)? The answer is $$2^{10}$$ and a few students realized: _Oh, it's like a checklist -- for each flavor of yogurt you either do or do not include a topping._ So they just reasoned through to arrive an an abstraction, that if there are $$k$$ toppings then there are $$2 \times 2^k = 2^{k+1}$$ flavor combinations. So just do a brute-force search to get $$k = 9$$ as the minimum number of toppings. 

Again: I saw all the factorials and binomial coefficients being kicked around, and oh, how I wanted to swoop in and save the students from themselves. But I chose to keep my mouth shut, and they figured it out. 

One student had this beautiful realization: If $$T$$ is the set of all the toppings that are avaialble (and the cardinality of $$T$$ is $$n$$), then the power set $$\mathcal{P}(T)$$ is the set of all combinations of flavors, and we learned that there are $$2^n$$ elements in that power set. We had _just covered_ sets and I couldn't have been more pleased that he made that connection, which I had not even thought of. 

Here's what I get from this experience:

+ __Students are not dumb and they are not blank slates.__ Each and every one of them, even the ones who have failed the course before (and there are several of those) has intelligence and the capacity to reason, and they have contexts that provide a lot of leverage for coming up with great mathematics. 
+ __My job as the instructor is not to teach them mathematics.__ I cannot really do that because I lack the ability to create neurons in other people's brains. What I do instead is __teach them how to learn mathematics, and how to create mathematics__, and I do that by creating the right kind of environment and setting them to work. 
+ __Every time I talk in a math class it takes away my students' opportunity to learn things. So I need to shut my mouth more.__ The exceptions would be if I am providing perspective on things, directing traffic in a discussion, making sure everybody gets a chance to speak, or asking for a clarification. 

This isn't to say the instructor should _never_ talk in class (what would we do? Mime?) but we should stay out of the way and save that "time for telling" until it's really necessary, and doesn't detract from what students are doing. 

