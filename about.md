---
layout: default
title: About
permalink: /about/
---

## Introduction

Sometime in 2020, I was watching Star Trek with my wife, my mind drifted, and I started wondering 
about how cable TV worked. For some reason I had a lot of extra time on my hands around then, so I 
started learning about what all was involved and then, arrogantly, declared to anyone willing to 
listen, that I was going to create my own cable system.

The more I thought about the project the more I fell in love with it. It wasn't just a project, it 
was (and is) a never-ending collection of projects. It's a theme around which projects can sprout. 
I am a software engineer by trade, and one of the aspects of the career I treasure most is the 
neverending stream of opportunities to learn new things. This is my model train set. It's never 
complete, and there will always be something more I can do or change with it. When I need a break 
from working on it, I can watch it. When I want to and am able to, I can find a new part of it to 
obsess over.

Even if this doesn't inspire you to build your own cable system, I hope you can appreciate the 
novelty of it, and I hope you have or find a hobby that brings you the amount of joy this has 
brought me.

## How it works, the simple(-ish) version

You can think of a cable system as multiple videos playing at the same time, and your TV knows how 
to focus on just one at a time. Imagine a 50 channel cable service (small by today's standards), 
then imagine a stack of 50 DVD players all playing something different. You can take the video and 
audio from each DVD player and put it on a separate radio frequency. This is called 
[modulation](/glossary/#rf-modulator). You can then take those 50 separate signals, all on 
different frequencies, and combine them to flow on a single cable. At that point, your TV just has 
to choose one frequency out of the 50 to focus on at a time. That's called tuning. Each channel has 
it's own frequency, so if you modulate to a channel's assigned frequency, you'll see and hear it on 
that channel.

Now, it would be a huge pain to swap discs constantly as you change what show is on, but people 
used to do this! Well, they most likely used tapes or maybe laserdiscs in some cases. Still, we're 
talking about running multiple channels ourselves! We can't be swapping tapes or discs constantly. 
Instead, what I've done is used a series of small, low cost, low powered computers to play the 
videos based off a centalized schedule. Oh, and I have them inserting commercials as well for a 
more authentic experience.

## The hardware and software involved

I have a small server rack that contains several Raspberry Pis (one per channel). They know what to 
play by asking the central scheduling server, which is also running on a Raspberry Pi. That one also 
doubles as the guide channel.

The videos are stored on a Synology NAS, and all the channel Raspberry Pis have read-only access to 
the shared directory. Each Raspberry Pi runs a piece of software I call "Technical Director", which 
is what consults the scheduling server and queues up shows and commercials. It displays the video 
content in fullscreen using libVLC.

The composite output of the Raspberry Pis each go into a separate modulator. I use Blonder Tongue 
mini-modulators, model MICM-(b, c, or d). 12 of these slot into a 2U rack which also contains a 
power supply for them. The Raspberry Pis are powered via PoE fed by a switch on the rack. The 
modulators all connect to inputs on a Blonder Tongue OC-12 signal combiner. This results in two 
outputs, one that has been attenuated enough for direct use, and another that has not been 
attenuated at all and has a very strong signal coming off it. This stronger output was made to be 
split many times and still have a decent strength. This equipment was likely
pulled from a school or motel. I got it off eBay.
