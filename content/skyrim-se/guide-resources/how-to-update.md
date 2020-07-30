---
title: "How To Update"
weight: 4
type: docs
description: >
  Instructions on how to update various tools and some mods.
---

## Mod Organizer 2

It is possible to update Mod Organizer 2 without affecting your setup if you leave certain files and folders intact. You can do this anytime, and it will not affect your saves, mod list, or even your UI settings.

### Remove the old version

- Close Mod Organizer 2 if you have it open in the background.
- Navigate to your existing Mod Organizer 2 installation.
- Delete all files and folders except for the following (see picture below):
  - `mods\`
  - `profiles\`
  - `ModOrganizer.ini`

![MO2 Before Update](/Pictures/guide-resources/mo2-before-update.png)

### Install the new version

- Download the new version of Mod Organizer 2 (Archive).
- Open the archive and move all files into your existing directory with the left-over files.
- Open Mod Organizer 2 as usual and you will see that your setup is fully intact.

## Cathedral Assets Optimizer

In order to update CAO without removing the custom TPF profiles, simply do the following:

- Navigate to `Your Modding Folder\Tools\Cathedral Assets Optimizer`.
- Delete everything except for the **profiles** folder.
- Download the new version of Cathedral Assets Optimizer.
- Open the archive and move everything except into the CAO folder.
- Merge and overwrite when prompted.

> This will leave the TPF profiles intact but overwrite the default profiles in case anything was changed about them.

## BethINI

- Navigate to `Your Modding Folder\Tools\BethINI` and delete everything inside that folder.
- Download the latest version of BethINI from the Nexus.
- Open the archive and extract everything into the now empty BethINI folder.
- Re-generate your INI files ([instructions here](https://thephoenixflavour.com/skyrim-se/guide-resources/various-tutorials/)).

## DynDOLOD

There is generally no need to update DynDOLOD and re-generate LOD for every new DynDOLOD update, especially when you're in the middle of a playthrough. However, if you change something about the landscape (the Alternate Branch Textures color for Enhanced Vanilla Trees for example), you need to re-run DynDOLOD and you should update it first.

**The instructions below are for updating DynDOLOD on an ongoing playthrough.**

### Disabling DynDOLOD

- Before you change anything in MO2, open the game and load your save.
- Make sure you're outside (not in an interior cell) in Tamriel.
- Press ESC and go into the DynDOLOD MCM.
- Under **Main >> Options**, uncheck **DynDOLOD is active**.
- A message box will pop up, notifying that DynDOLOD was deactivated (see below).
- Click **OK**, close the MCM, and go into an interior cell (any house or cave will do).
- Save and quit the game.

![Deactivate DynDOLOD](/Pictures/guide-resources/deactivate-dyndolod.png)

### Resaving without DynDOLOD

- Back in Mod Organizer 2, delete both **TexGen Output** and **DynDOLOD Output**.
- Start the game, load your save and create a new save. Then quit again.

### Updating DynDOLOD

- Download the **DynDOLOD Resources SE** main file from the [DynDOLOD](https://www.nexusmods.com/skyrimspecialedition/mods/32382?tab=files) mod page through MO2.
- Re-install it ([FOMOD instructions are here](https://thephoenixflavour.com/skyrim-se/mod-installation/06-graphics-baseline/)) and **Replace** the existing installation when prompted.
- Navigate to `Your Modding Folder\Tools\DynDOLOD` and delete everything inside the folder.
- Download the **DynDOLOD** main file [DynDOLOD](https://www.nexusmods.com/skyrimspecialedition/mods/32382?tab=files) mod page manually.
- Open the archive and extract everything into the now empty **DynDOLOD** folder.
- Go back to the [DynDOLOD](https://thephoenixflavour.com/skyrim-se/finalisation/04-dyndolod/) page in the Finalisation and follow all steps from **TexGen Configuration** onwards.
- After regenerating TexGen and DynDOLOD, load your save, and continue your playthrough!

> Since the folder wasn't changed, there is no need to update the file paths to the TexGen and DynDOLOD executables in MO2. They are still the same.

## Adamant - A Perk Overhaul

It is entirely possible to update Adamant in the middle of a playthrough with the help of Ish's Respec Mod. However, big updates for Adamant often require the guide's CRP to be updated as well which in turn is often accompanied by a guide update. So while Adamant is basically always safe to update, the CRP is not.

When Adamant as well as the guide and CRP received a save-safe update, you can do the following to update:

- Load your existing save with the old versions of Adamant and the CRP.
- Buy a **Draught of Fate Unwound** from an Alchemist (Elgrim in Riften is guaranteed to sell some).
- Drinking it will refund all your perks. Wait until you are notified that the process is completed.
- Save and quit the game.
- Update your TPF installation: Adamant, CRP, and anything else that may have changed.
- Load your save and spend your previously refunded perk points.

## Various Mods

### Creation Kit Fixes

- Download the newest version of the **CK64Fixes Release x.x** main file.
- Open the archive and extract all files into your **root** folder.
- Overwrite when prompted.

### SSE Engine Fixes

- If (Part 1) was updated, simply click **Mod Manager Download** and install through MO2 as usual.
- If (Part 2) was updated, click **Manual Download**.
- Open the archive and extract all files into your **root** folder.
- Overwrite when prompted.