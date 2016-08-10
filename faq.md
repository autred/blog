---
layout: page
title: FAQ
permalink: /faq/
tags: about
---

## How are you different from all the other stats sites?

Here are some of the features we think make us unique.  We also try to focus development on features that aren't already available elsewhere for free.

* Public match replay parsing.  Replay parsing allows us to extract much more data from games than the WebAPI offers.

* Open source.  We keep our code open source, so anyone can help contribute, or learn from our work and apply it to their own projects.  We also have downloads of player and match data for users to do their own analysis.

* Visualizations.  We do some pretty interesting visualizations of player match data, such as histograms, heatmaps, and word clouds.


## Why aren't my matches showing up at all?

There is a setting in the Dota 2 client called "Expose Public Match Data".
It is off by default, and if not enabled, your account_id is hidden in the Dota 2 API, so we can't identify you as the player who played in the match (although we still have a record of the match itself).
Once enabled, any matches played after that point should show up in your profile.

## Why isn't advanced data available for some of my matches?

This data comes from replay files (not the WebAPI), and there are several reasons:

* The replay isn't ready yet.  There is usually a delay after the match (~10 minutes) while we wait for Valve to make the replay downloadable. 

* The replay might not be available.  This happens occasionally, particularly in the SEA region.  If you can't get the replay in the client, we can't get it either.

* The match had no users who've visited recently.  We don't automatically parse these replays because they're unlikely to be looked at.  We still get the basic data from the API, but don't queue it for replay parsing.

* API/GC issues.  If the Steam API is down, we can't find out about new matches, and if the GC (Game Coordinator) is down, we can't get replays to parse.

* The parser crashed while trying to parse the match.  This might happen if something weird happened in the replay file that we didn't expect.  If you suspect a replay is breaking the parser, please open an issue on GitHub!

* The replay is expired.  Valve deletes replays after 10 days.  This means we probably won't be able to do replay parsing for most matches before you registered.  Parsed matches before that point are due to other players in the game having signed up previously.


## What do I do if I want to develop a feature/report a bug?

[Open an issue on GitHub](https://github.com/yasp-dota/yasp/issues) if you'd like to work on a feature or report a bug.


## How do you make money/keep the site running?

This started as a side project of a couple of college students and it still operates that way.
We don't intend to make a profit from it, although we try to at least break even on the server bills.
We're also happy to share our knowledge with the community by completely open-sourcing the entire site and stack we run it on.

Development is done by volunteers contributing in their free time, so we don't have employees to pay.
Donations from users pay for servers.

## Can I use your code in my own project?

All of our code is licensed under the GNU GPLv3.
This means you are free to use it in your own project.
The GPL states that if you make modifications to the software and distribute it, you should make those modifications open source as well.
We would also appreciate a credit/attribution in your project if you use our code.

## Who are the people behind the site?

Development is done by the community, and is open to any interested developer.

A publicly hosted deployment is managed by some of the contributors:

Albert Cui:

<div>
<img src="https://avatars3.githubusercontent.com/u/3838552?v=3&s=150"/>
</div>

* [albertcui.com](http://albertcui.com)
* [/u/Triple_A](http://reddit.com/user/Triple_A)

Albert founded the project.
He built the donation system, writes blog posts, creates data dumps, and produces financial reports.

Howard Chung:

<div>
<img src="https://avatars2.githubusercontent.com/u/3134520?v=3&s=150"/>
</div>

* [howardchung.net](http://howardchung.net)
* [/u/Snifflehopper](http://reddit.com/user/Snifflehopper)

Howard's a software engineer (Duke University '15) and casual Dota 2 player.
His favorite heroes are Nature's Prophet, Terrorblade, and Lycan, so he's probably that guy you hate in your pub matches.
He wrote most of the code, believes in rapid deployment cycles, and tries not to break things too much.

Nicholas Hanson-Holtry:

<div>
<img src="https://avatars1.githubusercontent.com/u/9388670?v=3&s=150"/>
</div>

* [/u/waterandshade](http://reddit.com/user/waterandshade)

Nick comes up with ideas for cool machine learning things to do with the data.
We're trying to get him to do more.

## What is your privacy policy?

* All of the data provided comes from public sources such as the Steam WebAPI, Steam community profiles, and match replay files.
* Valve allows you to opt-out by having "Expose Public Match Data" unchecked in your Dota 2 options.  This causes you to appear as anonymous in future matches, although existing data is not deleted.
* We use Google Analytics (and therefore cookies) to monitor site traffic. For more information, see [Google's privacy terms](https://www.google.com/policies/privacy/partners/).

## What are your terms and conditions?

* We do our best to keep the site running, but cannot make any guarantees of availability, including for donators.
* We are unable to provide refunds for donations.

## I have subscription-related questions.
* Can I change my subscription?
  * Besides canceling? No. If you want to change the amount or the payment method, cancel and remake it.
* Can I have multiple subscriptions?
  * Yes. Cause you're super duper!
* Something is wrong! I'm being billed a lot! Or something.
  * Email us at support@yasp.co. Sorry about that.
* How can I cancel my subscription?
  * Click [here](/cancel). This will cancel ALL your subscriptions.
            
## How can I help if I don't know how to code?

If you're not a developer, you can buy some <a href='//yasp.co/carry' target="_blank">Cheese</a> to help pay for servers, or tell your friends about how awesome this site is : )
