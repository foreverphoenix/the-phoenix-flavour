---
title: "Finalisation"
weight: 4
type: docs
description: >
  Final steps.
---

## Mod Organizer 2

All mods are installed in Mod Organizer 2 which is required to play the setup. I recommend adding the MO2 executable to your taskbar or creating a shortcut on your Desktop for easy access. 

- Navigate to your TPF Fallout 4 installation directory.
- Double-click **ModOrganizer.exe**.

## Frame Rate and VSYNC

One of the Creation Engine's drawbacks is the physics engine which is tied to the frame rate. Simply put, the game breaks if it runs at more than 60FPS. There is a mod that allows you to unlock the frame rate by dynamically adjusting havok settings at runtime, aptly called **High FPS Physics Fix**. WTP includes this mod as well as four pre-configured INI files of which you need to enable one.

The profiles allow any combination of **FPS cap** and **VSYNC** settings.

- **FPS** or frames per second is how the amount of still images shown every second are measured. The higher your FPS, the more fluid the game appears. The amount of frames per second that can be rendered depend on your hardware, primarily your CPU and GPU. In my opinion, a stable 60FPS is perfect for most games, including Fallout 4. Most systems should be able to achieve a consistent 60FPS in WTP.
- **VSYNC** is a technique that syncs a game's framerate to your monitor's refresh rate (hence the name). Enabling VSYNC prevents [screentearing](https://en.wikipedia.org/wiki/Screen_tearing) at the cost of latency and is always recommended. However, if your monitor supports G-Sync or FreeSync, you do not need to enable VSYNC by other means. G-Sync and FreeSync are advanced VSYNC methods applied globally to all fullscreen applications.

In Mod Organizer 2, you can see the **HIGH FPS PHYSICS FIX** section near the top of the mod order (left pane). The main mod is already checked, but you need to enable one of the **Pre-made INIs** as well. To figure out which profile you want, you need to consider your hardware:

- If your monitor **does not support G-Sync / FreeSync:** Check one of the `VSYNC` profiles.
- If your monitor **supports G-Sync / FreeSync:** Check one of the `No VSYNC` profiles.
- Whether to **cap** or **uncap** FPS comes down to personal taste. Personally, I prefer to cap at 60 FPS.

>> You must always have one profile checked.

![High FPS Physics Fix Profiles](/Pictures/fallout/installation/high-fps-physics-fix-profiles.png)

## Resolution

There are several relevant factors when deciding on which resolution to play at.

- **What is my monitor's aspect ratio?** Most monitors nowadays have an aspect ratio of 16:9. However, widescreen / ultrawide monitors with a 21:9 aspect ratio are also fairly common.
- **What is my monitor's resolution?** You are limited by your monitor's maximum resolution. On a 1440p monitor, you can play with a resolution of 2560x1440 or lower. Playing at 1080p on a 1440p monitor will yield better performance at the cost of image sharpness / clarity.
- **What is my hardware capable of?** Generally speaking, you will get the best performance playing at 1080p. However, TPF Fallout 4 has been optimised for good performance at 1440p so with decently modern hardware, you should get stable 60FPS at that resolution. Be warned that increasing the resolution will always impact performance.

### 16:9 - 1440p

This is the resolution I am playing and TPF Fallout 4 is optimised for it (meaning I conserved performance wherever possible). If you have a 1440Hz monitor and the hardware to play modded Fallout 4 at 1440p, **everything is configured correctly by default** and you can continue with the next page.

### 16:9 - 1080p or 2160p

If you own a 16:9 monitor and want to play at 1080p or 2160p, follow the instructions below. Note that playing at 4K will significantly impact performance.

- Click the puzzle icon in MO2 and select **INI Editor**.

![Open INI Editor](/Pictures/fallout/customisation/mo2-ini-editor.png)

- Switch to the **falloutprefs.ini** tab and scroll down to the [Display] section (see picture below).
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

- Click **Save** and close the window.

![Adjust resolution](/Pictures/fallout/installation/change-resolution.png)

### 21:9 - 1080p or 1440p

Please refer to the [Ultrawide Support](https://thephoenixflavour.com/fallout/customisation/ultrawide/) page.

---

#### Continue with the [New Game](https://thephoenixflavour.com/fallout/installation/new-game/) page.