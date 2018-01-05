---
layout: post
title:  "A vignette on specs grading and rigor"
date:   2015-06-16 17:24:05   
author: Robert Talbert
tags: 	'specs grading'
---

I've been using [specifications grading](http://chronicle.com/blognetwork/castingoutnines/2015/01/19/putting-specs-grading-to-work/) in my [fully-online calculus course](http://chronicle.com/blognetwork/castingoutnines/2015/05/14/is-flipping-an-online-course-possible/) this summer and it's been awesome. One of the reasons it is awesome is that it allows me to maintain a level of academic rigor that I've never had in a calculus class before, while making that rigor accessible to students and not just a wall they slam into. This morning I was grading some work from a student that really brought this home. Obviously to protect privacy, I am changing all the data in the problem and will alternate genders when referring to the student, but the situation is the same as in real life. 

Students were asked in a miniproject (which is our time/space-agnostic word for "lab assignment") to take a set of two-variable data -- which can be thought of as a function -- and then find a linear approximation to the function at a point, which they then go on to use to do some estimations. Let's say the data points include $$(3, 15)$$, $$(5, 9)$$, and $$(7, 3)$$ and the linear approximation is to be done at $$x = 5$$. 

The student correctly estimated the derivative at $$x=5$$ to be $$f'(5) \approx \frac{3-15}{7-3} = -\frac{12}{4} = - 3$$. Then he proceeded like so: 

$$\begin{align*}
L(x) &= f'(5)(x - 5) + f(5) \\
     &= -3(x-5) + 9 \\
     &= -3x + 24 \\ 
   3x &= 24 \\
   x &= 8
\end{align*}$$

The first three lines are spot-on. The second two lines are _computationally_ correct but not _logically_ correct because there is no reason to be setting $$L(x)$$ equal to 0 and solving. 

Let's pretend this is a 12-point problem. How many points would you award? On the one hand, the student _has_ done correct work. But it's embedded along with some other work that in _one_ sense is correct but in a larger sense is incorrect. What's that come out to: 10 points out of 12? 6 points? 12 points, because the correct work is there (albeit as a proper subset of the submission)? Or 0 points, because the answer is wrong and there are some conceptual issues here? 

Three things are apparent here. 

1. We could spend a lot of time, relatively speaking, trying to make Solomonic judgments about the point value of this work. Maybe it takes three minutes of deliberation to arrive at a value you feel comfortable with. That's not much, but scaled up to 30 students with similar work, that's an hour and half spent on <s>grading</s> hairsplitting that you could have spent doing something better, like actually giving feedback to students, or playing with your kids or running a 10K or watching _Sharknado_. 
2. No matter what you decide about the points, the student can, and possibly will, come back at you with a dispute. If you give $$n$$ points of credit out of 12, the student is likely to argue for $$\lceil (12-n)/2 \rceil$$ more points. Those arguments take time, let's say 10 minutes each, times how many students? You get the picture. 
3. And then what do you say on the student's work itself? If it were me, it depends on where that student's work is in the queue. If he is the first student I am grading, I'd probably circle the work and say: _"This work is unnecessary. Why?"_ with the slightly optimistic view that he will reply to me somehow. If she's in the middle of the stack, I'd circle it and say _"Unnecessary"_ and leave it at that. At the end of the stack, it'd just be a circle (along with spit stains and spilled coffee). The quality of the feedback diminishes with time, or rather with my energy. And anyway, what incentive does the student have to respond to your feedback, even if it doesn't suck? They've earned/lost the same amount of points either way, unless they dispute it, see above. 

Actually there's a fourth thing here: No matter what you do with the points, __it's a judgment call based on your best professional estimation__ of the quality of the work. The fact that it's wrapped in a numerical envelope doesn't make it numerical data. The point value you give is just a label, like a ZIP code. It has no inherent mathematical or statistical meaning. In fact all grading is like this. Even the fact that I consider the problem above to be worth giving in the first place is a "best professional judgment". Faculty and students need to get over the illusion of objectivity when it comes to numerical grading, and stop trying to do statistics with ZIP codes. 

On the other hand: Under the specs grading system for our course, we have [Specifications for Student Work](https://gist.github.com/RobertTalbert/824a300bce0186458423) that apply to the various forms of work we do. Miniproject work is not graded on points at all -- nothing the class is -- so there is no agonizing about giving whatever out of 12 points. Instead the work is graded as __Mastery__, __Progressing__, or __Novice__ based on the descriptions given in the specs. My specs tend to revolve around the presence or absence of _error_ in student work -- either computational, logical, syntactic, or semantic error -- and how significant and/or numerous the errors are. Briefly, __Mastery__ means the only errors present are small numbers of minor ones; __Novice__ means lots of errors in both quantity and quality, or one huge error that kills the whole assignment; __Progressing__ means "nearly __Mastery__" but not quite. __Novice__ miniproject work can be revised and resubmitted by spending a token, which students have five of to begin with; __Progressing__ work can be revised for free. (See the [syllabus](https://docs.google.com/document/d/14m-WX7Jwr2r2s-MG5ax2Bk2-Fh52kel5dEX8LXSYjKc/edit?usp=sharing) for the details.) 

So how does specs grading apply to my student here? Instead of losing my mind over points, I ask: _Does the work meet the standards for Mastery, in my best professional judgment?_ The answer here for me is "no" because of those last two lines in the solution. They cast doubt on whether the student understands the concept of the linear approximation yet -- it's not apparent that she knows what the linear approximation actually _is_. But it's also not all bad, in fact it's mostly good. Here's a paraphrasing of the feedback that I put on her work: 

>The work here seems to indicate that $$x = 8$$ is the final answer because it is on the final line of the solution. But above you have $$L(x)$$, which is usually the notation we use for the linear approximation. Could you clarify what the answer is? And if the final answer is $$L(x)$$, should you be solving for $$x$$ here? I can't be sure that you are  correct otherwise. 

And in his Blackboard gradebook along with the __Progressing__ mark is a blurb for the whole assignment that points out what she did well, and a directive to please revise and resubmit the work having addressed the issues that I pointed out. If he would take those issues under consideration, answer my questions and correct any mistakes, and resubmit -- which she can do without penalty over the next five weeks -- then he'll be upgraded to __Mastery__ level. I think she'll do it. Certainly all the incentives point toward revision and resubmission and there's no real downside. 

I can hold very high standards of rigor this way without regrets, because students aren't _losing points_ by my doing so. I can insist that students get solutions _exactly right_, for once, including notation and semantics. Other instances where I've awarded the __Progressing__ label (sometimes __Novice__) have included: 

+ Students using the notation $$\displaystyle{f'(x)_{\lim h \to 0} = \frac{f(x+h) - f(x)}{h}}$$ to calculate a derivative. In past years I'd had to either take off points for this and brace myself for grade disputes, or else swallow hard and overlook it. It's so much better to say: "This notation is syntactically and semantically meaningless. Correct notation matters here. Please look carefully at the definition and try again."
+ Students used technology to find a best-fit curve through a set of data, then took the derivative and said some stuff about rates of change. Some students chose a linear function to model clearly nonlinear data. Of course all the calculus is correct, but do I really think the student has mastered the concept of using calculus on real data if they think a linear function fits nonlinear data? Nope, and I'm not interested in communicating this through rational numbers like "8/12". Instead I marked it as __Progressing__ and said, "This is a really poor fit for your data, don't you think? We don't want to get into the habit of working with bad models. Try again with a model that is a better fit. It won't take you too long because it seems like you know the calculus part of this."

If there is any dispute, it will not be stupid point-grubbing but rather a discussion about _mathematics_ and about _professional standards of work_. Because I am not agonizing over points, I have time to give this kind of feedback. And the student _has_ to address the feedback in order to earn the __Mastery__ rating. 

"Try again" is just a lot better than "10/12". 
<!--stackedit_data:
eyJoaXN0b3J5IjpbOTc4NzIwODIwXX0=
-->