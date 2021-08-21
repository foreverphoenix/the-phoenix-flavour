---
title: "Introduction"
weight: 1
type: docs
description: >
  About Legends of the Frost.
---

## About Legends of the Frost

*What if Skyrim, but better?*

**Legends of the Frost** (LOTF) is a Wabbajack list for Skyrim SE. It is the lightest list I could conceive of, designed to be as close to vanilla as possible while bringing some much needed improvements to texture sharpness, distant terrain, and certain gameplay mechanics. I created it because for all my years of ~~playing~~ modding Skyrim SE I never finished the main quest once. With any other setup, I get caught in the same loop as most people: Updating, rebuilding, starting over again. LOTF is my attempt to fix that.

- **LOTF** is a small list in scope, strictly limited to fixing vanilla annoyances.
- **LOTF** features better distant terrain, sharper textures, and improved combat.
- **LOTF** does not come with an ENB preset and is very light on performance.
- **LOTF** will not receive updates requiring a new save for the forseeable future.

While future updates will almost certainly change them, here is what LOTF looks like in numbers:

- **Installation:** ~46GB
- **Downloads:** ~31GB
- **Mod Count:** 173
- **Plugin Count:** 98

> The file size is largely inflated by Base Coat and Skyrim Realistic Overhaul (the texture replacers) as well as the remastered audio files and generated outputs for LODs and facegen. 

### Features

- All essentials are installed, including the Skyrim Script Extender, the USSEP, and SSE Display Tweaks.
- A plethora of fixes and tweaks for a smoother vanilla-like experience.
- Fixed green-tinted blonde hair, weirdly bright falling leaves at night, and more.
- **More lush trees, actually 3D roads, less oily water**, and many other visual improvements.
- All textures replaced by cleaned and upscaled versions, courtesy of [Base Coat](https://www.nexusmods.com/skyrimspecialedition/mods/46850).
- Vanilla-like but higher quality textures for many objects provided by [Skyrim Realistic Overhaul](https://www.moddb.com/mods/skyrim-realistic-overhaul).
- Improved weathers with [Wander - A Weather Mod](https://www.nexusmods.com/skyrimspecialedition/mods/24439) consistent with the vanilla style and colours.
- Modern interface thanks to [SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/12604). The HUD is toggleable with [Immersive HUD](https://www.nexusmods.com/skyrimspecialedition/mods/12440).
- More resource management-oriented combat with [Blade and Blunt](https://www.nexusmods.com/skyrimspecialedition/mods/34549) (and vanilla damage modifiers).
- Better sound quality with the [Unofficial High Definition Audio Project](https://www.nexusmods.com/skyrimspecialedition/mods/18115) and [Audio Overhaul for Skyrim](https://www.nexusmods.com/skyrimspecialedition/mods/12466).

Legends of the Frost features rebuilt terrain LOD with [SSELODGen](https://stepmodifications.org/forum/topic/13451-xlodgen-terrain-lod-beta-84-for-fnv-fo3-fo4-fo4vr-tes5-sse-tes5vr-enderal-enderalse/?ct=1629204990) as well as highly improved object LOD and hybrid tree LOD generated with [DynDOLOD](https://www.nexusmods.com/skyrimspecialedition/mods/32382). All **facegen for vanilla NPCs was recreated** at twice the vanilla resolution with higher quality assets.

Please check the [Documentation](/lotf/documentation/) for more details on the included mods and why they were included, or check out the [Load Order Library](https://loadorderlibrary.com/lists/legends-of-the-frost) page for the full mod list and load order.

### Performance

LOTF has **no significant performance impact**. It was not designed to be a "lite" list -  I am using the BethINI High preset as well as DynDOLOD on High with hybrid trees - but the absence of an ENB preset should still make the list more than playable on all but the weakest PCs. While I relied almost exclusively on **Skyrim Realistic Overhaul** for textures which has largely vanilla-sized textures, DynDOLOD does increase the amount of VRAM required.

I personally play @1440p60FPS on a rather high-end PC (i7 10700k, RTX 3080) and barely ever dropped below 144FPS when I uncapped the framerate for testing purposes.

### About the name

Just like my Fallout 4 list is named after one of my favourite songs, I picked "Legends of the Frost" as tribute to the incredible [Miracle of Sound](https://www.youtube.com/channel/UCSfoxYTlCPFfglckBLrjpsA) (he's brilliant, his music is amazing, check him out). Way back in 2012, he collaborated with the equally amazing [Malukah](https://www.youtube.com/user/malufenix) on a Skyrim-themed song called, you guessed it, [Legends of the Frost](https://www.youtube.com/watch?v=0FLQ4rACE-0). It's one of his oldest songs, but it holds up very well and I love how well he captured the atmosphere of the game (as he always does).

## Installation

**Legends of the Frost** can only be installed via [Wabbajack](https://www.wabbajack.org/#/). There is no manual guide.

- To properly set up Skyrim SE for LOTF, [follow these instructions](/wj/wj-sse/game-setup/).
- To install LOTF through Wabbajack, [follow these instructions](/wj/wj-sse/list-installation/).

### MCM Instructions

LOTF only has a handful of Mod Configuration Menus (MCMs), most of which you should not need to touch. For instance, the **Radiant Requirements** MCM is already set up correctly with levels matching **Arena's** encounter zones thanks to the installed preset. However, you may wish to customise **Immersive HUD** in its MCM (change the hotkey, or adjust the transparency of various HUD elements) which can be done anytime.

## Customisation

LOTF is a very small list and I do not expect that I will ever much customisation options. However, there are a few small changes that you can make:

### Uncap the framerate

Thanks to [SSE Display Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/34705), it is absolutely possible to play Skyrim SE at above 60FPS without breaking the game. In my experience, the likelyhood of (minor) physics bugs occuring increases with the framerate which is why I personally prefer capping at 60FPS. You can also try capping at 75FPS or 90FPS if you really want a higher framerate. Due to LOTF's performance-light nature, you should be able to achieve such framerates on most PCs.

To change the FPS cap, you need to edit the INI file for SSE Display Tweaks:

- In **Mod Organizer 2**, expand the **ESSENTIALS** separator.
- Double-click the mod **SSE Display Tweaks**.
- Switch to the **INI Files** tab and select the **SSEDisplayTweaks.ini**.
- Scroll down to `FramerateLimit=` (around **Line 207**) and adjust the value to your liking.
- Press **CTRL + S** to save your changes and close the window.

![LOTF Uncap Framerate](/Pictures/lotf/lotf-uncap-framerate.png)

### Revert to vanilla font

If you prefer the vanilla font over my choice, Roboto, you can disable the font replacer anytime:

- In **Mod Organizer 2**, expand the **INTERFACE** separator.
- Uncheck the mod **Roboto Font Replacer**.

### Enable dot crosshair

If you prefer a subtle dot over the vanilla crosshair, follow these steps:

- In **Mod Organizer 2**, expand the **INTERFACE** separator.
- Check the mod **SkyHUD - White Dot Crosshair**.

### Access the Creation Club

If you want to access the Creation Club, through the main menu, do the following:

- In **Mod Organizer 2**, expand the **INTERFACE** separator.
- Uncheck the mod **ReCleaned Menu**.

### Enable Barenziah Quest Markers

Finding all 24 Stones of Barenziah during the [No Stone Unturned](https://en.uesp.net/wiki/Skyrim:No_Stone_Unturned) quest can be a bit of a slog. If you would prefer quest markers to show you exactly where the stones are located, turn on this option in the **SSoB** MCM:

![SSoB MCM](/Pictures/lotf/lotf-ssob-mcm.jpg)