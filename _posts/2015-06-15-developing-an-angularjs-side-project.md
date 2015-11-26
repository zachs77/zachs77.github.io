---
title: Starting to Develop An AngularJS Side Project
comments: true
author: Zach Shefska
excerpt: I always plan on finding a fitness center near the hotel I am staying at. Unfortunately, that never happens. Scouring Google search results for "gyms near Reston, VA" always proves a waste of time.
layout: post
permalink: /developing-an-angularjs-side-project/
categories:
  - AngularJS
  - Entrepreneurship
  - Programming
  - Side Projects
tags:
  - angularjs
  - gym finder
  - side project
---
<div class="ttr_start">
</div>

I have been urged by my peers to learn [AngularJS][1] in recent weeks. At work our in house application uses Angular and the other developers would like for me to be able to help maintain it.

With this in mind I have recently begun programming a new side project to learn and practice [AngularJS][1].

## The idea

The idea for this project was entirely inspired by a problem I frequently run into. When I am at home I religiously go to the gym. When I am away from home (on vacation, visiting family, etc) I never go to the gym.

I always plan on finding a fitness center near the hotel I am staying at. Unfortunately, that never happens. Scouring Google search results for &#8220;gyms near Reston, VA&#8221; always proves a waste of time. Google finds a few gyms near-by, but does a poor job helping me sign up for a one week membership.

Having repeatedly not been able to find a suitable gym with a reasonable one week pass I have decided to create GymFinder (the name is not set in stone).

Users open GymFinder in their browser and put in the zip-code they will be travelling to. GymFinder searches through a massive database of fitness center across the world and returns those that are within a specified radius.

Results also contain meta-data, such as the size of the gym, the equipment available, and the price for a one week pass. GymFinder helps people find the right gym when they go on trips. And if it doesn&#8217;t do that, then at least it will help me find a gym when I go on vacation!

## The tech

After consulting with other developers at work I have decided to use a fairly simple stack to create this application.

As mentioned above AngularJS will control nearly all of the application. Ajax requests will be done with Angular and a simple PHP server side script will call data from our mySQL database.

The GymFinder app will be a single page and take full advantage of AngularJS routing. There will be no user login or storing of data. Rather the application will be quite simple and only spit out results. This is simply for practice at the moment, more features will come down the line once I have a more complete understanding of Angular.

## The data

The most difficult aspect of this project is collecting, verifying, and storing enough data to make this project useful. After looking into using the Google Places API it became clear to me that creating an independent database of fitness centers was the best option.

The plan is to write some sort of script that will crawl the web and write to a csv file. A few websites such as [FitLink][2], [Directoryfitness][3], and [Gymnearme][4] seem to have all the data GymFinder would need (those websites have user interfaces that make then nearly impossible to use).

Two options are being considered for the crawling script. Option one would be to use an open source PHP script, while option two would be to write a simple bash script.

I am leaning towards writing a bash script. Bash scripting is fun, interesting, and has many practical applications at my work. Utilizing someone else&#8217;s PHP code does not seem like as much fun.

## Updates

I will mostly be working on GymFinder during the weekend. As progress is made I will be writing updates and sharing code.

<div class="ttr_end">
</div>

 [1]: https://angularjs.org/
 [2]: http://www.fitlink.com/gym-directory
 [3]: http://www.directoryfitness.com/
 [4]: http://gymnearme.com/directory/