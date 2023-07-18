---
title: "ModGroups"
weight:
type: docs
description: >
  About ModGroups and how to use them.
---

## About ModGroups

This article summarises some basic information on **ModGroups**.

{{< alert color="info" >}}I recommend reading the article on [Conflict Management](/bg/knowledge-base/conflict-management/) first.{{< /alert >}}

**ModGroups** are a purely cosmetic feature of [SSEEdit](/bg/tool-setup/sseedit/). They are meant to selectively hide conflicts that have already been reviewed and were found to be intentional, and do not affect the game at all.

When working through a large load order, some conflicts will disappear after changing the position of a plugin or creating a patch, but the majority is typically intentional which means SSEEdit with a filter for conflicts will always look like a rainbow - like there is still a lot of work to be done.

Rather than constantly coming back to the same record only to conclude that its conflict(s) require no intervention, it can be helpful to create a ModGroup that *hides* those conflicts.

{{< alert color="info" >}}Please consult the official [ModGroups documentation](https://tes5edit.github.io/docs/4-modgroups.html) on the Tome of xEdit site with any further questions.{{< /alert >}}

### Comparison

**Before:**

![Conflicts Pre-ModGroups](/Pictures/bg/core-module/conflicts-pre-modgroups.png)

**After:**

![Conflicts Post-ModGroups](/Pictures/bg/core-module/conflicts-post-modgroups.png)

## Creating ModGroups

ModGroups are created in SSEEdit, ideally after [filtering for conflicts](/bg/additional-modules/filter-for-conflicts/). If you have determined that all conflicts between a given pair of plugins (or a larger group) are fully intentional, you can create a new ModGroup for them.

- Highlight both/all plugins in the left pane.
- Right-click the selected plugins and select **Create ModGroup**.

### CRC32s

You will be asked whether you wish to include current CRC32s.

[CRCs](https://en.wikipedia.org/wiki/Cyclic_redundancy_check) are fragments of code that can be used to identify and compare files. You can see the current CRCs of your loaded plugins in the left pane in SSEEdit:

![CRCs](/Pictures/bg/knowledge-base/modgroups/crcs.png)

The CRC of a plugin will change when the plugin is modified (when it is renamed, ESL-flagged, records are edited/added/removed, etc). Including the current CRCs in the ModGroup means that it will <u>only</u> be valid for *these specific versions* of the plugins and break if a mod was modified (either by you or by the author in an update).

While updating CRCs in ModGroups is not particularly time-consuming, I nevertheless find it more convenient <u>not</u> to include the CRCs. This does mean that ModGroups may, at times, hide conflicts you have not yet reviewed after an updated to a plugin, though you can always do routine checks without ModGroups loaded later on.

{{< alert color="info" >}}My personal recommendation is not to include CRCs, but ultimately this is up to you.{{< /alert >}}

### ModGroup Flags

Next, you will be able to modify various settings. You can change them by clicking in the cell for the column and row of the setting and plugin, respectively.

- **Optional:** Plugins marked as optional do not have to be present for the ModGroup to be valid.
- **Target:** Conflicts in this plugin can be hidden.
- **Source:** Overwriting records in this plugin will hide the overwritten records in previous plugins.
- **Forbidden:** Plugins marked as forbidden will invalidate the ModGroup if present.
- **Ignore LO:** If empty, the load order of the plugins must be as listed in the ModGroup for it to be valid.
  - *Always:* Any load order is valid
  - *In Block:* Must adhere to load order of all plugins with this flag

{{< alert color="info" >}}For a more detailed overview, check the [Tome of xEdit](https://tes5edit.github.io/docs/4-modgroups.html#ModGroupFlags).{{< /alert >}}

### Naming Scheme

After adjusting the flags you need to enter a name for your new ModGroup at the top. The short version is: Name your Modgroup whatever you like.

Now, the long version.

If you use ModGroups a lot, you will probably create several dozen for a decently-sized load order in which case it makes sense to adhere to some kind of system. For example, I name my ModGroups after the plugins they contain, starting with the **Source** plugin, then going through the target plugins in the order they are loaded in.

My ModGroup for the two plugins from Realistic Water Two and the official master files (minus Skyrim.esm which cannot have critical conflicts) is named as follows:

- RealisticWaterTwo-OfficialMasterFiles-RealisticWaterTwoESM
  - *ModGroup for RealisticWaterTwo.esp, RealisticWaterTwo - Resources.esm, and the official master files*

If a patch is included, I usually combine the names of the target mods:

- RealisticWaterTwoMyrwatch-CCMyrwatch-RealisticWaterTwo
  - *ModGroup for Realistic Water Two, its CC Myrwatch Patch, and the Myrwatch creation itself*

This is a system that works *for me*. Please feel free to come up with your own as I would not call mine the objectively "best" by any stretch of the imagination.

### Source Mod

After entering a name for your ModGroup and click **OK**, you will be asked which plugin to "store" the ModGroup with.

To understand what this means, you need to know that a .modgroups file is essentially a text file with the names of the plugins inside. The file itself is named after the plugin it is associated with and only loads if that plugin is present. This is similar to plugin INIs and BSAs.

**Every ModGroup needs to be attached to a plugin.**

My ModGroups are always made for one specific plugin with the idea that if I remove the plugin, I also remove the ModGroup. This kind of modularity enables a good amount of flexibility where removing a mod does not force me to redo a number of ModGroups.

I recommend adopting a similar system with as few Source plugins as possible per ModGroup and storing each ModGroup with the Source plugin that is lowest in the load order.

- Select a plugin from the list, check it, and click **OK**.
- Click **OK** again to activate your ModGroup.

## ModGroups in MO2

ModGroup files will, as usual, be caught by the ***Overwrite*** after closing SSEEdit.

From there, you can either move the files to a **ModGroups** mod folder <u>or</u> create separate mod folders for each mod's ModGroups (this will only be one file unless that mod has more than one plugin).

As you may have guessed, I prefer the modularity and flexibility of separate mod folders:

- Realistic Water Two
- Realistic Water Two - ModGroups
- GKB Waves Reborn
- GKB Waves Reborn - ModGroups 

Handle your own ModGroups as you see fit.

## Editing ModGroups

ModGroups can be modified in two ways:

1. Directly through the **SSEEdit** interface by right-click in the left pane and selecting **Edit ModGroup**. This will allow you to change ModGroup flags but you cannot add or remove plugins.
2. Indirectly through a **text editor**. The .modgroups files can be opened in Notepad++ and similar software and edited there. This way, you *can* add or remove plugins (as well as rename plugins or change CRCs).