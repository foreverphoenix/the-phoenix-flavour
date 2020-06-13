---
title: "Arthmoor's Towns"
weight: 16
type: docs
description: >
  Instructions for the new towns by Arthmoor.
---

{{% alert title="Warning" color="warning" %}}
If you install this section, you will need to re-generate DynDOLOD later on.{{% /alert %}}

## The Dilemma

The five additional town mods by Arthmoor were removed from the main guide in the 3.2 update. The primary reason for that was that the majority of the userbase felt they detracted from immersion rather than adding to it due to the fact that the NPCs only have generic dialogue. They will not interact with the player in any way, there are no location specific comments or quests. The towns may feel like props, cardboard cutout stand-ins, rather than actual settlements.

A smaller part of the userbase argued however that even as pretend-towns, they add to the world of Skyrim. Without Arthmoor's Oakwood, the hold of Falkreath has zero settlements beyond its capital. Oakwood is also conveniently close to Lakeview Manor, the Hearthfire player home overlooking Lake Ilinalta, connecting the Manor to civilisation. 

It is therefore up to the individual user to decide what is more immersion-breaking: Towns where nobody interacts with you, or no towns at all.

**Please note that you need to either install all five towns or skip them all.**

## Helarchen Creek

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/4043?tab=files)

- **Main Files:** Helarchen Creek

#### Mod & Load Order

- Place the mod below **Provincial Courier Service** in the mod order and active it.
- Move the plugin below **Provincial Courier Service.esp** in your load order.

## Keld-Nar

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/14353?tab=files)

- **Main Files:** Keld-Nar

#### Mod & Load Order

- Place the mod below **Provincial Courier Service** (or previous Arthmoor Town Mods) in the mod order and active it.
- Move the plugin below **Provincial Courier Service.esp** (or previous Arthmoor Town Mods) in your load order.

#### Additional Instructions

- Run **SSEEdit** through Mod Organizer 2.
- In the plugin selection window, click **OK** to load all plugins.
- Wait until SSEEdit has finished loading.
- Find **Keld-Nar.esp** in the left pane and double-click it.
- Navigate to `Dialogue Topic\PerkInvestorBranch1Topic1`.
- Right-click and remove the following record:
  - `000B1FE9`
- Click **Yes, I am sure** when the warning window pops up and confirm to delete.
- Close SSEEdit. Click **OK** to save your changes.

> The record contains only one edit that is already made in the USSEP but overrides another one from Trade & Barter. The simplest solution is to just delete it.

![Keld-Nar - Delete Record](/Pictures/customisation/keldnar_delete_record.png)

## Simple Children - Keld-Nar Patch 

#### Download Instructions

- You already downloaded the necessary file during the main guide.

#### Installation Instructions

- Find **Simple Children - Patches** in your mod order, right-click it and select **Reinstall**.
- In the FOMOD, unselect everything except the **Keld-Nar** option on the second page.
- On the third page, set the **Prince and Pauper** and **Adopt Aventus Aretino** options both to **None**.
- After clicking **Install**, select **Rename** (we do not want to replace the original file).
- Rename the file to **Simple Children - Keld-Nar Patch** and click **OK**.

#### Mod & Load Order

- Place the mod below **Simple Children - Patches** in the mod order and active it.
- Move the plugin below **3D_FacegenForKids.esp** in your load order.

## Telengard

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/17423?tab=files)

- **Main Files:** Telengard

#### Mod & Load Order

- Place the mod below **Provincial Courier Service** (or previous Arthmoor Town Mods) in the mod order and active it.
- Move the plugin below **Provincial Courier Service.esp** (or previous Arthmoor Town Mods) in your load order.

## The Fall of Granite Hill

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/22512?tab=files)

- **Main Files:** The Fall of Granite Hill

#### Mod & Load Order

- Place the mod below **Provincial Courier Service** (or previous Arthmoor Town Mods) in the mod order and active it.
- Move the plugin below **Provincial Courier Service.esp** (or previous Arthmoor Town Mods) in your load order.

## Oakwood

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/27564?tab=files)

- **Main Files:** Oakwood

#### Mod & Load Order

- Place the mod below **Provincial Courier Service** (or previous Arthmoor Town Mods) in the mod order and active it.
- Move the plugin below **Provincial Courier Service.esp** (or previous Arthmoor Town Mods) in your load order.

## Landscape Fixes for Grass Mods - Oakwood

#### Download Instructions

- You already downloaded the necessary file during the main guide.

#### Installation Instructions

- Find **Landscape Fixes For Grass Mods - Patches for Arthmoor's Town** in your mod order, right-click it and select **Reinstall**.
- In the FOMOD, select only the **Patch for Oakwood** option.
- After clicking **Install**, select **Rename** (we do not want to replace the original file).
- Rename the file to **Landscape Fixes for Grass Mods - Oakwood Patch** and click **OK**.

#### Mod & Load Order

- Place the mod below **Landscape Fixes For Grass Mods - Patches for Arthmoor's Town** in the mod order and active it.
- Move the plugin below **Landscape For Grass Mods -Provincial Courier PATCH.esp** in your load order.

## Lanterns of Skyrim II - Patches for Arthmoor's Towns

#### Download Instructions

- You already downloaded the necessary file during the main guide.

#### Installation Instructions

- Click the spanner icon to the right of the profile drop-down and select **Create empty mod** (see screenshot below).
- Enter **Lanterns of Skyrim II - Patches for Arthmoor's Towns** as the name and click **OK**.
- Right-click the new, empty mod and select **Open in Explorer**.
- In your **Downloads** tab, find the **Lanterns Of Skyrim II - FOMOD v2.0** archive.
- Right-click it and select **Open File**.

![Create empty mod](/Pictures/finalisation/create_empty_mod.png)

At this point you need to extract the patches for Arthmoor's town mods. Move all files from the respective folder into your new mod folder. When asked whether you want to merge folders, click **Yes**.

- **Helarchen Creek:** Extract the meshes, textures, and plugin from the `LoS II - HC` folder.
- **Oakwood:** Extract the meshes, textures, and plugin from the `LoS II - Oak` folder.
- **Telengard:** Extract the plugin from the `LoS II - Tel` folder.
- **The Fall of Granite Hill:** Extract the meshes, textures, and plugin from the `LoS II - TFGH` folder.
- There is no patch for Keld-Nar.

 The resulting mod folder should look like this:

![LoS II Town Patches](/Pictures/customisation/los_ii_town_patches.png)

#### Mod Order

- Back in Mod Organizer 2, press F5 to refresh.
- Place the mod below the **Morrowloot Ultimate - INIGO Patch** in the mod order and activate it.
- Move the plugins below **MLU - Inigo.esp** in the load order.

## Arthmoor's Towns - Patch Pack

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/26092?tab=files)

- **Main Files:** Arthmoor's Towns - Patch Pack

#### FOMOD Instructions

- Since both **Realistic Water Two** and **Trade & Barter** are required mods in the guide, you will need to select the patches for all town mods that you have installed.

#### Mod & Load Order

- Place the mod below **Morrowloot Ultimate - INIGO Patch** in the mod order and active it.
- Move all plugins below **MLU - Inigo.esp** in your load order.
