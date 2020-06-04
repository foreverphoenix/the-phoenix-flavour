---
title: "All Geared Up Derivative"
weight: 3
type: docs
description: >
  Generating plugins and meshes for AllGUD.
---

## 3.1 xEdit Scripts

While we install the base mod already in Step 38, there is a number of additional steps to complete before the mod is fully implemented.

- Download the **AllGUD xEdit Scripts** main file from the [AllGUD](https://www.nexusmods.com/skyrimspecialedition/mods/28833?tab=files) mod page.
- Open the downloaded archive and double-click the folder inside.
- Extract all files from the **Edit Scripts** folder to `Your Modding Folder\Tools\SSEEdit\Edit Scripts`.

## 3.2 Alternate Textures Patches

### 3.2.1 Running the script

Before we can generate weapon meshes for all mods, there are three mods that use Alternate Textures for some new weapons which doesn't work with AllGUD. Thankfully, one of the AllGUD SSEEdit scripts was created to patch these mods.

- Run SSEEdit through Mod Organizer 2.
- In the plugin selection window, simply click **OK** to load all plugins.
- Wait until SSEEdit returns **Background loader: finished**.
- Click anywhere in the left pane (plugin list) and hit CTRL + A to select all plugins.
- Right-click the selected plugins and select **Apply Script**.
- Select the **AllGUD AlternateTextureModelsplosion** script and click **OK**.
- Enter **AllGUD - Alternate Textures Patch** as file name and click **OK**.
- Leave the next two windows blank and only click **OK** both times.
- Eventually SSEEdit will return **Done: Applying script**, and you can close the window.

### 3.2.2 Output

- Back in Mod Organizer 2, scroll down all the way to the **Overwrite** folder which contains the new plugin and meshes.
- Right-click it and select **Create Mod**.
- Enter **AllGUD - Alternate Textures Patch** as the name and click **OK**.
- Activate the new mod in your mod order.
- The plugin will now show up at the bottom of your load order, make sure it is checked.

### 3.2.3 Clean Masters

Unfortunately the plugin was assigned half our load order as master files so we will use SSEEdit to clean out master files that are not direct dependencies. Only the relevant plugins will remain master files to the plugin.

- Run SSEEdit through Mod Organizer 2.
- In the plugin selection window, simply click **OK** to load all plugins.
- Wait until SSEEdit returns **Background loader: finished**.
- Scroll down to the bottom and right-click **AllGUD - Alternate Textures Patch.esp**.
- Select **Clean Masters** and click **Yes I'm absolutely sure** when the warning window pops up.
- Close SSEEdit and click **OK** to save the changes.

## 3.3 Weapon Mesh Generator

### 3.3.1 New Mod Folder

- In Mod Organizer 2, click the spanner icon above the mod order pane and select **Create empty mod**.
- Enter **AllGUD - Weapon Meshes** as the name and click **OK**.
- Leave the new mod at the bottom of your mod order and activate it.

![Create empty mod](/Pictures/finalisation/create_empty_mod.png)

### 3.3.2 Running the script

- Run SSEEdit through Mod Organizer 2.
- In the plugin selection window, simply click **OK** to load all plugins.
- Wait until SSEEdit returns **Background loader: finished**.
- Click anywhere in the left pane (plugin list) and hit CTRL + A to select all plugins.
- Right-click the selected plugins and select **Apply Script**.
- Select the **AllGUD Weapon Mesh Generator** script and click **OK**.
- Click on the empty field below **Output Meshes Folder** and navigate to `Mod Organizer 2\mods`.
- Select the **AllGUD - Weapon Meshes** folder you created in the previous step and click **OK**.
- Click **Start** to begin generating the meshes.
- Eventually SSEEdit will return **Done: Applying script**, and you can close the window.

![AllGUD Weapon Patcher](/Pictures/finalisation/allgud_weapon_meshes.png)

## 3.4 Skeleton Patcher

### 3.4.1 New Mod Folder

- In Mod Organizer 2, click the spanner icon above the mod order pane and select **Create empty mod**.
- Enter **AllGUD - Skeleton Meshes** as the name and click **OK**.
- Leave the new mod at the bottom of your mod order and activate it.

### 3.4.2 Running the script

- Run SSEEdit through Mod Organizer 2.
- In the plugin selection window, simply click **OK** to load all plugins.
- Wait until SSEEdit returns **Background loader: finished**.
- Right-click anywhere in the left pane and select **Apply Script**.
- Select the **AllGUD Skeleton Patcher** script and click **OK**.
- Click on the empty field below **Output Meshes Folder** and navigate to `Mod Organizer 2\mods`.
- Select the **AllGUD - Skeleton Meshes** folder you created in the previous step and click **OK**.
- Click **Start** to begin generating the meshes.
- Eventually SSEEdit will return **Done: Applying script**, and you can close the window.

![AllGUD Skeleton Patcher](/Pictures/finalisation/allgud_skeleton_patcher.png)