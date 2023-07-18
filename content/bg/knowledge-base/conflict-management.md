---
title: "Conflict Management"
weight:
type: docs
description: >
  About different types of conflicts and how to address them.
---

## About Plugin Conflicts

This article outlines in general terms how **conflicts** should be managed.

{{< alert color="info" >}}I recommend reading the article on [Plugin Basics](/bg/knowledge-base/plugin-basics/) first.{{< /alert >}}

**Conflicts** occur when two or more plugins modify the same record in different ways. Because of how plugins are structured it is very possible and indeed normal for plugins to interact with each other, even if they seem to have wildly different purposes.

While <u>unintentional</u> conflicts can break mods and the game in various ways, most conflicts are <u>intentional</u> and require no intervention at all. One of the most important steps in building a load order is managing conflicts accordingly.

{{< alert color="info" >}}If you are interested in why this step fails to mention LOOT, you can read up on my opinion on the tool [here](/bg/knowledge-base/phoenix-on-loot/).{{< /alert >}}

### Conflict Management Tool

The ideal tool for viewing and addressing conflicts is [SSEEdit](/bg/tool-setup/sseedit/) which allows you to compare and modify multiple plugins at the same time (unlike the Creation Kit). It is excellent at visualising plugin interaction.

You can find conflicts easily by [applying a filter](/bg/additional-modules/filter-for-conflicts/).

## Types of Conflicts

There are three types of conflicts:

1. **Harmless conflicts** require no intervention because all desired changes are already present in the final layer.
2. **Load order conflicts** occur when all desired changes are in a layer that is not yet loaded last. In this case, the plugin simply needs to be repositioned.
3. **Complex conflicts** occur when multiple different layers contain desired changes which must be merged into a final layer (patch).

Managing conflicts requires you to understand (roughly) what a given change in a record *does* and to then determine whether or not a resulting conflict is harmful.

### Harmless Conflicts

Conflict management largely boils down to applying *common sense*.

For example, the mod [Relighting Skyrim](https://www.nexusmods.com/skyrimspecialedition/mods/8586) (a lighting overhaul if the name did not give it away) conflicts with **Update.esm** in multiple records:

![RS Update Conflict](/Pictures/bg/core-module/rs-update-conflict.png)

Since Update.esm is a *master* to RelightingSkyrim_SSE.esp and the latter literally exists to modify the former, it is a pretty safe bet that these conflicts are perfectly intentional and harmless.

{{< alert color="info">}}Conflicts arising when a plugin overwrites one of its masters is almost always intentional.{{< /alert >}}

More generally, you can also assume that a lighting overhaul's changes to light-related records are intentional, a water overhaul's changes to water-related records are intentional, and so forth.

### Load Order Conflicts

Many records are nested within other records: For example, [references](/bg/knowledge-base/references/) are contained within CELL records. If a plugin modifies or adds a reference, it must also include a copy of the CELL record, even if it does not modify it.

As a result, CELL records are often present as **ITMs** (Identical to Master) in multiple plugins which increases the risk of accidentally overwriting a modified layer of the record. You can see an example below:

![Load Order Conflict](/Pictures/bg/core-module/worldspace-conflict.png)

Here, an <u>intentional</u> change from Realistic Water Two is <u>unintentionally</u> being reverted to vanilla by Relighting Skyrim.

The solution is to load Realistic Water Two *below* Relighting Skyrim.

{{< alert color="info" >}}Conflicts arising from a plugin's edits being reverted to vanilla by another plugin are usually unintentional and can be resolved by swapping the load order.{{< /alert >}}

Mods that modify **CELL** records (like water and lighting overhauls) are best kept near the bottom of the load order as **late loaders** to minimise the chances of their edits being unintentionally reverted to vanilla and to keep patching to a minimum.

### Complex Conflicts

Data in plugins is not particularly self-contained and a single record usually affects a variety of things. Take NPC records: They determine the NPC's name, appearance, factions, traits, inventory, outfit, and much more. Mods that overhaul NPC appearance will inevitably clash with mods that change the contents of their inventory.

Below, you can see a simple example of two mods modifying a WRLD record:

![RW2 NGIC Conflict](/Pictures/bg/core-module/rw2-ngic-conflict.png)

Merely changing the load order would make one mod or the other work, but never both. A **patch** is required to add another layer into which all desired changes can be forwarded.

![RW2 NGIC Conflict Resolved](/Pictures/bg/core-module/rw2-ngic-resolved.png)

{{< alert color="info" >}}Conflicts arising from multiple plugins making different changes to the same records typically require a patch.{{< /alert >}}

Note that "making stuff green" in SSEEdit is not <u>always</u> the correct solution and indeed it is not always possible. You may recall that in the *harmless conflict* example SSEEdit was still displaying the record in bright red to show a conflict was happening.

**Rather than focusing on making SSEEdit look green, focus on forwarding all desired changes into the final layer.**

*That being said, it is easier to work with a large load order if you can avoid checking the same conflicts repeatedly. This is where [ModGroups](/bg/knowledge-base/modgroups/) come in handy.*