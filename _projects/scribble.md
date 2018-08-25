---
title: Scribble
layout: project
time_: Winter/Spring 2018
tags_: VR, Unity, iOS, interaction design
with_: Chris Valadez, Nishtha Bhatia, Tariq Patanam
---

Anyone who's tried VR long enough to encounter a search bar or a password screen knows that text input in VR sucks. Without an easy way to translate 2D metaphors of text input into 3D, text input has become one of VR's most subtly daunting UX problems.

Scribble explores handwriting as a fast, intuitive, and portable means of text input in VR. I worked on Scribble in a team of four, with sponsorship and support from Oculus.

[Video]
(This demo was created post hoc, as the original project was created with the Oculus Go without mirroring capabilities.)

We created Scribble as an iOS app that uses Google's stroke-based OCR API for handwriting recognition. The app streams 3DOF pose, parsed text, raw stroke, and button presses via a local TCP tunnel. Our initial prototyping showed handwriting to be nearly twice as fast as more common "laser pointer" methods of text input in VR, as well as significantly less taxing on users' arms over a longer period. Handwriting also has the added advantage of not requiring as much visual feedback, as most people don't have trouble writing without looking.

![]({{ site.url }}/assets/img/scribble/prototype-combine.jpg)

To demo Scribble, we created a VR brainstorming app for the Oculus Go. Affectionately named Stormi, the app receives Scribble's TCP streams and transforms the user's smartphone into a sticky pad. By jotting ideas onto their sticky pad and swiping them onto a virtual white board, users are able to digitize insights from brainstorming sessions without sacrificing the physicality of the exercise.

Further possibilities include version control for ideation, guided brainstorming sessions, and remote collaborative sessions.

[Screens from vid]
