---
title: "Regenerating Facegen"
weight:
type: docs
description: >
  How to regenerate facegen with the Creation Kit.
---

{{< alert color="info" title="Summary" >}}
> This module covers how to use the Creation Kit to regenerate facegen for all NPCs.<p>
> **Prerequisite(s):** [Creation Kit](/bg/tool-setup/creation-kit/), [Synthesis](/bg/tool-setup/synthesis/), [Cathedral Assets Optimizer](/bg/tool-setup/cao/){{< /alert >}}

## About Facegen

Please check the [Facegen](/bg/knowledge-base/facegen/) article for more information about facegen.

You should regenerate facegen when:

1. Changes to Head Parts, Tint Layers, etc, were made in the NPC's record.
2. New meshes for head parts (hair, eyes, mouth) were installed.
3. New textures for tint masks (make up, war paints, dirt overlays) were installed.

I recommend regenerating facegen for all NPCs (vanilla and mod-added) as one of the final steps when building a setup. The process is detailed below.

If you only need to regenerate facegen for specific NPCs, please check [the instructions at the bottom of this page](/bg/additional-modules/regenerating-facegen/#regenerating-specific-facegen).

## Prerequisites

Before you regenerate facegen please ensure that **conflict resolution is completed** at least for NPC records. The Synthesis patcher will pull data from the final overwriting record, so if NPC-modifying records are currently being overwritten and reverted to vanilla you would end up with mismatched facegen if you resolved the conflict later.

Any asset replacers for head parts and tint masks as well as any plugins modifying NPC appearance should be installed before regenerating facegen. All mods adding new NPCs should also be installed for perfect consistency across the board.

{{< alert color="warning" >}}I recommend <u>deleting</u> any facegen files from mods that add new NPCs as they will now be regenerated using assets from your setup to be consistent with each other and with the vanilla NPCs.{{< /alert >}}

### CK Fixes INI Tweak

By default, the Creation Kit will generate facetint textures of 512x512 resolution which yields small file sizes but looks fairly blurry. The resolution can be increased using [SSE Creation Kit Fixes](/bg/tool-setup/creation-kit/#creation-kit-fixes).

- Double-click **SSE Creation Kit Fixes** in your mod order.
- Switch to the **INI Files** tab and select the **skyrim64_test.ini**.
- Modify the following line:

```
[CreationKit_FaceGen]
TintMaskResolution=1024
```

You can further increase the resolution to `2048` if you intend to build a setup mostly for screenarchery and closeup pictures. Any resolution above `1024` is overkill for normal gameplay and will generate very large files.

**Remember to save your change before closing the window.**

<font size=2>*I also added `Increased tint mask resolution to 1024.` to the Notes tab for the mod.*</font>

{{< alert color="warning" >}}Remember that the vanilla game will only display tint masks in 512x512 resolution unless you added the appropriate tweak to the [SKSE.ini](/bg/additional-modules/skyrim-script-extender/#skse-ini-edits-for-skse).{{< /alert >}}

## Synthesis Patcher

To speed up the process of regenerating facegen for all NPCs that are present, we are going to use a very handy [Synthesis patcher](https://github.com/KingKai-1906/Synth-NPCs-Face-Data) by Sr. Kaio made for this express purpose. It will copy all NPC records into a single output plugin which can then be loaded into the Creation Kit for exporting facegen.

- Run **Synthesis** through Mod Organizer 2.
- Create a new group (see picture) and name it **Facegen Helper**.

![Synthesis New Group](/Pictures/bg/synthesis-new-group.png)

- Add a [patcher from Git](/Pictures/bg/synthesis-add-patcher-from-git.png) and switch to **Input**.
- As the repository link, enter `https://github.com/caiobraz/Synth-NPCs-Face-Data`.
- Select **SynthNPCsWithFaces.csproj** from the **Projects** drop-down.
- Click the blue checkmark to confirm.

![Add Synth Patcher](/Pictures/bg/additional-modules/regenerating-facegen/add-synth-patcher.png)

Give Synthesis a moment to import the new patcher. Once it is <mark>Ready</mark>, run the patcher.

![Synth Patcher Ready](/Pictures/bg/additional-modules/regenerating-facegen/synth-patcher-ready.png)

Generating the plugin should only take a few seconds, depending on how many plugins are present.

Close Synthesis when it is done.

### Patcher Output

Back in Mod Organizer 2, the newly generated plugin will have been caught by the ***Overwrite***.

- Ensure no other files are located in the ***Overwrite*** before right-clicking it and selecting **Create mod**.
- Name your new mod **Facegen Helper** and confirm.

I recommend keeping an **Outputs** separator at the bottom of your mod order and placing the new plugin here.

{{< alert color="info" >}}Feel free to jump into SSEEdit and have a look at the plugin's contents. It should contain copies of all NPC records (and therefore require all plugins that add NPCs) as well as all head parts so they are also loaded. Conveniently, the patcher.{{< /alert >}}

## Exporting Facegen

With the helper plugin in place, we can now jump into the **Creation Kit** to export facegen.

- Make sure the **Facegen Helper** plugin is active in the load order.
- Your ***Overwrite*** should be completely clean and empty.
- Run the **Creation Kit** through Mod Organizer 2.
- Click the little [folder icon](/Pictures/bg/additional-modules/porting-sle-plugins/ck-open-plugin.png) in the toolbar to open a plugin.
- Select **Facegen Helper.esp** and click **Set as Active File**.

Confirm and wait for the Creation Kit to load up the plugin. Proceed once it is [done](/Pictures/bg/additional-modules/porting-sle-plugins/ck-done-loading.png).

### NPC Records

NPC records can be found under **Actors** >> **Actor** in the Creation Kit where you can see a long list of NPCs that are currently part of the active plugin and any loaded masters.

- Check the box to **Show only active (*) forms** near the top left in the Creation Kit.

![Active Forms](/Pictures/bg/additional-modules/regenerating-facegen/ck-show-only-active-forms.png)

{{< alert color="info" >}}This is partially why we are using a helper plugin: Only NPC records present in the active plugin will show up in the list, filtering out any records that do not need to have facegen exported (such as children).{{< /alert >}}

Facegen can be exported by selecting one or several NPCs and pressing CTRL + F4. Now you can go through and select NPCs to export facegen one race at a time.*

<font size=2>\**Going one race at a time is a completely arbitrary way of splitting up the sheer amount NPCs so you do not try to export all at once and risk crashing the Creation Kit. You can also go for roughly 50-100 at a time.*</font>

**You must <u>skip</u> <mark>NordRaceAstrid</mark> (between NordRace and NordRaceVampire).** Selecting her will break all facegen.

- Sort the NPC records by **Race** (click the column and feel free to expand it).
- Select the first NPC of a race, press and hold SHIFT, scroll down to the last NPC and select it.
- Press **CTRL + F4** to export facegen for all highlighted NPCs and confirm.

For every batch of NPCs you will have to wait a moment for the Creation Kit to process all records.

Close the Creation Kit once you have exported facegen for all NPCs.

## Managing the output

At least 16GB of facegen files will now sit in your ***Overwrite*** in Mod Organizer 2. To bring down the total file size, I recommend packing all files into BSAs.

{{< alert color="info" >}}Packing the assets into archives means that they will be overwritten by any loose facegen files. This is why I recommended deleting other mods' facegen files earlier.{{< /alert >}}

- Right-click the ***Overwrite*** and select **Create Mod**.
- Name the new mod **Facegen Output** or similar and confirm.
  - *Note that the name will be used by CAO for the BSAs and plugins created in the next step.*
- Activate the new mod in the load order.

### Creating BSAs

Use the [Create BSA](/bg/tool-setup/cao/#create-bsa-profile) profile in **Cathedral Assets Optimizer** to pack up the assets.

- Open **Cathedral Assets Optimizer** and select the **SSE - Create BSA** profile.
  - *For instructions on how to create this profile, see the link above.*
- Click **Open Directory** and navigate to the mod folder: `\Mod Organizer 2\mods\Facegen Output\`.
- Select the folder and click **Run** in Cathedral Assets Optimizer.

Packing 16GB+ worth of assets will take a few minutes and I recommend stepping away in the meantime. You can check the tool's progress in the log tab.

### Finalisation

Once CAO has completed you can close it and return to Mod Organizer 2. Press F5 to refresh the UI.

The loose files will have been replaced with a set of plugins and archives. Make sure the plugins are active in the load order and that assets are overwriting correctly. If you have other BSA-packed facegen that you want to overwrite, place the plugins those BSAs are attached to below the Facegen Output plugins. Loose files will already overwrite.

**Disable Facegen Helper.** The patch is only necessary for exporting facegen.

Feel free to hop ingame and admire the results!

## Regenerating specific facegen

If you only need to export facegen for specific NPCs, you do not need to generate any Synthesis patches. Do be sure that the NPC's record is not being unintentionally overwritten and modify the **SSE Creation Kit Fixes** INI [as detailed above](/bg/additional-modules/regenerating-facegen/#ck-fixes-ini-tweak). Make sure all asset replacers for head parts and tint masks are active as well and delete existing facegen for that NPC.

- Load up the plugin in which the NPC is created in the **Creation Kit** (this can be a vanilla master file or a mod).
- Find the NPC(s) in question under **Actors** >> **Actor** and select it/them.
- Hit **CTRL + F4** to export facegen and confirm.

Wait for the CK to process everything and close it when it is done.

In Mod Organizer 2, be sure to move the facegen assets out of the ***Overwrite***. You can place them in the original mod's folder or in a separate one (the latter is recommended because otherwise you have to repeat the process when the mod is updated).