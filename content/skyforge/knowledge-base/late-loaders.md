---
title: "Late Loaders"
weight:
type: docs
description: >
  About the late loader plugins and how to handle them.
---

## About Late Loaders

**Late loaders** are plugins that are very likely to be overwritten by ITMs from other plugins and should be placed low (late) in the load order to win those conflicts.

{{< alert color="info" >}}I recommend reading the article on [Plugin Basics](/skyforge/knowledge-base/plugin-basics/) first.{{< /alert >}}

On mod pages, you will often see instructions to place plugins low or even last in the load order. This is a band-aid fix to avoid the plugin from being overwritten; no plugin actually has to "load last" to be work properly. What is important is that its vital changes are present in the final layer of the respective record.

### ITM Conflicts

Late loaders are almost always plugins that modify parent CELL or Worldspace records. These records are different from others in that they are *nested*: A Worldspace record (like *Tamriel*, the Skyrim overworld) contains various exterior CELLS which, in turn, contain [references](/skyforge/knowledge-base/references/).

**Any mod which modifies references contains ITMs\* of the parent CELL and Worldspace records.**

<font size=2>\**ITMs, or identical-to-master records, are unmodified copies of the original record.*</font>

This is why it is possible for a mod that adds a beehive to create a visual bug in a nearby river because its ITM of the affected CELL record is overwriting a water overhaul's change to water flow:

![RW2 Bees](/Pictures/skyforge/knowledge-base/late-loader/rw2-ohgodbees.png)

### Recognising Late Loaders

A typical late loader modifies records in Worldspace or CELL records.

Worldspace record edits are actually quite rare: They are usually found in water or map overhauls and very rarely in lighting mods (specifically *Lux*). CELL record edits are a lot more common: Water and lighting overhauls in particular will modify hundreds of CELL records.

**The following mods are typical late loaders:**

- Lighting overhauls like *Lux*
- Water overhauls like *Realistic Water Two* or *Water for ENB*
- Map overhauls like *A Clear World Map for Skyrim and Other Worlds* or *Flat World Map Framework*

Generally speaking, <mark>a mod that modifies many Worldspace or CELL records qualifies as a **late loader**</mark> because they are easily overwritten by ITMs from other mods. In such cases, creating patches to overwrite would be unnecessary work and keeping the plugins at the bottom of your load order is a better solution.

## Managing Late Loaders

I strongly recommend *against* blindly following mod page instructions to load a plugin last as this is often the mod author's attempt to prevent the user's inexperience from breaking the mod.

Instead, review the plugin in SSEEdit (as you always should) and determine whether it qualifies as a late loader. Those should then be placed below all other plugins.

**Any output plugins (Synthesis, DynDOLOD, etc) must still load <u>below</u> late loaders.**

### CELL Record Overwrite

Placing **late loaders** at the bottom of the load order only works if they are overwriting ITMs and not other late loaders. However, conflicts in CELL and Worldspace records are still very possible (and not uncommon), so patches are required.

To manage such conflicts I keep a **CELL Record Overwrite** plugin right below my late loaders. This plugin consists exclusively of Worldspace and CELL records, merging edits from multiple mods.

{{< alert color="info" >}}Naturally you can also use a unified **Conflict Resolution Patch.esp** at the bottom of your load order to resolve such issues. The point is that loading plugins late is not always the solution. Having to manually create a patch is often unavoidable.{{< /alert >}}

For example, below you can see a three-way conflict resolved in the CELL Record Overwrite:

![CELL Record Overwrite](/Pictures/skyforge/knowledge-base/late-loader/cell-record-overwrite.png)