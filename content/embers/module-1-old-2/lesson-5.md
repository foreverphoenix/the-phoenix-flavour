---
title: "Lesson 5: Load Order"
weight: 5
type: docs
no-list: false
description: >
 Plugin types, how to sort them, and addressing conflicts.
---

## Overview

- WIP

This lesson in particular contains a lot of reading. Don't worry about not remembering everything from your first pass: Everything discussed here will be further explained and put into action in later lessons.

## Basic Plugin Types

In the previous lesson, we had a closer look at the inner workings of plugins, how their records are organised and how they overwrite each other. This knowledge will now help us understand the differences between the various *types* of plugins as well as how to manage them.

There are three different plugin types as well as hybrid combinations of two or even all three of them that serve different purposes. Nevertheless, in their basic structure, all plugins are functionally identical across their various types. The differences are largely related to where they can be placed in the load order and the amount of records that they can store.

The most common file type for plugins is **ESP** (Elder Scrolls Plugin). When exporting changes from the Creation Kit (the official modding tool), this is the file type that the changes are saved in and almost all plugin-based mods make use of it. If you look at your current load order in Mod Organizer 2, you can see exactly one ESP plugin: SkyUI_SE.esp, displayed without any text decoration.

There are also **ESM** plugins (Elder Scrolls Master) which always load above the ESP plugins. In Mod Organizer 2, the official master files (Skyrim.esm, etc) are currently the only full ESM plugins present, displayed in ***bold italics***. They are also greyed out because their load order cannot be adjusted, they are hardcoded to always load first.

### 256 Plugin Limit

**The total number of ESM and ESP plugins in your load order cannot exceed 256 plugins, including the official master files.** This is due to the hexadecimal system used to define them: Each plugin's Index (the first two characters in their form ID) is made up of a combination of two symbols which in turn is based on their load order. The hexadecimal system has 16 unique characters and for two symbols there are exactly 256 possible combinations from 00 to FF ([see this table](https://files.renoise.com/forum/uploads/5358-hexadecimalchart1.png)). The hexadecimal FF is the decimal 255, so the maximum amount of plugins from 0 (00) to 255 (FF) is 256.

In Skyrim LE the plugin limit could be overcome by merging the records of multiple plugins into a single one. However, in Skyrim SE plugin merging has become essentially redundant for all but the largest of load orders thanks to the new ESL format of plugins introduced with the 2015 engine update.

## ESL Plugins

The **ESL** (Elder Scrolls Light) plugins are among the most important features of Skyrim SE. They were created for Bethesda's "Creation Club" in order to potentially add a large amount of additional plugins for various "creations".

All ESL plugins have the Index `FE:xxx`. The hexadecimal FE is the decimal 254, so all ESL plugins load in plugin slot 254. This is possible because their Index was extended to the third, fourth, and fifth character in their eight character form ID: An ESL's Index could be `FE:000` or `FE:08F`. The limit for ESLs is a whopping **4096** plugins.

The downside of ESLs is that they can store fewer records. Remember that each record must have a unique form ID and ESLs only have three digits left for a combination of the 16 hexadecimal characters instead of six like ESPs or ESMs. This means they can store 4096 unique form IDs of which the first 2048 are reserved by the engine. The remaining 2048 slots are still more than enough for small to medium size mods. Many separate ESL plugins are infinitely easier to handle than large plugin merges (imagine having many small drawers for screws of differents types and sizes instead of dumping all of them into a single big one).

Additionally, this limit only affects *new* records, records defined in the ESL plugin. There is no limit on how many records defined in *other* plugins they can hold. Many mods function mostly by editing existing (vanilla or mod-added) records and add few or no new records of their own. These types of plugins are especially suited to being ESL-ified.

### ESL Load Order

Regular **ESL** plugins are always forced between ESM and ESP plugins in the load order. Mod Organizer 2 displays them in *italics* like our *Disable USSEP Book.esl* which we created in the previous lesson. While the position of plugins in the load order can normally be manipulated via drag and drop, you will notice that you can change the order of the two ESP plugins at the bottom, but are unable to move them above the ESL or ESMs.

## Hybrid Plugins

You likely already noticed it: Most plugins in our load order right now are not consistent with the plugin types we just discussed. For example, the **Unofficial Skyrim Special Edition Patch.esp** is displayed in **bold** like an ESM but has the ESP file extension. And *Skyrim Landscape and Water Fixes - Light Sources.esp* is displayed in *italics* like an ESL plugin but also has the ESP file extension.

The type of a plugin is determined by two factors: File extension (.esm, .esp, .esl) and plugin flag. For example, a regular ESP has the .ESP extension and no plugin flag, it can be placed anywhere below the ESM and ESL plugins, and counts against the 256 plugin limit.

However, file extensions and plugin flags can be adjusted to allow for different combinations beyond the three main plugin types (ESM, ESP, ESL).

This is where **hybrid plugins** come into play.

### ESP-FE Plugins

If a plugin is rather small it may be far more practical to turn it into an ESL. Unfortunately, a full ESL (a .esl plugin with the ESL flag) will be forced to load below the ESMs and above the ESPs. In the case of conflicts between it and any ESPs, it cannot simply be moved below the other plugin. This is why full ESLs are relatively rare and most people use so-called **ESL-ified ESPs** or **ESP-FE plugins** instead. These plugins have the .ESP file extension but were flagged as ESL in SSEEdit.

Flagging ESPs as ESLs is a very common step in the assembly of a mod list, especially if there are enough ESMs and ESPs in the load order to approach the 256 plugin limit. Note that you cannot simply change the file extension of an ESP to .ESL since these two plugin types have differently structured form IDs. You need to first *renumber* the ESP's form IDs in SSEEdit before you can add the ESL flag to it (also in SSEEdit). How this works will be explained in more detail later on.

An ESP-FE plugin can be turned into a full ESL by simply renaming its file extension from .ESP to .ESL which is exactly what we did to the *Disable USSEP Book.esl* plugin in the previous lesson.

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

To recap: A plugin consists of many records. If a record exists in more than one plugin, the copy from the record that is loaded lower in the load order will be used by the game. This is also called the **rule of one**: The game cannot "merge" edits from overwriting records, it will only consider the one placed last.

Different versions of the same record are also referred to as **layers**. In the example from Lesson 4 (picture below), the USSEP contains a copy of a record from Skyrim.esm as a new layer. In the new layer, the USSEP makes an edit to the text of a note. Because the USSEP is below Skyrim.esm in the load order, its version of the record will be the one used by the game.

![Plugin Layers](/Pictures/embers/module-1/ussep-book-record-details.png)

Since modding means editing the base game, it makes sense that the official master files are all the way at the top so that all other plugins are placed below them and can overwrite. It also means that it is quite relevant where in the load order all the other plugins are placed because they affect each other in the same way. **Plugins overwrite each other in the order they are placed in.**

## Plugin Dependencies

Plugins can edit existing records, add new ones, or do a mix of both. If a plugin edits an existing record, it will depend on the plugin that the existing record was defined in. For example, in the image above the USSEP edits a record defined in Skyrim.esm and therefore requires Skyrim.esm to be active in the load order. In other words: Skyrim.esm is a master to the USSEP. **Plugins must always be placed *below* their masters so they can properly overwrite.**

All plugins need to have at least Skyrim.esm as a master file, but they can also depend on other plugins, official or mod-added. This is the case with **Landscape and Water Fixes.esp** which depends on the **Unofficial Skyrim Special Edition.esp**. If you uncheck the USSEP's plugin in the load order, Mod Organizer 2 will instantly warn you about the missing master. The notification in the upper right corner will light up and show the warning if you click on it.

![SLAWF Missing Master](/Pictures/embers/module-1/slawf-missing-master.png)

Alternatively, you can hover over the **Landscape and Water Fixes.esp** which has now been marked with a small warning sign icon to see all its dependencies and which master is missing.

Since the Landscape and Water Fixes plugin requires the USSEP plugin directly, we know that it must be placed *below* it in the load order as plugins are always placed below their masters. Re-enable the USSEP plugin and make sure it is placed above the Landscape and Water Fixes plugin before proceeding with the next step.

> It should be noted that Skyrim SE, unlike Skyrim LE, does not *always* immediately crash on launch when a master is missing. However, a missing master will still cause critical errors and has to be fixed.

## Additional Mods

Before we can begin to discuss conflict resolution, we need a few more example mods. Remember that the mods installed here are mostly picked for demonstration purposes and you can uninstall them after completing **Embers**. For now, we need examples.

### Weapons Armor Clothing and Clutter Fixes

[Weapons Armor Clothing and Clutter Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/18994), or WACCF, is one of the most popular baseline fix mods. It is also a touch controversial on account of its out-of-scope edits and the amount of work required to integrate it properly in a modded setup. I am personally of the opinion that it is worth it, you can make up your own mind later.

For now, please install the main file through Mod Organizer 2. Place the mod above **Skyrim Landscape and Water Fixes** in the mod order (left pane) and activate it.

You will notice that two plugins now appear in the load order (right pane). The second one, **WACCF_BashedPatchLvlListFix.esp**, is a helper plugin to create a so-called Bashed Patch which is an imperfect and outdated practice. We will discuss manually patching levelled lists later on.

Since we do not need the helper plugin and will not need it in the future, we might as well remove it. Remember that all mods are self-contained within mod folders under `\Mod Organizer 2\mods\`, but can easily be viewed and edited through MO2's interface:

- Double-click **Weapons Armor Clothing and Clutter Fixes** in your mod order.
- Switch to the **Filetree** tab where all the files in the mod's folder can be viewed.
- Delete the **WACCF_BashedPatchLvlListFix.esp** plugin.

![WACCF Delete Plugin](/Pictures/embers/module-1/waccf-delete-plugin.png)

Once again, I consider it good practice to document any steps taken, any edits or changes, in the **Notes** tab in Mod Organizer 2. This is optional, you must decide for yourself how thorough you want to be. I left myself a note reminding me that I "Removed the Bashed Patch helper plugin."

### WACCF Greatsword Weapon Speed Tweaks

[WACCF Greatword Weapon Speed Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/50250) is part of a collection of small mods. In vanilla, greatswords have a speed of either 0.75 or 0.7 (this affects how fast you can swing it). The USSEP equalises the values to 0.75 across the board so that all greatswords feel consistent and WACCF does the same thing but increased the swing speed further (to 0.8).

However, when using certain combat or perk mods that increase the swing speed of two handed weapons, they may become a little too fast. To solve this, **WACCF Greatword Weapon Speed Tweaks** once again lowers the swing speed of all greatsword back to the USSEP's value (0.75) while keeping all other WACCF changes.

Install **WACCF Greatsword Weapon Speed Tweaks** (found under Miscellaneous Files on the mod page) through Mod Organizer 2. Place the mod below **Weapons Armor Clothing and Clutter Fixes** and activate it.

### Guard Dialogue Overhaul

[Guard Dialogue Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/22075), or GDO, is a fantastic rework of Skyrim's guards. Their attitude towards the player will improve as the player's own legend grows. Additionally, the mod includes many bug fixes and adjustments to make certain lines play under more appropriate conditions. It also conflicts with WACCF which is very useful for our purposes.

Install the main file through Mod Organizer 2. Place the mod below **WACCF Greatword Weapon Speed Tweaks** and activate it.

### Audio Overhaul for Skyrim

[Audio Overhaul for Skyrim](https://www.nexusmods.com/skyrimspecialedition/mods/12466), or AOS, is the definitive sound FX mod for Skyrim SE. In addition to many new, distinct sounds, AOS also reworks audio range, reverb (sound reflection / echoes), and overall volume balance.

Install the main file through Mod Organizer 2. Leave it at the bottom of your mod order and activate it.

## Plugin Conflicts

Now that we have four new plugins added to our load order, three ESPs and one ESP-FE, we can jump back into SSEEdit and have a look at their inner workings as well as how they interact with each other.

Your load order should currently look like this:

![Lesson 5 Plugins](/Pictures/embers/module-1/lesson-five-plugins.png)

Go ahead and launch SSEEdit through Mod Organizer 2 once again. Remember that you can just click the icon we added to the toolbar in the top right in Mod Organizer 2. Click **OK** when the plugin selection window pops up (we want to load all plugins) and click **OK** again in the ModGroup window (leave them all unselected).

When adding new plugins to your load order, you will want to check them for two things: Their own implementation and how they interact with other mods. For now we will largely focus on the latter as the former requires in-depth knowledge that we have yet to acquire.

Mod interactions mostly boil down to conflicts: **Conflicts occur when two or more plugins change the same record.** Due to the "rule of one", the record from the plugin loading last will override and be the one used ingame. Now conflicts are not inherently "bad", they are quite normal and, in fact, unavoidable. Because of how plugins are structured, it is unusual for a mod to have no conflicts at all.

When building a mod setup, a lot of time is spent organising plugins, reviewing and, if necessary, addressing their conflicts, and adjusting their load order. Upon discovering a conflict between plugins, one may decide that it is harmless or even necessary, or that it needs to be addressed in one of two ways (by changing the load order or creating a patch). We will now take a look at different kinds of conflicts and how to deal with them.

## Conflict Resolution: Load Order

Let's start with the first one of the new plugins we just added:

- Double-click **Weapons Armor Clothing and Clutter Fixes.esp** in the left pane to expand the plugin.

From the long list of categories, we can see that WACCF edits a lot of different types of records.

- Double-click the **Armor** category and select the `[ARMO:000136D5] ArmorImperialCuirass "Imperial Armor"` record.

The record is highlighted in red, meaning that multiple plugins are editing the same record, changing different things. **This is a conflict.** Scrolling down in the right pane, we can see that WACCF is adjusting the Value and Armor Rating values for the Imperial Armor, but GDO is reverting them back to vanilla. The values are displayed in gray in the GDO layer, meaning they are *identical to master* (Skyrim.esm).

![GDO WACCF Conflict](/Pictures/embers/module-1/waccf-gdo-conflict.png)

Checking other Armor records, you will see that the pattern repeats itself: GDO frequently overwrites WACCF, reverting values to vanilla. Any keywords added by GDO are usually also present in WACCF, however.

### About SPIKE

In order to address conflicts, we need to understand them first.

The keywords added by WACCF/GDO that are prefixed with "SPIKE" come from a very old keyword resource (released in 2012) by the same name.

Using keywords from SPIKE.esm allowed for patchless feature integration between mods: For example, guards may comment on your armor not providing very much protection for which GDO added the keyword `SPIKEArmorWeak` as a condition. If a mod added a new armor that would also be considered "low-tier", it would not require a GDO patch; simply assigning the `SPIKEArmorWeak` keyword would be enough to make the armor function with GDO if that mod were installed but without outright requiring it. The idea was that everyone would have SPIKE.esm in their load order which would be the only hard requirement.

(If you're curious you can find more information about SPIKE [here](https://www.nexusmods.com/skyrim/articles/414/?).)

While SPIKE did not establish itself and keyword resources are not commonly used in Skyrim SE in the way that SPIKE was intended to be, GDO is still using its keywords (it was by the same author and originally served as proof of concept). Nowadays, all the SPIKE keywords are included with GDO, WACCF, and AOS as records injected in Update.esm (which you can tell from their index being `01`). As we previously established, injected records are another great way to create patchless compatibility between mods.

![SPIKE Injected Keywords](/Pictures/embers/module-1/spike-injected-keywords.png)

### The Solution

Luckily for us, WACCF and AOS have already added those same keywords to all armor and weapon records they edit in addition to their own changes. This means that both of them should be overwriting GDO. The conflicts between GDO and WACCF can therefore be resolved sufficiently by simply adjusting the load order: placing GDO above WACCF.

**If one of several conflicting plugins includes all changes from the others, the conflict can be resolved by changing the load order.**

Since the load order cannot be changed from inside SSEEdit, close it for now. Back in Mod Organizer 2, drag **Guard Dialogue Overhaul.esp** above **Weapons Armor Clothing and Clutter Fixes.esp** in the load order (right pane).

## Conflict Resolution: Harmless Conflicts

Now that we have addressed the first round of conflicts, re-open SSEEdit. In order to find more conflicts, we can use a filter that will automatically highlight them, making them easier to find.

- Right-click anywhere in the left pane and select **Apply Filter**.
- Copy the settings from the screenshot below and click **Filter**.

![Filter For Conflicts](/Pictures/embers/module-1/filter-for-conflicts.png)

Applying the filter will take a minute.

When it's done, you will see that your plugins are now color-coded. Only **SkyUI_SE.esp** is still displayed without highlight, meaning it is the only plugin that has *only* new records and does not overwrite or even conflict with existing records. Meanwhile, our previously created **Disable USSEP Book.esl** is displayed with a green highlight: It does overwrite an existing record (the ref record for the book we flagged as "initially disabled"), but it does not overwrite any other plugin's changes.

Looking at **Weapons Armor Clothing and Clutter Fixes**, it is highlighted in red: It conflicts with and overwrites other plugins.

- Expand **Weapons Armor Clothing and Clutter Fixes.esp**.
- Open the **Armor Addon** category and select the `[ARMA:00062302] UlfricTorsoAA` record.

![ARMA Record Conflict](/Pictures/embers/module-1/arma-record-conflict.png)

Armor Addon, or **ARMA**, records are always connected to Armor records, Ulfric's Clothes in this case (armor, clothing, and jewelry all count as "Armor" records). In this particular record, WACCF and the USSEP both appear to be implementing a new Alternate Texture Set as it turns out that the inventory model for Ulfric's Clothes is using the generic `1stPersonOutfitM_1.nif` mesh that is also used by some other Jarls.

We will take a closer look at meshes and textures later on. For now it is enough to know that the file path to its textures is defined within a mesh but Alternate Texture Sets can be used to change them for specific objects. In order to change the textures on the inventory model for Ulfric's Clothes to Ulfric's unique grey variant, an Alternate Texture Set can be defined in the ARMA record which is precisely what both the USSEP and WACCF are doing.

- Hold CTRL and click the `[TXTST:0502F6A6] USKPUlfricTorso` texture set.

![CTRL Click Records](/Pictures/embers/module-1/ctrl-click-xedit.png)

This will immediately take you to the record. Take note of which textures the USSEP changes the file paths to, then return to the ARMA record. To do so, simply paste its Form ID `00062302` in the Form ID box above the plugin list. Now CTRL-click the WACCF Alternate Texture Set to see what it does.

![USSEP WACCF Alt TXTS](/Pictures/embers/module-1/ussep-waccf-txts.png)

As it turns out, the two records do the same thing! Yes, there is a conflict, but only because both Alternate Texture Sets implemented to fix the problem have different Form IDs. Which one is used is ultimately irrelevant and there would be a conflict either way. No change is necessary.

### When is a conflict harmless?

In the example above, it's obvious: Both mods to the same thing. Since WACCF also changes the mesh path for the female model, it should overwrite so all its changes make it into the game, but regardless of load order, there will be a conflict.

But it may not always be as easy. Take a look at `000EAFDF` for example (remember you can search for Form IDs to quickly find a record). The USSEP changes the damage dealt by Nord Hero Arrows to 16 while WACCF changes it to 17 instead and also adjust its value. In cases like this one, the WACCF change should be preferred as it is part of a mod that explicitly overhauls balancing for all weapons and armors while the USSEP mostly fixes bugs and inconsistencies. This is why none of the other conflicts between the USSEP and WACCF need to be adressed, and WACCF should simply overwrite.




## Conflict Resolution: Patches

---




- GDO + WACCF for resolving conflicts via changing the load order
- RW2 + No Grass In Caves for resolving conflicts via a patch
- have a combination where there are conflicts that are okay and dont need resolving
- consistency patching (add mod with new greatsword and set speed to 0.75?)

0006230C needs patch

WACCF and USSEP NPC records conflict (USSEP removes perks?)