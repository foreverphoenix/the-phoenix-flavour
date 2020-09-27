---
title: "Wabbajack"
weight: 3
type: docs
description: >
  Installing Wabbajack and downloading TPF Fallout 4.
---

## Installation

- Download the [Wabbajack](https://www.wabbajack.org/#/) executable from the official website.
- Move the downloaded file to `Fallout 4 Modding\Wabbajack`.
- Double-click **Wabbajack.exe**. It will automatically download and install the latest version.

### Downloading TPF FO4

- Once Wabbajack is installed and open, click on **Browse Modlists**.
- Find **TPF Fallout 4** in the list and click the arrow to download.
- Click the dots next to **Installation Location** and choose a path.
- Choose an empty, high-level folder, e.g. `G:\TPF Fallout 4`.
  - SHOULD be on your SSD or otherwise fastest hard drive.
  - CANNOT be inside `Fallout 4 Modding\Wabbajack`.
  - CANNOT be inside the Fallout 4 installation folder.
  - CANNOT be inside `C:\Program Files` or `C:\Program Files x86`.
- Change the **Download Location** file path to `Fallout 4 Modding\Downloads`.
- Click the **Start** button on the left to begin the installation process.

> By downloading the mod archives to a different location, you can save space on your SSD. The archives are only required for the initial mod installation and future updates so there is no need to put them on a fast hard drive.

### Troubleshooting

Should anything go wrong during the installation process, please find the **Wabbajack.current.log** file inside `Fallout 4 Modding\Wabbajack\<version number>\logs\`. Upload it (drag and drop) into the TPF Fallout 4 support channel on either the TPF or Wabbajack Discord server.

## Game Folder Files

- Navigate to your Wabbajack installation directory
- Open the **Game Folder Files** folder. Select (CTRL+A) and copy (CTRL+C) all files inside.
- Find your Fallout 4 installation (`Steam\steamapps\common\Fallout4`) and paste all files there (CTRL+V).

![Game Folder Files](/Pictures/fallout/installation/game-folder-files.png)

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

---

#### Continue with the [New Game](https://thephoenixflavour.com/fallout/installation/new-game/) page.