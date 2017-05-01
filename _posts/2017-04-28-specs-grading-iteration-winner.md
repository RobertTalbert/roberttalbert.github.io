---
title: "Specifications grading: We may have a winner"
excerpt: "In January 2015, I launched my first attempt at specifications grading. This semester, I think I finally have something that works."
comments: true
share: true
tags:
  - Specs grading
  - SBSG
---

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/2017-04-28/iteration.jpg" alt="" class="full">


Two and a half years ago, [I decided](http://www.chronicle.com/blognetwork/castingoutnines/2014/12/02/thinking-about-grading/) that the traditional system of grading student work --- based on assigning point values to that work and then determining course grades based on the point values --- was working against my goals as a teacher, and I decided to replace it with [specifications grading](http://www.utimes.pitt.edu/?p=30598). I had just learned about specs grading through [Linda Nilson's book](http://a.co/8aSt6bY) on the subject. This happened right at the end of Fall semester 2014, and I spent the entire Christmas break doing a crash-course redesign of my Winter 2015 classes to install specs grading in them.

I've used specs grading fifteen times since then: once in Cryptography and Privacy, once in Abstract Algebra 2, twice in Calculus 1, four times in Discrete Structures 1, and eight times in Discrete Structures 2. It's fair to say that my implementation has been battle-tested and has undergone a fair bit of evolution in that time. The first attempt in Winter 2015 was pretty rough, but very promising. Every semester since then, I made changes and updates to try to address issues that students and I noticed.

But it was only this last semester, the one that just concluded this week, where I felt that at every point during the semester --- from day 1 all the way through turning in course grades yesterday --- the specs grading system I had in place was working the way I wanted. It's still not 100% there, of course, but I think I have a blueprint of how to use specs grading moving forward[^1] and of course, I want to share it with everyone.

## What is specs grading?

In specifications grading, instead of using points to assess student work, the work is graded on a two-level rubric --- that is, some variation on Pass/Fail or Satisfactory/Unsatisfactory. Instructors craft a set of specifications or "specs" for assignments that define what Satisfactory work looks like. When the work is handed in, the instructor simply categorizes it as Satisfactory or Unsatisfactory depending on whether it meets the specs or doesn't. There are no points, so there is no partial credit. Instead, instructors give detailed feedback on student work, and specs grading includes giving students the opportunity to revise their work based on the feedback, and submit a revision as an attempt to meet specs.

Specs grading still uses an A/B/C/D/F course grade reporting approach, but the letter grades are earned differently. Rather than calculating complex weighted averages of points --- which you can't do because there are no points --- letter grades are earned by completing "bundles" of work which increase in size and scope as the letter grade being targeted goes higher. The idea is that students who want a "C" in the course have to do a certain amount of work that meets the specs; those wanting a "B" have to do everything the "C" people do, but more of it and of higher quality and/or difficulty level. Similarly the "A" students do everything the "B" students do plus even greater quantity and quality.

Done right, specs grading allows students choice and agency in how and when they are assessed; students are graded on what they can _eventually_ show that they know, and they get to learn from mistakes and build upon failures; their grades are based on actual concrete evidence of learning; and the grades themselves convey actual meaning because they can be traced back to concrete evidence tied to detailed specifications of quality. The instructor often saves time too, because instead of determining how to allocate points (which takes more time than you think), she just determines whether the work is good enough or not, and gives feedback instead.

## My grading philosophy and the overall setup

The specs grading setup I am going to describe here is for Discrete Structures 2, a junior-level mathematics course taken almost exclusively by Computer Science majors. It's the second semester of a year-long sequence and it focuses on mathematical proof and the theory of graphs, relations, and trees. I think that much of the structure I am going to describe here could be ported to other math classes, though.

My overall belief about the course grade in this class (and in others) is that grades should be based on _concrete evidence of student success_ in three different areas:

1. Mastery of **basic technical skills**;
2. Ability to **apply basic technical skills and concepts to new problems**, both applied and theoretical; and
3. **Engagement** in the course.

Some people may debate whether or not "engagement" ought to be part of the grade. Personal experience with this course tells me that it should, in this case. What I mean here is not just attendance in class, but also preparation for class, active participation during class, and enagagement in the course outside of the class. I want students to treat the course as a high priority and engage with it as such.

If these are the things I want from the course, then I need to set up stuff for students to do and submit to me that will allow me to measure whether or not they are progressing or succeeding in those areas.  

For basic technical skills, I combed through the course and decided on a list of 20 basic skills that I felt were essential building-block skills for the course. Those are called **Learning Targets**. These were keyed to the four major topics in the course (proof, graphs, relations, trees). Here are a couple:

>**P.2:** I can identify the predicate being used in a proof by mathematical induction and use it to set up a framework of assumptions and conclusions for an induction proof.
>
>**G.6:** I can give a valid vertex coloring for a graph and determine a graph's chromatic number.

[Here's the full list](https://gist.github.com/RobertTalbert/30a00ecce9a91ec3d21c8e818831480f). Notice these are phrased in terms of concrete action verbs that produce assessable results.

For ability in application of these basic skills, students were given a series of **Challenge Problems**. These are problems that require students to apply what they learned about the basic skills and included a mix of "Theory" problems that involved writing proofs, programming assignments where students had to write Python code to solve a problem, and real-world applications. I started with a core of ten Challenge Problems but also wrote some more during the semester as I got inspired, and we ended up with 17 of these total. [Here's one](https://drive.google.com/file/d/0B3oyKFhpi58RLTVjRUIwQVJia2M/view?usp=sharing) that involved doing some proofs by induction. Another had students write a Python function that would compute the composition of two relations on a finite set. Another had students use Python code to experiment with a class of graphs, make a conjecture about their [clustering coefficients](https://en.wikipedia.org/wiki/Clustering_coefficient), and then prove their conjecture.

Finally, for engagement, I broke from the specs grading mold and used points, or what I called _engagement credits_. Students accumulated engagement credits through the course for doing things like completing their Guided Practice pre-class work on time and participating in class on certain days (especially the days close to breaks). Basically this was a way of incentivizing student work on the course for things that I needed them to do, especially outside of class.

I also had students take a final exam in the course, that I'll describe in the next section.

## Assessing student work

Each of these three areas above were assessed in pretty different ways.

The Learning Targets were assessed using short quizzes called _Learning Target assessments_. I set aside every other Friday in the course for students to take Learning Target assessments as well as a few extra days during the semester. [Here's an example of the assessment for Learning Target P.2](https://drive.google.com/open?id=0B3oyKFhpi58RTllmY2dfem10U2M) and [here's the one for G.6](https://drive.google.com/open?id=0B3oyKFhpi58RTkZEOUkyVHNTZ1U). Notice they are simple tasks that deal directly with the action verb in the Learning Target.

Students could come on these Fridays and take as many or as few of these Learning Target assessments as they wanted. Only the Learning Targets that we'd discussed in class were available, but once they were available they were _always_ available. Previously-given Learning Target assessments would have new versions of the same problem available to do. So a student who didn't feel ready to be assessed on Learning Target G.6 didn't have to take the assessment for G.6, but just wait two weeks and try it then.

Learning Target assessments were graded **Satisfactory/Unsatisfactory** according to specifications that I determined, and those specs are at the bottom of each Learning Target assessment so it's very transparent for everyone. If student work was Satisfactory, I just circled the "S" at the top of the page, and circled "U" otherwise.

Challenge Problems were _not_ graded Satisfactory/Unsatisfactory but rather using the [EMRN rubric](https://drive.google.com/file/d/0B3oyKFhpi58RdzN2VlpOMll5ckE/view?usp=sharing), which is a modification of the [EMRF rubric I wrote about here](http://rtalbert.org/blog/2016/specs-grading-emrf).[^2] "Pure" specs grading would say that I should not make things so complicated, and just use Satisfactory/Unsatisfactory with a high bar set for Satisfactory. But I've found that in math classes, written work is hard to get right and students get easily discouraged, so I felt there should be some detail added to the 2-level rubric to distinguish between Satisfactory work that is excellent versus merely "good enough", and Unsatisfactory work that is "getting there" versus that which has major shortcomings. Students would submit their Challenge Problems as PDFs or [Jupyter notebooks](http://jupyter.org) on Blackboard; I'd grade it there and leave feedback, then students could revise (see below).

Importantly, there were [no recurring deadlines on Challenge Problems](http://rtalbert.org/blog/2016/a-farewell-to-deadlines). Instead, students were allowed up to two Challenge Problem submissions per week (Monday--Sunday) which could be two new submissions, a new submission and a revision, or two revisions. The only fixed deadline for Challenge Problems was 11:59pm on the last day of classes, after which no submissions of any kind were accepted. This helps keep students from procrastinating until the end of the semester and dumping a ton of Challenge Problems into the system all at once. (Although there were issues with this; keep reading.)

Engagement credits were given for a variety of tasks, so whenever there was a task given out that could earn engagement credit, I'd just explain what it takes to earn the engagement credit and go from there.

At the end of the course students took a final exam. The final exam consisted of eight randomly selected Learning Target assessments that were given previousy in the course along with a final question for feedback on the course. The Learning Targets were selected so that at least one Learning Target from each of the four main course topics was represented. I'd never given a final exam in a specs grading class before this semester; in past classes, the final exam period was set aside as one more session for any student who needed to pass Learning Targets to have a chance to do so. I instituted the final exam this time because I wasn't satisfied that the combo of Learning Target assessments plus Challenge Problems was giving me reliable data about student learning. I was getting students who would pass a Learning Target early in the course, then forget that they had done so, and "accidentally" retake that Learning Target later... and not pass it. So I wanted to have one additional layer of assessment to get students to recertify on the basic skills at the end of the course. The fact that all I was doing was recycling old Learning Target assessments made this easy to make up, by just randomly selecting the Learning Targets and assessment versions and then merging the PDFs. (I made four different versions for test security.)

I broke again from the specs grading mold and graded the final using points, grading each recycled Learning Target with either 0, 4, 8, or 12 points. A 12-point score was given if the work would have earned Satisfactory marks according to the original specs, 8 if it was "almost Satisfactory", and so on. The feedback questions were given 4 points, bringing the total to an even 100 points.


## The revision process

As in all specs grading courses, almost all student work of consequence could be revised in some way.

Learning Target assessments could be "revised" by retaking them, either at a subsequent Learning Target assessment session on Friday, or by scheduling a 15-minute appointment in the office to do it orally. There was no limit on the number of times students could retake Learning Target assessments, but there _was_ a limit on office hours appointments: no more than twice a week, for 15 minutes each, and no more than two Learning Targets attempted per 15-minute session, and appointments had to be scheduled 24 hours in advance. Also, students had to try the Learning Target on paper first before doing it in the office. This was a policy purely to keep the number of office hours visits for Learning Target revisions down to a reasonable level.

For Challenge Problems, students could revise any Challenge Problem that received an "R" or "N" grade just by submitting a new version on Blackboard that addressed the feedback I gave. There were no limitations on the number of times students could revise Challenge Problems other than the two-submissions-per-week rule, and the fact that any Challenge Problem work that earned "N" required students to spend a token to revise.

What's a "token"? A token in specs grading is a sort of "get out of jail free" card that a student can spend to bend the rules of the course a little. Every student in my course started with five tokens. By spending a token, a student could purchase a third submission of a Challenge Problem in a given week (but these couldn't be "stacked", for example to get four submissions in a week for two tokens), to purchase a third 15-minute oral revision session in a week, or to purchase five engagement credits.

There were no revisions available for Guided Practice, the final exam, or any item that earned engagement credits.


## Assigning course grades

The "specs" part of this system so far has come from the Satisfactory/Unsatisfactory rubric and EMRN rubric used for grading Learning Target assessments and Challenge Problems. Most of the engagement credit-earning items were also graded Satisfactory/Unsatisfactory. Specs grading also has to do with the assigning of course grades, and here is how it worked in my course.

First of all, let's distinguish between the **base grade** for the course and the **modified grade**. The base grade is just the A B, C, D, or F that a student earns. The modified grade is the base grade modified up or down by a plus or minus. Course grades were determined by a simple two-step process.

The _base grade_ in the course was determined using this table:

| To earn this grade: | Accomplish the following: |
|:------------------: | :-------------------------|
| A | Earn **Satisfactory** marks on **19** Learning Targets; _and_ complete **10 Challenge Problems** with at least an M mark, including at least five "E" marks.  |
| B | Earn **Satisfactory** marks on **17** Learning Targets; _and_ complete **7 Challenge Problems** with at least an M mark, including at least three "E" marks.  |
| C | Earn **Satisfactory** marks on **15** Learning Targets; _and_ complete **5 Challenge Problems** with at least an M mark. (No "E" marks required.) |
| D | Earn **Satisfactory** marks on **13** Learning Targets. (No Challenge Problems required.)  |

So the base grade in the course is entirely determined by three points of information: (1) how many Learning Targets you pass, (2) how many Challenge Problems you pass, and (3) how many Challenge Problems show excellent work. (An "F" grade is awarded if a student doesn't complete the requirements for a "D".)

The grade of "C" is considered "baseline competency", and to earn that grade you have to complete the "C bundle", which is passing 75% of the Learning Targets and completing five Challenge Problems, with no requirement of excellent/exemplary work required. The "B bundle" is everything in the "C bundle" with more Learning Targets passed and more Challenge Problems completed plus some evidence of excellent/exemplary work. The "A bundle" is likewise everything in the "B bundle" with even more Learning Targets and Challenge Problems completed plus even more extensive evidence of excellent/exemplary work. Notice, students get to choose which Challenge Problems they attempt -- we had 17 Challenge Problems in all and students just picked the ones they liked[^3].

Additionally, students targeting an A or B grade in the course had to complete at least one "theory" oriented Challenge Problems with an E or M grade (i.e. successfully write a proof for a mathematical conjecture) or else the final grade was lowered by one-half letter.

If the only grade we awarded were these five letters, this would be extraordinarily simple. But we also award plus/minus grades, and so I had to add rules into the system for how this works. I chose to approach this by awarding plus/minus modifications on the basis of the final exam and on engagement. The base grade was raised by a plus, lowered by a minus, or lowered by an entire letter as follows:

+ Add a **plus** to the base grade if you earn at least **60** engagement credits *and* earn **at least an 85%** on the final exam.
+ Add a **minus** to the base grade if you earn between **30 and 39** engagement credits (inclusively) *or* earn  **between 50% and 69%** (inclusively) on the final exam.
+ Lower the base grade **one full letter** if you earn **fewer than 30** engagement credits *or* earn **lower than 50%** on the final exam.

So, students' _base grades_ are determined by the really important stuff in the class --- basic skills and the ability to apply them. Those base grades earn plus/minus grades by their performance on the final and their engagement in the course. There was some insulation in place in case a student did poorly on the final or had low levels of engagement, but it would still affect their grades. Note that there's a "safe zone" cutoff here of 70% on the final and 40 engagement credits. Students who do this well are immune from their base grade being penalized.

In my view, the whole plus/minus system here fouls up what it otherwise a beautifully simple grading system, but according to the Dean's office I _have_ to have some plus/minus system in place. This is the best I could come up with.

To help students keep up with this, they were given two visual aids. First there was [this scorecard that they could use to track their progress on their base grade](https://drive.google.com/file/d/0B3oyKFhpi58RY29vRHhwLTR4X28/view?usp=sharing) --- just check off or fill in the boxes as the semester progressed. Then, to navigate the plus/minus system, there was [this flowchart](https://drive.google.com/file/d/0B3oyKFhpi58RaEFQYVgxV3RyQkE/view?usp=sharing) that got students from their base grade to the final grade in just a few questions.

## How it turned out

I haven't gotten back evaluations for this course yet, so I just have verbal feedback and mid-semester surveys to go on. But based on what I have, students were totally thrilled by this system. They remarked about how it took a little while to get used to it, but once they "got it" they wished that all their other courses did the same thing. Computer science majors in particular --- who make a career out of determining how to debug their code from feedback given by the compiler --- really resonate with the idea of being able to debug their math work by using detailed feedback. I've been contacted by at least one other professor in the CS department here who's had students from my course talk about how much they appreciated it and how much it helped them learn.

For my part, I could definitely see students learn in ways that traditional grading, with its one-and-done approach to assessing skills, simply doesn't support. Students' ability with proof especially benefitted. Most of my students had _seen_ proof in their first-semester class because that's a required topic, but their proof skills were virtually non-existent in my class.Their first attempts were usually pretty sad. But with feedback and office hours visits, they kept at it, and eventually almost everyone was able to whip at least one induction proof into shape, and could demonstrate skills with proof through Learning Targets P.1--P.4. A few became really fascinated with induction proofs and did several of these on their own free will.

I really liked the _simplicity_ of this system as well, with the base grade determined by a simple lookup on a four-line table and the modifications done with another similar table. My past attempts at specs grading were detailed but tended to be like Rube Goldberg machines, sort of bloated and complicated. I was really going for simplicity and minimalism this time, and while again the plus/minus system messes this up somewhat, I was still very happy with the results.

I also liked that this system focused student conversations away from points and the grubbing of points and toward content and knowledge. I never heard anything like, "_I need to earn an 86.2 on the last test in order to bring my average up to a B_". Instead I heard conversations like, "_I need to complete one more Challenge Problem to get a B, should I focus on applications of graph theory or writing code to implement a relation?_" or "_I've taken Learning Target P.3 three times without success and it's because I don't get structural induction --- can we talk about that?_"

Likewise, this system inverts the way students tend to approach the course as a whole, that is by coming to class without a clear idea of what they want out of it and just hoping for the best. Here, students have to think about the grade they want to earn _first_, then this tells them which "bundle" to look at in the syllabus and this lays out an agenda for what they need to accomplish in the course. There is no "hoping for a grade"; the student is in control and we talk about _targeting the grade you wish to earn_ instead of hoping for the grade you think you "deserve".

This was the first time I'd tried oral revisions of Learning Targets in the office and I thought that was a great success, especially on proof-related targets where students could just _talk_ through the problems rather than writing so much down. I think in some cases I got much better information about student learning by talking face-to-face with them rather than reading their writing.

I also think the final exam was good for providing that extra layer of assessment that allowed me to triangulate my data about student performance from the Learning Targets and the Challenge Problems, and students couldn't just clock out of the course once they'd reached the requirements of their chosen grade bundle.


## What I will do differently next time

I continue to believe that doing away with recurring deadlines for Challenge Problems is a good idea and student work is better without them. At the same time, students really struggled with procrastination. Although I had measures in place to help with this[^5], by the end of week 9 in a 14-week semester, the median number of _submissions_ of Challenge Problems --- not Challenge Problems passed, but _submitted_ --- was _one_. Therefore the vast majority of students were still cramming in Challenge Problems during the last three weeks of class; I received 75 different Challenge Problems to grade over the weekend of week 12 for instance. I eventually dug out from under the grading, but procrastination cost some students a passing grade. So while I'll continue this quota/single deadline system in the future, we all need to take procrastination more seriously.

The final exam helped eliminate false positives in the course, but next time I'm going to make the final contain not only old Learning Targets but also some conceptual questions, to get data on students' conceptual understanding and not just basic technical skill. For example I had some students who could perform [Warshall's Algorithm](https://en.wikipedia.org/wiki/Floyd%E2%80%93Warshall_algorithm) but I am not sure they know what this algorithm does or why it works.

Finally, while I'm convinced this specs grading system isn't more complex than traditional grading systems, it's quite different, and it requires that students really take a consistently hands-on approach to the class by learning the system, reading the syllabus carefully, and paying attention to announcements and calendar events regarding graded work. Unfortunately this is by far my students' weakest link --- managing information streams, projects, calendar events, and tasks. I feel like there should be a course-within-a-course here that includes some basic GTD training and accountability for staying current with course info, because failure on this front absolutely destroyed some students.

---

To conclude here: I am a convert to specs grading and I do not see myself going back to traditional grading anytime soon. It's just too good. I still hate grading like everybody else, but at least now when I grade, I am giving feedback to students rather than splitting hairs over points, and it's really changed the dynamic of my classes for the better.

For those who are interested, [here is the syllabus for the course with all the details](https://drive.google.com/file/d/0B3oyKFhpi58RVExMNFpleUVoRlk/view?usp=sharing) (yes, I actually left stuff out in this post).

Now, ask me some questions about this.

---

Image credit: Nick Hughes, "iterations" https://goo.gl/LH6YHS

[^1]: My next class isn't until Fall 2018 because of [my sabbatical](http://rtalbert.org/sabbatical), so I need this post for myself, too, to help me remember how to do this 15 months from now.

[^2]: I changed the "F" to "N" because the letter "F" in my opinion is so emotionally loaded for students that it simply cannot be used in any context for grading any more. I could make the top grade "F" for "Fabulous" rather than "E" for "Exemplary" and students would still think they failed. The letter "F" is done in education.

[^3]: Which in practice often turned out to be the ones they felt would be easiest. Some definitely looked for the easy way out. But most students found they gravitated toward certain kinds of problems and developed a real interest in those topics because _they picked them_.

[^4]: We did have a syllabus quiz, for engagement credit, during the first week of class and syllabus review items sprinkled into assignments in the course, but that wasn't enough for some.

[^5]: For example I set up "incentive checkpoints" that awarded engagement credit in big chunks for finishing a certain number of Challenge Problems and Learning Targets by certain points in the course, and the only way to earn a plus grade in the course was to hit at least one of those checkpoints.
