---
title: "Technical Basics"
weight: 2
type: docs
description: >
  Mods, their components, and how they function on a basic level.
---

## Vanilla Skyrim

### The Root Folder

`steamapps\common\Skyrim Special Edition`

After installing Skyrim SE through Steam, the installation folder will have a size of about 13GB. This folder is referred to as the **Root** folder and contains (among other files) the game’s executables: SkyrimSE.exe and SkyrimSELauncher.exe.

Any mods that must be installed into the **Root** folder cannot be installed with a mod manager and must be moved into the root folder manually. Examples of mods that belong in the **Root** folder are SKSE, ENBSeries, and CK Fixes.

### The Data Folder

`steamapps\common\Skyrim Special Edition\Data`

The root folder also contains another important directory: the **Data** folder. This is where the vast majority of mods belong, and mod managers are typically used to manage its contents. Confusing the **Root** and **Data** folders will lead to mods not working, as they need to be in the correct directory in order for the game to recognise them, so be sure to keep the difference in mind.

Inside the **Data** folder you can find the "skeleton" of vanilla Skyrim: its five master plugins and associated archives. All game files are stored here in these two file formats. These are the five master plugins (or official master files):

- Skyrim.esm
- Update.esm
- Dawnguard.esm
- HearthFires.esm
- Dragonborn.esm

The first is the original game’s plugin and the largest of them all. The second one contains all additions and fixes that were patched in post-launch and for the Special Edition re-release. The remaining three plugins belong to the DLC as the names indicate.

### The INI Folder

`C:\Users\{USERNAME}\Documents\My Games\Skyrim Special Edition`

After running the game for the first time, the INI folder, containing the game’s configuration files, will be generated. Besides the **Skyrim.ini** and **SkyrimPrefs.ini** (which store the game’s settings), the INI folder also contains the **Saves** folder with your save files.

> There will be several more folders added automatically later on where certain mods store their LOG files.

### Folder Types

As the above should have made clear, it's important to move files into the proper directories, otherwise they simply won't work. Installing the Skyrim Script Extender or ENBSeries into the Data folder is a very common beginner's mistake. Over the course of the Beginner's Guide and throughout the Full Guide, I will refer to those three folders simply by the names defined here (Root, Data, and INI folder).

## Plugins

### Elder Scrolls Plugins

Plugins are files with the extensions ESP, ESL, or ESM. They edit records from Skyrim’s master files or add new ones.

The most common plugin format is the **Elder Scrolls Plugin** (ESP), and it is used for the majority of mods. ESPs can be created using the official modding tool, the Creation Kit, or the community’s tool, SSEEdit, and they can contain all kinds of data for cells, worldspaces, NPCs, their behaviours and appearances, game rules, quests with their different stages, dialogue, and so on. Vanilla Skyrim does not have any ESPs, only ESMs.

**Elder Scrolls Master** plugins (ESM) are always loaded at the top of your load order, before your ESPs. An ESP always requires at least one ESM which is usually Skyrim.esm. However, ESPs may also require other ESPs. These dependencies are not mere suggestions; they are hard requirements, and missing a plugin’s required master will result in errors and crashes.

It is possible to flag an ESP as ESM. This will cause the plugin to load near the top of your load order and above the regular ESPs.

### Plugin Limit and ESL Plugins

You can load a maximum of 255 ESPs and ESMs (including the five master files) into the game. If you exceed that limit, Skyrim will crash on launch.

**Elder Scrolls Light** plugins (ESL) are, however, the exception. They are smaller: they have a lower formID budget, meaning that they can store less data, which is why they are often used for smaller mods, patches, or dummy plugins. ESLs are loaded in their own plugin space, and they will always be moved below your ESMs and above your ESPs in your load order. You can load about 4096 ESL plugins, but the exact number varies as it depends on the amount of data each ESL stores. ESL plugins were originally added in 2017 for the Creation Club.

The final plugin type is a hybrid of either ESM or ESP with an added ESL flag. By flagging an ESM or ESP as ESL, you may force it to load in ESL space and prevent it from counting toward the 255 ESM+ESP limit. Additionally, you will be able to manipulate its load order instead of being forced to load it between ESMs and ESPs. An "ESL-ified" master plugin – **ESM-ESL** - will load at the top of your load order with the other ESMs, while an "ESL-ified" regular plugin - **ESP-Lite** or **ESP-FE** - will load with all other ESPs.

You can flag any plugin as ESL so long as it does not exceed the maximum amount of FormIDs. If the plugin adds new FormIDs (that are not part of a master plugin such as the official master files), you will also have to renumber (compact) them.

In order to convert an ESP to ESL, you will have to flag it as ESL and rename the file extension from ESP to ESL. Any ESL can be converted to an ESP-Lite by simply changing the file extension from ESL to ESP.

### Plugin INIs

Plugins can load INI files that have the same name, for example **Grass Plugin.esp** would load **Grass Plugin.ini**. One can then add any line that appears in Skyrim.ini with the exception of lines that also appear in SkyrimPrefs.ini. The INI settings defined in plugin INIs will overwrite the originals from the Skyrim.ini.

One popular use case is grass mods like in the example above. By default, the line `iMinGrassSize` in Skyrim.ini has a value of 60 for vanilla grass density. Grass mods typically lower this value, thereby increasing the grass density, and they often do this through a plugin INI. This eliminates the need of editing the base INI files.

## Load Order & Conflicts

### Example Load Order

We already established that ESMs load at the top of your load order, followed by your ESLs and eventually your ESPs. The load order is essentially a list of all your plugins. Since they overwrite each other, it is important to sort them correctly. Here is what your load order with different types of plugins may look like:

**Bold** indicates an ESM, *Cursive* indicates an ESL.

- **Skyrim.esm**
- **Update.esm**
- **Dawnguard.esm**
- **HearthFires.esm**
- **Dragonborn.esm**
- **Unofficial Skyrim Special Edition Patch.esp**  <<< `an ESM-ified ESP`
- ***DwemerGatesNoRelock.esl***  <<< `an ESM-ified ESL`
- **Lanterns of Skyrim.esm**  <<< `a regular ESM`
- *Disarming Traps Is Dangerous.esl*  <<< `a regular ESL`
- SkyUI.esp  <<< `a regular ESP`
- *Modern Brawl Bug Fix.esp*  <<< `an ESL-ified ESP`

*Replace the above with a screenshot from the SkyPlus setup once that's available.*

### The Rule of One

The data inside those plugins is saved and sorted in the form of **records**. Each record has its own unique **Form ID** which is used to identify and link to it. These records function like layers, and only the one on the top can be read – it covers up all those below. If one of the layers below the one on top edits the same record, a conflict arises. This is also referred to as **The Rule of One**.

To elaborate, here is a simplified example:

- **Plugin A.esp**
  - Record 1
  - ~~Record 2~~
- **Plugin B.esp**
  - Record 2
  - Record 3

Our two example plugins both edit two records, and both of them touch Record 2. This is a conflict! Since **Plugin B** is lower in the load order, it will overwrite **Plugin A** and its version of Record 2 will be loaded in the game.

### Load Order Adjustments

### Conflict Resolution

### The Solution

- Why patches & manual CR are essential.
- Why LOOT, Merged Patch, and Bashed Patch aren't the be-all-and-end-all.

## Assets

### File Types

"Assets" is the general term for all kinds of loose files, such as textures, meshes, and scripts. All vanilla assets are stored within 18 **Bethesda Softworks Archives** (or BSAs) which in turn are located inside your **Data** folder. These BSAs work much like ZIP or RAR archives - they contain loose files, compressed to save space, and require specific software to un- or re-pack them.

These are the most popular filetypes:

* **Textures** – DDS
* **Meshes –** NIF
* **Scripts** – PEX
* **Script Source -** PSC *only required if you want to edit and recompile scripts; otherwise they can be ignored*
* **Interface** – SWF
* **Sounds, Music** – XWM / WAV
* **Voices** – FUZ
* **(SKSE) Plugins** – DLL
* **Animations, Skeleton** – HKX
* **Configuration Files** – INI / XML / JSON

### Bethesda Softworks Archives

As mentioned, BSAs are used to store and compress loose files. Every BSA must be attached to a plugin with the same name; for instance, **Snow.bsa** would be loaded by **Snow.esp** and not **Trees.esp**. Without an active plugin to load it, a BSA will not be recognised and used by the game. The plugin can be a "dummy": an empty plugin that contains no records. Files can be packed into BSAs using a tool that is  included in the Creation Kit installation and extracted with community-made tools such as Bethesda Archive Extractor.

Occasionally, you may come across ESP+BSA combinations with one **Snow.bsa** and one **Snow - textures.bsa**. The second archive contains, as the name suggests, only textures (DDS files), and it will be loaded as usual by **Snow.esp**.

There is also an uncompressed variant of BSAs, which is used to store sound and music files.

Regular BSAs (**Example.bsa**) for Skyrim SE must be 2GB or smaller, while texture BSAs (**Example - textures.bsa**) versions may be a little larger. This is why the assets of larger mods (and of Skyrim SE itself) are split up into multiple archives.

## Mod Order

### Loose Files

Assets in your mod order overwrite each other just like records from plugins do in your load order, although it is a bit more straightforward here. If, for instance, **Mod A** contains one version of the texture **Example.dds** and **Mod B** contains a different version, the mod that is loaded lower will overwrite.

* **Mod A**
  * ~~Example.dds~~
* **Mod B**
  * Example.dds

### Packed Files

Things get more complicated once BSAs are added to the mix. Packed assets are by default overwritten by loose assets *regardless* of mod order. Let’s assume **Mod C** also contains **Example.dds**. However, it is packed in a BSA. In this case, **Mod B** would still overwrite:

* **Mod A**
  * ~~Example.dds~~
* **Mod B**
  * Example.dds
* **Mod C**
  * Example.bsa {~~Example.dds~~}

### Load Order

Assets packed within BSAs overwrite based on the load order of their plugins.

* **Plugin A.esp**
  * Plugin A.bsa {~~Example.dds~~}
* **Plugin B.esp**
  * Plugin B.bsa {Example.dds}

## Porting LE mods to SE

The vast  majority of mods created for Skyrim LE (the 2011 version) can easily be  ported to Skyrim SE (2016 remaster). Many of them do not in fact need  any additional steps and can immediately be installed for SE.

* **Plugins** must be re-saved in the Creation Kit, a procedure that may seem daunting at first but can be completed within a minute.
* **Archives** must be extracted and potentially repacked. Attempting to run Skyrim SE with an active LE BSA will result in a crash on launch.
* **Textures** are usually fine and can be used in SE, although some may benefit from a different type of compression.
* **Meshes** can cause all kinds of issues up to and including crashes. They must be run through Cathedral Assets Optimizer or SSE NIF Optimizer.
* **Animations** are usually fine but may also be run through Cathedral Assets Optimizer.
* **SKSE Plugins** can be ported by people capable of recompiling and updating them in Visual  Studio if the original source code is publicly available.
* **ENBSeries presets** cannot be ported to SE as both the game’s as well as SE ENB shaders have changed.

All other file types, such as scripts, sounds, and interface (shockwave files) are generally safe to be used in SE.