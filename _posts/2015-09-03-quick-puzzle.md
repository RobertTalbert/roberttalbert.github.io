---
layout: post
title:  "A selection puzzle that sheds light on human thinking"
date:   2015-09-03 17:27:11   
author: Robert Talbert
tags: 	teaching
---

One of the hardest days of the semester in my view is the first day. It's difficult to plan. I'm not a big icebreaker guy because I don't care for small talk. I think it's wasteful to go over the syllabus (make a video instead). But I also don't like jumping right into the course material because the enrollment in the class is in flux, and people who join the class later will get behind. So I want to do something with students that motivates the big ideas of the course and gets them engaged with each other. Those are hard to come up with. 

Fortunately, this past summer a former student of mine emailed me an article that had an idea that from the moment I saw it, I knew I wanted to try it during the first couple of days of my three Discrete Structures for Computer Science courses this fall (which started on Monday). This is a two-semester sequence, and I'm teaching two sections of the first semester and on section of the second. 

The activity comes in two parts. 

### Part 1

Below are four cards lying flat on a table. Each card has a single-digit number on one side and one of two colors (blue or green) on the other side. The first and second cards you see show a 5 and an 8. The third and fourth cards are blue and green respectively. 

![Cards]({{ site.baseurl }}/assets/Wason.png)

Now consider the following statement:

>If a card shows an even number on one face, then its opposite face is blue.

Question: __Which cards must you turn over in order to test the truth of this statement, without turning over any unnecessary cards?__ 

Students were seated at square tables in groups of 4 and had the above on a sheet of paper along with a 4x4 grid with all 16 possible choices for which cards to turn over. I gave them three minutes to think about this task silently to themselves, and then they marked the box in the grid with their choice. I collected these and tallied up the class' responses while they went on to Part 2. 

### Part 2

Now suppose you're a police officer in a bar[^bar_fn] looking for underage drinkers. The rule you are following is: 

>If a person is drinking beer, then that person must be over 21. 

You see four people, and through prior investigation you know the following information about each of those four people: 

![Drinkers]({{ site.baseurl }}/assets/Wason2.png)

Question: __Which people do you need to check to make sure the rule is being followed?__

Again, I gave the students three minutes to make their choices before we moved on to the discussion and debrief. 

### The Results and Discussion 

When the three minutes were up, I let them talk about their reasoning with each other while I tallied up all the responses from the class to the number/color card question. Those responses were all over the place. In the first semester courses (both sections) there was a wide spread of responses covering about 2/3 of the possible choices, and nowhere near a majority on any one item. __Only 5 people (out of 30) voted for the correct answer in one section and only 7 in the other (also out of 30).__ In the second semester course, the responses were a lot more uniform -- __15 out of 32 voting for the right answer__, and the other 17 spread over only 3-4 different responses. In either case though --- __the majority of students were not getting the correct response__. And in the full class discussion, even when a student was able to explain his reasoning clearly, other students seemed skeptical. 

But when we switched to the underage drinking question, it was like night and day. In the first semester courses between 75% and 85% of the students were getting the right answer; in the second-semester course it was nearly everyone. And they were able to explain their reasoning with ease -- in fact they thought the right answer was obvious and needed no explanation. 

### The Punchline

The punchline, of course, is that __these two problems are exactly the same except for the context__. The "right answers" are even given in the same positions in the graphics. And yet the differences lead to quite different results, and give some very interesting insights into how we think and what we need to think more clearly. 

Of course, I didn't make this activity up. [This is a classic psychology experiment known as the Wason selection task](http://nautil.us/blog/the-simple-logical-puzzle-that-shows-how-illogical-people-are). When Peter Wason ran this experiment, 90% of his subjects responded incorrectly to the number/card version of the task. Not only this, when shown the correct responses, his subjects said that _they would choose the same cards again if asked_. This led Wason and subsequent researchers to theorize that the human brain tends to cut corners when confronted with an abstract task --- which should come as a surprise to nobody, but it has serious implications for students wanting to become mathematicians, statisticians, or computer scientists like my students. 

The underage drinking version of the task was made later, in 1982 by psychologists Richard Griggs and James Cox. In their study, 75% of the subjects chose the correct response. The same logical rule underlies both versions of the task, but when put into a familiar context, the brain becomes much better at applying this rule. 

I told the students that this activity highlights at least three things. 

1. It highlights the need for _structures_ -- hence the name of the course -- to help us reason clearly about abstractions. I think it's no coincidence that the second-semester students, who studied logic during the first semester of the course and who have generally a lot of experience applying logic to engineering and programming, showed higher success rates on the card version. They have a _structure_ that supports their brains when it wants to cut corners. 
2. It strongly highlights the importance of _context_ when dealing with abstraction. Yes, we need to study the mathematics in the course on its terms, with proper notation and whatnot. But the results of the task, and of the psychologists' studies, strongly suggests that we will make a lot more meaning out of the mathematics if we couch it in familiar terms. 
3. More technically, it illustrates a common problem-solving technique especially prevalent in discrete mathematics, which is to map the current problem onto a more familiar one, solve the more familiar one, and then map it back. 

Personally, this experiment also reminds me that __mathematics often has as much do to with psychology as it does with logic__. For example, deciding whether a theorem has been proven usually is the result of a process of persuasion, rather than as the outcome of an emotionless calculation. We don't typically decide that mathematics is correct against our wills. So it's smart to pay attention to the human element when writing mathematics or writing code. 

Finally, this is a fun exercise to turn into a recurring character in the course. The next time students want to believe that the converse of a conditional statement is equivalent to the statement, I'll ask them: If I see a person who is over 21, should I arrest him if he's not drinking? 

PS: I never told you the answers. Discuss in the comments. 

---

[^bar_fn]: There was some discussion here among some of my friends because in some places, people who are underage are not even allowed into bars. We're assuming that they are. 