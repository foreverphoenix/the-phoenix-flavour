---
title: "Utilities & Frameworks"
weight: 2
type: docs
description: >
  Mod recommendations.
---

##### [Crash Logger](https://www.nexusmods.com/skyrimspecialedition/mods/59818)

{{< alert color="success" >}}**Essential.** Everyone should install this mod.{{< /alert >}}

Crash Logger is absolutely essential for troubleshooting. While the logs can be hard to read, they are crucial for tracking down issues. The linked version is up-to-date for SSE, AE, and VR, and will write to `\Documents\My Games\Skyrim Special Edition\SKSE\`.

I recommend pairing the plugin with [Crash Log Tools](/bg/tool-setup/crash-log-tools/).

**Requirements:** Skyrim Script Extender, Address Library for SKSE

##### [Rogue Master Detector](https://www.nexusmods.com/skyrimspecialedition/mods/93040)

{{< alert color="info" >}}**Recommended.** Very useful in any setup.{{< /alert >}}

Rogue Master Detector is an SKSE plugin which finds and logs masters that are loaded out of order. While missing masters cause errors, there are no *visible* errors when a plugin is loaded <u>above</u> its master. SSEEdit will automatically fix the load order, but the game will not, and out-of-order plugins will not function properly.

After launching the game, Rogue Master Detector creates a log file under `\Documents\My Games\Skyrim Special Edition\SKSE\` with any out-of-order plugins listed inside. Check the log and fix the load order if necessary.

**Requirements:** Skyrim Script Extender, Address Library for SKSE

##### [SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/12604)

{{< alert color="success" >}}**Essential.** Everyone should install this mod.{{< /alert >}}

SkyUI is nearly as crucial as SKSE. It not only overhauls the entire interface to be properly usable for mouse + keyboard but also adds the **mod configuration menu** feature. Other mods can add MCMs (settings menus) which can be accessed and configured as naturally as the base game settings.

If you prefer (parts of) the vanilla UI, you can (selectively) overwrite SkyUI with [Hide SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/12770) while retaining the MCM feature. There are also various extensions and reskins for SkyUI.

**Requirements:** Skyrim Script Extender

##### [QUI](https://www.nexusmods.com/skyrimspecialedition/mods/65343)

{{< alert color="info" >}}**Recommended.** Very useful in any setup.{{< /alert >}}

QUI combines an ingame plugin explorer (extremely useful for testing) with some vanilla interface tweaks, all of it being optional.

**Requirements:** Skyrim Script Extender, SkyUI

#### Settings File

QUI can be configured via its **QUI.toml** which can be overwritten with a custom file. This is usually preferable as changes will not be lost when updating the main mod.

- [Create a new empty mod](/Pictures/bg/create-empty-mod.png) in Mod Organizer 2 and name it **QUI - Settings**.
- Right-click the new mod and select **Open in Explorer**.
- Create the following folder structure: `\Mod Organzier 2\mods\QUI - Settings\SKSE\Plugins\`.
- Inside the **Plugins** folder, right-click, and select **New** >> **Text Document**.
- Name the file **QUI_Custom.toml**. <u>Remember to change the file extension.</u>

Back in Mod Organizer 2, press F5 to refresh the UI. Place the new mod below **QUI** and activate it.

You can now copy any settings from the default **QUI.toml** into the **QUI_Custom.toml** and customise them there.

#### Plugin Explorer

I personally like to pause the game while browsing through the plugin explorer. I also change the hotkey from F11 to F8 because it works better with my usual hotkey choices.

Paste the following into the **QUI_Custom.toml**:

```
[PluginExplorer]
Pause = true

[PluginExplorer.Key]
KeyboardToggle = 66
```

<u>Remember to save your changes before closing the window.</u>

I added `Game will pause in plugin browser. Changed hotkey to F8.` to the Notes tab afterwards.

#### Controller Tweak

QUI contains the [Stay At The System Page](https://www.nexusmods.com/skyrimspecialedition/mods/18397) that is otherwise no longer available for the current version of Skyrim SE. This tweak restores behaviour from the PC version of Skyrim LE where pressing ESCAPE would open the system menu as opposed to the journal. Since controllers have fewer buttons, the system button would open the journal instead in console versions of the game. This behaviour was added to the PC version of Skyrim SE.

If you play on m+kb, I recommend leaving the tweak enabled. ESCAPE will open the System Menu while J opens the Journal.

If you play on controller and prefer quick access to the Journal over quick access to the System Menu, you can set the default option for the system button back to the Journal in the **QUI_Custom.toml**:

```
[JournalMenu]
DefaultPage = 0
```

<u>Remember to save your changes before closing the window.</u>