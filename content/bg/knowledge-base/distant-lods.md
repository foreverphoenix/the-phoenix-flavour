---
title: "Distant LODs"
weight:
type: docs
description: >
  About the several types of distant LODs.
---

## About Distant LODs

{{< alert color="info" >}}This article draws heavily on and occasionally quotes from resources written by **sheson**, the creator of [DynDOLOD](/bg/tool-setup/dyndolod/) and the authority on all things related to LODs. Please check the [DynDOLOD website](https://dyndolod.info/) for more detailed information.{{< /alert >}}

In the context of Creation Engine modding, **distant LOD** (level-of-detail) describes far-away objects and landscape. The further the object or terrain is from the player, the lower the quality in which it is rendered. This improves performance.

**LODs should be regenerated in modded setups for better quality and to integrate the installed mods.**

{{< alert color="success" >}}Contrary to popular belief, generating DynDOLOD on the Low preset should not negatively impact performance while still noticeably improving distant terrain.{{< /alert >}}

### Types of LOD

There are multiple types of LOD:

- [Object LOD](https://dyndolod.info/Help/Object-LOD) "are combined meshes and textures for objects that do not change and are not animated, like buildings or landscape features like mountains and rocks."
- [Tree LOD](https://dyndolod.info/Help/Tree-LOD) is a separate LOD system for rendering distant trees as [flat cardboard cutouts](https://dyndolod.info/sites/dyndolod/files/images/tree-lod.webp). With DynDOLOD you can also generate much higher quality 3D or hybrid Object LOD for trees.
- [Terrain LOD](https://dyndolod.info/Help/Terrain-LOD-and-Water-LOD) "is the distant ground and large (cell sized) bodies of water." Regenerating it ensures that your close-up landscape textures match and blend with distant terrain.
  - *The world map uses Terrain LOD meshes and textures (LOD Level 32).*
- [Grass LOD](https://dyndolod.info/Help/Grass-LOD) visually extends grass into the distance without the performance cost of fully rendering it.

**Terrain LOD** is generated with [SSELODGen](/bg/tool-setup/sselodgen/).

**Object** and **Tree LOD** are generated with [DynDOLOD](/bg/tool-setup/dyndolod/).

<font size=2>*SSELODGen can also generate Object and Tree LOD, but not as high quality as DynDOLOD.*</font>

**Grass LOD** is also generated with [DynDOLOD](/bg/tool-setup/dyndolod/) but requires some extra steps and tools.

{{< alert color="info">}}If you are interested in **Grass LOD**, please consult [Althro's guide](https://github.com/The-Animonculory/Modding-Resources/blob/main/Grass%20Lods.md).{{< /alert >}}

### LOD Resources

Creating matching LODs for your mods requires additional resources. Some of those are provided on the Nexus while others, namely [billboards](https://dyndolod.info/Help/Tree-Grass-LOD-Billboards), must be generated with TexGen specifically for your setup. Billboards are required for **Tree** and **Grass LOD** and must generated with TexGen before running DynDOLOD.

For **Terrain LOD** generation, LOD resources may be provided by the author for improved blending. If so, overwrite the original mod with the LOD resources while running SSELODGen and *disable them afterwards*.

DynDOLOD resources should be left <u>enabled</u> after LOD generation.

Installation instructions for resources that should be present in any setup are covered in the [SSELODGen](/bg/tool-setup/sselodgen/) and [DynDOLOD](/bg/tool-setup/dyndolod/) setup instructions.

## When should I generate LODs?

LOD (and Occlusion) generation are generally the final steps in building a setup because all objects and assets must be present to be incorporated. DynDOLOD copies from the final layer of each plugin so all conflict resolution must be completed at this point as well.

That being said, I typically generate *temporary* object, tree, and terrain LOD after completing my visual baseline for a setup. This allows me to approximate the level of graphical quality as well as performance I will eventually have while giving me a good backdrop for hand-picking assets and testing ENB presets. In this case I would only generate for the Tamriel worldspace to speed up the process.

{{< alert color="warning" >}}DynDOLOD uses Terrain LOD meshes to optimise Object LOD. Always generate Terrain LOD first.{{< /alert >}}

### Regenerating Terrain LOD

**Terrain LOD** should be regenerated after changing landscape textures.

It is possible to regenerate Terrain LOD after beginning a playthrough because it is affected by mods (mesh and texture replacers) that can be added or removed at any time. Remove your previous output, then rerun [SSELODGen](/bg/tool-setup/sselodgen/).

### Regenerating Object and Tree LOD

**Object** and **Tree LOD** should be regenerated when the position of objects changed or new objects were added (for example, a new ruin was added to the Morthal swamp or some trees were resized in the Rift). Unless the LOD assets changed (for example, because you changed your tree overhaul), you do <u>not</u> need to regenerate billboards with TexGen.

The TexGen and DynDOLOD outputs can be regenerated in an ongoing playthrough, but this requires some extra steps:

1. Load your save and make sure you are in an exterior cell.
2. Disable DynDOLOD in the ingame MCM.
3. Go into an interior cell (like a house or a dungeon).
4. Create a manual save and exit the game.
5. Remove your old DynDOLOD output (and TexGen, if necessary).
6. Reload your save and click OK to missing plugins.
7. Create a manual save and exit the game.
8. Update DynDOLOD and regenerate the output(s).
9. Load your save and continue your playthrough.