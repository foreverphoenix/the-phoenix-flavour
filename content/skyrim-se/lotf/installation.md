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

## Steam Installation

> **Skip this step if you are using the GOG version of Skyrim SE.** Note that if, for whatever reason, you have both Steam and GOG version installed, Wabbajack will prioritise the Steam version.

**LOTF requires the latest version of Skyrim SE.** This is currently `1.6.640.0` on Steam.

Because LOTF is using the default game folder (with the Root Builder plugin), it is crucial that this folder is located **outside** any UAC-protected folders. To ensure this is the case and that no left-over files from previous mod setups can interfere with LOTF, I recommend doing a full clean install of the game.

If you never modded Skyrim SE and/or never installed other Wabbajack lists, you may skip the full reinstall. However, I still recommend you verify the game files through Steam.

- Uninstall **Skyrim SE** through Steam.
- Navigate to the Steam directory where Skyrim SE was previously installed.
- If there is still a `\Steam\steamapps\common\Skyrim Special Edition\` folder, delete it.

> When uninstalling a game through Steam, only vanilla files are removed. Mod-added files must be deleted manually.

### INI Folder

Other game files are located inside the so-called **INI Folder** which should be cleaned out as well. It contains your **savegames** as well as the game’s INI files and, if you modded Skyrim before, SKSE plugin logs.

- Navigate to the INI Folder: `C:\Users\{Your User Name}\Documents\My Games\Skyrim Special Edition\`.
- If you have an ongoing vanilla playthrough, back up the **Saves** folder.
- Delete everything inside the **Skyrim Special Edition** folder.

### Set language to English

**LOTF requires the English language version of Skyrim SE.** If you are currently playing in a language other than English, please go into the settings for Skyrim SE in your Steam library and revert the language to English.

### Installation Directory

The reinstallation also serves the purpose of relocating the game files to a better directory. Using UAC protected folders (such as `C:\Program Files\` or `C:\Program Files x86\`) for the game or any modding tools has a risk of causing issues down the line. It is best to avoid those folders to begin with.

> Most Wabbajack list curators, myself included, will not provide support for people that disregard this warning and use UAC protected folders anyway.

Note that this does not include the Steam client. Most people will have it installed under `C:\Program Files x86\Steam\` which is completely fine.

Skyrim SE and Legends of the Frost (Mod Organizer 2) should be installed on the same hard drive. Ideally that hard drive would be an SSD to reduce loading times and eliminate stuttering.

### Steam Library

In order to prevent some confusion, I will refer to the Library in Steam as the **Game Library**. It is the second of four items in the top menu in the Steam client and contains a list of all your games.

A **Steam Library** on the other hand is a folder on your hard drive into which Steam games are installed. By default, this would be `C:\Program Files x86\Steam\steamapps\common\`. Since we do not want to have files inside a UAC protected folder like `Program Files x86`, we should not install Skyrim SE in the default directory. A new **Steam Library** is required.

> Unfortunately Steam allows only one Steam Library per hard drive. You can find a workaround [here](https://github.com/LostDragonist/steam-library-setup-tool/wiki/Usage-Guide).

**If you already have a separate Steam Library outside the UAC protected folders on the drive you want to install Skyrim SE and LOTF on, skip ahead to the next step.**

Otherwise follow the instructions below to create a new Steam Library:

- Open **Steam** and go into the **Settings**.
- In the Downloads tab, select **Steam Library Folders**.
- Click **Add Library Folder**.
- Point it to a location somewhere outside the UAC protected folders, e.g. `G:\Steam Library\`.
- Close all windows when you’re done.

### Reinstallation

Now we can re-install Skyrim SE:

- Open Steam and go into your **Game Library**.
- Find **Skyrim Special Edtion** in the list and click **Install**.
- As location, select a **Steam Library** in a non-UAC protected folder and click **Next**.

Wait for the download to complete before you proceed.

### INI Files & Creations

After re-installing the game, it is important to launch it at least once through Steam so that the registry keys are set up, allowing Wabbajack and Mod Organizer to find the game. Upon launching the game, the default set of INI files will also be regenerated.

- Find **Skyrim Special Edtion** in your **Games Library** and hit **Play**.
- You will be prompted with a notification that Skyrim SE is configuring your video options, click **OK**.
- Click **OK** again in the next window.

The preset that is selected now will be irrelevant. LOTF uses its own set of INI files.

- Click **Play** to launch the game.

In the main menu, you should be prompted with a message box, informing you that the AE DLC Creations would not be downloaded.

- Click **OK** and wait for the download to complete.
- Exit the game.

### Future Proofing

Updates to Skyrim SE will break the Skyrim Script Extender and a variety of mods, and render you unable to play until those mods have been updated in turn. To prevent this from happening, I recommend changing the game's update behaviour in Steam.

This way, you will be able to postpone an update indefinitely as long as you always launch the game through Mod Organizer 2.

- Open Steam and find **Skyrim Special Edtion** in your **Game Library**.
- Right-click it and select **Properties**
- In the **Updates** tab, change **Automatic updates** to **Only update this game when I launch it**.
- Close the **Properties** window.

## GOG Installation

> Skip this step if you installed Skyrim SE through Steam.

**LOTF requires the latest version of Skyrim SE.** This is currently `1.6.659.0` on GOG.

Because LOTF is using the default game folder (with the Root Builder plugin), it is crucial that this folder is located **outside** any UAC-protected folders. To ensure this is the case and that no left-over files from previous mod setups can interfere with LOTF, I recommend doing a full clean install of the game.

- Uninstall **Skyrim Special Edition** through GOG Galaxy.
- Navigate to the directory where Skyrim SE was previously installed.
- If there is still a `\Skyrim Special Edition\` folder, delete it.

(It is possible that only vanilla files are removed by the uninstallation process while mod-added files must be deleted manually.)

### INI Folder

Other game files are located inside the so-called **INI Folder** which should be cleaned out as well. It contains your **savegames** as well as the game’s INI files and, if you modded Skyrim before, SKSE plugin logs.

- Navigate to the INI Folder: `C:\Users\{Your User Name}\Documents\My Games\Skyrim Special Edition\`.
- If you have an ongoing vanilla playthrough, back up the **Saves** folder.
- Delete everything inside the **Skyrim Special Edition** folder.

### Set language to English

**LOTF requires the English language version of Skyrim SE.** If you previously switched to a language other than English, please follow these instructions:

- In GOG Galaxy, open the **Skyrim Special Edition** page.
- Click the configuration button next to **Play**.
- Select **Manage installation** > **Configure**.
- Set **Language** to **English** and click **OK**.

### Reinstallation

Now we can re-install Skyrim SE through GOG Galaxy. When choosing an installation directory, keep the following in mind:

- Skyrim SE must be located **outside** any UAC-protected folders, e.g. `C:\Program Files\` or `C:\Program Files x86\`.
- Skyrim SE should be located **on the same hard drive** that you will be installing LOTF on.

Ideally, install the game on an SSD for improved loading times.

Wait for the download to complete before you proceed.

### Regenerating INIs

After re-installing Skyrim SE, it is important to launch it once so that the registry keys are set up, allowing Wabbajack and Mod Organizer to find the game. Upon launching the game, the default set of INI files will also be regenerated.

- Find **Skyrim Special Edtion** in your **Games Library** and hit **Play**.
- You will be prompted with a notification that Skyrim SE is configuring your video options, click **OK**.
- Click **OK** again in the next window, then quit the launcher.

## Wabbajack Installation

Next up, you need to install the Wabbajack tool itself:

- Download [Wabbajack](https://www.wabbajack.org/#/) from the official website.
- Extract the archive to a high-level folder, e.g. `G:\Wabbajack\`.

**Do not install Wabbajack into UAC protected directories.** These include `\Program Files\` and `\Program Files x86\` as well as the Downloads, Desktop, Documents, etc, folders.

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

Navigate to your **Legends of the Frost** folder and launch the **ModOrganizer.exe** within. In the top right drop-down menu, **Skyrim Script Extender** should already be selected and you can now launch the game by clicking **Run**.

> **GOG people:** Double-click the `GOG Support` separator in MO2 and activate all four mods grouped below it before launching the game.

![Play LOTF](/Pictures/lotf/installation/launch-lotf.png)

### MCM Instructions

LOTF only has a handful of Mod Configuration Menus (MCMs). **Presets are automatically applied so you don't need to edit anything manually.** I strongly recommend not changing anything in the MCMs unless you have something specific in mind.

### Performance Profile

If your system is on the lower mid end, you may want to try the **Performance** profile.

Note that saves are profile-specific. You can switch from the regular to the performance profile mid-playthrough, but you would have to copy over the saves from `\Legends of the Frost\profiles\Legends of the Frost\saves\` to `\Legends of the Frost\profiles\Legends of the Frost - Performance\saves\` manually. Please do not attempt to switch from the CC profile to either the regular or performance profile in an ongoing playthrough.

Check the picture below to see how to switch to a different profile in MO2:

![Swap MO2 Profile](/Pictures/lotf/installation/lotf-performance-profile.png)

### Customisation

Before you begin a new playthrough, you may want to check out the tweaks and optional mods that are supported for LOTF on the [Customisation](/skyrim-se/lotf/customisation) page.