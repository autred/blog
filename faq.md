---
layout: page
title: FAQ
permalink: /faq
tags: faq
---

How are you different from all the other stats sites?

Here are some of the features we think make us unique.  We also try to focus development on features that aren't already available elsewhere for free.

* Free public match replay parsing.  Most similar services offer this as a premium feature.  Replay parsing allows us to extract much more data from games than the API offers.

* Open source.  We keep our code open source, so anyone can help contribute, or learn from our work and apply it to their own projects.  We also have downloads of player and match data for users to do their own analysis.

* Visualizations.  We do some pretty interesting visualizations of player match data, such as histograms, heatmaps, and word clouds.


Why aren't my matches showing up at all?

There is a setting in the Dota 2 client called "Expose Public Match Data".
It is off by default, and if not enabled, your account_id is hidden in the Dota 2 API, so we can't identify you as the player who played in the match (although we still have a record of the match itself).
Once enabled, any matches played after that point should show up in your profile.

Why isn't [some match] being parsed?

There are several reasons why we wouldn't have parsed data for a match:

* The replay isn't ready yet.  There is usually a delay after the match (~10 minutes) while we wait for Valve to make the replay downloadable. 

* The replay might not be available.  This happens occasionally, particularly in the SEA region.  If you can't get the replay in the client, we can't get it either.

* The match had no users who've visited recently.  We don't automatically parse these matches because they're unlikely to be looked at.  We still get the basic data from the API, but don't queue it for parse.

* The Dota 2 Network is down.  During server maintenances (usually on Tuesday), we can't get replays until we can connect again.

* The parser crashed while trying to parse the match.  This might happen if something weird happened in the replay file that we didn't expect.

* The replay is expired.  Valve deletes replays after 7 days, so we can't parse these matches.

Since we only parse the replays of active users, we have only parsed a small percentage of all the Dota 2 matches ever played, and only those after August 2014.
This means we probably won't be able to do replay parsing for the majority of your historical matches (from before registration).


What do I do if I want to develop a feature/report a bug?

[Open an issue on GitHub](https://github.com/yasp-dota/yasp/issues) if you'd like to work on a feature or report a bug.


How do you make money/keep the site running?

This started as a side project of a couple of college students and it still operates that way.
We don't intend to make a profit from it, although we try to at least break even on the server bills.
We're also happy to share our knowledge with the community by completely open-sourcing the entire site and stack we run it on.

Development is done by volunteers contributing in their free time, so we don't have employees to pay.
Donations from users pay for servers.

Can I use your code in my own project?

All of our code is licensed under the GNU GPLv3.
This means you are free to use it in your own project.
The GPL states that if you make modifications to the software and distribute it, you should make those modifications open source as well.
We would also appreciate a credit/attribution in your project if you use our code.

Who are the people behind the site?

The project is maintained by the core dev team, along with contributions from interested community developers.

Development began in August 2014, with a public release in January 2015.  

<div>
<img src="https://avatars2.githubusercontent.com/u/3134520?v=3&s=150"/>
</div>
Howard Chung:
----
* [howardchung.net](http://howardchung.net)
* [/u/suuuncon](http://reddit.com/user/suuuncon)
* [Player Profile](/players/88367253)

Howard's a software engineer (Duke University '15) and casual Dota 2 player.
His favorite heroes are Nature's Prophet, Terrorblade, and Lycan, so he's probably that guy you hate in your pub matches.
He also enjoys playing ultimate and board games.

Howard wrote most of the code and is constantly playing with new technologies to strive for better performance and lower cost.

<div>
<img src="https://avatars3.githubusercontent.com/u/3838552?v=3&s=150"/>
</div>
Albert Cui:
----
* [albertcui.com](http://albertcui.com)
* [/u/Triple_A](http://reddit.com/user/Triple_A)
* [Player Profile](/players/102344608)

Albert came up with the original idea for the site and manages the bills.  He built the donation system.

<div>
<img src="https://avatars1.githubusercontent.com/u/9388670?v=3&s=150"/>
</div>
Nicholas Hanson-Holtry:
----
* [/u/waterandshade](http://reddit.com/user/waterandshade)
* [Player Profile](/players/75392401)

Nick comes up with ideas for cool machine learning things we can do with the d

What is your privacy policy?

* All of the data provided comes from public sources such as the Steam WebAPI, Steam community profiles, and match replay files.
* Valve allows you to opt-out by not selecting "Expose Public Match Data" in your Dota 2 options.  This causes you to appear as anonymous in future matches, although existing data is not deleted.
* We use Google Analytics (and therefore cookies) to monitor site traffic. For more information, see [Google's privacy terms](https://www.google.com/policies/privacy/partners/).


What are your terms and conditions?

* We do our best to keep the site running, but cannot make any guarantees of availability, including for donators.
* We are unable to provide refunds for donations.

* Can I change my subscription?
  * Besides canceling? No. If you want to change the amount or the payment method, cancel and remake it.
* Can I have multiple subscriptions?
  * Yes. Cause you're super duper!
* Something is wrong! I'm being billed a lot! Or something.
  * Email us at support@yasp.co. Sorry about that.
* How can I cancel my subscription?
  * Click [here](/cancel). This will cancel ALL your subscriptions.
            
How can I help if I don't know how to code?

If you're not a developer, you can buy some <a href='/carry' target="_blank">Cheese</a> to help pay for servers, or tell your friends about how awesome this site is : )
