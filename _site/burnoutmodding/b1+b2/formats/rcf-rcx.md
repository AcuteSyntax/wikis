**RCF/RCX** is a vehicle data container format used exclusively by Burnout 2. It contains the car's model, LODs, textures and potentially(?) physics info and other metadata. This format can be considered a precursor to the [BGV format](https://acutesyntax.github.io/wikis/burnoutmodding/takedown-era/formats/bgv) used from Burnout 3 to Dominator. 

An important difference to make is that RCF files are the models used for the main menu and are higher quality than the RCX models, which are the ones used ingame. Unlike RCX, RCF also does not use separate body parts; all its model data is stored in several submeshes instead. 


**All currently known offsets:**
```
0x00 - version code(?)
0x08 - file size
0x38 - unknown pointer(?) always 0x1880, seems to point to something
0x7C to 0x8C - pointer table (model/lod ptrs?)
0x88: texture pointer
```