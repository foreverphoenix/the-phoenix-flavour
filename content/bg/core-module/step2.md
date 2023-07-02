---
title: "Step 2"
weight: 2
type: docs
description: >
  Folder structures and file management. Skyrim Script Extender.
---

{{< alert color="info" title="Summary" >}}
> This step covers the differences between the root and data folder, the files that belong in each of them, and how those files can be managed with Mod Organizer 2. It also covers the installation of the Skyrim Script Extender.{{< /alert >}}

With the game freshly (re)installed and set up with Mod Organizer, we will now look at folder structures and how that affects mods.

The unmodded, pristine version of Skyrim that we restored previously is referred to as **Vanilla Skyrim**. It is about 12.7GB in size (plus up to 5.8GB for Creations) and located in a Steam library directory.

### Root Folder

Navigate to your Skyrim SE installation. The file path is `\Steam\steamapps\common\Skyrim Special Edition\`.

{{< alert color="info">}}You can use [this shortcut](/Pictures/bg/mo2-open-game-folder.png) in Mod Organizer 2 to quickly locate the folder.{{< /alert >}}

This is your **root folder**. It contains the two executables: **SkyrimSE.exe**, which directly opens the game, and **SkyrimSELauncher.exe**, which starts the Launcher first. The latter is what Steam runs when you start the game through the Steam UI.

![Root Folder](/Pictures/bg/core-module/skyrim-root-folder.png)

### Data Folder

The **data folder** is located inside the **root folder**. Open it now.

The **data folder** contains all game files which are split into **plugins (ESMs)** and **archives (BSAs)**. There are five **ESMs** containing all game data and 18 **BSAs** containing all assets. They are used by the engine to build the game.

{{< alert color="info">}}The five ESMs are also referred to as the **official master files**.{{< /alert >}}

![Data Folder](/Pictures/bg/core-module/skyrim-data-folder.png)

## Data Folder Files

The basic structure of mods is the same as the basic structure of the official game files.

There are **plugins** and **assets**.

- **Plugins** contain game data. They have the file extension **ESP**, **ESL**, or **ESM**.
- **Assets** are loose files. There are many kinds of assets, including textures, meshes, scripts, and so on.

**Assets** are often stored in **archives (BSAs)**. You can think of BSAs as 7ZIP / WinRAR archives for Skyrim assets (textures, scripts, etc). They require a plugin of the same name in order to be loaded. All vanilla game BSAs are therefore loaded by **Skyrim.esm**.

{{< alert color="warning" >}} Mods that are structured like the vanilla game files always belong in the data folder.{{< /alert >}}

![Mod Structure](/Pictures/bg/diagrams/basic-mod-structure.png)

### Mod Managers

Imagine this: You install 100 mods. Each of these mods consists of a different combination of plugins, archives, and loose files. You extract them all into the data folder. Many of them interact: They are patches or modifications for each other and therefore they contain some of the same files (as in: files with the same name). As you install these mods, they overwrite each other in the order of installation.

Now you want to update or remove a mod. Oh, no.

Unless you remember exactly which files belong to that mod and unless they never interacted with files from another mod, you now have a veritable situation on your hands. Fun issues that may ensue include "purple" objects or broken mechanics due to overwritten or missing assets. It is virtually impossible to build a functioning setup of even moderate dimensions in this fashion.

That is why we use mod managers to manage data folder files. **Mod Organizer 2** is particularly good at this.

### MO2's Virtual File System

The developer of Mod Organizer 2, Tannin, came up with a clever way of avoiding data folder spaghetti: When you install a mod through MO2 it is extracted into its own folder rather than into the data folder. This way, files from different mods never clash.

Here is the resulting folder structure:

- `\Mod Organizer 2\mods\Mod 1\<files from mod 1>`
- `\Mod Organizer 2\mods\Mod 2\<files from mod 2>`
- `\Mod Organizer 2\mods\Mod 3\<files from mod 3>`
- ...

When you launch any application (a modding tool or the game itself) through Mod Organizer 2, it builds a **virtual data folder** from the files in the separate folders at runtime.

{{< alert color="success" >}}**This creates the concept of a mod order:** All mods remain separate from each other. You will never lose track of files and any conflicts between mods (when they contain files of the same name) are visualised in Mod Organizer 2. You then review these files and decide which file should win the conflict by changing the order of the mods or selectively hiding/removing files.{{< /alert >}}

And that is why Mod Organizer 2 is going to be your best friend. Cherish it!

### Viewing the Data Folder

You can check your virtual data folder in the **Data** tab in the right pane in MO2.

Below you can see your *actual* data folder on the left (no creations, just vanilla files). On the right you can see your *virtual* data folder as previewed by MO2 which *does* include the creations as they are currently being managed by MO2.

![VDF](/Pictures/bg/core-module/virtual-data-folder.png)

## Root Folder Files

Mod Organizer 2 exists to manage the contents of the **data folder** which contains the vanilla game files and which is also where the vast majority of mods belong.

What about the **root folder**?

<u>Mods that do not belong into the data folder are rare.</u> They typically hook into the game's engine in some way which is why they must be located in the same directory as the game's executables, that is, the root folder.

Standard procedure involves managing **data folder mods** with a mod manager and dropping **root folder mods** directly into the root folder. This works fine because there are far fewer root folder mods and they clash very rarely.

That being said, there is an alternative that I strongly prefer and recommend.

### Root Builder

Enter **Root Builder**, a plugin for Mod Organizer 2 which enables it to manage root folder mods.

(You can think of MO2 plugins as mods for MO2. Yes, we are modding the mod manager.)

What are the advantages of Root Builder?

- You can manage <u>all mods</u> in Mod Organizer 2, keeping your Skyrim installation 100% clean and vanilla.
  - *This means your setup is completely self-contained and can exist alongside any number of other modlists.*
- You can use MO2 functionality for version number tracking, custom notes, conflict management, etc.
- You can use MO2 as an ENB / ReShade manager, switching between presets painlessly while retaining modifications.

{{< alert color="warning" >}}Making **Root Builder** optional is not currently feasible for this guide. While the plugin is not perfect, I believe that its benefits more than outweight the minor issues it sometimes causes.{{< /alert >}}

{{< alert >}}Please refer to the [Root Builder](/bg/additional-modules/root-builder/#installation) module for installation instructions.{{< /alert >}}

## Skyrim Script Extender

With **Root Builder** in place, we can install what is arguably the most important mod of all: The **Skyrim Script Extender** (SKSE).

{{< alert >}}Please refer to the [Skyrim Script Extender](/bg/additional-modules/skyrim-script-extender/) module for more details and installation instructions.{{< /alert >}}

## Meta Files

When downloading mods from the Nexus, a **.meta** file with various information about the mod will be downloaded alongside it and data from this meta file, like the mod's URL, Nexus category, and version number, will be automatically extracted from the meta file when installing the mod through MO2. Some of this data is then displayed in the MO2 UI.

The meta file will also automatically reflect the installation status of the mod in the **Downloads** pane. Currently, the downloaded MO2 plugins and SKSE are listed as "Downloaded" rather than "Installed" because we installed them manually. Address Library is properly marked as "Installed" because we *did* install it through the UI.

(After uninstalling a mod, its archive will be listed as "Uninstalled" in the **Downloads** tab.)

{{< alert color="info" >}}**The following instructions are optional.** You can absolutely ignore this feature and skip ahead to [Step 3](/bg/core-module/step3/) as it is purely cosmetic.{{< /alert >}}

I personally update my metas *religiously* to keep track of which mods I have yet to install or update and which archives can be removed. The larger your setup the more important it is to be diligent in keeping MO2 clean.

In this case, I will mark the manually installed mods as "Installed" by modifying their meta files.

- Right-click the **Curation Club** archive in your **Downloads** tab and select **Open Meta File**.
  - *You may have to choose an app. I recommend setting **Notepad++** as the default.*
- Change **installed** from **false** to **true** near the bottom of the file.

{{< alert color="info" >}}Here you can also see the other data saved in the meta files, including version number, description, link, and more.{{< /alert >}}

- Save your change and close the file.
- Repeat the process for the **Root Builder** and **Skyrim Script Extender** meta files.

Order has been restored.

### Version Number

Since we did not install the **Skyrim Script Extender** through Mod Organizer 2, it did not import any data from the meta file. I do, however, like to use MO2 to keep track of version numbers and updates, so I am filling in the required data manually.

- Double-click **Skyrim Script Extender** in your mod order.
- Switch to the **Nexus Info** tab.
- Under **Mod ID** enter **30379**.

You can find the ID for SKSE (and any other Nexus mod) in the respective URL ([reference picture](/Pictures/bg/core-module/find-mod-id.png)). This will allow Mod Organizer 2 to track the mod page and notify you about updates as well as enable the option to right-click the mod and quickly open the Nexus page.

- Under **Version** enter the current version, i.e. **2.2.3**.

After you close the window again, the version number will appear properly in the **Versions** column in the MO2 UI like it will for all mods that you install in the future.

---

#### Please continue with [Step 3](/bg/core-module/step3/).