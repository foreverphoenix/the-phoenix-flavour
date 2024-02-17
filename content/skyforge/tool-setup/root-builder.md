---
title: "Root Builder"
weight:
type: docs
description: >
  How to set up Root Builder.
---

{{< alert color="info" title="Summary" >}}
> This module covers the purpose and installation of the Root Builder plugin for MO2.<p>
> **Prerequisite(s):** [Mod Organizer 2](/skyforge/tool-setup/mo2/){{< /alert >}}

## About Root Builder

**Root Builder** is a plugin for Mod Organizer 2.

It allows us to install and manage files that must go into the root folder through Mod Organizer 2. When we launch the game or any tool through Mod Organizer 2, all root folder files will be *temporarily* moved into the actual root folder by the plugin. When the game or tool is closed, those files will automatically be removed again from the root folder. Pretty neat, huh?

There are multiple advantages to using **Root Builder**:

- The root folder will always stay clean and vanilla, and there will be no overlap between multiple modded setups.
- This allows you to run a personal setup and a Wabbajack list independently from each other.*
- All files are managed through Mod Organizer 2 for easy activation/deactivation, version control, custom notes, etc.
- (Potential support for the GOG version of Skyrim in this guide later on!)

<font size=2>\**All setups must run the same version of Skyrim to share a root folder. However, most Wabbajack lists that are not on the latest version use the Stock Game folder system (see below) and will thus not interfere at all.*</font>

{{< alert color="warning" >}}If we were to dump all root folder files into the root folder it would quickly become difficult to tell which files are vanilla and which are mod-added, and, if they are mod-added, which version is currently installed. This gets nowhere near as bad as an unmanaged data folder, but it is inconvenient and we do not like inconvenience.{{< /alert >}}

**With Mod Organizer 2 and Root Builder we can build an almost completely self-contained modded setup.\***

<font size=2>\**We could use the Stock Game folder system and create an entire new copy of the vanilla game files (i.e., the root folder) to make the setup fully self-contained. However, that would add about 13GB of files without offering any meaningful benefits for most regular users.*</font>

{{< alert color="info" >}}Is Root Builder perfect? I would not say that. However, the issues that I have encountered with the plugin (in about a year of heavy use) are very minor and easy to fix. While not everyone likes the plugin, I personally find it invaluable and highly recommend it.{{< /alert >}}

## Installation

**Root Builder** is hosted on the Nexus.

- Download the latest version of [Root Builder](https://www.nexusmods.com/skyrimspecialedition/mods/31720?tab=files) (click **Mod Manager Download**).
- In Mod Organizer 2, switch to the **Downloads** tab in the right pane.
- Right-click the downloaded mod and select **Open File**.
- Extract the **rootbuilder** folder to `\Mod Organizer 2\plugins\`.

{{< alert color="warning" >}}To quickly access the **plugins** folder, you can click [the folder icon](/Pictures/skyforge/mo2-plugins-folder-shortcut.png) above the left pane and select **Open MO2 Plugins Folder**.{{< /alert>}}

Restart Mod Organizer 2.

![Root Builder Installation](/Pictures/skyforge/modding-resources/root-builder-installation.png)

---

#### If you are currently working through the Beginner's Guide, return to [Step 2](/skyforge/beginners-guide/step2/#mo2-separators).