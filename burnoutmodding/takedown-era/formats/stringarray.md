---
layout: page
permalink: /burnoutmodding/takedown-era/formats/stringarray/
---

The **String Array** format is used exclusively by the Takedown Era of Burnout games and contains all text strings used by the game's UI elements, including the menus, ingame messages and HUD elements.

Similar to Texture Dictionaries, there is a Criterion String at the beginning of the file describing the file type (`STRINGARRAY`), and a pointer table containing the offsets of each string. Hashed string arrays, used by Burnout Revenge as well as both versions of Burnout Dominator, use 4-byte IDs to tag each string. Consequently, the pointer tables in hashed arrays point to the IDs, which are located next to the string in question.