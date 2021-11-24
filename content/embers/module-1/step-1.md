---
title: "Step 1: Skyrim Setup"
weight: 1
type: docs
description: >
  Setting up the correct version of Skyrim.
---

## Skyrim

**Embers** is a guide for and requires a Steam copy of [Skyrim Special Edition](https://store.steampowered.com/app/489830/). Whether you own the Anniversary Edition DLC is irrelevant.

There are a number of  notable differences between the various versions of Skyrim that have been released since 2011 which are important to be aware of when modding the game. The most substantial change came in 2016 when the remastered **Skyrim Special Edition** (SSE) was released, featuring a 64bit engine upgrade with far-reaching consequences for the modding community. Most mods created for **Classic Skyrim** (the 2011 version with the 32bit engine) need to be ported before they can be used safely in SSE.

Arguably the most important tool for modding is the **Skyrim Script Extender** (SKSE) which needed a full rewrite for Skyrim SE. Without SKSE, many of the best mods out there will straight up not work. Different versions of SKSE are now available for Classic Skyrim, Skyrim SE, Skyrim VR, and Skyrim AE.

> SKSE is not compatible with the PC Xbox Game Pass version of Skyrim SE; hence, a Steam copy is required.

Although the modding scene for Skyrim SE had a slow start, it has grown massively since 2016. Nowadays, many mods are developed exclusively for SSE and the most exciting new releases are usually exclusive to SSE as well. Due to this and the stability improvements that the engine upgrade provided, SSE is the superior option for modding today.

**Skyrim Anniversary Edition** (SAE) was released in 2021 as an update for Skyrim SE. The Anniversary Edition DLC has to be purchased separately, but the patch that accompanied it was applied to all SSE installations. Mods function the same in SAE as in SSE, although SKSE needed to be partially rewritten so that there is now a version of SKSE for AE in addition to the one for SSE.

While currently there are no advantages in using Skyrim SE `1.6.x` (post-AE versions) over Skyrim SE `1.5.97.0` (pre-AE version), mods are usually developed for the latest version available, meaning that in time the community will move on to post-AE versions of Skyrim. This is why **Embers** was written for the post-AE versions as well.

> If you want to know more about the various releases and re-releases of Skyrim, check the [Skyrim Versions](/other-resources/skyrim-versions/) article.

## Modding Folder

Before we start messing with the game files, please go ahead and create a modding folder in a convenient location. This folder will hold certain file backups as well as all your downloaded mod archives so it may get rather big. Since the archives are not needed for actual gameplay (they will be unpacked and installed), I recommend storing them on a hard drive where space is not an issue. Any HDD will do.

Throughout the guide I will be referring to this folder as **Your Modding Folder**.

- Create a top level folder, e.g. `F:\Skyrim SE Modding\`.
- Within that new folder create several more as shown below:

![Your Modding Folder](/Pictures/embers/module-1/your-modding-folder.png)

## Spring Cleaning

Now comes the boring part: We need to make sure your Skyrim SE installation is absolutely pristine and that no traces of previous modding setups remain on your PC. Additionally, we will ensure the game files are located in a suitable location.

**Uninstall Skyrim SE through Steam.** (If you currently have the game installed.)

### Mod Files

Navigate to where the game was installed which is probably `C:\Program Files x86\Steam\steamapps\common\`. If there is still a **Skyrim Special Edition** folder in this location after uninstalling the game through Steam, it means you had non-vanilla (meaning mod-added) files in your game folder. These are not removed when uninstalling the game and may get in the way of the **Embers** setup.

Delete the **Skyrim Special Edition** folder if it still exists after uninstalling the game.

### Documents Folder

Next we will take a look at the **Documents** folder.

> If you have never run Skyrim SE before, this folder will not exist for you and you can skip ahead to the next step, **Game Language**.

- Navigate to `C:\Users\Your User Name\Documents\My Games\Skyrim Special Edition\`

This directory may contain multiple files and folders: The **Skyrim.ini** and **SkyrimPrefs.ini** are the game's primary configuration files, they will become very relevant later on. There may also be a **saves** folder which, you guessed it, contains your save games. If you have any vanilla saves that you would like to hold on to, move the **saves** folder to `\Your Modding Folder\Backups\` from where you can restore it
anytime. Lastly, the Documents folder may also include mod-generated files such as logs.

- Make sure you have backed up any saves you want to keep.
- Delete the entire **Skyrim Special Edition** folder.

The folder and INI files will be freshly regenerated very soon.

That's it. Skyrim SE is now completely removed from your system.

## Game Language

Skyrim supports a bunch of different languages natively, but mods do not. Since many mods also do not require translations in the first place and some of the ones that do have third-party translations available, it is theoretically possible to play modded in Skyrim in a language other than English. However, this will complicate your setup immensely. Translations, where available, may be outdated or incomplete. They may not cover voice acting. They may not exist for some of your mods at all.

Ultimately, translating any records (and certain textures!) untouched by existing patches plus fixing conflicts between translations and mods will add a hefty amount of work on top of everything else. I do not recommend it, especially not for a beginner.

If your game is currently set to a language other than English, you can change this quickly in Steam. The English files will be downloaded immediately if you have the game currently installed, or the next time you install the game. Please note that an English language copy of Skyrim SE is mandatory for **Embers**.

- Right-click **The Elder Scrolls V: Skyrim Special Edition** in your Steam games library.
- Select **Properties** and switch to the **Language** tab.
- Ensure that the language is set to **English**.

![Set language to English](/Pictures/tpf/initial-setup/skyrim-se-english.png)

## Installation Directory

In order to prevent various issues down the line, it is highly recommended not to install the game or any tools in **UAC-protected folders** such as `C:\Program Files\` and `C:\Program Files x86\`. UAC-protected folders in Windows are special because they require admin privileges for read/write permissions which can break various modding tools.

Because of this, you will likely have to create a new **Steam Library**.

> Already familiar with Steam Libraries and have one available outside UAC-protected folders? Skip ahead to the next step.

### Steam Library

A **Steam Library** is a directory on your hard drive designated as an installation folder by Steam; if you install any game, this is where it will be installed to. If you have multiple Steam Libraries, you will be able to choose in which to install a given game.

The default Steam Library is located inside your Steam installation folder. If you installed Steam itself without specifically changing the installation directory, it will now be located within `C:\Program Files x86\Steam\` and your default Steam Library will be `C:\Program Files x86\Steam\steamapps\common\` - within a UAC-protected folder, exactly where we do not want it to be.

In the Steam settings, any folder on your hard drive can be designated to be a Steam Library. By default, there can only be one Steam Library per hard drive, however, a workaround exists.

### Ideal Directory

Skyrim should be installed:

- in a Steam Library outside the UAC-protected folders ...
- ... which is ideally on an SSD or otherwise fastest hard drive.

> An SSD is recommended for faster loading times. Depending on its speed, an HDD may also negatively impact overall performance.

If you want to create a new Steam Library on your `C:\` drive but already have your regular Steam installation and its default Steam Library on the same drive, you will need to use LostDragonist's [Steam Library Setup Tool](https://github.com/LostDragonist/steam-library-setup-tool/wiki/Usage-Guide) to create a second Steam Library on that drive (follow the link for instructions).

Otherwise, open the **Settings** in Steam, go to the **Downloads** tab, and click the **Steam Library Folders** button. You can choose the drive and folder for your new Steam Library directly through the interface. Once set up, the new Steam Library can be selected upon installing a new game.

## Reinstalling Skyrim

Find the game in your library (in the Steam app) and click the big blue **INSTALL** button. Make sure to select a Steam Library outside any UAC-protected folders as the location to install all files to and wait for the game to be fully downloaded.

**Proceed when the download is complete.**

## First Test Run

At this point, we should see if Skyrim launches properly. Running the game once serves multiple purposes:

- The `\Documents\My Games\Skyrim Special Edition\` folder including its INI files will be regenerated.
- The registry keys will be set up which is required for modding tools to recognise your installation.
- Certain issues with your vanilla game can be detected now.

> Always remember to launch Skyrim once after updating or re-installing it, or after verifying game files.

In Steam, click the big green **PLAY** button to open the launcher.

- A message box will pop up, informing you that Skyrim SE will now be configured based on your hardware.
- Click **OK** twice to confirm (we will modify the INI files later on).
- Click the **PLAY** option in the launcher and wait until you are in the Skyrim main menu.
- **AE OWNERS:** Skyrim will prompt you with a message box, then proceed to download the creations. Wait for it to finish.
- Quit the game from the main menu. If you got this far, everything appears to be running smoothly.

> If Skyrim is unable to detect your hardware, it’s likely because you have a newer graphics card. You can safely ignore this as we will regenerate INIs from scratch later on.

![Regenerating INIs](/Pictures/tpf/initial-setup/regenerating-inis.png)

## Creation Club Content

If you own any Creation Club content, through AE or otherwise, it will have been redownloaded along with the base game.

For all intents and purposes, creations are just mods. They can interact with mods and cause the same kind of compatibility issues that mods can cause with each other. You will likely want to pick and choose from them just like you pick and choose your mods.

For now I highly recommend removing the creations from your data folder and backing them up elsewhere. You will be able to reinstall them later on in a much more convenient and controlled fashion.

- Go to **Your Modding Folder** and create a new folder called **Creation Club** within the **Backups** folder.
- Navigate to `\Steam\steamapps\common\Skyrim Special Edition\Data\`.
- Move all files beginning with **cc** into the new CC backups folder.

![Creation Club Backup](/Pictures/embers/module-1/creation-club-backup.png)

---

#### Continue with [Step 2: Mod Organizer 2](/embers/module-1/step-2/).