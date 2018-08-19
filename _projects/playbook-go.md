---
layout: project
title: Playbook Go
time_: Winter 2018
tags_: VR, Unity, Oculus Go, interaction design
---

Playbook Go is a wireless, one-to-many VR instructional tool that effectively scales how instructors and coaches do training. It leverages the portability of standalone Oculus Go headsets, and was created with Unity using the UNET multiplayer API.

<p><div class="yt-video-wrapper"><iframe src="https://www.youtube.com/embed/S7rBHZ6hDKU" frameborder="0" allow="encrypted-media" allowfullscreen></iframe></div>
<center><sub><i>The trainer operates a 2D desktop interface, while multiple trainees can simultaneously and individually see what the trainer is doing.</i></sub></center></p>

While interning at [STRIVR](https://strivr.com/){:target="_blank"}, I was fortunate to not only help ship an initial MVP to a major client, but have enough time left over to work on a smaller project of my own design, which turned into Playbook Go.

At the time, most of STRIVR's products were built for the Oculus Rift, which presented clear challenges to both scalability (one trainer to one trainee at a time) and convenience (bulky VR laptops and messy cabling). Also at the time, Oculus Go dev kits were recently released ahead of its spring launch and there were a few in the office. I saw a clear opportunity for STRIVR to take advantage of standalone VR for training, and I set out to create a working demo before the end of my internship.

![]({{ site.url }}/assets/img/playbookgo1.png)

In creating Playbook Go, I took heavy inspiration from [Google Expeditions](https://edu.google.com/expeditions/#about){:target="_blank"}, which is a Cardboard app that's essentially "VR fieldtrips." Notably, the app included the following features:

* **Wireless, one-to-many connectivity**---teachers oversaw the lesson on a tablet
* **Gaze detection**---teachers could see where each student was looking
* **Attention direction**---teachers could point students to look at specific points of interest, and dynamic arrows would appear in each student's headset

Because I created the project in Unity, I had the distinct pleasure of wrangling with Unity's infamous UNET multiplayer API to enable sync'd video playback and gaze/attention tracking. Using a similar model to many local multiplayer games, each trainee (player) would connect to a room created by a trainer (host/server). This way the trainer is able to capture the gaze of each trainee, as well as make broadcasted manipulations to the VR video visible to everyone else.

![]({{ site.url }}/assets/img/playbookgo2.png)

Each of those features was present in my final Playbook Go demo, which additionally included the ability for trainers to markup the VR video with a brush. The demo was very well-received, and prompted the leadership team to further consider the far-reaching benefits of scaling VR training via standalone headsets.