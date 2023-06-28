---
title: "Customisation"
weight: 3
type: docs
description: >
  Various supported tweaks for Legends of the Frost.
---

## Performance INIs

For an extra ~10-15FPS, you can switch to a set of more performance-friendly INI files. Among other things, the performance INIs have lowered settings for distant terrain, render grass and shadows at a shorter distance, and disable volumetric lighting (godrays).

- Navigate to `\Legends of the Frost\mods\Legends of the Frost - Performance INIs\`.
- Copy the **Skyrim.ini** and **SkyrimPrefs.ini** inside.
- Paste the INIs to `\Legends of the Frost\profiles\Legends of the Frost\`.

**Confirm to overwrite existing INIs.**

A backup of the default INIs are also included under `\Legends of the Frost\mods\Legends of the Frost - Default INIs\` so you can switch back at any time.

## Higher or Uncapped FPS

Thanks to [SSE Display Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/34705), it is absolutely possible to play Skyrim SE at above 60FPS without breaking the game. In my experience, the likelyhood of (minor) physics bugs occuring increases with the framerate which is why I personally prefer capping at 60FPS. You can also try capping at 75FPS or 90FPS if you really want a higher framerate. Due to LOTF's performance-friendly nature, you should be able to achieve such framerates on most PCs.

To change the FPS cap, you need to edit the INI file for SSE Display Tweaks:

- In **Mod Organizer 2**, expand the **Essential Mods** separator.
- Double-click **SSE Display Tweaks - LOTF Settings**.
- Switch to the **INI Files** tab and select the **SSEDisplayTweaks.ini**.
- Change the value for `FramerateLimit=` to your liking.
- Press **CTRL + S** to save your changes and close the window.

![LOTF Uncap Framerate](/Pictures/lotf/customisation/lotf-uncap-framerate.png)

## Widescreen Support

The user interface mods included with LOTF (as well as the vanilla Skyrim UI) are optimised for 16:9 monitors (i.e., resolutions like 1920x1080, 2560x1440, 3840×2160). Anyone playing on ultrawide monitors (2560x1080 or 3440x1440) will need a few extra patches in order to make the user interface scale properly. These are preinstalled in LOTF and need only be activated.

Wabbajack will already have correctly set your resolution in the INI files so no manual adjustments are required.

- Disable **SkyUI - 3D Item Offset Fix** under the **Essential Mods** separator.
- Enable all mods grouped below the **Widescreen Patches** separator:

![LOTF Widescreen Support](/Pictures/lotf/customisation/lotf-widescreen-support.png)

## Optional Tweaks

LOTF features a handful of additional mods that are disabled by default, but may be enabled at any time. You can find them grouped below the **Optional Tweaks** separator.

![LOTF Widescreen Support](/Pictures/lotf/customisation/lotf-optional-tweaks.png)

## Enable Barenziah Quest Markers

Finding all 24 Stones of Barenziah during the [No Stone Unturned](https://en.uesp.net/wiki/Skyrim:No_Stone_Unturned) quest can be a bit of a slog. If you would prefer quest markers to show you exactly where the stones are located, turn on this option in the **SSoB** MCM:

![SSoB MCM](/Pictures/lotf/lotf-ssob-mcm.jpg)