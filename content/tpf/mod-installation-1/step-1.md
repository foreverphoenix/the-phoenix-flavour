---
title: "Step 1: Utilities"
weight: 1
type: docs
description: >
  Required mods and frameworks.
---

This separator should already contain the **SKSE Scripts** and **SKSE INI** mods. Place the new mods below them.

##### [Address Library for SKSE Plugins](https://www.nexusmods.com/skyrimspecialedition/mods/32444?tab=files)

#### Download Instructions

- **Main Files:** All in one (Anniversary Edition)

##### [Crash Logger](https://www.nexusmods.com/skyrimspecialedition/mods/59596?tab=files)

#### Download Instructions

- **Main Files:** Crash Logger

##### [PapyrusUtil](https://www.nexusmods.com/skyrimspecialedition/mods/13048?tab=files)

#### Download Instructions

- **Main Files:** PapyrusUtil AE - Scripting Utility Functions

##### [powerofthree's Papyrus Extender](https://www.nexusmods.com/skyrimspecialedition/mods/22854?tab=files)

#### Download Instructions

- **Main Files:** Papyrus Extender SE

#### FOMOD Instructions

- **DLL:** SSE v1.6+ ("Anniversary Edition")

##### [JContainers](https://www.nexusmods.com/skyrimspecialedition/mods/16495?tab=files)

#### Download Instructions

- **Main Files:** JContainers SE

> Make sure to pick the second main file for AE (1.6.x).

##### [Scaleform Translation Plus Plus](https://www.nexusmods.com/skyrimspecialedition/mods/22603?tab=files)

#### Download Instructions

- **Main Files:** ScaleformTranslationPP

##### [Base Object Swapper](https://www.nexusmods.com/skyrimspecialedition/mods/60805?tab=files)

#### Download Instructions

- **Main Files:** Base Object Swapper SE

#### FOMOD Instructions

- **DLL:** SSE v1.6+ ("Anniversary Edition")

##### [Spell Perk Item Distributor](https://www.nexusmods.com/skyrimspecialedition/mods/36869?tab=files)

#### Download Instructions

- **Main Files:** Spell Perk Item Distributor - AE

##### [Keyword Item Distributor](https://www.nexusmods.com/skyrimspecialedition/mods/55728?tab=files)

#### Download Instructions

- **Main Files:** Keyword Item Distributor - SE

##### [Dynamic Armor Variants](https://www.nexusmods.com/skyrimspecialedition/mods/65963?tab=files)

#### Download Instructions

- **Main Files:** Dynamic Armor Variants

#### FOMOD Instructions

- **Game Version:** Skyrim Special Edition
- **Select Addons:**
  - ~~UIExtensions Menu~~
  - ~~Hidden Equipment~~

##### [MCM Helper](https://www.nexusmods.com/skyrimspecialedition/mods/53000?tab=files)

#### Download Instructions

- **Main Files:** MCM Helper SE (1.6)

##### [ConsoleUtil](https://www.nexusmods.com/skyrimspecialedition/mods/24858?tab=files)

#### Download Instructions

- **Main Files:** ConsoleUtilSSE

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

- **Main Files:** ENB Helper SE 2.1 for SSE 1.6.xxx

##### [ENB Helper Plus](https://www.nexusmods.com/skyrimspecialedition/mods/62743?tab=files)

#### Download Instructions

- **Main Files:** ENB Helper Plus

#### FOMOD Instructions

- **Core Files:** ENB Helper Plus for 1.6.x (Post-AE)

##### [ENB Input Disabler](https://www.nexusmods.com/skyrimspecialedition/mods/62796?tab=files)

#### Download Instructions

- **Main Files:** ENB Input Disabler

#### FOMOD Installer

- **Core Files:** ENB Input Disabler for 1.6.x (Post-AE)

##### [Auto Input Switch](https://www.nexusmods.com/skyrimspecialedition/mods/54309?tab=files)

#### Download Instructions

- **Main Files:** Auto Input Switch

> Download the first main file for Skyrim Special Edition 1.6.x.

##### [Screenshot Helper](https://www.nexusmods.com/skyrimspecialedition/mods/64124?tab=files)

#### Download Instructions

- **Main Files:** Screenshot Helper

#### FOMOD Instructions

- **Core Files:** Screenshot Helper for 1.6.x (Post-AE)

##### [xSHADOWMANx's Dll Loader](https://www.nexusmods.com/skyrimspecialedition/mods/3619/?tab=files)

#### Download Instructions

- **Main Files:** DllLoader

#### Installation Instructions

Step 1:

- Double-click the mod in the **Downloads** pane to install it.
- Right-click the **Data** folder and select **\<Set as data directory>**.
- Click **OK** and **Ignore** (the directory *is* correct).

Step 2:

- Right-click **DllLoader** in the **Downloads** pane and select **Open in Explorer**.
- Extract **DINPUT8.dll** to `\The Phoenix Flavour\Stock Game\`.

#### Additional Instructions

- Double-click **xSHADOWMANx's DLL Loader** in the mod order.
- Switch to the **INI Files** tab and select the **DllLoader.ini**.
- In **Line 2**, set `iEnableLogging` to `0`.
- Press CTRL + S to save your change and close the window.

##### [Keyboard Shortcuts Fix](https://www.nexusmods.com/skyrimspecialedition/mods/3620?tab=files)

#### Download Instructions

* **Main Files:** KeyboardShortcutsFix

#### Installation Instructions

- After installing the mod from the **Downloads** pane, right-click it in the mod order and select **Open in Explorer**.
- Create two new folders `\Plugins\Sumwunn\` and move all files from the top level folder into the `\Sumwunn\` folder.

![Keyboard Shortcuts Fix](/Pictures/tpf/mod-installation/keyboard-shortcuts-fix.png)

#### Additional Instructions

- Double-click **Keyboard Shortcuts Fix** in your mod order.
- Switch to the to **INI Files** tab and select the **KeyboardShortcutsFix.ini**.
- In **Line 2**, set `iEnableLogging=` to `0`.
- Press CTRL + S to save your change and close the window.

---

#### Continue with the [Essential Mods](/tpf/mod-installation-1/step-2/) page.