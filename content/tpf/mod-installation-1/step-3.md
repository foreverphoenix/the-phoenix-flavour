---
title: "Step 3: Assorted Plugins"
weight: 3
type: docs
description: >
  Various SKSE and NET Script Framework plugins.
---

##### [Scrambled Bugs](https://www.nexusmods.com/skyrimspecialedition/mods/43532?tab=files)

#### Download Instructions

- **Main Files:** Scrambled Bugs
- **Main Files:** Scrambled Eggchantments
- **Optional Files:** Underfilled Soul Gems - Soul Gem Too Small

#### Additional Instructions - Scrambled Bugs

- Double-click **Scrambled Bugs** in your mod order.
- Switch to the **Text Files** tab and select the **ScrambledBugs.json** file.
- In **Line 11**, set `"magicEffectConditions":` to `false`.
- In **Line 30**, set `"equipBestAmmo:"` to `true`.
- In **Line 34**, set `"powerAttackStamina` to `true`.
- In **Line 37**, set `"underfilledSoulGems":` to `true`.
- Hit **CTRL+S** to save and close the window.

#### Additional Instructions - Scrambled Eggchantments

- Double-click **Scrambled Eggchantments** in your mod order.
- Switch to the **Text Files** tab and select the **ScrambledEggchantments.json** file.
- In **Line 8**, set `"enchantmentValue":` to `true`.
- Hit **CTRL+S** to save and close the window.

##### [powerofthree's Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/51073?tab=files)

#### Download Instructions

- **Main Files:** powerofthree's Tweaks
- **Optional Files:** INI file

> We are installing the INI file separately so it does not get overwritten when the main file is updated.

#### Additional Instructions

- Double-click **powerofthree's Tweaks** in your mod order.
- Switch to the **INI Files** tab and select the **po3_Tweaks.ini**.
- In **Line 72**, change `No Attack Messages =` to `3`.
- In **Line 86**, change `Grabbing Is Stealing =` to `true`.
- Hit **CTRL+S** to save your changes and close the window.

##### [Bug Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/33261?tab=files)

#### Download Instructions

- **Main Files:** Bug Fixes SSE v3

##### [Actor Limit Fix](https://www.nexusmods.com/skyrimspecialedition/mods/32349?tab=files)

#### Download Instructions

- **Main Files:** ActorLimitPlugin v2

##### [NPC AI Process Position Fix](https://www.nexusmods.com/skyrimspecialedition/mods/40261?tab=files)

#### Download Instructions

- **Main Files:** NPC AI Process Pos Fix-SSE-V4.05d

##### [Animated Static Reload Fix](https://www.nexusmods.com/skyrimspecialedition/mods/53761?tab=files)

#### Download Instructions

- **Main Files:** Animated Static Reload Fix - SSE

##### [Equip Enchantment Fix](https://www.nexusmods.com/skyrimspecialedition/mods/42839?tab=files)

#### Download Instructions

- **Main Files:** Equip Enchantment Fix

##### [Simple Offence Suppression](https://www.nexusmods.com/skyrimspecialedition/mods/41764?tab=files)

#### Download Instructions

- **Main File:** Simple Offence Suppression

##### [Classic Paralysis](https://www.nexusmods.com/skyrimspecialedition/mods/45931?tab=files)

#### Download Instructions

- **Main Files:** Classic Paralysis

##### [Enhanced Reanimation](https://www.nexusmods.com/skyrimspecialedition/mods/43500?tab=files)

#### Download Instructions

- **Main Files:** Enhanced Reanimation

#### Additional Instructions

The INI file for Enhanced Reanimation would normally be generated upon launching the game and then be dumped into the MO2 Overwrite. Since multiple mods work like this, it would create a mess of various different files that need to be manually moved into their appropriate mod folders. It's faster to simply create the file by hand and in the right spot.

- Right-click **Enhanced Reanimation** in your mod order and select **Open in Explorer**.
- Navigate to `SKSE\Plugins\`. Right-click and select **New > Text Document**.
- Rename it from **New Text Document.txt** to **po3_EnhancedReanimation.ini**.
- Open your new INI file and paste the following inside:

```
[Settings]

;fast travel fix
Fast Travel = true

;reanimated necromancers can cast reanimate spells
Necromancer Cast = true

;reanimate decapitated enemies
Decapitated NPCs = true


[Riding]

;ride reanimated horses/mounts (not dragons)
Ride Horses = true

;patch all reanimate spells so mounts can be reanimated
Patch Horses = true
```

- Save your changes and close the file.

##### [Sales Overflow Solved](https://www.nexusmods.com/skyrimspecialedition/mods/41625?tab=files)

#### Download Instructions

* **Main Files:** Sales Overflow Solved

##### [Better Stealing](https://www.nexusmods.com/skyrimspecialedition/mods/32295?tab=files)

#### Download Instructions

- **Main Files:** BetterStealing v2

#### Additional Instructions

- Double-click **Better Stealing** in your mod order.
- In the **Text Files** tab, select the **BetterStealing.config.txt**.
- Scroll down to **Max Price** and set the value to **100**.
- Press **CTRL+S** to save and close the window.

![Better Stealing Tweak](/Pictures/tpf/mod-installation/better-stealing-tweak.png)

##### [Essential Favorites](https://www.nexusmods.com/skyrimspecialedition/mods/42997?tab=files)

#### Download Instructions

- **Main Files:** Essential Favorites

#### Additional Instructions

Same thing as with Enhanced Reanimation - we don't want a dozen INI files in our Overwrite to sort into the correct mod folders. Additionally, there is a small tweak to make in the INI file for Essential Favorites: No Disarm was set to false as otherwise Disarm shouts used against the player would be pointless.

- Right-click **Essential Favorites** in your mod order and select **Open in Explorer**.
- Navigate to `SKSE\Plugins\`. Right-click and select **New > Text Document**.
- Rename it from **New Text Document.txt** to **po3_EssentialFavorites.ini**.
- Open your new INI file and paste the following inside:

```
[Settings]

;Prevents favorited items from being sold
No Bartering = true

;Prevents favorited weapons from being disarmed
No Disarm = false

;Prevents favorited ingredients from showing up in Alchemy menu
No Alchemy = true

;Prevents favorited items from showing up in Crafting menu
No Crafting = true

;Prevents favorited items from being disenchanted
No Disenchanting = true

;Prevents favorited items from being dropped
No Drop Item = false

;Prevents favorited items from being gifted
No Gifting = false
```

- Save your changes and close the file.

##### [Remember Lockpick Angle - Updated](https://www.nexusmods.com/skyrimspecialedition/mods/26838?tab=files)

#### Download Instructions

- **Main Files:** Remember Lockpick Angle - Updated

##### [I'm Walkin' Here](https://www.nexusmods.com/skyrimspecialedition/mods/27742?tab=files)

#### Download Instructions

- **Main Files:** I'm Walkin' Here

##### [Vampires Cast No Shadows](https://www.nexusmods.com/skyrimspecialedition/mods/46107?tab=files)

#### Download Instructions

* **Main Files:** Vampires Cast No Shadows

##### [Uninterrupted Invisibility](https://www.nexusmods.com/skyrimspecialedition/mods/21729?tab=files)

#### Download Instructions

- **Main Files:** Uninterrupted Invisibility v2

##### [Uninterrupted Ethereal Form](https://www.nexusmods.com/skyrimspecialedition/mods/21765?tab=files)

#### Download Instructions

- **Main Files:** Uninterrupted Ethereal Form v2

##### [Stay At The System Page - Updated](https://www.nexusmods.com/skyrimspecialedition/mods/19832?tab=files)

#### Download Instructions

- **Main Files:** Stay At System Page

##### [Time Format Changer](https://www.nexusmods.com/skyrimspecialedition/mods/28921?tab=files)

#### Download Instructions

- **Main Files:** Time Format Changer - FOMOD Installer

I am making an exception for this mod in that it is **optional** and you may skip it. As a European, I prefer having a 24h clock (AM/PM confusing me a great deal), but this will not be the case for everyone. If you prefer the default 12h clock, feel free to skip this mod or make your own choice in the FOMOD installer.

#### FOMOD Instructions

- **Choose a preset:** Vanilla 24h

##### [Yes I’m Sure](https://www.nexusmods.com/skyrimspecialedition/mods/24898?tab=files)

#### Download Instructions

* **Main Files:** YesImSure

##### [Whose Quest Is It Anyway](https://www.nexusmods.com/skyrimspecialedition/mods/23581?tab=files)

#### Download Instructions

- **Main Files:** WhoseQuestIsItAnyway

##### [Forget Spell](https://www.nexusmods.com/skyrimspecialedition/mods/51125?tab=files)

#### Download Instructions

Download **Forget Spell 1.2.2** from the Old Files section.

- **Old Files:** Forget Spell

#### FOMOD Instructions

- **Choose Game:** Skyrim Special Edition
- **Interface:** SkyUI

---

#### Continue with the [Fixes & Tweaks](/tpf/mod-installation-1/step-4/) page.