---
title: "Basic Instructions"
weight: 2
type: docs
description: >
  Detailed instructions for certain procedures such as porting mods.
---

## Converting Plugins

> "Resave Example.esp in the Creation Kit."

Plugins with Form Version 43 (typically downloaded from the Classic Skyrim Nexus) must be re-saved in the CK.

* Run the **Creation Kit** through Mod Organizer 2.
* Once it is loaded up, go to **File > Data**.
* Select the plugin you need to convert in the list and click **Set as Active File**.
* Click **OK** and wait for the Creation Kit to load up the plugin.
* Go to **File > Save**. There will be a small confirmation message (**Saving… done!**) at the bottom of the window.
* Close the Creation Kit.
* Afterwards, you can right-click the mod in MO2 and select **Mark converted/working**.

## Cleaning Plugins

> "Clean Example.esp with SSEEdit."

Very rarely a plugin may contain ITMs or deleted records in which case you need to run it through the QuickAutoClean version of SSEEdit (just like we did with the official master files).

* Run **SSEEdit - Quick Cleaning** through Mod Organizer 2.
* Check only the plugin you were instructed to clean in the plugin list.
* Click **OK** and wait for the process to complete (`Quick Clean mode finished`).
* Close SSEEdit.

## Extracting BSAs

> "Unpack Example.bsa through Mod Organizer 2."

Archives should be unpacked if they were created with the 32bit CK (which will crash SSE) or if included files need to be loose in order to overwrite or be selectively deleted.

* Switch to the **Archives** tab in the right pane of Mod Organizer 2.
* Find the archive you need to unpack and right-click it (it will only show up if the mod is active).
* Navigate to `Mod Organizer 2\mods`, click on the mod folder the archive belongs to and click **Select Folder**.
* After unpacking the files, press F5 to refresh Mod Organizer 2.

## Optimising SLE Assets

> "Run the mod through Cathedral Assets Optimiser."

Skyrim LE meshes often need to be fixed and optimised by Cathedral Assets Optimizer before they can be used in SE. We will also use CAO on mods to optimise (compress) included textures sometimes. If a Classic Skyrim mod does not have instructions to run it through CAO this is because I already did so and found that no meshes or textures needed optimising.

* Run **Cathedral Assets Optimizer** (do not launch it through Mod Organizer 2).
* Select the **SSE - Optimise SLE Assets** profile from the drop-down menu.
* Click **Open Directory** and navigate to `Mod Organizer 2\mods`.
* Click on the folder of the mod you wish to optimise and hit **Select Folder**.
* Back in CAO, click **Run** and wait for the process to complete.
* Afterwards, you can right-click the mod in MO2 and select **Mark converted/working**.

## Fixing Meshes

> "Run the mod through SSE NIF Optimizer."

Very few mods in the guide need to be run through SSE NIF Optimizer instead of Cathedral Assets Optimizer to fix their meshes.

* Double-click **SSE NIF Optimizer.exe** which should be located inside Your Modding Folder.
* Click **Browse** and navigate to `Mod Organizer 2\mods`.
* Click on the folder of the mod you wish to optimise and hit **Select Folder**.
* Click **Optimise** and wait until the process is finished.
* Close **SSE NIF Optimizer**.

## Resizing Textures

> "Downsize the textures with Cathedral Assets Optimizer."

At times (re)textures are only available in a size unreasonably large for regular gameplay, potentially impacting performance for those with low VRAM. In those cases we will utilise CAO to reduce the texture resolution by half.

* Run **Cathedral Assets Optimizer**.
* Select the **SSE - Downsize Textures** profile from the drop-down menu.
* Click **Open Directory** and navigate to `Mod Organizer 2\mods`.
* Click on the mod containing the textures and **Select folder**.
* Back in CAO, click **Run** and wait for the process to be completed.