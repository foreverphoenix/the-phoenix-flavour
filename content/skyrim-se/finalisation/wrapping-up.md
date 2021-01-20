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

After applying the loadorder.txt and restarting MO2, there should be no plugins below the **Conflict Resolution Patch.esp** in the load order (right pane).

If there are other plugins below the CRP, you either made a mistake during the mod installation, or a mod was updated and the loadorder.txt is not accounting for it yet. If this happens, please join us on Discord and post your Modwat.ch link in the `#guide-support` channels.

## Check for MO2 Warnings

MO2 has inbuilt functionality that checks for plugins with Form 43 (Skyrim LE plugins that have not been re-saved in the Creation Kit). If no issues are detected, the **Notifications** icon in MO2 will be greyed out.

* If the button is not greyed out, open the **Notifications** window and check its contents.
* Any plugins that are listed must be re-saved in the Creation Kit now.

![Check for Form43 Plugins](/Pictures/skyrim-se/finalisation/check-for-form43-plugin.png)

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
* Raven Rock - Fix Exit on Horseback.esp **compact FormIDs**
* Dawnguard Dont Hunt Cured Vampires.esp
* ChargeDialogueFix.esp
* ImperialSoldiersEscortFix.esp
* WindhelmSegregation.esp
* Move it Dammit.esp
* Runandwalkpaces.esp
* No More Standing Too Close SSE 1-0.esp
* Realistic-Voice.esp **compact FormIDs**
* No NPC Greetings.esp
* Don'tTalkWithYourMouthFull.esp
* Random Encounter Tweaks.esp
* dD-No Spinning Death Animation Merged.esp
* SparklesSE.esp
* SimplySmallerWolfs2.esp
* SIDT - Special Edition.esp
* dD-Medium Script Range.esp
* dD-Reduced Wound Size.esp
* DeadlySpellImpacts.esp
* Enhanced Vanilla Trees SSE.esp
* ~~UniqueBorderGates-All-PointTheWay.esp~~ *already flagged*
* UniqueBorderGates-All-BetterDGEntrance.esp **compact FormIDs**
* RUSTIC SOULGEMS - Sorted.esp
* homeymealyum.esp
* GQJ_DG_vampireamuletfix.esp
* Miscellaneous Quests…as Miscellaneous Quests.esp
* Mortal Enemies - No RunWalk Changes.esp
* Realistic Melee Range.esp
* Realistic AI Detection 2 SE Lite.esp **compact FormIDs**
* Northerner Diaries in Skyrim.esp **compact FormIDs**
* Still.esp
* Hun Lovaas.esp
* NirShor-MusicalLore.esp **compact FormIDs**

> After renumbering the form IDs for Northern Diaries in Skyrim.esp and NirShor-MusicalLore.esp, the Phoenix - Merged Music Patch.esp will also be marked as updated which is intended behaviour as the previously renumbered form IDs are referenced there and updated accordingly.