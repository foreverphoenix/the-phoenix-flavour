---
title: "Miscellaneous"
weight: 30
type: docs
description: >
  Various smaller mods with niche features.
---

##### [Irondusk's Saddlebags](https://www.nexusmods.com/skyrim/mods/91395?tab=files)

#### Download Instructions

- **Main Files:** Saddlebags 5-17-18

#### Porting Instructions

- Resave the plugin in the Creation Kit.

#### Additional Instructions

Saddlebags includes not only a horse storage feature but also a Lesser Power called Horse Whistle which calls your last ridden horse to your location. Nether's Follower Framework already contains the same feature, but you can set it to a specific hotkey in the NFF MCM, making it a good deal more convenient than using yet another power.

Disable Saddlebag's horse call power by following these steps:

- Run **SSEEdit** through Mod Organizer 2.
- Click **OK** in the plugin selection window to load all plugins.
- Wait for SSEEdit to return `Background Loader: finished`.
- Scroll down in the left pane to **Saddlebags.esp** and double-click it.
- Double-click the **Quest** category and select the `SaddlebagsQuest` record.
- Under **Aliases** >> **Alias Spells**, delete the following (see screenshot below):
  - `HorseWhistleSpell "Horse Whistle" [SPEL:9D001D92]`
- When the warning window pops up, click **Yes I'm absolutely sure**.
- Close SSEEdit and click **OK** to save your changes.

> This will prevent the power from being given to the player, effectively disabling it.

![Saddlebags Disable Whistle](/Pictures/skyrim-se/mod-installation/saddlebags-disable-whistle.png)

##### [Quick Light](https://www.nexusmods.com/skyrimspecialedition/mods/12633?tab=files)

#### Download Instructions

* **Main Files:** Quick Light SE

##### [Ish's Respec Mod](https://www.nexusmods.com/skyrimspecialedition/mods/1960?tab=files)

#### Download Instructions

- **Main Files:** Ish's Respec Mod

##### [Durnehviir Resurrected](https://www.nexusmods.com/skyrimspecialedition/mods/14272?tab=files)

#### Download Instructions

* **Main Files:** Durnehviir Resurrected

#### FOMOD Instructions

* **Restoration Speed:**
  * Normal
* **Color:**
  * Green
* **Degree of Restoration:**
  * Full Restore
* **Patches:**
  * ~~Durnehviir: God of Death~~

##### [Simple Player Home Improvements](https://www.nexusmods.com/skyrimspecialedition/mods/37236?tab=files)

#### Download Instructions

* **Main Files:** Simple Home Improvements AIO (Proudspire 4 Beds)

##### [Improved Shadowmarks](https://www.nexusmods.com/skyrimspecialedition/mods/17609?tab=files)

#### Download Instructions

* **Main Files:** Improved Shadowmarks (512)

> This mod also contains new textures for the Shadowmarks. Fortunately, since the textures are packed in a BSA, they will be automatically overwritten by the better looking ones from Ennead Shadowmarks if you installed that mod.

##### [Delphine’s Map Reveals Dragon Mounds](https://www.nexusmods.com/skyrimspecialedition/mods/26301?tab=files)

#### Download Instructions

* **Main Files:** Delphine’s Map Reveals Dragon Mounds SE v1.0

##### [Bring Meeko to Lod](https://www.nexusmods.com/skyrimspecialedition/mods/25246?tab=files)

#### Download Instructions

* **Main Files:** Bring Meeko to Lod SE

##### [Serana’s Blood Tomb Curse](https://www.nexusmods.com/skyrimspecialedition/mods/26852?tab=files)

#### Download Instructions

* **Main Files:** SeranasTombBloodCurse SE v1.1

##### [Karstaag - The Frost King Reborn](https://www.nexusmods.com/skyrimspecialedition/mods/14328?tab=files)

#### Download Instructions

* **Main Files:** Karstaag - The Frost King Reborn

#### FOMOD Instructions

* **Plugin:** Transparency Reduced and Infinite Summons