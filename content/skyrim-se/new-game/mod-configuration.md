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

![Initialisation complete](/Pictures/skyrim-se/new-game/initialisation-complete.jpg)

## A Matter of Time

- You can either:
  - Configure the clock widget to your liking.
  - Untick **Show** for each module in the **General** tab to hide it until you are ready to customise it.
  - If you installed my personal AMOT preset, go to **Presets** and click **Load user settings** (see screenshot).

![Load AMOT Preset](/Pictures/skyrim-se/new-game/load-amot-preset.jpg)

## All Geared Up Derivative

- In the **NPC** tab, check **Enable Weapons**.

![AllGUD MCM](/Pictures/skyrim-se/new-game/allgud-mcm.jpg)

## Cathedral Weathers

- Uncheck **Configuration Spell** (redundant when you can access the MCM).

![Cathedral Weathers MCM](/Pictures/skyrim-se/new-game/cw-mcm.jpg)

## Diverse Dragons Collection

- Open the MCM once, then exit it.

> By doing so, the mod will recognise that you have SKSE and SkyUI installed and automatically removes its configuration tool from your Powers menu.

## Follower Framework

### NPC Behaviour (optional)

* Turn on the following options under **Activity** >> **Sandboxing**:
  * Ignore Special Furniture
  * Stop During Player Dialogue
  * Only Sandbox In Town

> My preferences. Optional.

### Horse Whistle (optional)

NFF features a bindable horse whistle hotkey which you can press to call the last ridden mount to your location.

* Under **Activity** >> **Player Horse**, bind a **Call Player Horse Hotkey**.

### Regard System (optional)

*  Disable the Regard system under **Gameplay** >> **Regard**:
  * Allow Regard: Off

> This is completely optional. The feature works perfectly fine, I just don't like it personally.

### Additional Powers (optional)

* Disable the **Command Followers** ability under **System** >> **Casted Abilities** to further de-clutter your Powers menu.
* You can define a hotkey for it above.

### ConsoleUtil Support

* Under **System** >> **Core**, check the **Enable ConsoleUtil** option.

## Genuinely Intelligent Soul Traps

This mod - while focusing on bug fixes and soul gem multithreading - comes with some very nifty level requirement options. If you like, you can set level requirements for each of its special features as well as the for capturing of each tier of souls. Toggle and adjust this system in the **Leveling** tab.

## Growl - Werebeasts of Skyrim

* Toggle on **Invulnerable During Transformation**.

## Immersive HUD

### Toggle Settings (optional)

- You can change the hotkey to display the HUD here.
- I recommend turning on the **Key Press Toggles** option but that is a personal preference.

### Link Widgets (optional)

- Check **Link ALL SkyUI Widgets**.

> If you installed A Matter of Time, this will link the clock widget to the HUD so that it gets toggled alongside the other components (such as the compass). 

![iHUD link widgets](/Pictures/skyrim-se/new-game/ihud-link-widgets.jpg)

## moreHUD

- In the **Enemy's Level** tab, uncheck the following options:
  - Show Magicka Meter
  - Show Stamina Meter

> These only clutter up the interface in my opinion. You can also disable Health numbers if you like.

![moreHUD MCM](/Pictures/skyrim-se/new-game/morehud-mcm.jpg)

## Realistic Water Two

* Under **Mod Options** >> **Blacksmith Forge Water**, toggle the following options:
  * Kynesgrove
  * Rorikstead

![Realistic Water 2 MCM](/Pictures/skyrim-se/new-game/rwt-mcm.jpg)

## Storm Lightning

By default, the lightning storms with this mod are pretty intense. I'd suggest changing to a different preset (above "default") to tone them down a little.

- Under **Presets**, select any one on one of the options.

![Storm Lightning MCM](/Pictures/skyrim-se/new-game/storm-lightning-mcm.jpg)

## Timing Is Everything

Another large MCM, and one you should configure now, at the start of the game as it affects many quests that start very early on in Vanilla. I’ve personally increased the Dawnguard level requirements to 30+ and set Dragonborn to start only after Alduin’s defeat but this is all down to your preferences and plans for this playthrough.

Thanks to the FISSES support, it is also possible to load, save and share custom presets through the MCM (**Extra Options** tab).

## Trade & Barter

- Under **Barter Rates** >> **Settings**, check the **Modify Barter Settings** box.

![Trade and Barter MCM](/Pictures/skyrim-se/new-game/trade-barter-mcm.jpg)

## Wonders of Weather

* Under **Rainsplashes**, set **Level** to **Disabled** to turn the effect off.

> This is done to prevent CTDs.

![Wonders of Weather MCM](/Pictures/skyrim-se/new-game/wow-mcm.jpg)

## Starting the game

Once you’re done configuring everything, save the game manually. Then talk to the Statue of Mara, select one of the options and interact with the bed in the corner to truly start your playthrough.

As for the options, going with the `vanilla start` is entirely possible but you can also choose the `I am camping in the woods` option for a faster alternative that drops you in the same region but skips the cart ride and execution sequence. It is NOT recommended that you choose the `vampire lair` option as that has been known to cause issues with vampire mods.

> For the best experience **I recommend the vanilla start** as it is impossible to balance all the various options that AS LAL offers.

**Good luck and have fun!**

![Select game start](/Pictures/skyrim-se/new-game/select-game-start.jpg)