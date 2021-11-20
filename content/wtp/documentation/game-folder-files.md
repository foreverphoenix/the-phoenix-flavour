---
title: "Game Folder Files"
weight: 1
type: docs
description: >
  All files that need to be moved into the root folder manually.
---

While regular mods for Bethesda games are installed into the **data** folder, there are some additional tools that belong into the **root** folder. These are not automatically moved by Wabbajack. Instructions for them are included in the **Installation** setup, this page merely serves as an overview over the files in question and their purpose.

> WTP does not use the Stock Game Folder system and likely never will.

### Fallout 4 Script Extender

The [Fallout 4 Script Extender (F4SE)](http://f4se.silverlock.org/) is essential to modding Fallout 4 and required by many mods. Its executable and DLLs have to be inside the root folder.

- `f4se_1_10_163.dll`
- `f4se_loader.exe`
- `f4se_steam_loader.dll`

### xSE Plugin Preloader

The [xSE Plugin Preloader F4](https://www.nexusmods.com/fallout4/mods/33946) is required for Buffout.

- `IpHlpAPI.dll`
- `xSE PluginPreloader.xml`

### Buffout 4 TBB Redist

[Buffout 4](https://www.nexusmods.com/fallout4/mods/47359) requires the TBB library, a small plugin that needs to be placed in the root folder.

- `tbbmalloc.dll`

### F4 Creation Kit Fixes

[F4 Creation Kit Fixes](https://www.nexusmods.com/fallout4/mods/51165) are mostly installed for my benefit for when I do have to hop into the CK.

- `\Data\F4CKFixes\`
- `fallout4_test.ini`
- `tbb.dll`
- `winhttp.dll`

### ENBSeries Binaries

The [ENBSeries for Fallout 4](http://enbdev.com/download_mod_fallout4.htm) binaries, required for ENB presets to work.

- `d3d11.dll`
- `d3dcompiler_46e.dll`

### enblocal.ini

My personal enblocal.ini with customised hotkeys.

- `enblocal.ini`

### FallOpt ENB

The [FallOpt ENB](https://www.nexusmods.com/fallout4/mods/55662) preset.

- `\enbseries\`
- `enbseries.ini`