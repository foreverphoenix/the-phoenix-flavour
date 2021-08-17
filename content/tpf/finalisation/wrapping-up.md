---
title: "Wrapping Up"
weight: 1
type: docs
description: >
  Final edits and touches.
---

## Conflict Resolution Patch

- Create a **FINAL PATCHES** separator in Mod Organizer 2.
- Download the [Conflict Resolution Patch](https://www.nexusmods.com/skyrimspecialedition/mods/14223?tab=files) from the guide’s Nexus page.
- Install it as usual, place it last below the **FINAL PATCHES** separator, and activate it.

## Facegen

Facegen for all vanilla and mod-added NPCs was regenerated with TPF's appearance section as base. That means all improvements to assets such as warpaints will now also apply to NPC's faces, plus their facetint textures is twice the vanilla resolution.

- Download [The Phoenix Flavour - Facegen](https://www.nexusmods.com/skyrimspecialedition/mods/14223?tab=files) from the guide's Nexus page.
- Install the mod as usual, place it below the Conflict Resolution Patch in the mod order, and activate it.

## Load Order TXT

The pre-made TXT will arrange your plugins exactly like the way they are sorted in my personal setup. This is much faster than adjusting the load order manually or setting up LOOT with custom rules.

- Click anywhere in the right pane (load order) and select **Enable all**.

> This will ensure all plugins are active prior to sorting them. Plugins may be unchecked automatically when renaming their file extensions from ESL to ESP as we did multiple times throughout the guide.

### Applying the load order

* Download the [Universal Load Order TXT](https://www.nexusmods.com/skyrimspecialedition/mods/14223?tab=files) from the guide’s Nexus page.
* Open the archive and extract the **loadorder.txt** to `Mod Organizer 2\profiles\The Phoenix Flavour`.
* Restart Mod Organizer 2 and the changes will be applied.

After applying the loadorder.txt and restarting MO2, there should be no plugins below the **The Phoenix Flavour - Facegen.esp** in the load order (right pane).

If there are other plugins below the Facegen plugin, you either made a mistake during the mod installation, or a mod was updated and the loadorder.txt is not accounting for it yet. Go back to the mod(s) in question (they will be highlighted in the mod order when you click on the plugin in the load order) and re-install them according to the instructions in the guide.

If you are unable to resolve all issues, please join us on Discord and post your Modwat.ch link or a picture of the bottom of your load order in the `#tpf-guide-support` channels.

## Check for MO2 Warnings

In Mod Organizer 2, check the notification icon in the top right corner (see screenshot below). Any issues found there should be fixed now. If it is greyed out, there are no warnings and you are good to go!

There are multiple different warnings that you may encounter:

- **Missing Masters:** One of your plugins is missing a master file. It is marked with an exclamation mark in your load order. This is most likely due to skipping a mod that was not optional or selecting the wrong option in a FOMOD installer. Go back to the mod’s instructions in the guide and double-check everything.
- **Form 43 Plugin:** You forgot to re-save plugins in the Creation Kit. Re-save them now.
- **Outdated SKSE Plugin:** Check the plugin's mod page to see if there is a new version.
- **Files in Overwrite:** Share a screenshot on Discord so we can take a look.

![Check for Form43 Plugins](/Pictures/tpf/finalisation/check-for-form43-plugin.png)

