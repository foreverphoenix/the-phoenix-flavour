---
title: "Installation"
weight: 2
type: docs
description: >
  How to install or update TPF with Wabbajack.
---

## Requirements

- Skyrim Special Edition on Steam, including the [Anniversary Edition DLC](https://store.steampowered.com/app/1746860/The_Elder_Scrolls_V_Skyrim_Anniversary_Upgrade/).
- Latest version of Windows 10 or 11 (required by Wabbajack).
- At least a free [Nexus Mods](https://www.nexusmods.com/) account. [Premium](https://www.nexusmods.com/premium) is <u>highly</u> recommended for automated downloads.
- Latest drivers for your GPU ([NVIDIA](https://www.nvidia.com/Download/index.aspx), [AMD](https://www.amd.com/en/support), or [Intel](https://www.intel.com/content/www/us/en/download-center/home.html)).

### Disk Space

A full installation of TPF requires **~??GB** of diskspace, with an additional **~??GBs** for downloads. It is highly recommended to install TPF on an **SSD** for improved performance and faster loading times.

### MO2 Prerequisites

Mod Organizer 2 requires the Microsoft Visual C++ Redistributable and .NET Framework 4.8, two basic packages. You likely already have them installed, but please grab the two installers linked below and run them. If the packages are already present on your system, the installers should notify you and abort.

- Download and install [Visual C++ 2019](https://aka.ms/vs/16/release/vc_redist.x64.exe).
- Download and install [.NET Framework 4.8](https://dotnet.microsoft.com/download/dotnet-framework/thank-you/net48-web-installer).

If either of the redists were missing on your system, they will be installed now. Afterwards, you may be required to restart your PC.

### Skyrim Clean Install

TPF requires a clean install with the following specifications:

- Skyrim Special Edition `1.6.1170` plus Anniversary Edition DLC
- Creation Kit <u>not</u> installed (you can add it later)
- Language set to English
- Installation directory outside UAC-protected folders

There are detailed instructions for performing a clean install [here](/tpf/resources/clean-install/).

## Wabbajack Setup

Next up you need to install the Wabbajack tool itself:

- Download [Wabbajack](https://www.wabbajack.org/#/) from the official website.
- Extract the archive to a high-level folder, e.g. `C:\Wabbajack\`.

**Do not install Wabbajack into UAC protected directories.** These include Program Files and Program Files x86 as well as the Downloads, Desktop, Documents, etc, folders.

- Double-click **Wabbajack.exe** to launch the tool. It will automatically update itself to the latest version.

## Installing TPF

You can now install TPF through Wabbajack:

- Click the **Browse Modlists** button in the Wabbajack tool.
- Find **The Phoenix Flavour** in the gallery of mod lists and click the arrow button to download the installation file.

In the installation window, you will need to define two folders:

- **Installation Location** is where TPF will be installed to. Choose a high-level folder such as `C:\The Phoenix Flavour\` that is outside UAC protected folders (Program Files, Documents, etc).
- **Download Location** is where the downloaded mod archives will be stored. By default, they will be placed within your main TPF folder, but you can change the file path if you want to keep the files elsewhere.

Once both folder locations have been set, click the button on the right to begin the installation process.

### Troubleshooting

If you run into any issues during the installation process, please refer to the [Troubleshooting](/tpf/resources/troubleshooting/) page.

## Playing TPF

Once the installation process has completed successfully, you can play the game. However, you cannot access TPF by launching Skyrim through Steam.

Instead, navigate to `\The Phoenix Flavour\` and launch the **ModOrganizer.exe**. This will open Mod Organizer 2.

- Check the [Customisation] page for further modification options.
- Check the [Documentation] or at least the [Quick Start Guide].
- Or just click play to jump into the game!

## Updating TPF