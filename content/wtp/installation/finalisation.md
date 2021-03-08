---
title: "Finalisation"
weight: 4
type: docs
description: >
  Final steps.
---

## Mod Organizer 2

All mods are installed in Mod Organizer 2 which is required to play the setup. You must always launch F4SE through MO2.

- Navigate to your **Welcome to Paradise** installation directory.
- Double-click **ModOrganizer.exe**.

>  I recommend adding ModOrganizer.exe to your taskbar or creating a shortcut on your Desktop for easy access.

## LUTs

An easy way to customise the overall tone of the game is by changing the color palettes - through LUTs. I have included three different options of which you can choose one or none. Take a look at the mod pages and their preview pictures.

You can change or disable LUTs at any time.

- Under the **LUT (OPTIONAL)** separator in Mod Organizer 2, check your preferred option.
- Check the pictures for [Neutral Look Up Tables LUT](https://www.nexusmods.com/fallout4/mods/1016).
- Check the pictures for [Fallout 4 Enhanced Color Correction](https://www.nexusmods.com/fallout4/mods/5060).

## Controller Fix

For FallUI, the interface overhaul, I increased the Pipboy resolution in the `fallout4prefs.ini` file. Unfortunately this will cause the map cursor to lock in the upper left corner when playing with a controller.

If you play with a controller, follow these instructions to revert the INI tweak:

- Click the puzzle icon in MO2 and select **INI Editor**.

![Open INI Editor](/Pictures/wtp/installation/mo2-ini-editor.png)

- Switch to the **fallout4prefs.ini** tab and scroll down to the **[Display]** section.
- Revert the following lines to the values shown below:

```
uPipboyTargetHeight=700
uPipboyTargetWidth=876
```

- Close the window and click **Yes** to save your changes.

![Controller Fix](/Pictures/wtp/installation/controller-fix.png)

## Frame Rate and VSYNC

One of the Creation Engine's drawbacks is the physics engine which is tied to the frame rate. Simply put, the game breaks if it runs at more than 60FPS. However, there is a mod that allows you to unlock the frame rate by dynamically adjusting havok settings at runtime, aptly called **High FPS Physics Fix**.

- **FPS** or frames per second are how the amount of still images shown every second are measured. The higher your FPS, the more fluid the game appears. The amount of frames per second that can be rendered depends on your hardware, primarily your CPU and GPU. In my opinion, a stable 60FPS is perfect for most games, including Fallout 4. Most systems should be able to achieve a consistent 60FPS in WTP.
- **VSYNC** is a technique that syncs a game's framerate to your monitor's refresh rate (hence the name). Enabling VSYNC prevents [screentearing](https://en.wikipedia.org/wiki/Screen_tearing) at the cost of latency and is always recommended. However, if your monitor supports G-Sync or FreeSync, you do not need to enable VSYNC by other means. G-Sync and FreeSync are advanced VSYNC methods applied globally to all fullscreen applications.

> **By default, WTP is capped to 60 FPS. VSYNC is disabled.**

### Enable VSYNC

Unless your monitor supports G-SYNC or FreeSync, I recommend enabling VSYNC in High FPS Physics Fix. To do so, follow these instructions:

- Double-click **High FPS Physics Fix** in your mod order (left pane in Mod Organizer 2).
- Switch to the **INI Files** tab and select the **HighFPSPhysicsFix.ini** file.
- In **Line 14**, set `EnableVSync=` to **true**.
- Press **CTRL + S** to save and close the window.

![Enable VSYNC](/Pictures/wtp/installation/enable-vsync.png)

### FPS Cap

If you are unhappy with the default cap at 60FPS, you can change it. To do so, follow these instructions:

- Double-click **High FPS Physics Fix** in your mod order (left pane in Mod Organizer 2).
- Switch to the **INI Files** tab and select the **HighFPSPhysicsFix.ini** file.
- In **Line 55**, change the value for `InGameFPS=` to your desired FPS cap. Set to **0** to uncap the frame rate.
- Press **CTRL + S** to save and close the window.

![Change FPS Cap](/Pictures/wtp/installation/change-fps-cap.png)

## Resolution

There are several relevant factors when deciding on which resolution to play at.

- **What is my monitor's aspect ratio?** Most monitors nowadays have an aspect ratio of 16:9. However, widescreen / ultrawide monitors with a 21:9 aspect ratio are also fairly common.
- **What is my monitor's resolution?** You are limited by your monitor's maximum resolution. On a 1440p monitor, you can play with a resolution of 2560x1440 or lower. Playing at 1080p on a 1440p monitor will yield better performance at the cost of image sharpness / clarity.
- **What is my hardware capable of?** Generally speaking, you will get the best performance playing at 1080p. However, WTP has been optimised for good performance so with decently modern hardware, you should get stable 60FPS at 1440p as well. Be warned that increasing the resolution will always impact performance.

> **By default, WTP is running at 1440p.**

### Changing the resolution

If you want to play at **1080p** or **2160p**, you need to change the resolution in the falloutprefs.ini file. Note that playing at 4K may strongly impact performance.

- Click the puzzle icon in MO2 and select **INI Editor**.

![Open INI Editor](/Pictures/wtp/installation/mo2-ini-editor.png)

- Switch to the **fallout4prefs.ini** tab and scroll down to the **[Display]** section (see picture below).
- Edit the following two lines with the respective values for your desired resolution:

**For 1080p - 1920x1080:**

```
iSize H=1080
iSize W=1920
```

**For 2160p - 3840x2160:**

```
iSize H=2160
iSize W=3840
```

- Close the window and click **Yes** to save your changes.

![Adjust resolution](/Pictures/wtp/installation/change-resolution.png)

### Ultrawide Monitor

If you are playing on an 21:9 ultrawide monitor, please refer to the [Ultrawide Support](/wtp/wtp-resources/ultrawide/) page.

---

#### Continue with the [New Game](/wtp/installation/new-game/) page.