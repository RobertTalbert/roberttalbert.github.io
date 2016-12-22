---
layout: post
title:  "My workflow for creating Guided Practice assignments in 5 somewhat easy steps"
date:   2015-07-08 13:24:57   
author: Robert Talbert
tags: 	workflow
---
As I think most people who read this blog know, all of my classes are designed and taught using a flipped learning methodology that places a premium on students having significant learning experiences before the entire class as a group works on anything. The assignments that I give students to guide them through these primary-engagement experiences I call "Guided Practice", and [I've written at length on how I design these and the theory on which they are based](http://chronicle.com/blognetwork/castingoutnines/2014/03/04/the-inverted-calculus-course-using-guided-practice-to-build-self-regulation/). 

I'm making out the assignments for next week's Calculus class, and I thought I'd do something a little different and write about the process of how I actually make and deploy these, as well as how students submit work, from a technical how-to point of view. 

## Ingredients 

First of all, the steps I'll detail are assuming a Mac environment. I think a lot of this can be ported easily to other platforms though. You'll need: 

+ A text editor capable of working with [Markdown](http://daringfireball.net/projects/markdown/) and a knowledge of Markdown (or at least a willingness to learn)
+ A web browser and internet connection
+ A terminal app and modicum of comfort level using the terminal
+ [Pandoc](http://pandoc.org/), which you can install [here](http://pandoc.org/installing.html)  
+ Google Drive
+ [Bitly](http://bitly.com) or some other URL shortening service 

For my students, Guided Practice assignments are deployed as simple, unformatted HTML files posted to the web. [Here is an example of a finished product](http://mth201.proftalbert.com/gp/gp31.html) that was actually used last week in my class. Now let's go through the building process one step at a time. 

## Step 1: Make the Guided Practice base file 

__Each Guided Practice starts as a basic Markdown file.__ [Here is the template that I use](https://gist.github.com/RobertTalbert/378fbf6e390d8ae97011) in case you need a starting point; you'll need to click on the "Raw" button to see/copy the actual Markdown code. You can copy this if you want and save it, then rename it once you've added content. 

For me, I use Sublime Text (it's one of the few paid apps on my Macbook and the price tag is _totally_ worth it) and I have this entire Markdown file saved as a snippet. When I'm ready to write, I open a new file, type `gp` and then hit `Tab` and boom, there it is, and I can tab through the various entries as I add text. Saves time. 

Note that the base file has the parts that fit with my theory behind Guided Practice. Obviously you should modify the template if you do things differently. 

We're using Markdown because it's very easy to structure the document and format the text without bloating the file up. If you need to format your text using bold, italics, or strikethrough, [there's simple Markdown syntax for that](http://daringfireball.net/projects/markdown/basics). There is also Markdown syntax for including images, links, and even tables. 

Important note: This file is eventually going to be turned into an HTML file. So if you need to include some HTML, go ahead. For example, you can put embed code in the file for things like Geogebra applets ([here's an example from my class](http://mth201.proftalbert.com/gp/gp16.html)) or YouTube videos. If you want to include math notation, we're going to use [MathJax](https://www.mathjax.org/) when we convert the file. MathJax is a program that renders LaTeX using a server-side Javascript engine, so there's nothing to install and you just use the usual dollar-sign delimiters to go into math mode. 

[Here's the raw Markdown for one of our earlier Guided Practices](https://gist.github.com/RobertTalbert/f3f269e6d7d75c7e34cc) that has straight text, Markdown formatting, embed code, and LaTeX all living in the same place. Again, click the "Raw" button to see the unrendered, raw Markdown. 

Once you've added all your content, save the file using a `.md` file extension. For the purposes of this example, let's suppose we have created the file `gp35.md` (maybe Guided Practice for Section 3.5 in the book). 

## Step 2: Create the response form and get a link to it

The next step is to create a form for students to submit their work and questions on the Exercises section of the Guided Practice. [Google Forms](https://www.google.com/forms/about/) is the go-to tool: simple and free to use, and useful for archiving and analyzing student data. 

I use a template for Guided Practices that looks like this: 

![Guided Practice template]({{ site.baseurl }}/assets/gptemplate.png)

To create a new instance, make a copy (so as not to overwrite yout template), change the title (by clicking on it and editing the text), then add however many other blanks you need. I keep the first blank (family/last name) and last blank (any other questions?) intact on each assignment. For the exercise responses, you can use short text, paragraph text (as I have here), multiple choice, etc. -- Google Forms are super flexible in the kinds of questions you can ask. To save time I usually don't elaborate on the header for the exercise responses; they just say "Response to exercise 1:", "Response to exercise 2:", etc. because the exercises themselves are back on the Guided Practice form. 

The form you make here is not what students fill out. To see the _real_ form,  click on "View Live Form" in the menu bar, and you'll see something like: 

![GP form]({{ site.baseurl }}/assets/gpform.png)

This is the actual form that students will use. We can simply copy the URL for this page and push it out to students, but notice that the URL is a mile long. It helps to shorten it. So copy the URL; then go to `bitly.com` or your favorite URL shortener and get a shortlink for it. Make sure to go back to the last line of the base Markdown file and put a link to the response form and re-save the base file. Then, we're good to go on to the next step. 

## Step 3: Convert the base file to HTML

Now we're going to convert the base file from Markdown to HTML using MathJax to handle the math notation. This is the shortest step but possibly the most mysterious. Open your Terminal app and navigate to the directory where you saved the mase Markdown file (use the `cd` command). Then at the terminal prompt, type: 

    pandoc gp35.md -s --mathjax -o gp35.html

Replace `gp35` with whatever you called your file. The computer will think for a second and then give you the next prompt. If you do `ls` you'll see a new file, `gp35.html` has been created. Just like that, we have the assignment we will now give to students. 

Here's what that terminal command did. In the Ingredients you installed a program called Pandoc. This is a low-level app -- there's no icon for it; it runs in the background when called -- that essentially takes any kind of text file and turns it into any other kind of text file. The `pandoc` at the beginning calls this program. (You should really take time to learn Pandoc. It's an amazing tool.)

Then, the `gp35.md` just tells Pandoc which file to start with. The `-s` flag tells Pandoc to produce a standalone file as a result. The `--mathjax` flag (note the double dash marks) tells Pandoc to use MathJax to take any LaTeX code that was in `gp35.md` and render the notation using MathJax. The `-o` flag tells Pandoc that the next item coming up is to be the name of the output; then we give it the name of the output, `gp35.html`. The end result is a file called `gp35.html` that has taken the base Markdown file and converted it to HTML with all the math notation rendered properly. 

It helps at this point to type `open gp35.html` in the terminal, which will open `gp35.html` or whatever you called it as a local file in your web browser, where you can check it over to make sure everything was converted OK. If it did, move on to Step 4. 

## Step 4: Deploy! 

We're ready to give this assignment out to students. You can do this in at least a couple of ways. 

You could simply post the HTML file somewhere (Blackboard, Dropbox, email attachment, etc.) and have students download it and open it locally in their web browser. As long as they are connected to the internet when they open it, everything should work. 

A more elegant solution is to find a place to host the HTML file so that it's publicly accessible, then send just the link out to students, or post the link to your CMS. Then there is no file to manage; they just click the link and there they are. 

The "send the link not the file" approach is elegant but unfortunately it can be fraught with technical difficulty, mainly because you have to find a host for the files. When I first started using HTML for these assignments, I was using a Wordpress.com blog instead of a CMS for my courses, and it was easy -- just upload the HTML file to Wordpress and insert a link to it, and then give the link to students. But for this summer's course, I used Blackboard because this is my university's standard platform for online courses. I figured it would be the same as with a Wordpress blog -- just upload the HTML file to Blackboard and let students click on it. The problem with this is that when the HTML file opens, the _text_ shows up fine, but none of the math notation renders. This is because MathJax, which handles the math notation, uses Javascript and Blackboard doesn't play nicely with Javascript apparently. Bottom line: CMS's don't play nicely with MathJax all the time. 

Not having math notation in the assignment for a Calculus class is kind of a big problem. So I ended up using some web space at Bluehost that I pay for to host domain names and websites (like my old proftalbert.com website). I made a subdomain called `mth201.proftalbert.com` and then uploaded all my HTML assignments to a `gp` folder. At that point, they are publicly accessible as web pages with unique URL's, and since they are not sealed within Blackboard, there's no problem with the MathJax. 

That's a major pain just to get HTML files onto the internet. However there might be simpler solutions, for example using a [GitHub Pages project or organizational page](https://help.github.com/articles/user-organization-and-project-pages/) for your class. I'll let people propose alternatives in the comments.

## Step 5: Gather student submissions

At this point all the really technical stuff is done. Students now work on the assignment and submit responses using the Google Form. What's important to remember pedagogically is that those responses are _data_ that you want to use to make adjustments to class time. So we need a plan for accessing and using the data. 

Fortunately the Google Form makes this easy. When students click to submit their response forms, all the data is dumped into a Google spreadsheet where you can slice, dice, and order things at will. You can just go into the spreadsheet before class, make a quick look to see patterns and trends, then address those in some appropriate way in class. 

Grading is even simpler since I grade these on a Pass/No Pass basis with "Pass" just meaning a good-faith effort to be right on each exercise. Just sort the spreadsheet by last/family name to put it in alphabetical order, look through to see if anybody _didn't_ give good faith effort, and then just go down your gradebook and score __Pass__ or __No Pass__. It takes about 90 seconds for me to grade a class of 30 students. 

## Conclusion

So this workflow of Markdown &#8594; Pandoc &#8594; HTML has worked out really well for me. What I really like is that none of the files is very big or complicated, and the process is future-proof since really we're only working with plain text files. I prefer working in Markdown whenever possible because of its flexibility and simplicity. Keeping the output in HTML gives me multiple options for deploying the assignments either as files or links. Honestly I think the weak link here is the Google Form, because you never seem to know when Google is going to [pull the plug on an otherwise useful tool](http://mashable.com/2013/03/13/google-kills-google-reader/). 


