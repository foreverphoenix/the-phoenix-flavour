---
title: "Documentation"
weight: 4
type: docs
description: >
  Notes and references for WTP.
---

## Game Folder Files

While regular mods for Bethesda games are installed into the **data** folder, there are some additional tools that belong into the **root** folder. These are not automatically moved by Wabbajack. Instructions for them are included in the **Installation** setup, this page merely serves as an overview over the files in question and their purpose.

> WTP does not use the Stock Game Folder system and likely never will.

#### Fallout 4 Script Extender

The [Fallout 4 Script Extender (F4SE)](http://f4se.silverlock.org/) is essential to modding Fallout 4 and required by many mods. Its executable and DLLs have to be inside the root folder.

- `f4se_1_10_163.dll`
- `f4se_loader.exe`
- `f4se_steam_loader.dll`

#### xSE Plugin Preloader

The [xSE Plugin Preloader F4](https://www.nexusmods.com/fallout4/mods/33946) is required for Buffout.

- `IpHlpAPI.dll`
- `xSE PluginPreloader.xml`

#### Buffout 4 TBB Redist

[Buffout 4](https://www.nexusmods.com/fallout4/mods/47359) requires the TBB library, a small plugin that needs to be placed in the root folder.

- `tbbmalloc.dll`

#### ENBSeries Binaries

The [ENBSeries for Fallout 4](http://enbdev.com/download_mod_fallout4.htm) binaries, required for ENB presets to work.

- `d3d11.dll`
- `d3dcompiler_46e.dll`

#### enblocal.ini

My personal enblocal.ini with customised hotkeys.

- `enblocal.ini`

#### Spectrum ENB

The [Spectrum ENB](https://www.nexusmods.com/fallout4/mods/58028) preset.

- `\enbseries\`
- `enbseries.ini`

## INI Settings

As usual, I have used [BethINI](https://www.nexusmods.com/fallout4/mods/67) to generate the INI files before adding some manual tweaks. The default INI set is based on the **High** preset while the performance INI set uses the **Medium** one.

- **VSYNC** is always turned off, it is forced through High FPS Physics Fix
- **Ambient occlusion** is always turned off, we are using ENB AO instead
- **TAA** is used for anti aliasing (as opposed to FXAA)
- **Godrays** are disabled in the performance INIs only

### Fallout4.ini

```
[Display]
fPipboyScreenEmitIntensityPA=1.25
fPipboyScreenDiffuseIntensityPA=0.15

[Pipboy]
bPipboyDisableFX=1
bPipboyEffectColorOnLight=0
fPAEffectColorB=0.392
fPAEffectColorG=0.722
fPAEffectColorR=0.376
```

### Fallout4Prefs.ini

```
[Display]
uPipboyTargetHeight=1400
uPipboyTargetWidth=1752

[Interface]
iHUDColorB=100
iHUDColorG=184
iHUDColorR=96

[Pipboy]
fPipboyEffectColorB=0.3920
fPipboyEffectColorG=0.7220
fPipboyEffectColorR=0.3760
```

## Visual Changes

Fallout 4 was never a particularly beautiful game, but it has solid graphics. Compared to older Fallout titles, it is a great deal more colourful and "cartoonish", no green filter like in Fallout 3 and no distinct dusty hue like in Fallout New Vegas.

In my changes for WTP, I have decided to stay faithful to the vanilla colours and style, opting to focus largely on improving texture quality. Any more profound changes such as a tree overhaul would have susbstantially increased the list's complexity due to FO4's precombine system which is the only thing that keeps performance from turning into a slide show.

### Weather & Lighting

Welcome to Paradise includes [Lightweight Lighting - A Weather and Interior Lighting Overhaul](https://www.nexusmods.com/fallout4/mods/57680) which subtly improves lighting while retaining the original colour palette. Combined with the lightweight [Spectrum ENB](https://www.nexusmods.com/fallout4/mods/58028) preset, it constitutes a solid upgrade over vanilla without changing the original style.

![WTP Day](/Pictures/wtp/documentation/wtp-day.jpg)

![WTP Dusk](/Pictures/wtp/documentation/wtp-dusk.jpg)

![WTP Night](/Pictures/wtp/documentation/wtp-night.jpg)

### Landscape

In keeping with the pledge to stick with the vanilla style, I added [Lush Landscapes](https://www.nexusmods.com/fallout4/mods/9292) (the "Dried" edition) as the grass overhaul which does a good job at improving vanilla's sparse vegetation. Water was greatly improved by [Water Enhancement Textures](https://www.nexusmods.com/fallout4/mods/20775) and [Wave Animation Vanilla Enhanced](https://www.nexusmods.com/fallout4/mods/41568).

![WTP Landscape](/Pictures/wtp/documentation/wtp-landscape.jpg)

## Texture Packs

In Fallout 4, loose assets can actually have a significant impact on performance and load time over BA2 packed assets, far more so than in Skyrim SE. This is why most mod authors pack up their assets in archives and it is why I have been religiously packing up most loose assets in WTP. On this page I am listing the mods that the individual textures and meshes in the custom WTP texture packs are from.

Note that the assets were *not* repackaged and redistributed. Each of the individual mods will be downloaded for you from their original mod pages by Wabbajack, then packed up into archives to match my own setup.

#### Texture Pack - Clutter

- [Grey Tortoise Cigarettes Redux](https://www.nexusmods.com/fallout4/mods/28204)
- [Bottles Label Overhaul](https://www.nexusmods.com/fallout4/mods/1500)
- [Sweet Roll 5000](https://www.nexusmods.com/fallout4/mods/32224)
- [Retextured Water - By Ben Ephla](https://www.nexusmods.com/fallout4/mods/20399)
- [Gold Bars - FNV Dead Money Inspired Replacer](https://www.nexusmods.com/fallout4/mods/45675)
- [Better Ammo Boxes](https://www.nexusmods.com/fallout4/mods/8087)
- [Duffle Bag Retexture 2K](https://www.nexusmods.com/fallout4/mods/8879)
- [Retextured First Aid Kids - Ephla's Unique First Aid](https://www.nexusmods.com/fallout4/mods/16841)
- [PatrickJr's Redone Bobbleheads](https://www.nexusmods.com/fallout4/mods/12062)
- [Classic Wasteland Survival Guide - Magazine Retexture](https://www.nexusmods.com/fallout4/mods/49999)
- [U.S. Covert Operations Manual Revised - Magazine Retexture](https://www.nexusmods.com/fallout4/mods/53012)
- [Total Hack - Magazine Retexture](https://www.nexusmods.com/fallout4/mods/50253)
- [Library and Subway Tokens HD Remastered](https://www.nexusmods.com/fallout4/mods/52206)
- [Globes 2K](https://www.nexusmods.com/fallout4/mods/34246)
- [Wall Worldmap](https://www.nexusmods.com/fallout4/mods/34014?tab=files)
- [ADs 2X Rez](https://www.nexusmods.com/fallout4/mods/37762)

#### Texture Pack - Apparel

- [Pipboy UHD 2K](https://www.nexusmods.com/fallout4/mods/40633)
- [Vault Suit UHD 4K](https://www.nexusmods.com/fallout4/mods/40952)
- [Combat Armor No Star Decal](https://www.nexusmods.com/fallout4/mods/524)
- [Robot Armor Retextured](https://www.nexusmods.com/fallout4/mods/12187)
- [Mechanist Armor Retextured](https://www.nexusmods.com/fallout4/mods/13053)
- [Marine Helmet with Tactical Hood](https://www.nexusmods.com/fallout4/mods/14340)
- [Piper's Coat HR](https://www.nexusmods.com/fallout4/mods/14010)
- [Better House Dress Shoes](https://www.nexusmods.com/fallout4/mods/36704)
- [Eyewear and Mask Retexture](https://www.nexusmods.com/fallout4/mods/5021)
- [Shorter Gas Masks](https://www.nexusmods.com/fallout4/mods/19272)

#### Texture Pack - Power Armors

- [Power Armors Redone](https://www.nexusmods.com/fallout4/mods/27917)
- [Power Armors Redone Extended - CPAO Textures](https://www.nexusmods.com/fallout4/mods/28033)
- [Power Armors Redone Extended - Minutemen Paint Job Textures](https://www.nexusmods.com/fallout4/mods/28033)
- [Power Armor Jetpack 2K HD](https://www.nexusmods.com/fallout4/mods/30796)
- [Matching White Brotherhood Rank Insignia](https://www.nexusmods.com/fallout4/mods/4092)

#### Texture Pack - Weapons

- [10mm HD](https://www.nexusmods.com/fallout4/mods/33107)
- [The Fantastic Forty Four](https://www.nexusmods.com/fallout4/mods/24398)
- [The Hunting Rifle Set](https://www.nexusmods.com/fallout4/mods/49185)
- [The Ballistic Series](https://www.nexusmods.com/fallout4/mods/49369)
- [Scratch Made - New Double Barrel Shotgun Textures](https://www.nexusmods.com/fallout4/mods/2211)
- [The Laser Series](https://www.nexusmods.com/fallout4/mods/48567)
- [CC's FUHD Institute Laser Weapons](https://www.nexusmods.com/fallout4/mods/37723)
- [The Plasma Project](https://www.nexusmods.com/fallout4/mods/48321)
- [The Meritable Minigun](https://www.nexusmods.com/fallout4/mods/24506)
- [Missile Launcher HD](https://www.nexusmods.com/fallout4/mods/33381)
- [The Fancy Fatman](https://www.nexusmods.com/fallout4/mods/24460)
- [Gauss Rifle UHD](https://www.nexusmods.com/fallout4/mods/41107)
- [The Flamer Project](https://www.nexusmods.com/fallout4/mods/51479)
- [Cryolator HD](https://www.nexusmods.com/fallout4/mods/31564)
- [Broadsider HD](https://www.nexusmods.com/fallout4/mods/31611)
- [Leafblower Junk Jet](https://www.nexusmods.com/fallout4/mods/51557)
- [The Delightful Deliverer](https://www.nexusmods.com/fallout4/mods/24813)
- [The Radical Ripper](https://www.nexusmods.com/fallout4/mods/24606)
- [Grognak's Axe](https://www.nexusmods.com/fallout4/mods/38644)
- [Kremvh's Tooth Replacer](https://www.nexusmods.com/fallout4/mods/6960)
- [M26 Fragmentation Grenade Replacer](https://www.nexusmods.com/fallout4/mods/37749)

#### Texture Pack - Creatures

- [Delightful Dead Fish](https://www.nexusmods.com/fallout4/mods/14726)
- [CC's UHD Bloatflies - Reimagined](https://www.nexusmods.com/fallout4/mods/53516)
- [CC's UHD Radscorpions](https://www.nexusmods.com/fallout4/mods/36533)
- [CC's Enhanced Vanilla Mirelurks](https://www.nexusmods.com/fallout4/mods/36434)
- [Protectron HD](https://www.nexusmods.com/fallout4/mods/15038)
- [Assaultron HD](https://www.nexusmods.com/fallout4/mods/36045)
- [CC's FUHD Sentry Bots](https://www.nexusmods.com/fallout4/mods/37680)
- [CC's Liberty Prime](https://www.nexusmods.com/fallout4/mods/53619)
- [CC's UHD Fog Crawlers](https://www.nexusmods.com/fallout4/mods/36857)
- [CC's UHD Aliens](https://www.nexusmods.com/fallout4/mods/36460)

## Gameplay Changes

WTP features a good amount of quality of life improvements. These include:

- [Start Me Up](https://www.nexusmods.com/fallout4/mods/18946): The Basic version of this mod included in WTP allows you to skip the pre-war part of the Prologue.
- [Consume Without Pickup](https://www.nexusmods.com/fallout4/mods/45072): Immediately use a Stimpak or eat that Radstag stew without having to pick it up first.
- [Baka Wait Anywhere](https://www.nexusmods.com/fallout4/mods/52723): Allows you to wait anywhere without having to sit down (but with a few conditions).
- [Automatically Lowered Weapons](https://www.nexusmods.com/fallout4/mods/20093): The player automatically lowers their weapon when not in combat.
- [Easy Lockpicking and Hacking](https://www.nexusmods.com/fallout4/mods/31527): Only the correct word appears when hacking. Locks can be picked without having to adjust the angle.

### Quest Adjustments

[No Quest Autostart series](https://www.nexusmods.com/fallout4/users/2652197?tab=user+files): The DLC quests will no longer start automatically upon reaching the required level. You will need to either listen to the associated radio broadcast or actively go to the related location. Note that the level requirements was not removed, but the quests will no longer be automatically added to your quest log.

[Keep Radiants in the Commonwealth](https://www.nexusmods.com/fallout4/mods/25934): Any radiant quests received in the Commonwealth will now always send you to locations within the Commonwealth (as opposed to DLC areas which they previously could).

[Preston Garvey No Radiant Settlement Quests](https://www.nexusmods.com/fallout4/mods/24940): After taking the Castle for the Minutemen, Preston Garvey will no longer give you radiant quests with the exception of those that you cannot get through the Radio Freedom broadcasts.

[Whose Quest Is It Anyway](https://www.nexusmods.com/fallout4/mods/51979): Upon attempting to remove a quest item from your inventory, you will now be notified which quest the item is locked by.

### Simple Crafting Station

All vanilla Chem Stations were renamed to "Crafting Stations" to account for the fact that you can craft pretty much anything at them. Their models were changed accordingly by [this excellent mod](https://www.nexusmods.com/fallout4/mods/44691).

Holotapes to configure a few mods were moved to a unique category at Crafting Stations called MOD CONFIG. They can now be crafted for free.

![Config Holotape Crafting](/Pictures/wtp/documentation/config-holotape-crafting.jpg)

### Photo Mode

WTP includes the amazing [Photo Mode](https://www.nexusmods.com/fallout4/mods/49997) by reg2k. It's the perfect tool for screenarchers, pause the game and find the perfect angle for a great picture. You can access it through ESCAPE menu or define a hotkey in the associated MCM.

## Power Armor

While WTP touches little on the gameplay side of things, I did change how power armors were distributed and how their paint jobs work to be quite different from vanilla.

### Distribution

Quick summary of the changes:

- You will find fewer full power armors sets and more separate pieces.
- T-45 and Raider power armor pieces will be more commonly found.
- T-51 power armor pieces will be more commonly found.
- T-60 power armor pieces can be found exclusively on Brotherhood troops.
- X-01 power armor pieces are rare. There are only two full sets in the Commonwealth.

In vanilla, one may be forgiven to think that before the bombs dropped every citizen of Boston had a set of power armor stored in their backyard. There are just so bloody many of them! In order to cut down the amount of armors you find, I added [Some Assembly Required](https://www.nexusmods.com/fallout4/mods/12050) for its hand-placed power armor pieces (and removed everything else it did). In most locations where before there was a power armor frame often with a full set, you will now find separate pieces or other rare loot. Additionally, pieces of Raider, T-45, or (rarely) T-51 power armor were hand-placed in various locations around the Commonwealth.

Since this change means there will be far fewer frames found in the world, I added [Restore Power Armor Frames](https://www.nexusmods.com/fallout4/mods/20890) which will allow you to extract the frames from dead NPCs.

According to lore, **T-60 power armor** had not yet replaced the T-51 in the standard army loadout before the bombs dropped and did not enter mass-production until the Brotherhood of Steel procured the means to do so much later on. As such it makes no sense for T-60 sets to be significantly more common than T-51 in the Commonwealth. In WTP, T-60 sets are given exclusively to Brotherhood troops. Atom Cats now wear T-45 power armor sets instead of T-60. The only T-60 set you can find outside of the Brotherhood is the [Tesla](https://fallout.fandom.com/wiki/Tesla_T-60_armor) variant from the Automatron DLC.

There is one full set of T-51 power armor including frame and fusion core in a heavily fortified location. See the SPOILER SECTION at the bottom if you want to know where to find it.

In the levelled lists, T-60 pieces were replaced by T-45 pieces and X-01 pieces were replaced by T-51 pieces.

As for **X-01 power armor**, there are only two full sets to be found: One of them is the [Quantum X-01](https://fallout.fandom.com/wiki/Quantum_X-01_power_armor) from the Nuka World DLC. The second consists of regular X-01 pieces you will have to gather from various locations around the Commonwealth. Scroll to the bottom of this page to the SPOILER SECTION to find out where exactly those six pieces can be found.

### Paint Jobs

In vanilla, many paint jobs also have non-cosmetic effects such as stat increases. The mod [Power Armor Materials AND Paints](https://www.nexusmods.com/fallout4/mods/4619) separates these two so you can control the paint job and "material" (the non-cosmetic buffs) separately. This required some integration patching with other power armor mods added in WTP.

Paint jobs now all cost 2 oil and 2 steel to apply (matching the Creation Club paint jobs). They no longer increase weight or value of the armor piece and will not yield a loose mod upon swapping to a different one.

Additionally, paint jobs were made available for a greater variety of power armor pieces by [Consistent Power Armor Overhaul](https://www.nexusmods.com/fallout4/mods/11234) and [Minutemen Paint Job](https://www.nexusmods.com/fallout4/mods/28029). Both of those mods are supported by the amazing [Power Armors Redone Extended](https://www.nexusmods.com/fallout4/mods/28033) so the new paint job variants are of the same style and quality as the vanilla power armors retextured by [Power Armors Redone](https://www.nexusmods.com/fallout4/mods/27917).

| Paint Jobs           | T-45 | T-51 | T-60 | X-01 |
| -------------------- | ---- | ---- | ---- | ---- |
| Factory              | x    | x    | x    | x    |
| Winterized (white)   | x    | x    | x    | x    |
| Military (olive)     | x    | x    | x    | x    |
| Brotherhood of Steel | x    | x    | x    | x    |
| Minutemen            | x    | x    | x    | x    |
| Vault-Tec            | x    | x    | x    | x    |
| Railroad             | -    | x    | -    | -    |
| Institute            | -    | -    | -    | x    |
| Atom Cats            | x    | x    | x    | x    |
| Hot Rod Flames       | x    | x    | x    | x    |
| Hot Rod Shark        | x    | x    | x    | x    |
| Hot Rod Hot Pink     | x    | x    | x    | x    |
| Vim!                 | -    | x    | -    | -    |
| Vim! Refresh         | -    | x    | -    | -    |
| Sugar Bombs          | -    | x    | -    | -    |
| Abraxo               | -    | x    | -    | -    |

> The Brotherhood of Steel paint job has multiple variants for any PA Left Arm pieces to display your rank insignia (Knight, Sentinel, Paragon). For all other pieces, there is only a single "Brotherhood of Steel" paint job as there are no rank-specific decals for them.

The **Abraxo** and **Sugar Bombs** paint jobs for the T-51 (added by the Contraptions DLC) will no longer be available by default. You need to find special promotional holotapes for each to unlock the paint jobs. Their locations are listed in the SPOILER SECTION at the bottom of this page.

The **Vault-Tec** paint job for the T-45, T-51, T-60, and X-01 power armors is similarly disabled at the start of the game and can be unlocked by a holotape. You can find it in the Overseer's office of any vault.

### Other Changes

[Power Armor Animation Changes](https://www.nexusmods.com/fallout4/mods/4408) makes entering and exiting your power armor out of combat much faster. Upon exiting your power armor frame, your fusion core will immediately be placed in your inventory thanks to [Take Your Cores](https://www.nexusmods.com/fallout4/mods/14773). This saves you from having to grab them manually. If you leave the cores in, NPCs like your settlers may decide to take your power armor for a walk and they don't always return it either. [No PA Battery Pathing](https://www.nexusmods.com/fallout4/mods/33080) removes the dreaded struggle of getting behind your power armor and slotting in the fusion core which in vanilla, if you get stuck, lasts up to 16 seconds.

## Settlement Building

The building system was generally improved by the following mods:

- [Place Everywhere](https://www.nexusmods.com/fallout4/mods/9424) removes the dreaded red outlines. You can now build anywhere and have much finer movement controls.
- [New Infinite Settlement Budget Plugin](https://www.nexusmods.com/fallout4/mods/16939) significantly increases the building budget (so be careful).
- [Visible Idle Markers](https://www.nexusmods.com/fallout4/mods/46453) helps prevent building objects on idle markers which NPCs would clip through to reach the marker.
  
**Building objects in settlements no longer grants XP.**

> The more objects you place in a settlement (or technically the higher the overall polycount of all object gets), the more performance will degrade. With the expanded building budget it is now up to the player to decorate carefully and mind the framerate.

### Scrapping Machine

The mod [Scrapping Machine](https://www.nexusmods.com/fallout4/mods/35793) adds some very useful ~~washing~~ scrapping machines that you can build in your workshop. Any junk items placed inside will be broken down into their base scrap. This is extremely useful because junk broken down for components when crafting or building may cause unused base scrap to be lost.

![WTP Scrap 1](/Pictures/wtp/documentation/wtp-scrap-1.jpg)

![WTP Scrap 2](/Pictures/wtp/documentation/wtp-scrap-2.jpg)

![WTP Scrap 3](/Pictures/wtp/documentation/wtp-scrap-3.jpg)

## Keybinds

WTP comes with a bunch of custom hotkeys, all of which can be configured in MCMs or INI files.

#### ENBSeries

Hotkeys for ENB can be adjusted in the `enblocal.ini` (located in the root folder). [Here](https://keycode.info/) is a great website to quickly figure out the keycode for any key by simply pressing it.

- **F8** Toggle FPS Counter
- **F10** Toggle ENB Effect
- **F11** Open ENB GUI

#### Workshop

- **Y** Open the Workshop (Faster Workshop)
- **F1** Toggle Place Everywhere (can build objects anywhere)
- **F2** Toggle Snapping (requires Place Everywhere mode to be on)

#### HUD

- **V** Toggle HUD (if Immersive HUD is enabled)
- **H** Toggle clock widget (if HoloTime is enabled)

#### Other

- **P** Open Photo Mode
- **CTRL + B** Toggle Radio
- **CTRL + G** Use Stimpak

## New Content

### Additional Music

WTP both adds new tracks to the background music as well as to the Diamond City radio. The new additions were carefully selected to match the vanilla atmosphere so as not pull you out of the game.

The following mods expand the game's soundtrack:

- [Musical Lore - Wasteland Edition](https://www.nexusmods.com/fallout4/mods/14531)
- [Fallout Suite - Soundtrack Extension for Fallout 4](https://www.nexusmods.com/fallout4/mods/15870)
- [Bleak Beauty - A Fallout 4 Fan Made OST](https://www.nexusmods.com/fallout4/mods/9663)

> The music mods' individual plugins were replaced by a patched and merged one.

[Diamond City Radio Extended](https://www.nexusmods.com/fallout4/mods/56898) adds over 140 new songs to the radio's catalogue.

### Pip-Boy Color Variations

[Pip Boy Retextured](https://www.nexusmods.com/fallout4/mods/47858) adds eight new colour variations (paint jobs) for the Pip Boy like the Creation ones but for free. You can change your Pip Boy's paint job whenever you like at any Armor Workbench.

### K-9 Harness

I'm a huge fan of fadingsignal's [K-9 Harness](https://www.nexusmods.com/fallout4/mods/17686) for Dogmeat so I had to add it to WTP. Instead of it being craftable, I have placed one harness in a location that fits thematically. Either trust that you will find it naturally on your travels or check the SPOILER SECTION at the bottom of this page if you want to know where it is.

### CC Modular Military Backpack

Also by fadingsignal is the [Modular Military Backpack](https://fallout.fandom.com/wiki/Modular_military_backpack) which matches the K-9 Harness beautifully. It is a Creation so you will need to buy it from the Creation Club. There are instructions for installing the Creation in WTP on the [Installation](/fo4/wtp/installation/#creation-club) page.

Note that the backpack will no longer be given to you upon leaving Vault 111 and it will not be distributed either. You can find a single one within Vault 111 that you can pick up at the start of the game.

![CC Backpack](/Pictures/wtp/documentation/cc-backpack.jpg)

## SPOILER SECTION

**PLEASE DO NOT KEEP SCROLLING IF YOU DON'T WANT TO KNOW WHERE VARIOUS RARE ITEMS ARE FOUND.**

### X-01 Power Armor

You can find X-01 power armor pieces in the following locations:

- [The Prydwen](https://fallout.fandom.com/wiki/The_Prydwen): X-01 Helmet (vanilla)
- [Old Gullet Sinkhole](https://fallout.fandom.com/wiki/Old_Gullet_sinkhole): X-01 Left Arm
- [Boxing Gym](https://fallout.fandom.com/wiki/Boxing_gym): X-01 Right Armor
- [Museum of Witchcraft](https://fallout.fandom.com/wiki/Museum_of_Witchcraft): X-01 Torso
- [Greenetech Genetics](https://fallout.fandom.com/wiki/Greenetech_Genetics): X-01 Left Leg
- [O'Neill Family Manufacturing](https://fallout.fandom.com/wiki/O%27Neill_Family_Manufacturing): X-01 Right Leg

### Full T-51 Set

There is a full suit of T-51 on the rooftop of the [35 Court](https://fallout.fandom.com/wiki/35_Court) in the Financial District, downtown Boston.

### PA Paint Jobs

You can find holotapes to unlock certain power armor paint jobs in the following locations:

- [Super-Duper Mart](https://fallout.fandom.com/wiki/Super_Duper_Mart_(Fallout_4)): Sugar Bombs paint job (T-51)
- [Charlestown Laundry](https://fallout.fandom.com/wiki/Charlestown_laundry): Abraxo paint job (T-51)

### K-9 Harness

Can be found at the [Malden police station](https://fallout.fandom.com/wiki/Malden_police_station), upstairs.