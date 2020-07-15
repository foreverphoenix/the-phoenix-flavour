---
title: "Gameplay Overhauls"
weight: 24
type: docs
description: >
  Larger mods affecting gameplay.
---

##### [Mysticism - A Magic Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/27839?tab=files)

#### Download Instructions

* **Main Files:** Mysticism - A Magic Overhaul

##### [Adamant - A Perk Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/30191/?tab=files)

#### Download Instructions

* **Main Files:** Adamant - A Perk Overhaul

##### [Complete Crafting Overhaul Remastered (CCOR)](https://www.nexusmods.com/skyrimspecialedition/mods/28608?tab=files)

#### Download Instructions

* **Main Files:** Complete Crafting Overhaul Remastered

##### [Complete Crafting Overhaul Remastered - JS Circlet Replacer Patch](https://www.nexusmods.com/skyrimspecialedition/mods/19518?tab=files) (conditional)

{{% alert title="Mod Dependency" color="warning" %}}
Only install this mod if you installed **JS Circlet Replacer**. Otherwise skip it.{{% /alert %}}

#### Download Instructions

* **Miscellaneous Files:**
  * JS Circlet Replacer_CCOR

##### [Morningstar - Minimalistic Races of Skyrim](https://www.nexusmods.com/skyrimspecialedition/mods/22298?tab=files) (optional)

#### Download Instructions

* **Main Files:** Morningstar 1.4.0

#### Additional Instructions

* Double-click **Morningstar - Minimalistic Races of Skyrim** in your mod order.
* Switch to the **Filetree** tab and rename the plugin to:
  * Morningstar - Minimalistic Races of Skyrim.**esp**

> This will turn the ESL into an ESP-Lite plugin, allowing us to manipulate its load order.

##### [Subtle But Classless](https://www.nexusmods.com/skyrimspecialedition/mods/2744?tab=files) (optional)

#### Download Instructions

* **Main Files:** Subtle but Classless

##### [Subtle But Classless - USSEP and EEO Patch](https://www.nexusmods.com/skyrimspecialedition/mods/26092?tab=files) (conditional)

{{% alert title="Mod Dependency" color="warning" %}}
Only install this mod if you installed **Subtle But Classless**. Otherwise skip it.
{{% /alert %}}

#### Download Instructions

* **Main Files:** Subtle but Classless - USSEP and EEO Patch

##### [Growl - Werebeasts of Skyrim](https://www.nexusmods.com/skyrimspecialedition/mods/31245?tab=files)

#### Download Instructions

* **Main Files:** Growl 1.4.0

##### [Sacrosanct - Vampires of Skyrim](https://www.nexusmods.com/skyrimspecialedition/mods/3928?tab=files)

#### Download Instructions

* **Main Files:** Sacrosanct v515

##### [Carriage and Ferry Travel Overhaul (CFTO)](https://www.nexusmods.com/skyrimspecialedition/mods/8379?tab=files)

#### Download Instructions

* **Main Files:** Carriage and Ferry Travel Overhaul
* **Optional Files:** CFTO - Dawnstar by Arthmoor Patch

##### [CFTO - Winterhold Carriage](https://www.nexusmods.com/skyrimspecialedition/mods/27236?tab=files)

#### Download Instructions

* **Main Files:** CFTO - Winterhold Carriage

##### [Night Eye Overhaul (NEO)](https://www.nexusmods.com/skyrimspecialedition/mods/9177?tab=files)

#### Download Instructions

* **Main Files:** Night Eye Overhaul

#### FOMOD Instructions

* Change nothing, click **Install**.

#### Additional Instructions

* Delete the following file(s) and/or folder(s):
  * `Night Eye Overhaul.esm`
  * `Night Eye Overhaul.esp`

##### [Night Eye Overhaul - Plugin Replacer](https://www.nexusmods.com/skyrimspecialedition/mods/23794?tab=files)

#### Download Instructions

* **Main Files:** Night Eye Overhaul - Plugin Replacer - Sacrosanct Version

##### [Trua - Minimalistic Faiths of Skyrim](https://www.nexusmods.com/skyrimspecialedition/mods/32549?tab=files) (optional)

#### Download Instructions

* **Main Files:** Trua 1.0.1

##### [Irondusk's Saddlebags](https://www.nexusmods.com/skyrim/mods/91395?tab=files) (optional)

#### Download Instructions

- **Main Files:** Saddlebags 5-17-18

#### Porting Instructions

- Resave the plugin in the Creation Kit.

#### Additional Instructions

Saddlebags comes not only with a horse storage feature but also a Lesser Power called Horse Whistle which calls your horse to your location. Nether's Follower Framework already contains the same feature, but you can set it to a specific hotkey in the NFF MCM, making it a good deal more convenient than using yet another power.

It's optional but I highly recommend disabling Saddlebag's horse call power by following these steps:

- Run **SSEEdit** through Mod Organizer 2.
- Click **OK** in the plugin selection window to load all plugins.
- Wait for SSEEdit to return `Background Loader: finished`.
- Scroll down in the left pane to **Saddlebags.esp** and double-click it.
- Double-click the **Quest** category and select the `SaddlebagsQuest` record.
- Under **Aliases** >> **Alias Spells**, delete the following (see screenshot below):
  - `HorseWhistleSpell "Horse Whistle" [SPEL:9D001D92]`
- Close SSEEdit and click **OK** to save your changes.

> This will prevent the power from being given to the player, effectively disabling it.

![Saddlebags Disable Whistle](/Pictures/mod_installation/saddlebags_disable_whistle.png)