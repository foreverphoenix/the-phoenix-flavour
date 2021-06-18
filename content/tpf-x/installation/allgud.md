---
title: "AllGUD"
weight: 11
type: docs
description: >
  Instructions for All Geared Up Derivative.
---

## AllGUD

All Geared Up Derivative, or AllGUD for short, is a pretty involved mod. It includes dual sheath redux functionality (meaning if you're dual wielding, both weapons are sheathed instead of only the main hand one) as well as always visible gear (so your bow doesn't magically disappear when you swap to sword and shield). Thanks to its implementation, compatibility can ensured effortlessly with SSEEdit patchers which are capable of generating dual sheath meshes from scratch.

AllGUD also adds many other (toggleable) pieces of visible equipment such as potions on your belt, a torch, money pouch, and more. All of these as well as the weapons can be enabled for both the player and NPCs, and there are many more customisation options in AllGUD's MCM.

Since release 4.6, TPF is using [Simple Dual Sheath](https://www.nexusmods.com/skyrimspecialedition/mods/50049) instead which does not include always visible gear or additional visible equipment but does not require running patchers either. AllGUD is more involved than Simple Dual Sheath, both in the installation and ingame while offering a great many more features.

### Separators

Create an **ALL GEARED UP - TPF-X** separator below the other TPF-X separators.

If you haven't already, also create a new **PATCHER OUTPUT - TPF-X** separator to place below the regular **PATCHER OUTPUT** separator.

## AllGUD and related mods

**You must DISABLE Simple Dual Sheath in the mod order before you proceed.**

### [**All Geared Up Derivative (AllGUD)**](https://www.nexusmods.com/skyrimspecialedition/mods/28833?tab=files)

#### Download Instructions 

- **Main Files:** All Geared Up Derivative SE

### [**AllGUD - RUSTIC ANIMATED POTIONS Patch**](https://www.nexusmods.com/skyrimspecialedition/mods/49669?tab=files)

#### Download Instructions

- **Main Files:** AllGUD - Rustic Animated Potions Patch

### [**AllGUD Conditions Fix**](https://www.nexusmods.com/skyrimspecialedition/mods/26092?tab=files)

#### Download Instructions

- **Main Files:** AllGUD Conditions Fix

## AllGUD Scripts

- Download the **AllGUD xEdit Scripts** main file from the [**AllGUD**](https://www.nexusmods.com/skyrimspecialedition/mods/28833?tab=files) mod page.
- Open the downloaded archive and double-click the folder inside.
- Extract everything from the **Edit Scripts** folder to `Your Modding Folder\Tools\SSEEdit\Edit Scripts`.

### Fixed texture script

One of the AllGUD scripts assigns faulty texture file paths to the generated meshes which will prevent the resulting objects from looking as intended. Fortunately, this was fixed by Dusky and provided to us ([source](https://github.com/foreverphoenix/the-phoenix-flavour/issues/26)).

- Download the fixed script from [**Mediafire**](https://www.mediafire.com/file/fd0d6qj78lpjbas/AllGUD_AlternateTextureModelsplosion_-_Fixed.pas/file).
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

![Alternate Textures Patch](/Pictures/tpf/finalisation/allgud-alt-textures-fixed.png)

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

![Create empty mod](/Pictures/tpf/finalisation/create-empty-mod.png)

### Fixed Script

The original script has a bug. A fixed version is available on the Nexus.

- Download the [**AllGUD Weapon Mesh Generator Script Fix**](https://www.nexusmods.com/skyrimspecialedition/mods/38151?tab=files) manually.
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

![AllGUD Weapon Patcher](/Pictures/tpf/finalisation/allgud-weapon-meshes.png)

## Skeleton Patcher

- In Mod Organizer 2, once again click the tools icon above the mod order pane and select **Create empty mod**.
- Enter **AllGUD - Skeleton Meshes** as the name and click **OK**.
- Leave the new mod at the bottom of your mod order and activate it.

![Create empty mod](/Pictures/tpf/finalisation/create-empty-mod.png)

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

> Selecting all plugins first with CTRL + A is not necessary for this script.

![AllGUD Skeleton Patcher](/Pictures/tpf/finalisation/allgud-skeleton-patcher.png)

## Result

Now that you have installed the mod with all fixes and run the SSEEdit scripts, you have three new output folders in Mod Organizer 2, all of which should be enabled. If they appear as empty, remember to press F5 to refresh the UI.

AllGUD is now properly installed and ready to go.

### MCM Instructions

AllGUD has a fairly large MCM and most of the changes here come down to personal preference.

I recommend checking **Enable Weapons** in the **NPC** tab so that they also display shields on back etc.

If you want to disable the misc items (I'm personally not a fan but YMMV), you can do so for the player and NPCs separately on the **Misc - Player** and **NPC** pages respectively. It is also possible to selectively disable some misc items while keeping the rest.

![AllGUD MCM 1](/Pictures/tpf-x/installation/allgud-mcm-1.jpg)

![AllGUD MCM 2](/Pictures/tpf-x/installation/allgud-mcm-2.jpg)