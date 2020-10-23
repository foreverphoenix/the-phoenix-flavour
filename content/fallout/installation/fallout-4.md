---
title: "Fallout 4"
weight: 2
type: docs
description: >
  Re-installation and configuration of the vanilla game.
---

## Installation directory

In order to ensure that your Fallout 4 installation is pristine and vanilla, we are going to completely re-install the game. This is especially important if you have modded the game previously as left-over files might interfere with your WTP installation.

### UAC protected folders

The reinstallation also serves the purpose of relocating the game files to a better directory. Using UAC protected folders (such as `C:\Program Files` or `C:\Program Files x86`) for the game or any modding tools has a risk of causing issues down the line. It is best to avoid those folders to begin with. Most Wabbajack list authors, including myself, will not provide support for people that disregard this warning and use UAC protected folders anyway.

Note that this does not include the Steam client. Most people will have it installed under `C:\Program Files x86\Steam` which is completely fine.

### Preferred hard drive

Fallout 4 and Mod Organizer 2 should always be installed on the same hard drive. Ideally that hard drive would be an SSD to reduce loading times and eliminate stuttering.

## Uninstallation

Skip this if you do not have Fallout 4 installed.

- Open Steam and go into your games library.
- Find **Fallout 4** in the list, right-click it and select **Manage** >> **Uninstall**.
- Click **Uninstall** to confirm.
- Navigate to your Fallout 4 directory. This is most likely:
  - `C:\Program File x86\Steam\steamapps\common\Fallout 4`
- Delete any left-over files in this folder.

### INI Folder

 More Fallout-related files are located inside the so-called **INI Folder** which needs to be cleaned out as well. It contains your savegames as well as the game's INI files and, if you modded Fallout 4 before, F4SE plugin logs.

- Navigate to the **INI Folder:**
  - `C:\Users\{Your User Name}\Documents\My Games\Fallout4`
- If you have an ongoing vanilla playthrough, back up the **Saves** folder.
- Delete everything inside the **Fallout4** folder.

> You can simply move the **Saves** folder to **Fallout 4 Modding\Backups**.

## Reinstallation

### What is a Steam Library?

In order to prevent some confusion, I will refer to the Library in Steam as the **Game Library**. It is the second of four items in the top menu in the Steam client and contains a list of all your games.

A **Steam Library** on the other hand is a folder on your hard drive into which Steam games are installed. By default this would be `C:\Program Files x86\Steam\steamapps\common\`. Since we do not want to have files inside a UAC protected folder like Program Files x86, we should not install Fallout 4 in the default directory. A new **Steam Library** is required.

> It is important to note that Steam only allows one Steam Library per hard drive, although there is a workaround. If for instance you already have a Steam Library on your C drive, but you want to have your modding files on C as well, you need to create a second Steam Library manually following the instructions [here](https://steamcommunity.com/discussions/forum/1/1355112940663240029).

### Creating a new library

If you already have a separate Steam Library outside the UAC protected folders on the drive you want to install Fallout 4 and Mod Organizer 2 on, skip ahead to the next step (Reinstalling the game).

Otherwise follow the instructions below to create a new Steam Library:

- Open **Steam** and go into the **Settings**.
- In the Downloads tab, select **Steam Library Folders**.
- Click **Add Library Folder**.
- Point it to a location somewhere outside the UAC protected folders, e.g. `G:\Steam Library\`.
- Close all windows when you’re done.

### Setting the language to English

Non-English installations of Fallout 4 are not supported.

- Right-click **Fallout 4** in your Steam games library.
- Select **Properties** and switch to the **Langauge** tab.
- Ensure that the language is set to **English**.

![Fallout English](/Pictures/fallout/installation/fallout-english.png)

### Reinstalling the game

- Open Steam and go into your **Game Library**.
- Find **Fallout 4** in the list and click **Install**.
- As location, select the **Steam Library** you just created and click **Next**.

Wait for Fallout 4 to be downloaded before you proceed.

### Regenerating INI Files

After re-installing the game, it is important to launch it at least once through Steam so that the registry keys are set up. Otherwise, certain modding tools may not recognise the game. Upon launching the game, the default set of INI files will also be regenerated.

- Find **Fallout 4** in your **Games Library** and hit **Play**.
- You will be prompted with a notification that Fallout 4 is configuring your video options, click **OK**.
- Click **OK** again to the next window and hit **Exit** to close the launcher again.

![Regenerate INIs](/Pictures/fallout/installation/regenerate-inis.png)

## Future Updates

The most important mod for any Bethesda game is the **Script Extender**, a resource that is in turn required for many key mods. The **Fallout 4 Script Extender** (F4SE) is *version dependent*. It requires a specific version of Fallout 4. For instance, F4SE 0.6.21 *requires* Fallout 4 1.10.163, and will not work with any other version of the game.

Unfortunately any update for the Creation Club requires the game executables to be updated which breaks F4SE every time. When that happens, the Script Extender team usually updates F4SE within a few days. Any F4SE plugins will have to be updated by their respective authors as well which can take several weeks.

In order to prevent Creation Club updates from interrupting your playthrough and breaking your game, we are going to disable automatic updates in Steam. We are also going to backup the current version's executables so you can restore them at any time.

### Disable Auto Updates

- Open Steam and find **Fallout 4** in your **Game Library**.
- Right-click it and select **Properties**
- In the **Updates** tab, change **Automatic updates** to the following setting:
  - Only update the game when I launch it
- Close the **Properties** window.

![Steam Disable Auto Updates](/Pictures/fallout/installation/steam-disable-auto-updates.png)

### Executables Backup

Although Steam will no longer update Fallout 4 automatically, I still recommend keeping backups of the two executables (**Fallout4.exe** and **Fallout4Launcher.exe**), just in case. If you accidentally updated, all you need to do to roll back is replace the executables in your **root** folder with the ones you backed up. This also comes in handy if you had to regenerate INI files or validate game files through Steam for whatever reason and were forced to update.

- Navigate to `steamapps\common\Fallout4` and copy (CTRL + C) the following files:
  - **Fallout4.exe**
  - **Fallout4Launcher.exe**
- Paste (CTRL + V) them to `Fallout 4 Modding\Backups\Executables 1.10.163.0`.

## Official High Resolution Texture Pack

Bethesda published a free 55GB texture pack with upscaled 4K textures that are nowhere near worth the hard drive space, especially not when compared to higher quality mod-added textures. If you had the HD DLC installed previously, you need to disable it in Steam.

- Open **Steam** and go into your **Game Library**.
- Go to the **Fallout 4** page and click **Manage my 8 DLC**.
- Uncheck **Fallout 4 - High Resolution Texture Pack** in the list and click **Save**.

![Disable HD DLC](/Pictures/fallout/installation/disable-hd-dlc.png)

## Creation Club Content

If you bought any "creations" from the Creation Club (or grabbed some while they were available for free), they may still be present in your Data folder. Since WTP does not currently support Creation Club content you need to remove the files from your **Data** folder for the time being.

- Navigate to `steamapps\common\Fallout4\Data` and cut (CTRL + X) all files starting with **cc**.
- Paste (CTRL + V) all files to `Fallout 4 Modding\Backups\Creation Club`.

---

#### Continue with the [Wabbajack](https://thephoenixflavour.com/fallout/installation/wabbajack/) page.