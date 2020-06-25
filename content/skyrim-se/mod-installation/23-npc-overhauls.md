---
title: "23 NPC Overhauls"
weight: 23
type: docs
description: >
  Facegen overhauls for specific NPCs.
---

## 23.1 Vanilla NPCs Ruhmastered

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/25977?tab=files)

* **Main Files:** Vanilla NPCs SSE Ruhmastered v2.1
* **Optional Files:** Vanilla NPCs SSE Ruhmastered with Beast Glow v2.0 --- `merge with the main file`
* **Optional Files:** Vanilla Vampire NPCs SSE Ruhmastered Vampire Red Glow v2.0 --- `merge with the main file`

> Make sure the resulting file is called **Vanilla NPCs SSE Ruhmastered** in Mod Organizer 2. The name will later be used for a dummy ESP which in turn will not be recognised by the loadorder.txt if it isn't called exactly this.

#### Additional Instructions

In order to be able to control the mod’s facegen files via load order, we need to pack the loose files in a BSA and activate it with an empty plugin.

* Open **Cathedral Assets Optimizer**.
* From the **Profiles** drop-down menu, select the **SSE - Create BSA** profile.
* Click **Open Directory** and point it at the `Mod Organizer 2\mods\Vanilla NPCs SSE Ruhmastered` folder.
* Click **Run** to start the process. You can check the progress in the **Log** tab.
* Close Cathedral Assets Optimizer once it’s done. Refresh (F5) Mod Organizer 2 and you will see the assets are now packed.

## 23.2 Windsong Immersive Character Overhaul (WICO)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/2136?tab=files)

* **Main Files:** WICO Special Edition – VNL 0.9f

#### FOMOD Instructions

* **Options:** Custom
* **Patch Files:** ~~USSEP Compatible Patch~~
* **Option 01:** ~~Additional Followers~~
* **Option 02:** ~~Clean Body Textures~~
* **Option 03:** ~~Less Flush Face Textures~~
* **Option 04:** ~~The Witcher Gear Sets~~

> We do not install the pre-packaged USSEP Patch because it is incomplete. 

#### Additional Instructions

* Delete the following file(s) and/or folder(s):
  * `WICO - Immersive Character.esp`
  * `WICO - Immersive Character.bsa`
  * `WICO - Immersive Character.bsl`
  * `WICO - Immersive People.bsa`
  * `WICO - Immersive People.bsl`

> Basically this removes all vanilla texture replacers and the new player character presets, leaving only the changes to individual NPCs. A stripped BSA with matching facegen for those changes will be installed in the next step.

## 23.3 Windsong Immersive Character Overhaul – Stripped BSA

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/5049?tab=files)

* **Main Files:** Striped BSA for default settings

## 23.4 Windsong Immersive Character Overhaul – USSEP and CRF Patches

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/26092?tab=files)

* **Main Files:** Windsong Immersive Character Overhaul – USSEP and CRF Patches

#### FOMOD Instructions

* Change nothing, simply click **Next** and **Install**.

## 23.5 Ethereal Elven Overhaul

#### [Download Instructions](https://www.nexusmods.com/skyrim/mods/24273?tab=files)

* **Main Files:** Ethereal Elven Overhaul

#### Additional Instructions

* Delete the following file(s) and/or folder(s):
  * `meshes\actors\character\facegendata\`
  * `textures\actors\character\facegendata\`
  * `ethereal_elven_overhaul.esp`

## 23.6 Ethereal Elven Overhaul – SSE Patch

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/7351?tab=files)

* **Main Files:** Special Edition patch

## 23.7 TK Children

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/5916?tab=files)

* **Main Files:** TK Children SE

#### FOMOD Instructions

* Irrelevant, just click **Next** and **Install**. We are only interested in this mod’s TRI files which are required for Simple Children.

#### Additional Instructions

* Delete the following file(s) and/or folder(s):
  * `meshes\actors\character\facegendata`
  * `meshes\actors\character\TKChildren`
  * `textures\`
  * `TKChildren.esp`
  * `TKChildren.esm`

Rename the mod to **TK Children - TRI Files** in order to indicate that it is not the full mod.

## 23.8 Simple Children

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/22789?tab=files)

* **Main Files:** Simple Children Main - FOMOD
* **Update Files:** Simple Children - Updated Textures
* **Optional Files:** Simple Children - Babette Glowing Eyes
* **Optional Files:** Patches for Simple Children - AIO

#### FOMOD Instructions - Main File

* **Texture Choices:** Paler Eye Area

#### FOMOD Instructions - Updated Textures

* **Texture Options:** Clean Face and Body Textures

#### FOMOD Instructions - Patches

* **Patches Page 1:**
  * ~~Beyond Reach~~
  * ~~Beyond Skyrim Bruma~~
  * ~~Blackthorn – A Buildable Town In The Rift~~
  * ~~Books Of Skyrim~~
  * ~~Cutting Room Floor~~
  * ~~Dragons Keep SE~~
  * ~~ETaC – Darkwater Crossing~~
  * ~~ETaC – Dawnstar~~
  * ~~ETaC – Riverwood~~
  * ~~ETaC – Rorikstead~~
  * ~~Expanded Towns and Cities – Complete~~
  * ~~Falskaar~~
  * ~~Gavrostead SE~~
  * ~~Greater Skaal Village~~
  * ~~Helgen Reborn~~
  * ~~Immersive Weapon Integration~~
  * ~~Immersive World Encounters~~
* **Patches Page 2:** 
  * ~~Inconsequential NPCs~~
  * Interesting NPCs
  * ~~Keld-Nar~~
  * ~~Legacy of the Dragonborn~~
  * ~~Moon and Star~~
  * ~~Outlaws and Revolutionaries~~
  * ~~Qaxe’s Questorium~~
  * ~~Rigmor of Bruma~~
  * ~~Rigmor of Cyrodiil~~
  * ~~Settlements Expanded~~
  * ~~Solitude Expansion~~
  * The Forgotten City
  * ~~The People of Skyrim Complete~~
  * ~~Wyrmstooth~~
* **Prince and Pauper:**
  * USSEP Version
* **Adopt Aventus Aretino:**
  * Adopt Aventus Aretino + Prince and Pauper + USSEP
* **Skaal Coat For Kids:**
  * ~~Skaal Coat Addon~~

#### Mod Order

* Place **Simple Children - Patches** below the **PATCHES** separator.