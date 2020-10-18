---
layout: page
permalink: /burnoutmodding/patchdb/
---

Community-contributed patches and cheats, for use with the PCSX2, PPSSPP and Dolphin emulators.

# Burnout (PS2, NTSC-U)

```
//Disable Screen Bob + Blur (patch by: escape209)
patch=1,EE,2031758C,word,00000000
patch=1,EE,20372D60,word,00000000
```

# Burnout 2 (GameCube, NTSC-U)

```
//Disable Rain/Snow (patch by: Unknown)
042206e0 00000000
```


# Burnout 3 (PS2, NTSC-U) [April 28th, 2004 demo]

```
//PCSX2 Speedhacks (patch by: AcuteSyntax)
patch=1,EE,205121B4,byte,00000000 //Environment maps
patch=1,EE,205121BD,byte,00000000 //Specular
patch=1,EE,205121BE,byte,00000000 //Motion blur
```

```
//Freecam (R3+UP to enable, R3+DOWN to disable) [patch by: Edness]     
patch=1,EE,D04F50DC,extended,0000FFEB
patch=1,EE,203C10A0,extended,00000001
patch=1,EE,D03A519C,extended,0000FFBB
patch=1,EE,203C10A0,extended,00000004
```


# Burnout 3: Takedown (PS2, NTSC-U)

```
//PCSX2 Speedhacks (patch by: escape209) 
patch=1,EE,20665F28,byte,00000000 // 00000001 // Bloom, disabling this gives biggest performance boost
patch=1,EE,20665F29,byte,00000000 // 00000001 // Background fog, hardware backends don't emulate this correctly as of 23/08/2017
patch=1,EE,20665F2A,byte,00000000 // 00000001 // Motion blur, D3D11 hardware has problems with this
patch=1,EE,20665F20,byte,00000000 // 00000001 // Environment maps (make cars have reflections)
```

```
//Heavyweights are always selectable (patch by: escape209)
patch=1,EE,01E8EE94,byte,01
```

```
//Traffic Invincibility (patch by: AcuteSyntax)
patch=1,EE,204E1634,extended,7FFFFFFF
```

```
//Kamikaze Traffic (patch by: Dominator)
patch=1,EE,2064EC98,extended,00010101
```

```
//Freecam (R3+UP to enable, R3+DOWN to disable) [original patch by: AcuteSyntax,
improved by: Edness]
patch=1,D03A519C,extended,0000FFEB
patch=1,205179C0,extended,00000001      
patch=1,D04F50DC,extended,0000FFBB      
patch=1,205179C0,extended,00000004      
```


# Burnout Legends (USA + EUR, Greatest Hits/v2.00)

```
//patch by: Dark
_C0 Enable Timer
_L 0x2024A834 0x24A50001
_C0 Disable Timer
_L 0x2024A834 0x00000000
```

```
//patch by: Dark
_C0 Reset Play Time
_L 0x205E4A7C 0x00000000
```

```
//patch by: Dark
_C0 Fast AI
_L 0x20178274 0x0A200800
_L 0x20002000 0x3C0808B7
_L 0x20002004 0x8D0864E8
_L 0x20002008 0x11100005
_L 0x20002010 0x3C01435A
_L 0x20002014 0xAE010AB0
_L 0x20002020 0x0A25E09F
_L 0x20002024 0xC60F1444
_C0 Normal AI
_L 0x20178274 0xC60F1444
```

```
//patch by: Dark
_C0 Show Race AI Names
_L 0x2020C07C 0x00000000
```

```
//patch by: Dark
_C0 Harder Pursit Mode
_L 0x205415F4 0x00000001
_L 0x20575B54 0x00010101
_L 0x20577FB4 0x00010101
```

```
//patch by: Dark
_C0 AI Always Boosts
_L 0x205736F4 0x00010101
_L 0x20575B54 0x00010101
_L 0x20577FB4 0x00010101
_L 0x2057A414 0x00010101
_L 0x2057C874 0x00010101
```

```
//patch by: Dark
_C0 No Road Rage Damage
_L 0x2056EC24 0x3F800000
```

```
//patch by: Dark
_C0 Enable Motion Blur
_L 0x0040BE6A 0x00000001
_C0 Disable Motion Blur
_L 0x0040BE6A 0x00000000
```

```
//patch by: Dark
_C0 Red Boost
_L 0x0056EE61 0x00000001
_C0 Blue Boost
_L 0x0056EE61 0x00000000
_C1 Default Boost Colors
_L 0x201ED674 0x10C0000A
```

```
//patch by: Dark
_C0 All Cars Have Normal Boost
_L 0x201ED674 0x10C6000A
_C0 All Cars Have Dominator Boost
_L 0x201ED674 0x00000000
```

```
//patch by: Dark
_C0 Normal Boost Color Modifier
_L 0x203AC504 0x3F300000 //brightness: float from 0.0 to 1.0
_L 0x203AC510 0x3E800000 //red: float from 0.0 to 1.0
_L 0x203AC514 0x3F800000 //green: float from 0.0 to 1.0
_L 0x203AC518 0x3F800000 //blue: float from 0.0 to 1.0
_C0 Dominator Boost Color Modifier
_L 0x203AC524 0x3F800000 //brightness: float from 0.0 to 1.0
_L 0x203AC530 0x00000000 //red: float from 0.0 to 1.0
_L 0x203AC534 0x3F800000 //green: float from 0.0 to 1.0
_L 0x203AC538 0x3F800000 //blue: float from 0.0 to 1.0
```

```
patch by: AcuteSyntax
_C0 Disable HUD
_L 0x0040BE6B 0x00000000
_C1 Enable HUD
_L 0x0040BE6B 0x00000001
```

```
//patch by: AcuteSyntax
_C0 Proper FOV
_L 0x0040BF30 0x3FAAAAAB
_C1 Default FOV
_L 0x0040BF30 0x3F800000
```

```
//patch by: KabutoKun
_C0 Allow up to 5 rivals on races (game crashes on pursuits)
_L 0xE0010001 0x000D4B0C
_L 0x200D4B0C 0x26730003
```

```
//patch by: KabutoKun
_C0 Always allow heavyweights
_L 0xE0010005 0x000F8840
_L 0x200F8840 0x28A40006
_C0 Always allow heavyweights [MP]
_L 0xE0060006 0x000E7BB4
_L 0x200E7BB4 0x2A870007
_L 0x200E7BB0 0x10C0000D//DelaySlot1
_L 0x200E7BD4 0x2A870007
_L 0x200E7BD0 0x10C70005//DelaySlot2
_L 0x200E7BE4 0x2A870007
_L 0x200DCE08 0x10000005
```

```
//patch by: KabutoKun
_C0 Kamikaze/panic traffic ON
_L 0xE0010000 0x00221EB0
_L 0x20221EA4 0x34040001
_C0 Kamikaze/panic traffic OFF
_L 0xE0010001 0x00221EA4
_L 0x20221EA4 0x90A418CA
```

```
//patch by: KabutoKun
_C0 1x(64x64) vehicleReflections, default
_L 0xE0070004 0x00055C84
_L 0x20055C8C 0x24840909
_L 0x20041DE8 0x24C60040
_L 0x20041E18 0x24840606
_L 0x20237A60 0x34060040
_L 0x20237A64 0x34070040
_L 0x20237A6C 0x34080040
_L 0x20237A68 0x0E2154D8//JalDelay
_C0 2x(128x128) vehicleReflections
_L 0xE0070004 0x00055C84
_L 0x20055C8C 0x24840909
_L 0x20041DE8 0x24C60080
_L 0x20041E18 0x24840707
_L 0x20237A60 0x34060080
_L 0x20237A64 0x34070080
_L 0x20237A6C 0x34080080
_L 0x20237A68 0x0E2154D8//JalDelay
_C0 4x(256x256) vehicleReflections
_L 0xE0070004 0x00055C84
_L 0x20055C8C 0x24840909
_L 0x20041DE8 0x24C60100
_L 0x20041E18 0x24840808
_L 0x20237A60 0x34060100
_L 0x20237A64 0x34070100
_L 0x20237A6C 0x34080100
_L 0x20237A68 0x0E2154D8//JalDelay
```

```
//patch by: KabutoKun
_C0 Allow unlimited vehicle colors
_L 0xE0040006 0x000F88FC
_L 0x200F88FC 0x00000000
_L 0x200F8AF4 0x10000003
_L 0x200F8CC4 0x00801021
_L 0x2020A170 0x01A02021
_C0 Force 8 colors for vehicles
_L 0xE00D01AB 0x00209FB4
_L 0x20209FB4 0x0E2DBAEC//Jal1
_L 0x2036EBB0 0x27BDFFE0
_L 0x2036EBB4 0xAFBF0018
_L 0x2036EBB8 0xAFB00010
_L 0x2036EBBC 0x0E2101AB//Jal2
_L 0x2036EBC0 0x00A08021
_L 0x2036EBC4 0x8E190060
_L 0x2036EBC8 0x34180008//ColorCount
_L 0x2036EBCC 0xA33800B0
_L 0x2036EBD0 0x8FBF0018
_L 0x2036EBD4 0x8FB00010
_L 0x2036EBD8 0x03E00008
_L 0x2036EBDC 0x27BD0020
_C0 Default colors for vehicles
_L 0xE001BAEC 0x00209FB4
_L 0x20209FB4 0x0E2101AB//Jal1
```

```
//patch by: KabutoKun
_C1 Traffic checking, ON
_L 0xE00109C0 0x0016D08C
_L 0x003B09C0 0x00000001
_C0 Traffic checking, OFF
_L 0xE00109C0 0x0016D08C
_L 0x003B09C0 0x00000000
```

```
//patch by: AcuteSyntax
_C0 Traffic Invincibility ON
_L 0x00397A80 0x7F430000
_C1 Traffic Invincibility OFF
_L 0x00397A80 0x42960000
```


# Burnout Legends (July 8th, 2005 beta)

(all patches in this section by KabutoKun)

```
_C0 Particle: Yellow fxsparks OFF
_L 0xE00225A0 0x001F2ED0
_L 0x201F2ED0 0x00000000
_L 0x201F2EE0 0x00000000
_C0 Particle: Yellow fxsparks ON,default
_L 0xE0020000 0x001F2ED0
_L 0x201F2ED0 0x0E2125A0
_L 0x201F2EE0 0x1480FFFB
_C0 Particle: fxpopcorn count=0/OFF
_L 0xE0010005 0x001F2D9C
_L 0x201F2D9C 0x00000000
_C0 Particle: fxpopcorn count=1
_L 0xE0020001 0x001F2DCC
_L 0x201F2DD0 0x2A240001
_L 0x201F2D9C 0x16E00005
_C0 Particle: fxpopcorn count=2
_L 0xE0020001 0x001F2DCC
_L 0x201F2DD0 0x2A240002
_L 0x201F2D9C 0x16E00005
_C0 Particle: fxpopcorn count=3
_L 0xE0020001 0x001F2DCC
_L 0x201F2DD0 0x2A240003
_L 0x201F2D9C 0x16E00005
_C0 Particle: fxpopcorn count=4,default
_L 0xE0020001 0x001F2DCC
_L 0x201F2DD0 0x2A240004
_L 0x201F2D9C 0x16E00005
```

```
_C0 Traffic density v1: 1x,default
_L 0xE0010FC0 0x00226940
_L 0x20226940 0xC48C0000
_C0 Traffic density v1: 3x
_L 0xE0120000 0x00226940
_L 0x20226940 0x0E200FC0
_L 0x20226944 0x00000000
_L 0x20226948 0x4616603E
_L 0x2022694C 0x00000000
_L 0x20226950 0x45010019
_L 0x20003F00 0x8C990000
_L 0x20003F04 0x7F383800
_L 0x20003F08 0x340F00FE
_L 0x20003F0C 0x130F0007
_L 0x20003F10 0x44996000
_L 0x20003F18 0x44980000
_L 0x20003F1C 0x46006302
_L 0x20003F20 0x44196000
_L 0x20003F24 0x7DF93804
_L 0x20003F28 0xAC990000
_L 0x20003F2C 0x03E00008
_L 0x20003F30 0x00000000
_L 0x20003F14 0x3C184040//Multiplier
```

```
_C0 Always allow heavyweights [MP]
_L 0xE0060006 0x000E558C
_L 0x200E558C 0x2A870007
_L 0x200E5588 0x10C0000D//DelaySlot1
_L 0x200E55AC 0x2A870007
_L 0x200E55A8 0x10C70005//DelaySlot2
_L 0x200E55BC 0x2A870007
_L 0x200DAA4C 0x10000005
```

```
_C0 Force 8 colors for vehicles
_L 0xE00DFF79 0x002069A0
_L 0x202069A0 0x0E2DC3AC//Jal1
_L 0x20370EB0 0x27BDFFE0
_L 0x20370EB4 0xAFBF0018
_L 0x20370EB8 0xAFB00010
_L 0x20370EBC 0x0E20FF79//Jal2
_L 0x20370EC0 0x00A08021
_L 0x20370EC4 0x8E190060
_L 0x20370EC8 0x34180008//ColorCount
_L 0x20370ECC 0xA33800B0
_L 0x20370ED0 0x8FBF0018
_L 0x20370ED4 0x8FB00010
_L 0x20370ED8 0x03E00008
_L 0x20370EDC 0x27BD0020
_C0 Default colors for vehicles
_L 0xE001C3AC 0x002069A0
_L 0x202069A0 0x0E20FF79//Jal1
```

# Burnout Legends (June 6, 2005 GameSharing/Debug beta)

(all patches in this section by KabutoKun)

```
_C0 Traffic checking, ON
_L 0xE0013830 0x001B51AC
_L 0x00483830 0x00000001
_C0 Traffic checking, OFF
_L 0xE0013830 0x001B51AC
_L 0x00483830 0x00000000
```

```
_C0 Unlock debug menu BLgndsGS v1.1
_L 0xE0011440 0x0000D44A
_L 0x2000D448 0x10000002
_C0 Lock debug menu BLgndsGS v1.1, default
_L 0xE0011000 0x0000D44A
_L 0x2000D448 0x14400002
```

```
_C0 Redirect debug SaveData to memstick v1.1
_L 0xE012B728 0x002CA344
_L 0x202CA344 0x34B4EAB0//Path1Ptr
_L 0x202CA338 0x3C0508BC
_L 0x202CA340 0x0E2B22F8//DelaySlot
_L 0x202CA36C 0x340601FF
_L 0x203CEAB0 0x3A30736D//Path1,ms0
_L 0x203CEAB4 0x53474C42
_L 0x203CEAB8 0x7661535F
_L 0x203CEABC 0x74614465
_L 0x203CEAC0 0x00002F61
_L 0x202CA348 0x0E2F3AB4//Path2
_L 0x203CEAD0 0x90590000
_L 0x203CEAD4 0x3418002E
_L 0x203CEAD8 0x17190003
_L 0x203CEADC 0x3C0F4567
_L 0x203CEAE0 0x35EF6244
_L 0x203CEAE4 0xAC4F0000
_L 0x203CEAE8 0x03E00008
_L 0x203CEAEC 0x27A40020
```

^ You still need to create the directory structure before the above cheat will be able to work properly and save via the debug menu. [Save this CMD file](https://cdn.discordapp.com/attachments/548257604166615041/764538057462382612/CreateBLDIRs.cmd) to the root of your PPSSPP memstick (in the same directory as the PSP folder) and run it, it'll create the folders.

# Burnout Revenge (PS2, NTSC-U) [July 14th, 2005 build]

(all patches in this section by Speedyheart)

```
//Disable Bloom
patch=1,EE,21C29B48,byte,00000000 // 00000001
```

```
// don't render glow
patch=1,EE,00440223,word,00000000
```

```
//Force Lap COUNT
patch=1,EE,01F034E4,word,00000009
```

```
//Enable Lives in Road Rage?
patch=1,EE,0043C958,word,00000000
```

```
// Force Car Unlock Camera (Crashes After the camera)
patch=1,EE,004485B0,word,00000000`
```

```
//unlock all at title screen
patch=1,EE,0018EDE0,word,0812E07E
patch=1,EE,004B81F8,word,3C040055
patch=1,EE,004B81FC,word,0C0435EE 
patch=1,EE,004B8200,word,24848410
patch=1,EE,004B8204,word,3C1201C4
patch=1,EE,004B8208,word,3405961F
patch=1,EE,004B820c,word,08063B7A
patch=1,EE,004B8210,word,00000000
```

```
/ No UpdateRestricted
patch=1,EE,00180300,word,00000000
```

```
// No UpdateLocked
patch=1,EE,00180308,word,00000000
```

```
//Progression Stuff (defaults: 0, 1, 0, 1 respectively)
patch=1,EE,21F8B488,word,00000001
patch=1,EE,21F8B48C,word,00000001
patch=1,EE,21F8B490,word,00000001
patch=1,EE,21F8B494,word,00000001
```

```
//All Challenges Unlocked
patch=1,EE,00131380,word,146200BE
```

```
//Unlock All Cars
patch=1,EE,00130E44,word,10000064
```

```
//Challenge Sheets?
patch=1,EE,0013472C,word,10000003`
```

```
//Replace Progressive Scan Menu w/ Debug Menu
patch=1,EE,00434CFC,word,26B50BB0
```

```
//Unlock tracks 
patch=1,EE,0013106C,word,1000000A
patch=1,EE,00131084,word,1000000A
```

```
//volumes
patch=1,EE,00441B1C,word,3f800000
patch=1,EE,00441B18,word,3f800000
patch=1,EE,00441B14,word,3f800000
patch=1,EE,00441B10,word,3f800000
```

```
//world physics impulse scale (0.5 default)
patch=1,EE,004405F0,word,3f000000
```


# Burnout Revenge (PS2, NTSC-U)

```
//PCSX2 Speedhacks (patch by: escape209)
patch=1,EE,21BFE7B8,byte,00000000 // 00000001 // Bloom
patch=1,EE,21BFE7B9,byte,00000000 // 00000001 // Fog
patch=1,EE,21BFE7BA,byte,00000000 // 00000001 // Motion blur
```

# Burnout Dominator (PS2, NTSC-U)

```
//Disable Bloom (patch by: escape209)
patch=1,EE,2043E818,byte,00000000
```


# Burnout Dominator (PSP, USA)

```
//patch by: AcuteSyntax
_C0 Enable Motion Blur
_L 0x0054421A 0x00000001
_C1 Disable Motion Blur (default)
_L 0x0054421A 0x00000000
```

```
//patch by: KabutoKun
_C0 Traffic checking, ON
_L 0xE00123C4 0x001277B8
_L 0x003C23C4 0x00000001
_C1 Traffic checking, OFF
_L 0xE00123C4 0x001277B8
_L 0x003C23C4 0x00000000
```