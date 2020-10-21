---
title: Asset Formats (models, textures, sounds, etc.)
---

Documentation for the various asset types used by the Burnout games (i.e mesh formats, texture and sound codecs) can be found here.

### Model Data 
Files containing model data on Burnout PS2 and PSP contain both the actual mesh data as well as the GPU commands required to render the models (these commands use arguments related to the specific vertices being drawn, so they have to be grouped in as data with the rest of the file). PS2 models from the Takedown Era-games seem to store their vertex data as rows of 4-byte floating-point numbers, with 3 floats in each row; it's possible each of the floats represent the X, Y and Z coordinates of the vertex.

Each "block" of mesh data on the PS2 version begins with the hex sequence `00 00 00 05 03 01 00 01 00 80`.

Files that contain model data:
* [.BGV and .BTV](https://acutesyntax.github.io/wikis/burnoutmodding/takedown-era/formats/bgv.html)
* .DAT (STATIC and STREAMED)

### Texture Data
Burnout PS2 and PSP's textures are stored as uncompressed bitmaps, which use CLUT4 (16-color) and CLUT8 (256-color) color palettes, with the palette itself being a little ways underneath the texture data.

Burnout PS2's texture headers are 0x250 bytes in length; PSP texture headers are 0x110. Both games use different texture swizzling methods, and PS2 texture CLUTs seem to use a signed char(?) for the texture's alpha channel as opposed to an unsigned one.

Burnout Xbox textures seem to use some form of compression (likely DXT).

Files that contain texture data:
* [.BGV and .BTV](https://acutesyntax.github.io/wikis/burnoutmodding/takedown-era/formats/bgv.html)
* [.TXD (Texture Dictionaries)](https://acutesyntax.github.io/wikis/burnoutmodding/takedown-era/formats/texdic.html)
* .DAT (STATIC, STREAMED and ENVIRO)

### Sound Data
The PS2 versions of Burnout use Sony's proprietary PS-ADPCM format for its sound data, while the Xbox versions use Microsoft's XWB format. Burnout PSP also uses PS-ADPCM for its sound effects, however the samples themselves are stored in Electronic Arts' SDT container format. 

In contrast to the console versions, songs and FMV audio tracks are stored as separate files on the PSP versions and are encoded in ATRAC3+ format, another Sony codec.