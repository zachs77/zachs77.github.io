---
title: Can You Win Fantasy Football With Quantitative Analysis?
comments: true
author: Zach Shefska
excerpt: "I have a theory, if winning at daily fantasy is skill based then I should be able to win more times than I lose. I don't have an innate ability to predict who will have a breakout game or what player is overrated from week to week. Rather, I can rely on quantitative analysis."
layout: post
permalink: /can-you-win-fantasy-football-with-quantitative-analysis/
categories:
  - Programming
tags:
  - data analysis
  - fantasy football
  - portfolio theory
---
<div class="ttr_start">
</div>

Last weekend marked the beginning of the 2015 National Football League season. From that weekend until Valentine&#8217;s day there will not be a single Saturday or Sunday without some form of college or professional football on tv.

Fantasy football leagues, and one day fantasy football games have swelled in popularity. Daily fantasy sports have picked up the most steam as of late.

Companies like [DraftKings][1] and [FanDuel][2] have both received billion dollar valuations from investors and are poised to payout hundreds of millions in &#8220;winnings&#8221; this season. As these corporations face legal challenges (daily fantasy sports and online gambling are nearly synonymous) I have thought to revitalize an old idea.

I have a theory, if winning at daily fantasy is skill based then I should be able to win more times than I lose. I don&#8217;t have an innate ability to predict who will have a breakout game or what player is overrated from week to week. Rather, I can rely on quantitative analysis.

Applying the same principles of financial analysis and portfolio theory to fantasy football teams *should* produce favorable results.

There is one major caveat in my plan &#8211; I am no financial analyst. Unfortunately I have only taken a few classes on quantitative methods, statistics, and financial theory. (Yes mom, this is me admitting that going back to school would be beneficial in this context.) None the less there are a myriad of open source tools and resources to draw from that should make this a successful project.

## Getting the data

I do not follow fantasy football religiously. I really don&#8217;t follow fantasy football at all. Thankfully [Boris Chen][3], and [Fantasy Football Analytics][4] do.

These two websites have been my main resource for data on players. Both websites use different techniques to rate players and project points.

Boris generates tiers of players from a gaussian mixture model. He pulls his data from the consensus rankings at [Fantasypros.com][5].

Fantasy Football Analytics goes more in depth for each player. They provide a projection for the season, the risk involved in drafting that player, and the value over replacement. Their data set is very robust, very deep, and very informative. I have used their projections and calculations for my simulations.

## Creating a model

*There is probably a much better way to generate simulations than the technique I am about to lay out. Please give me suggestions for the model &#8211; I appreciate your help.*

For the Monte Carlo simulation we need to assign probabilities to each player. If I assign probabilities that are not accurately weighted then the model will not work well.

As a baseline I have decided to assign probabilities based on the players projected points per game divided by their risk value. This generates probabilities that favor players who are projected to be more consistent.

Henry Markowitz&#8217;s portfolio theory suggests that rational investors will always choose a portfolio that has the best risk-expected return profile. In fantasy football this should also hold true.

By assigning probability to a player based on their return (points per game), and their risk (degree of uncertainty of players&#8217; projected points) we have created a model that loosely follows Markowitz&#8217;s principles.

## Strategy

I will be running simulations in Microsoft Excel. This can be burdensome on a personal computer, but the technique is relatively straight forward.

DraftKings does not finalize their &#8220;price&#8221; per player until the day of competition. This means that the teams I am currently generating are not necessarily realistic. Once the salary data is confirmed I will be able to generate &#8220;real&#8221; teams.

I know of no way to restrict excel to generate &#8220;teams&#8221; that fall below the $50,000 salary cap. As a work around I have assigned a background color to all cells that are above $50,000 in the &#8220;total salary&#8221; column.

After running my simulations I will randomly take 500 of the generated teams and play them on [DraftKings][1]. For now I will be using a [DraftKings CSV upload][6] plugin &#8211; in the future (if this works), I would like to write a script that automates this process.

In an attempt to mimic diversification (another one of Markowitz&#8217;s fundamental principles) I will play as many teams as possible. The more randomly generated teams I play, the more diverse my portfolio becomes.

There are many different types of leagues on DraftKings. The two that have drawn most of my attention are head to head competitions, and aggregate competitions.

A head to head competition gives you a 50% chance of winning. Your lineup competes against another users team. The team that scores more points wins. One on one competitions pay out $.80 on every dollar. If you enter a $1 competition and win, you get back $1.80.

An aggregate competition pays out winnings to the teams that finish in the top 20% of points scored. Your team competes against every other users team. If you enter an aggregate competition you can win between 1x and 100x your entry fee. For example, in a $1 league you could win $2 up to $100 if you come in first.

I have decided (as of now), to enter my teams in both competitions. I have no data driven approach to determine which league will provide better returns over time. I&#8217;m certain there is a way to determine this, I simply do not know how.

I plan to play 500 teams on week one of the NFL season. I will have $500 on the line. To break even on my head to head match-ups I will need to win 56% of the games. To break even on the aggregate league I will need place multiple teams within the top 20%.

## Suggestions

So, what do you think? If you have a suggestion, tip, or advice, please let me know. I will be posting updates on the simulation and my earnings (losses) as the NFL season gets going.

<div class="ttr_end">
</div>

 [1]: https://www.draftkings.com/r/zachshefska
 [2]: https://www.fanduel.com/
 [3]: http://www.borischen.co/
 [4]: http://fantasyfootballanalytics.net/
 [5]: http://fantasypros.com/
 [6]: https://rotogrinders.com/threads/introducing-our-new-script-extension-to-help-you-bulk-enter-lineups-on-draftkings-766518