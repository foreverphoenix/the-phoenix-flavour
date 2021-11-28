---
title: "Step 2: Skyrim and Steam"
weight: 2
type: docs
description: >
  Configuring Skyrim SE and Steam settings.
---

## Spring Cleaning

If you ever modded Skyrim before, chances are you have left-over files in various directories. The first step in this guide is going to be cleaning those up as they can interfere with the TPF setup.

**If you have Skyrim SE installed, please uninstall it now.** Don't skip this step, even if you never modded Skyrim.

Unfortunately, when uninstalling the game through Steam, only vanilla files will be removed while mod-added files will stay. If you did mod the game previously, please navigate to your Steam games directory which is probably:

 `C:\Program Files x86\Steam\steamapps\common\` 

Delete the **Skyrim Special Edition** folder if it is still there.

### Documents Folder

> If you literally just bought Skyrim SE and never ran it, this folder will not exists on your hard drive and you can skip to the next step.

Additional configuration files as well as your save games are stored in the `\Documents\My Games\Skyrim Special Edition\` directory. We will remove this folder also and then regenerate a fresh set of INI files later on.

- Navigate to `C:\Users\<Your User Name>\Documents\My Games\Skyrim Special Edition\`.

If you have vanilla save files that you would like to keep, you need to back them up now. Copy the **saves** folder to `\Your Modding Folder\Backups\`. From there you can restore it anytime you wish. 

- Delete the `\My Games\Skyrim Special Edition\` folder with all its contents.

## Game Language

Non-English installations are not supported. Skyrim SE must be set to English in Steam.

- Right-click **The Elder Scrolls V: Skyrim Special Edition** in your Steam games library.
- Select **Properties** and switch to the **Language** tab.
- Ensure that the language is set to **English**.

![Skyrim SE English](/Pictures/tpf/initial-setup/skyrim-se-english.png)

## Reinstallation

From TPF 5.0 onward, we are using the **Stock Game** folder system for which we will copy all game files to a custom directory. This means that where you let Steam install the base game does not matter anymore. It does not need to be on the same hard drive as your modded setup.

It is usually recommended to download Skyrim SE to a location outside of any UAC-protected folders. These include `C:\Program Files` and `C:\Program Files x86` as well as any default folders like Documents, Downloads, or Desktop. UAC-protected folders have higher security standards in Windows which may interfere with modding tools.

However, for TPF this will not matter since we are going to create a second installation folder anyway.

- Reinstall **Skyrim SE** through **Steam**.

---

**Wait for the download to finish before you proceed.**

### Quick Launch

After (re)-installing, updating, or verifying Skryim SE, you always need to launch the game once so that the registry keys are set up and the INI files are regenerated. This is absolutely necessary for other tools to be able to find and recognise the game.

- Launch **Skyrim SE** through **Steam**.
- A window will come up, informing you that Skyrim SE will now be configured based on your hardware.
- Click **OK** twice to confirm and hit **Exit** once it’s done.

> If Skyrim is unable to detect your hardware, it's likely because you have a newer graphics card. You can safely ignore this as we will be configuring the INI files through BethINI later on.
 
![Regenerating INIs](/Pictures/tpf/initial-setup/regenerating-inis.png)

## Disable Auto Updates

When Skyrim SE receives another update - which, thanks to the Creation Club, happens every once in a while - Address Libary for SKSE will need an update. Substantial updates may even require SKSE to be updated which can disrupt the modding scene for weeks. Stock Game folder will protect you from automatic updates that would otherwise render you unable to start the game, but preventing automatic updates is still recommended.

You can continue to play the previous version of Skyrim SE with SKSE64 and all your mods by simply setting the game to only update when launching it (through Steam). Since you start the game through the SKSE64 launcher, Steam will never update.

- Open Steam and find **The Elder Scrolls V: Skyrim Special Edition** in your **Game Library**.
- Right-click it, select **Properties** and switch to the **Updates** tab.
- Make sure **Automatic updates** is set to **Only update this game when I launch it**.
- Problem solved!

![Disable Auto Updates](/Pictures/tpf/initial-setup/sse-disable-auto-updates.png)

## Creations

If you own the Anniversary Edition, bought any creations separately, or grabbed some while they were up for free, they will be re-installed alongside Skyrim SE. **The guide does not support Creation Club content** so you will have to move them away from the game files.

*However, there are TPF Addons that do add Creation Club support. If you choose to install any of them later on, you will then be able to reinstall the respective “creations” as mods from your backups.*

- Create a new folder: `Your Modding Folder\Backups\Creation Club`.
- Select all files beginning with **cc** (ESLs and BSAs) in your **Data** folder and hit CTRL+X.
- Navigate to your new **Creation Club** folder and paste them there (CTRL+V)

## Disable Steam Overlay

> This step is optional.

While I’ve never had any issues with the Steam Overlay in modded Skyrim SE, that seems to be an exception and it is indeed common practice to disable it as a precaution. Note that after following the instructions below the overlay will only be disabled for Skyrim SE, not for other games.

Since disabling the Steam Overlay will also prevent you from taking screenshots with Steam, I personally keep it enabled. Again, it never caused me trouble.

- Open Steam and find **The Elder Scrolls V: Skyrim Special Edition** in your games library.
- Right-click it, select **Properties**.
- Uncheck **Enable the Steam Overlay while in-game**.
- Close the window.

---

#### Continue with the [Mod Organizer 2](/tpf/initial-setup/step-3/) page.