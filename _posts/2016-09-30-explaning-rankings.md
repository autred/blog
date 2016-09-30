---
layout:     post
title:      Explaining Rankings
summary:    An explanation of how rankings work
---

This post hopefully will explain the methodology behind hero rankings in a more layman-friendly manner.

Factors considered:  
 * Number of wins  
 * Average MMR in matches played  

Factors NOT considered:  
 * KDA, GPM, etc.  
 
I chose these factors in order to discourage players from stat-padding in order to increase their rankings.

Methodology:  
 * When a player wins a match, they score points equal to (average visible MMR in match / 1000) ^ 7 for the hero they played.  
 * We apply an exponent so higher MMRs are able to score points more rapidly than lower ones.  A match won at 6000 MMR scores 128 times as many points as one won at 3000 MMR.  
 * The division is intended to scale down the MMR to a reasonable number since we are applying an exponent to it.  
 * The exponentiation factor has been adjusted several times to weight MMR more heavily and will be 7 starting 2016-10-01.  
 * Losses score negative points (new change for 2016-10-01).  This weights win rate more heavily.
 * Each hero has its own individual ranking list.
 * The score used for the ranking is the sum of the points in the current ranking period.

Data storage:  
 * Hero rankings utilize Redis zsets (sorted sets) for fast update/lookup of any player's rank.  
 * The methodology currently in use has the benefit of being efficiently updated.  We simply need to INCR the player's score in the corresponding zset whenever they win a game.  

Reset (seasons):  
 *  Rankings will reset every 3 months (January, April, July, and October 1st), which clears all lists.  This is for a couple of reasons:  
  * Rankings should reflect recent data.  If a player has played thousands of games previously on a hero but hasn't in the last year, they should not occupy a permanent slot on the rankings.  
  * It's easier to tweak and adjust the ranking formula when the rankings reset periodically (we can apply the new formula shortly prior to the reset and avoid having to back-calculate rankings for all previous matches).  

If you have any suggestions or ideas, please open an issue on GitHub for discussion, or start a discussion on our Discord channel!  
