---
title: Bloodflow VR
layout: project
order_: 5
time_: Spring 2018
tags_: VR, Unity, computer graphics
prev_desc_: cardiovascular simulations in VR
prev_img_: /assets/img/index/bloodflow-vr.jpg
ext_links_: Stanford Daily Article|https://www.stanforddaily.com/2018/07/23/pediatric-cardiologist-uses-vr-to-visualize-heart-defects/
---

I collaborated with [Lighthaus Inc.](https://www.lighthaus.us/){:target="_blank"} and the [Marsden Lab](https://cbcl.stanford.edu/about/mission){:target="_blank"} at Stanford to make cardiovascular simulations come alive in VR. Specifically, I created a data pipeline from [SimVascular](http://simvascular.github.io/){:target="_blank"}---a cardiovasular blood flow simulator---to Unity, where the timestep results of those simulations can be animated and freely manipulated in VR.

<p><div class="vid-wrapper-bf"><video autoplay loop muted playsinline>
  <source src="/assets/vid/streamlines.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video></div>
<center><sub><i>Animated pressure streamlines (videos might not play on mobile).</i></sub></center></p>

Medical simulation data is very dense, much denser than data one might typically use in a game engine such as Unity. The files produced by simulators like SimVasular ended up being way too large for Unity to smoothly import, render, and export. I had to find ways to reduce the upfront data footprint, as well as optimize how Unity ingested and rendered the results.

One persistant problem was that aggregate timestep files generated for any sufficiently detailed simulation regularly topped dozens of gigabytes. At the time, Unity---despite being a 64-bit engine---was not able to export shared resources exceeding 4gb. In other words, Unity is normally not able to export single scenes that contain more than 4gb of content. Cache trickery was necessary to get around this, in which a series of "dummy" scenes were created and preloaded in chunks of 4gb apiece.

<p><div class="vid-wrapper-bf"><video autoplay loop muted playsinline>
  <source src="/assets/vid/flow.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video></div></p>

<p><div class="vid-wrapper-bf"><video autoplay loop muted playsinline>
  <source src="/assets/vid/heart.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video></div></p>
