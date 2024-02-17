---
title: "Plugin Basics"
weight:
type: docs
description: >
  About plugins (ESM, ESP, ESL).
---

## About Plugins

This article summarises some basic knowledge about **plugins**.

Mods (and the game data of the vanilla game) consists of two basic file types: **Plugins** and [assets](/skyforge/knowledge-base/asset-basics/).

**Plugins** with the extensions **.esm**, **.esp**, or **.esl** are a file type specific to the Creation Engine.* They can be created, viewed, and modified in the official [Creation Kit](/skyforge/tool-setup/creation-kit/) and the community tool [SSEEdit](/skyforge/tool-setup/sseedit/).

<font size=2>\**All of Bethesda Game Studios' games and Obsidian's Fallout New Vegas are developed in the Creation Engine.*</font>

Plugins populate the **load order**. Managing the load order and editing plugins for compatibility and consistency with each other is a major part of building a modded setup.

## Records

Plugins contain game data in the form of **records**. Each plugin can contain hundreds and thousands of records which are split up into a variety of categories. All vanilla records are defined in the five **official master files:**

- Skyrim.esm
- Update.esm
- Dawnguard.esm
- HearthFires.esm
- Dragonborn.esm

{{< alert color="info" >}} The first plugin contains data from the vanilla game. The third, fourth, and fifth contain data from the three DLCs. Update.esm is used for offical post-release patches, mostly to overwrite and modify Skyrim.esm.{{< /alert >}}

### Example

**Alvor** is the blacksmith from Riverwood whom you meet after completing the prologue. Since this NPC (Non-Player Character) was part of the vanilla game, he is <u>defined</u> in **Skyrim.esm**.

His NPC record defines Alvor's name, his appearance, voice, race, faction membership, inventory contents, outfit, and much more. Below, you can see the top of Alvor's NPC record when viewed in SSEEdit.

![Alvor Record](/Pictures/skyforge/knowledge-base/plugin-basics/alvor-record.png)

## Form IDs

Every **record** can be identified by its unique **Form ID**. Form IDs consist of 8 [hexadecimal](https://en.wikipedia.org/wiki/Hexadecimal) numbers (1-9 and A-F). The first two characters are the **Index** which changes depending on load order position while the remaining six characters are unique to the record.

Example: The Form ID for Alvor's NPC record is `00013475`.

### Index

Skyrim.esm <u>always</u> loads first so its Index stays `00` and it is always followed by Update.esm with the index `01`. In the Skyrim LE days, it was possible to only one *some* of the DLC, so the Index of the remaining master files depended on which you owned.

If you only owned the **Dragonborn** DLC, this would be your load order:

- <mark>[00]</mark> Skyrim.esm
- <mark>[01]</mark> Update.esm
- <mark>[02]</mark> Dragonborn.esm

In Skyrim SE, which contains all DLC, this is your load order:

- <mark>[00]</mark> Skyrim.esm
- <mark>[01]</mark> Update.esm
- <mark>[02]</mark> Dawnguard.esm
- <mark>[03]</mark> HearthFires.esm
- <mark>[04]</mark> Dragonborn.esm

{{< alert color="warning" >}}Because each Form ID can only be used once per plugin and each plugin has a unique Index, there can never be two identical Form IDs.{{< /alert >}}

### Plugin Limit

The two-character Index creates an important limitation: **The load order cannot exceed 256 ESM and ESP plugins.**

{{< alert color="info" >}}Why? Because the hexadecimal system has 16 unique characters and there are exactly 256 possible combinations of these characters for the two-character Index. The hexadecimal **FF** is the decimal **255**, so the maximum amount of plugins from 0 (00) to 255 (FF) is 256 ([see this table](/Pictures/skyforge/beginners-guide/hexadecimalchart.png) for a good visualisation).{{< /alert >}}

The load order limit can be circumvented in two ways:

1. Merging multiple smaller plugins together to create a single bigger one.
2. Using the ESL file format.

Since ESL plugins were added in Skyrim SE, merging has become largely redundant. ESLs will be discussed extensively further down on this page.

## Layers

SSEEdit visualises plugins as **layers** which makes it easy to understand interaction between plugins. Each plugin contains one version of a record (either the original or a copy) which is equal to one layer.

Below, you can see a record that is <u>defined</u> in Skyrim.esm and <u>modified</u> in Update.esm:

![Plugin Layers](/Pictures/skyforge/knowledge-base/plugin-basics/plugin-layers.png)

**The game only reads the final overwriting version of each record.**

Both Skyrim.esm and Update.esm modify the same record, but only the layer from Update.esm will be loaded into the game because it is loaded last. Any previous layers will be completely ignored.

### Implications

Because plugins overwrite each other according to the order they are loaded in and only one plugin can modify a record, it is important to ensure that the correct plugin is placed last.

**The correct load order is crucial for mods to function as intended.**

## Conflicts

A **conflict** occurs when multiple plugins modify the same record in different ways. While SSEEdit will visualise conflicts in alarming shades of red and orange, not all conflicts are actually harmful. In fact, most conflicts are fully intentional and indeed unavoidable.

Below, you can see a perfectly harmless *critical conflict* arising from the fact that both **Dawnguard.esm** and **HearthFires.esm** modified the same **Skyrim.esm** record in different ways:

![Critical Conflict](/Pictures/skyforge/knowledge-base/plugin-basics/critical-conflict.png)

### Patches

When two or more plugins make different modifications to the same record and you wish to keep (some) changes from all of them, you need to create a new **patch**. This means consolidating all desired changes in one final layer.

| **Master**   | **Plugin A** | **Plugin B** | **Patch** |
| ---------- | -------- | -------- | ----- |
| ~~*Original*~~ | <mark>Edit 1</mark> | ~~*Original*~~ | <mark>Edit 1</mark> |
| ~~*Original*~~ | ~~Edit 2~~ | <mark>Edit 3</mark> | <mark>Edit 3</mark> |
| ~~*Original*~~ | <mark>Edit 4</mark> | ~~Edit 5~~ | <mark>Edit 4</mark> |
| *Original* | *Original* | *Original* | *Original* |

**This is why <u>both</u> load order adjustments <u>and</u> patches are required for a functional setup.**

## Dependencies

When a plugin modifies a record defined in another plugin, a **dependency** is created.

Take our earlier example, Alvor: Any mod that changes his NPC record <u>requires</u> Skyrim.esm as a **master** because that is where the record originates. If Skyrim.esm were not present, this would create a *missing master* error which can create various problems, including crashes.

**All plugins must have their master files loaded <u>above them</u> at all times.**

## Plugin Types

There are three different types of plugins:

- **Elder Scrolls Plugin** (ESP) (ESP) are the most common file type. They count toward the 256 plugin limit and load at the bottom of the load order in *ESP space*.
- **Elder Scrolls Master** (ESM) plugins always load before all ESPs at the top of the load order in *ESM space*. They also count toward the 256 plugin limit and differ from ESPs primarily in how they handle *references*.
  - *Read more about [references](/skyforge/knowledge-base/references/).*
- **Elder Scrolls Light** (ESL) plugins typically load in *ESM space* at the top of the load order. They do <u>not</u> count toward the 256 plugin limit and have a smaller Form ID capacity.
  - *Read more about [ESL Plugins](/skyforge/knowledge-base/esl-plugins/).*

### Plugin Flags

The plugin type is defined by:

1. The file extension: .ESP, .ESM, .ESL.
2. The plugin flag: ESL, ESM.

{{< alert color="warning" >}}All ESMs have the ESM flag and all ESLs have the ESL flag. ESPs do not have a plugin flag.{{< /alert >}}

You can view **Plugin Flags** in SSEEdit:

![Plugin Flags](/Pictures/skyforge/knowledge-base/plugin-basics/plugin-flags.png)

### Hybrid Plugins

**Hybrid plugins** can be created by mixing plugin flags and file extensions:

- Plugins with the .ESP and .ESL file extensions can be ESM-flagged to be treated as ESMs (load in ESM space and able to unload temporary references).
- Plugins with the .ESP and .ESM file extensions can be ESL-flagged to be treated as ESLs (no longer count toward the plugin limit at the cost of a reduced Form ID budget).

### Load Order

The five official master files as well as any present [Creation Club](/skyforge/knowledge-base/creation-club/) plugins are hard-coded to always load at the top of the load order. They are followed by ESMs and ESPs.

- **Skyrim.esm** >> `ESM`
- **Unofficial Skyrim Special Edition Patch.esp** >> `ESM-flagged ESP`
- ***Vanilla Script MicroOptimizations.esl*** >> `ESM-flagged ESL`
- *Unofficial Skyrim Creation Club Content Patch.esl* >> `ESL`
- SkyUI.esp >> `ESP`
- *MCMHelper.esp* >> `ESL-flagged ESP`

{{< alert color="warning" >}}Plugins in ESM space (ESMs, ESLs, ESM-flagged ESPs) always load <u>above</u> and are overwritten by plugins in ESP space (ESPs, ESL-flagged ESPs).{{< /alert>}}