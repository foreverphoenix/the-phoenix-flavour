---
title: "Introduction"
weight: 1
type: docs
description: >
  About Skyrim Modding Essentials.
---

**Skyrim Modding Essentials** is a Wabbajack utility list for Skyrim Special Edition, intended to jumpstart a new mod setup with all the required tools and basic mods. As such, it is intended for *experienced* modders and no support will be provided beyond the contents of the list itself. 

The list was made for Skyrim SE 1.6.x, though the Anniversary Edition DLC is not required.

Support is available on the [Aetherius Modding](https://discord.gg/xRrHRsb5e9) Discord server.

## Features

Check the complete mod list and load order on [Load Order Library](https://loadorderlibrary.com/lists/skyrim-modding-essentials).

- A lean, basic setup clocking in at around 3.8GB plus less than 1GB of downloads.
- Latest stable version of [Mod Organizer 2](https://www.nexusmods.com/skyrimspecialedition/mods/6194) installed with a separate copy of the vanilla game (Stock Game Folder).
- A collection of handy Mod Organizer 2 plugins for various purposes, [see the full list here](/skyrim-se/sme/documentation/#mo2-plugins).
- All modding tools you could possibly need are included and pre-configured, [see the full list here](/skyrim-se/sme/documentation/#modding-tools).
- [Skyrim Script Extender](https://skse.silverlock.org/) with a correctly configured SKSE.ini file and [Address Library for SKSE Plugins](https://www.nexusmods.com/skyrimspecialedition/mods/32444).
- All the essentials, including but not limited to [MCM Helper](https://www.nexusmods.com/skyrimspecialedition/mods/53000), [SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/12604), and [SSE Display Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/34705).
- Clean MO2 setup with documentation for all changes in the Notes and further documentation on the [website](/skyrim-se/sme/documentation/).
- The foundational collections of tweaks and fixes: [SSE Engine Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/17230), [po3's Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/51073), [Scrambled Bugs](https://www.nexusmods.com/skyrimspecialedition/mods/43532).
- Additional fixes that should be relevant for and compatible with any setup with [further recommendations](/skyrim-se/sme/recommendations/).
- Optionally includes full widescreen support with all relevant patches.
- Optionally includes ENB binaries, premade enblocal.ini, and supplementary mods.

SME uses the Stock Game folder system. That means the setup includes a unique copy of your vanilla game, ensuring the setup is completely standalone and whatever you keep in your default installation folder will not affect the setup at all. This is a lifesaver when you keep more than one instance of MO2. Setting up all tools for Stock Game folder can be a little annoying so you're welcome, it's all done for you.

## Installation

Please refer to the [Installation](/skyrim-se/sme/installation/) page.

## FAQ

**What about VSYNC?**

VSYNC is forced through SSE Display Tweaks by default which is preferable to Skyrim's native VSYNC, or ENB VSYNC. In other words, there is nothing you need to change.

**How do I enable widescreen support?**

Check all the mods from the Widescreen Support section. The monitor resolution should be set correctly by default.

**Are any texture replacers included?**

No, because I wanted to keep the list as lean as possible and because there is no point. For those who wish to have improved vanilla textures, just grab [Project Clarity](https://www.nexusmods.com/skyrimspecialedition/mods/45306). Everyone else has their preferred texture packs, or they're completely nuts and hand-pick everything (don't look at me like that, I know I'm not the only one who does it). Similarly, there are no LODs. Do 'em yourself, that's what the list is for.

**Can I suggest a mod for inclusion?**

Yes, you can! Please do so on our [Discord Server](https://discord.gg/xRrHRsb5e9) and be aware that the likelihood that I will say "no" is quite high. Because this list has to provide a good base for *any* setup, the criteria for new additions are quite strict.

#### Why isn't X mod included?

[FileAccess Interface for Skyrim SE Scripts (FISSES)](https://www.nexusmods.com/skyrimspecialedition/mods/13956): Not included because it tends to become unstable when it is used to load presets for multiple MCMs. Mod authors should use [MCM Helper](https://www.nexusmods.com/skyrimspecialedition/mods/53000) to make saving MCM configurations easy and convenient.

The mesh fixes section is very incomplete, but I refrained from adding several mods because of how sensitive to conflicts they are. Figuring out your setup's meshes is somewhat time-consuming and depends on whether you use split meshes to minimise flickering (grab [Flickering Meshes Fix](https://www.nexusmods.com/skyrimspecialedition/mods/53957)) and whether you use parallax. Additionally, many mesh fix mods have a lot of overlap with other mods which at times include them, modified or as-is. Finally, mods like [Fixed Mesh Lighting](https://www.nexusmods.com/skyrimspecialedition/mods/53653) (highly recommended) include many patches which, again, depend on your own setup. Completing this section is therefore up to you.

(To be expanded.)

## Credits

- Thanks to **Luca** for the original SMEFT list and the cover image for SME!
- Thanks to **Althro** for [documenting the stock game setup](https://github.com/The-Animonculory/Modding-Resources) because my dumb ass can never remember it.