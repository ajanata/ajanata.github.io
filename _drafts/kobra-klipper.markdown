---
layout: post
title:  "Running Klipper on an Anycubic Kobra"
# date:   2024-01-27 20:30:00 -0700
categories:
    - blog
tags:
    - electronics
    - 3dprinting
---

My first 3D printer was an [Anycubic Kobra](https://store.anycubic.com/products/kobra) (not Pro, not 2, not Max, not anything).
It was a fine printer to get into the hobby, but the default Marlin firmware left some things to be desired.
I made attempts at building my own versions of the firmware (and succeeded with tuning a few minor options),
but the way they provided the [source](https://github.com/ANYCUBIC-3D/Kobra) under the GPL made it difficult to use a mainline Marlin build.
I started using [Octoprint](https://octoprint.org/) within months,
but I was never able to get the firmware to work with some key features&ndash;the most important of which was being able to pause the print,
which is required to use a filament run-out sensor.
Once I upgraded to a [Bambu Lab A1](https://us.store.bambulab.com/products/a1) (... before the heat bed recall),
I decided it was time to try to figure out how to get Klipper to work with the Kobra,
since I'd have the A1 to rely on to actually do printing while I messed with the Kobra.
It was not the most straightforward process, but it was also not as difficult as I feared it would be.
I had to scrounge around several sources to put it all together, though,
so I'm making an attempt to document the entire process here in case there's somebody else out there wanting to do this. 

<!--more-->
When I started my [Protogen head project](https://www.youtube.com/playlist?list=PL0zWUBwyQ7w8FVm4xew8T0MdTpzYQ-wPM) last year,
I originally wanted to avoid having to get a 3D printer due to space constraints and also just not wanting to have to deal with it.
That didn't last long, though, as I quickly determined I needed to print mounting brackets for the frame I was using
(and eventually a replacement inner frame, as the one I purchased broke and the replacement that was shipped got porch pirated).
