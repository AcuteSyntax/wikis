---
layout: page
permalink: /burnoutmodding/takedown-era/formats/bgd/
---

The **Burnout Game Data** (.BGD) filetype contains configuration data and settings for each track, like the traffic density levels, whether or not the track is forward or reverse, the player's spawn coordinates, the start/end location of a lap, signature takedown data, and much more. Burnout 2 uses BGD to store its track data as well (albeit a much older version of the format). Each track has its own BGD file; it can be found in the track's folder alongside the track's other files.

Starting with Burnout 3's demo, this format started using single numbers at the very start of the file to mark the version (like [BGV.](https://acutesyntax.github.io/wikis/burnoutmodding/takedown-era/formats/bgv))

```
Burnout 3 Demo = 0x07
Takedown/Legends = 0x09
Revenge Demo = 0x10
Revenge 0714 alpha/Revenge Final= 0x11
Dominator PS2 = 0x13
Dominator PSP = 0x0B
```
