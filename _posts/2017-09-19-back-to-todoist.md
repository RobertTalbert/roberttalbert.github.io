---
title: "Why I am going back to ToDoist from todo.txt"
excerpt: "Earlier in the summer, I migrated my GTD system from ToDoist to the text-based todo.txt system. I'm changing back, and here's why."
comments: true
share: true
tags:
  - GTD 
  - Productivity
---

Back in July, [I reported on a switch I was making in the tools I use to implement Getting Things Done](http://rtalbert.org/plaintext-gtd/). Briefly: My setup up to that point was to use [ToDoist](http://www.todoist.com) for all of my task lists, but I was beginning to be concerned about the control and flexibility that a proprietary system provided. So I switched to a purely text-based system using the [todo.txt format](http://todotxt.org/) that uses only plain text files. 

While it's not good to tinker with a GTD system that works --- because you end up spending time thinking about the sytem itself rather than using the system to Get Things Done --- I had a light summer, and so if I were going to experiment, this would be the time. So I used todo.txt all summer long and my initial impressions of it were very positive. But in the end, I had some issues with todo.txt that made me rethink my choice, and __I have decided to go back to using ToDoist__. I wanted to explain why, and discuss some things that I learned about GTD systems in the process. 

## Reason 1: Syncing 

The main reason I am migrating away from todo.txt is a serious issue with syncing the `todo.txt` file itself across different devices. This gets a little technical, so bear with me. 

The way todo.txt works is that there is a `todo.txt` file that contains all my tasks, and this file lives on Dropbox. This file can be accessed in different ways and from different devices. But ultimately it's just a text file that you just edit (using an app, a command line shell, or just a text editor). Importantly: If you are using todo.txt across multiple devices, Dropbox takes care of syncing this file. And there's where the problem comes in. 

Let's suppose you have a `todo.txt` file on Dropbox and are working with it on two devices, say a tablet and a phone. Suppose the tablet is offline but the phone is online. Before doing any editing, the most recently-synced version of `todo.txt` lives locally on both devices. Now suppose you use the tablet (offline) to make a change to the file, say marking a task as complete and adding one or two new tasks. Those changes are made but not synced, because the tablet is offline. Now suppose that, while the tablet is still offline, you use your phone to make even more changes. The changes are made and _are_ synced, because the phone is online. 

So far so good. But now, suppose you switch the tablet back online and it connects to Dropbox. What happens to `todo.txt`? What I _want_ to happen is that the changes that I made on the tablet catch up with the changes made on the phone, and all these changes are pulled together, resolved, and merged into a new version of `todo.txt` that is synced to all my devices. Alas, this is not what happens. Instead, Dropbox will take the most recently-synced version of the file and simply push it to all my devices. In our scenario, the newest version of `todo.txt` is the one edited on the phone. That version is the new official version of the file, and when the tablet syncs, all of the changes made on the tablet while offline are simply, and irrevocably, wiped out. 

How do I know this, you ask? Because while on the DC/NYC trip, I was on a plane to DC and did some reviewing, making a bunch of edits to `todo.txt` on my iPad, which was offline (in airplane mode). When I arrived in DC, my iPad was still in airplane mode but I did more work with `todo.txt` using my phone en route to my hotel. When I got to my hotel and got the tablet online, I looked at `todo.txt` and all of my tablet edits were gone. And there's no getting these back, because Dropbox never saw the tablet-version of the file. 

Obviously this isn't acceptable for me. This all-or-nothing approach to syncing might work for some people, for example those who only manage tasks on a single device or who are always online. For me, this is a fatal flaw in the system, one that makes the system fundamentally untrustworthy. 

With ToDoist, syncing is different. If you are offline on a device and add, change, or complete a task and then do the same on a second, online device, when the first device is reconnected to the internet, _both_ sets of changes are faithfully represented in ToDoist once the the offline device is back on. This is the way it should work and must work for me to be able to trust the system. 


## Reason 2: Shallow App Ecosystem

A second, lesser reason for going back to ToDoist is that most of the apps for todo.txt are not very good, to put it mildly. There _are_ apps for this system in a lot of different platforms, and that's a strength. However, most of the apps that are there are underdeveloped, or even outright abandoned, and they lack functionality and polish. 

[Gina Trapani created todo.txt at Lifehacker back in 2006](https://lifehacker.com/166299/geek-to-live--list-your-life-in-txt). Initially there was a lot of excitement, and rightfully so, since there were basically no task management apps at all in those days besides maybe [DevonThink](http://www.devontechnologies.com/products/devonthink/overview.html). That excitement and the corresponding development of the ecosystem seems to have lasted about five years. After 2011, todo.txt dropped off the radar. Many of the apps listed at the todo.txt home page have not been updated since then. For example, [the GitHub repo for the official Android todo.txt app has not had a commit since 2014](https://github.com/todotxt/todo.txt-android). Many of the other GitHub repos for todo.txt projects are similarly ghost-town-like. Up until just last month, the official website by Gina Trapani had not been updated in a few years and several of the links to apps led to 404's. Of the apps that are still being maintained, [some of them are just plain ugly](http://todo.martinsgill.co.uk/) and are relatively clunky to use, compared with ToDoist. 

A great exception to this rule is [TodoTxtMac](https://mjdescy.github.io/TodoTxtMac/) which is maintained by [Michael Descy](https://github.com/mjdescy). The app is updated in what seems like quarterly intervals and it's clear that Mike puts a lot of love into this project. If there were more app developers out there putting in the same elbow grease as Mike does, the todo.txt system would be a lot better off. 

I'm encouraged by the recent news that Gina [just last month transfered all development of todo.txt over to an open community](http://blog.todotxt.org/post/164525181522/community-and-the-future-of-todotxt). Maybe this means that some momentum can be generated to get todo.txt up to date. Until then, the app ecosystem is just too weak.

## Reason 3: The "It Just Works" factor

Finally, a reason that I switched back to ToDoist is that things in ToDoist simply work the way you want them to, without having to hack anything. Take recurring tasks for example. I found one todo.txt app supports recurring tasks, in the sense that when you mark the task done it automatically recurs in the list. Outside of that app, making truly recurring tasks is basically impossible; and in the `todo.txt` file itself, this _is_ impossible. At one point I had an IFTTT recipe set up that did this but it inexplicably stopped working at one point, messed up my `todo.sh` file (that controls the command line tool) and I never got it to work again no matter how much hacking I did. I even looked into learning about cron jobs and maybe using this Unix functionality to schedule appendices to text files. But then I realized, this is crazy, and it's more trouble for me than it was worth. 

On the other hand, if you want to add a task that recurs on the 25th of the month every month, in ToDoist you just type in `25th of each month` when you enter the task, and ToDoist adds the recurrence. That's it. (You might argue that recurring tasks should go on the calendar, not in a next action list; but I want them to be in the next action list, dang it.) 

Bottom line, the GTD system should not be something you spend a lot of time working with or thinking about. ToDoist is such a system for me; todo.txt ended up not being such a system for me when it comes to features that stray outside the core. 

## What I learned 

I learned a lot from using todo.txt, and I think it's still a system that fits a lot of people's needs, just not mine. Three lessons in particular stand out. 

First, I learned the lesson that __simplicity is essential__. The main attraction of todo.txt is that it's just a simple text file --- nothing more, nothing less, and no fluff or needless bells or whistles. Coming back to ToDoist, I am choosing not to use any of the features that I consider inessential, for example Google Calendar integration (which is important for some people but not for me). I am trying to keep things as text-file-like as I can. If ToDoist ever bloats out to the point where I cannot ignore the inessentials, I'll reconsider my choices. 

Second, I learned that a __completely frictionless GTD system is not always best__. That is, __some friction is good__. Before when using ToDoist, it's so easy to get things into the system that I was putting _everything_ into the system without thinking about whether the thing I was capturing was something that I _should_ be thinking about. Todo.txt forced me to slow down a little when adding things in, because there's no email-to-inbox feature and no real "quick entry" feature. That slight bit of friction in deciding whether certain "stuff" is truly worth my time, which is a great feature of analog systems like [bullet journaling](http://bulletjournal.com/), is something that I am disciplining myself to mimic now. 

Third and finally, I learned and still believe that __your data must remain under your control and must be reasonably portable__, just in case you ever need to switch systems. Again, `todo.txt` is just a text file and therefore future-proof; you don't have to worry about whether the data in it can be ported to a new computer if needed, or even printed out and kept analog. I learned in this process that [you can export your data from ToDoist](https://support.todoist.com/hc/en-us/articles/115001799989-Backups), and it comes out as a CSV file --- not quite as simple as a plain .txt file but still something that can be stored and worked with in case I ever feel I need to bail on ToDoist. I have no such assurances from other systems that might lock my data into a format that I cannot port. Whatever system a person uses, portability has to be near the top of the priority list. 

So it was a useful experiment, and in another work/life situation todo.txt would be a great fit for me, but for now it's back to the ranks of ToDoist users with me. 

