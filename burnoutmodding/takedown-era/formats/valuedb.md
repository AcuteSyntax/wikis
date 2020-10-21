---
title: VDB.XML/VDB.BIN (Value Database)
---

Named `VDB.XML` in Burnout 3 and Legends and renamed to `VDB.BIN` starting with Burnout Revenge's demo; the **Value Database** is a hash map used exclusively by the Takedown Era of games. The VDB contains configuration data for various aspects of the game, including:
  * Per-car AI/sound/camera settings
  * Per-car boost gain/loss rates 
  * Various per-car performance and physics statistics (i.e top speeds, which are stored in the file as floating-point numbers)
  * Miscellaneous camera configuration data
  * Sound configuration


**All currently known offsets:**
```
0x00 - Maximum Number of CSV Files
0x04 - Maximum Value Amount
0x08 - Maximum Array Elements
0x0C - Maximum Number of Arrays
0x10 - Maximum Write Buffer Length
```