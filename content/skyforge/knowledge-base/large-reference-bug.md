---
title: "Large Reference Bug"
weight:
type: docs
description: >
  About causes and fixes for the large reference bug.
---

## Large References

{{< alert color="info" >}}This article draws on and quotes the article on the [large reference bug](https://dyndolod.info/Help/Large-References) in the DynDOLOD documentation.{{< /alert >}}

A **large reference** is a [reference](/skyforge/knowledge-base/references/) "that has an entry on the RNAM list on the worldspace record in the the ESM-flagged master plugin that adds the record". The base record of a large reference must be a **Static** (STAT) and **Movable Static** (MSTT). Its "object bounds volume on the base record and scale of the reference must be larger than the [fLargeRefMinSize](/Pictures/skyforge/knowledge-base/large-reference-bug/large-ref-min-size.png) global" (meaning they are physically big).

Large references are relevant for distant objects (LOD), specifically the **large references grid**.

### Large References Grid

The **large references grid** is a feature added in Skyrim SE to increase distant detail by rendering particularly large objects further away. The system is <u>active</u> when `uLargeRefLODGridSize` (SkyrimPrefs.ini) has a higher value than `uGridsToLoad` (Skyrim.ini). Both settings can be found in the `[General]` section.

{{< alert color="info" >}}If you followed my [INI configuration](/skyforge/modding-resources/ini-config) instructions, the large ref system should be active.{{< /alert >}}

![Large Refs](https://dyndolod.info/sites/dyndolod/files/images/large-references.webp)

### Large Reference Bug

**The large reference bug occurs when the LOD model of an object persists after the full model is loaded in.** As a result there will be flickering (z-fighting) where the two models overlap, or the full model will be entirely obscured by the very low-detail and low-res LOD version.

(This is also sometimes described as the *LOD not unloading bug*.)

You can see examples [here](https://vimeo.com/625772521) and [here](https://vimeo.com/641994013). Note how the houses and the bridge to the college are flickering because both LOD and full model are loaded at the same time.

The bug is typically caused by **large references** being present *outside* of ESM plugins. Whether they are modified is irrelevant: Even if the reference is only present as an ITM in an ESP plugin, it will break the large ref system and, as a result, trigger the bug. A large reference in an ESP that is flagged as *Initially disabled* will also trigger the bug.

Less common causes of the bug include a base record of a large reference not being a (Moveable) Static (STAT or MSTT) or improperly ported mods (the latter is logged and fixed by DynDOLOD).

{{< alert color="info" >}}For more details, please consult the [DynDOLOD documentation](https://dyndolod.info/Help/Large-References).{{< /alert >}}

### Finding & Fixing the Bug

To my knowledge, the only way to locate *large references* outside of ESMs is running [DynDOLOD](/skyforge/modding-resources/lod-occlusion/) which will create a log with all records that can trigger the bug. I do not believe that an SSEEdit script currently exists to scan for large refs in ESP plugins.

There are three solutions to the issue:

1. **ESM-flagging plugins** that contain large references. This can be tricky when said plugins have many patches or have masters that are ESPs because forcing it to load in ESM space would break the dependency.
   - *It is possible to only move the large references into an ESM and leaving everything else in ESP space.*
2. **Disabling the large ref system** by ensuring that `uLargeRefLODGridSize` is set to the same value as `uGridsToLoad`.
   - *The default should be uGridsToLoad=5.*
3. **Generating DynDOLOD NG** with the *large reference bug workarounds* (see below).

The third option requires the most effort but should yield the best results.

## DynDOLOD

For Skyrim SE DynDOLOD generates both an ESM *and* an ESP precisely because of the large reference system. Any large references that it needs to modify are modified in the ESM to prevent the bug.

If the large reference system is <u>active</u>, the **Large References Fix** should be <u>enabled</u> in the DynDOLOD MCM:

![Large Ref Fix](https://dyndolod.info/sites/dyndolod/files/images/mcm-sse-main.webp)

### Large Ref Bug Workarounds

DynDOLOD NG features experimental **workarounds** for the large reference bug. To enable these, you must use the NG DLL and scripts instead of the regular ones and ensure that no plugins contain deleted large references. The latter is done most easily by [cleaning plugins](/skyforge/modding-resources/cleaning-plugins/).

More details and installation instructions can be found on the [DynDOLOD](/skyforge/tool-setup/dyndolod/) page. The [LOD & Occlusion](/skyforge/modding-resources/lod-occlusion/) page contains instructions on how to generate DynDOLOD with the large reference bug workarounds.