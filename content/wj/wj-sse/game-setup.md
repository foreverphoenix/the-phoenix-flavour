---
title: "Game Setup"
weight: 1
type: docs
description: >
  How to prepare your Skyrim SE installation for a Wabbajack list.
---

All Wabbajack lists come with extensive documentation, most of which covers the preparation of your Skyrim SE installation. These steps are largely identical for every (Skyrim SE) Wabbajack list and are covered in great detail below.

Please refer to the documentation of your Wabbajack list before installing it and use the instructions provided. Do not follow the instructions on this page unless your list links back here.

> If you are wondering why my instructions are so much more extensive than those of most Wabbajack lists, it is because I explain many of the steps and changes in far greater detail. That does not mean Wabbajack lists' documentation is insufficient, but installation instructions are not usually a priority for them. Meanwhile this page exists solely to provide instructions that are as comprehensive and easy-to-follow as possible.

---

The following lists currently link back to this page:

- None (yet)

## Requirements

Any Wabbajack list requires you to own a Steam copy of [Skyrim SE](https://store.steampowered.com/app/489830/The_Elder_Scrolls_V_Skyrim_Special_Edition/). The tool will not work with pirated copies of the game. Should Discord moderators suspect that you are using a pirated copy of Skyrim upon asking for support, they will request proof of purchase. If you fail to produce any, they will remove you from the server. Piracy of any kind is not tolerated.

Wabbajack currently only supports **the latest version of Windows 10**. Linux support is planned, but not currently available.

You also must have an account on [Nexus Mods](https://www.nexusmods.com/). A free account is sufficient, although you would have to download mods by hand. Wabbajack helps with this by opening the pages and highlighting the files you need, but it will still take a while to download hundreds of files manually. With Nexus Premium, you can simply click install in Wabbajack and all files will be downloaded manually. This limitation with free accounts is due to the Nexus API; Wabbajack has no control over it.

### Disk Space

A good amount of free disk space is required. The documentation for your chosen Wabbajack list should indicate exactly how big the **mods** and **downloads** folders will be after the installation. The **mods** folder is part of the Mod Organizer 2 setup and contains all the actual files that are loaded into the game, as such it ought to be on a fast hard drive (ideally an SSD).

The **downloads** folder meanwhile contains the downloaded mod archives that are needed for reinstalling mods or updating the list, but not for playing. They can be stored on another hard drive like a slower HDD. They can also be deleted after installing the list, but in that case you would need to redownload *all files* when updating the Wabbajack list.

### Visual C++ Redist

The Microsoft Visual C++ Redistributable is a basic package required by Mod Organizer 2. You probably already have it installed with Windows but it is best to make sure.

- Open the official [Microsoft Visual C++ website](https://support.microsoft.com/en-us/topic/the-latest-supported-visual-c-downloads-2647da03-1eea-4433-9aff-95f26a218cc0).
- Scroll to the **Visual Studio 2015, 2017 and 2019** section.
- Download the following file: `vc_redist.x64.exe`.
- Run the executable, it will guide you through the installation process.

![VC Redist](/Pictures/tpf/initial-setup/vc-redists.png)

### Antivirus Software

Plenty of antivirus software by third parties has caused Wabbajack and Mod Organizer 2 significant trouble in the past. They frequently disable or partially disable functionality of either tool by quarantining files. It is recommended to simply rely on **Windows Defender**. You can also disable your antivirus or add exceptions for Wabbajack and Mod Organizer 2.

(This does not meant that that either tool is full of viruses, merely that not all third party antivirus programs out there have manually flagged the latest versions of them as harmless. If you are worried about viruses, note that the Nexus checks all uploaded files up to a certain limit for viruses using [Virus Total](https://www.virustotal.com/gui/home/upload).)

## Skyrim Cleanup

Wabbajack lists can only installed for clean, vanilla installations of Skyrim SE. Please remove any traces of previous modded setups before using Wabbajack. A quick and easy way to do this used to be the [Skyrim Shredder](https://www.nexusmods.com/skyrimspecialedition/mods/30133) tool by Wabbajack team member and list author trawzified. However, the tool is currently not usable due to a Steam update so the cleaning has to be done manually.

If you have existing **Mod Organizer 2** setups *as portable instances*, you do not need to remove them. One of MO2's primary features is that each portable instance is self-contained without ever touching the vanilla files, meaning they will not interfere with each other. All Wabbajack lists use MO2 with portable instances so you can install several lists alongside each other.

### Uninstalling Skyrim

First, we need to remove the vanilla files:

- Uninstall the game through Steam.

While uninstalling through Steam will remove all vanilla files from your hard drives, any mod-added files will remain in place.

- Navigate to where Skyrim was installed, this is likely: `C:\Program Files x86\Steam\steamapps\common\`.
- If there is still a **Skyrim Special Edition** folder in this location, delete it.

This will leave your vanilla saves and INI files in place. They are stored under `C:\Users\Your Username\Documents\My Games\Skyrim Special Edition\` and will not interfere with your Wabbajack installation as Mod Organizer 2 uses its own directories for saves and INI files. You will be able to play vanilla Skyrim with your old saves anytime by launching the game through Steam instead of MO2.

## Steam Settings

Before we can reinstall the game, we need to adjust some settings in Steam.

- In Steam, open the **Properties** for Skyrim SE.
- In the **Updates** tab, make sure **Automatic Updates** is set to **Only update this game when I launch it**.
- In the **Language** tab, make sure the **Language** is set to **English**.

### About automatic updates

Automatic updates are restricted because they can render you unable to play the game. Skyrim SE still updates on occasion when new content for the Creation Club is added or existing Creations are updated. Whenever that happens the [Skyrim Script Extender](http://skse.silverlock.org/) (SKSE) will not work until it also receives an update, and without SKSE any Wabbajack list is unplayable.

With the changed settings, you will still be able to launch the game through Mod Organizer 2 as usual which will not forcibly update the game and allow you to stay on the previous version for however you long you like, or until SKSE and the Wabbajack list are updated.

### English language requirement

No Wabbajack lists currently support languages other than English, and attempting to run Wabbajack with non-English base files will result in a strange mix of both languages. Localisation is not as easy as editing string files; the names for most objects, etc, are defined in plugins. Patching an entire Wabbajack list for any non-English language would be a considerable amount of work.

**Non-English setups will not receive support.**

## Installation Directory

In order for Wabbajack and Mod Organizer 2 to work properly, **you must install Skyrim SE outside any protected folders**. These folders include `C:\Program Files\` or `C:\Program Files x86\`. As Steam is installed into one of these folders by default and Steam games are installed within the Steam installation folder by default, you will need to adjust some settings.

Steam installs game files into so called **Libraries**. These are folders in which you will then be able to install various games in. For example, here is [my primary Steam Library](/Pictures/wj/sse/steam-library-example.png). As you can see, it is on another SSD and not located within the `\Steam\` root folder. If you have Steam installed in a UAC protected folder, you will need to create a new Steam Library *outside* that folder and install Skyrim SE there.

Folders that you should **not** use include these:

- `C:\Program Files\`
- `C:\Program Files x86\`
- `C:\Users\` (which includes Downloads, Documents, Desktop, etc,)

Generally speaking a top-level folder such as `G:\Steam Games\` is preferable. It should also ideally be located on an **SSD**.

### Creating a new Steam Library

If you did not install Steam in any UAC protected folders or you already have an additional Steam Library outside any UAC protected folders, you can skip this step.

Otherwise follow these instructions to create a new Steam Library:

- Open **Steam** and go into the **Settings**.
- In the **Downloads** tab, select **Steam Library Folders**.
- Click **Add Library Folder**.
- Point it to a location somewhere outside the UAC protected folders, for example `G:\Steam Library\`.
- Close all windows when you’re done.

> It is important to note that Steam only allows one **Steam Library** per hard drive. However, there is a workaround: If you already have a **Steam Library** on your C:\ drive but inside a UAC protected folder and you want to have Skyrim and your mod files on the same drive, please check out [LostDragonist’s Steam Library Setup Tool](https://github.com/LostDragonist/steam-library-setup-tool/wiki/Usage-Guide).

![New Library](/Pictures/tpf/initial-setup/new-steam-library.png)

## Reinstalling Skyrim

Since all preparations have now been completed, we can reinstall the game through Steam:

- Find **Skyrim** in your games library and click the **Install** button.
- Choose a Steam Library outside UAC protected folders as the location for the install.
- Wait until Skyrim has been fully downloaded and installed before you proceed.

**After Skyrim is installed, please launch the game once.** You can start it through Steam and quit from the main menu. This will set up necessary hooks in the registry without which certain tools would not be able to detect that the game is installed.

### Directories

Navigate to `\Your Steam Library\steamapps\common\Skyrim Special Edition\`.

This is your **root** folder. It contains the executables (**SkyrimSE.exe** and **SkyrimSELauncher.exe**) and you will be required to install several other files into this directory later on. Mod managers such as Mod Organizer 2 do not affect this folder.

Within the **root** folder you will find the **data** folder. Open it now. This is where all vanilla game files are stored in **plugins** (ESMs) and **archives** (BSAs). This is also the folder in which all mod files belong. Mod Organizer 2 will not actually move files here, it creates instead a virtual version of it, meaning the actual **data** folder will remain in its pristine vanilla state.

Try to remember the difference between **root** and **data** folder as it will make understanding any further instructions much easier.

- **Root:** `\Your Steam Library\steamapps\common\Skyrim Special Edition\`
- **Data:** `\Your Steam Library\steamapps\common\Skyrim Special Edition\Data\`

## Creation Club

The Creation Club was added for Skyrim SE and Fallout 4 in 2017. It features additional content in the form of small packages, Creations, which are sold for real-world money. By default, Wabbajack lists do not support Creations except when explicitly stated. Any Creations you own should be removed from your game files before installing a Wabbajack list. If your chosen list supports Creations, you can later re-install them as mods through Mod Organizer 2.

Creations you own should have been re-downloaded alongside the game when you re-installed it. 

- Navigate to your **data** folder.

This is where any Creations will be installed. You will recognise them by their names as they are always prefixed with **cc** for "Creation Club" [as you can see here](/Pictures/wj/sse/data-folder-creations.png). Creations consist of one **ESL** plugin and one or more archives (**BSAs**).

- Move any files prefixed with **cc** out of your **data** folder for the time being.
- I recommend keeping them as backups somewhere on your hard drive.

## Conclusion

After following all steps, you now have a properly prepared Skyrim SE installation that you can install a Wabbajack list for. Please continue with the [List Installation](/wj/wj-sse/list-installation/) page.