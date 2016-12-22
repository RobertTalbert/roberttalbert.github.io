---
layout: post
title:  "Specs grading with the EMRF rubric, part 2"
---

[In a previous post, I wrote about the EMRF rubric](http://rtalbert.org/blog/2016/specs-grading-emrf) and how I am using it right now in my classes, which are using specifications grading. Here I want to discuss a few instances of how I've used it so far, and the kinds of effects this rubric has had on the narrative within, and about those classes. 

### Case 1: Using EMRF on a purely computational problem

In one of my classes (Cryptography and Privacy) one of the learning targets is 

>I can find the value of $$a \pmod n$$ for any integer $$a$$ and positive integer $$n$$ and perform modular arithmetic using addition and multiplication.

The problem they get consists of eight basic modular arithmetic computations to do involving adding, multiplying, and exponentiating. Unlike most work I give students to do, I don't especially care if they show their work on this problem. All I care about is whether they can compute the answer correctly or not. So the EMRF rubric is simply: 

+ E = All eight answers are correct. 
+ M = Either 6 or 7 out of 8 are correct. 
+ R = All parts are attempted but fewer than 6 answers are correct. 
+ F = Not all parts are attempted. 

The idea being that if students can do modular arithmetic correctly 8 times in a row in a single sitting, that's pretty exemplary and I am relatively certain they have mastered the concept. If they can do it correctly about 3/4 of the time then I consider that "good enough". Otherwise they need to practice some more and try again later. 

### Case 2: Using EMRF on a proof, part 1

The EMRF rubric gets a little more interesting when applying it to more complex work, like mathematical proofs. I have an activity I like to do in proof based courses where students "grade" a piece of work that I present to them. Students read through a proposition and proposed proof and then use clickers to rate the work according to the [specifications for student work document](https://gist.github.com/RobertTalbert/641c29bd9f3fc60cba93). 

Here's an example of an induction proof that students worked with:

![]({{ site.baseurl }}/assets/proofanalysis.png)

In the pre-class activity only 65% of students correctly identified that the proposition was true but that there is a major flaw -- the base case in the proof is missing. Most of the remaining 35% said the proof had only minor errors to be corrected that had to do with style and phrasing. In class, I put this proof up on the screen and asked students what grade they would give it, if they were me. About 1/3 of the students said either E or M, about 1/3 R, and about 1/3 F. We had a really interesting discussion then about what constitutes passing versus non-passing work, and what differentiates E from M. Once students saw the missing base case, all the E/M people switched to F! Students are much harsher graders than I am. 

For me, this is an F grade because it's fragmentary. (One could make a good argument for R, though.) A nice teaching moment in the discussion was that __the grade of F does not mean catastrophic failure. It means "fragmentary"__ and many times, work graded at an F is five minutes and two sentences away from E, which is the case for this proof. 


### Case 3: Using EMRF on a proof, part 2 

In my discrete structures course (same class as Case 2) we have this learning target on which students have to demonstrate proficiency: 

>I can outline and analyze a mathematical proof using weak induction, strong induction, and structural induction.

(There's another learning target where they have to actually _write_ a proof.) Here is one of the problems from a recent assessment on this target: 

>Consider the following proposition: __Every positive integer greater than 1 is divisible by at least one prime number.__ Assuming we prove this using strong induction, write clear statements of the base case, induction hypothesis, and inductive step. 

Here are some of the less-than-E responses and how I graded them with the rubric: 

+ A student used $$n = 1$$ as the base case and showed that since $$1$$ is divisible by itself and $$1$$ is prime, then the base case holds. The rest of the proof outline went off without errors. __In this case I gave the student an M.__ Does the work meet expectations? __Yes__: The student has provided evidence that they understand the most important aspects of strong induction. Is it complete and well-communicated? __No__: The base case is wrong. This is not a trivial error, otherwise this would be an E. But it's an error that can be corrected through written comments. If the student really wants to earn an E on this target, they can always take the assessment again later and get the base case right. 
+ A student set up the correct base case. For the inductive hypothesis, the student assumed that for some positive integer $$k$$, $$k$$ is divisible by a prime number; then stated that we want to prove that $$k+1$$ is divisible by a prime number. __In this case I gave the work an R.__ Does the work meet expectations? __No:__ The whole point of strong versus weak induction is that the inductive hypothesis is different, and work that doesn't demonstrate evidence that they understand this, has not met expectations. Is there evidence of partial understanding? __Yes:__ The rest of the outline is fine. The student just needs to try it again. 
+ A student set up the right base case. For the inductive hypothesis, the student said that we will assume that $$2, 3, 4, \dots, k$$ are divisible by a prime number _for all positive integers $$k$$_; then stated that we want to prove that $$k+1$$ is divisible by a prime number. __In this case I gave the work an R.__  Does the work meet expectations? __No:__ Outlines of induction proofs are expected to show understanding of the basic logic underlying the concept of induction, and getting the quantifier wrong in the inductive hypothesis casts doubt on that understanding. It's a significant logical error in which the proof assumes the conclusion. But, is there evidence of partial understanding? __Yes:__ The rest of the proof is fine. The student just needs to try it again and get the quantifier right. 

One of the many things I like about this rubric and the process of continuous revision that it feeds is that the assessment process is now, [in the words of Dee Fink, "educative" rather than "auditive"](http://www.deefinkandassociates.com/GuidetoCourseDesignAug05.pdf). That is, the assessment process is helping students _learn_ mathematics rather than simply telling them what they don't know. 

It also saves a ton of time. In all these cases, the decision of what grade to attach took me less than 90 seconds, including the time it took to actually read the work. In a traditional grading setting, I would have to not only spot the error but then go on to agonize over whether a messed-up base case should get 10 out of 12 or 11 out of 12 or... And then repeat for the other two cases, and I can guarantee that would take an order or magnitude longer. It left me with enough time to write down meaningful feedback in complete sentences. 

Another way this saves time is that I very rarely get work that evaluates to an F. Since students can redo assessments through the semester, if they find themselves taking an assessment and can't produce a coherent finished project, they just bail out, and the work never gets turned in. And that's exactly what they should do, and make plans to try again next time. 

### How this changes the narrative

Yesterday I handed back some work on assessments, and a student pulled me aside and asked if he could argue for a higher grade. He had done work on a problem (solving a recurrence relation) where he made an initial algebra error that was serious, but then worked through the rest of the procedure correctly. I had given him an R; he was arguing for an M. 

Sounds familiar, except this time the student was not grubbing for points -- what's a "point"? -- but rather presenting a coherent and well-considered explanation for why, in his opinion, his work meets the standards for M. It was an exchange between two people on the same level. I did not agree with his argument in the end -- the standards for this problem clearly state that you have to get the answer right in order to be eligible for a passing mark -- but after telling the student this, I could also say, "You definitely show evidence of understanding. You'll get this right next time." It wasn't about _points_, it was about _quality_ and there's a world of difference here. 

I suspect some of you reading my evaluations above are disagreeing with me, but probably the disagreement is on _quality_ issues (standards), not _quantity_ issues (points). That's a narrative that I want to support. 

