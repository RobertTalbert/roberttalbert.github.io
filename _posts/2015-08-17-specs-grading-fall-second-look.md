---
layout: post
title:  "Specs grading for Fall classes: A second look"
date:   2015-08-17 12:17:48   
author: Robert Talbert
tags: 	"specs grading"
---
I've been at conferences or on vacation for the last two weeks, but I'm now back and engaging in the mad sprint to the start of Fall semester classes. I am still sort of at the beginning of the six-part series on specs grading ([first post here](http://rtalbert.org/blog/2015/Specs-grading-report-part-1/), [second post here](http://rtalbert.org/blog/2015/Specs-grading-report-part-2/)) but I wanted to jump ahead a little and put out some information about how I plan to use specs grading in my Fall classes. This could be considered part 6 of the series, I suppose. 

My two courses for the fall are Discrete Structures for Computer Science 1 (two sections) and Discrete Structures for Computer Science 2 (one section). These two courses are very similar to each other. The first course deals with sets, counting, logic, proof, and probability; the second deals with relations, functions, recursion, graphs, and trees. Together they fit to form a comprehensive introduction to the mathematics that computer science majors will need. As I've mentioned before, the demographics bear this out: as of July 6 when I last checked the enrollments, 85% and 87% of the students in the first course and 93% of the students in the second course were CS majors. 

Here is the current version of the syllabus for the first course: [https://gist.github.com/RobertTalbert/70b92330e57672bd0cdc](https://gist.github.com/RobertTalbert/70b92330e57672bd0cdc) The syllabus for the second course is virtually identical, except for the change in the topics and a blurb about how students in the second course should be especially familiar with the basics of mathematical proof. 

Here are the main features of the grading system. To understand these better in context of the rest of the course, read the entire syllabus.

There are two general categories of work that students will do to produce evidence that they've mastered the course objectives: stuff they will do to show they have mastered the subject matter itself, and stuff they will do as daily class activities to show they are _trying_ to master that subject matter and be a functioning part of the class learning community. 

Daily activities consist of three types of items. There is _Guided Practice_ which [I've detailed before](http://chronicle.com/blognetwork/castingoutnines/2014/03/04/the-inverted-calculus-course-using-guided-practice-to-build-self-regulation/) as an important part of the flipped learning experience students will have. There is also something called __Homework A__ which consists of basic (not necessarily easy) problems and exercises that they will do between classes. The Homework A will be written up on paper, then brought to class, at which point they will discuss and correct their work in groups and present their group's solution at the board. Using [Dana Ernst's popular "colored felt tip pen" procedure](http://danaernst.com/felt-tip-pens/) students can make corrections in class to their work while preserving a record of their initial attempts. There are 30 students in the class, so I expect there to be between 8 and 10 groups in each class writing solutions at the board and discussing their work. Students will be expected to contribute as the lead presenter for their group occasionally during the semester. 

So immediately you can see that I am giving these courses [a distinctly IBL flavor](http://www.inquirybasedlearning.org/?page=What_is_IBL), which is something I've been meaning to do for a while. 

These three activities -- Guided Practice, group presentations, and leading presentations -- are all graded on a __Pass/No Pass__ basis with "Pass" meaning that there was a good faith effort to be right, nothing was left blank, and the work is clearly communicated. These contribute to a category I call __Learning Community__. Students have to _certify_ that they have been "positive, caring, and productive members of the learning community" by completing a sufficient number of items at __Pass__ level. Students can _certify at Level 1_ or _at Level 2_ in the Learning Community; Level 2 is distinguished form Level 1 by simply the number of things they complete at __Pass__ level. Generally speaking, if a student Passes all the Guided Practice, contributes to all the group Homework A presentations, and does a couple of presentations themselves, they earn Level 2 with room to spare. Students who complete fewer of the Guided Practices can make up for it by doing more presentations and vice versa. 

Students also have to _certify mastery on course content_ by completing _learning bundles_ throughout the course. Every course topic has a learning bundle at two levels: Level 1 and Level 2. Certifying on a topic at Level 1 means the student has shown evidence of mastery of basic concepts and computations for that topic. Level 2 requires certification at Level 1, plus more evidence of performance at a higher level. 

Students certify on learning bundles in two ways: 

+ By completing an in-class timed assessment covering the tasks that are associated with the bundle. For example, the tasks for the Level 1 Sets assessment will include computing unions, intersections and differences of sets; expressing sets in roster notation and in set-comprehension notation; and a few other basic items. Tasks for the Level 2 sets assessment will contain more complex tasks such as working with infinite unions and intersections. 
+ By completing a set of problems called Homework B. These contain problems that require creative thinking, often programming, to solve. Each bundle will have its own requirements for Homework B; for example if a Homework B set has 8 problems in it, then __Pass__ing 4 out of 8 of those may be required for Level 1, while 7 out of 8 are required for Level 2. 

To certify at Level 1 on a bundle, pass the Level 1 timed assessment and satsify the requirements for Level 1 on the Homework B (whatever those are). To certify at Level 2, first certify at Level 1; then pass the Level 2 timed assessment and satsify the requirements for Level 2 on the Homework B --- and complete what I call a __Big Picture__ item. 

The concept behind Big Picture is that some of the course goals are not just content mastery but also have to do with metacognition, making connections between math and CS, and learning from failure. Basically Big Picture is a big list of stuff that students can do to demonstrate they've satisfied those objectives, to be done as add-ons to their other work. For example a student can choose a "productive failure" activity for the Counting bundle by going to one of their Homework B problems that they didn't pass, but eventually passed through revision, and then discussing where they went wrong on that problem and how they fixed themselves. One thing I'm kind of excited about is that these Big Picture items don't have to be written essays; they can be videos, blog posts, presentations, musicals, etc. or even just office hours meetings. The medium is up to the student. 

Finally -- in addition to _certifying_ on these bundles, students have to _recertify_ at the end of the semester by taking miniature versions of the initial certification assessments. I am setting aside the entire last week of class and the final exam period for recertifications. 

This is an addition that addresses one of the major shortcomings of the specs grading implementations I've used in the past, namely that once students __Pass__ an objective early on, they are never required to revisit it. This led in Implementations 1a and 1b to situations where students would __Pass__ an objective, then accidentally retake the assessment on it because they forgot they passed it, and then failed it on the second try. There is sometimes too a problem where students fulfill the requirements for their grade and then disengage from the course. With recertification, students _have_ to come back at the end of the course and show that they retain some mastery of what they originally Passed. 

As for the way that grades are assigned, that's all included in the syllabus and so you should have a look at that if you want the details. Briefly, to earn a "C" in the class, which is minimum baseline competency, you have to certify at Level 1 on all five topics and then recertify on the first four of those (the fifth one is left out because it comes late in the semester), certify and recertify at Level 2 on one topic of your choice, and be a Level 1 member of the Learning Community. Higher grades require higher levels of certification and recertification as well as higher levels of Learning Community participation. 

Figuring out how to handle plus/minus grades is hard. I tried several times to come up with general rules for when to award a plus or minus until I gave up, because I wasn't happy with any of them. So I ended up just making up separate conditions for each possible plus/minus grade. That adds complexity, but I have a table in the syllabus that I think lays out the requirements for each grade pretty clearly. 

Some things that I like about this iteration of specs grading: 

+ Students are getting a lot of choice as to how they want to satisfy the course learning objectives. 
+ Students have to recertify their content mastery, not just certify it once. 
+ There is a focus not only on content but on _community_. I will have more to say about this later; it's one of the big takeaways from my experience with the online calculus course this summer. 
+ It seems like it ought to be pretty simple to get a C in the course; but earning higher than this requires significant effort. This is the way it should be. Getting lower than a C will require conscious effort; similarly for getting higher than a C. 

Some things that I am not sure about yet: 

+ Will we have time in class to handle all those group presentations? 
+ Will CS majors riot at having to work in groups and present stuff? They are not always the most social lot. 
+ Is the grading load that I am creating for myself sustainable? I think so, but maybe I'm not seeing something. 
+ I am sort of uncomfortable with the "certification" language because it carries some of the baggage of the current debate about higher education, specifically whether higher ed is about more than just certification of skills. However that language does resonate with CS majors, who are familiar with the concept of IT certification (A+, Microsoft, etc.). And "certification" under this system does require more than just a full checklist of procedural skills. 


I want to make sure that I give adequate credit to [Justin Dunmyre of Frostburg State University](http://www.frostburg.edu/dept/math/math-faculty/justin-dunmyre/). I met him at the recent R.L. Moore/IBL conference in Austin where he was giving a poster presentation on his use of specs grading in introductory statistics, and his methods seemed to fill a lot of needs in my own implementation. A lot of what you read in my syllabi is heavily appropriated from his statistics courses. Anything stupid or off the wall is my own contribution. 

So, have a look at all this and let me know what you think, and what I haven't thought of. 