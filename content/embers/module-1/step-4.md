---
title: "Step 4: Script Extender"
weight: 4
type: docs
description: >
  Understanding and installing the Skyrim Script Extender.
---

## The Skyrim Script Extender

If you have any previous modding experience at all, you will likely have heard of the **Skyrim Script Extender** or **SKSE** for short. Of all the mods and tools out there, the Script Extender is one of the most vital ones: It *extends* the scripting capabilities of the engine, allowing mod authors to implement features that would not have been possible before. SKSE is required by many mods, among them the most complex ones available.

A popular example of an SKSE-dependant feature is the **Mod Configuration Menu**, or **MCM** for short, which is part of the UI overhaul mod [SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/12604). But there are also a multitude of SKSE-based plugins that, among other things, fix engine-level bugs that could not have been addressed otherwise.

### SKSE and Skyrim Updates

Any updates for Skyrim SE change the main executable, **SkyrimSE.exe**, which then requires Script Extender to be updated in turn. SKSE is **version dependent** and will *only* work with the specific version of Skyrim SE it was compiled for. For example, SKSE SE version `2.0.20` functions only with the last pre-Anniversary Edition version of Skyrim SE, `1.5.97.0`.

The new SKSE AE was made for the post-AE versions of Skyrim SE. For **Embers**, you are currently expected to run the latest (post-AE) Skyrim SE build, `1.6.323.0`, with the corresponding SKSE AE build `2.1.3`.

The issue of version dependency does not only affect SKSE and the base game, but also SKSE and SKSE plugins. While some SKSE-dependent mods only use functions added by SKSE in their scripts and do not require a *specific* version of SKSE to actually work, there are also the so-called SKSE plugins. These files with the `.dll` extension are dependent on a specific SKSE version the same way SKSE is dependent on a specific Skyrim SE version.

> SKSE plugins (DLLs) are not to be confused with Skyrim plugins (ESMs, ESPs, ESLs). The former are written in C or C++ and specific to the Script Extender. The latter are created in the Creation Kit or community-made tools, and specific to Creation Engine games.

### Address Library for SKSE

To fix the problem of SKSE and SKSE plugins breaking with every Skyrim update, **meh321** (the author of a number of groundbreaking mods) released [Address Library for SKSE](https://www.nexusmods.com/skyrimspecialedition/mods/32444). It is a modder's resource allowing SKSE plugins to become version independent from SKSE by storing their offsets in a separate database instead. This has all but eliminated the problem of Skyrim updates: Since Address Library was released, the vast majority of SKSE plugins has been updated to utilise the resource and no longer requires a specific version of SKSE.

Due to the substantial changes that were made to the SkyrimSE.exe in the AE update, patch `1.6.318.0`, there is now a new version of Address Library exclusively for SAE, covering versions `1.6.x`. Various SKSE plugins for SKSE AE were updated to use this version of Address Library.

We will install Address Library after installing SKSE.

## Update Proofing

The version specific nature of SKSE and related mods makes forced updates of the base game quite disruptive. They can completely break a modded setup, rendering you unable to play.

Fortunately, update-proofing your game is simple:

- In your games library in Steam, right-click **The Elder Scrolls V: Skyrim Special Edition**.
- Select **Properties** and switch to the **Updates** tab.
- Make sure **Automatic updates** is set to **Only update this game when I launch it**.

Of course, this would still force you to update whenever you attempt to launch the game through its default executables. However, SKSE comes with its own launcher (which you must always use to launch the game for it to work properly). Launching the game through SKSE will *not* prompt Steam to update, meaning you can stay on an older version of the game for as long as you desire.

> Since we are using the Stock Game folder system, our copy of Skyrim for **Embers** is already protected from unwanted updates. Nevertheless, ensuring that the base game files are also not updated automatically is good practice and ensures you always have the version of Skyrim that you need available.

![Steam Disable Auto Updates](/Pictures/embers/module-1/steam-disable-updates.png)

## Downloading SKSE

First up, we should check the current version of Skyrim SE:

- Navigate to `\Mod Organizer 2\Stock Game\`.
- Right-click the **SkyrimSE.exe** inside and select **Properties**.
- Switch to the **Details** tab and check under **Product version**.

![Skyrim Check Version](/Pictures/embers/module-1/skyrim-version-check.png)

Now that we know which version of Skyrim SE we have installed, we know which version of SKSE to download:

- Open the official [Skyrim Script Extender](https://skse.silverlock.org/) website, the only place where SKSE is distributed.
- The current version of SKSE for AE, `build 2.1.x`, should correlate with the current Skyrim SE version, `runtime 1.6.xxx`.
- Download SKSE for Skyrim AE by clicking the **Download 7z file** link.

> Make sure to grab the correct file. The classic, SE, or VR versions will not work with post-AE versions of Skyrim SE.

![SKSE Download Version](/Pictures/embers/module-1/skse-download-version.png)

I personally keep the archives for the Script Extender (past and current version) under `\Your Modding Folder\ARCHIVE\Script Extender\`. Decide for yourself whether you wish to keep the archive around, and, if so, where to store it.

## SKSE Loader

SKSE only functions properly if Skyrim SE is run through its executable, **skse_loader.exe**, meaning you can no longer click play in Steam or open the game through its launcher. This executable as well as the two SKSE DLLs must be in the same folder as the game executables, your **root folder**.

- Open the downloaded archive and double-click the folder inside. There are a number of files and folders inside.
- Extract **skse64_1_6_xxx.dll**, **skse64_loader.exe**, and **skse64_steam_loader.dll** to `\Mod Organizer 2\Stock Game\`.

The two text files are, as you can tell from the names, the readme and changelog. There is no need to extract them as well.

> The exact file names may differ in the screenshot if SKSE updated in the meantime.

![SKSE Root Files](/Pictures/embers/module-1/skse-root-files.png)

If you currently have Mod Organizer 2 open, close it now. Then re-open it. SKSE should have been detected automatically and you will now be able to select it from the executables drop-down menu.

- Click the gears icon in the **Toolbar** to open the **Executable** settings.
- Select the new **SKSE** executable which should already have the correct file paths.
- Drag it up to the top of the executables list and click **OK**.

**Do not launch the game yet - we have not finished the SKSE installation.**

![MO2 SKSE EXE](/Pictures/embers/module-1/mo2-skse-exe.png)

## SKSE Scripts

Going back to the downloaded SKSE archive, you will notice two folders inside: **Data** and **src**. The latter is short for "source", meaning it contains the source code as resources for mod authors which we do not need.

The **Data** folder contains scripts which are a required component of SKSE. Theoretically, we could have dropped the **Data** folder containing the scripts into the **root folder** alongside the executable and DLLs where it would have merged with the existing **data folder**. 

However, those scripts are regular assets belonging into the **data folder** and can therefore be handled by Mod Organizer 2 instead.

To install the SKSE scripts in Mod Organizer 2, we can simply drop the files into a new **mod folder**.

- In Mod Organizer 2, click the crossed tools icon above the mod order and select **Create empty mod**.

![MO2](/Pictures/embers/module-1/create-empty-mod.png)

- Enter **SKSE Scripts** as the name and click **OK**.
- Right-click your new mod in the left pane and select **Open in Explorer**.
- Go back to the SKSE archive and double-click the **Data** folder.
- Extract the **Scripts** folder into your new **SKSE Scripts** mod folder.
- In MO2, press F5 to refresh and finally check the box to activate your new mod.

When you next launch SKSE through Mod Organizer 2 (we will do that shortly), the scripts will be loaded in the virtual data folder and recognised by SKSE just as if you had installed it directly in the **data folder**. Meanwhile, unchecking the mod in MO2 is enough to completely remove it from your virtual data folder.

![SKSE Scripts MO2](/Pictures/embers/module-1/skse-scripts-mo2.png)

### Version Number

Since one major advantage of MO2's virtual data folder is the ability to easily update mods, we should note the version number for the mod we just installed. Of course, we could simply change the mod name to include the SKSE version number. But MO2 has a more elegant solution.

- Double-click **SKSE Scripts** in your mod order.
- Switch to the **Nexus Info** tab.

When downloading mods from the Nexus, a meta file with various information about the mod will be downloaded alongside it. Since we did not download SKSE from the Nexus, there is no meta file. Under **Version**, you can now enter `2.1.3` (or whichever is the current SKSE version).

After you close the window again, the version number will appear properly in the **Versions** column in the MO2 UI like it does for all mods that you will install in the future.

![SKSE Scripts Version](/Pictures/embers/module-1/skse-scripts-version.png)

## SKSE INI

Two of SKSE's features need to be enabled in an INI file: 

`iTintTextureResolution` allows you to adjust the texture resolution of tint masks. By default, Skyrim's tint masks (this includes war paints, make-up, or dirt masks applied to faces) can only have a resolution of 512x512 pixels which can look very blurry. Even if you install 2048x2048 pixel (2K) retextures, they will look like 512x512 ingame.

`ClearInvalidRegistrations` is intended to clean up orphaned OnUpdate() events and prevent saves from bloating or breaking as a result of uninstalling certain mods.

### Creating SKSE INI

The SKSE INI must be located under `\Data\SKSE\SKSE.ini` so we can use Mod Organizer 2 and create it from scratch.

- Once again click the crossed tools icon and select **Create empty mod**.
- Name the new mod **SKSE INI** and click **OK**.
- Right-click the new mod and select **Open in Explorer**.
- Inside the new mod folder, create another new folder called **SKSE**.
- Within that **SKSE** folder, right-click and select **New** >> **Text Document**.
- Rename the file to **SKSE.ini** (make sure to change the file extension from TXT to INI).
- After changing the file extension and confirming, a warning window will pop up. Click **Yes**.

![SKSE INI Creation](/Pictures/embers/module-1/skse-ini-creation.png)

### INI Edits for SKSE SE

- Go back into Mod Organizer 2 and press F5 to refresh.
- Double-click **SKSE INI** in your mod order and switch to the **INI Files** tab.
- Select the `SKSE\SKSE.ini` file.
- Copy and paste the following into the empty file:

```
[Display]
iTintTextureResolution=2048

[General]
ClearInvalidRegistrations=1
```

> You can set the texture resolution for face tints to any resolution you like, although anything above 2048 (2K) is simply overkill. Keep in mind that you will also have to install higher resolution retextures for tint masks later on for this setting to make a difference.

- Hit **CTRL+S** to save your edits and close the window.
- Check the box for the new mod to enable it.

### Other SKSE INI Settings

> The below INI settings **should not** be added to your SKSE.ini.

Beyond the two settings that we added, there are other options that are largely relics of the SLE days.

One allows you to adjust memory allocation, but while memory was a real issue in Skyrim LE, the 64bit engine upgrade in Skyrim SE all but solved the problem. The settings were very recently enabled in SKSE for SE; however, most people use the memory manager from SSE Engine Fixes instead (another mod, to be installed soon).

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

## Address Library

Since the Script Extender is now installed, we should also install **Address Library for SKSE** which is a hard requirement for many SKSE plugins and essentially an extension of SKSE itself.

- Open the Nexus page for [Address Library for SKSE](https://www.nexusmods.com/skyrimspecialedition/mods/32444) and switch to the **Files** tab.
- Locate the **All in one (Anniversary Edition)** main file and click the **Mod Manager Download** button to download through MO2.

![Address Library Download](/Pictures/embers/module-1/address-library-download.png)

This will now download the file through Mod Organizer 2 into the downloads folder we previously specified, `\Your Modding Folder\ARCHIVE\MO2 Downloads\`. After installing the mod, the downloaded archive will remain in that folder as a backup and so you can reinstall it at a later point.

- In the right pane of Mod Organizer 2, switch to the **Downloads** tab.
- Double-click the downloaded file.

Before installing a mod, you can rename it. The name you enter here will correspond to the name of the folder that will be created for the mod under `\Mod Organizer 2\mods\` and show up in the mod order (left pane of MO2). I frequently rename mods, often to reflect the version I downloaded, so you may find that your mods are sometimes named differently than they are in my screenshots. This is purely a matter of taste ~~and my own obsession with a clean naming scheme~~.

In the case of this mod, I did not adjust the name.

- Click **OK** to install the mod.
- It will now appear in your mod order. Check the box to activate it.

![Address Library Installation](/Pictures/embers/module-1/address-library-installation.png)

## Test Run

Before we install some more SKSE-related mods, we should make sure SKSE is running properly. As mentioned earlier, Skyrim must be run through the SKSE executable for SKSE to work, that simply means that you need to double-click **skse64_loader.exe** instead of **SkyrimSE.exe** to play. It also means that you CANNOT launch the game through Steam anymore (if you want to play with SKSE and mods) since that starts the **SkyrimSELauncher.exe**.

Additionally, we established that any tool as well as the game itself MUST be run through Mod Organizer 2 as they cannot otherwise access MO2's virtual data folder. They would simply read the actual **data folder** where no mods are installed. If we now ran SKSE outside of MO2, the game would launch, but the scripts would not be loaded as they are installed through MO2. Any mods installed later on that reference those scripts would *not* work.

**Always start the game by running the Script Extender through Mod Organizer 2.**

- Make sure all new SKSE-related mods are checked in the left pane of Mod Organizer 2.
- Select **SKSE** from the executables drop-down menu in Mod Organizer 2.
- Click **Run** to launch the Skyrim Script Extender through Mod Organizer 2.

![SKSE MO2 Launch](/Pictures/embers/module-1/skse-mo2-launch.png)

Instead of opening the launcher, running the game through SKSE will bring you into the main menu directly.

Once you're in the main menu, open the **console**, a dev tool that will be hugely important, particularly for troubleshooting. You can bring it up by pressing the **tilde** key:

![Tilde key](https://www.computerhope.com/cdn/keyboard/tilde.jpg)

- In the console, type **skse** and hit Enter (capitalisation is irrelevant).
- It should return the version of SKSE you just installed.
- If everything works, close the console (press the **tilde** key again).
- Quit the game.

> Version in the screenshot may differ from yours if SKSE updated in the meantime.

![SKSE Check Ingame](/Pictures/embers/module-1/skse-check-ingame-ae.jpg)

---

#### Continue with [Step 5: Essential Mods](/embers/module-1/step-5/).