---
title: Playbook Go
layout: project
order_: 2
time_: Winter 2018
prev_desc_: wireless, networked VR training
prev_img_: /assets/img/index/playbook-go.jpg
tags_: VR, Unity, Oculus Go, interaction design
---

Playbook Go is a wireless, one-to-many VR instructional tool that effectively scales how instructors and coaches do training. It leverages the portability of standalone Oculus Go headsets, and was created with Unity using the UNET multiplayer API.

<p><div class="yt-vid-wrapper"><iframe src="https://www.youtube.com/embed/S7rBHZ6hDKU?rel=0&amp;showinfo=0" frameborder="0" allow="encrypted-media" allowfullscreen></iframe></div>
<center><sub><i>The trainer operates a 2D desktop interface, while multiple trainees can simultaneously and individually see what the trainer is doing.</i></sub></center></p>

While interning at [STRIVR](https://strivr.com/){:target="_blank"}, I was fortunate to not only help ship an MVP to a major client, but also have time left over to work on a smaller project of my own design, which turned into Playbook Go.

At the time, most of STRIVR's products were built for the Oculus Rift, which presented clear challenges to both scalability (one trainer to one trainee at a time) and convenience (bulky VR laptops and messy cabling). Also at the time, Oculus Go dev kits were recently released ahead of its spring launch. I saw a clear opportunity for STRIVR to take advantage of standalone VR for training, so I set out to create a working demo before the end of my internship.

![]({{ site.url }}/assets/img/playbookgo1.jpg)

In creating Playbook Go, I tooked towards [Google Expeditions](https://edu.google.com/expeditions/#about){:target="_blank"} as an example of a shared, curated VR experience. I took heavy inspiration from their concept of a "VR fieldtrip" in the following features:

* **Wireless, one-to-many connectivity**---teachers oversee the shared lesson wirelessly on a tablet
* **Gaze detection**---teachers can see where each student is looking
* **Attention direction**---teachers can point students to look at specific points of interest, which cause guiding arrows to appear in each student's headset

To implement these networked features, I had the distinct pleasure of wrangling with Unity's infamous UNET multiplayer API to enable sync'd video playback and gaze/attention tracking. Using a similar model to many local multiplayer games, each trainee (player) would connect to a room created by a trainer (host/server). This way the trainer or teacher is able to capture the gaze of each trainee, as well as make broadcasted manipulations to the VR video that are visible to everyone.

![]({{ site.url }}/assets/img/playbookgo2.jpg)

My final Playbook Go demo at a company all-hands also included the ability for trainers to markup the VR video with a brush. The demo was very well-received, and prompted leadership to further consider the far-reaching benefits of scaling VR training via standalone headsets.
