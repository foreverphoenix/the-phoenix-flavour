---
title: "Max Height Data"
weight:
type: docs
description: >
  About the Max Height Data (MHDT) value in plugins.
---

## The MHDT Field

**Max Height Data (MHDT)** is a possible value that can be set in **CELL** and **WRLD** (Worldspace) records. It may vary between plugins if it is not missing entirely and causes conflicts that have no obvious solution.

{{< alert color="success" >}}**TL;DR:** Max Height Data conflicts can be mostly disregarded. Ideally you would let the value from the USSEP or (when present) from DynDOLOD/Occlusion overwrite.{{< /alert >}}

In many Skyrim.esm records the field is left empty while the DLC add a value:

![MHDT Tamriel](/Pictures/skyforge/knowledge-base/max-height-data/mhdt-tamriel.png)

Certain mods in turn forward one of the values from the official master files, add their own, or leave the field empty again. How should these conflicts be addressed?

### What does MHDT do?

The following is a quote from Arthmoor ([source](https://forums.nexusmods.com/index.php?/topic/1740126-a-simple-world-patch/?p=15067621)):

{{< alert color="info" >}}This MHDT data is speculated to have something to do with dragon height data. Telling them where they can and can't fly while airborn. Sort of serving as their navmesh. There is no solid proof of this though.

[...]

With thousands of mods in the game not forwarding this data (because why would they - it requires DLC) **there is no way that [max height data] being missing is going to matter.** Every mod would break the game. Bethesda's own DLC would break the game, because Dragonborn's MHDT data will clearly not be taking Dawnguard into account, and vice-versa. So just the mere presence of Dragonborn in the game should cause Castle Volkihar to get blocked.{{< /alert >}}

On the xEdit Discord, Arthmoor added ([source](https://discord.com/channels/471930020454072348/505059178365190146/1084213469324263526)):

{{< alert color="info">}} Height data in individual CELL records does matter and dragons will take it into account when those cells are loaded.{{< /alert >}}

TechAngel wrote the following in a post in the STEP forum ([source](https://stepmodifications.org/forum/topic/8358-mhdt-max-height-data/?do=findComment&comment=240176)):

{{< alert color="info" >}}Max height data is merged at runtime, therefore, leaving it blank will not have any impact if the mod is not drastically changing the heights for the cells it's editing (most mods don't). DynDOLOD updates this data, I think, to correct heights for cells that have objects in them that extended beyond the default heights (e.g. installing a mod that has taller trees vs vanilla trees). This height data is also used to updating the occlusion data using xLODGen or DynDOLOD.{{< /alert >}}

### MHDT Conflicts

As TechAngel mentioned, Occlusion generated with [xLODGen](/skyforge/tool-setup/xlodgen) or [DynDOLOD](/skyforge/tool-setup/dyndolod/) as well as the DynDOLOD plugins themselves often modify Max Height Data for cells. These outputs will overwrite everything else.

Where DynDOLOD and xLODGen do not recalculate Max Height Data, I recommend forwarding the value from the Unofficial Skyrim Special Edition Patch.

### Recalculating MHDT

If Max Height Data does not match placed objects, dragons may clip through tall trees or buildings in flight. You should be able to fix this by loading the plugin adding the tall objects into the Creation Kit and regenerating Max Height Data. Make sure it then overwrites any other plugins modifying the same CELL.

![CK Generate MHDT](/Pictures/skyforge/knowledge-base/max-height-data/generate-mhdt-ck.png)