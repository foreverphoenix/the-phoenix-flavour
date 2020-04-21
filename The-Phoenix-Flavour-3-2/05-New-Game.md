![logo](../Media/tpf_logo.png)

**TABLE OF CONTENTS**
- [01. Final Adjustments](#01-final-adjustments)
  - [1.1 Timing](#11-timing)
  - [1.2 MO2 Notifications](#12-mo2-notifications)
  - [1.3 New Profile](#13-new-profile)
  - [1.4 Optional Mods](#14-optional-mods)
  - [1.5 ENB Shader Cache](#15-enb-shader-cache)
  - [1.6 New Game](#16-new-game)
- [02. Mod Configuration](#02-mod-configuration)
  - [2.1 Initialisation](#21-initialisation)
  - [2.2 Wildcat - Configuration Power](#22-wildcat---configuration-power)
  - [2.3 Mod Configuration Menus](#23-mod-configuration-menus)
  - [2.4 A Matter of Time MCM](#24-a-matter-of-time-mcm)
  - [2.5 All Geared Up Derivative MCM](#25-all-geared-up-derivative-mcm)
  - [2.6 Complete Crafting Overhaul Remastered MCM](#26-complete-crafting-overhaul-remastered-mcm)
  - [2.7 Diverse Dragons Collection MCM](#27-diverse-dragons-collection-mcm)
  - [2.8 Nether's Follower Framework MCM](#28-nethers-follower-framework-mcm)
  - [2.9 Genuinely Intelligent Soul Traps MCM](#29-genuinely-intelligent-soul-traps-mcm)
  - [2.10 Growl - Werebeasts of Skyrim MCM](#210-growl---werebeasts-of-skyrim-mcm)
  - [2.11 Immersive HUD MCM](#211-immersive-hud-mcm)
  - [2.12 moreHUD MCM](#212-morehud-mcm)
  - [2.13 Obsidian Weathers MCM](#213-obsidian-weathers-mcm)
  - [2.14 Realistic Water Two MCM](#214-realistic-water-two-mcm)
  - [2.15 Relationship Dialogue Overhaul MCM](#215-relationship-dialogue-overhaul-mcm)
  - [2.16 Timing Is Everything MCM](#216-timing-is-everything-mcm)
  - [2.17 VioLens MCM](#217-violens-mcm)
  - [2.18 Wildcat - Combat in Skyrim MCM](#218-wildcat---combat-in-skyrim-mcm)
  - [2.19 Wonders of Weather MCM](#219-wonders-of-weather-mcm)
  - [2.20 Starting the game](#220-starting-the-game)

![separator](../Media/separator.png)

# 01. Final Adjustments

## 1.1 Timing

Before starting a new playthrough, there are some considerations.

Has there been a Skyrim update recently? If so, SKSE64, the mods depending on it as well as the guide may receive an update very soon, and it may be worth it to wait a week or two for everything to catch up before diving into the game.

> Also keep an eye on my blog or our Discord server in case a major update for the guide or a mod is imminent.

## 1.2 MO2 Notifications

Before jumping into the game, go through one final checkup. In Mod Organizer 2, go to **View > Notifications**. If this is greyed out, you are good to go! If not there are multiple different warnings you might encounter:

- **Missing Masters:** One of your plugins is missing a master file. It is marked with an exclamation mark in your load order. This is most likely due to skipping a mod that was not optional or selecting the wrong option in a FOMOD  installer. Go back to the mod’s instructions in the guide and double-check everything.

- **Form 43 Plugin:** You forgot to re-save one or several plugins in the Creation Kit. Re-save them now.

- **Outdated SKSE Plugin:** Check the plugin's mod page to see if there is a new version.

- **Files in your overwrite:** This one is not particularly problematic and you can probably ignore it for the time being.

## 1.3 New Profile

- In Mod Organizer 2, open the **Profiles** window (Tools > Profiles or CTRL + P).
- Select your **The Phoenix Flavour** or **The Phoenix Flavour - Customised** profile and click **Copy**.
- Enter a name for the new profile. Here are some suggestions:
  - `The Phoenix Flavour - {name of the character for the playthrough}`
  - `The Phoenix Flavour - {name of the build or playstyle for the playthrough}`
  - `The Phoenix Flavour - Playthrough 1`
- Click **OK** and select your new profile in the list. Make sure both options at the bottom are checked:
  - Use profile-specific Save Games
  - Use profile-specific Game INI Files
- Close the **Profiles** window.
- Switch to your new profile in Mod Organizer 2.

## 1.4 Optional Mods

In your new profile, go through your mod order again - this is your last opportunity to disable some optional mods that you'd rather not use for your upcoming playthrough. Keep in mind that some optional mods have dependencies (like patches or replacer plugins) that would need to be disabled also. Others will be masters for DynDOLOD.esp and you would have to regenerate DynDOLOD if you were to disable them.

## 1.5 ENB Shader Cache

If you installed ENBSeries, you should be decently sure that your current preset is the one you want to use in your playthrough. Of course you can still switch anytime but if you are planning on sticking with the preset for a while at least, I'd recommend turning on Shader Cache in the enblocal.ini. This will speed up the game launch process as ENB won't have to reload its shaders every time.

- Open **ENBMan**.
- Double-click the **Skyrim SE** profile.
- Disable your current preset (click the checkmark to save if you changed anything).
- Click the gears icon in the **Global Settings** section.
- Double-click **enblocal.ini**.
- Scroll down to the performance area and double-click **ShaderCache**.
- Change the value to **True** and click the green checkmark to confirm.
- Close the window and click **Yes** to save your change.
- Close out of the **Global Configuration Files** window and reactivate your preset.

## 1.6 New Game

- Run **SKSE** through Mod Organizer 2.
- Select **NEW** in the Skyrim main menu to start your playthrough.

![separator](../Media/separator.png)

# 02. Mod Configuration

## 2.1 Initialisation

After starting a new game, you will be dropped in the **Alternate Start – Live Another Life** cell where you can customise your character, then configure your mods before you actually start playing.

Stand still and wait until all messages have run through in the upper left corner (check the screenshot below). Then hit **ESCAPE** and create a manual save before you continue.

![Initialisation complete](Pictures/new_game/Initialisation_complete.jpg)

## 2.2 Wildcat - Configuration Power

While  Wildcat (the main combat overhaul) does come with a fantastic MCM, it also adds a (for SkyUI users) completely redundant lesser power for configuration purposes to your character. In order to remove it, you need to click your way through all its options until the very last one (simply select all the default options) and finally you can opt to remove the power from the menu. Customise the mod later on through the MCM.

![Wildcat Config Power](Pictures/new_game/wildcat_config_power.jpg)

## 2.3 Mod Configuration Menus

Thanks to SkyUI, it is possible to configure most mods directly through their Mod Configuration Menu – or MCM for short – which you can access through the main menu. Hit **ESCAPE** and select **MCM**. See recommended changes for most of the guide’s MCMs below.

## 2.4 A Matter of Time MCM

- You can either:
  - Configure the clock widget to your liking.
  - Untick **Show** for each module in the **General** tab to hide it until you are ready to customise it.
  - If you installed my personal AMOT preset, go to **Presets** and click **Load user settings** (see screenshot).

![Load AMOT Preset](Pictures/new_game/load_amot_preset.jpg)

## 2.5 All Geared Up Derivative MCM

- In the **NPC** tab, check **Enable Weapons**.

![AllGUD MCM](Pictures/new_game/allgud_mcm.jpg)

## 2.6 Complete Crafting Overhaul Remastered MCM

### 2.6.1 Menu Filters (optional)

* Under **Recipe Display** > **Crafting Menu Filters**, disable:
  * Crafting Categories
  * Item Type Filters

> While I think CCOR’s crafting menu filters are a great idea, I very much dislike their implementation and prefer to disable them entirely.

### 2.6.2 Equipment Breakdown (optional)

* Under **Crafting Options** > **Breakdown Equipment**, disable:
  * At Smelter
  * At Tanning Rack

> Equipment breakdown can throw off balancing since you get more crafting resources that way. I personally don’t like the feature at all.

### 2.6.3 Upgrading Leveled Items

* Under **Miscellaneous** > **Leveled Items**, disable:
  * Upgrade via Crafting

## 2.7 Diverse Dragons Collection MCM

By simply opening the MCM once, the mod will recognise that you have SKSE and SkyUI installed, and automatically removes its configuration tool from your Powers menu.

## 2.8 Nether's Follower Framework MCM

### 2.8.1 NPC Behaviour

* Turn on the following options under **Activity** > **Sandboxing**:
  * Ignore Special Furniture
  * Stop During Player Dialogue
  * Only Sandbox In Town

### 2.8.2 Regard System (optional)

*  Disable the Regard system under **Gameplay** > **Regard**:
  * Allow Regard: Off

> This is completely optional. The feature works perfectly fine, I just don't like it personally.

### 2.8.3 Additional Powers (optional)

* You can disable the **Command Followers** ability under **System** > **Casted Abilities** to further de-clutter your Powers menu.

### 2.8.4 ConsoleUtil Support

* Under **System** > **Core**, check the **Enable ConsoleUtil** option.

## 2.9 Genuinely Intelligent Soul Traps MCM

This mod - while focusing on bug fixes and soul gem multithreading - comes with some very nifty level requirement options. If you like, you can set level requirements for each of its special features as well as the for capturing of each tier of souls. Toggle and adjust this system in the **Leveling** tab.

## 2.10 Growl - Werebeasts of Skyrim MCM

* Toggle on **Invulnerable During Transformation**.

## 2.11 Immersive HUD MCM

### 2.11.1 Toggle Settings (optional)

- You can change the hotkey to display the HUD here.
- I recommend turning on the **Key Press Toggles** option but that is a personal preference.

### 2.11.2 Link Widgets (optional)

- Check **Link ALL SkyUI Widgets**.

> If you installed A Matter of Time, this will link the clock widget to the HUD so that it gets toggled alongside the other components (such as the compass). 

![iHUD link widgets](Pictures/new_game/ihud_link_widgets.jpg)

## 2.12 moreHUD MCM

- In the **Enemy's Level** tab, uncheck the following options:
  - Show Magicky Meter
  - Show Stamina Meter

> These only clutter up the interface in my opinion. You can also disable Health numbers if you like.

![moreHUD MCM](Pictures/new_game/morehud_mcm.jpg)

## 2.13 Obsidian Weathers MCM

* Click **Remove Spell** to get rid of the spell that was added for non-SkyUI users. All options can be configured through the MCM.
* Click **Enable Season FX** if you would like to have seasonal weathers (more snow in winter etc).

![Obsidian Weathers MCM](Pictures/new_game/obsidian_weathers_mcm.jpg)

## 2.14 Realistic Water Two MCM

* Under **Mod Options** > **Blacksmith Forge Water**, toggle the following options:
  * The Fall of Granite Hill `if you installed that mod during the Customisation section`
  * Kynesgrove
  * Rorikstead

![Realistic Water 2 MCM](Pictures/new_game/rwt_mcm.jpg)

## 2.15 Relationship Dialogue Overhaul MCM

* Under **Other Options** > **Toggle NPCs**, disable:
  * Allow RDO Added Followers
  * Allow Terek

![Relationship Dialogue Overhaul MCM](Pictures/new_game/rdo_mcm.jpg)

## 2.16 Timing Is Everything MCM

Another large MCM, and one you should configure now, at the start of the game as it affects many quests that start very early on in Vanilla. I’ve personally increased the Dawnguard level requirements to 30+ and set Dragonborn to start only after Alduin’s defeat but this is all down to your preferences and plans for this playthrough.

Thanks to the FISSES support, it is also possible to load, save and share custom presets through the MCM (**Extra Options** tab).

## 2.17 VioLens MCM

* Under **Melee**, enable **Player Killmove Immunity**.
  * Killcams against the player character often trigger and kill you even if you could have survived the hit HP-wise.
* If you like, you can also disable Killmoves entirely (Melee and/or Ranged).

## 2.18 Wildcat - Combat in Skyrim MCM

* Personal recommendation: Disable **Injuries**.

## 2.19 Wonders of Weather MCM

* Under **Rainsplashes**, set **Level** to **None** to disable the effect (I personally think it looks odd most of the time). This is optional.

## 2.20 Starting the game

Once you’re done configuring everything, save the game manually. Then talk to the Statue of Mara, select one of the options and interact with the bed in the corner to truly start your playthrough.

As for the options, going with the `vanilla start` is entirely possible but you can also choose the `I am camping in the woods` option for a faster alternative that drops you in the same region but skips the cart ride and execution sequence. It is NOT recommended that you choose the `vampire lair` option as that has been known to cause issues with Sacrosanct.

**Good luck and have fun!**

![Select game start](Pictures/new_game/select_game_start.jpg)