---
title: "Step 9: Load Order"
weight: 9
type: docs
description: >
  Placeholder.
---

## Basic Plugin Types

In the previous step, we had a closer look at the inner workings of plugins, how their records are organised and how they overwrite each other. This knowledge will now help us understand the differences between the various *types* of plugins as well as how to manage them.

There are three different plugin types as well as hybrid combinations of two or even all three of them that serve different purposes. Nevertheless, in their basic structure, all plugins are functionally identical across their various types. The differences are largely related to where they can be placed in the load order and the amount of records that they can store.

The most common file type for plugins is **ESP** (Elder Scrolls Plugin). When exporting changes from the Creation Kit (the official modding tool), this is the file type that the changes are saved in and almost all plugin-based mods make use of it. If you look at your current load order in Mod Organizer 2, you can see exactly one ESP plugin: `SkyUI_SE.esp`, displayed without any text decoration.

There are also **ESM** plugins (Elder Scrolls Master) which always load above the ESP plugins. In Mod Organizer 2, the official master files (Skyrim.esm, etc) are currently the only full ESM plugins present, displayed in ***bold italics***. They are also greyed out because their load order cannot be adjusted, they are hardcoded to always load first.

### 256 Plugin Limit

**The total number of ESM and ESP plugins in your load order cannot exceed 256 plugins, including the official master files.** This is due to the hexadecimal system used to define them: Each plugin's Index (the first two characters in their form ID) is made up of a combination of two symbols which in turn is based on their load order. The hexadecimal system has 16 unique characters and for two symbols there are exactly 256 possible combinations from 00 to FF ([see this table](https://files.renoise.com/forum/uploads/5358-hexadecimalchart1.png)). The hexadecimal FF is the decimal 255, so the maximum amount of plugins from 0 (00) to 255 (FF) is 256.

In Skyrim LE the plugin limit could be overcome by merging the records of multiple plugins into a single one. However, in Skyrim SE plugin merging has become essentially redundant for all but the largest of load orders thanks to the new ESL format of plugins introduced with the 2016 engine update.

## ESL Plugins

**ESL** (Elder Scrolls Light) plugins are among the most important features of Skyrim SE. They were initially made for Bethesda's Creation Club in order to potentially add a large amount of additional plugins for various Creations.

All ESL plugins have the Index `FE:xxx`. The hexadecimal FE is the decimal 254, so all ESL plugins load in plugin slot 254. This is possible because their Index was extended to the third, fourth, and fifth character in their eight character form ID: An ESL's Index could be `FE:000` or `FE:08F`. The limit for ESLs is a whopping **4096** plugins.

The downside of ESLs is that they can store fewer records. Remember that each record must have a unique form ID and ESLs only have three digits left for a combination of the 16 hexadecimal characters instead of six like ESPs or ESMs. This means they can store 4096 unique form IDs of which the first 2048 are reserved by the engine. The remaining 2048 slots are still more than enough for small to medium size mods. Many separate ESL plugins are infinitely easier to handle than large plugin merges (imagine having many small drawers for screws of differents types and sizes instead of dumping all of them into a single big one).

Additionally, this limit only affects *new* records, i.e., records defined in the ESL plugin. There is no limit on how many records defined in *other* plugins they can hold. Many mods function mostly by editing existing (vanilla or mod-added) records and add few or no new records of their own. These types of plugins are especially suited to being ESL-ified.

### ESL Load Order

Regular **ESL** plugins are always forced between ESM and ESP plugins in the load order. Mod Organizer 2 displays them in *italics* like our *Disable USSEP Book.esl* which we created in the previous step. While the position of plugins in the load order can normally be manipulated via drag and drop, you will notice that you can change the order of the two ESP plugins at the bottom, but are unable to move them above the ESL or ESMs.

## Hybrid Plugins

You likely already noticed it: Most plugins in our load order right now are not consistent with the plugin types we just discussed. For example, the **Unofficial Skyrim Special Edition Patch.esp** is displayed in **bold** like an ESM but has the ESP file extension. And *Skyrim Landscape and Water Fixes - Light Sources.esp* is displayed in *italics* like an ESL plugin but also has the ESP file extension.

The type of a plugin is determined by two factors: File extension (.esm, .esp, .esl) and plugin flag. For example, a regular ESP has the .ESP extension and no plugin flag, it can be placed anywhere below the ESM and ESL plugins, and counts against the 256 plugin limit.

However, file extensions and plugin flags can be adjusted to allow for different combinations beyond the three main plugin types (ESM, ESP, ESL).

This is where **hybrid plugins** come into play.

### ESP-FE Plugins

If a plugin is rather small it may be far more practical to turn it into an ESL. Unfortunately, a full ESL (a .esl plugin with the ESL flag) will be forced to load below the ESMs and above the ESPs. In the case of conflicts between it and any ESPs, it cannot simply be moved below the other plugin. This is why full ESLs are relatively rare and most people use so-called **ESL-ified ESPs** or **ESP-FE plugins** instead. These plugins have the .ESP file extension but were flagged as ESL in SSEEdit.

Flagging ESPs as ESLs is a very common step in the assembly of a mod list, especially if there are enough ESMs and ESPs in the load order to approach the 256 plugin limit. Note that you cannot simply change the file extension of an ESP to .ESL since these two plugin types have differently structured form IDs. You need to first *renumber* the ESP's form IDs in SSEEdit before you can add the ESL flag to it (also in SSEEdit). How this works will be explained in more detail later on.

An ESP-FE plugin can be turned into a full ESL by simply renaming its file extension from .ESP to .ESL which is exactly what we did to the *Disable USSEP Book.esl* plugin in the previous step.

### Light Master Plugins

Plugins can also be flagged as ESMs. If a plugin is very small, but should load very early for whatever reason, it is convenient to create an ESL and flag it as an ESM. This will save another ESP/ESM plugin slot though of course at the cost of record space. The resulting plugin will be forced to load near the top of the load order with all other ESMs.

Most Creations come with Light Master plugins, like ***ccbgssse037-curios.esl***. Creations are hardcoded to load below the official master files and above any other plugins.

### ESM-ified ESPs

An ESP that contains records intended to load early in the mod order can also simply be ESM-ified by adding the ESM flag to it in SSEEdit. This requires no changes to the form IDs. It will have the .ESP file extension, load with all other ESMs near the top, and count toward the ESP/ESM plugin limit. This is the case with the **Unofficial Skyrim Special Edition Patch.esp**.

### ESM-ESP-ESL Plugins

And of course there is the combination of all three file types: An ESP plugin flagged as ESM to load near the top of the load order *and* as ESL to use ESL plugin space so as not to count toward the ESP/ESM plugin limit. One such plugin is ***Landscape and Water Fixes.esp*** in our load order.
