---
layout: post
title:  "Specifications grading report, part 2: Context"
date:   2015-07-15 12:18:38   
author: Robert Talbert
tags: 	"specs grading"
---
This is the second installment in an ongoing technical report on my use of specifications grading. [Here's the first post](http://rtalbert.org/blog/2015/Specs-grading-report-part-1/). In this post, I want to give a bit of my own history with grading that would explain why I made the jump to specs grading and what problems I hoped to solve with it. 

This needs explaining because, heading into Winter semester 2015 (that's the climate-appropriate Michigan term for the semester that runs from January through April) where I first used specs grading, I had absolutely no intention of doing anything with my grading system. I hadn't even heard of specs grading until November 2014, when I first heard about it through this article featuring Linda Nilson. I was inspired by that article and her book, so much so that I then embarked on a five-week crash course to completely rethink the way I do assessment and grading, almost immovably embedded in 20 years of classroom practice, so that I could get a workable implementation ready for January 5, 2015. I spent my entire holiday break working on this and wore myself out mentally in the process. What would drive a person to do this? What did I see? 

### My history with traditional grading

Prior to January 2015, every class I had ever taught had a grading system based on the usual premises: Students do stuff that is related to the course objectives; that stuff is then assessed a point value based on a total that represents "perfect" work; and then these point totals flow like tributaries into a larger river of points, with suitable statistical adjustments to make the flow more representative of the relative value of the work to the course. In the end, the adjusted flow of points is itself a number value that is then mapped to a letter that gives an overall rating that indicates the extent to which students have mastered the course content. 

My approach to assessment has gotten more and more nuanced since I started teaching back in 1994 as a Vanderbilt graduate student. At first, teaching Calculus for Engineers twice a year, I just gave three tests and a final. At some point during grad school, I started folding in other assessments like graded homework. Once I started teaching at a small liberal arts college, where skills like communication and critical thinking were explicitly valued, I added in assessments like reading/writing assignments, computer labs, and structured participation credits. But no matter how <strike>Byzantine</strike> nuanced the _assessment_ setup was, the _grading_ setup was still the same: assess point values to the work, set up a statistical algorithm to adjust the point flow to match relative value of each piece of work, and then do the statistics at the end to assign a letter grade. It always went back to points and statistics.

### What's so bad about points 

I never questioned _why_ I used points and statistics for grading. It was how I personally had always been graded and how everyone around me graded. But in the 20 years since I started, I grew more and more dissatisfied with point-based grading. As of Fall 2014, just before I discovered specs grading, I could pinpoint four specific things about traditional grading that made me unhappy: 

1. __Too many false positives.__ Every course I taught has had at least one person whose grade is a lot higher than his skill level indicates. This is actually rarely a person getting an "A" where it is undeserved. It's more frequently students getting "B" grades when really they are more like "C" or lower students; or students getting a "C" who quite honestly don't demonstrate baseline skill and should get an "F". Shouldn't a "B" student be able to do _some_ things at "A" level? 
2. __Too many false negatives.__ On the flip side, I always have students who works hard and who I am certain can _eventually_ demonstrate mastery on the content and the learning objectives, but who may be just a step behind the rest of the class; or had a significant issue in their personal lives on one day during the semester; or had the flu during one of the tests; and so on. Another instance of the grade not portraying the true skill of the student. 
3. __Encouragement of a game-playing approach.__ But by far my worst problem with traditional points-based grading is that it encourages, almost demands, that students consider my courses to be a game where the object is to score as many points as possible. At the beginning of the course, students seem to care about actually learning the material. By the end, they are just trying to score points and it doesn't matter how or why. For some, this is the way they approach the course throughout. 
4. __Students are disempowered.__ It hit me one day how often I'd heard students say, _"I hope to get a good grade in this course."_ They _hope to get_, as if the grade in the course is the result of a pseudorandom process or an act of faith. _I'll just put up some kind of work, not necessarily good, and maybe the prof will give me enough points on just enough things that I'll make it_. My whole shift to the flipped learning model was predicated on giving students more control, more oversight, more choice in what they learn and how they learn it --- to break the dependency on me as the professor for their learning and to make them responsible agents in their education. Can I really say that I'm doing that well when my grading system, the backbone of how I assess student work, promotes the opposite? 

### What about standards-based grading? 

A quick word about standards-based grading: I'd encountered SBG a few years ago, mainly through [this series of blog posts](http://shawncornally.com/wordpress/?page_id=114) and through the usage of SBG by some of my Grand Valley State colleagues. I was intrigued and at first I thought, maybe this is the way forward. But every time I looked at SBG implementations, I ended up thinking: _This will crush me and I will be grading constantly if I go this route._ I wanted to believe. But I could never come up with a way to make SBG work for me and not put me at the bottom of an avalanche of finely detailed paperwork. I've had SBG proponents try to show me the way but it's never changed my mind. Sorry guys. 

### Two experiences that changed my thinking

Two things happened during the summer and fall of 2014 that made me ready to ditch traditional grading once and for all. 

First of all, in the summer: I signed all three of my kids up for swim camp at GVSU. My kids were 5, 8, and 10 years old at the time and at radically different places in their physical development. So the swim instructors, as expected, worked with them differently in different age groups. You might be thinking that the big epiphany was this differentiated instruction, but that's not it. What made me really stop and think was the performance report, the "report card", that each of my kids got. Here's the one for my 8-year old: 

![Swimming report]({{ site.baseurl }}/assets/swimreport.png)

Kids in her group were expected to work on levels 1--4. Notice it doesn't give a letter grade. My 8-year old didn't get a "B" in swimming. Even if she had, what would that letter indicate? Would it mean she was doing 80% of each level? Or 100% of the first three levels but only 20% of the fourth one? Or what? The letter conveys no information about actual skill. 

Instead, this report has a simple rubric (color coded); clear outcomes; and a clear indication of how well each learner is doing on each outcome. I must have been thinking about my misgivings with traditional grading, because this report stopped me in my tracks. It's simple. It's based on evidence. It's set up to help the learner know how well he or she is doing and provides a way of setting goals for improvement. I was captivated. I tweeted: 

<blockquote class="twitter-tweet" lang="en"><p lang="en" dir="ltr">Kids&#39; &quot;report card&quot; from swim camp. Can we do something similar for math? <a href="https://twitter.com/hashtag/sbg?src=hash">#sbg</a> <a href="http://t.co/TczklPaAMJ">pic.twitter.com/TczklPaAMJ</a></p>&mdash; Robert Talbert (@RobertTalbert) <a href="https://twitter.com/RobertTalbert/status/484757926117376000">July 3, 2014</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

Second of all, in the fall: In Winter 2014 and Fall 2014, I had an unusually high number of instances of false negatives -- students whose grades truly didn't indicate their potential, their skill, or their facility with the course concepts. I had a student who'd had me before in a class and who had a great attitude coming in, who invariably figured out course concepts one week following her tests; she became hostile and bitter and did not do well. There was another student who was bright and capable but kept having personal issues that interfered with her work; the bad grades piled up and eventually she had to drop. 

Teaching and learning is all about people, and it pains me when my students suffer needlessly because of the silliness of a traditional grading system. I swore that before another year goes by I am going to do something about the broken system of grading I'd been putting up with, for no good reason, for 20 years. 

### ...And along came specs grading

I didn't have a good answer to the question of _how_ I was going to make my decisive break with traditional grading until I read [this article from Linda Nilson](http://www.utimes.pitt.edu/?p=30598). I read the article several times, immediately ordered [her book](http://www.amazon.com/Specifications-Grading-Restoring-Motivating-Students/dp/1620362422) and devoured it, and [did a public Google Hangout](https://youtu.be/1AI9n0_5obI) with my friend and colleague T.J. Hitchman to talk it through. 

What I saw in specs grading is what I listed in the first post in this series.  It deals effectively with all the problems I had with traditional grading, without the overhead that seemed to come with standards-based grading. It seemed almost too good to be true -- maybe I'd finally stumbled across the answer to 20 years' worth of mounting frustration with traditional grading. I knew from around Chapter 3 of Linda's book that I _had_ to switch to specs grading -- whatever it took, for the sake of my students and for my own sanity and professional integrity. 

And I had to do it _now_. The upcoming semester was just six weeks away and I had already designed the backbone of my courses. Switching to specs grading would mean ripping out most of that design, figuring out an implementation that works for a math course (Linda's book has examples in it but most are not in mathematics), and get it ready to go... in six weeks, three of which were filled up with closing out the current semester. 

So I spent every moment between December and January 5 (that wasn't already occupied) thinking and blogging about specs grading, drafting and re-drafting syllabi, making changes, and finally settling on a system and getting as far as I could with populating my courses. I was exhausted when classes started. When day 1 of Winter 2015 semester started and I told my students: _Nothing in this class has any point value whatsoever; all your work is graded pass-fail and your grade determined by a list of achievements at passing level_ I thought: That's it. I'm crazy. I'm done. I don't even have tenure yet, so what do I think I'm doing? The students are going to first think I'm trolling them, then they're going to kill me. 

But I've never let stupid ideas or the threat of bodily harm get in the way before of my teaching before, so why start now? 

### In our next episode...

In the next installment, I'll detail "implementation 1a" of specs grading used in my Discrete Structures for Computer Science course, including what went well and what were, shall we say, "learning experiences". Stay tuned and leave me your questions below. 




