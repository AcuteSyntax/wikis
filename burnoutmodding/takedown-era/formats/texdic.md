---
title: TXD (Texture Dictionary)
---

The **Texture Dictionary** (.TXD) format is used by all Burnout games up to Paradise and is used to store textures, hence its name. The Takedown Era games mainly use this format for storing frontend textures (HUD and UI elements) and global textures (textures used in common places throughout the game, like car undersides and broken glass). These can be found in the FRONTEND.TXD and GLOBAL.TXD files in the `/DATA` folder of Burnout 3 and Burnout Legends.

At the beginning of each Texture Dictionary (offset `0x00`) is a Criterion String describing the file type (`TEXDIC`), and a pointer table immediately afterward (offset `0x08`) listing the locations of each texture. 

Alongside each pointer is a number that increases by 1 with each successive pointer; these numbers are presumably used as a way of identifying each texture, so that the game's executable knows the correct places at which to apply them.