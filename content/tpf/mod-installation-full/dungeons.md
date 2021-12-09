---
title: "Dungeons"
weight: 17
type: docs
description: >
  Retextures for underground areas, ruins, barrows, and related clutter.
---

##### [Underground - A Dungeon Texture Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/14365?tab=files)

#### Download Instructions

* **Main Files:** Underground FOMOD

> There is no need to download the Whiterun Tower Fix because regenerating DynDOLOD later on will correct the issue.

#### FOMOD Instructions

* **Main Options:**
  * Custom installation
* **Options:**
  * 00 Caves
  * 01 Mines
  * 02 Nordic
  * ~~03 Dwemer~~
  * 04 Imperial
  * 05 Riften
  * 06 Apocrypha

#### Additional Instructions

- Delete the following file(s) and/or folder(s):
  - `textures\dlc02\dungeons\apocrypha\apocryphabanner01.dds`
  - `textures\dlc02\dungeons\apocrypha\apocryphabanner01_g.dds`
  - `textures\dlc02\dungeons\apocrypha\apocryphabanner01_n.dds`
  - `textures\dungeons\riften\ratwaywood01.dds`
  - `textures\dungeons\riften\ratwaywood01_n.dds`

#### Helgen Mud Fix

One of the meshes in Underground is in the wrong folder and will cause the mud on the ground during the intro quest to be weirdly shiny.

- Right-click **Underground** in your mod order and select **Open in Explorer**.
- Navigate to `meshes\clutter` and create a new folder called **helgen**.
- Move **helgenmud01.nif** into the new **helgen** folder.
- The resulting file path should be `meshes\clutter\helgen\helgenmud01.nif`.

> The reason why I am not doing this within MO2's UI is because it can get a bit buggy when moving files and sometimes doesn't show that the file has indeed been moved.

