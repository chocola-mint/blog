---
title: "The Making of 'Flight to Paradise' @ Mini Jam 99"
categories:
  - gamedev
tags:
  - gamejam
  - postmortem
---

<iframe frameborder="0" src="https://itch.io/embed/1387248?border_width=5&amp;bg_color=434343&amp;fg_color=ffffff&amp;link_color=5b9dfa" width="560" height="175"><a href="https://chocola-mint.itch.io/flight-to-paradise">Flight to Paradise by chocola-mint</a></iframe>

So, this is my second game jam, and the first one in which I'm working alone. I figured that it would be a good chance to explore my own abilities, and there are still some time until school starts, so I thought, why not?

## Day 1

### Hour -3 ~ 0 (Preparation)

I had given the theme of the mini jam (birds) a bit of thought before, and decided to open Unity and start preparing. Itch's mini jams have one limitation, only announced after the start of the game jam, and so there was the chance of my idea needing some additional modifications to fit the limitation, but it was a risk I was willing to take.

In any case, since it was going to be a game about birds, I had to go and look for bird assets. My go-to locations are [opengameart.org](https://opengameart.org/) and [itch.io's assets catalog](https://itch.io/game-assets). Only free assets are considered. I found a nice bird model on opengameart.org and decided to go with it.

A recent project I was involved in had serious scoping issues, so I did extra care to make sure that I wasn't too greedy with my game design. It was a simple idea - a relay race of life, with birds passing the baton to the next caged bird on the screen, in the hopes that one of them could escape from a dangerous maze and find paradise (freedom). It was an idea that required *no rigidbody physics*, dramatically reducing the number of possible bugs that could end up wasting my time.

A problem with using free assets is that since they're gathered from multiple sources, they're bound to have inconsistent styles, which could be visually unappealing. My strategy was to use solid colors to overwrite the sprites and models' textures. That means using an unlit colored material for the bird, and a sprite shader that replaces the sprite's image's RGB channels with the color given by the Sprite Renderer component. With that in mind, I hunted down the remaining free assets, and whipped up a title screen. The overall art style will be **minimalist**.

Around this time, the jam started, and the limitation was announced - "can't stop moving." A bit simple, but my game design was a perfect fit for the limitation, and so I carried on. It was around noon, so I left to eat lunch and take a break.

### Hour +2 ~ +8 (Gameplay)

In the next few hours I did the following:
1. Wrote a script for the bird that keeps moving towards its right, controllable with the keyboard. For simplicitly, I used the old polling-based input API.
2. Added a few sawblades and used a script to make them spin.
3. Came up with some cheap particle effects and used them for when the bird touches the sawblades' triggers.
4. Implemented "bird reincarnation."
5. Finished up the first room's layout.

And then I left to have dinner.

### Hour +10 ~ +13

For the second room, I wanted to have new traps to spice things up. The first trap was a turret that fires at the player, and so I quickly wrote a script for the turret and the bullet it fires.

For the second trap, I wanted to have lasers, but quickly realized that it would be too complicated and just not worth it, so I settled on moving sawblades. Those, however, weren't as simple as they seemed.

I wanted to have a lot of moving sawblades, and obviously they wouldn't necessarily have the same movement patterns. I tried to write a script that could interpolate over a path denoted by other game objects, but that also became very complicated and I eventually decided to scrap the code. After that, I settled on using animators and animations to settle the issue.

Using animators has a great pro in that it is a codeless state machine, reducing chances for error. Leveraging the recording feature of animations could also let me visualize the paths just-in-time. The drawbacks are mainly that this approach results in creating a lot of animation files.

With this approach, I dropped two moving sawblades in the second room, and finished its layout. I realized that the second room was bigger than the first, and that a separate camera would be appropriate, so I decided to install Cinemachine for virtual camera support. I had planned for low-res visuals originally, but the need for the camera to zoom out made me cut that idea out.

I then went back to add tutorial on how to play the game. Since the design was sufficiently simple, I decided to embed the tutorial inside the game (rather than writing it in plaintext on a separate document). A button sprite and an arrow sprite were enough, both of which I could draw myself.

With all the work done, I went to sleep.


### Hour +21 ~ +24

Around this time, I worked on the third room, and decided to add a switch mechanism to really make the reincarnation mechanism interesting. A bird would have to flip a switch for the bird in the next room so that when it gets to fly, it wouldn't be met with a dead end. This means having to draw the sprite for a switch, as well as animating a sawblade accordingly. I then added a few more larger rooms and reaching around 70% completion.

Around this point, I have already streamlined the development process, being able to create one room after another efficiently.

~~So I took a break in the afternoon and went to watch a Yakuza 2 livestream.~~

### Hour +34 ~ +38

For the night, I added a second turret type and kept expanding the game at a breakneck pace. I barely needed to write any code, and my progress was amazing. By the end of the night, I had the gameplay finished, as well as a time and score system with HUD shown on the screen.

### Hour +45 ~ +48

I added BGM and SFX to the game around this time. I figured that some "coins" would be a good idea to make the score the player sees feel more dynamic, so I made some particles for a coin. I also fixed some minor visual issues for the better.

The rest of the morning was spent on playtesting, and then compiling builds for each platform, and finally recording the gameplay video and writing the game's project page.

In the end, I managed to submit my game one day before the deadline. I may have underscoped this time around, but at least it's better than overscoping, so there's that. Perhaps I could try a harder genre next time...