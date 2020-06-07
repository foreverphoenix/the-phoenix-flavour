---
title: "New Music"
weight: 8
type: docs
description: >
  Instructions for mods that add new music tracks plus a merged patch.
---

Music tracks are added for certain parts of Skyrim through the **Music Type** records. They are split into multiple categories, including MUSCombat and different MUSExplore / MUSDiscover types. While mods that add additional music tracks use their own records for the new tracks, they need to add those records to the **Music Type** lists. Adding more than one music mod at a time will most likely require you to create a patch (if both mods add to the same Music Type) and forward all music tracks into the new plugin. This is as simple as using drag-and-drop.

For this section, I am including my personal favourite music overhauls plus a merged patch for them. If you are not comfortable editing the merged patch in SSEEdit, you must install all mods listed below and the patch. Alternatively you can install just one of the mods in which case the merged patch will not be necessary.

## The Northerner Diaries - Immersive Edition

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/28108?tab=files)

- **Main Files:** The Northerner Diaries - Skyrim and Solstheim

## Still - Skyrim Inspired Music

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/19401?tab=files)

- **Main Files:** Still - ESP Version

## Melodies of Civilization - Skyrim Fan-Made Music

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/30014?tab=files)

- **Main Files:** Melodies of Civilization 1.01

## Hun Lovaas - Skyrim Fan-Made Combat Music

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/16123?tab=files)

- **Main Files:** Hun Lovaas - ESP version

## Musical Lore - Soundtrack Mod by Nir Shor

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/3200?tab=files)

- **Main Files:** Musical Lore V1.2

## Phoenix - Merged Music Patch

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/26092?tab=files)

- **Main Files:** Phoenix - Merged Music Patch

## Additional Instructions

#### Mod & Load Order

- Place all mods including the patch below the **SOUNDS & MUSIC** separator.
- Place the plugins in the order you installed them in below the other audio mods:

![Music Mods LO](/Pictures/customisation/music_mods_lo.png)

#### ESL Flags

The patch itself depends on the **main files** of each music mod which are (with the exception of Melodies of Civilisation) all regular ESPs. However, now that the patch is present in your load order, you can easily renumber form IDs for the other plugins and flag them as ESL.

- Run **SSEdit** through Mod Organizer 2.
- Click **OK** in the plugin selection window to load all your plugins.
- Wait for SSEEdit to return `Background Loader: finished`.
- Right-click and select **Compact FormIDs for ESL** for the following plugins:
  - Northerner Diaries in Skyrim.esp
  - NirShor-MusicalLore.esp
- There will be a warning, click **Yes**.
- Flag the following plugins as ESL (Record Header >> Record Flags >> Check ESL):
  - Northerner Diaries in Skyrim.esp
  - Still.esp
  - Hun Lovaas.esp
  - NirShor-MusicalLore.esp
- Close SSEEdit and click **OK** to save your changes.

> Note that the merged patch will show up as edited which it should be. The renumbered FormIDs for Northerner Diaries in Skyrim.esp and NirShor-MusicalLore.esp were updated in the patch.


