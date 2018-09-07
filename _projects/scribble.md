---
title: Scribble
layout: project
order_: 1
time_: Winter/Spring 2018
prev_desc_: VR text input via handwriting
prev_img_: /assets/img/index/scribble.jpg
tags_: VR, Unity, iOS, interaction design
with_: Chris Valadez, Nishtha Bhatia, Tariq Patanam
---

Anyone who's tried VR long enough to encounter a search bar or a password screen knows that text input in VR sucks. Without an easy way to translate the metaphors of 2D text input into 3D, text input has become one of VR's most subtly daunting UX problems.

Scribble explores handwriting as a fast, intuitive, and portable means of text input in VR. I worked on Scribble within a team of four, with sponsorship and support from Oculus.

<p><div class="yt-vid-wrapper"><iframe src="https://www.youtube.com/embed/v7YRMaLWRPg?rel=0&amp;showinfo=0" frameborder="0" allow="encrypted-media" allowfullscreen></iframe></div>
<center><sub><i>Using an HTC Vive for this demo since the Oculus Go doesn't support video capture yet.</i></sub></center></p>

We designed Scribble as an iOS app that uses Google's stroke-based OCR API for handwriting recognition. The app streams 3DOF pose, parsed text, raw stroke, and button presses via a local TCP tunnel. Our initial prototyping showed handwriting to be nearly twice as fast as more common "laser pointer" methods of text input in VR, as well as significantly less taxing on users' arms over a longer period. Handwriting also has the added advantage of emphasizing haptic, not visual feedback, since most people don't have trouble writing without looking.

<p><div class="img-wrapper"><img class="html-image" src="{{ site.url }}/assets/img/prototype-combined.jpg"></div>
<center><sub><i>"Paper" prototyping with a smartphone (left), a laser pointer (top right), and a Gear VR controller (bottom right).</i></sub></center></p>

To demo Scribble, we created a VR brainstorming app for the Oculus Go. Affectionately named Stormi, the app receives Scribble's TCP streams and transforms the user's smartphone into a sticky pad. By jotting ideas onto their sticky pad and swiping them onto a virtual white board, users are able to digitize insights from brainstorming sessions without sacrificing the physicality of the exercise.

Further possibilities include version control for ideation, guided brainstorming sessions, and remote collaborative sessions via multiplayer networking.

![]({{ site.url }}/assets/img/scribble1.jpg)
