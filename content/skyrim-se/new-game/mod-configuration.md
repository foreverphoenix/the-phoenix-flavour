---
title: "Mod Configuration"
weight: 2
type: docs
description: >
  Ingame mod configuration instructions.
---

## Initialisation

After starting a new game, you will be dropped in the **Alternate Start - Live Another Life** cell where you can customise your character, then configure your mods before you actually start playing.

Stand still and wait until all messages have run through in the upper left corner (check the screenshot below). Then hit **ESCAPE** and create a manual save before you continue.

Thanks to SkyUI, it is possible to configure most mods directly through their Mod Configuration Menu – or MCM for short – which you can access through the main menu. Hit **ESCAPE** and select **MCM**. See recommended changes for most of the guide’s MCMs below.

![Initialisation complete](/Pictures/new_game/Initialisation_complete.jpg)

## A Matter of Time

- You can either:
  - Configure the clock widget to your liking.
  - Untick **Show** for each module in the **General** tab to hide it until you are ready to customise it.
  - If you installed my personal AMOT preset, go to **Presets** and click **Load user settings** (see screenshot).

![Load AMOT Preset](/Pictures/new_game/load_amot_preset.jpg)

## All Geared Up Derivative

- In the **NPC** tab, check **Enable Weapons**.

![AllGUD MCM](/Pictures/new_game/allgud_mcm.jpg)

## Cathedral Weathers

- Uncheck **Configuration Spell** (redundant when you can access the MCM).

![Cathedral Weathers MCM](/Pictures/new_game/cw-mcm.jpg)

## Complete Crafting (CCOR)

#### Menu Filters (optional)

* Under **Recipe Display** >> **Crafting Menu Filters**, disable:
  * Crafting Categories
  * Item Type Filters

> While I think CCOR’s crafting menu filters are a great idea, I very much dislike their implementation and prefer to disable them entirely.

### More Jewelry

* Under **Crafting Options** >> **Additional Items**, disable:
  * More Jewelry

The added circlets would use vanilla models and textures, inconsistent with the vanilla cirlcets changed by JS Circlet Replacer.

### Equipment Breakdown (optional)

* Under **Crafting Options** >> **Breakdown Equipment**, disable:
  * At Smelter
  * At Tanning Rack

> Equipment breakdown can throw off balancing since you get more crafting resources that way. I personally don’t like the feature at all.

### Upgrading Leveled Items

* Under **Miscellaneous** >> **Leveled Items**, disable:
  * Upgrade via Crafting

![CCOR MCM](/Pictures/new_game/ccor_crafting_optiosn.jpg)

## Diverse Dragons Collection

- Open the MCM once, then exit it.

> By doing so, the mod will recognise that you have SKSE and SkyUI installed and automatically removes its configuration tool from your Powers menu.

## Follower Framework

### NPC Behaviour

* Turn on the following options under **Activity** >> **Sandboxing**:
  * Ignore Special Furniture
  * Stop During Player Dialogue
  * Only Sandbox In Town

> My preferences. Optional.

### Regard System (optional)

*  Disable the Regard system under **Gameplay** >> **Regard**:
  * Allow Regard: Off

> This is completely optional. The feature works perfectly fine, I just don't like it personally.

### Additional Powers (optional)

* Disable the **Command Followers** ability under **System** >> **Casted Abilities** to further de-clutter your Powers menu.
* You can define a hotkey for it above.

### ConsoleUtil Support

* Under **System** >> **Core**, check the **Enable ConsoleUtil** option.

## Genuinely Intelligent Soul Traps MCM

This mod - while focusing on bug fixes and soul gem multithreading - comes with some very nifty level requirement options. If you like, you can set level requirements for each of its special features as well as the for capturing of each tier of souls. Toggle and adjust this system in the **Leveling** tab.

## Growl - Werebeasts of Skyrim MCM

* Toggle on **Invulnerable During Transformation**.

## Immersive HUD

### Toggle Settings (optional)

- You can change the hotkey to display the HUD here.
- I recommend turning on the **Key Press Toggles** option but that is a personal preference.

### Link Widgets (optional)

- Check **Link ALL SkyUI Widgets**.

> If you installed A Matter of Time, this will link the clock widget to the HUD so that it gets toggled alongside the other components (such as the compass). 

![iHUD link widgets](/Pictures/new_game/ihud_link_widgets.jpg)

## moreHUD

- In the **Enemy's Level** tab, uncheck the following options:
  - Show Magicka Meter
  - Show Stamina Meter

> These only clutter up the interface in my opinion. You can also disable Health numbers if you like.

![moreHUD MCM](/Pictures/new_game/morehud_mcm.jpg)

## Relationship Dialogue Overhaul

* Under **Other Options** >> **Toggle NPCs**, disable:
  * Allow RDO Added Followers
  * Allow Terek

![Relationship Dialogue Overhaul MCM](/Pictures/new_game/rdo_mcm.jpg)

## Realistic Water Two

* Under **Mod Options** >> **Blacksmith Forge Water**, toggle the following options:
  * Kynesgrove
  * Rorikstead

![Realistic Water 2 MCM](/Pictures/new_game/rwt_mcm.jpg)

## Timing Is Everything

Another large MCM, and one you should configure now, at the start of the game as it affects many quests that start very early on in Vanilla. I’ve personally increased the Dawnguard level requirements to 30+ and set Dragonborn to start only after Alduin’s defeat but this is all down to your preferences and plans for this playthrough.

Thanks to the FISSES support, it is also possible to load, save and share custom presets through the MCM (**Extra Options** tab).

## Wonders of Weather

* Under **Rainsplashes**, set **Level** to **Disabled** to disable the effect.

> This is done to prevent CTDs.

## Starting the game

Once you’re done configuring everything, save the game manually. Then talk to the Statue of Mara, select one of the options and interact with the bed in the corner to truly start your playthrough.

As for the options, going with the `vanilla start` is entirely possible but you can also choose the `I am camping in the woods` option for a faster alternative that drops you in the same region but skips the cart ride and execution sequence. It is NOT recommended that you choose the `vampire lair` option as that has been known to cause issues with Sacrosanct.

**Good luck and have fun!**

![Select game start](/Pictures/new_game/select_game_start.jpg)