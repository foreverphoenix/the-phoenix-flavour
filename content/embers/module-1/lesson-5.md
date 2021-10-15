---
title: "Lesson 5: Load Order"
weight: 5
type: docs
no-list: false
description: >
 Plugins, their differences, and how to sort them.
---

## Overview

- WIP

## Basic Plugin Types

In the previous lesson, we had a closer look at the inner workings on plugins, how their records are organised and how they overwrite each other. This knowledge will now help us understand the differences between the various kinds of plugins.

There are three different plugin types as well as hybrid combinations of two or even all three of them that serve different purposes. Nevertheless, in their basic structure, all plugins are functionally identical across their various types. The differences are largely related to where they can be placed in the load order and the amount of records that they can store.

The most common file type for plugins is **ESP** (Elder Scrolls Plugin). When exporting changes from the Creation Kit (the official modding tool), this is the file type that the changes are saved in and almost all plugin-based mods make use of it. If you look at your current load order in Mod Organizer 2, you can see exactly one ESP plugin: SkyUI_SE.esp, displayed without any text decoration.

There are also **ESM** plugins (Elder Scrolls Master) which always load above the ESP plugins. In Mod Organizer 2, the official master files (Skyrim.esm, etc) are currently the only full ESM plugins present, displayed in ***bold italics***. They are also greyed out because their load order cannot be adjusted, they are hardcoded to always load first.

### 256 Plugin Limit

**The total number of ESM and ESP plugins in your load order cannot exceed 256 plugins.** This is due to the hexadecimal system used to define them: Each plugin's Index (the first two characters in their form ID) is made up of a combination of two symbols. The hexadecimal system has 16 unique characters and for two symbols there are exactly 256 possible combinations from 00 to FF ([see this table](https://files.renoise.com/forum/uploads/5358-hexadecimalchart1.png)). The hexadecimal FF is the decimal 255, so the maximum amount of plugins is 0 to 255 = 256.

In Skyrim LE the plugin limit could be overcome by merging the records of multiple plugins into a single one. However, in Skyrim SE plugin merging has become essentially redundant for all but the largest of load orders thanks to the new ESL format of plugins introduced with the 2015 engine update.

## ESL Plugins

Among the major differences between Skyrim LE and Skyrim SE are the new **.ESL** (Elder Scrolls Light) plugins. They were created for Bethesda's "Creation Club" in order to potentially add a large amount of additional plugins for various "creations".

All ESL plugins have the Index `FE:xxx`. The hexadecimal FE is the decimal 254, so all ESL plugins load in plugin slot 254. This is possible because their Index was extended to the third, fourth, and fifth character in their eight character form ID: An ESL's Index could be `FE:000` or `FE:08F`. The limit for ESLs is a whopping **4096** plugins.

The downside of ESLs is that they can store fewer records. Remember that each record must have a unique form ID and ESLs only have three digits left for a combination of the 16 hexadecimal characters instead of six like ESPs or ESMs. This means they can store 4096 unique form IDs which is still more than enough for all but the largest of mods. Many separate ESL plugins are infinitely easier to handle than large plugin merges (imagine having many small drawers for your various screws instead of dumping all of them into a single big one).

Additionally, this limit only affects *new* records, records defined in the ESL plugin. There is no limit on how many records defined in *other* plugins they can hold. Many mods function mostly by editing existing (vanilla or mod-added) records and add few or no new records of their own. These types of plugins are especially suited to being ESL-ified.

### ESL Load Order

Regular **.ESL** plugins are always forced between ESM and ESP plugins in the load order. Mod Organizer 2 displays them in *italics* like our *Disable USSEP Book.esl* which we created in the previous lesson. While the position of plugins in the load order can normally be manipulated via drag and drop, you will notice that you can change the order of the two ESP plugins at the bottom, but are unable to move them above the ESL or ESMs.

## Hybrid Plugins

You likely already noticed it: Most plugins in our load order right now are not consistent with the plugin types we just discussed. For example, the **Unofficial Skyrim Special Edition Patch.esp** is displayed in **bold** like an ESM but has the ESP file extension. And *Skyrim Landscape and Water Fixes - Light Sources.esp* is displayed in *italics* like an ESL plugin but also has the ESP file extension.

The type of a plugin is determined by two factors: File extension (.esm, .esp, .esl) and plugin flag. For example, a regular ESP has the .ESP extension and no plugin flag, it can be placed anywhere below the ESM and ESL plugins, and counts against the 256 plugin limit.

However, file extensions and plugin flags can be adjusted to allow for different combinations beyond the three main plugin types (ESM, ESP, ESL).

This is where **hybrid plugins** come into play.

### ESP-FE Plugins

If a plugin is rather small it may be far more practical to turn it into an ESL. Unfortunately, a full ESL (a .esl plugin with the ESL flag) will be forced to load below the ESMs and above the ESPs. In the case of conflicts between it and any ESPs, it cannot simply be moved below the other plugin. This is why full ESLs are relatively rare and most people use so-called **ESL-ified ESPs** or **ESP-FE plugins** instead. These plugins have the .ESP file extension but were flagged as ESL in SSEEdit.

Flagging ESPs as ESLs is a very common step in the assembly of a mod list, especially if there are enough ESMs and ESPs in the load order to approach the 256 plugin limit. Note that you cannot simply change the file extension of an ESP to .ESL since these two plugin types have differently structured form IDs. You need to first *renumber* the ESP's form IDs in SSEEdit before you can add the ESL flag to it (also in SSEEdit). How this works will be explained in more detail later on.

An ESP-FE plugin can be turned into a full ESL by renaming its file extension from ESP to ESL which is exactly what we did to the *Disable USSEP Book.esl* plugin in the previous lesson.

### Light Master Plugins

But ESP plugins are not the only plugin type that can be flagged as ESL: You can do the same thing with ESMs. If a plugin serves as a mod resource or is supposed to load very early for other reasons, it is convenient to use the ESM format which automatically forces it near the top. If that plugin is also very small, then flagging it as ESL in SSEEdit will save another ESP/ESM plugin slot. This requires the same steps as creating an ESP-FE plugin (renumbering form IDs and flagging as ESL in SSEEdit).

### ESM-ified ESPs

An ESP that contains records intended to load early in the mod order can also simply be ESM-ified by adding the ESM flag to it in SSEEdit. This requires no changes to the form IDs. It will have the .ESP file extension, load with all other ESMs near the top, and count toward the ESP/ESM plugin limit.

### ESM-ESP-ESL Plugins

And of course there is the combination of all three file types: An ESP plugin flagged as ESM to load near the top of the load order *and* as ESL to use ESL plugin space so as not to count toward the ESP/ESM plugin limit. One such plugin is ***Landscape and Water Fixes.esp*** in our load order.

## Basic Load Order

Plugins are always ordered as follows:

- Official Master Files (ESM)
- Creation Club Content (ESL, Light Master)
- All ESM-flagged plugins (ESM, ESM-ified ESP, Light Master, ESM-ESP-ESL)
- All ESL plugins (ESL)
- All ESP plugins (ESP, ESP-FE)

In Mod Organizer 2, you can generally tell file types apart by their file extensions and text decoration in the load order (right pane):

- ***Skyrim.esm*** >> `ESM`
- ***Update.esm*** >> `ESM`
- ***Dawnguard.esm*** >> `ESM`
- ***HearthFires.esm*** >> `ESM`
- ***Dragonborn.esm*** >> `ESM`
- ***Unofficial Skyrim Special Edition Patch.esp*** >> `ESM-ified ESP`
- ***Landscape and Water Fixes.esp*** >> `ESM-ESP-ESL`
- *Disable USSEP Book.esl* >> `ESL`
- *Skyrim Landscape and Water Fixes - Light Sources.esp* >> `ESP-FE`
- SkyUI_SE.esp >> `ESP`

You can tell apart hybrid plugins in ESM space by looking at the **Flags** column where a yellow dot marks any ESL-flagged ESM or ESP plugins. In regular ESP space, you can easily recognise ESL-ified ESPs because they are displayed in *italics*.

![ESM-ESP-ESL Plugin](/Pictures/embers/module-1/ESM-ESP-ESL.png)

## The Rule of One

A plugin consists of many records. If a record exists in more than one plugin, the copy from the record that is loaded lower in the load order will be used by the game. This is also called the **rule of one**. In the example from Lesson 4 (picture below), the USSEP contains a copy of a record from Skyrim.esm as a new layer. In the new layer, the USSEP makes an edit to the text of a note. Because the USSEP is below Skyrim.esm in the load order, its version of the record will be the one used by the game.

Since modding means editing the base game, it makes sense that the official master files are all the way at the top so that all other plugins are placed below them and can overwrite. It also means that it is quite relevant where in the load order all the other plugins are placed because they affect each other in the same way. **Plugins overwrite each other in the order they are placed in.**

![Plugin Layers](/Pictures/embers/module-1/ussep-book-record-details.png)

## Plugin Dependencies

Plugins can edit existing records, add new ones, or do a mix of both. If a plugin edits an existing record, it will depend on the plugin that the existing record was defined in. For example, in the image above the USSEP edits a record defined in Skyrim.esm and therefore requires Skyrim.esm to be active in the load order. In other words: Skyrim.esm is a master to the USSEP. **Plugins must always be placed *below* their masters so they can properly overwrite.**

All plugins need to have at least Skyrim.esm as a master file, but they can also depend on other plugins, official or mod-added. This is the case with **Landscape and Water Fixes.esp** which depends on the **Unofficial Skyrim Special Edition.esp**. If you uncheck the USSEP's plugin in the load order, Mod Organizer 2 will instantly warn you about the missing master. The notification in the upper right corner will light up and show the warning if you click on it.

![SLAWF Missing Master](/Pictures/embers/module-1/slawf-missing-master.png)

Alternatively, you can hover over the **Landscape and Water Fixes.esp** which has now been marked with a small warning sign icon to see all its dependencies and which master is missing.

Since the Landscape and Water Fixes plugin requires the USSEP plugin directly, we know that it must be placed *below* it in the load order as plugins are always placed below their masters. Be sure to re-enable the USSEP plugin and to place it above the Landscape and Water Fixes plugin before proceeding with the next step.

> It should be noted that Skyrim SE, unlike Skyrim LE, does not *always* immediately crash on launch when a master is missing. However, a missing master will still cause critical errors and has to be fixed.
