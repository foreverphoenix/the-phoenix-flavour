---
title: "Installation"
weight: 2
type: docs
description: >
  Installation guide for The Phoenix Flavour.
---

## Requirements

- [Skyrim Special Edition](https://store.steampowered.com/app/489830/The_Elder_Scrolls_V_Skyrim_Special_Edition/) plus [Anniversary Edition DLC](https://store.steampowered.com/app/1746860/The_Elder_Scrolls_V_Skyrim_Anniversary_Upgrade/) on Steam.
- Latest version of Windows 10 (required by Wabbajack).
- At least a free [Nexus Mods](https://www.nexusmods.com/) account, Premium is recommended.
- Latest drivers for your GPU ([NVIDIA](https://www.nvidia.com/Download/index.aspx) or [AMD](https://www.amd.com/en/support)).

> A Nexus Premium subscription is highly recommended for a significantly faster and easier installation. Without Premium, you will need to click download for every mod while Premium allows Wabbajack to automatically download everything for you.

### Disk Space

**The Phoenix Flavour** currently requires **~140GB** of free disk space for the list installation (which includes a copy of the vanilla game) and another **~87GB** for the downloaded archives. It is recommended to install TPF on an **SSD**.

> The exact figures vary from update to update.

The initial installation process will be faster if the downloaded archives are also on an SSD. They can be moved to a different drive afterwards as they are not necessary for gameplay, only for updating the list. If you delete them, you will have to redownload them if you want to update TPF so it's recommended to keep them.

### MO2 Prerequisites

Mod Organizer 2 requires the Microsoft Visual C++ Redistributable and .NET Framework 4.8, two basic packages. Chances are you already have them installed, but please grab the two installers linked below and run them. If the packages are already present on your system, the installers should notify you.

- Download and install [Visual C++ 2019](https://aka.ms/vs/16/release/vc_redist.x64.exe).
- Download and install [.NET Framework 4.8](https://dotnet.microsoft.com/download/dotnet-framework/thank-you/net48-web-installer).

If either of them were missing on your system, they will be installed now. Afterwards, you may be required to restart your PC.

## Skyrim SE Setup

**TPF requires the latest version of Skyrim SE.** For clarification, this latest version is a post-AE release (currently `1.6.353.0`). The Anniversary Edition DLC is required because some of the better Creations were integrated into TPF.

- If you are on **Skyrim SE 1.6.353.0**, you can install TPF without any further steps.
- If you are on any older version, please verify files through Steam to install the update.

**Please make sure to launch the game at least once before running Wabbajack.** If you just updated or (re)installed the game, this is necessary for setting up registry keys as modding tools will otherwise be unable to recognise the game. This will also prompt the Creations to be (re)downloaded. You can quit from the main menu.

### Set language to English

**TPF requires the English language version of Skyrim SE.**

If you are currently playing in a language other than English, please go into the settings for Skyrim SE in your Steam library and revert the language to English. After changing the language, Steam should automatically download the required files (launch the game to force the download if it doesn't).

After updating the game language, please launch the game once and quit from the main menu.

## Wabbajack Installation

Next up you need to install the Wabbajack tool itself:

- Download [Wabbajack](https://www.wabbajack.org/#/) from the official website.
- Extract the archive to a high-level folder, e.g. `C:\Wabbajack\`.

**Do not install Wabbajack into UAC protected directories.** These include Program Files and Program Files x86 as well as the Downloads, Desktop, Documents, etc, folders.

Double-click **Wabbajack.exe** to launch to tool. It will automatically update itself to the latest version.

### The Phoenix Flavour

You can now install TPF through Wabbajack:

- Download the latest beta version of TPF from our [Discord](https://discord.gg/xCPxJFbCTS) and extract the archive to a convenient location
- Click the **Install from Disk** button in the Wabbajack tool.
- Navigate to and select **The Phoenix Flavour.wabbajack**.

In the installation window, you will need to define two folders:

**Installation Location** is where TPF will be installed to. Choose a high-level folder such as `C:\The Phoenix Flavour\` that is outside UAC protected folders (Program Files, Documents, etc).

**Download Loaction** is where the downloaded mod archives will be stored. By default, they will be placed within your main TPF folder, but you can change the file path if you want to keep the files elsewhere.

> You can reuse the same downloads folder for any number of Wabbajack lists. This will most likely speed up the installation process.

Once both folder locations have been set, click the button on the right to begin the installation process.

### Installation Process

If you have **Nexus Premium**, this is all you have to do. Lean back and relax while Wabbajack downloads and installs TPF for you.

If you only have a free Nexus account, Wabbajack will open the mod pages for you and guide you through the process of downloading all files. Afterwards, it will proceed with the installation as usual.

You can follow along as Wabbajack installs the list. It will display previews with summaries and links to the mods being installed. Don't let the log irritate you. Unless the installation is aborted completely, you don't have to worry about any warnings.

**In case the installation does fail:** Try restarting Wabbajack first. You will not lose progress as the tool will pick up where it left off. Should the installation fail again, please join us on [Discord](https://discord.gg/xCPxJFbCTS), grab the `@TPF 5.0` role, and post your `wabbajack.current.log` in the `#beta-testing` channel. You can find all Wabbajack logs in your Wabbajack installation folder under `\Wabbajack\logs\`.

In most cases the installation should complete successfully on the first try. The tool will let you know when it has.

## Playing TPF

Navigate to your **The Phoenix Flavour** folder and launch the **ModOrganizer.exe** within. In the top right drop-down menu, **The Phoenix Flavour** (a renamed `skse64_loader.exe`) should already be selected and you can now launch the game by clicking **Run**.

> The Phoenix Flavour uses the **Stock Game Folder** system. There are no Game Folder Files to move manually.

I highly recommend checking the [Customisation](/skyrim-se/tpf/customisation) page before diving into the game.

**Please do NOT modify the Mod Configuration Menus** unless specifically instructed to do so. They have been preconfigured.