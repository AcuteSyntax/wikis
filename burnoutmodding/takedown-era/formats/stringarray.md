---
title: String Array
---

The **String Array** format is used exclusively by the Takedown Era of Burnout games and contains all text strings used by the game's UI elements, including the menus, ingame messages and HUD elements.

Similar to [Texture Dictionaries](https://acutesyntax.github.io/burnoutmodding/takedown-era/formats/texdic), there is a Criterion String at the beginning of the file describing the file type. This string is `STRINGARRAY` for the non-hashed array type used from Burnout 3's demo to Legends, and `HASHIDARRAY` for the hashed array type used by Revenge and Dominator.
 
Directly after this is a pointer table containing the offsets of each string. **Hashed arrays**, used by Burnout Revenge as well as both versions of Burnout Dominator, use 4-byte IDs to tag each string. Consequently, the pointer tables in hashed arrays point to the IDs, which are located right next to the string in question.

