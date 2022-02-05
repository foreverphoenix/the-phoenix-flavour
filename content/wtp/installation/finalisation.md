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

## Controller Fix

The resolution of the Pip-Boy interface was increased in the `fallout4prefs.ini` file. Unfortunately this will cause the map cursor to lock in the upper left corner when playing with a controller.

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
- **VSYNC** is a technique that syncs a game's framerate to your monitor's refresh rate (hence the name). It prevents [screentearing](https://en.wikipedia.org/wiki/Screen_tearing) at the cost of latency and is always recommended.

> Welcome to Paradise caps the framerate at 60 and forces VSYNC through High FPS Physics Fix.

### Adjusting the FPS Cap

If you are unhappy with the default cap at 60FPS, you can change it. To do so, follow these instructions:

- In Mod Organizer 2, double-click the **ESSENTIALS** separator at the top to expand it.
- Doubl-click **High FPS Physics Fix - WTP Settings** which contains a custom INI for High FPS Physics Fix.
- Switch to the **INI Files** tab and select the **HighFPSPhysicsFix_Custom.ini** file.
- In **Line 2**, change the value for `InGameFPS=` to your desired FPS cap. Set to **0.0** to uncap the frame rate.
- Press **CTRL + S** to save and close the window.

![Change FPS Cap](/Pictures/wtp/installation/change-fps-cap.png)

## Ultrawide Support

> Skip this page and continue with the [New Game](wtp/installation/new-game/) instructions if you have a 16:9 monitor.

Since release 2.2, WTP officially supports ultrawide monitors with a **21:9 ratio**, i.e. resolutions of **2560x1080** or **3440x1440**. This requires a few minor changes in Mod Organizer 2 that you should go through before starting your playthrough.

### INI Changes

Upon installing WTP, Wabbajack should automatically detect your monitor's default resolution and configure Fallout4Prefs.ini accordingly. However, if you wish you can check this and make sure the correct resolution is set. To do so, open the **INI Editor** in MO2, go to the **Fallout4Prefs.ini** tab and scroll to the **[Display]** section.

If the resolution is not correct, change it and click the **SAVE** button at the bottom before closing the window.

![Change Resolution](/Pictures/wtp/installation/change-resolution.png)

### Additional Mods

In Mod Organizer 2, find the **ULTRAWIDE SUPPORT (21-9)** separator in the left pane and double-click to expand it. There are three mods below it. Activate all three by checking the boxes. This will add an additional plugin to the load order which you do not need to adjust because it is empty and only exists to load an INI file.

![Ultrawide Mods](/Pictures/wtp/installation/ultrawide-mods.png)

---

#### Continue with the [Ultrawide](/wtp/installation/ultrawide/) page.