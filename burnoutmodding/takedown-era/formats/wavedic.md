---
layout: page
permalink: /burnoutmodding/takedown-era/formats/wavedic/
---

The **Wave Dictionary** (.AWD) audio container format is used exclusively by the Takedown Era of Burnout games. Unlike similar format RWS, AWD stores its audio samples in a linked list; meaning the header of each sample contains a pointer to the previous sample, the sample after it, and its own data. AWD is capable of storing samples of differing frequencies.

According to the debug data of Burnout Revenge's Alpha 7 build, AWD can store a maximum of 55 samples.