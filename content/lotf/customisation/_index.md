---
title: "Customisation"
weight: 3
type: docs
description: >
  Various supported tweaks for Legends of the Frost.
---

## Performance INIs

If you want to squeeze some extra frames out of LOTF, but also want to keep the 3D tree LOD from the regular profile or the AE support from the Creation Club profile, you can do so by copying over the INI files from the Performance profile. Among other things, the Performance INIs have lowered settings for distant terrain, renders grass and shadows at a shorter distance, and disables volumetric lighting (godrays). They still have the default shadow resolution (2K) and ambient occlusion enabled.

- Navigate to `\Legends of the Frost\profiles\Legends of the Frost - Performance\`.
- Copy the **Skyrim.ini** and **SkyrimPrefs.ini** inside.

If you want to play on the regular (non-CC) profile, paste the INIs to:

- `\Legends of the Frost\profiles\Legends of the Frost\`

If you want to play on the Creation Club profile, paste the INIs to:

- `\Legends of the Frost\profiles\Legends of the Frost - Creation Club\`

**Confirm to overwrite existing INIs.**

## Higher or Uncapped FPS

Thanks to [SSE Display Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/34705), it is absolutely possible to play Skyrim SE at above 60FPS without breaking the game. In my experience, the likelyhood of (minor) physics bugs occuring increases with the framerate which is why I personally prefer capping at 60FPS. You can also try capping at 75FPS or 90FPS if you really want a higher framerate. Due to LOTF's performance-friendly nature, you should be able to achieve such framerates on most PCs.

To change the FPS cap, you need to edit the INI file for SSE Display Tweaks:

- In **Mod Organizer 2**, expand the **ESSENTIALS** separator.
- Double-click **SSE Display Tweaks - LOTF Settings**.
- Switch to the **INI Files** tab and select the **SSEDisplayTweaks.ini**.
- Change the value for `FramerateLimit=` to your liking.
- Press **CTRL + S** to save your changes and close the window.

![LOTF Uncap Framerate](/Pictures/lotf/customisation/lotf-uncap-framerate.png)

## Widescreen Support

The user interface mods included with LOTF (as well as the vanilla Skyrim UI) are optimised for 16:9 monitors (i.e., resolutions like 1920x1080, 2560x1440, 3840×2160). Anyone playing on ultrawide monitors (2560x1080 or 3440x1440) will need a few extra patches in order to make the user interface scale properly. These are preinstalled in LOTF and need only be activated.

- Enable all four widescreen patches below the **INTERFACE** separator:

![Enable Widescreen Patches](/Pictures/lotf/customisation/enable-widescreen-patches.png)

## Obsidian Weathers

By default, LOTF is running [Wander - A Weather Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/24439); however, you can swap this out with the pre-installed [Obsidian Weathers and Seasons](https://www.nexusmods.com/skyrimspecialedition/mods/12125). For best results, also install **The Truth ENB** (see [ENB for LOTF](/lotf/enb-for-lotf/) page).

> **Important:** If you are swapping mid-playthrough, you need to first force a default (vanilla) weather through the console (type `fw 81a` and press Enter), then go into an interior cell. Save the game, close it. Disable Wander, Wander Less Intense Fogs, and AOS Wander Patch. Load your save and save again. Quit. Enable Obsidian Weathers and related mods. Load your save and resume your playthrough.

- Double-click the **WEATHER & LIGHTING** separator to expand it.
- Disable the Wander related mods and enable the Obsidian Weathers related mods:

![Obsidian Weathers 1](/Pictures/lotf/customisation/obsidian-weathers-1.png)

- Double-click the **SOUNDS & MUSIC** separator to expand it.
- Disable the AOS Wander Patch and enable the AOS Obsidian Patch:

![Obsidian Weathers 2](/Pictures/lotf/customisation/obsidian-weathers-2.png)

- In the load order, position the new plugins as shown below:

![Obsidian Weathers 3](/Pictures/lotf/customisation/obsidian-weathers-3.png)

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