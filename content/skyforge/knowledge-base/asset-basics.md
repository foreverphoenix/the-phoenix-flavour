---
title: "Asset Basics"
weight:
type: docs
description: >
  About assets (loose and packed).
---

## About Assets

This article summarises some basic knowledge about **assets**.

Mods (and the game data of the vanilla game) consists of two basic file types: [Plugins](/skyforge/knowledge-base/plugin-basics/) and **assets**.

### Asset Types

All asset types must be located in the **data folder** in a top-level folder of the same name (i.e., `\Skyrim Special Edition\Data\Textures\`). The following file types are recognised by the game:

- **Textures** (.DDS)
- **Meshes** (.NIF)
- **Scripts** (.PEX)
- **Animations** (.HKX)
- **Interface** (.SWF)
- **SKSE\Plugin** (.DLL)
- **Sound\Voice** (.FUZ)
- **Sound\FX** (.WAV)
- **Music** (.XWM)

<font size=2>*The list is not 100% complete, but these are the important ones.*</font>

Different asset types handle very differently from each other (unlike plugins) and more time is required to learn how to substantially modify them. On the other hand, sound design, 3D modelling, etc, are (again, unlike plugins) widely applicable skills and not unique to Bethesda's Creation Engine.

Generally speaking, you do not need to become as adept at modifying different types of assets as you do at modifying plugins in order to build a solid setup.

## Bethesda Softworks Archives

Assets can be present in two forms: as **loose files** or **BSA-packed**. Loose files <u>always</u> overwrite packed assets.

**Bethesda Softworks Archives** (BSA) are essentially 7ZIP or WinRAR archives for Creation Engine assets. All vanilla assets are packed into the 17 BSAs in the data folder which are compressed to save space. Many mods are also published with their assets packed into a BSA.

{{< alert color="warning" >}}In Skyrim SE, BSAs have a size limit of **2GB**.{{< /alert >}}

### BSA Types

There are two types of BSAs:

- Example.bsa
- Example - Textures.bsa

Obviously, the latter type is intended specifically for textures. Use the regular type for all other kinds of assets.

BSAs can be **compressed** or **uncompressed**. Looking at the vanilla BSAs, you will notice that archives containing textures and meshes are *compressed* while all others are *uncompressed*. I recommend mirroring this logic when creating new BSAs.

{{< alert color="info" >}}There are also some additional flags uncovered by fireundubh [as documented here](https://wiki.fireundubh.com/skyrim/bsa-flags).{{< /alert >}}

### Loading BSAs

**A BSA always requires a plugin with the same name to be loaded.**

*Example.esp* (or ESL/ESM) can load *Example.bsa* and *Example - Textures.bsa*, but no more than that. If the name does not match exactly the BSA will not be loaded. The plugin does not need to have any content, it can be an empty 'dummy' (in which case it should ideally be an ESP-FE).

{{< alert color="info" >}}The vanilla BSAs are actually loaded via the **Skyrim.ini** file and it should be *technically* possible to load additional BSAs by adding them to the INI. However, this is not particularly convenient so it is not done.{{< /alert >}}

### Manipulating BSAs

You can preview BSAs through Mod Organizer 2 or with [Bethesda Archive Extractor](/skyforge/tool-setup/bae/). Different ways of extracting BSAs are described [here](/skyforge/modding-resources/extracting-bsas/) while creating a **Cathedral Assets Optimizer** profile for re-packing BSAs is detailed [here](/skyforge/tool-setup/cao/#create-bsa-profile).

Unlike Fallout 4, you do not have to worry about massive performance drops with loose files over archived ones. The only files you should <u>never</u> unpack are `\lodsettings\example.lod` files because the game only recognises them when they are in a BSA.

## Mod Order

Similar to how plugins overwrite each other according to their placement in the **load order**, so do assets overwrite each other according to their placement in the **mod order**.

The mod order is a concept created by Mod Organizer 2 and its *virtual data folder* which prevents assets from irrevocably overwriting and replacing each other by placing them in separate folders.

{{< alert color="success" >}} **The mod order is functionally identical to the load order:** If multiple mods [plugins] contain different versions of the same asset [record], the mod [plugin] that is placed lowest will win the conflict and overwrite.{{< /alert >}}

### BSAs & Load Order

As a consequence of being attached to plugins, **BSAs adhere to load order** rather than mod order. This means <u>assets packed into BSAs overwrite each other in the order of their plugins</u>.

It makes sense to BSA-pack assets from mods that serve as a baseline intended to be overwritten. On the flipside, assets from mods that should generally overwrite are best kept as loose files.

You may also want to extract an archive in order to be able to compare its assets to other assets in your mod order. [NifSkope](/skyforge/tool-setup/nifskope/), for example, can only load loose textures and meshes, not BSA-packed ones.

### Archives & Plugins

If you have two archives or plugins *with the same name*, the one from the mod lower in the load order will overwrite and replace the other. BSAs and ESPs/ESMs/ESLs are essentially a type of asset as well and adhere to the mod order.