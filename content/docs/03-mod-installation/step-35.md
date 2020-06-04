---
title: "New Items & Equipment"
weight: 35
type: docs
description: >
  More armor variants and unique equipment.
---

## 35.1 Armor and Clothing Extension (ACE)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/19002?tab=files)

* **Main Files:** Armor and Clothing Extension

## 35.2 Armor and Clothing Extension – MCM Fix

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/23471?tab=files)

* **Main Files:** WACCF_MCM_Fix

## 35.3 Weapons Armor Clothing and Clutter Fixes – CBBE Patch

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/19176?tab=files)

* **Main Files:** Weapons Armor Clothing and Clutter Fixes – CBBE Patch

#### FOMOD Instructions

Make sure **Armor and Clothing Extension** is activated before you proceed.

* **WACCF:** WACCF + ACE

#### Mod Order

* Place the mod below the **PATCHES** separator.

## 35.4 aMidianBorn Content Addon

#### [Download Instructions](https://www.nexusmods.com/skyrim/mods/24909?tab=files)

* **Optional Files:** aMidianBorn – Content Addon

## 35.5 aMidianBorn Content Addon

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/35390?tab=files)

* **Main Files:** aMidianBorn Content Addon

#### About the mod

This is kryptopyr's official AMB CA SSE port which includes an updated plugin and some fixed assets. The original AMB CA is still required which is why we installed it in the previous step.

## 35.6 Practical Female Armors - AMB Content Addon (optional)

#### Download Instructions

- You already downloaded this file.

#### Installation Instructions

* Find the following file in your **Downloads** tab:
  * Practical Female Armors SE - All-In-One Installer - NMM BAIN-2628-1-3o
* Double-click to install as usual.
* Rename the file to **Practical Female Armors - AMB Content Addon** to prevent overwriting the original.
* In the FOMOD installer, select only the **aMidianBorn Content Addon** option on the final page.

## 35.7 Common Clothes and Armors

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/21305?tab=files)

* **Main File:** Common Clothes and Armors

## 35.8 Common Clothes and Armors – CBBE Patch

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/31750?tab=files)

* **Main Files:** Common Clothes and Armors – CBBE Patch

#### FOMOD Instructions

* **Body Shape:** CBBE Vanilla

## 35.9 Armor of Yngol

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/5006?tab=files)

* **Main File** - Yngol SSE

## 35.10 Unique Scimitars

#### [Download Instructions](https://www.nexusmods.com/skyrim/mods/60896?tab=files)

* **Main File** - Redguard unique scimitars 1.3 

#### Porting Instructions

* Resave **Redguard_unique_swords.esp** in the Creation Kit.

#### Additional Instructions

This will disable crafting of the four scimitars in order to make them truly unique.

* Run SSEEdit through Mod Organizer 2.
* Click **OK** in the plugin selection window to load all mods and wait.
* Once everything is loaded up, double-click **Redguard_unique_swords.esp** (left pane – bottom).
* Double-click the **Constructible Object** category.
* Select the following four records, right-click and **Remove** (see picture):
  * **RecipeWeaponRobin**
  * **RecipeWeaponNajash**
  * **RecipeWeaponRysh**
  * **RecipeWeaponRysh2**
* Close SSEEdit and click **OK** to save your changes.

![Disable Crafting Unique Scimitars](/Pictures/mod_installation/disable_crafting_unique_scimitars.png)

## 35.11 Kthonia’s Unique Weapon Pack – Dragonborn Weapons (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/15050?tab=files)

* **Main File** - Kthonia’s Weapon Pack SE – Smaller Textures (2K)

#### Additional Instructions

* Run SSEEdit through Mod Organizer 2.
* Click **OK** in the plugin selection window to load all mods and wait.
* Once everything is loaded up, double-click **ktWeaponPackSE.esp** (left pane – bottom).
* Double-click the **Weapon** category.
* Select the **mkChitinBow01** record and scroll down to the **Keywords** section.
* Right-click and remove the following keyword:
  * `DLC2ArmorMaterialChitinLight [KYWD:04024102]`
* Next, select the **mkChitinBow02_nopearls** record and scroll down to the **Keywords** section once again.
* Right-click and remove the same keyword:
  * `DLC2ArmorMaterialChitinLight [KYWD:04024102]`
* Close SSEEdit and click **OK** to save your changes.

> The bow with two perks would benefit twice as much from tempering which is unintended. This bug was found and fixed by [Kulharin](https://www.nexusmods.com/skyrimspecialedition/mods/29298) but the fix can easily be applied to your own copy of the plugin without an additional patch ESP.

![Fix Kthonia Chitin Bow](/Pictures/mod_installation/fix_kthonia_chitin_bow.png)