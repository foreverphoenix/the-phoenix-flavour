---
title: "Customisation"
weight: 3
type: docs
description: >
  Small tweaks anyone can do for Legends of the Frost.
---

## Uncap the framerate

Thanks to [SSE Display Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/34705), it is absolutely possible to play Skyrim SE at above 60FPS without breaking the game. In my experience, the likelyhood of (minor) physics bugs occuring increases with the framerate which is why I personally prefer capping at 60FPS. You can also try capping at 75FPS or 90FPS if you really want a higher framerate. Due to LOTF's performance-friendly nature, you should be able to achieve such framerates on most PCs.

To change the FPS cap, you need to edit the INI file for SSE Display Tweaks:

- In **Mod Organizer 2**, expand the **ESSENTIALS** separator.
- Double-click **SSE Display Tweaks - LOTF Settings**.
- Switch to the **INI Files** tab and select the **SSEDisplayTweaks.ini**.
- Change the value for `FramerateLimit=` to your liking.
- Press **CTRL + S** to save your changes and close the window.

![LOTF Uncap Framerate](/Pictures/lotf/customisation/lotf-uncap-framerate.png)

## Interface Adjustments

### Enable Roboto Font Replacer

I am personally partial to [Roboto](https://www.nexusmods.com/skyrimspecialedition/mods/1779) for my font in Skyrim. You can enable (or disable) the font replacer any time:

- In **Mod Organizer 2**, expand the **INTERFACE** separator.
- Check the mod **Roboto Font Replacer**.

### Enable dot crosshair

If you prefer a subtle dot over the vanilla crosshair, follow these steps:

- In **Mod Organizer 2**, expand the **INTERFACE** separator.
- Check the mod **SkyHUD - White Dot Crosshair**.

### Enable 24h time format

If you prefer a 24h time format over the 12h one (e.g., 23h instead of 11pm), do this:

- In **Mod Organizer 2**, expand the **INTERFACE** separator.
- Check the mod **Time Format Changer**.

### Access the Creation Club

If you want to access the Creation Club through the main menu, do the following:

- In **Mod Organizer 2**, expand the **INTERFACE** separator.
- Uncheck the mod **ReCleaned Menu**.

## Gameplay Adjustments

### Change sprinting from toggle to hold

If you want to be able to hold the Sprint key to sprint instead of press it once to toggle, do this:

- In **Mod Organizer 2**, expand the **IMPROVED CONTROLS** separator.
- Check the mod **Classic Sprinting Redone**.

### Skip Lockpicking

If you are tired of the lockpicking minigame, I included a mod to skip it. Interacting with a locked container will unlock it, but consume lockpicks based on the lock difficulty.

- In **Mod Organizer 2**, expand the **SKSE & NET PLUGINS** separator.
- Check the mod **No Lock Picking**.

### Increase combat difficulty

If you find combat to be too easy, it is advisable to disable the Blade & Blunt vanilla damage modifiers plugin before increasing the difficulty through the game settings:

- In **Mod Organizer 2**, expand the **GAMEPLAY** separator.
- Uncheck the mod **Blade and Bunt - Vanilla Difficulty Modifiers**.

### Enable Barenziah Quest Markers

Finding all 24 Stones of Barenziah during the [No Stone Unturned](https://en.uesp.net/wiki/Skyrim:No_Stone_Unturned) quest can be a bit of a slog. If you would prefer quest markers to show you exactly where the stones are located, turn on this option in the **SSoB** MCM:

![SSoB MCM](/Pictures/lotf/lotf-ssob-mcm.jpg)

## Visual Adjustments

### Swap to Obsidian Weathers

By default, LOTF is running [Wander - A Weather Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/24439) with an older, tweaked version of [Yuevie's Minimal ENB](https://www.nexusmods.com/skyrimspecialedition/mods/37098). However, you can swap this out with the pre-installed [Obsidian Weathers and Seasons](https://www.nexusmods.com/skyrimspecialedition/mods/12125). If you are swapping to Obsidian Weathers it is also recommended to install The Truth ENB preset (see following section).

> **Important:** If you are swapping mid-playthrough, you need to first force default weather through the console (type `fw 81a` and press Enter), then go into an interior cell. Save the game, close it. Disable Wander, Wander Less Intense Fogs, and AOS Wander Patch. Load your save and save again. Quit. Enable Obsidian Weathers and related mods. Load your save and resume your playthrough.

- Double-click the **WEATHER & LIGHTING** separator to expand it.
- Disable the Wander related mods and enable the Obsidian Weathers related mods:

![Obsidian Weathers 1](/Pictures/lotf/customisation/obsidian-weathers-1.png)

- Double-click the **SOUNDS & MUSIC** separator to expand it.
- Disable the AOS Wander Patch and enable the AOS OBsidian Patch:

![Obsidian Weathers 2](/Pictures/lotf/customisation/obsidian-weathers-2.png)

- In the load order, position the new plugins as shown below:

![Obsidian Weathers 3](/Pictures/lotf/customisation/obsidian-weathers-3.png)

### Swap to The Truth ENB

The Truth ENB is a fantastic preset that I initially wanted to install for LOTF. Unfortunately, the author believes the Nexus' TOS to be infringing upon mod authors' rights and decided to move the preset to the AFKMods website which does not have the server capacity to support Wabbajack. Thus, the preset needs to be downloaded manually by any user wishing to install it.

I personally believe that the extra steps required for the Truth ENB are more than worth it as the preset looks amazing, especially with Obsidian Weathers (though it should look good with Wander as well).

- Create an account on the [AFKMods](https://www.afkmods.com/) website.
- Download the [Truth ENB](https://www.afkmods.com/index.php?/files/file/2241-the-truth-enb/) preset from the linked page.

![Truth ENB 1](/Pictures/lotf/customisation/truth-enb-1.png)

- Navigate to your root folder: `\Legends of the Frost\Stock Game\`.
- Delete the **enbcache** and **enbseries** folders as well as the **enbseries.ini**.

This will fully remove the previously installed ENB preset without removing ENB (d3d11.dll, d3dcompiler_46e.dll) or my customised ENB settings (enblocal.ini). If you decide to switch back at any point, you can find a backup of all LOTF preset and ENB files under `\Legends of the Frost\mods\LOTF Wander ENB (Backup)\`.

- Open the downloaded The Truth ENB archive.
- Extract the **enbseries** folder and **enbseries.ini** file into your Stock Game folder.

![Truth ENB 2](/Pictures/lotf/customisation/truth-enb-2.png)

I personally set `EnableRainWetSurfaces` to false in the preset (I do not like the effect at all). This can be done ingame through the UI or in the enbseries.ini in the Stock Game folder.

Additionally, it is recommended to disable Skyrim's volumetric light (godrays) as the Truth preset has ENB godrays enabled by default. Refer to the picture below for instructions.

> Note that INI tweaks are reset when updating LOTF.

![Truth ENB 3](/Pictures/lotf/customisation/truth-enb-3.png)

### Completely Remove ENB

For those who really struggle with performance, disabling ENB altogether may provide a welcome performance boost although I would recommend trying the performance profile first. You can temporarily toggle off ENB ingame by pressing F12 to see the difference in visuals and performance (enable the FPS counter with F8 to check your framerate).

If you really want to disable ENB, all you need to do is delete the **d3d11.dll** from `\Legends of the Frost\Stock Game\`.

In addition, please also disable one mod depending on ENB complex particle lights:

- In Mod Organizer 2, double-click the **WEATHER & LIGHTING** separator to expand it.
- Disable the **Radiant - Candles** mod which would make candles look weird without ENB.

You can also re-enable ambient occlusion to replace ENB ambient occlusion. The effect comes with a performance impact as well as a noticable visual improvement:

![Enable SSE AO](/Pictures/lotf/customisation/enable-sse-ao.png)