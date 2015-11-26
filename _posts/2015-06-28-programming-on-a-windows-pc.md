---
title: Programming On a Windows PC
comments: true
author: Zach Shefska
excerpt: "I'm used to developing on the Mac operating system (a huge thank you to the CEO of the company I work at for recently getting the development team new computers), and over the past 6 months I have done nearly all my programming on a Mac. Yet, when I am at home and working on a project I am left with my trusty 2012 Acer PC running Windows."
layout: post
permalink: /programming-on-a-windows-pc/
categories:
  - Programming
tags:
  - environment
  - programming
  - windows
---
<div class="ttr_start">
</div>

During the past two weeks I have been working weeknights and weekends on a simple AngularJS side-project. (I wrote more about that project [here][1] if you are interested).

I&#8217;ve been writing all the code on my Windows PC.

This has been quite a change. I&#8217;m used to developing on the Mac operating system (a huge thank you to the CEO of the company I work at for recently getting the development team new computers), and over the past 6 months I have done nearly all my programming on a Mac. Yet, when I am at home and working on a project I am left with my trusty 2012 Acer PC running Windows.

After contemplating a complete removal of Windows OS and installing Linux I decided to tough it out and spend some time re-configuring my personal laptop as a development environment.

## House cleaning

The first thing I did was remove garbage bloatware. I found a great site called [Should I Remove It?][2] which helped me decide what software was going to stay and what software had to go.

The first time I opened up the &#8220;Uninstall or change program&#8221; window on Windows I was overwhelmed. After browsing Should I Remove It, and doing a bit of googling I ended up  removing a few dozen programs.

## Command line

Coming from a Mac operating system I am familiar with the Mac, and even Linux shell. Trying to use those same commands in the Windows PowerShell became so annoying that I decided to install [Cygwin][3].

Rather than adapt to Windows, I brought Linux into the equation. Cygwin provides nearly all the functionality of a Linux terminal to a Windows machine. This does not mean Cygwin transforms your Windows computer into a Linux machine, but it does enough to keep you sane.

The Cygwin website says it best, &#8220;Cygwin is not a way to magically make native Windows apps aware of UNIX®&#8221;.

## Git, Node, Bower&#8230;

Next came the installation of [Git][4]. Followed by [Node.js][5]. Finished off with [Bower][6] for good measure.

I installed Node for the first time on this computer specifically to install Bower. I have never worked with Node, and all I know about it comes from reading occasional posts that grace the front page of Hacker News.

I know enough about Node to understand that it is powerful and important. Before installing Bower I went to [NodeSchool][7] and completed a few courses. I would suggest doing the same if you blindly install it like I did.

Finally I installed Bower which poses the question;

<pre>Why learn the in's and out's of package control when you can simply install Bower and have every dependency installed for you?!?</pre>

Yeah, terrible mindset, I know. But seriously, Bower makes it so seamless and easy to start building a new application. Learning and managing my own packages is something on the future checklist, in the meantime, Bower to the rescue.

## Wamp and Sublime

Two more software installations were necessary before I could start working on my Angular project. A local server, and a great text editor.

I have used[ Wamp][8] for years. I used Wamp when I was 14 and didn&#8217;t know what Javascript was. Wamp is solid, and provides the perfect foundation to start developing locally.

At work I have been using [Panic Coda 3][9] for the past few months. Coda is great. Publishing in Coda takes away the necessity of an FTP, and the preview mode has been a time saver every single day. But for developing locally and on a Windows machine Coda went out the window.

I installed [Sublime Text 3][10], changed a few small settings and got to work.

## Time to write code

Setting up my environment to program on a Windows PC was relatively easy. Which reminds me, now is about the time I should get back to writing some code!

<div class="ttr_end">
</div>

 [1]: http://shefska.com/developing-an-angularjs-side-project/
 [2]: http://www.shouldiremoveit.com/
 [3]: https://cygwin.com/
 [4]: http://git-scm.com/download/win
 [5]: https://nodejs.org/
 [6]: http://bower.io/
 [7]: http://nodeschool.io/
 [8]: http://www.wampserver.com/
 [9]: https://panic.com/coda/
 [10]: http://www.sublimetext.com/3