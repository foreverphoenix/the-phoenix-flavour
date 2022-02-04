---
title: "Step 3: Assorted Plugins"
weight: 3
type: docs
description: >
  Various SKSE and NET Script Framework plugins.
---

##### [SSE Gameplay Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/41953?tab=files)

#### Download Instructions

- **Main Files:** GameplayTweaks v6

#### Configuration Instructions

- Double-click **SSE Gameplay Tweaks** in your mod order.
- Switch to the **Text Files** tab and select the **GamePlayTweaks.config.txt** file.
- In **Line 29**, set `BlockPotionUse.Enabled =` to `True`.
- In **Line 32**, set `BlockPotionUse.BlockPotionInCombat =` to `False`.
- In **Line 38**, set `BlockPotionUse.BlockPoisonInCombat =` to `False`.
- In **Line 126**, set `DisableAutoFullHeal.Enabled =` to `True`.
- In **Line 128**, set `DisableAutoFullHeal.DisableOnRest =` to `0`.
- In **Line 148**, set `ImpurePotionCostMultiplier.Enabled =` to `True`.
- In **Line 149**, set `ImpurePotionCostMultiplier.CostMultiplier =` to `0.4`.
- In **Line 158**, set `PlayerCreatedPotionCostChange.Enabled =` to `True`.
- In **Line 159**, set `PlayerCreatedPotionCostChange.CostMultiplier =` to `0.8`.
- In **Line 367**, set `TeammateDetection.Enabled =` to `True`.
- In **Line 410**, set `TrainingGoldDisappearsFromNPC.Enabled =` to `True`.

> The first set of changes will disallow consuming food or drink during combat. The second will disable Health/Stamina/Magicka being restored on selecting attributes after a level-up. The third will reduce the value of player-created potions, especially impure ones. Finally, your followers will no longer be detectable by enemies when the player is undetected and gold spent at skill trainers will no longer be added to the trainer's inventory (thus disallowing the player from simply taking it back if the trainer is also a follower).

##### [Scrambled Bugs](https://www.nexusmods.com/skyrimspecialedition/mods/43532?tab=files)

#### Download Instructions

- **Main Files:** Scrambled Bugs
- **Main Files:** Scrambled Eggchantments
- **Optional Files:** Underfilled Soul Gems - Soul Gem Too Small

#### Configuration Instructions - Scrambled Bugs

- Double-click **Scrambled Bugs** in your mod order.
- Switch to the **Text Files** tab and select the **ScrambledBugs.json** file.
- In **Line 11**, set `"magicEffectConditions":` to `false`.
- In **Line 30**, set `"equipBestAmmo:"` to `true`.
- In **Line 34**, set `"powerAttackStamina` to `true`.
- In **Line 37**, set `"underfilledSoulGems":` to `true`.
- Hit **CTRL+S** to save and close the window.

#### Configuration Instructions - Scrambled Eggchantments

- Double-click **Scrambled Eggchantments** in your mod order.
- Switch to the **Text Files** tab and select the **ScrambledEggchantments.json** file.
- In **Line 8**, set `"enchantmentValue":` to `true`.
- Hit **CTRL+S** to save and close the window.

##### [powerofthree's Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/51073?tab=files)

#### Download Instructions

- **Main Files:** powerofthree's Tweaks
- **Optional Files:** INI file

> We are installing the INI file separately so it does not get overwritten when the main file is updated.

#### Configuration Instructions

- Double-click **powerofthree's Tweaks** in your mod order.
- Switch to the **INI Files** tab and select the **po3_Tweaks.ini**.
- In **Line 49**, change `Faction Stealing =` to `true`.
- In **Line 69**, change `No Attack Messages =` to `3`.
- In **Line 83**, change `Grabbing Is Stealing =` to `true`.
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

- **Main File:** Simple Offence Suppression SE

##### [Classic Paralysis](https://www.nexusmods.com/skyrimspecialedition/mods/45931?tab=files)

#### Download Instructions

- **Main Files:** Classic Paralysis

##### [Enhanced Reanimation](https://www.nexusmods.com/skyrimspecialedition/mods/43500?tab=files)

#### Download Instructions

- **Main Files:** Enhanced Reanimation SE

#### Configuration Instructions

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

#### Configuration Instructions

- Double-click **Better Stealing** in your mod order.
- In the **Text Files** tab, select the **BetterStealing.config.txt**.
- Scroll down to **Max Price** and set the value to **100**.
- Press **CTRL+S** to save and close the window.

![Better Stealing Tweak](/Pictures/tpf/mod-installation/better-stealing-tweak.png)

##### [Essential Favorites](https://www.nexusmods.com/skyrimspecialedition/mods/42997?tab=files)

#### Download Instructions

- **Main Files:** Essential Favorites

#### Configuration Instructions

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

* **Main Files:** Vampires Cast No Shadows SE

##### [Uninterrupted Invisibility](https://www.nexusmods.com/skyrimspecialedition/mods/21729?tab=files)

#### Download Instructions

- **Main Files:** Uninterrupted Invisibility v2

##### [Uninterrupted Ethereal Form](https://www.nexusmods.com/skyrimspecialedition/mods/21765?tab=files)

#### Download Instructions

- **Main Files:** Uninterrupted Ethereal Form v2

##### [Pause After Unload Unscripted](https://www.nexusmods.com/skyrimspecialedition/mods/60958?tab=files)

#### Download Instructions

- **Main Files:** Pause After Unload Unscripted SE-1.0.0.9.rar

##### [Stay At The System Page - Updated](https://www.nexusmods.com/skyrimspecialedition/mods/19832?tab=files)

#### Download Instructions

- **Main Files:** Stay At System Page

##### [Time Format Changer](https://www.nexusmods.com/skyrimspecialedition/mods/28921?tab=files)

#### Download Instructions

- **Main Files:** Time Format Changer (Legacy SE)

I am making an exception for this mod in that it is **optional** and you may skip it. As a European, I prefer having a 24h clock (AM/PM confusing me a great deal), but this will not be the case for everyone. If you prefer the default 12h clock, feel free to skip this mod or make your own choice in the FOMOD installer.

#### FOMOD Instructions

- **Choose a preset:** Vanilla 24h

##### [Yes I’m Sure](https://www.nexusmods.com/skyrimspecialedition/mods/24898?tab=files)

#### Download Instructions

Download **YesImSure 1.5.0** from the Old Files section.

* **Old Files:** YesImSure

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

##### [Classic Sprinting Redone](https://www.nexusmods.com/skyrimspecialedition/mods/20166?tab=files)

#### Download Instructions

- **Main Files:** Classic Sprinting Redone (Legacy SE)

##### [Better Jumping](https://www.nexusmods.com/skyrimspecialedition/mods/18967?tab=files)

#### Download Instructions

Download **Better Jumping SE 1.7.1** from the Old Files section.

- **Old Files:** Better Jumping SE

---

#### Continue with the [Fixes & Tweaks](/tpf/mod-installation-1/step-4/) page.