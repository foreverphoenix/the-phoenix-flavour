![Logo](Pictures/Logo%20Mockup.png)

- [Installation Instructions](#installation-instructions)
  - [Overview](#overview)
  - [General Instructions](#general-instructions)
    - [Downloading Mods](#downloading-mods)
    - [Installing Mods](#installing-mods)
    - [FOMOD Instructions](#fomod-instructions)
    - [Deleting Files](#deleting-files)
    - [Manual Editing Instructions](#manual-editing-instructions)
  - [Special Instructions](#special-instructions)
    - [Convert Plugin](#convert-plugin)
    - [Clean Plugin](#clean-plugin)
    - [Extract BSA](#extract-bsa)
    - [Optimise SLE Assets](#optimise-sle-assets)
    - [Fix Meshes](#fix-meshes)
    - [Resize Textures](#resize-textures)
- [01. Essential Mods](#01-essential-mods)
  - [1.1 Address Library for SKSE Plugins](#11-address-library-for-skse-plugins)
  - [1.2 SSE Engine Fixes](#12-sse-engine-fixes)
  - [1.3 .NET Script Framework (NSF)](#13-net-script-framework-nsf)
  - [1.4 SSE Display Tweaks](#14-sse-display-tweaks)
  - [1.5 Autorun Console Commands (ACC)](#15-autorun-console-commands-acc)
  - [1.6 Performance Optimized Textures for SSE](#16-performance-optimized-textures-for-sse)
  - [1.7 Unofficial High Definition Audio Project (optional)](#17-unofficial-high-definition-audio-project-optional)
  - [1.8 Unofficial Skyrim Special Edition Patch (USSEP)](#18-unofficial-skyrim-special-edition-patch-ussep)
  - [1.9 Alternate Start - Live Another Life (AS LAL)](#19-alternate-start---live-another-life-as-lal)
  - [1.10 Skyrim Particle Patch](#110-skyrim-particle-patch)
  - [1.11 Static Mesh Improvement Mod (SMIM)](#111-static-mesh-improvement-mod-smim)

# Installation Instructions

## Overview

After completing the Setup, you are equipped with a correctly installed and configured instance of Mod Organizer 2 that is set up for the Skyrim Script Extender. It is now time to dive into the by far longest section in the guide – the mod installation.

- The mods themselves are split up into forty categories which correspond to the separators of the same names installed for MO2 in the Setup. **Each set of mods must be installed in the order they are listed in** and grouped below their respective separator.
- Instructions for which file(s) to download as well as any further steps are listed below the mod name. These detailed instructions are **mandatory** and must be followed.
- All listed mods are **required** and must be installed unless they are clearly flagged as **(optional)** in which case you may skip them. Whether or not a mod is optional is typically determined by interactions with other mods (patches and dependencies).
- Occasionally a mod will have further steps noted under **Additional Instructions** or **Porting Instructions** such as “Resave Example.esp in the Creation Kit”. You can find detailed instructions further down on this page.
- It may be faster to download all mods of one page first, then install them and finally go through all additional instructions.

**Do not attempt to launch Skyrim SE before you are instructed to**. During the installation you will have missing dependencies and unresolved conflicts fixed later by additional mods.

## General Instructions

### Downloading Mods

* Almost all mods are hosted on the Nexus.
* CTRL-clicking a mod’s name will take you immediately to its Nexus page.
* The files listed under **Download Instructions** are marked with the respective section you can find them in on the Nexus:
  * Main Files
  * Update Files
  * Optional Files
  * Miscellaneous Files
  * Old Files
* In the **Files** section on the mod page, download the file(s) by clicking "Mod Manager Download".
  * When a mod has special requirements, they are then listed in a pop-up window where you will have to click the **Download** button again.
  * Don’t worry about these requirements, they are included in the guide or otherwise taken care of.

### Installing Mods

* After downloading a mod, switch to the **Downloads** tab in the right pane of Mod Organizer 2 and double-click the file(s) to install.
* This may open a FOMOD installer if the mod includes one. In this case you need to follow the **FOMOD Instructions** listed in the guide.
* After installing a mod you may want to rename it in order to reflect the version you downloaded or options you selected in the FOMOD:
  * For retextures it is useful to add the texture resolution: **Embers HD 2k**.
  * If there are different versions, note down which one you downloaded: **Less Ugly Tundragrass – Redder Variant**.
* When installing more than one file from the same mod page, always click **Rename** when prompted and give the file a unique name to install it separately. ==**Do not select Merge or Replace**==.

### FOMOD Instructions

Some mods come with a FOMOD Installer in which case instructions are provided. Occasionally the choices do not have to be strictly followed (particularly when they are related to texture resolution or variations) however there are some FOMODs that you have to install exactly as indicated in the instructions. Please do follow the provided instructions.

### Deleting Files

* When instructed to delete one or several files, double-click the mod in your mod order.
* Switch to the **Filetree** tab and find the files you need to remove.
* Simply right-click them and select **Remove** (or select them and hit DELETE on your keyboard).

### Manual Editing Instructions

Very rarely you will be instructed to edit a plugin directly in SSEEdit. If you never touched this program before, it may be somewhat  confusing at first. The edits you will be asked to make are quite simple and straight-forward however. Mods with such instructions are always optional and may be skipped.

## Special Instructions

### Convert Plugin

> "Resave Example.esp in the Creation Kit."

Plugins with Form Version 43 (typically downloaded from the Classic Skyrim Nexus) must be re-saved in the CK.

* Run the **Creation Kit** through Mod Organizer 2.
* Once it is loaded up, go to **File > Data**.
* Select the plugin you need to convert in the list and click **Set as Active File**.
* Click **OK** and wait for the Creation Kit to load up the plugin.
* Go to **File > Save**. There will be a small confirmation message (**Saving… done!**) at the bottom of the window.
* Close the Creation Kit.
* Afterwards, you can right-click the mod in MO2 and select **Mark converted/working**.

### Clean Plugin

> "Clean Example.esp with SSEEdit."

Very rarely a plugin may contain “dirty edits” or deleted records in  which case you need to run it through the QuickAutoClean version of  SSEEdit (just like we did with the official master files).

* Run **SSEEdit – QuickAutoClean** through Mod Organizer 2.
* Check only the plugin you were instructed to clean in the plugin list.
* Click **OK** and wait for the process to complete (`Quick Clean mode finished`).
* Close SSEEdit.

### Extract BSA

> "Unpack Example.bsa through Mod Organizer 2.

Occasionally you will be instructed to unpack an archive, either because it was packed with the 32bit CK, or because we need the files  loose to overwrite or selectively delete.

* Switch to the **Archives** tab in the right pane of Mod Organizer 2.
* Find the archive you need to unpack and right-click it (it will only show up if the mod is checked in the mod and load order).
* Navigate to `Mod Organizer 2\mods`, click on the mod folder the archive belongs to and click **Select Folder**.
* After unpacking the files, press F5 to refresh Mod Organizer 2.
* Double-click the mod the archive is part of in your mod order.
* Switch to the **Filetree** tab and right-click > delete the BSA.

Deleting the BSA after extracting it is extremely important. Your game may crash on launch otherwise.

### Optimise SLE Assets

> "Run the mod through Cathedral Assets Optimiser."

Skyrim LE meshes often need to be fixed and optimised by Cathedral Assets Optimizer before they can be used in SE. We will also use CAO on mods to optimise (compress) included textures sometimes. If a Classic Skyrim mod does not have instructions to run it through CAO this is because I already did so and found that no meshes or textures needed optimising.

* Run **Cathedral Assets Optimizer** (do not launch it through Mod Organizer 2).
* Select the **SSE – Optimise SLE Assets** profile from the drop-down menu.
* Click **Open Directory** and navigate to `Mod Organizer 2\mods`.
* Click on the folder of the mod you wish to optimise and hit **Select Folder**.
* Back in CAO, click **Run** and wait for the process to complete.
* Afterwards, you can right-click the mod in MO2 and select **Mark converted/working**.

### Fix Meshes

> “Run the mod through SSE NIF Optimizer.”

Very few mods in the guide need to be run through SSE NIF Optimizer instead of Cathedral Assets Optimizer to fix their meshes.

* Double-click **SSE NIF Optimizer.exe** which should be located inside Your Modding Folder.
* Click **Browse** and navigate to `Mod Organizer 2\mods`.
* Click on the folder of the mod you wish to optimise and hit **Select Folder**.
* Click **Optimise** and wait until the process is finished.
* Close **SSE NIF Optimizer**.

### Resize Textures

>"Downsize the textures with Cathedral Assets Optimizer."

At times (re)textures are only available in a size unreasonably large for regular gameplay, potentially impacting performance for those with low VRAM. In those cases we will utilise CAO to reduce the texture resolution by half.

* Run **Cathedral Assets Optimizer**.
* Select the **SSE – Downsize Textures** profile from the drop-down menu.
* Click **Open Directory** and navigate to `Mod Organizer 2\mods`.
* Click on the mod containing the textures and **Select folder**.
* Back in CAO, click **Run** and wait for the process to be completed.

![separator](Pictures/Separator.png)

# 01. Essential Mods

## 1.1 [Address Library for SKSE Plugins](https://www.nexusmods.com/skyrimspecialedition/mods/32444?tab=files)

```ruby
# DOWNLOAD INSTRUCTIONS
```

- **Main File** - All in one

## 1.2 [SSE Engine Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/17230?tab=files)

```yaml
# DOWNLOAD INSTRUCTIONS
```

- **Main File** - (Part 1) Engine Fixes

```json
# PRELOADER INSTALLATION
```

- Download the following file manually:
  * **(Part 2) Engine Fixes – skse64 Preloader and TBB Lib**
- Open the downloaded archive.
- Extract the following files into your **root** folder:
  * **d3dx9_42.dll**
  * **tbb.dll**
  * **tbbmalloc.dll**
- Click **Yes** when asked to overwrite.

```markdown
# ENGINE FIXES INI
```

* Double-click **SSE Engine Fixes** in your mod order.
* Switch to the **INI-Files** tab and select the **EngineFixes.ini**.
* Edit the following line:
  * `SleepWaitTime = true`
* Close the window and click **Yes** when asked to save your change.

## 1.3 [.NET Script Framework (NSF)](https://www.nexusmods.com/skyrimspecialedition/mods/21294?tab=files)

```markdown
# DOWNLOAD INSTRUCTIONS
```

- **Main Files** – NetScriptFramework SkyrimSE v13

## 1.4 [SSE Display Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/34705?tab=files)

```markdown
# DOWNLOAD INSTRUCTIONS
```

- **Main File** - SSE Display Tweaks

## 1.5 [Autorun Console Commands (ACC)](https://www.nexusmods.com/skyrimspecialedition/mods/24919?tab=files)

```markdown
# DOWNLOAD INSTRUCTIONS
```

- **Main Files** – ACC – Autorun Console Commands

## 1.6 [Performance Optimized Textures for SSE](https://www.nexusmods.com/skyrimspecialedition/mods/21166?tab=files)

```markdown
# DOWNLOAD INSTRUCTIONS
```

- **Main Files** – performance textures max res 1024 min res 512 v8

## 1.7 [Unofficial High Definition Audio Project](https://www.nexusmods.com/skyrimspecialedition/mods/18115?tab=files) (optional)

```markdown
# DOWNLOAD INSTRUCTIONS
```

- **Main Files** – Music – HQ
- **Main Files** – Voices EN – Part 1
- **Main Files** – Voices EN – Part 2

## 1.8 [Unofficial Skyrim Special Edition Patch (USSEP)](https://www.nexusmods.com/skyrimspecialedition/mods/266?tab=files)

```markdown
# DOWNLOAD INSTRUCTIONS
```

- **Main Files** – Unofficial Skyrim Special Edition Patch

```markdown
# ADDITIONAL INSTRUCTIONS
```

- Delete the following file(s) and/or folder(s):
  * `Unofficial Skyrim Special Edition Patch.modgroups`

## 1.9 [Alternate Start - Live Another Life (AS LAL)](https://www.nexusmods.com/skyrimspecialedition/mods/272?tab=files)

```markdown
# DOWNLOAD INSTRUCTIONS
```

- **Main Files** – Alternate Start – Live Another Life

## 1.10 [Skyrim Particle Patch](http://enbseries.enbdev.com/forum/viewtopic.php?t=1499)

==**INSTALLATION INSTRUCTIONS**==

- Find the **SPECIAL EDITION** section in the forum post linked above and click the **GOOGLE DRIVE** link (see picture).
- Download the archive from Google Drive and move it manually to `Your Modding Folder\ARCHIVE\MO2 Downloads`.
- Go to the **Downloads** tab and double-click the mod to install it as usual.
- I recommend renaming it simply to **Skyrim Particle Patch** after the installation.

![Skyrim Particle Patch download link](..\Pictures\Mod Installation\Skyrim Particle Patch download link.png)

```markdown
# ADDITIONAL INSTRUCTIONS
```

- Delete the following file(s) and/or folder(s):
  * `Particle Patch for ENB SSE.esp`

> The plugin is not needed. Its functionality was replaced by ENB Helper.

## 1.11 [Static Mesh Improvement Mod (SMIM)](https://www.nexusmods.com/skyrimspecialedition/mods/659/?tab=files)

```markdown
# DOWNLOAD INSTRUCTIONS
```

- **Main Files** – SMIM SE 2-08

```markdown
# FOMOD INSTRUCTIONS
```

- **Main Installer Choice:** Skyrim 2016 Special Edition: Everything

```markdown
# ADDITIONAL INSTRUCTIONS
```

- Delete the following file(s) and/or folder(s):
  * `meshes\architecture\farmhouse\walkway\walkwaycwall01.nif`
  * `meshes\architecture\solitude\doors\sgatedoor.nif`

> **Mesh 1:**
> The deleted mesh will be replaced either by the fixed version contained in Skyrim Landscape and Water Fixes or by Real Walls 3D.

> **Mesh 2:**
> Deleting the mesh will allow you to use a different retexture for the gate.