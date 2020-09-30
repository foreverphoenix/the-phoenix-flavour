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

## Resolution

There are several relevant factors when deciding on which resolution to play at.

- **What is my monitor's aspect ratio?** Most monitors nowadays have an aspect ratio of 16:9. However, widescreen / ultrawide monitors with a 21:9 aspect ratio are also fairly common.
- **What is my monitor's resolution?** You are limited by your monitor's maximum resolution. On a 1440p monitor, you can play with a resolution of 2560x1440 or lower. Playing at 1080p on a 1440p monitor will yield better performance at the cost of image sharpness / clarity.
- **What is my hardware capable of?** Generally speaking, you will get the best performance playing at 1080p. However, TPF Fallout 4 has been optimised for good performance at 1440p so with decently modern hardware, you should get stable 60FPS at that resolution. Be warned that increasing the resolution will always impact performance.

### 16:9 - 1440p

This is the resolution I am playing and TPF Fallout 4 is optimised for it (meaning I conserved performance wherever possible). If you have a 1440Hz monitor and the hardware to play modded Fallout 4 at 1440p, **everything is configured correctly by default** and you can continue with the [New Game](https://thephoenixflavour.com/fallout/installation/new-game/) page.

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

## Frame Rate and VSYNC

One of the Creation Engine's drawbacks is the physics engine being tied to the frame rate. Simply put, the game breaks if it runs at more than 60FPS. There is a mod that allows you to unlock the frame rate by dynamically adjusting havok settings at runtime; however, most people are unlikely to get above 60FPS consistently anyway which is why TPF Fallout 4 does not include this mod. This means you have to **cap the frame rate to 60FPS**.

Additionally, you will need to force **VSYNC** in order to prevent [screentearing](https://en.wikipedia.org/wiki/Screen_tearing). By default, the game's inbuilt VSYNC is disabled in the TPF Fallout 4 INI files as it tends to be more of a performance hit than forcing VSYNC by other means would. Some monitors feature the G-Sync or FreeSync technologies which automatically force VSYNC in fullscreen applications.

### NVIDIA Inspector

My personal go-to method of capping the framerate is the NVIDIA Inspector which obviously only works if you have an NVIDIA GPU. AMD users might be able to achieve the same effect through RivaTuner. As for forcing VSYNC, this can be done through NVIDIA Inspector as well if your monitor does not feature G-Sync or FreeSync.

- Download and install [NVIDIA Inspector](https://www.guru3d.com/files-details/nvidia-inspector-download.html).
- Open the program and click the little icon next to **Driver Version** to open the profile settings.

![Open profile settings](/Pictures/fallout/installation/nvidia-inspector.png)

- Select **Fallout 4** from the Profiles drop-down menu at the top.
- Under **Sync and Refresh**, change the following:
  - Set Frame Rate Limiter to **60 FPS**
  - Set Vertical Sync to **Force on** (if your monitor does NOT feature G-Sync / FreeSync)
- Click **Apply changes** and close the profile settings window.

> Note that clean-installing your GPU driver will reset all profiles in which case you need to re-do this step.

![NVIDIA Inspector Profile](/Pictures/fallout/installation/nvidia-inspector-profile.png)

---

#### Continue with the [New Game](https://thephoenixflavour.com/fallout/installation/new-game/) page.