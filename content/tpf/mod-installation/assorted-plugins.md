---
title: "Assorted Plugins"
weight: 37
type: docs
description: >
  Various Script Extender or NET Script Framework based plugins.
---

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

##### [Whose Quest Is It Anyway](https://www.nexusmods.com/skyrimspecialedition/mods/23581?tab=files)

#### Download Instructions

* **Main Files:** WhoseQuestIsItAnyway

##### [Yes I’m Sure](https://www.nexusmods.com/skyrimspecialedition/mods/24898?tab=files)

#### Download Instructions

* **Main Files:** YesImSure

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

* **Main Files:** Remember Lockpick Angle - Updated

##### [Classic Sprinting Redone](https://www.nexusmods.com/skyrimspecialedition/mods/20166?tab=files)

#### Download Instructions

* **Main Files:** Classic Sprinting Redone

##### [Better Jumping](https://www.nexusmods.com/skyrimspecialedition/mods/18967?tab=files)

#### Download Instructions

* **Main Files:** Better Jumping SE

##### [I'm Walkin' Here](https://www.nexusmods.com/skyrimspecialedition/mods/27742?tab=files)

#### Download Instructions

* **Main Files:** I'm Walkin' Here

##### [Disable Follower Collision](https://www.nexusmods.com/skyrimspecialedition/mods/35925?tab=files)

#### Download Instructions

- **Main Files:** DisableFollowerCollision v1.0.0 for SkyrimSE

##### [Free Look](https://www.nexusmods.com/skyrimspecialedition/mods/42620?tab=files)

#### Download Instructions

* **Main Files:** Free Look v3

##### [Vampires Cast No Shadows](https://www.nexusmods.com/skyrimspecialedition/mods/46107?tab=files)

#### Download Instructions

* **Main Files:** Vampires Cast No Shadows

##### [Uninterrupted Invisibility](https://www.nexusmods.com/skyrimspecialedition/mods/21729?tab=files)

#### Download Instructions

- **Main Files:** Uninterrupted Invisibility v2

##### [Uninterrupted Ethereal Form](https://www.nexusmods.com/skyrimspecialedition/mods/21765?tab=files)

#### Download Instructions

- **Main Files:** Uninterrupted Ethereal Form v2