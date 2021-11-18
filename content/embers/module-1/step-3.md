---
title: "Step 3: Root and Data"
weight: 3
type: docs
description: >
  The root and data folders, and how to manage them.
---

## Vanilla Skyrim

The unmodded, pristine version of Skyrim that we restored in Step 1 is referred to as **vanilla Skyrim**. It is about 12.7GB in size (without creations) and located in a Steam library directory.

### File Name Extensions

Before we continue, please make sure file name extensions are set to visible in Windows Explorer for you. This may already be the case, but if it is not, you should enable them now as you will be telling file types apart by their extensions which is rather important.

- To see file name extensions, go into **Windows Explorer**.
- In the **View** tab/ribbon, make sure the **File name extensions** box is ticked.

![File Name Extension](/Pictures/embers/module-1/file-name-extensions.png)

## Root Folder

Navigate to your Skyrim SE installation. The file path is `\Steam\steamapps\common\Skyrim Special Edition\`.

![MO2 Root Folder](/Pictures/embers/module-1/skyrim-root-folder.png)

This is your **root folder**. It contains the two executables, **SkyrimSE.exe** which directly opens the game, and **SkyrimSELauncher.exe** which starts the Launcher first. The latter is what Steam runs when you start the game.

## Data Folder

The **data folder** is located within the **root folder**. Open it now.

![MO2 Data Folder](/Pictures/embers/module-1/skyrim-data-folder.png)

The **data folder** contains all game files which are split into **plugins** and **archives**: There are five **ESMs** (plugins) containing all records and 18 **BSAs** (archives) containing all assets. What precisely plugins and archives are and what they do will be discussed later on; for now it is enough to know that they constitute the bulk of the game.

Mods are no different from the base game files: They can consist of plugins or assets, or both, and the assets can be packed in BSAs or they can be loose. **Like the base game files, mods always belong into the data folder.** If you install a mod into the root folder, it will simply not be recognised by the game and it will not work.

## Data Folder Files

Mods can consist of various files that are not always neatly stowed away in BSAs with a matching plugin. A large modded setup may consist of hundreds of plugins and thousands of loose files. When building such a setup, managing those loose files is one of the core concerns.

If all those loose files were simply dropped into the **data folder**, new files would overwrite existing files with the same name. Although this could be undone, the original file would still be lost once it had been overwritten. Every file conflict would have to be painstakingly reviewed *before* installing a new mod (each of which may contain hundreds of loose files). Short of creating dedicated Excel tables, it would be impossible to keep track of which files belong to which mod.

Nexus Mod Manager was certainly an improvement over dropping files into the **data folder** manually. For mods installed into the **data folder** through its interface, it did track which files belonged to which mod, but it could not remember if you had overwritten any of them. The worst case scenario was that upon uninstalling one mod, you inadvertendly removed parts of a different mod that you had overwritten the first mod with.

This method of modding meant that, ideally, you would need to know the order in which mods should overwrite each other *before* you installed them. Additionally, if you updated a mod and the previous version of it had some files that were removed in the update, you had to know that was the case in the first place and then track those files down to delete them by hand.

### MO2's Virtual File System

Arguably the most exciting feature of the original Mod Organizer was the **Virtual File System**, for **VFS** for short. Over the years, Nexus Mod Manager and its successor, Vortex, implemented similar functionalities although the modern Mod Organizer 2 remains the champion of asset managers.

Here is how it works:

MO2 builds a virtual **data folder** from various mod files at runtime. Instead of extracting mod files into the **data folder** directly, they are extracted into separate, self-contained **mod folders**. No files ever actually conflict with or overwrite each other. Your folder structure will look like this:

- `\Mod Organizer 2\mods\Mod 1\<files from mod 1>`
- `\Mod Organizer 2\mods\Mod 2\<files from mod 2>`
- `\Mod Organizer 2\mods\Mod 3\<files from mod 3>`
- ...

Mods being installed separately from one another created the concept of a **mod order**: If two mods contain the same files, the one placed lower in the mod order will overwrite in the virtual data folder. But because the files never *actually* conflict, you can change which file overwrites any time by changing the order of the two mods. You can also review and compare those files without having to reinstall and overwrite, and you will always know which mod they belong to.

**The importance of asset management and mod order cannot be understated.** We will look at examples later on to illustrate this further.

Because of the VFS, the game and most modding tools must be run through Mod Organizer 2 as they would not be able to access the virtual data folder otherwise.

## Root Folder Files

Mod Organizer 2 and other mod managers exist to manage the contents of the **data folder**. They do not, however, control the **root folder**.

Of course very few mods belong into the root folder to begin with. The Skyrim Script Extender is one of them, an essential framework that we will discuss more in the next step. ENB or ReShade for advanced post processing effects also need to be placed in the root folder.

While MO2 allows for self-contained mod setups, having to place certain files into the root folder still causes overlap between setups. If you run several different ones, a Wabbajack list and a personal setup for example, swapping out ENBs or having to be on the same version of SKSE may become annoying.

## Stock Game Folder

**In order to create a fully self-contained modded setup we are going to create a copy of the root folder in a custom location.** This means that the base game files in your current installation folder will remain completely untouched. You will even be able to edit them without affecting your modded setup.

- Navigate to your Mod Organizer 2 installation folder and create a new **Stock Game** inside.
- Copy the contents from your default **root folder** into this new folder.
- This may take a minute depending on your hard drive (around 13GB of files are being copied).

As long as your default Skyrim SE installation is in place, Steam will recognise the game if it is now launched from your custom location.

> If you're wondering: Yes, this is exactly the Stock Game Folder system that many Wabbajack lists use.

### Redirecting MO2

Mod Organizer 2 still uses your default root folder so it needs to be updated.

- Make sure Mod Organizer 2 is **closed**.
- Find **ModOrganizer.ini** in you MO2 installation folder.

To edit this INI file (and other configuration files later on), I highly recommend installing [Notepad++](https://notepad-plus-plus.org/). It is an open-source, feature-rich alternative to Window's default Notepad and more than worth it even for simple text file editing.

If you do not have Notepad++ installed yet, I recommend installing it now. Afterwards, you can set it to be the default app to open INI files by following these steps:

- Right-click your **SKSE.ini** file and select **Open with** >> **Choose another app**.
- Choose **Notepad++**, and check the **Always use this app to open .ini files** box at the bottom.
- Click **OK** to confirm.

> In **Embers**, all pictures of INIs not edited through Mod Organizer 2 will show Notepad++.

![Notepad++ Set Default](/Pictures/embers/module-1/notepadpp-set-default.png)

Let's continue with **ModOrganizer.ini**:

- Open the INI file in Notepad++ (or another editor of your choice).
- Change the **gamePath** to the new copy you just created.

![Stock Game INI](/Pictures/embers/module-1/stock-game-ini.png)

- Save your changes and close the INI file.

Re-open Mod Organizer 2 and open the **Settings**. In the **Paths** tab, it should now have updated the file path to the managed game:

![MO2 Managed Game](/Pictures/embers/module-1/mo2-managed-game.png)

### Updating the executables

As we discussed previously, any executables must be run through Mod Organizer 2 if you want the files managed by MO2 to be recognised. For now, we should edit the default executables to use our copy of the game folder.

- Open the **Executables** settings in MO2 by clicking the gears icon in the Toolbar.
- For the **Skyrim Special Edition** executable, click the button next to **Binary** and navigate to your new **Stock Game** folder.
- Double-click the **SkyrimSE.exe** inside to select it.
- Click the button next to **Start in** and navigate to your **Stock Game** folder once again.
- Click **Select Folder** to set it as the new root folder.

![Update MO2 Executables](/Pictures/embers/module-1/update-mo2-executables.png)

Repeat the same process for the **SkyrimSELauncher.exe**, updating both file paths. Afterwards, click **OK** to close the settings window and save your changes.

### Test Run

To see if everything was updated properly, we should test if the game can still be properly launched through Mod Organizer 2.

- Make sure **Skyrim Special Edition** is selected in the executables drop down in the top right.
- Hit the **Run** button to launch the game.
- Quit from the main menu if all went smoothly (otherwise go back to check if you missed something).

![MO2 Launch SSE](/Pictures/embers/module-1/mo2-launch-sse.png)

---

#### Continue with [Step 4: Script Extender](/embers/module-1/step-4/).