---
title: Sounds of the Woods
layout: project
order_: 75
time_: Spring 2018
tags_: VR, Unity, Oculus Go, game design
with_: Angela He
ext_links_: Oculus Store|https://www.oculus.com/experiences/go/1283301105105802/;GitHub Page|https://github.com/kyleqian/SOUNDS-OF-THE-WOODS;Project Poster|/assets/misc/257Poster_KyleAngela.pdf
prev_desc_: audio-based VR horror game
prev_img_: /assets/img/index/sotw.jpg
title_replacement_: /assets/img/sotw-banner.jpg
---

## Overview
Sounds of the Woods is an audio-based horror game for the Oculus Go. Using the Go's 3DOF controller as a flashlight to ward off the unknown, players become increasingly reliant on their ears as the sky grows ever darker.

This game was created as a part of a Stanford course at CCRMA on [Neuroplasicity and Musical Gaming](https://ccrma.stanford.edu/courses/257-spring-2018/pages/overview/){:target="_blank"}, and is available for free on the Oculus Store with a couple thousand downloads. Naturally, it is best experienced with headphones or earbuds in a quiet place.

<p><div class="vid-wrapper-yt"><iframe src="https://www.youtube.com/embed/3kUTf5dbFSs?rel=0&amp;showinfo=0" frameborder="0" allow="encrypted-media" allowfullscreen></iframe></div>
<center><sub><i>My flashlight runs out of battery in the presence of an invisible creature. This playthrough was done on an HTC Vive for ease of recording.</i></sub></center></p>

## Design

#### _Motivation_

This game began as a VR experience to simulate deteriorating eyesight. The key insight was that VR HMDs completely occlude vision, meaning as creators, we not only have the power to show users immersive content, but we also blindfold them by default. The original concept was that the player would start by accomplishing everyday tasks with normal vision, but as their vision deteriorates, they would be forced to rely more and more on other senses.

Eventually, we scoped it down to just one task and swapped out vision deterioration with fading sunlight. To further scope down the game, we decided to develop for the Oculus Go, at the time barely a week old in the market.

#### _Constraints_

On one hand, developing for the Go imposed a number of significant limitations which we worked around:

| Challenge | Solution |
|---|---|
| No 6DOF HMD, so players could get sick if they tried to move around. | Premise of the game is that you're injured and stuck in the woods, so have a seat. |
| No 6DOF controllers for interactions such as firing arrows in the dark. | Ward off enemies with just a flashlight, which gives instant, persisting accuracy feedback. |
| Generally poor rendering horsepower. | Most of the art is completely 2D, particularly the grass, which can simply face one direction since the player doesn't move. |
| Not specific to the Go, but 3D audio lacks vertical distinguishability. | All mandatory enemies only appear at or near eye level, and only move on the horizontal plane. |

On the other hand, a major win with using the standalone Go, besides ease of setup, is that even if enemies appear behind the player, they can twist and turn around all they want without fear of getting tangled in wires. This is especially true (and more fun) if they sit in a swivel chair.

## Implementation

Sounds of the Woods was created entirely in Unity for the Oculus Go, with myself as the programming half. Nearly all assets and scripts were created from scratch for this game, except for the trees and sounds.

The core game logic is driven by a GameManager which tracks the time of day and triggers specific functionality, split between the Creature, (visual) Effects, and Sound managers. For example, when enough time has passed and Afternoon turns to Dusk, the GameManager triggers its OnPhaseUnloaded event for Afternoon and its OnPhaseLoaded event for Dusk. In response:

* CreatureManager despawns the friendly deer and squirrels, and spawns a random number of hostile bunnies, raccoons, and wolves.
* EffectsManager starts driving the moon across the sky, starts lerping the lighting effects from Afternoon presets to Dusk presets, and spawns fireflies.
* SoundManager downpitches the background music and gradually lowers the volume.

## Results

The relatively short length of the game lends itself well to demos. Players along a wide spectrum of age and gaming/VR experience are able to quickly pick up the game with minimal instruction. The flashlight mechanic in particular is very intuitive, as it only has one button and is used for a singular purpose.

Many players respond favorably to the wolves, as their circling movement pattern works well with 3D sound, making them the most satisfying creatures to localize. The wolves are also primarily responsible for making players turn all around, back and forth in their seats, taking full advantage of the standalone HMD.

Some players find the game quite unnerving or scary. Although the visual aesthetic of the game seems harmless and cartoonish at first, as the night grows darker, the feel of the game becomes more and more defined by the increasingly menacing audio effects. By the darkest portion of the game, players are essentially in pitch black, forced to rely on their ears as their flashlight battery continues to dwindle.

<p><div class="img-wrapper"><img class="html-image" src="/assets/img/sotw-combined.jpg"></div>
<center><sub><i>Best enjoyed with noise-cancelling headphones!</i></sub></center></p>

![](/assets/img/sotw3.jpg)

![](/assets/img/sotw2.jpg)

![](/assets/img/sotw1.jpg)
