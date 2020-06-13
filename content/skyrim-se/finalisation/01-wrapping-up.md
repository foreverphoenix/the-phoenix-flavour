---
title: "01 Wrapping Up"
weight: 1
type: docs
description: >
  Final edits and touches.
---

## 1.1 Misc College of Winterhold Tweaks

We were previously unable to properly install **Misc College of Winterhold Tweaks** by SomethingObscure in Step 27 because the FOMOD options required the matching plugins to be available in the load order. These plugins are now in your available so we can re-install the mod.

Find **Misc College of Winterhold Tweaks** in your mod order, right-click it and select **Reinstall**.

### 1.1.2 FOMOD Instructions

* **Arniel's Appeals:**
  * Arniel's Appeals
* **A College Coup:**
  * A College Coup
  * Obscure's College of Winterhold Add-on
  * Immersive College NPCs Add-on
  * Interesting NPCs Add-on
* **Dead Dunmer Delivery:**
  * Dead Dunmer Delivery
* **Governable Gatekeeper:**
  * Governable Gatekeeper
* **Expedite the Expirate:**
  * Expedite the Expirate
* **Unflappable Faculty:**
  * Unflappable Faculty
* **The Early Elementalist:**
  * None
* **Inescapable Insights:**
  * Merged Version

> The **Early Elementalist** module allows you to Wait in the Hall of Elements. This is done by removing the "Can't Wait" flag in that cell. Because this record has to be forwarded into the Conflict Resolution Patch anyway (to patch it with changes from other mods, namely Luminosity), there is no point in keeping the original ESP. In short - skip the option, it is already implemented in the CRP. 

## 1.2 Conflict Resolution Patch

* Download the [Conflict Resolution Patch](https://www.nexusmods.com/skyrimspecialedition/mods/14223) from the guide’s Nexus page.
* Install it as usual and place it last below the **PATCHES** separator.

## 1.3 Load Order TXT

The pre-made TXT will arrange your plugins exactly like the way they are sorted in my personal setup. This is much faster than adjusting the load order manually or setting up LOOT with custom rules.

* Download the [Universal Load Order TXT](https://www.nexusmods.com/skyrimspecialedition/mods/14223) from the guide’s Nexus page.
* Open the archive and extract the **loadorder.txt** to `Mod Organizer 2\profiles\The Phoenix Flavour`.
* Restart Mod Organizer 2 and the changes will be applied.

After applying the loadorder.txt and restarting MO2, there should be no plugins below **Conflict Resolution Patch.esp** in the load order (right pane). If there are plugins, you either made a mistake during the mod installation, or a mod was updated and the loadorder.txt is not accounting for it yet. If this happens, please join us on Discord and post your Modwat.ch link in the #request-support channel.

## 1.4 Check for MO2 Warnings

MO2 has inbuilt functionality that checks for plugins with Form 43 (Skyrim LE plugins that have not been re-saved in the Creation Kit). If any are detected, the **Notifications** icon in MO2 will no longer be greyed out.

* Open the **Notifications** window and check its contents.
* Any plugins that are listed must be re-saved in the Creation Kit now.

![Check for Form43 Plugins](/Pictures/finalisation/check_for_form43_plugin.png)

## 1.5 Flag Plugins as ESL

### 1.5.1 Example Plugin

While at this point many installed plugins are already flagged as ESL (ESP-Lite) and we are not exceeding the maximum of 255 ESP+ESM plugins, there are several more plugins that may easily be flagged as ESL in order to save plugin slots. This completely removes the need to merge some plugins.

* Run **SSEEdit** through Mod Organizer 2.
* Click **OK** in the plugin selection window to load all your mods.
* Wait until SSEEdit has finished loading up your plugins and returns `Background loader: finished`.
* Right-click **UniqueBorderGates-All-PointTheWay.esp** in the left pane (near the bottom) and select **Compact FormIDs for ESL**.
* A warning window will pop up, click **Yes, I’m absolutely sure**.
* Another warning will inform you that there are indeed FormIDs to renumber. Click **Yes**.
* The process itself takes a mere second. When it’s done, switch back to the **View** tab at the bottom to see the plugin’s file header.
* Right-click the empty space to the right of **Record Flags** and select **Edit**.
* In the next window, check only **ESL** and click **OK**.
* The plugin is now successfully flagged as ESL! **Don’t close SSEEdit yet.**

> Plugins that contain no new records with new FormIDs and only edit existing records (from the official master files or other mods) do not need to have their FormIDs renumbered. When you attempt to renumber them, a window will pop up informing you that there was **Nothing to do**.

### 1.5.2 Remaining Plugins

You will now need to repeat the process for a handful of other mods, most of which will not need their FormIDs renumbered. The plugins to ESL-ify are listed below. Simply add the ESL flag to each of them and don’t forget to renumber FormIDs first for those that need it.

* QuestsAreInSkyrimUSSEP.esp
* SIDT - Special Edition.esp
* Improved Snow - Obsidian Weathers.esp
* dD-Medium Script Range.esp
* dD-Reduced Wound Size.esp
* DeadlySpellImpacts.esp
* Enhanced Vanilla Trees SSE.esp
* EVT_LightSnowTrees_Replacer (For Vurts).esp
* GQJ_DG_vampireamuletfix.esp
* CBBE.esp
* Subtle but Classless.esp
* Miscellaneous Quests…as Miscellaneous Quests.esp
* Northerner Diaries in Skyrim.esp **compact FormIDs**
* Still.esp
* Hun Lovaas.esp
* NirShor-MusicalLore.esp **compact FormIDs**
* ~~UniqueBorderGates-All-PointTheWay.esp~~
* UniqueBorderGates-All-BetterDGEntrance.esp **compact FormIDs**
* CFTO - Arthmoor Danwstar Patch.esp
* RDO - USSEP.esp

> If you installed the new music mods, the Music Merge patch will show up as edited when closing SSEEdit. This is intended behaviour. The formIDs renumbered in Northerner Diaries in Skyrim.esp and NirShor-MusicalLore.esp were updated in the plugin.