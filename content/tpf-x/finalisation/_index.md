---
title: "Finalisation"
weight: 4
type: docs
description: >
  Final steps and rerunning patchers.
---

## Load Order

Please double-check that your plugins are sorted as instructed in the **Load Order** section on the [Getting Started](/tpf-x/getting-started/#load-order) page.

## Outputs

You need to rebuild several patchers if you installed mods from the following modules:

- New Companions
- Player Homes

If you only installed mods from the other modules, skip this. You are done!

Strictly speaking not every single mod from those modules require you to rerun *all* patchers. However, I really don't feel like maintaining a list of "rerun this if you installed X, that if you installed Y" so just regenerate them all and rest assured that everything is up-to-date.

> If you installed Folkvangr, you may have noticed that it comes with some landscape textures. I have refrained from adding instructions to regenerate terrain LOD because I personally elected to skip the ~40mins of xLODGen blocking my PC at the cost of some mismatched textures that I never notice ingame anyway - they are forest ground textures and they are either covered by foliage or obscured by trees.

### Old Outputs

In Mod Organizer 2 under the **PATCHER OUTPUT**, disable the following outputs:

- TexGen_Output
- DynDOLOD_Output
- SSELODGen - Occlusion Data

### Regenerating Outputs

Each of the folders for the new outputs should have the same name as the old ones *but* with **TPF-X** added so they are easy to distinguish from (and do not replace) the regular TPF outputs.

- Regenerate **TexGen** and **DynDOLOD** with [these instructions](/tpf/finalisation/dyndolod/). Rename the output folders before moving them to MO2\mods.
- Regenerate **Occlusion** with [these instructions](/tpf/finalisation/occlusion/).

## Mod Config

MCM instructions are listed on the installation pages of each separate module if appropriate.