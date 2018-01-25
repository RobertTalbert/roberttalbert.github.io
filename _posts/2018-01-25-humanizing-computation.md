---
title: "Humanizing computation"
excerpt: "Mathematics education needs an update in its ideas about the role of hand computation: Let the human do human things, and the computer do computer things."
comments: true
share: true
tags:
  - Teaching
  - Mathematics 
---

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/brain-2750415_1280.png" alt="" class="full"> 


As most readers know, [I am on sabbatical](http://rtalbert.org/sabbatical) through May, and then I do not teach again until August. When I finally return to the classroom, I will have been gone 15 months from teaching in a formal setting -- a very long time by anybody's metric. But it doesn't mean that I'm not teaching _informally_. This, I do on a regular basis with my three kids who are in the third, sixth, and eighth grades. And a conversation I recently had with my oldest, on a math subject that was giving her some difficulty, served as a message to remind me about my own teaching philosophy here in this long working vacation from formal teaching. 

She was learning about systems of linear equations -- for example where you're given $3x + y = 2$ and $x - y = 6$ and you are supposed to determine whether there is a single $(x,y)$ pair that satisfies both at the same time, and if so then to find that pair. (In this case, there is such a pair, namely $x = 2, y = -4$.) This wasn't coming easily for her, especially "story problems" where she was given a verbal description of a situation and she has to represent it as a system of linear equations, _then_ solve it and interpret the results. This homework session turned into an hour-long working meeting in my home office. Afterwards, I started a conversation with her about where this concept of linear systems leads. It went a little like this:

---

**RT**: You know, I teach about this stuff at the university. There are a lot of cool applications. 

**Daughter**: What's it like?  

**RT**: Well, for example we think about, what if there aren't *two* equations with *two* variables, but three equations and three variables? Or ten equations and ten variables? Or 100 equations and 75 variables? Because the stuff we use the math on, is pretty complicated. It's called [linear algebra](https://en.wikipedia.org/wiki/Linear_algebra). 

**D**: Whoa! That sounds hard. There must be a million steps you have to do. 

**RT**: Well, we don't do it exactly the way you just did it [_by solving one equation for a single variable, plugging the result into the other equation and solving for the single variable, and then back-substituting --- a.k.a. the [method of substitution](https://www.mathportal.org/algebra/solving-system-of-linear-equations/substitution-method.php)_] because that method doesn't work very well on bigger systems. So instead we have a thing called a "matrix" that we can use to hold all the parts of a system, and then [a method](https://en.wikipedia.org/wiki/Gaussian_elimination) that a computer can run that can easily find solutions even for huge systems. 

**D**: So, you're saying that you teach people how to use computers? 

**RT**: [_pause_] Well, I do, but that's only part of it. **I teach people how to use their brains and how to use math, to take word problems and turn them into something that a computer can use, and then use a computer to find answers and then how to interpret what those answers mean**. 

**D**: Because the computer can't read the problem and figure it out on its own. 

**RT**: Exactly. 

---

What I just explained to my daughter here is called [computational thinking](https://en.wikipedia.org/wiki/Computational_thinking), and our conversation reminded me that computational thinking is central to how I think about teaching and learning. In a computational thinking environment, learners approach authentic, complex problems phrased in natural language. Then they use mathematical concepts to interpret those problems in a way that make them amenable to computation using a computer. Then those computations are done, using a computer, and the human then looks at the results and draws conclusions and makes interpretations. 

It's not that I think that hand-computations, like being able to solve a system by hand, are unimportant. When I teach linear algebra, where linear systems are studied in depth, students are required to show that they've mastered the ability to solve 2x2 and 3x3 systems by hand as part of their course grade. But once they've mastered this, they aren't required or even expected to do this again --- they are to use a computer instead. Why? **Because humans are meant to do human things, not computer things**. The human element of linear algebra is the hard part: Translating a complex, often ambiguous description of a problem into terms that accurately represent the problem in the form that allows computer analysis, then doing the computer analysis and figuring if the results mean anything, and if so, what.   

I tend to think of mathematical algorithms, whether it's in linear algebra or calculus or anywhere else, in the same category as any kind of algorithm. There is some value in carrying out these algorithms by hand, namely to the extent that they help the learner reason mathematically _about_ the algorithms. Beyond this, doing hand computations is for recreation only. When I teach sorting algorithms in my discrete structures class, it's done with the understanding that computers will do all the sorting --- it's the human's job to understand the concepts of the sorting algorithm and to reason about it, for example to understand why [bubble sort](https://en.wikipedia.org/wiki/Bubble_sort) is $O(n^2)$ while [merge sort](https://en.wikipedia.org/wiki/Merge_sort) is $O(n \log n)$. I like for those students to first use the algorithms to sort analog objects, like shuffled decks of cards of increasing size, to get the algorithm "under their fingers" and to literally _feel_ the complexity of each. But nobody expects computer scientists to do this sorting by hand except for fun; that's why God made computers. The computer scientist instead is there to reason about problems and to know why sorting is needed in the first place, and which algorithm is best, and how to use the results.

It's the same with mathematical computations: **Let the human translate the problem using their brains and using math into a form that a computer can work with. Then let the computer compute. Then let the human do what's uniquely human, which is to determine the validity and meaning of the result.** 

This is hardly a new idea. Seymour Papert championed this concept in [_Mindstorms_](http://a.co/cdDYDY8) and took it several steps further, arguing that kids should be learning mathematics _by_ programming computers. But in the nearly four decades since that book was published, the message hasn't significantly penetrated either the K12 or the college curriculum. I think it's time for math educators to change that. You can start with any mathematics course, and the best ones are the ones that seem inextricably linked with hand computation --- like Calculus. Here's an example of an activity I often give to Calculus students. 

>Pick a large city near where you grew up and get population data for that city going back to 1980. In 2017, was your city growing or shrinking? How fast? If it was growing, how long will it be until it hits a population of 10 billion people? If shrinking, how long until there is nobody left in the city? Bonus: Explain what, if anything, is wrong with your answer to the last question. 

You have to have a reasonably sound idea about calculus to even know that this could be seen as a calculus problem at all --- you cannot just think of calculus as a collection of algorithmic rules. There are multiple ways to attack this problem. You could plot the data on [Desmos](http://www.desmos.com) or in a spreadsheet and get a best-fit curve for it (Human questions arise: *Which curve? Is linear good enough? Quadratic? What are the tradeoffs for using higher-order polynomials versus something else?*) and then take the formula for that curve and differentiate it using computer software. Or, you could use the data to get an approximation. (Human question: *What if the only population data you have are census data which are collected only every 10 years?*) Then you have to figure out how to frame the question about future population mathematically --- solving it with a computer is not the hard part. Then, you have to think about the limitations of the answer to that question. 

Anybody who says that a student who can work through this series of questions and share their thinking in a clear and coherent way isn't "doing calculus" needs an update to their definition of "doing calculus". Again, if the ability to take derivatives by hand is important, and I think it is at least a little important, then this can be done elsewhere, for example through gateway exams or as part of a standards-based grading package. But, let the human do human things and the computer do computer things. 

Computation is computation no matter where it's found. Learn it by hand to the extent that it helps you reason about it, and come to a strong understanding of the algorithms that govern it. But then let the computer do it and focus on the human part instead. Unless, like me, you find doing hand computations to be relaxing --- in which case, enjoy it as much as you want! 

Image: https://pixabay.com/p-2750415/?no_redirect 
