---
title: "Clean Install"
weight: 2
type: docs
description: >
  How to perform a clean install of Skyrim SE.
---

## Uninstalling Skyrim

If you ever modded Skyrim before, chances are you have left-over files in various directories. We will thus begin with a bit of spring cleaning and make sure we start from a clean slate.

If you currently have Skyrim installed, please begin by uninstalling the game.

- Find **Skyrim Special Edition** in your Steam Library.
- Right-click the game and select **Manage** > **Uninstall**.
- Click **Uninstall** again in the message box that follows to confirm.

![Uninstall Skyrim](/Pictures/manual/setup/clean-install/uninstall-skyrim.png)

### Creation Kit

If you had the **Creation Kit** for Skyrim SE installed through Steam, uninstall it in the same way.

### Mod Files

{{< alert color="info" >}}Skip this step if you never modded Skyrim before.{{< /alert >}}

Steam will uninstall all vanilla files but it will not touch mod files. Any leftover files added by mods must be deleted manually.

- Navigate to where the game was installed (most likely `C:\Program Files x86\Steam\steamapps\common\`).
- If there is still a **Skyrim Special Edition** folder in this location, delete it.

### INI Folder

{{< alert color="info" >}}Skip this step if you never played Skyrim SE on this PC before (the folder would not exist).{{< /alert >}}

When clean-installing Skyrim, the **INI Folder** should be cleared out as well -- not only to remove clutter but also to ensure that a fresh set of INI files can be acquired later on.

- Navigate to `C:\Users\<Your User Name>\Documents\My Games\Skyrim Special Edition\`.
 
{{< alert color="warning" >}}If you have save files that you want to keep, make a backup of the **saves** folder now.{{< /alert >}}

- Delete the entire **Skyrim Special Edition** folder.

The folder and INI files will be regenerated upon launching the game after the reinstallation.

{{< alert color="success" >}} And that is all. Skyrim SE is now completely removed from your system.{{< /alert >}}

## Game Language

{{< alert color="info" >}}Skip this step if you never changed the game language.{{< /alert >}}

An English-language installation of Skyrim is <u>mandatory</u> for TPF.

- Right-click **The Elder Scrolls V: Skyrim Special Edition** in your Steam games library.
- Select **Properties** and switch to the **Language** tab.
- Ensure that the language is set to **English**.

![english](/Pictures/manual/setup/clean-install/steam-skyrim-english.png)

## Installation Directory

Before reinstalling Skyrim, we need to select an adequate location. There are two aspects to keep in mind:

1. **Skyrim should be installed to your fastest drive** -- ideally an SSD -- which will reduce load times. Running Skyrim from an HDD negatively impacts performance, causing stuttering and frame drops.
2. Additionally, **Skyrim <u>must not</u> be located within any UAC-protected folders** as this may prevent modding tools from properly accessing the game files.

### UAC-Protected Folders

Your Steam installation is probably located inside `C:\Program Files x86\Steam\`. By default, all Steam games are installed within this folder in `\Steam\steamapps\common\<Game>\`.

The problem is that `C:\Program Files\` and `C:\Program Files x86\` are so-called **UAC-protected folders** (UAC = user account control). UAC-protected folders in Windows are special because they require admin privileges for read/write permissions. This can break functionality in modding tools.

{{< alert color="warning" >}}Therefore, Skyrim should be installed to a location <u>outside</u> any UAC-protected folders.{{< /alert >}}

### Steam Libraries

When installing a game through Steam, you can select any of your **Steam Libraries** as the installation folder. A Steam Library is simply a folder on one of your harddrives that has been set in Steam as an installation directory for games. The default Steam Library is contained within the Steam installation folder itself. 

If you installed Steam under `C:\Program Files x86\` you will need to create a new Steam Library in a different location. Once set up, the new Steam Library can be selected as the installation directory upon installing a new game.

{{< alert color="warning" >}}Skip ahead to [Reinstalling Skyrim](/manual/setup/skyrim-and-steam#reinstalling-skyrim) if you already have a Steam Library outside UAC-protected folders.{{< /alert >}}

#### Option 1 -- On the same drive

By default, you can only have one Steam Library per hard drive. If you want to create a second Steam Library on the same hard drive that you installed Steam on, please use [LostDragonist’s Steam Library Setup Tool](https://github.com/LostDragonist/steam-library-setup-tool/wiki/Usage-Guide) and follow the instructions from the link.

#### Option 2 -- On a different drive

If you want to create a new Steam Library on a drive that is not `C:\`, follow these steps:

- Open the **Settings** in Steam and go to the **Storage** tab.
- Find the little ➕ icon near the top to add a new Steam Library.
- Select the desired hard drive.

![Add Steam Library](/Pictures/manual/setup/clean-install/add-steam-library.png)

## Reinstalling Skyrim

Now we can finally reinstall Skyrim.

- Find the game in the Steam Library tab and click the big blue Install button.
- As the installation location choose a Steam Library on your fastest hard drive and outside UAC-protected folders.
    - Example: `X:\SteamLibrary\steamapps\common\Skyrim Special Edition\`
- Proceed when the download is completed.

![Install Skyrim](/Pictures/manual/setup/clean-install/install-skyrim.png)

## Test Run

Last but not least we should make sure that our new installation of Skyrim launches properly. 

Running the game after reinstallation serves multiple purposes:

- To regenerate the `\Documents\My Games\Skyrim Special Edition\` folder. This includes the generation of a fresh set of INI files.
- To set up the registry keys, which is required for modding tools to recognise your installation.
- To detect issues with your vanilla game (i.e., file corruption during the installation).

{{< alert color="warning" >}}Always launch Skyrim once after updating or reinstalling the game, or after verifying game files.{{< /alert >}}

- Launch Skyrim through Steam.

A message box will pop up, informing you that Skyrim SE will now be configured based on your hardware. If Skyrim is unable to detect your hardware, it is likely because you have a newer graphics card that is not recognised. You can ignore the warning.

- Click **OK** twice to confirm. We will configure the INI files later on.
- Click the **PLAY** option in the launcher and wait until you are in the Skyrim main menu.
- Skyrim will prompt you with a message box and proceed to download all creations. Wait for it to finish.
- Quit the game from the main menu.

### File and Folder Structure Basics (*)

Before you proceed with the next step, I highly recommend taking a moment to [read this article](/manual/resources/folder-structure/) on folder structure and terminology. It's a quick read without additional instructions and will help you better understand the instructions in the next step. 

---

<font size=4>Continue with [Mod Organizer 2](/manual/setup/mo2/).</size>