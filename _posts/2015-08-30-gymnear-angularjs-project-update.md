---
title: 'GymNear &#8211; AngularJS Project Update'
comments: true
author: Zach Shefska
excerpt: "I ditched the idea of scraping the internet to create my own database of gyms and fitness centers. Instead I went with Google's API. Google has a fantastic database with more information then I would have ever been able to successfully pull together. The issue Google faces is when it comes to displaying that information to the end user."
layout: post
permalink: /gymnear-angularjs-project-update/
categories:
  - AngularJS
  - Entrepreneurship
  - Programming
tags:
  - angularjs
  - gym near
  - side project
---
<div class="ttr_start">
</div>

Two months ago I posted about an [AngularJS side project][1] that I had planned to begin working on. Over the past 8 weeks I have broken ground and launched an initial 1.0 app. I have gained an understanding of AngularJS, built a website that I am proud of, and had fun along the way.

[GymNear.com][2] is a simple to use and effective app that helps users find a gym or fitness center near them. Users enter in a location and the app responds back with a list of gyms nearby.

In my original post I wrote about how difficult it was to find a gym when google searching. I went as far as to say, &#8220;Scouring Google search results for &#8216;gyms near Reston, VA&#8217; always proves a waste of time.&#8221;.

Which is ironic, because I am now entirely relying on the Google Places API to serve content.

I ditched the idea of scraping the internet to create my own database of gyms and fitness centers. Instead I went with Google&#8217;s API. Google has a fantastic database with more information then I would have ever been able to successfully pull together. The issue Google faces is when it comes to displaying that information to the end user.

A google search of &#8220;Gyms near Reston, VA&#8221; will still be a waste of time. Intermixed with the good results are advertisements and unrelated content. With [GymNear.com][2] the user is presented with 20 of the closest gyms, that is it.

Essentially, all I have done is made a simplified Google. It works, it is easy to use, and it provides immediate value, I am really happy with where it stands.

## Design

I decided on a minimalist design for GymNear. When looking at competitors I thought there was a great opportunity to differentiate GymNear with clean, simple design.

Other websites that offer the same functionality look like they are from 2002&#8230;

<div id='gallery-1' class='gallery galleryid-249 gallery-columns-3 gallery-size-large'>
  <figure class='gallery-item'> 
  
  <div class='gallery-icon landscape'>
    <a href='http://shefska.com/gymnear-angularjs-project-update/gymnear1/'><img src="http://i0.wp.com/shefska.com/wp-content/uploads/2015/08/gymnear1.png?resize=840%2C390" class="attachment-large" alt="GymNearMe.com" data-recalc-dims="1" /></a>
  </div></figure><figure class='gallery-item'> 
  
  <div class='gallery-icon landscape'>
    <a href='http://shefska.com/gymnear-angularjs-project-update/gymnear3/'><img src="http://i2.wp.com/shefska.com/wp-content/uploads/2015/08/gymnear3.png?resize=840%2C390" class="attachment-large" alt="FitLink.com" data-recalc-dims="1" /></a>
  </div></figure><figure class='gallery-item'> 
  
  <div class='gallery-icon landscape'>
    <a href='http://shefska.com/gymnear-angularjs-project-update/gymnear4/'><img src="http://i0.wp.com/shefska.com/wp-content/uploads/2015/08/gymnear4.png?resize=840%2C390" class="attachment-large" alt="directoryfitness.com" data-recalc-dims="1" /></a>
  </div></figure>
</div>

With GymNear I knew I wanted something that looked both modern and simple.

<div id='gallery-2' class='gallery galleryid-249 gallery-columns-3 gallery-size-large'>
  <figure class='gallery-item'> 
  
  <div class='gallery-icon landscape'>
    <a href='http://shefska.com/gymnear-angularjs-project-update/gymnear2/'><img src="http://i2.wp.com/shefska.com/wp-content/uploads/2015/08/gymnear2.png?resize=840%2C390" class="attachment-large" alt="The homepage" aria-describedby="gallery-2-253" data-recalc-dims="1" /></a>
  </div><figcaption class='wp-caption-text gallery-caption' id='gallery-2-253'> The homepage </figcaption></figure><figure class='gallery-item'> 
  
  <div class='gallery-icon portrait'>
    <a href='http://shefska.com/gymnear-angularjs-project-update/gymnear6/'><img src="http://i2.wp.com/shefska.com/wp-content/uploads/2015/08/gymnear6.png?resize=719%2C1024" class="attachment-large" alt="Results page after clicking on a gym" aria-describedby="gallery-2-257" data-recalc-dims="1" /></a>
  </div><figcaption class='wp-caption-text gallery-caption' id='gallery-2-257'> Results page after clicking on a gym </figcaption></figure><figure class='gallery-item'> 
  
  <div class='gallery-icon portrait'>
    <a href='http://shefska.com/gymnear-angularjs-project-update/gymnear5/'><img src="http://i0.wp.com/shefska.com/wp-content/uploads/2015/08/gymnear5.png?resize=719%2C1024" class="attachment-large" alt="The map changes based on the location you enter" aria-describedby="gallery-2-250" data-recalc-dims="1" /></a>
  </div><figcaption class='wp-caption-text gallery-caption' id='gallery-2-250'> The map changes based on the location you enter </figcaption></figure>
</div>

## Functionality

In the spirit of not having to make the user think (thank you [Steve Krug][3]), I have limited GymNear&#8217;s functionality. The only thing a user can do on the site is enter a location and click on a link.

Initially I wanted to include reviews, ratings, directions and any other information that I could find when returning results. I decided against this, at least for now in an attempt to make GymNear as easy to use as possible.

By providing bare-bones functionality the user gets exactly what they expect, while also leaving the window open for future features to be added.

## Tech

Creating GymNear with Google&#8217;s API has allowed me to bypass nearly all &#8220;back-end&#8221; development. The entire application is built in Angular, and I have not yet set up a node server on the back-end.

Currently GymNear works by sending an API call to the Google Maps Place Service with the user entered location. It returns an array of objects which I then display on the page. When a user clicks on more info I pass that specific gyms place_id to Google&#8217;s Place Details API which returns another object with a ton of relevant information.

Essentially, what I have made is a website that makes a ton of requests to Google.

I have yet to set up a Node server, but that is a top priority. GymNear serves an entire JavaScript page to the browser which makes conventional SEO impossible. [Prerender][4] allows for AJAX heavy websites to be crawled effectively by search engines. Prerender runs on Node, and I have no experience setting up either.

In addition to configuring Prerender I am also planning on implementing [UI Router][5]. I would like to create 50 or so pages that serve content for specific locations. For example, gymnear.com/boston, or gymnear.com/atlanta. I think creating webpages like these would work well and help Gymnear rank higher for specific search terms.

Hopefully between Prerender and Angular UI Router GymNear will be able to get picked up by search engines.

## Moving Forward

Building version 1.0 of [GymNear][2] has been a blast. I will continue to post updates as more people use the application, and as new features and technical updates are made. If you are going to teach yourself a language or framework, this is the way to do it. Find a project and simply plug away.

<div class="ttr_end">
</div>

 [1]: http://shefska.com/developing-an-angularjs-side-project/
 [2]: http://gymnear.com/
 [3]: http://www.amazon.com/Dont-Make-Me-Think-Usability/dp/0321344758
 [4]: https://prerender.io/
 [5]: https://github.com/angular-ui/ui-router