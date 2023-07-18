---
title: "References"
weight:
type: docs
description: >
  About references and ESM space.
---

## About References

This article summarises some basic knowledge about **references**.

{{< alert color="info" >}}I recommend reading the article on [Plugin Basics](/bg/knowledge-base/plugin-basics/) first.{{< /alert >}}

**References** (REFR) records make up the vast majority of records in the vanilla game files which is why [SSEEdit](/bg/tool-setup/sseedit/) specifically caches these records to speed up the process of opening a load order.

References are generally *things* placed in the world: This includes items like swords or flora like shrubs as well as spawn points, trigger boxes for scripts, and activators to display button prompts. Each reference links to a base object that it is placing and controls the placement, visibility, ownership, and other traits of the object.

### Base ID versus Ref ID

When viewing objects ingame through [More Informative Console](/bg/recommended-mods/console-improvements/#more-informative-console), you will see not one but two Form IDs:

- The **Base ID** is the original (weapon, NPC, tree, etc) record of the object that is placed.
- The **Ref ID** is the specific copy of the object you are looking at.

The distinction is important when trying to modify the reference: If you want to change its placement, you need to look at the Ref record. If you want to change the placed object, you need to look at the Base record.

![Form IDs](/Pictures/bg/core-module/ussep-book-formid.png)

## Persistent versus Temporary

There are two types of references:

- **Temporary references** only load into memory when the player is close by and are unloaded when they are no longer needed.
- **Persistent references** are always loaded into memory upon launching the game, regardless of player proximity.

{{< alert color="info" >}}Persistent references also appear to vary in their *level of persistence*. You can read a write-up by Arthmoor on the topic [here](https://www.afkmods.com/index.php?/topic/4250-skyrim-levels-of-persistence/).{{< /alert >}}

![Refs](/Pictures/bg/core-module/temporary-persistent-refs.png)

References being persistent has important implications for adding, updating, and removing mods in an ongoing playthrough: Depending on their level of persistence, you may need to let the CELL containing the reference(s) reset while other objects are permanently baked into the save as soon as you load the game with them.

### Reference Handle Cap

The cap for references that are active at a time is **1048576**. Anything above that will cause issues and instability. [SSE Engine Fixes](/bg/recommended-mods/essential-mods/#sse-engine-fixes) will warn you if you are approaching the cap.

The amount of loaded references can be reduced by moving plugins into ESM space.

{{< alert color="info" >}} Read this [reddit post](https://www.reddit.com/r/skyrimmods/comments/ag4wm7/psa_the_reference_handle_cap_or_diagnosing_one_of/) for more information on the reference handle cap.{{< /alert >}}

### ESM Space

The difference between ESP and ESM space largely affects references. As previously mentioned, temporary references should be *unloaded* when the player has moved out of range, but this is actually only the case in ESM space.

**Temporary references in ESP space are handled like persistent references and always loaded at the start of the game.**

This means that every temporary references added <u>or</u> modified by an ESP will permanently count toward the cap. As a consequence, you are much more likely to reach the cap eventually with a big load order.

The solution to the problem is to ESM-flag mods with many (new or modified) temporary references. Fortunately, most mods that add large worldspaces are already shipped as ESMs so that their considerable number of temporary references is not always active.

## Overriden Forms (ONAM)

When a plugin in ESM space overwrites references from another plugin (which is necessarily also in ESM space), the references in question must be added to the **Overriden Forms (ONAM)** list in the Plugin Header. Otherwise, the edit to the reference will simply be ignored.

When you ESM-flag a plugin in SSEEdit, all overwritten references are added to this list automatically.

![ONAM](/Pictures/bg/knowledge-base/references/onam.png)

### ESLs and ONAM

There is an edge case where you may end up with an ESM space plugin that overwrites references without adding them to the ONAM list:

If you want to turn an ESL-ified ESP into a full ESL, technically all you need to do is change its file extension. However, this will place the plugin in a strange position where it is loaded in ESM space without actually having the ESM flag. If that plugin contains references, they will not be added to the Overriden Forms list and its modifications will be ignored by the game.

When turning an ESP or ESP-FE into a full ESL, always go through SSEEdit and also add the ESM flag. There are no downsides to this. If the plugin overwrites references, SSEEdit will populate the Overriden Forms list to make sure the mod does not break.