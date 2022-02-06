---
title: "Lucid Dive - A postmortem"
categories:
  - gamedev
tags:
  - Lucid Dive
  - postmortem
---

The game in question is over [here](https://chocola-mint.itch.io/lucid-dive). Check it out if you haven't already.
{: .notice--info}

Lucid Dive is a game our team spent roughly four months on. While the finished product is fairly pretty, the same cannot be said for the development process.

One thing we did right was starting early. ~~And even then, there are apparently teams from other universities that had started all the way back in July or so.~~ We really needed all the time we could get, for not just writing code and producing assets, but also for iterating upon the game design.

... Yeah, that thing. Game design.

In short, **2D action platformers are very difficult to do right.**

Here's the deal, after shooting down quite a few ideas in the first few discussions, we arrived at a design where the player moves around the level with a hookshot. The hookshot could be aimed at anywhere and used to pull the player towards any surface it lands on. It turned up to be surprisingly complicated to implement, but the code itself was the least of our worries. The problem was that, it was just too plain, to be called a "feature."

We were dreaded when we realized that fact. It was about a month before the final presentation day, we had finals for other subjects just around the corner, and we had walked ourselves into a corner.

Now, in all fairness, it is entirely reasonable for a prototype to be scrapped in four months for an actual game studio. That's what they call design iteration. For them, all they would lose from it would be time, but for us, it was close to total destruction of our future hopes.

Our art lead had come up with including combos in the game, an idea he had gotten from our instructor, but under the constraints of a looming deadline and nearly no time, there wasn't much we could do to fully adapt a combo system (as that would require more graphical assets). We settled with a system that involved scores and health restoration. In other words, basically nothing. ~~But hey, numbers appear on the left of the screen, so at least that's giving players good feedback.~~

In any case, we did not - and could not - fix the issue. The feedback we received later was much more positive despite the fact that we had added nothing else, ~~but I suspect that that was in part out of pity~~.

So yeah, in retrospect, aside from getting a more balanced team, we really should've picked an easier genre.