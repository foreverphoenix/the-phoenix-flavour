---
title: "Wabbajack"
weight: 6
type: docs
description: >
  Setup instructions for the Wabbajack version of TPF.
---

## Orientation

Hi there, this is the **Wabbajack** section of the guide. If you have so far followed the manual guide (Initial Setup, Mod Installation, Finalisation), please continue with the [Mod Configuration](/tpf/mod-configuration/) page, the Wabbajack section is NOT for you. Move along, nothing to see here.

If you want to install TPF via Wabbajack, you ARE in the right place. Make sure you've read the [Introduction](/tpf/introduction/) page and let's get started.

## Requirements

- [Skyrim Special Edition](https://store.steampowered.com/app/489830/The_Elder_Scrolls_V_Skyrim_Special_Edition/) on Steam.
- A legit Windows 7 / 8 / 8.1 / 10 installation (64bit).
- A free (or Premium) account on [Nexus Mods](https://www.nexusmods.com/).
- Around **80GB** of free space on an SSD / fast HDD.

> Remember that **Nexus Premium** is highly recommended to automate the mod download process. Otherwise, you'll have to click the download buttons manually for 500+ files.

### Visual C++ Redist

The Microsoft Visual C++ Redistributable is a basic package required by Mod Organizer 2. You probably already have it installed but it's best to make sure.

- Open the official [Microsoft Visual C++ website](https://support.microsoft.com/en-us/help/2977003/the-latest-supported-visual-c-downloads).
- Scroll to the **Visual Studio 2015, 2017 and 2019** section.
- Download the following file: ` vc_redist.x64.exe`.
- Run the executable, it will guide you through the installation process.

![VC Redist](/Pictures/tpf/initial-setup/vc-redists.png)

## Clean Skyrim

There are various ways to nuke existing Skyrim installations. For the purposes of being quick and thorough, we're going to reinstall the game from scratch.

Re-installing Skyrim SE on an SSD is highly recommended for better performance. The hard drive must have at least **80GB** of free space.

- **Uninstall Skyrim SE through Steam.**
- Navigate to the installation directory (`Steam\steamapps\common\Skyrim Special Edition`).
- Delete any left-over files within that folder.
- Navigate to `C:\Users\Your Username\Documents\My Games\Skyrim Special Edition`.
- Delete everything inside that folder (any old savefiles will be deleted also).

### Steam Settings

- In Steam, open the **Properties** for Skyrim SE.
- In the **Updates** tab, make sure **Automatic Updates** is set to **Only update this game when I launch it**.
- In the **Language** tab, make sure the **Language** is set to **English**.

> Non-English installations of Skyrim SE are not supported.

### Reinstallation

- **Reinstall Skyrim SE through Steam.**
- Once Skyrim SE is reinstalled, run it from Steam.
- Click **OK** twice to regenerate your INI files.
- Close the launcher.

> Skyrim SE should **NOT** be installed inside C:\Program Files or C:\Program Files x86.

### Creation Club

If you own any Creation Club content, it was likely reinstalled alongside Skyrim SE. TPF does not support CC content and you need to move those files out of your Skyrim SE installation.

- Navigate to `Steam\steamapps\common\Skyrim Special Edition\Data`.
- Delete or move away any files starting with **cc**.

## Modding Folder

Your Modding Folder will contain files not related to the actual TPF setup. Therefore it doesn't require a fast hard drive and should be located on a simple HDD. It will contain all downloaded mod archives which are not needed after the initial installation unless you want to update TPF. It is recommended you keep them as redownloading them takes a lot of time.

- Create a new **Skyrim SE Modding** folder on a hard drive of your choosing.
- Inside your new Skyrim SE Modding folder, create a **Wabbajack** and a **TPF Downloads** folder.

### Installation Folder

The instance of Mod Organizer 2 containing the actual TPF setup SHOULD be located on an SSD for better performance. Your chosen hard drive must have at least **80GB** of free space.

- Create a new **The Phoenix Flavour** folder on or near the root (top level) of your fastest hard drive, eg: `C:\The Phoenix Flavour`.

## TPF Installation

- Download [Wabbajack](https://www.wabbajack.org/#/) from the official website.
- Move the downloaded executable into your **Wabbajack** folder.
- Double-click **Wabbajack.exe**.

### Download Modlist

- Click the **Browse Modlists** button to open the Gallery.
- Find **The Phoenix Flavour** in the list and click the download button.
- Point **Installation Location** at your **The Phoenix Flavour** folder.
- Point **Download Location** to your **Downloads** folder.
- When all locations are configured, you can click the triangular **Start** button.

The download and subsequent installation of all mods will take a while depending on your internet connection. You can close Wabbajack at any time to pause the process. The next time you open Wabbajack, it will pick up where it left off.

Wait until Wabbajack has finished installing TPF before moving on to the next step.

### Game Folder Files

Some files must be moved into the root folder which cannot be managed by Mod Organizer 2. You need to move them by hand.

- Navigate to your TPF installation `\The Phoenix Flavour\`.
- Double-click the **Game Folder Files** folder and copy all files within (but not the folders).
- Navigate to your Skyrim SE root folder `\Steam\steamapps\common\Skyrim Special Edition\` and paste all files.
- Choose one of the ENB presets: Rudy ENB (quality) or Serio's ENB (performance).
- Double-click the respective folder and copy the contents.
- Paste them into your root folder `\Steam\steamapps\common\Skyrim Special Edition\` as well.

![Game Folder Files](/Pictures/tpf/wabbajack/game-folder-files.png)

### Enable VSYNC

VSYNC is disabled by default as I am playing on a GSYNC monitor. If you do not have either FreeSync or GSYNC, you need to re-enable VSYNC in SSE Display Fixes, otherwise you will encounter screentearing.

- Double-click **SSE Display Tweaks** in Mod Organizer 2 (below the ESSENTIAL MODS separator near the top).
- Switch to the **INI Files** tab and select the **SSEDisplayTweaks.ini**.
- Scroll to **Line 71** and change `EnableVSync=` to `true`.
- Close the window and click **Yes** to save your change.

### Uncap Framerate

Since we are using SSE Display Tweaks, it is possible to uncap the framerate without breaking the game. However, for this you must disable native VSYNC which means you will suffer from screentearing unless your monitor is capable of G-Sync or FreeSync.

- Double-click **SSE Display Tweaks** in Mod Organizer 2 (below the ESSENTIAL MODS separator near the top).
- Switch to the **INI Files** tab and select the **SSEDisplayTweaks.ini**.
- Scroll to **Line 205** and change `Frameratelimit=` to your desired value.
- Close the window and click **Yes** to save your change.

## Playing TPF

It is not possible to run modded Skyrim through Steam. You must always start the game by running SKSE through Mod Organizer 2. Note that I renamed the **SKSE** executable to **The Phoenix Flavour** and changed the icon for it as well.

- Open your installation folder `C:\The Phoenix Flavour\` and double-click the **ModOrganizer.exe** inside.
- In Mod Organizer 2, make sure **The Phoenix Flavour** is selected as executable.
- Hit **Run** to start the game. Select **NEW** in the main menu.
- After completing the intro quest (Helgen), continue with the [Mod Configuration](/tpf/mod-configuration) page.

![Launch Game](/Pictures/tpf/wabbajack/launch-game.png)