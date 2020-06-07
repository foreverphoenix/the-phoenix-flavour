---
title: "New Mechanics & Features"
weight: 36
type: docs
description: >
  Additional gameplay mechanics not present in the vanilla game.
---

## 36.1 Simply Knock (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/14098?tab=files)

* **Main Files:** Simply Knock SE 1.0.3 Release

#### Additional Instructions

The mod includes outdated plugins for PapyrusUtil and Simply Knock, both of which will be replaced with updated ones.

* Delete the following file(s) and/or folder(s):
  * `SKSE`

## 36.2 Simply Knock SKSE64 DLL (optional)

{{% alert title="Mod Dependency" color="warning" %}}
Only install this mod if you installed **Simply Knock**. Otherwise skip it.{{% /alert %}}

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/24297?tab=files)

* **Main Files:** SimplyKnockSE SKSE64 2.0.17 DLL

## 36.3 Quick Light (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/12633?tab=files)

* **Main Files:** Quick Light SE

## 36.4 ENB Light – Quick Light Patch (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/22574?tab=files)

* **Optional Files:** ENB Light - patch for Quick Light SE

## 36.5 Trua - Minimalistic Faiths of Skyrim (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/32549?tab=files)

* **Main Files:** Trua 1.0.1

## 36.6 Choose Your Own Arch-Mage

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/30887?tab=files)

* **Main Files:** Choose Your Own Arch-Mage

## 36.7 Adopt Aventus Aretino

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/3257?tab=files)

* **Main Files:** Adopt Aventus Aretino

## 36.8 Irondusk's Saddlebags (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrim/mods/91395?tab=files)

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