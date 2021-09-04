---
title: "Lesson 2: Script Extender"
weight: 2
type: docs
no-list: false
description: >
 The Skyrim Script Extender.
---

## Overview

- The Skyrim Script Extender and its significance.
- Skyrim SE updates and how to update-proof your installation.
- The root and data folder, and the differences between them.
- MO2's virtual file system and (roughly) how it works.
- Installation of the Script Extender and related mods.

## The Skyrim Script Extender

If you have any previous modding experience at all, you will likely have heard of the **Skyrim Script Extender** or **SKSE** for short. Of all the mods and tools out there, the Script Extender is one of the most vital ones: It *extends* the scripting capabilities of the engine, allowing mod authors to implement features that would not have been possible before. SKSE is required by many mods, among them the most complex ones available.

A popular example of an SKSE-dependant feature is the **Mod Configuration Menu**, or **MCM** for short, which is part of the UI overhaul mod [SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/12604). But there are also a multitude of SKSE-based plugins that, among other things, fix engine-level bugs that could not have been addressed otherwise.

### SKSE and Skyrim Updates

Due to its very nature, the Skyrim Script Extender is **version dependant**. Any version of SKSE will *only* work with the specific version of Skyrim SE it was compiled for. For example, the current version (as of Summer 2021) of SKSE, `2.0.19`, functions only with the latest version of Skyrim SE, `1.5.97.0`.

Unfortunately, Skyrim SE is still being updated occasionally. These patches are almost exclusively to add or update "creations" for the Skyrim SE "Creation Club" (an ingame store for mini DLC) and rarely ever changes something about the base game, but they will break SKSE regardless. In the past it has taken anywhere from between a few days to a few weeks for the SKSE team to update for the latest version of Skyrim.

The issue of version dependancy does not only affect SKSE and the game, but also SKSE and SKSE plugins. While some SKSE-dependant mods only use functions added by SKSE in their scripts and do not require a specific version of SKSE to function, there are also the so-called SKSE plugins. These files with the `.dll` extension are dependant on a specific SKSE version the same way SKSE is dependant on a specific Skyrim SE version.

Until recently, mod authors had to wait for the SKSE team to update whenever Skyrim updated before they could update their own SKSE plugins in turn. Occasionally, authors were not actively modding anymore when a Skyrim patch dropped and were not around to update their mods until weeks later, if at all. Since many mods have closed permissions, nobody else could update their mods for them either. And because SKSE plugins are among the most complex of mods (written in C or C++), there are very few people capable of updating them for a new Skyrim version to begin with.

This was the primary problem with Skyrim SE - until the Address Library was released.

### Address Library

To fix the problem of SKSE and SKSE plugins breaking with every Skyrim update, **meh321** (the author of a number of groundbreaking mods) released [**Address Library for SKSE**](https://www.nexusmods.com/skyrimspecialedition/mods/32444). It is a modder's resource allowing SKSE plugins to become version independent from SKSE by storing their offsets in a separate database instead. This has all but eliminated the problem of Skyrim updates: Since Address Library was released, the vast majority of SKSE plugins has been updated to utilise the resource and no longer requires a specific version of SKSE.

## Update Proofing

While the release of Address Library has all but eliminated the danger of parts of your setup being rendered unplayable due to a Skyrim update, it is still important to make sure your game is not updated automatically when a new patch drops. Otherwise, you will still be unable to play until SKSE is updated for the new version.

Fortunately, update-proofing your game is simple:

- In your games library in Steam, right-click **The Elder Scrolls V: Skyrim Special Edition**.
- Select **Properties** and switch to the **Updates** tab.
- Make sure **Automatic updates** is set to **Only update this game when I launch it**.

Of course, this would still force you to update whenever you attempt to launch the game through its default executables. However, SKSE comes with its own launcher (which you must always use to launch the game for it to work properly). Launching the game through SKSE will *not* prompt Steam to update, meaning you can stay on an older version of the game for as long as you desire.

![Steam Disable Auto Updates](/Pictures/tpf/initial-setup/sse-disable-auto-updates.png)

### Game Backup

Accidents happen - and rolling back to a previous version of Skyrim if you unintentionally updated to a newer version can be annoying. If you want to be absolutely certain, you can use Steam to create a compressed backup of the current version of the game. This can be done by right-clicking the game and going to **Properties** >> **Local Files** >> **Backup game files**.

I personally only keep manual backups of the executables (**SkyrimSE.exe** and **SkyrimSELauncher.exe**). Reverting to them is enough to launch an old version of SKSE when the game updated. However, if a Skyrim patch also affected any of the game files, this may still not be enough (always check the changelog). In that case, you need to restore a full backup of all files.

## File Name Extensions

Before we continue, please make sure file name extensions are set to visible in Windows Explorer for you. This may already be the case, but if it is not, you should enable them now as you will be telling file types apart by their extensions which is rather important.

- To see file name extensions, go into **Windows Explorer**.
- In the **View** tab/ribbon, make sure the **File name extensions** box is ticked.

![File Name Extension](/Pictures/embers/module-1/file-name-extensions.png)

## Root and Data Folder

After so much talk about the Script Extender, we should install it. However, we cannot do it through Mod Organizer 2. To understand why SKSE must be installed differently from other mods, we need to talk about the root and data folders.

Navigate over to your Skyrim installation, `\Your Steam Library\steamapps\common\Skyrim Special Edition\`. This folder is referred to as the **root folder**. In its current vanilla state, it will look like this:

![Skyrim Root Folder](/Pictures/embers/module-1/skyrim-root-folder.png)

Among the folders within the root folder, you will notice the **data folder** at the top. This is the other most important directory. Open it:

![Skyrim Data Folder](/Pictures/embers/module-1/skyrim-data-folder.png)

The **data folder** contains all game files which are split into **plugins** and **archives**: There are five **ESM** plugins containing all records and 18 **BSAs** (archives) containing all assets. What precisely plugins and archives are and what they do will be discussed later on; for now it is enough to know that they constitute the bulk of the game.

> Skyrim plugins are not to be confused with SKSE plugins. The former is created in the Creation Kit or community-made tools, and specific to Creation Engine games. The latter are plugins written in C or C++ and specific to the Skyrim Script Extender.

Mods are, in essence, no different to the base game files, they can consist of plugins or assets, or both, and the assets can be packed in BSAs or they can be loose. **Like the base game files, mods always belong into the data folder.** If you install a mod into the root folder, it will simply not be recognised by the game and it will not work.

Mod Organizer 2 and other mod managers exist to manage the contents of the **data folder**. They do not, however, control the **root folder**.

SKSE is not a mod as such. It is a modder's resource and a framework. Almost all parts of SKSE must be installed into the **root folder** which is exactly why it cannot be installed through Mod Organizer 2.

## Installing SKSE

First up, we should check the current version of Skyrim SE:

- Navigate to your **root folder**.
- Right-click the **SkyrimSE.exe** inside and select **Properties**.
- Switch to the **Details** tab and check under **Product version**.

![Skyrim Check Version](/Pictures/tpf/initial-setup/skyrim-se-1-5-97-0.png)

Now that we know which version of Skyrim SE we have installed, we know which version of SKSE to download:

- Open the official [**Skyrim Script Extender**](https://skse.silverlock.org/) website, the only place where SKSE is distributed.
- As you can see the current version of SKSE, `build 2.0.19`, correlates with my current Skyrim version, `runtime 1.5.97`.
- Download the 7z archive for Skyrim SE (make sure to grab the correct file, the classic or VR versions will not work with SE).

![SKSE Download Version](/Pictures/embers/module-1/skse-download-version.png)

I personally keep the archives for the Script Extender (past and current version) under `\Your Modding Folder\ARCHIVE\Script Extender\`. You must decide for yourself whether you wish to keep the archive around, and if so where to store it, or whether you'll simply delete it after extracting the files.

### SKSE Loader

SKSE only functions properly if Skyrim SE is run through its executable, **skse_loader.exe**, meaning you can no longer click play in Steam or open the game through its launcher. This executable as well as the two SKSE DLLs must be in the same folder as the game executables, your **root folder**.

- Open the downloaded archive and double-click the folder inside. There are a number of files and folders inside.
- Extract **skse64_1_5_97.dll**, **skse64_loader.exe**, and **skse64_steam_loader.dll** into your **root folder**.

The two text files are, as you can tell from the names, the readme and changelog. There is no need to extract them into your **root folder** as well.

![SKSE Root Files](/Pictures/embers/module-1/skse-root-files.png)

If you currently have Mod Organizer 2 open, close it now. Then re-open it. SKSE should have been detected automatically and you will now be able to select it from the executables drop-down menu. However, do not attempt to launch the game through SKSE yet as we have not completed the installation.

> Why SKSE and almost all tools must be run through MO2 will be explained shortly.

![SKSE MO2 Executable](/Pictures/embers/module-1/skse-mo2-executable.png)

Going back to the downloaded SKSE archive, you will notice two folders inside: **Data** and **src**. The latter is short for "source", meaning it contains the source code as resources for mod authors which we do not need.

The **Data** folder though contains scripts which are a required component of SKSE. Theoretically, we could have dropped the **Data** folder containing the scripts into the **root folder** alongside the executable and DLLs where it would have merged with the existing **data folder**. 

However, those scripts are regular assets belonging into the **data folder** and can therefore be handled by a mod manager instead. The best feature of Mod Organizer 2 is precisely the way it handles mod files: It is time to talk about the virtual file system.

## Managing Mod Files

As mentioned, mods can consist of various files: They are not always neatly stowed away in BSAs with a matching plugin. A large modded setup may consist of hundreds of plugins and thousands of loose files, such as those SKSE scripts. A big part of building a setup is managing those loose files, that is, deciding which files should overwrite.

If all those loose files are simply dropped into the **data folder**, new files will overwrite existing files with the same name. Although this can be undone, the original file will still be lost once it has been overwritten. Every file conflict must painstakingly be reviewed *before* installing a new mod (each of which may contain hundreds of loose files). Short of creating dedicated Excel tables, it is impossible to keep track of which files belong to which mod.

Nexus Mod Manager was certainly an improvement over dropping files into the **data folder** manually. For mods installed into the **data folder** through its interface, it did track which files belonged to which mod, but it could not remember if you had overwritten any of them. The worst case scenario was that upon uninstalling one mod, you inadvertendly removed parts of a different mod that you had overwritten the first mod with.

This method of modding meant that, ideally, you would need to know the order in which mods should overwrite each other *before* you installed them. Additionally, if you updated a mod and the previous version of it had some files that were removed in the update, you had to know that was the case in the first place and then track those files down to delete them by hand.

In short: It was absolute chaos. But this chaos was once what everyone had to contend with - until Mod Organizer revolutionised asset management.

### MO2's Virtual File System

Arguably the most exciting feature of the original Mod Organizer was the **Virtual File System**, for **VFS** for short. Over the years, Nexus Mod Manager and its successor, Vortex, implemented similar functionalities although the modern Mod Organizer 2 remains the champion of asset managers.

**This is how it works:**

MO2 builds a virtual **data folder** from various mod files at runtime. Instead of extracting mod files into the **data folder** directly, they are extracted into separate, self-contained **mod folders**. No files ever actually conflict with or overwrite each other.

Mods being installed separately from one another created the concept of a **mod order**: If two mods contain the same files, the one placed lower in the mod order will overwrite in the virtual data folder. But because the files never *actually* conflict, you can change which file overwrites any time by changing the order of the two mods. You can also review and compare those files without having to reinstall and overwrite, and you will always know which mod they belong to.

**The importance of asset management and mod order cannot be understated.** We will look at examples later on to illustrate this further.

Because of the VFS, the game and most modding tools must be run through Mod Organizer 2 as they would not be able to access the virtual data folder otherwise.

## SKSE Scripts

To install the SKSE scripts in Mod Organizer 2, we can simply drop the files into a new **mod folder**.

- Navigate to `\Mod Organizer 2\mods\` and create a new folder: **SKSE Scripts**.
- Double-click the **Data** folder inside the SKSE archive.
- Extract the **Scripts** folder into your new **SKSE Scripts** mod folder.

Go back into Mod Organizer 2 and press F5 which will refresh the UI. Your new mod will appear in the left pane which is the **mod order**. Check the box to activate it and when you next launch SKSE through Mod Organizer 2 (we will do that shortly), the scripts will be loaded in the virtual data folder and recognised by SKSE just as if you had installed it directly in the **data folder**. Similarly, unticking it is enough to completely remove it from your virtual data folder.

### Version Number

Since one major advantage of MO2's virtual data folder is the ability to easily update mods, we should note the version number for the mod we just installed. Of course, we could simply change the mod name to include the SKSE version number. But MO2 has a more elegant solution.

- Double-click **SKSE Scripts** in your mod order.
- Switch to the **Nexus Info** tab.

When downloading mods from the Nexus, a meta file with various information about the mod will be downloaded alongside it. Since we did not download SKSE from the Nexus, there is no meta file and MO2 has changed the Mod ID to -1. Under **Version**, you can now enter **2.0.19** (or whichever is the current SKSE version).

After you close the window again, the version number will appear properly in the **Versions** column in the MO2 UI like it does for all mods that you will install in the future.

![SKSE Scripts Version](/Pictures/embers/module-1/skse-scripts-version.png)

## Test Run

Before we install some more SKSE-related mods, we should make sure SKSE is running properly. As mentioned earlier, Skyrim must be run through the SKSE executable for SKSE to work, that simply means that you need to double-click **skse64_loader.exe** instead of **SkyrimSE.exe** to play. It also means that you CANNOT launch the game through Steam anymore (if you want to play with SKSE and mods) since that starts the **SkyrimSELauncher.exe**.

Additionally, we established that any tool as well as the game itself MUST be run through Mod Organizer 2 as they cannot otherwise access MO2's virtual data folder. They would simply read the actual **data folder** where no mods will be installed to. If we now ran SKSE outside of MO2, the game would launch, but the scripts would not be loaded as they are only installed through MO2. Any mods installed later on that reference those scripts would *not* work.

**Always start the game by running the Script Extender through Mod Organizer 2.**

- Make sure the **SKSE Scripts** mod is checked in the left pane of Mod Organizer 2.
- Select **SKSE** from the executables drop-down menu in Mod Organizer 2.
- Click **Run** to launch the Skyrim Script Extender through Mod Organizer 2.

![SKSE MO2 Launch](/Pictures/embers/module-1/skse-mo2-launch.png)

Instead of opening the launcher, running the game through SKSE will bring you into the main menu directly.

Once you're in the main menu, open the **console**, a dev tool that will be hugely important particularly for troubleshooting. You can bring it up by pressing the **tilde** key:

![Tilde key](https://www.computerhope.com/cdn/keyboard/tilde.jpg)

- In the console, type **skse** and hit Enter (capitalisation is irrelevant).
- It should return the version of SKSE you just installed.
- If everything works, close the console (press the **tilde** key again).
- Quit the game.

![SKSE Check Ingame](/Pictures/embers/module-1/skse-check-ingame.jpg)

## SKSE INI

Two of SKSE's features can only be enabled through an INI file: 

`iTintTextureResolution` allows you to adjust the texture resolution of tint masks. By default, Skyrim's tint masks (this includes war paints, make-up, or dirt masks applied to faces) can only have a resolution of 512x512 pixels which can look very blurry. Even if you install 2048x2048 pixel (2K) retextures, they will look like 512x512 ingame.

`ClearInvalidRegistrations` is intended to clean up orphaned OnUpdate() events and prevent saves from bloating or breaking as a result of uninstalling certain mods.

### Creating SKSE INI

The SKSE INI must be located under `\Data\SKSE\SKSE.ini` so we can use Mod Organizer 2 and create it from scratch.

- Navigate to `\Mod Organizer 2\mods\` and create a new **SKSE INI** folder.
- Open the new folder and create a new **SKSE** folder inside.
- Within that **SKSE** folder, right-click and select **New** >> **Text Document**.
- Rename the file to **SKSE.ini** (make sure to change the file extension from TXT to INI).
- After changing the file extension and confirming, a warning window will pop up. Click **Yes**.

![SKSE INI Creation](/Pictures/embers/module-1/skse-ini-creation.png)

### Notepad++

To edit the new INI file, you *can* simply open it through Notepad, which is a default TXT editor pre-installed in Windows. However, I highly recommend installing [**Notepad++**](https://notepad-plus-plus.org/), an open-source, feature-rich alternative. Even for simple text file editing, it is more than worth it, and we will need it again for other INI, TOML, and JSON files later on.

If you do not have Notepad++ installed yet, I recommend installing it now. Afterwards, you can set it to be the default app to open INI files by following these steps:

- Right-click your **SKSE.ini** file and select **Open with** >> **Choose another app**.
- Choose **Notepad++**, and check the **Always use this app to open .ini files** box at the bottom.
- Click **OK** to confirm.

> In **Embers**, all pictures of INIs not edited through Mod Organizer 2 will show Notepad++.

![Notepad++ Set Default](/Pictures/embers/module-1/notepadpp-set-default.png)

### INI Edits for SKSE SE

- Open **SKSE.ini** with your preferred text editor (e.g. Notepad++).
- Copy and paste the following into the empty file:

```
[Display]
iTintTextureResolution=2048

[General]
ClearInvalidRegistrations=1
```

> You can set the texture resolution for face tints to any resolution you like, although 2048 (2K) should be perfect for most people. Anyone looking to primarily take close-up screenshots rather than play the game can potentially increase the resolution to 4096 (4K). Keep in mind that you will also have to install higher resolution retextures for tint masks later on for this setting to make a difference.

- Hit **CTRL+S** to save your edits and close the file.
- Back in Mod Organizer 2, press F5 to refresh the UI.
- **SKSE INI** will appear in your mod order (left pane).
- Check the new mod to enable it.

### Other SKSE INI Settings

> The below INI settings **should not** be added to your SKSE.ini.

Beyond these two settings, there are other options that are largely relics of the SLE days.

One allows you to adjust memory allocation, but while memory was a real problem in Skyrim LE, the 64bit engine upgrade in Skyrim SE all but solved the problem. The settings were very recently enabled in SKSE for SE, however, most people use the memory manager from SSE Engine Fixes instead (another mod, to be installed soon).

```
[Memory]
DefaultHeapInitialAllocMB=
ScrapHeapSizeMB=
```

There is also an option to enable diagnostics. I am not entirely certain if this is valid in SKSE for SE to begin with (the changelog makes no mention of it), but it would be irrelevant anyway. What it logs is missing master files and missing plugins in a save. You will be able to see the former in Mod Organizer 2 and the latter upon attempting to load a save after disabling plugins that it relies on.

We will talk about the implications of missing masters and missing plugins later on. For now, it suffices to know that we will have easier ways of detecting those problems.

```
[General]
EnableDiagnostics=1
```

## Address Library for SKSE

Finally we are coming full circle, returning to **Address Library**, the mod we talked about at the beginning of the lesson. Since the Script Extender is now installed, we should also install Address Library which is a hard requirement for many SKSE plugins and essentially an extension of SKSE itself.

- Open the Nexus page for [**Address Library for SKSE**](https://www.nexusmods.com/skyrimspecialedition/mods/32444).
- Switch to the **Files** tab.
- Click the **Mod Manager Download** button for the main file.

![Address Library Download](/Pictures/embers/module-1/address-library-download.png)

This will now download the file through Mod Organizer 2 into the downloads folder we previously specified, `\Your Modding Folder\ARCHIVE\MO2 Downloads\`. After installing the mod, the downloaded archive will remain in that folder as a backup and so you can reinstall it at a later point.

- In the right pane of Mod Organizer 2, switch to the **Downloads** tab.
- Double-click the downloaded file and click **OK** to install it.
- It will now appear in your mod order. Check the box to activate it.

![Address Library Installation](/Pictures/embers/module-1/address-library-installation.png)

## Conclusion

With the proper setup of the Script Extender and all related files out of the way, we are now free to install most other mods.