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

#### FOMOD Instructions

- **DLL:** SSE v1.5.97 ("Special Edition")

##### [JContainers](https://www.nexusmods.com/skyrimspecialedition/mods/16495?tab=files)

#### Download Instructions

- **Main Files:** JContainers SE

##### [Scaleform Translation Plus Plus](https://www.nexusmods.com/skyrimspecialedition/mods/22603?tab=files)

#### Download Instructions

Download **Scaleform Translation Plus Plus 1.4.1** from the Old Files section.

- **Old Files:** ScaleformTranslationPP

##### [Spell Perk Item Distributor](https://www.nexusmods.com/skyrimspecialedition/mods/36869?tab=files)

#### Download Instructions

- **Main Files:** Spell Perk Item Distributor - SSE

##### [Keyword Item Distributor](https://www.nexusmods.com/skyrimspecialedition/mods/55728?tab=files)

#### Download Instructions

- **Main Files:** Keyword Item Distributor - SE

##### [Base Object Swapper](https://www.nexusmods.com/skyrimspecialedition/mods/60805?tab=files)

#### Download Instructions

- **Main Files:** Base Object Swapper SE

#### FOMOD Instructions

- **DLL:** SSE v1.5.97 ("Special Edition")

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
SetGS fCombatAimProjectileRandomOffset 70
```

- Close the window and click **Yes** when asked to save.

> The added commands will expand the radius in which NPCs can move when they sandbox and lower NPC's accuracy with ranged attacks, as well as disable character lighting and physics damage sustained when colliding with clutter objects.

![ACC Add MFS](/Pictures/tpf/mod-installation/autorun-commands.png)

##### [ENB Helper](https://www.nexusmods.com/skyrimspecialedition/mods/23174?tab=files)

#### Download Instructions

- **Main Files:** ENB Helper SE 1.5 for SSE 1.5.97

##### [ENB Helper Plus](https://www.nexusmods.com/skyrimspecialedition/mods/62743?tab=files)

#### Download Instructions

- **Main Files:** ENB Helper Plus

#### FOMOD Instructions

- **Core Files:** ENB Helper Plus for 1.5.97 (Pre-AE)

##### [ENB Input Disabler](https://www.nexusmods.com/skyrimspecialedition/mods/62796?tab=files)

#### Download Instructions

- **Main Files:** ENB Input Disabler

#### FOMOD Installer

- **Core Files:** ENB Input Disabler for 1.5.97 (Pre-AE)

##### [Auto Input Switch](https://www.nexusmods.com/skyrimspecialedition/mods/54309?tab=files)

#### Download Instructions

- **Main Files:** Auto Input Switch

##### [Keyboard Shortcuts Fix](https://www.nexusmods.com/skyrimspecialedition/mods/3620?tab=files)

#### Download Instructions

* **Main Files:** KeyboardShortcutsFix_SKSE64

#### Additional Instructions

- Double-click **Keyboard Shortcuts Fix** in your mod order.
- Switch to the to **INI Files** tab and select the **KeyboardShortcutsFix.ini**.
- In **line 2**, set `iEnableLogging=` to `0`.
- Press CTRL + S to save your changes and close the window.

##### [Screenshot Helper](https://www.nexusmods.com/skyrimspecialedition/mods/64124?tab=files)

#### Download Instructions

- **Main Files:** Screenshot Helper

#### FOMOD Instructions

- **Core Files:** Screenshot Helper for 1.5.97 (Pre-AE)

##### [Dragonborn Presence - Discord Rich Presence](https://www.nexusmods.com/skyrimspecialedition/mods/25287?tab=files)

#### Download Instructions

This is purely a Discord integration mod. With it installed, other people will be able to see your character's name, level, and location in your profile on Discord. As not everyone might want or need that, **this mod is optional**. You may skip it if you wish.

- **Main Files:** Dragonborn Presence

#### Installation Instructions

The mod consists of an ESP, SKSE plugin, and scripts as well as an additional DLL plugin. The latter needs to be placed in the **root** folder.

- Begin the installation process as usual by double-clicking the archive in the **Downloads** tab.
- Right-click the **Data** folder and select **Set as \<data> directory**.
- Click **OK** to install the mod.

Now we need to place the DLL in the **root** folder:

- Right-click the downloaded archive in the **Downloads** tab and select **Open File**.
- Extract the `discord-rpc.dll` to `\The Phoenix Flavour\Stock Game\`.

The mod is now properly installed.

---

#### Continue with the [Essential Mods](/tpf/mod-installation-1/step-2/) page.