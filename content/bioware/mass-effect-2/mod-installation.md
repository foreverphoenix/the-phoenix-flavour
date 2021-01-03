---
title: "Mod Installation"
weight: 3
type: docs
description: >
  Instructions for ME3TMM and ALOT.
---

## Installation Order

Time to install some mods! As is necessary for Mass Effect games, we are going to install gameplay-related mods first before setting up the texture pack ALOT which comes with its own installer.

## Binkw32 Proxy DLL

This is a small plugin which enables the console as well as modified DLC mods in Mass Effect 2, the latter feature is required for ME2 Recalibrated. If you are interested to learn more, check out the [Github repository](https://github.com/Erik-JS/masseffect-binkw32).

- Download the bundled binaries from [Dropbox](https://www.dropbox.com/sh/vejorqi4zo54g70/AAAnm0kk7rUq0gPB1U_m5DEwa?dl=0).
- Navigate to `Mass Effect Modding\Tools` and create a new folder **"Binkw32 Proxy DLL"**.
- Open the downloaded archive and extract its contents into the new folder.

### Installation

- Double-click the **me2_binkw32.zip** to open it.
- Navigate to your Steam/Origin installation of Mass Effect 2 and open the **Binaries** folder.
- Extract the plugins, **binkw23.dll** and **binkw32.dll**, from the archive into the folder.
- Click **Replace** when prompted.

> It's also possible to install the plugin through ME3TMM with a single click. I just really like having manual backups on my hard drive ~~and also I'd already written the instructions by the time I had figured that out~~.

## ME2 Recalibrated

The Recalibrated series of mods is a collection of tweaks and fixes with some additional content restorations and additions in the case of the ME2 version.

- Download both the main and the update file from the [Nexus page](https://www.nexusmods.com/masseffect2/mods/169?tab=files).
- Move both archives to `Mass Effect Modding\Mass Effect 2\Mods`.

### Installation

- Open the main archive **ME2Recalibrated v1.1** and double-click the **1 BASE GAME** folder inside.
- Navigate to your `Mass Effect 2\BIOGame\CookedPC` folder.
- Extract the **PlotManager.pcc** file from the archive into this folder. Confirm when asked to overwrite.
- Move up one level in the archive and open the **2 DLC MOD** folder.
- Navigate to your `Mass Effect 2\BIOGame\DLC` folder.
- Extract the **DLC_MOD_ME2Re** folder into this folder.

### Lair of the Shadow Broker

Skip this step if you don't have the Lair of the Shadow Broker DLC.

- Move up one level in the archive and open the **3 DLC PATCH - LOTSB** folder.
- Navigate to your `Mass Effect 2\BIOGame\DLC\DLC_MOD_ME2Re\CookedPC` folder.
- Extract all files from the archive into this folder.

### Zaaed - The Price of Revenge

Skip this step if you don't have the Zaaed - The Price of Revenge DLC.

- Move up one level in the archive and open the **4 DLC PATCH - ZAAED** folder.
- Navigate to your `Mass Effect 2\BIOGame\DLC\DLC_MOD_ME2Re\CookedPC` folder.
- Extract the file from the archive into this folder.

### Altered Appearance

Skip this step if you don't the Altered Appearance Packs 1 and 2.

- Move up one level in the archive and open the **6 - OPTIONAL - Alt Appearance DLC** folder.
- Navigate to your `Mass Effect 2\BIOGame\DLC\DLC_MOD_ME2Re\CookedPC` folder.
- Extract all files from the archive into this folder.

### Update

- Open the **ME2Re_v1.1.2_Update** archive.
- Navigate to your `Mass Effect 2\BIOGame\DLC\DLC_MOD_ME2Re\CookedPC` folder.
- Extract the three **.pcc** files from the archive into this folder.
- Overwrite when prompted.

## ME3TMM Mods

Open the mod manager, ME3TMM. If you followed my ME1 guide, the mods installed then will appear in the left pane. You can hide them for the time being by clicking the **ME1** button above.

- Mods are downloaded as ZIP / RAR files from the Nexus.
- Drag and drop the downloaded archive into ME3TMM, the mod manager.
- In the window that will come up, you need to click **Import mods** to add it to your library.
- Afterwards, select the mod in the left pane and click **Apply Mod** (button in the bottom right).
- This will occasionally prompt a quick menu with different options.

**If dragging and dropping a mod does not work:**

- In ME3TMM, go to **Mod Management** >> **Import Mod** >> **Import Mod from [file format]**.
- Navigate to the mod and double-click it to import it.

### Mods that I'm using

- [No Mini Games](https://www.nexusmods.com/masseffect2/mods/63?tab=files): Download the main file, select Keyboard/Mouse during the installation.
- [Oriana Looks Like Miranda's Twin](https://www.nexusmods.com/masseffect2/mods/255?tab=files): Download the main file, select Vanilla Textures during the installation.

### Other Recommended Mods

- [Modern Weapon Pack](https://www.nexusmods.com/masseffect2/mods/202)
- [Recovered Powers](https://www.nexusmods.com/masseffect2/mods/247)
- [New Armor Colors and Casual Outfits](https://www.nexusmods.com/masseffect2/mods/251)

## Manual Installation

In addition to the two mods already installed via ME3TMM, I using two more that haven't been updated for the new mod manager and need to be installed manually.

### Remove Shared Cooldowns

Since the original [Remove Shared Cooldowns](https://www.nexusmods.com/masseffect2/mods/118) mod edits the same file as the already installed No Mini Games, a patched version of it must be installed to prevent breaking either mod.

- Download the main file of [Remove Shared Cooldowns Compatibility Patch for No Mini Games](https://www.nexusmods.com/masseffect2/mods/205?tab=files).
- Navigate to `Mass Effect 2\BIOGame\CookedPC`.
- Open the downloaded archive and extract the **SFXGame.pcc** file into that folder.
- Overwrite when prompted.

### Mass Effect 2 Crushed Blacks Fix

- Download the main file of [Mass Effect 2 To Dark Fix](https://www.nexusmods.com/masseffect2/mods/135?tab=files).
- Open the download archive and drop the **Engines** folder inside into your Mass Effect folder.
- Click **Yes** to merge folders and overwrite when prompted.
 
## Graphic Mods

### ALOT for Mass Effect 2

ALOT is basically a texture pack but it does come with an installer and integration for other texture mods. After running the ALOT installer, you cannot change your mods anymore so it is done at the very end.

- Navigate to `Mass Effect Modding\Mass Effect 2` and create a new folder: **ALOT Installer**.
- Open the Nexus Page for [A Lot Of Textures (ALOT) for ME 2](https://www.nexusmods.com/masseffect2/mods/68?tab=files).
- Download the main file **ALOT for ME2 12.0** and the optional file **Improved Static Lighting for ME2**.
- Move both files to `Mass Effect Modding\Mass Effect 2\Mods` after downloading them.
- Open the *main file*, double-click the folder inside and extract everything into the `Mass Effect Modding\Mass Effect 2\ALOT Installer` folder.

> Using the Torrent download may be faster if you don’t have Nexus Premium.

### ALOV for Mass Effect 2

ALOV is a high quality upscale for cutscenes for the ALOT installer in 1080p 60FPS or 2160p 60FPS quality. Please note that the 4K version may come with a performance hit so it is advisable to download the 1080p when playing on a weaker PC.

- Open the [A Lot Of Videos (ALOV) for ME2](https://www.nexusmods.com/masseffect2/mods/245?tab=files) mod page.
- Download *either* the **ALOV for ME2 - v2.1 (1080p)** *or* the **ALOV for ME2 - v2.1 (4K)** main file.
- Download the **ALOV for ME2 - ALOT Addon** miscellaneous file.
- Move both downloaded archives to `Mass Effect Modding\Mass Effect 2\Mods`.

> Using the Torrent download may be faster if you don’t have Nexus Premium.

### Asari Remastered

This is an Asari retexture that is recommended on the ALOT mod page. It does look different from Vanilla but is similar to and consistent with the "Smooth Faces" option included with the MEUITM texture pack for Mass Effect 1 which I used.

- Open the [Asari Remastered](https://www.nexusmods.com/masseffect2/mods/204?tab=files) mod page.
- Download the **Asari NPCs Remastered TPF version** main file.
- Download the **Liara T'Soni Remastered TPF version** main file.
- Download the **Samara Remastered TPF Version** main file.
- Move all three archives to `Mass Effect Modding\Mass Effect 2\Mods`.

### Weapon Retextures by TheDarkFalcon

These are an off-Nexus collection of retextures recommended to be installed alongside ALOT.

- Download the **Weapon Mantis M-92 HR** retexture from [Dropbox](https://onedrive.live.com/?authkey=%21ADmvZwC%5FH0ruIWc&cid=DBE0E01C958EBA9F&id=DBE0E01C958EBA9F%21391&parId=DBE0E01C958EBA9F%21106&o=OneUp).
- Open the [Google Drive](https://drive.google.com/drive/folders/1ha-PdId0T6O_AgSs-LAEsmpV8ILgCpuc) repository where all remaining files are located.
- Download the **WpnCarnifex_HRv1.5.zip** file from Google Drive
- Download the **WpnKatana_HRv1.5.zip** file from Google Drive.
- Download the **WpnPredator_HR1.5.zip** from Google Drive.
- Download the **WPNShuriken_HR1.5.zip** from Google Drive.
- Move all four downloaded archives and the loose TPF file to `Mass Effect Modding\Mass Effect 2\Mods`.

### ME2Recalibrated ALtered Appearance

Earlier I recommended the installation of the Altered Appearance module of ME2 Recalibrated for those who own the two DLC packs. In order to also update the changes in the squad selection menu, there are a few TPF files (textures) that need to be installed which is done through the ALOT installer.

- Double-click the **ME2Recalibrated v1.1** archive which should be inside `Mass Effect Modding\Mass Effect 2\Mods`.
- Open the **6 OPTIONAL - Alt Appearance DLC** folder inside, then open the **Textures** folder.
- Extract the two files into the `Mass Effect Modding\Mass Effect 2\Mods` folder.
- Select both files, right-click them and select **Add to archive** (or whatever option your archiving tool adds).
- Rename the archive to something recognisable such as **ME2 Recalibrated AltAp DLC**.

## ALOT Installer

Now that all relevant files have been downloaded, it is time to install them with ALOT.

- Navigate to `Your Modding Folder\Tools\ALOT` and double-click **ALOTInstaller.exe**.
- If an update is available, wait until it is downloaded and installed.
- Click **Import assistant** > **Select files to import**.
- Navigate to `Your Modding Folder\Mass Effect 2\Mods` and double-click the **Improved Static Lighting** archive.
- Wait for the ALOT installer to import the mod. Click **Close import assistant** once it's done.

Repeat the same process for **ALOV for ME2** (1080p or 4K) as well as the weapon retextures (four archives and one loose file).

### Additional Mods

Some mods do not have manifest files to be automatically recognised by the ALOT installer. They need to be installed using the custom option.

- Open the ALOT **Import assistant** and click on **Add files**.
- Navigate to `Your Modding Folder\Mass Effect 2\Mods` and double-click the ALOV ALOT Addon archive.
- Click the **Mass Effect 2** logo to set ME2 as the target game.
- Adding this will only take a second. Click **Close import assistant** once it's done.

Repeat for the custom **ME2 Recalibrated AltAp DLC** archive we created earlier as well as all three archives from the **Asari Remastered** mod.

## Texture Installation

- Click **Install Textures**, the button in the bottom right corner.
- All options and mods should be enabled by default.
- Feel free to toggle off 4K Texture LODs if you are concerned with performance.
- Click **Begin Installation** once you're ready.
- Click **I understand, install** when the warning window pops up. This is the point of no return.

The remainder of the installation procedure will now run automatically. This will take a while.

When it's done, click **Continue** and close the ALOT installer.