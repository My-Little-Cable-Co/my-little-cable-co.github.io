---
layout: default
title: Glossary
permalink: /glossary/
---

{% include glossary_definition.html
   term_id="rf-modulator"
   term="RF modulator"
   definition='An RF modulator is a device that takes a video signal and alters the frequency (modulates!) to a specific desired frequency. For the purposes of this website, this can be simplified to: "Composite Video + Audio comes in from a source device and is output over coax as a specific channel."'
%}

{% include glossary_definition.html
   term_id="multi-input-rf-modulator"
   term="A multi-input RF modulator"
   definition="An RF modulator that has multiple video inputs and is able to output each of them on different channels simultaneously. These essentially work as multiple modulators and a combiner all in one unit, and can be desired by casual hobbyists due to their compact nature. Note: There are many RF modulators that were created for older video game systems that may seem like the same thing as this, but are little more than source selectors. They can only output one source at a time, and only on either channel 3 or channel 4."
%}

{% include glossary_definition.html
   term_id="analog-tv"
   term="A TV capable of tuning analog signals"
   definition="We are using RF modulators that output analog frequencies due to them being relatively inexpensive. One of the reasons they are less expensive is because analog TV signals are rarely used since the move to digital. Most modern TVs either have digital-only tuners, or even no tuner at all! You should ensure that the TVs you plan to use with your setup are capable of tuning analog signals. If would be fairly safe to just get an old CRT TV, but make sure you have a plan for recycling it responsibly once you are done with it or it reaches the end of its life. Alternatively, you could get an external tuner that can accept analog signals."
%}

{% include glossary_definition.html
   term_id="channelized-modulator"
   term="Channelized modulator"
   definition="An RF modulator that is preconfigured to only modulate to a specific channel's frequency. No matter the input, it will always output on that one specific channel."
%}

{% include glossary_definition.html
   term_id="agile-modulator"
   term="Agile modulator"
   definition="An RF modulator that can be set to modulate to any channel's frequency. This can be done via dip switches or with channel + or - buttons accompanied by a channel number display."
%}

{% include glossary_definition.html
   term_id="signal-combiner"
   term="Signal combiner"
   definition="A device that takes individual channel signals and merges them into one. This is how you go from 2 (or more) cables each carrying one channel to 1 cable where you can flip between the channels. They vary in the number of signals that they can combine into one. Some devices take in 8, some take in 12, some take in 24! If you were to set up a large number of channels, you may end up needing a signal combiner for your signal combiners!"
%}

{% include glossary_definition.html
   term_id="distribution-amplifier"
   term="Distribution amplifier"
   definition="If you are making your cable system available to many TVs throughout a building, you may need one or more distribution amplifiers to ensure the signal is strong enough for a TV to receive it by the time it gets there. Splitters and wall taps weaken the signal along the way. Starting out with a signal that is too strong for a TV can allow you to receive the correct signal strength after being weakened between the amplifier and the television."
%}

{% include glossary_definition.html
   term_id="raspberry-pi"
   term="Raspberry Pi"
   definition="A small, generally inexpensive ARM-based single board computer. There are many models and revisions. Most have native composite video output, but many require a 3.5mm TRRS cable, which can be difficult to source. The Pi Zero provides solder pads where a composite video connector can be attached, but you would need to purchase a DAC to get an audio output from somewhere besides the HDMI port. The Raspberry Pi 4 has composite output disabled by default, but it can be re-enabled by modifying the config.txt file. Doing so will negatively impact performance."
%}

{% include glossary_definition.html
   term_id="network-attached-storage"
   term="Network attached storage (NAS)"
   definition="A dedicated file server on your local network. Useful for storing the videos that will be playing on your channels. Streaming them over the network connection will be better for the health of your Raspberry Pi's Micro SD card."
%}

{% include glossary_definition.html
   term_id="network-switch"
   term="Network switch"
   definition="Shares a network connection over many LAN ports. Some are able to send Power over Ethernet, which, when used in conjunction with a PoE hat on a Raspberry Pi 3+ or Raspberry Pi 4, could make for a very efficient and clean setup."
%}

{% include glossary_definition.html
   term_id="equipment-rack"
   term="Equipment rack"
   definition='Most of the equipment we are dealing with was made to fit into a standard 19" wide equipment rack. Sometimes called "server racks", these metal structures allow you to mount your equipment securely and neatly.'
%}

{% include glossary_definition.html
   term_id="video-files"
   term="Video files"
   definition="These make up some of the content that you will feature on your channels. I can't tell you where to get them, though. Maybe you already have them?"
%}
