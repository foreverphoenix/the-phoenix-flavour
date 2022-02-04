---
title: "Installation"
weight: 2
type: docs
description: >
  Installation guide for Legends of the Frost.
---

## Requirements

- [Skyrim Special Edition](https://store.steampowered.com/app/489830/The_Elder_Scrolls_V_Skyrim_Special_Edition/) on Steam.
- Latest version of Windows 10 (required by Wabbajack).
- At least a free [Nexus Mods](https://www.nexusmods.com/) account, Premium is recommended.
- Latest drivers for your GPU ([NVIDIA](https://www.nvidia.com/Download/index.aspx) or [AMD](https://www.amd.com/en/support)).

> A Nexus Premium subscription is highly recommended for a significantly faster and easier installation. Without Premium, you will need to click download for every mod while Premium allows Wabbajack to automatically download everything for you.

### Disk Space

**Legends of the Frost** currently requires **~53GB** of free disk space for the list installation and another **~30GB** for the downloaded archives. It is recommended to install LOTF on an **SSD**.

The initial installation process will be faster if the downloaded archives are also on an SSD. They can be moved to a different drive afterwards as they are not necessary for gameplay, only for updating the list. If you delete them, you will have to redownload them if you want to update LOTF so it's recommended to keep them.

### Visual C++ Redist

The Microsoft Visual C++ Redistributable is a basic package required by Mod Organizer 2. You probably already have it installed with Windows but it is best to make sure.

- Open the official [Microsoft Visual C++](https://support.microsoft.com/en-us/topic/the-latest-supported-visual-c-downloads-2647da03-1eea-4433-9aff-95f26a218cc0) website.
- Scroll to the **Visual Studio 2015, 2017 and 2019** section.
- Download the following file: `vc_redist.x64.exe`.
- Run the executable, it will guide you through the installation process.

![VC Redist](/Pictures/tpf/initial-setup/vc-redists.png)

### Microsoft .NET 5.0

Additionally, .NET 5.0 is required for the mod **Scrambled Bugs**. The game will not launch if you do not have it installed.

- Open the official [.NET 5.0 Runtime](https://dotnet.microsoft.com/download/dotnet/5.0/runtime) website.
- Download the **desktop app x64** *and* **console app x64** installers and run them one after the other.

![Dot NET Download](/Pictures/lotf/installation/dot-net-download.png)

## Skyrim SE Setup

**LOTF requires the latest version of Skyrim SE.** For clarification, this latest version is a post-AE release (currently `1.6.353.0`). A copy of your vanilla executables downgraded to 1.5.97.0 will be placed in LOTF's custom stock game folder, but in order to install the list you need to have an up-to-date Steam installation of the game. The Skyrim AE DLC itself is not required and not supported outside the optional Creation Club profile (instructions on how to use that will be linked later).

- If you are on **Skyrim SE 1.6.342.0**, you can install LOTF without running the downgrade patcher.
- If you are on any older version, please verify files through Steam to install the update.

**Please make sure to launch the game at least once before running Wabbajack.** If you just updated or (re)installed the game, this is necessary for setting up registry keys as modding tools will otherwise be unable to recognise the game. You can quit from the main menu.

### Set language to English

**LOTF requires the English language version of Skyrim SE.**

If you are currently playing in a language other than English, please go into the settings for Skyrim SE in your Steam library and revert the language to English. After changing the language, Steam should automatically download the required files (launch the game to force the download if it doesn't).

After updating the game language, please launch the game once and quit from the main menu.

## Wabbajack Installation

Next up you need to install the Wabbajack tool itself:

- Download [Wabbajack](https://www.wabbajack.org/#/) from the official website.
- Extract the archive to a high-level folder, e.g. `C:\Wabbajack\`.

**Do not install Wabbajack into UAC protected directories.** These include Program Files and Program Files x86 as well as the Downloads, Desktop, Documents, etc, folders.

Double-click **Wabbajack.exe** to launch to tool. It will automatically update itself to the latest version.

### Legends of the Frost

You can now install LOTF through Wabbajack:

- Click the **Browse Modlists** button in the Wabbajack tool.
- Find **Legends of the Frost** in the gallery of mod lists and click the arrow button to download the installation file.

![LOTF on WJ](/Pictures/lotf/installation/lotf-on-wj.png)

In the installation window, you will need to define two folders:

**Installation Location** is where LOTF will be installed to. Choose a high-level folder such as `C:\Legends of the Frost\` that is outside UAC protected folders (Program Files, Documents, etc).

**Download Loaction** is where the downloaded mod archives will be stored. By default, they will be placed within your main LOTF folder, but you can change the file path if you want to keep the files elsewhere.

Once both folder locations have been set, click the button on the right to begin the installation process.

![LOTF Installation WJ](/Pictures/lotf/installation/lotf-installation-wj.png)

### Installation Process

If you have **Nexus Premium**, this is all you have to do. Lean back and relax while Wabbajack downloads and installs LOTF for you.

If you only have a free Nexus account, Wabbajack will open the mod pages for you and guide you through the process of downloading all files. Afterwards, it will proceed with the installation as usual.

You can follow along as Wabbajack installs the list. It will display previews with summaries and links to the mods being installed. Don't let the log irritate you. Unless the installation is aborted completely, you don't have to worry about any warnings.

**In case the installation does fail:** Try restarting Wabbajack first. You will not lose progress as the tool will pick up where it left off. Should the installation fail again, please join us on [Discord](https://discord.gg/xCPxJFbCTS), grab the `@LOTF` role, and post your `wabbajack.current.log` in the `#lotf-support` channel. You can find all Wabbajack logs in your Wabbajack installation folder under `\Wabbajack\logs\`.

In most cases the installation should complete successfully on the first try. The tool will let you know when it has.

## Playing LOTF

Navigate to your **Legends of the Frost** folder and launch the **ModOrganizer.exe** within. In the top right drop-down menu, **Legends of the Frost** (a renamed skse64_loader.exe) should already be selected and you can now launch the game by clicking **Run**.

> Legends of the Frost uses the **Stock Game Folder** system. There are no Game Folder Files to move manually.

![Play LOTF](/Pictures/lotf/installation/launch-lotf.png)

### MCM Instructions

LOTF only has a handful of Mod Configuration Menus (MCMs). Presets are automatically applied so you don't need to edit anything manually. I strongly recommend not changing anything in the MCMs unless you have something specific in mind.

### Customisation

Before you begin a new playthrough, you may want to check out the tweaks and optional mods that are supported for LOTF on the [Customisation](/lotf/customisation) page.

Additionally, there are two extra profiles included with the base LOTF one in Mod Organizer 2.

- If you own **Creation Club** content / the AE DLC, you can use the LOTF CC profile. [Instructions here](/lotf/creation-club/).
- If your system is well below Skyrim's usual system requirements, you may want to try the **Performance** profile.

> Note that saves are profile-specific. You can switch from the regular to the performance profile mid-playthrough, but you would have to copy over the saves from `\Legends of the Frost\profiles\Legends of the Frost\saves\` to `\Legends of the Frost\profiles\Legends of the Frost - Performance\saves\` manually. Please do not attempt to switch from the CC profile to either the regular or performance profile in an ongoing playthrough.

Check the picture below to see how to switch to a different profile in MO2:

![Swap MO2 Profile](/Pictures/lotf/customisation/swap-mo2-profile.png)

### ENB Hotkeys

The hotkeys to toggle ENB on/off, open the GUI, or display the FPS meter are the same as in TPF and WTP:

- **F8** toggles the FPS counter.
- **F10** toggles the ENB effect.
- **F11** opens the ingame GUI.

All other functions (screenshot, FPS cap, toggle DOF) were disabled. I recommend taking screenshots with Steam by pressing F12.