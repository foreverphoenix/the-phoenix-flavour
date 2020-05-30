---
title: "Skyrim Realistic Overhaul"
weight: 9
type: docs
description: >
  Installing and optimizing Skyrim Realistic Overhaul.
---

## 9.1 Download

Skyrim Realistic Overhaul is the most comprehensive texture overhaul out there, over 10GB in size and covering nearly every single texture in the game. We will use it as a base retexture for our setup.

Unfortunately SRO is not on the Nexus and we will have to download it from ModDB. Because the files are so large, the download may take a while (depending on your internet connection) and it may be advisable to let them load overnight.

Otherwise you can also continue with the Mod Installation section for now as the installation of SRO can be completed anytime.

* Open the [Skyrim Realistic Overhaul](https://www.moddb.com/mods/skyrim-realistic-overhaul/downloads) page on ModDB and download the following files:
  * `Skyrim Realistic Overhaul Part 1`
  * `Skyrim Realistic Overhaul Part 2`
  * `Skyrim Realistic Overhaul Part 3`
  * `Skyrim Realistic Overhaul 1.8 Update`

**Do not download the file for Original Skyrim (SLE).**

> It is  technically not necessary to download the **Update** file as it will be overwritten completely with the full TPF installation. I have included it anyway for the sake of completeness as well as for people skipping many of the other retextures.

## 9.2 File Extraction

* Create a new folder inside `Your Modding Folder\temp` and name it **Skyrim Realistic Overhaul**.
* Extract the **textures** folders from all downloaded SRO archives into the new **Skyrim Realistic Overhaul** folder in this order:
  * Part 1
  * Part 2
  * Part 3
  * Update
* This will take a while. **Make sure to merge and overwrite when asked.**
* Eventually you will have a single **textures** folder with the size of a solid **10.2GB**.

![SRO Textures Folder](Pictures/setup/sro_textures_folder.png)

## 9.3 Processing with CAO

In order to be able to control the mod order of SRO and ensure it can be overwritten by other retexture mods, we will also pack the textures in BSAs (archives) and load the matching plugins high up in the load order. All packed up, the entirety of SRO will be reduced to 8.32GB this way.

**If you have 3GB of VRAM or less:** Use the **SSE – Skyrim Realistic Overhaul (Performance)** profile. In addition to repacking the textures, CAO will also half their resolution (all 4k textures to 2k, all 2k textures to 1k) which will help save VRAM. Note that this will take more time and result in less plugins and archives.

- Run **Cathedral Assets Optimizer** (do not open it through Mod Organizer 2.)
- From the **Profiles** drop-down menu, select one of the **SSE – Skyrim Realistic Overhaul** profiles (Quality / Performance).
- Click **Open Directory** and point it at the `Your Modding Folder\temp\Skyrim Realistic Overhaul` folder.
- Click **Run** to start the process. Click **Yes to All** if asked to save changes.
- This will take a while! You can monitor the progress in the **Logs** tab.
- Wait until the CAO log returns: `[INFO] Process completed`.

![Process SRO in CAO](Pictures/setup/process_sro_in_cao.png)

## 9.4 Installation

* Navigate to `Your Modding Folder\temp\Skyrim Realistic Overhaul` which now contains several ESPs and BSAs:
  * **Quality:** 6 ESPs+BSAs, 8.33GB in total
  * **Performance:** 2 ESPs+BSAs, 2.29GB in total
* Move the **Skyrim Realistic Overhaul** folder containing the packed files to `Mod Organizer 2\mods`.
* Back in Mod Organizer 2, press F5 to refresh.
* **Skyrim Realistic Overhaul** should now appear at the bottom of your mod order.
* Drag it up all the way below the **MAIN VISUAL MODS** separator and activate it.
