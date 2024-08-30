---
layout: default
title: ""
---

## What is this?
{: #what}

<picture>
  <source srcset="/assets/img/guide_scroll_290.webp" type="image/webp">
  <img src="/assets/img/guide_scroll_novideo.png" alt="An image of the program guide on a CRT television.">
</picture>

This is a resource for creating your own personal little cable company.
Personally, I'm aiming for a 12 channel system, including a program guide
channel, a weather channel, and more. Check out my system status
[here.](/my-setup)

## Why would anyone do that?
{: #why}

For fun, mostly. Play with some new-to-you technology and create your own channels with their own personas.

## How do you do it?
{: #how}

Like many hobbies, there are varying degrees of how "into it" you get. It has
definitely taken me a lot more time, money, and effort than I initially
thought. I have a small server rack containing a 24 port PoE networking
switch, a shelf that holds one set of (Raspberry Pi 3b+, PoE Hat) per channel,
a Blonder Tongue MIRC-12 2U mini-modulator rack w/ power supply containing 12
MICM-b modulators, and a Blonder Tongue OC-12 output combiner.

The whole thing pretty much flows in rack order, top to bottom. My Synology
NAS lives elsewhere on my network and holds all of the TV Shows, Movies, and
Commercials that play on my cable system. The switch provides data and power
to the Raspberry Pis, which output composite video to the modulators. The
modulators have their signals packaged together in the output combiner, which
provides the final signal viewable on the TVs throughout my house.

One of the Raspberry Pis runs the [Scheduler](https://github.com/My-Little-Cable-Co/Scheduler)
application. That same Raspberry Pi is responsible for outputting the video
feed of the program guide. Each other Raspberry Pi runs the 
[Technical Director](https://github.com/My-Little-Cable-Co/Technical-Director) 
program, which consults the scheduler and queues up the videos, interspersing
commercials as needed.

The combination of those two programs gets you a simulation of a TV channel,
and several of those starts to look like a cable system. By coming up with
coherent schedules for a given channel's persona, you can create a fairly
realistic experience.

Not all channels have to show videos, either! For example, the brilliant
[WS4000 Simulator](https://www.taiganet.com/) gives you a very realistic
weather channel with current forecasts and weather data for your area. You can
tell the Scheduler that the weather channel is a 24 hour listing (like the
guide channel), and feed the output of WS4000 to that channel's modulator.
Another example might be a music video channel, where instead of showing
episodes of a show, each timeslot represents a theme or genre. This channel
would have a similar, but better suited for the context Technical
Director-style program controlling the video feed.

Something I'd like to do in the future is have the Scheduler be able to
"follow" a real channel's listings, and use my HD Homerun to add OTA channels
that show classic content. I look forward to seeing what others build.
