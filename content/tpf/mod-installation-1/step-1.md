---
title: "Step 1: Utilities"
weight: 1
type: docs
description: >
  Required mods and frameworks.
---

This separator should already contain the **SKSE - Scripts** and **SKSE INI** mods. Place the new mods below them.

##### [Address Library for SKSE Plugins](https://www.nexusmods.com/skyrimspecialedition/mods/32444?tab=files)

#### Download Instructions

- **Main Files:** All in one (Special Edition)

##### [.NET Script Framework](https://www.nexusmods.com/skyrimspecialedition/mods/21294?tab=files)

#### Download Instructions

- **Main Files:** NetScriptFramework SkyrimSE v18

##### [PapyrusUtil](https://www.nexusmods.com/skyrimspecialedition/mods/13048?tab=files)

#### Download Instructions

Download **PapyrusUtil 3.9** from the Old Files section.

- **Old Files:** PapyrusUtil SE - Scripting Utility Functions

##### [powerofthree's Papyrus Extender](https://www.nexusmods.com/skyrimspecialedition/mods/22854?tab=files)

#### Download Instructions

- **Main Files:** Papyrus Extender SE

##### [JContainers](https://www.nexusmods.com/skyrimspecialedition/mods/16495?tab=files)

#### Download Instructions

- **Main Files:** JContainers SE

##### [Scaleform Translation Plus Plus](https://www.nexusmods.com/skyrimspecialedition/mods/22603?tab=files)

#### Download Instructions

- **Main Files:** ScaleformTranslationPP

##### [Spell Perk Item Distributor](https://www.nexusmods.com/skyrimspecialedition/mods/36869?tab=files)

#### Download Instructions

- **Main Files:** Spell Perk Item Distributor - SSE

##### [MCM Helper](https://www.nexusmods.com/skyrimspecialedition/mods/53000?tab=files)

#### Download Instructions

Download **MCM Helper 1.3.0** from the Old Files section.

- **Old Files:** MCM Helper SE

##### [ConsoleUtil](https://www.nexusmods.com/skyrimspecialedition/mods/24858?tab=files)

#### Download Instructions

Download **ConsoleUtilSSE 1.2.0** from the Old Files section.

- **Old Files:** ConsoleUtilSSE

##### [Console Commands Extender](https://www.nexusmods.com/skyrimspecialedition/mods/28210?tab=files)

#### Download Instructions

- **Main Files:** Console Commands Extender

*This mod was added mostly for the `spp` console command which allows you to quickly cheat perk points. This can be useful for testing, since vanilla Skyrim has no command to directly add perk points.*

##### [Autorun](https://www.nexusmods.com/skyrimspecialedition/mods/45451?tab=files)

#### Download Instructions

- **Main Files:** Autorun

#### Additional Instructions

- Rename **Autorun.esp** to **Autorun.esl**.

#### Console Commands

Game settings can be implemented in two ways: They can be added to a plugin or toggled in the console using the `SetGS` command. When using the console, the command would have to be entered every time the game is restarted. Fortunately we have Autorun which will execute any console commands configured in its text file automatically when loading a save.

- Double-click **Autorun** in Mod Organizer 2.
- Switch to the **Text Files** tab and select the **Autorun.txt** file.
- Copy and paste the following lines into the text field:

```
cl off
SetGS fPhysicsDamage1Mass 9999999
SetGS fCombatAimProjectileRandomOffset 70
```

- Close the window and click **Yes** when asked to save.

> The added commands will expand the radius in which NPCs can move when they sandbox and lower NPC's accuracy with ranged attacks, as well as disable character lighting and physics damage sustained when colliding with clutter objects.

![ACC Add MFS](/Pictures/tpf/mod-installation/autorun-commands.png)

##### [ENB Helper](https://www.nexusmods.com/skyrimspecialedition/mods/23174?tab=files)

#### Download Instructions

- **Main Files:** ENB Helper SE 1.5 for SSE 1.5.97

---

#### Continue with the [Essential Mods](/tpf/mod-installation-1/step-2/) page.