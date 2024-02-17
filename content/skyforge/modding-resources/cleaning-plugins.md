---
title: "Cleaning Plugins"
weight:
type: docs
description: >
  How to clean plugins with SSEEdit QAC.
---

{{< alert color="info" title="Summary" >}}
> This module covers how to "clean" plugins, including the official master files and creations, with SSEEdit.<p>
> **Prerequisite(s):** [SSEEdit](/skyforge/tool-setup/sseedit/) (including Quick Auto Clean), [LOOT](/skyforge/tool-setup/loot/) (optional), [LOOT Warning Checker](/skyforge/tool-setup/loot-warning-checker) (optional){{< /alert >}}

## Quick Auto Clean

{{< alert color="warning" >}}If you are unsure whether you should "clean" any plugins, read [this article](/skyforge/knowledge-base/cleaning-plugins/) first.{{< /alert >}}

Plugin "cleaning" used to be a semi-involved process with multiple steps but has since been simplified. It is done with [SSEEdit](/skyforge/tool-setup/sseedit/) in the **Quick Auto Clean** mode. SSEEdit comes with a preconfigured executable for it.

You can clean plugins either by manually running SSEEdit in -QAC mode or by using [LOOT Warning Checker](/skyforge/tool-setup/loot-warning-checker/) which is slightly faster.

I will demonstrate both methods using the official master files as an example.

{{< alert color="info" >}}When cleaning plugins is needed, you can use LOOT to find plugins that are "unclean". However, keep in mind that LOOT's masterlist is limited and may be outdated or incomplete. If you missed any plugins, DynDOLOD NG should warn you about them later.{{< /alert >}}

### Backups

When modifying offical files (the official master files or creations), I am in the habit of creating *copies* rather than modifying the files in the default installation folder. This has the advantage that you can move or verify files without having to repeat the process.

{{< alert color="info" >}}In the case of an actual update to the game, (some of) the official files are usually modified in which case you do need to repeat the process with the new version(s).{{< /alert >}}

- Create a new mod in MO2 and name it **Official Master Files - Cleaned**.
- Copy the following ESMs from your installation folder into the new mod folder:
  - Update.esm
  - Dawnguard.esm
  - Hearthfires.esm
  - Dragonborn.esm
- Place the new mod below the originals in Mod Organizer 2.

{{< alert color="danger" >}}Skyrim.esm cannot and *should not* be cleaned. It consists exclusively of new records and has no masters.{{< /alert >}}

![OMF Backups](/Pictures/skyforge/modding-resources/cleaning-plugins/overwrite-omf.png)

For creations I tend to copy all plugins that need cleaning into a similar **Creation Club - Cleaned** mod before processing them. LOOT will tell you which creations have ITMs and/or deleted references.

For plugins from mods I would not create separate copies, but add to the **Notes** tab in Mod Organizer 2 that the plugin was modified as a reminder to yourself. This way, you will know that you need to check and possibly re-clean the plugin when the mod is updated.

### Manual Cleaning

Plugins can be "cleaned" with SSEEdit Quick Auto Clean <u>one at a time</u>. When cleaning the official master files, start with Update.esm and proceed according to their load order (Dawnguard > HearthFires > Dragonborn). When cleaning plugins from mods, clean masters before dependencies.

- Run **SSEEdit QAC** through Mod Organizer 2.
- Check the plugin you wish to clean and click **OK**.

![Cleaning 1](/Pictures/skyforge/modding-resources/cleaning-plugins/cleaning-1.png)

The remainder of the process is fully automated and will take a few minutes. Simply wait for SSEEdit to return `Quick Clean mode finished` at which point you can close the tool.

### LOOT Warning Checker

The [LOOT Warning Checker](/skyforge/tool-setup/loot-warning-checker/) plugin will list all plugins that the LOOT Masterlist considers in need of cleaning with a handy **Fix** button that will automatically run SSEEdit QAC. For plugins that are in the masterlist, this is slightly faster than launching QAC manually.

![Cleaning 2](/Pictures/skyforge/modding-resources/cleaning-plugins/fix-to-clean.png)