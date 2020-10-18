---
layout: page
permalink: /burnoutmodding/takedown-era/formats/bgv/
---

**BGV** (Burnout Game Vehicle, BTV or Burnout Traffic Vehicle for traffic cars) is a file format used by the Takedown Era of Burnout games. This format contains all data related to the game's vehicles, including mesh data, LODs, texture data, pointers to external files (e.g. value database, the car's HWD and LWD files), deformation matrices and physics configuration info. BTV files are identical in every way to BGVs, with the only difference between the two being their file extensions.

All currently known offsets for revision 0x17 can be found [here.](https://docs.google.com/spreadsheets/d/1t0ZpOjCC9_2RJfcgQ8NLD8oJZfoZmpxxHEnNF5AN2Wo/edit?usp=sharing)

## Revision Differences
This format underwent a number of revisions and structural changes during the time it was in use. Because of this, BGVs use a single number at the start of the file to indicate its version:

```
0x14 = Burnout 3 Demo
0x17 = Takedown/Legends/Dominator PSP
0x1D = Revenge Demo
0x1F = Revenge/Dominator PS2
0x25* = Revenge Xbox 360
```

*(Revision 0x25 BGVs are compressed with ZLib, so they'll have to be manually decompressed using [Offzip](https://zenhax.com/viewtopic.php?t=5) if you wish to analyze/modify them.)

* 0x14 BGVs are the only version to use *global pointers* for the LOD submesh lists mentioned below. These point to the exact location in the file of each submesh, whereas local pointers (used by 0x17 and up) use offsets relative to the beginning of the LOD (i.e a pointer to `0x1820` in a 0x14 BGV would appear to point to `0x140` in all other revisions).

* Revision 0x17 has a hardcoded limit of 6 body parts (not counting the car's wheels and chassis); this limit was bumped up to 8 starting with revision 0x1D.

* Revision 0x1D and up stores deformation matrices in a different order to previous revisions.

## LOD Databases
LODs, or Levels of Detail, are lower-poly, lower-detail (hence the name) models that games use for objects that are far away from the player, to keep framerates smooth. LOD Databases contain all of the 3D mesh data for any given vehicle. In turn, BGVs contain 4 LODs of minimum (LOD 0), low (LOD 1), medium (LOD 2) and high (LOD 3) quality.

Each LOD in a BGV contains a list of pointers to its submeshes at the very beginning; there are always exactly 12 pointers since it seems the maximum amount of submeshes a BGV can contain is 12, though it's unknown if this rule is enforced by the game or if it can be larger than that.