---
title: "Documentation"
weight: 3
type: docs
description: >
  Documentation for Skyrim Modding Essentials.
---

## Creation Club

**SSE Modding Essentials** does not require the full AE DLC, but it does include the four free Creations (Fishing, Survival, Rare Curios, Saints & Seducers) because they are required dependencies for the [Unofficial Skyrim Special Edition Patch](https://www.nexusmods.com/skyrimspecialedition/mods/266). They are located inside the "Creation Club Content" folder at the top of your mod order.

### Creation Organizer

For those who own more Creation and want to use them, I included the wonderful [Creation Organizer](https://www.nexusmods.com/skyrimspecialedition/mods/66329). In order for Creation Organizer to work, you need to have all creations you own in your default installation folder (that is, `Steam\steamapps\common\Skyrim Special Edition\Data`). If you just (re)installed the game, you may need to launch it once for your owned Creations to be downloaded.

You can "run" Creation Organizer by clicking the option shown below. MO2 will freeze up for a while, just let it do its thing.

![Creation Organizer](/Pictures/sme/creation-organizer.png)

By default, the JSON is set up to move all Creations you own into the "Creation Club Content" folder which already contains the four required Creations. If you want each Creation installed to its own folder, go to `Modding Essentials\Tools\Creation Organizer\` where you will find alternative JSONs. The second one is the default one from the mod page and the third is intended for Wabbajack lists (adding the [NoDelete] tag to each mod folder).

Pick whichever JSON you like and use it to overwrite the existing one inside `Modding Essentials\plugins\creation_organizer\`. Then run Creation Organizer again through the MO2 interface. Afterwards, you can delete the "Creation Club Content" folder.

## Modding Tools

The following tools are installed and configured for the SME Game Root folder:

- [SSEEdit](https://www.nexusmods.com/skyrimspecialedition/mods/164)
- [DynDOLOD 3](https://www.nexusmods.com/skyrimspecialedition/mods/68518) and [SSELODGen](https://stepmodifications.org/forum/topic/13451-xlodgen-terrain-lod-beta-94-for-fnv-fo3-fo4-fo4vr-tes5-sse-tes5vr-enderal-enderalse/)
- [Project New Reign - Nemesis Unlimited Behaviour Engine](https://www.nexusmods.com/skyrimspecialedition/mods/60033)
- [SSE NIF Optimizer](https://www.nexusmods.com/skyrimspecialedition/mods/4089)
- [Bethesda Archive Extractor](https://www.nexusmods.com/skyrimspecialedition/mods/974), recommended to be set as the default app for opening BSAs, very convenient!
- [Cathedral Assets Optimizer](https://www.nexusmods.com/skyrimspecialedition/mods/23316), including my basic profiles
- [NifSkope](https://github.com/niftools/nifskope), both Dev 7 and the elusive Dev 8
- [Octagon](https://www.nexusmods.com/skyrimspecialedition/mods/28773)
- [zEdit](https://github.com/z-edit/zedit/releases)
- [BethINI](https://www.nexusmods.com/skyrimspecialedition/mods/4875)
- [LOOT - Load Order Optimisation Tool](https://www.nexusmods.com/skyrimspecialedition/mods/1918)
- [Wrye Bash](https://www.nexusmods.com/skyrimspecialedition/mods/6837)
- [BodySlide and Outfit Studio](https://www.nexusmods.com/skyrimspecialedition/mods/201)
- [EasyNPC](https://www.nexusmods.com/skyrimspecialedition/mods/52313)

Terrain LOD generated with SSELODGen will be placed in `Skyrim Modding Essentials\Tools\xLODGen\Output\`. Move it from there into the mods folder. It is recommended to change the xLODGen output to a location *outside* your MO2 folder before generating terrain LOD.

Though BethINI is included, I did not regenerate the INI files. The SME profile in Mod Organizer 2 is using Skyrim's default INIs with the High preset. Profile-specific INI files are enable.

Make backups of your load order before running Wrye Bash. It may sometimes try to deactivate your plugins and reorder them alphabetically.

I added LOOT because it can be quite useful for curating your own load order and master list, but please do not just click "Sort" and expect your setup to be magically perfected.

> For more information for LOD generation, please check [Althro's guide](https://github.com/The-Animonculory/Modding-Resources/blob/main/DynDOLOD.md).

### MO2 Plugins

- [deorder's plugins](https://github.com/deorder/mo2-plugins)
- [LostDragonist's MO2 Plugins](https://www.nexusmods.com/site/mods/82)
- [Crash Log Tools](https://www.nexusmods.com/skyrimspecialedition/mods/66743)
- [NIF Preview](https://www.nexusmods.com/skyrimspecialedition/mods/69813)
- [LOOT Config Loader](https://www.nexusmods.com/skyrimspecialedition/mods/60864), see [Github](https://github.com/Exit-9B/LOOTConfigLoader/blob/main/README.md) for documentation
- [Creation Organizer](https://www.nexusmods.com/skyrimspecialedition/mods/66329)
- [Kezyma's Root Builder](https://www.nexusmods.com/skyrimspecialedition/mods/31720)
- [Kezyma's Profile Sync](https://www.nexusmods.com/skyrimspecialedition/mods/60690)

LOOT Preventifier (from LostDragonist's MO2 Plugins) was also included, but disabled by default.

Many of these plugins do nothing until they've been configured. Check their mod pages for details.

### SSEEdit

Generated cache for SSEEdit will be saved to a "cache" folder within the SSEEdit installation directory (`Modding Essentials\Tools\SSEEdit\`), and plugin backups will be saved to a "backups" folder within the same directory. The prompt which warns about making changes to plugins was disabled with the `-IKnowWhatImDoing` argument.

The QuickAutoClean exe was also added with the `-DontCache` argument in case you wish to clean the official master files (without this argument, the cleaning would nuke parts of Apocrypha).

I also installed [mator's xEdit Patching Framework](https://www.nexusmods.com/skyrim/mods/68617) and mator's [Automation Tools for TES5Edit](https://www.nexusmods.com/skyrim/mods/49373).

## ENBSeries

Since many people use ENB presets, I included a set of essentials:

- The latest enbseries binaries with a preconfigured enblocal.ini which you can use with any preset
- [Particle Patch for ENB](https://www.nexusmods.com/skyrimspecialedition/mods/65720) with [Fixed Skeever Dinner Meshes](https://www.nexusmods.com/skyrimspecialedition/mods/68481) and [Ghost Pile Seam Fix](https://www.nexusmods.com/skyrimspecialedition/mods/67841)
- [ENB Helper](https://www.nexusmods.com/skyrimspecialedition/mods/23174) with [ENB Helper Plus](https://www.nexusmods.com/skyrimspecialedition/mods/62743) and [ENB Input Disabler](https://www.nexusmods.com/skyrimspecialedition/mods/62796)

In the enblocal.ini, VSYNC is disabled because SSE Display Tweaks is used for VSYNC instead. The framelimit is turned off. If you want to limit your framerate, it is highly recommended to do so using SSE Display Tweaks. Finally, the hotkeys were adjusted, please check the "Hotkeys" section further down on this page for more information.

If you want to install an ENB, copy the three files from `SSE Modding Essentials\Tools\ENBSeries\` to `SSE Modding Essentials\Game Root\` (ignore the WABBAJACK_NOMATCH_INCLUDE). Then download your favourite preset and extract the preset files (enbseries.ini and the enbseries folder) into `SSE Modding Essentials\Game Root\` as well.

## Further Notes

**Please always be careful when adding mods and familiarise yourself with the existing setup first.** 

The configuration files for various mods were left untouched except for a few cases which are marked in the MO2 notes. Enable/disable settings based on your setup and preferences.

I included [Face Discoloration Fix](https://www.nexusmods.com/skyrimspecialedition/mods/42441) which fixes mismatched facegen at runtime. However, that doesn't mean you should no longer worry about facegen because if you let all your facegen conflicts be handled by the plugin there is a performance impact. For the love of Talos, regenerate your facegen! Refer to [Althro's Guide](https://github.com/The-Animonculory/Modding-Resources/blob/main/Regenerating%20Faces%20in%20the%20Creation%20Kit.md) if you are not sure how to do it.

### Modder's Tools

[More Informative Console](https://www.nexusmods.com/skyrimspecialedition/mods/19250) adds debugging functionality to the console. Click on any item, static, or NPC ingame to see their Base/Ref ID and other vital data which is vital for troubleshooting and fixing up your setup.

[QUI](https://www.nexusmods.com/skyrimspecialedition/mods/65343) not only includes [Stay At The System Page](https://www.nexusmods.com/skyrimspecialedition/mods/19832) for Skyrim 1.6, but also adds a menu through which you can access items added by mods, sorted by plugin, all of which is highly customisable. You can open the menu ingame with **F8** (the hotkey can be changed in the config file in MO2).

[Where In Special Edition Am I](https://www.nexusmods.com/skyrimspecialedition/mods/30907) adds a convenient method to determine your exact location ingame, at least until you have DynDOLOD set up in which case its MCM has the same feature.

### Hotkeys

The hotkeys for some of the mods/tools included in Modding Essentials were slightly tweaked in a way that I feel is more convenient. These tweaks assume that you are otherwise using the default hotkeys for quicksave/quickload (F5 and F9 respectively).

- **F7** toggles the ENB FPS counter
- **F8** opens the QUI ingame item browser
- **F9** is the default quickload
- **F10** opens the ENB GUI
- **F11** toggles the ENB effect