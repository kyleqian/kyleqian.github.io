---
title: Scribble
layout: project
order_: 80
time_: Winter/Spring 2018
prev_desc_: VR text input via handwriting
prev_img_: /assets/img/index/scribble.jpg
tags_: VR, Unity, iOS, interaction design
with_: Chris Valadez, Nishtha Bhatia, Tariq Patanam
---

## Overview

Scribble explores handwriting as a method of text input in VR. It is one part iOS app, which turns the phone into a 3DOF notepad, and one part Unity plugin, which receives inputs wirelessly from the iOS app. Text input on Scribble is fast, intuitive, and portable, making it perfect for standalone VR HMDs. I worked on Scribble within a team of four, with support from Oculus.

<p><div class="vid-wrapper-yt"><iframe src="https://www.youtube.com/embed/v7YRMaLWRPg?rel=0&amp;showinfo=0" frameborder="0" allow="encrypted-media" allowfullscreen></iframe></div>
<center><sub><i>Used an HTC Vive for this demo since the Oculus Go didn't support video capture.</i></sub></center></p>

## Design

#### _Motivation_

Text input in VR sucks. Just ask anyone who's tried VR long enough to encounter a search bar or login screen. The most commonly used mechanic is point-and-click, similar to using a laser pointer. This mechanic is fairly intuitive and lightweight to implement, but it has several notable flaws, including arm fatigue. Without a clear optimal solution, text input has become one of VR/AR's most subtly daunting UX problems.

#### _Tradeoffs_

Each of the existing text input methods for VR has unique tradeoffs. Below is a brief summary of a few popular options:

| Method | Pros | Cons |
|---|---|---|
| Point-and-click | intuitive, portable | arm fatigue, slow, can be imprecise |
| Keyboard | very fast, ergonomic, powerful | not portable, can't see hands |
| Voice input | fast, expressive, intuitive | not private, not precise |

Our initial prototyping showed handwriting to be nearly twice as fast as point-and-click, as well as significantly less taxing on users' arms over a longer period. With point-and-click, users experienced noticeable arm fatigue within 30 seconds of continuous clicking, whereas handwriting was comfortable for much longer. Handwriting also has the added advantage of emphasizing haptic over visual feedback, since most people don't have trouble writing without looking.

<p><div class="img-wrapper"><img class="html-image" src="/assets/img/prototype-combined.jpg"></div>
<center><sub><i>"Paper" prototyping with a smartphone (left), a laser pointer (top right), and a Gear VR controller (bottom right).</i></sub></center></p>

## Implementation

Scribble turns an iPhone into a 3DOF notepad using Google's stroke-based OCR API for handwriting recognition. It streams 3DOF pose, parsed text, raw strokes, and button presses via a local TCP tunnel to the Unity plugin. The Unity plugin finds the app by first broadcasting its IP address via UDP, after which it connects and streams via TCP.

To demo Scribble, we created a VR brainstorming app for the Oculus Go. By jotting ideas onto their sticky pad and swiping them onto a virtual white board, users are able to digitize insights from brainstorming sessions without sacrificing the physicality of the exercise.

![](/assets/img/scribble1.jpg)
