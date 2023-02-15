---
title: "Installation"
weight: 2
type: docs
description: >
  Installation guide for Legends of the Frost.
---

## Requirements

- Skyrim Special Edition on [Steam](https://store.steampowered.com/app/489830/The_Elder_Scrolls_V_Skyrim_Special_Edition/) **or** [GOG](https://www.gog.com/en/game/the_elder_scrolls_v_skyrim_special_edition).
- The **Anniversary Edition DLC** (or all Creations bought separately).
- Latest version of Windows 10 (required by Wabbajack).
- At least a free [Nexus Mods](https://www.nexusmods.com/) account, Premium is recommended.
- Latest drivers for your GPU ([NVIDIA](https://www.nvidia.com/Download/index.aspx) or [AMD](https://www.amd.com/en/support)).

> A Nexus Premium subscription is highly recommended for a significantly faster and easier installation. Without Premium, you will need to click download for every mod while Premium allows Wabbajack to automatically download everything for you.

### Disk Space

**Legends of the Frost** currently requires **~34GB** of free disk space for the list installation and another **~26GB** for the downloaded archives. It is recommended to install LOTF on an **SSD**.

The initial installation process will be faster if the downloaded archives are also on an SSD. They can be moved to a different drive afterwards as they are not necessary for gameplay, only for updating the list. If you delete them, you will have to redownload them if you want to update LOTF so it's recommended to keep them.

### MO2 Prerequisites

Mod Organizer 2 requires the Microsoft Visual C++ Redistributable and .NET Framework 4.8, two basic packages. Chances are you already have them installed, but please grab the two installers linked below and run them. If the packages are already present on your system, the installers should notify you.

- Download and install [Visual C++ 2019](https://aka.ms/vs/16/release/vc_redist.x64.exe).
- Download and install [.NET Framework 4.8](https://dotnet.microsoft.com/download/dotnet-framework/thank-you/net48-web-installer).

If either of them were missing on your system, they will be installed now. Afterwards, you may be required to restart your PC.

## Skyrim SE Setup

**LOTF requires the latest version of Skyrim SE.** This is currently `1.6.640.0` on Steam or `1.6.659.0` on GOG.

Because LOTF is using the default game folder (with the Root Builder plugin), it is crucial that this folder is located **outside** any UAC-protected folders. To ensure 


(FULL REINSTALL INSTRUCTIONS NEEDED)






- If you are on the latest version, you can install LOTF without any further steps.
- If you are on any older version, please verify files through Steam to install the update or reinstall the game through Steam.

**Please make sure to launch the game at least once before running Wabbajack.** If you just updated or (re)installed the game, this is necessary for setting up registry keys as modding tools will otherwise be unable to recognise the game. You can quit from the main menu.

### Set language to English

**LOTF requires the English language version of Skyrim SE.**

If you are currently playing in a language other than English, please go into the settings for Skyrim SE in your Steam library and revert the language to English. After changing the language, Steam should automatically download the required files (launch the game to force the download if it doesn't).

After updating the game language, please launch the game once and quit from the main menu.

> If you own the Anniversary Edition DLC, the game will download all creations on first launch. This may take a few minutes.

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

**Download Location** is where the downloaded mod archives will be stored. By default, they will be placed within your main LOTF folder, but you can change the file path if you want to keep the files elsewhere.

Once both folder locations have been set, click the button on the right to begin the installation process.

![LOTF Installation WJ](/Pictures/lotf/installation/lotf-installation-wj.png)

### Installation Process

If you have **Nexus Premium**, this is all you have to do. Lean back and relax while Wabbajack downloads and installs LOTF for you.

If you only have a free Nexus account, Wabbajack will open the mod pages for you and guide you through the process of downloading all files. Afterwards, it will proceed with the installation as usual.

You can follow along as Wabbajack installs the list. It will display previews with summaries and links to the mods being installed. Don't let the log irritate you. Unless the installation is aborted completely, you don't have to worry about any warnings.

**In case the installation does fail:** Try restarting Wabbajack first. You will not lose progress as the tool will pick up where it left off. Should the installation fail again, please join us on [Discord](https://discord.gg/xCPxJFbCTS), grab the `@LOTF` role, and post your `wabbajack.current.log` in the `#lotf-support` channel. You can find all Wabbajack logs in your Wabbajack installation folder under `\Wabbajack\logs\`.

In most cases the installation should complete successfully on the first try. The tool will let you know when it has.

## Playing LOTF

Navigate to your **Legends of the Frost** folder and launch the **ModOrganizer.exe** within. In the top right drop-down menu, **Legends of the Frost** (a renamed `skse64_loader.exe`) should already be selected and you can now launch the game by clicking **Run**.

> Legends of the Frost uses the **Stock Game Folder** system. There are no Game Folder Files to move manually.

![Play LOTF](/Pictures/lotf/installation/launch-lotf.png)

### MCM Instructions

LOTF only has a handful of Mod Configuration Menus (MCMs). **Presets are automatically applied so you don't need to edit anything manually.** I strongly recommend not changing anything in the MCMs unless you have something specific in mind.

### Customisation

Before you begin a new playthrough, you may want to check out the tweaks and optional mods that are supported for LOTF on the [Customisation](/skyrim-se/lotf/customisation) page.

It is *highly recommended* to add **The Truth ENB** to LOTF for much improved visuals. [Instructions here](/skyrim-se/lotf/enb-for-lotf/).

Additionally, there are two extra profiles included with the base LOTF one in Mod Organizer 2.

- If you own **Creation Club** content / the AE DLC, you can use the LOTF CC profile. [Instructions here](/skyrim-se/lotf/creation-club/).
- If your system is on the lower mid end, you may want to try the **Performance** profile.

> Note that saves are profile-specific. You can switch from the regular to the performance profile mid-playthrough, but you would have to copy over the saves from `\Legends of the Frost\profiles\Legends of the Frost\saves\` to `\Legends of the Frost\profiles\Legends of the Frost - Performance\saves\` manually. Please do not attempt to switch from the CC profile to either the regular or performance profile in an ongoing playthrough.

Check the picture below to see how to switch to a different profile in MO2:

![Swap MO2 Profile](/Pictures/lotf/customisation/swap-mo2-profile.png)