---
title: "Wrapping Up"
weight: 1
type: docs
description: >
  Final edits and touches.
---

## Conflict Resolution Patch

* Download the [Conflict Resolution Patch](https://www.nexusmods.com/skyrimspecialedition/mods/14223?tab=files) from the guide’s Nexus page.
* Install it as usual and place it last below the **FINAL PATCHES** separator.

## Load Order TXT

The pre-made TXT will arrange your plugins exactly like the way they are sorted in my personal setup. This is much faster than adjusting the load order manually or setting up LOOT with custom rules.

### Enabling all plugins

- Click anywhere in the right pane (load order) and select **Enable all**.

> This will ensure all plugins are active prior to sorting them. Plugins may be unchecked automatically when renaming their file extensions.

### Applying the load order

* Download the [Universal Load Order TXT](https://www.nexusmods.com/skyrimspecialedition/mods/14223?tab=files) from the guide’s Nexus page.
* Open the archive and extract the **loadorder.txt** to `Mod Organizer 2\profiles\The Phoenix Flavour`.
* Restart Mod Organizer 2 and the changes will be applied.

After applying the loadorder.txt and restarting MO2, there should be no plugins below the **Conflict Resolution Patch.esp** and the other official but optional patches in the load order (right pane).

If there are other plugins below, you either made a mistake during the mod installation, or a mod was updated and the loadorder.txt is not accounting for it yet. If this happens, please join us on Discord and post your Modwat.ch link in the `#guide-support` channels.

![Load Order Final Plugins](/Pictures/finalisation/loadorder-final-plugins.png)

## Check for MO2 Warnings

MO2 has inbuilt functionality that checks for plugins with Form 43 (Skyrim LE plugins that have not been re-saved in the Creation Kit). If no issues are detected, the **Notifications** icon in MO2 will be greyed out.

* If the button is not greyed out, open the **Notifications** window and check its contents.
* Any plugins that are listed must be re-saved in the Creation Kit now.

![Check for Form43 Plugins](/Pictures/finalisation/check_for_form43_plugin.png)

## Flag Plugins as ESL

### Example Plugin

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

### Remaining Plugins

You will now need to repeat the process for a handful of other mods, most of which will not need their FormIDs renumbered. The plugins to ESL-ify are listed below. Simply add the ESL flag to each of them and don’t forget to renumber FormIDs first for those that need it.

* QuestsAreInSkyrimUSSEP.esp
* SIDT - Special Edition.esp
* dD-Medium Script Range.esp
* dD-Reduced Wound Size.esp
* DeadlySpellImpacts.esp
* Enhanced Vanilla Trees SSE.esp
* ~~UniqueBorderGates-All-PointTheWay.esp~~
* UniqueBorderGates-All-BetterDGEntrance.esp **compact FormIDs**
* GQJ_DG_vampireamuletfix.esp
* CBBE.esp
* Subtle but Classless.esp
* CFTO - Arthmoor Danwstar Patch.esp
* RDO - USSEP Patch.esp
* Miscellaneous Quests…as Miscellaneous Quests.esp
* Northerner Diaries in Skyrim.esp **compact FormIDs**
* Still.esp
* Hun Lovaas.esp
* NirShor-MusicalLore.esp **compact FormIDs**

> If you installed the new music mods, the Music Merge patch will show up as edited when closing SSEEdit. This is intended behaviour. The formIDs renumbered in Northerner Diaries in Skyrim.esp and NirShor-MusicalLore.esp were updated in the plugin.