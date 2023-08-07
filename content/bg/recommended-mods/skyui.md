---
title: "SkyUI"
weight: 2
type: docs
description: >
  Mod recommendations.
---

##### [SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/12604)

{{< alert color="success" >}}**Essential.** Everyone should install this mod.{{< /alert >}}

SkyUI is a major interface overhaul which transforms Skyrim's console UI into one optimised for mouse and keyboard (while still being perfectly functional with controller). More information is visible at a glance and menus are far easier to navigate.

Most major interface overhauls are SkyUI reskins and require SkyUI as the base.

In addition to overhauling the interface, SkyUI also adds the **Mod Configuration Menu**, a framework for mods to add neatly integrated customisation options accessible through the ESCAPE menu.

**Requirement(s):** Skyrim Script Extender

##### [SkyUI - Source 5.1](https://github.com/schlangster/skyui/wiki)

{{< alert color="danger" >}}**Situational.** Only install this mod if you need it.{{< /alert >}}

Source files for SkyUI are needed if you ever want to (re)compile scripts calling SkyUI functions. For example, you will need the source files to [automate MCMs](/bg/additional-modules/automating-mcms/).

I recommend grabbing both the 5.1 and 5.2 source files because you need to match the version that was used to create the script when trying to recompile. It is good to have the latest version, but you may also need older versions at times.

<u>If you are not planning on modifying any MCMs, you do not need to install the SkyUI source files.</u>

**Requirement(s):** SkyUI

#### Installation

The source files for SkyUI 5.1 are available on the SkyUI Github:

- Download the **SkyUI 5.1 SDK** from the [SkyUI Wiki](https://github.com/schlangster/skyui/wiki) or use this [direct link](https://drive.google.com/file/d/0B4iEH8ar3jtxbFlkVzZSVHN0alk/view?resourcekey=0-bTFKQxbSl6Y_4-dZDHE0AQ) to the Google Drive.
- Create a new folder under `\Mod Organizer 2\mods\` and name it **SkyUI - Source 5.1**.
- Open the downloaded archive and extract the **Scripts** folder into the new mod folder.

The "mod" should only be active when recompiling scripts that call SkyUI functions.

##### [SkyUI - Source 5.2](https://github.com/MrOctopus/nl_online)

{{< alert color="danger" >}}**Situational.** Only install this mod if you need it.{{< /alert >}}

*See description for **SkyUI - Source 5.1.***

**Requirement(s):** SkyUI

#### Installation

The source files for SkyUI 5.2 were updated by Mr Never Lost (MrOctopus) and are available on Github:

- Download the [repository](https://github.com/MrOctopus/nl_online) by going to **Code** >> **Download ZIP** ([picture](/Pictures/bg/recommended-mods/skyui/skyui-source-git.png)).
- Create a new folder under `\Mod Organizer 2\mods\` and name it **SkyUI - Source 5.2**.
- Create a new **scripts** folder inside.
- Open the downloaded archive and open the **skyui** folder inside.
- Extract the **source** folder into the new **scripts** folder.

The "mod" should only be active when recompiling scripts that call SkyUI functions.

##### [SkyUI - Flashing Savegame Fix](https://www.nexusmods.com/skyrimspecialedition/mods/20406?tab=files)

{{< alert color="info" >}}**Recommended.** Very useful in any setup.{{< /alert >}}

This mod fixes a SkyUI a bug where the small thumbnail for saves flickers wildly in the menu. If you use any SkyUI reskin, this file will probably be overwritten.

<u>Skip this mod if you are on widescreen.</u>

**Requirement(s):** SkyUI

##### [Fix Note Icon for SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/32561?tab=files)

{{< alert color="info" >}}**Recommended.** Very useful in any setup.{{< /alert >}}

This mod fixes a SkyUI a bug where the small thumbnail for saves flickers wildly in the menu. If you use any SkyUI reskin, this file will probably be overwritten.

<font size=2>*I usually rename this mod to "SkyUI - Fix Note Icon" so it nicely matches the other SkyUI fixes. This is very optional.*</font>

**Requirement(s):** Skyrim Script Extender, Address Library for SKSE, SkyUI

##### [SkyUI - Ghost Item Bug Fix](https://www.nexusmods.com/skyrimspecialedition/mods/49106?tab=files)

{{< alert color="info" >}}**Recommended.** Very useful in any setup.{{< /alert >}}

This mod fixes a few minor issues with SkyUI groups in the Favourites menu.

**Requirement(s):** SkyUI

##### [SkyUI 3D Item Offset Fix](https://www.nexusmods.com/skyrimspecialedition/mods/92602?tab=files)

{{< alert color="info" >}}**Recommended.** Very useful in any setup.{{< /alert >}}

This mod fixes the slightly off-centre placement of item previews in SkyUI specifically for 16:9 resolutions. The placement can be modified in the MCM, but it is easier to simply use this modified script.

I strongly recommend downloading the version that also support [MCM Helper](/bg/recommended-mods/utilities-frameworks/#mcm-helper) which is another essential mod. Since MCM Helper's assets are packed into a BSA, this mod's loose files will still overwrite, even if it is placed higher in the mod order.

<font size=2>*Here, too, I add a hyphen to the mod name so it matches the other fixes for SkyUI: "SkyUI - 3D Item Offset Fix".*</font>

<u>Skip this mod if you are on widescreen.</u>

**Requirement(s):** SkyUI, MCM Helper (optional)

##### [Wider MCM Menu for SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/22825?tab=files)

{{< alert color="info" >}}**Recommended.** Very useful in any setup.{{< /alert >}}

This mod extends the size of the MCM to be better legible. Check the screenshots and download one of the main files (I prefer the first one).

<u>Skip this mod if you are on widescreen.</u>

**Requirement(s):** SkyUI