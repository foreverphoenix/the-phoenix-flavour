---
title: "Step 1: Skyrim Setup"
weight: 1
type: docs
description: >
  Placeholder.
---

Before we can dive into modding Skyrim, we need to make sure that you are equipped with the correct version of the game, installed in the correct directory.

As stated in the [Introduction](/bg/introduction/), this guide requires the [Steam version](https://store.steampowered.com/app/489830/The_Elder_Scrolls_V_Skyrim_Special_Edition/) of Skyrim Special Edition. It does not cover Skyrim Legendary Edition or Skyrim VR modding, and will not work with the Microsoft Store or Epic Games Store versions of Skyrim SE.

> If you want to know more about the various versions of Skyrim and how they differ with regards to modding, [refer to this article].

## Spring Cleaning

Before starting a new modded setup, an often overlooked but essential step is a full clean install of the game. We need to make sure your copy of Skyrim is absolutely pristine and that no traces of previous modding setups remain on your PC. 

If you currently have the game installed: **Uninstall Skyrim SE through Steam**.

## Mod Files

> You can skip this step if you never modded Skyrim SE before.

Navigate to where the game was installed which is probably `C:/Program Files x86/Steam/steamapps/common/`. If there is still a **Skyrim Special Edition** folder in this location after uninstalling the game through Steam, it means you had non-vanilla (mod-added) files in your game folder. These are not removed when uninstalling the game and may get in the way of your new setup.

Delete the **Skyrim Special Edition** folder if it still exists after uninstalling the game.

### Documents Folder

> You can skip this step if you never run Skyrim SE on this PC before because this folder will not exist.

Next, we will take a look at the Documents folder. Navigate to `C:/Users/Your User Name/Documents/My Games/Skyrim Special Edition/`.

This directory may contain multiple files and folders: The **Skyrim.ini** and **SkyrimPrefs.ini** are the game’s primary configuration files, they will become very relevant later on. There may also be a **saves** folder which, you guessed it, contains your save games. Lastly, the Documents folder may also include mod-generated files such as logs.

- If you have save files that you want to keep, *back them up now*.
- Delete the entire **Skyrim Special Edition** folder.

The folder and INI files will be regenerated very soon.

And that is it. Skyrim SE is completely removed from your system.

## Game Language

Skyrim supports a bunch of different languages natively, but mods do not. Since many mods also do not require translations in the first place and some of the ones that do have third-party translations available, it is *theoretically* possible to play modded in Skyrim in a language other than English.

However, this will complicate your setup immensely. Translations, where available, may be outdated or incomplete. They may not cover voice acting. They may require editing of dozens of texture templates in Photoshop. They may not exist for some of your mods at all.

> Translating any mods untouched by existing patches plus fixing conflicts between translations and mods will add a hefty amount of work on top of everything else. I do not recommend it, especially not for a beginner.

**An English-language installation of Skyrim SE is mandatory for this guide.**

- Right-click **The Elder Scrolls V: Skyrim Special Edition** in your Steam games library.
- Select **Properties** and switch to the **Language** tab.
- Ensure that the language is set to **English**.

![Steam Set Language](steam-set-language.webp)

## Installation Directory

It is highly recommended to install the game to your fastest hard drive, ideally an SSD, which will reduce up load times. Running Skyrim from an HDD may negatively impact performance, causing stuttering and frame drops.

Additionally, Skyrim must not be located within a UAC-protected folder.

### UAC-Protected Folders

Your Steam installation is probably located under `C:\Program Files x86\Steam\` and, by default, all Steam games are installed inside the Steam directory under `\Steam\steamapps\common\<Game>\`. The problem here is that `C:\Program Files\` and `C:\Program Files x86\` are so-called UAC-protected folders (UAC = user account control). UAC-protected folders in Windows are special because they require admin privileges for read/write permissions which can break various modding tools.

Because of this, Skyrim SE must be installed to a location outside any UAC-protected folders.

### Steam Libraries

When installing a game through Steam, you can select any of your Steam Libraries as installation folder. The default Steam Library is within the Steam installation itself. If you installed Steam in `C:\Program Files x86\`, you will need to create a new Steam Library in a different location.

> If you already have a second Steam Library outside UAC-protected folders, skip ahead to **Reinstalling Skyrim**.

By default, you can only have one Steam Library per hard drive. If you want to create a second Steam Library on the same hard drive that you installed Steam on, please use LostDragonist’s [Steam Library Setup Tool](https://github.com/LostDragonist/steam-library-setup-tool/wiki/Usage-Guide) and follow the instructions from the link.

If you want to create a new Steam Library on another hard drive, follow these steps:

- Open the **Settings** in Steam and go to the **Downloads** tab.
- Click the **Steam Library Folders** button.
- Choose the drive and folder for your new Steam Library directory through the interface.

Once set up, the new Steam Library can be selected as the installation directory upon installing a new game.

## Reinstalling Skyrim

Now you can reinstall Skyrim. Find the game in the Steam app and click the big blue Install button. As the installation location choose a Steam Library on your fastest hard drive and outside UAC-protected folders.

**Proceed when the download is completed.**

## Test Run

At this point, we should see if Skyrim launches properly. Running the game once serves multiple purposes:

- The `\Documents\My Games\Skyrim Special Edition\` folder including its INI files will be regenerated.
- The registry keys will be set up which is required for modding tools to recognise your installation.
- Certain issues with your vanilla game can be detected now.
  
> Always remember to launch Skyrim once after updating or re-installing it, or after verifying game files.

**Launch the game through Steam.**

- A message box will pop up, informing you that Skyrim SE will now be configured based on your hardware.
- Click **OK** twice to confirm (we will modify the INI files later on*).
- Click the **PLAY** option in the launcher and wait until you are in the Skyrim main menu.

> **AE owners:** Skyrim will prompt you with a message box, then proceed to download the creations. Wait for it to finish.

- Quit the game from the main menu. If you got this far, everything appears to be running smoothly.

\**If Skyrim is unable to detect your hardware, it is likely because you have a newer graphics card. You can safely ignore this as we will regenerate INIs from scratch later on.*

---

[Continue with Step 2.](/bg/module-1/step-2/)