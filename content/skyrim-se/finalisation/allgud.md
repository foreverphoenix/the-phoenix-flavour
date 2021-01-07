---
title: "All Geared Up Derivative"
weight: 3
type: docs
description: >
  Generating plugins and meshes for AllGUD.
---

## SSEEdit Scripts

While we install the base mod already, there is a number of additional steps to complete before the mod is fully implemented.

- Download the **AllGUD xEdit Scripts** main file from the [AllGUD](https://www.nexusmods.com/skyrimspecialedition/mods/28833?tab=files) mod page.
- Open the downloaded archive and double-click the folder inside.
- Extract everything from the **Edit Scripts** folder to `Your Modding Folder\Tools\SSEEdit\Edit Scripts`.

### Fixed texture script

One of the AllGUD scripts assigns faulty texture file paths to the generated meshes which will prevent the resulting objects from looking as intended. Fortunately, this was fixed by duskyBabz and provided to us ([source](https://github.com/foreverphoenix/the-phoenix-flavour/issues/26)).

- Download the fixed script from [Mediafire](https://www.mediafire.com/file/fd0d6qj78lpjbas/AllGUD_AlternateTextureModelsplosion_-_Fixed.pas/file).
- Move the file to `Your Modding Folder\Tools\SSEEdit\Edit Scripts`.

## Alternate Textures Patches

Before we can generate weapon meshes, there are some weapons that use Alternate Textures which doesn't work with AllGUD. Thankfully, one of the AllGUD SSEEdit scripts was created to patch these weapons.

- Run SSEEdit through Mod Organizer 2.
- In the plugin selection window, simply click **OK** to load all plugins.
- Wait until SSEEdit returns **Background loader: finished**.
- Click anywhere in the left pane (plugin list) and hit **CTRL + A** to select all plugins.
- Right-click the selected plugins and select **Apply Script**.
- Select the **AllGUD AlternateTextureModelsplosion - Fixed** script and click **OK**.
- Enter **AllGUD - Alternate Textures Patch** as file name and click **OK**.
- Leave the next two windows blank and only click **OK** both times.
- Eventually SSEEdit will return **Done: Applying script**, and you can close the window.
- Click **OK** when prompted to save your changes.

![Alternate Textures Patch](/Pictures/skyrim-se/finalisation/allgud-alt-textures-fixed.png)

### Output

- Back in Mod Organizer 2, scroll down all the way to the **Overwrite** folder which contains the new plugin and meshes.
- Right-click it and select **Create Mod**.
- Enter **AllGUD - Alternate Textures Patch** as the name and click **OK**.
- Activate the new mod in your mod order.
- The plugin will now show up at the bottom of your load order, make sure it is checked.

## Weapon Mesh Generator

- In Mod Organizer 2, click the tools icon above the mod order pane and select **Create empty mod**.
- Enter **AllGUD - Weapon Meshes** as the name and click **OK**.
- Leave the new mod at the bottom of your mod order and activate it.

![Create empty mod](/Pictures/skyrim-se/finalisation/create-empty-mod.png)

### Fixed Script

The original script has a bug. A fixed version is available on the Nexus.

- Download the [AllGUD Weapon Mesh Generator Script Fix](https://www.nexusmods.com/skyrimspecialedition/mods/38151?tab=files) manually.
- Open the downloaded archive and extract the script to `Your Modding Folder\Tools\SSEEdit\Edit Scripts`.
- Confirm when asked to overwrite.

### Running the script

- Run SSEEdit through Mod Organizer 2.
- In the plugin selection window, simply click **OK** to load all plugins.
- Wait until SSEEdit returns **Background loader: finished**.
- Click anywhere in the left pane (plugin list) and hit **CTRL + A** to select all plugins.
- Right-click the selected plugins and select **Apply Script**.
- Select the **AllGUD Weapon Mesh Generator** script and click **OK**.
- Click on the empty field below **Output Meshes Folder** and navigate to `Mod Organizer 2\mods`.
- Select the **AllGUD - Weapon Meshes** folder you created in the previous step and click **OK**.
- Click **Start** to begin generating the meshes.
- Eventually SSEEdit will return **Done: Applying script**, and you can close the window.

![AllGUD Weapon Patcher](/Pictures/skyrim-se/finalisation/allgud-weapon-meshes.png)

## Skeleton Patcher

- In Mod Organizer 2, once again click the tools icon above the mod order pane and select **Create empty mod**.
- Enter **AllGUD - Skeleton Meshes** as the name and click **OK**.
- Leave the new mod at the bottom of your mod order and activate it.

![Create empty mod](/Pictures/skyrim-se/finalisation/create-empty-mod.png)

### Running the script

- Run SSEEdit through Mod Organizer 2.
- In the plugin selection window, simply click **OK** to load all plugins.
- Wait until SSEEdit returns **Background loader: finished**.
- Right-click anywhere in the left pane and select **Apply Script**.
- Select the **AllGUD Skeleton Patcher** script and click **OK**.
- Click on the empty field below **Output Meshes Folder** and navigate to `Mod Organizer 2\mods`.
- Select the **AllGUD - Skeleton Meshes** folder you created in the previous step and click **OK**.
- Click **Start** to begin generating the meshes.
- Eventually SSEEdit will return **Done: Applying script**, and you can close the window.

![AllGUD Skeleton Patcher](/Pictures/skyrim-se/finalisation/allgud-skeleton-patcher.png)