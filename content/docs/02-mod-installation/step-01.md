---
title: "Essential Mods"
weight: 1
type: docs
description: >
  Basic mods and frameworks.
---

## Address Library for SKSE Plugins

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/32444?tab=files)

- **Main Files:** All in one

## SSE Engine Fixes

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/17230?tab=files)

- **Main Files:** (Part 1) Engine Fixes

#### Preloader

- Download the following file manually:
  * **(Part 2) Engine Fixes - skse64 Preloader and TBB Lib**
- Open the downloaded archive.
- Extract the following files into your **root** folder:
  * **d3dx9_42.dll**
  * **tbb.dll**
  * **tbbmalloc.dll**
- Click **Yes** when asked to overwrite.

#### Engine Fixes INI

* Double-click **SSE Engine Fixes** in your mod order.
* Switch to the **INI-Files** tab and select the **EngineFixes.ini**.
* Edit the following line:
  * `SleepWaitTime = true`
* Close the window and click **Yes** when asked to save your change.

## .NET Script Framework (NSF)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/21294?tab=files)

- **Main Files:** NetScriptFramework SkyrimSE v13

## SSE Display Tweaks

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/34705?tab=files)

- **Main Files:** SSE Display Tweaks

## Autorun Console Commands (ACC)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/24919?tab=files)

- **Main Files:** ACC - Autorun Console Commands

## Unofficial High Definition Audio Project

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/18115?tab=files)

- **Main Files:** Music - HQ
- **Main Files:** Voices EN - Part 1
- **Main Files:** Voices EN - Part 2

## Unofficial Skyrim Special Edition Patch (USSEP)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/266?tab=files)

- **Main Files:** Unofficial Skyrim Special Edition Patch

#### Additional Instructions

- Delete the following file(s) and/or folder(s):
  * `Unofficial Skyrim Special Edition Patch.modgroups`

## Alternate Start - Live Another Life (AS LAL)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/272?tab=files)

- **Main Files:** Alternate Start - Live Another Life

## Skyrim Particle Patch

#### [Download Instructions](http://enbseries.enbdev.com/forum/viewtopic.php?t=1499)

- Find the **SPECIAL EDITION** section in the forum post linked above and click the **GOOGLE DRIVE** link (see picture).
- Download the archive from Google Drive and move it manually to `Your Modding Folder\ARCHIVE\MO2 Downloads`.
- Go to the **Downloads** tab and double-click the mod to install it as usual.
- I recommend renaming it simply to **Skyrim Particle Patch** after the installation.

![Skyrim Particle Patch download link](/Pictures/mod_installation/skyrim_particle_patch_download.png)

#### Additional Instructions

- Delete the following file(s) and/or folder(s):
  - `textures\effects\gradients\gradwhitewater.dds`
  - `Particle Patch for ENB SSE.esp`

> The plugin is not needed. Its functionality was replaced by ENB Helper. The texture can cause water spray to look much darker than intended with Realistic Water Two.

## Static Mesh Improvement Mod (SMIM)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/17230?tab=files)

- **Main Files:** SMIM SE 2-08

#### FOMOD Instructions

- **Main Installer Choice:** Skyrim 2016 Special Edition: Everything

#### Additional Instructions

- Delete the following file(s) and/or folder(s):
  * `meshes\architecture\farmhouse\walkway\walkwaycwall01.nif`
  * `meshes\architecture\solitude\doors\sgatedoor.nif`

> The first mesh will be replaced either by the fixed version contained in Skyrim Landscape and Water Fixes or by Real Walls 3D.  Deleting the second mesh will allow you to use a different retexture for the Solitude city gate.