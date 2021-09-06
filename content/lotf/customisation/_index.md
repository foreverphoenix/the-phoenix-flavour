---
title: "Customisation"
weight: 3
type: docs
description: >
  Small tweaks anyone can do for Legends of the Frost.
---

LOTF is a very small list and I do not expect that I will ever add many customisation options. However, there are a few small changes that you can make:

## Uncap the framerate

Thanks to [SSE Display Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/34705), it is absolutely possible to play Skyrim SE at above 60FPS without breaking the game. In my experience, the likelyhood of (minor) physics bugs occuring increases with the framerate which is why I personally prefer capping at 60FPS. You can also try capping at 75FPS or 90FPS if you really want a higher framerate. Due to LOTF's performance-friendly nature, you should be able to achieve such framerates on most PCs.

To change the FPS cap, you need to edit the INI file for SSE Display Tweaks:

- In **Mod Organizer 2**, expand the **ESSENTIALS** separator.
- Double-click the mod **SSE Display Tweaks**.
- Switch to the **INI Files** tab and select the **SSEDisplayTweaks.ini**.
- Scroll down to `FramerateLimit=` (around **Line 207**) and adjust the value to your liking.
- Press **CTRL + S** to save your changes and close the window.

![LOTF Uncap Framerate](/Pictures/lotf/lotf-uncap-framerate.png)

## Revert to vanilla font

If you prefer the vanilla font over my choice, Roboto, you can disable the font replacer anytime:

- In **Mod Organizer 2**, expand the **INTERFACE** separator.
- Uncheck the mod **Roboto Font Replacer**.

## Enable dot crosshair

If you prefer a subtle dot over the vanilla crosshair, follow these steps:

- In **Mod Organizer 2**, expand the **INTERFACE** separator.
- Check the mod **SkyHUD - White Dot Crosshair**.

## Enable 24h time format

If you prefer a 24h time format over the 12h one (e.g., 23h instead of 11pm), do this:

- In **Mod Organizer 2**, expand the **INTERFACE** separator.
- Check the mod **Time Format Changer**.

## Access the Creation Club

If you want to access the Creation Club through the main menu, do the following:

- In **Mod Organizer 2**, expand the **INTERFACE** separator.
- Uncheck the mod **ReCleaned Menu**.

## Skip Lockpicking

If you are tired of the lockpicking minigame, I included a mod to skip it. Interacting with a locked container will unlock it, but consume lockpicks based on the lock difficulty.

- In **Mod Organizer 2**, expand the **GAMEPLAY** separator.
- Check the mod **No Lock Picking**.

## Enable Barenziah Quest Markers

Finding all 24 Stones of Barenziah during the [No Stone Unturned](https://en.uesp.net/wiki/Skyrim:No_Stone_Unturned) quest can be a bit of a slog. If you would prefer quest markers to show you exactly where the stones are located, turn on this option in the **SSoB** MCM:

![SSoB MCM](/Pictures/lotf/lotf-ssob-mcm.jpg)

## Increase combat difficulty

If you find combat to be too easy, it is advisable to disable the Blade & Blunt vanilla damage modifiers plugin before increasing the difficulty through the game settings:

- In **Mod Organizer 2**, expand the **GAMEPLAY** separator.
- Uncheck the mod **Blade and Bunt - Vanilla Difficulty Modifiers**.