---
title: "The Making of 'Sorting Battle'"
categories:
  - gamedev
tags:
  - Sorting Battle
  - open source
  - postmortem
---

<iframe frameborder="0" src="https://itch.io/embed/1860397?bg_color=ffffff" width="552" height="167"><a href="https://chocola-mint.itch.io/sorting-battle">Sorting Battle by chocola-mint</a></iframe>

It's been awhile, huh.

## Conceptualization

The core design of Sorting Battle was conceptualized in the September of 2021. The original idea was to make it into a Godot-based hyper-casual mobile game, much like the typical match-3 puzzle games (Bejeweled, Candy Crush, etc.)

But, I was also very busy back then. Specifically, I was working on [Lucid Dive](lucid-dive-postmortem), so I had no choice but to put Sorting Battle on the back burner.

## Revival

It was not until late 2022 that I found an opportunity to bring Sorting Battle back. As you may have known, I'm also a teaching assistant for our university's Game Programming course ~~which is mostly run by teaching assistants rather than the lecturer~~. The lecturer approached me with the idea of locking the topic of the course's final project to "an AI-based game," trying to find new games to add to the catalog of his lab's educational platform, which usually hosts reinforcement learning winter camps.

I declined, of course, but my primary concerns weren't with how this might limit creativity freedom (it *would*), but rather how none of the teaching assistants here were qualified to guide students to actually design such a game. However, I did find the idea interesting, and was motivated to make myself able to design such a game.

This naturally brought me to suggesting the idea to my team in a Machine Learning course I was taking. I added a competitive aspect to the design (inspired by Tetris Attack and Puyo Puyo), so that the game becomes complex enough for us to try solving with reinforcement learning. In all fairness, I had also suggested other ML-related projects (namely, a model that can add normals to a 2D image, and a browser extension that can filter YouTube livestream troll/spam messages based on crowdsourced data collection), but they still liked the game idea more, so we stuck to it.

## Making it open source

Around the same time, I was also becoming insecure with my portfolio. I had a lot of games under my belt, but not a lot of code to demonstrate *how* I work. My portfolio would be fine as a solo programmer, but if I want to work with other programmers, I need to have some clean code to show that I'm safe to work with. 

Games are notoriously difficult to make open source. Most code libraries on the Internet are licensed liberally, usually under the MIT license, but a game is more than just the code. Art assets, music assets, these are the problem. Although you can find a lot of them published for *free*, but quite a few of them explicitly disallow redistribution. When you put a game project up on GitHub, you're inevitably redistributing those assets as well, so they can't be used here. Thankfully, [opengameart.org](opengameart.org) provides a lot of assets that allow redistribution.

## Developing the game

On paper, my responsibilities were mostly just the frontend Unity application, making everything look professional and feel good, but I also ended up coordinating with the reinforcement learning team a lot, providing feedbacks on their results every now and then. It was a fantastic display of teamwork, and I enjoyed my time thoroughly designing and developing *Sorting Battle*.

I won't bore you with the technical aspects of the game here, but if you're interested, you can refer to [the GitHub repository](https://github.com/chocola-mint/Sorting-Battle) for more detail. I think I did a good job bringing everything together, all without using ML-Agents.
