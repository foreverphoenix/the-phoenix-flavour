---
title: "Skyrim and Steam"
weight: 2
type: docs
description: >
  Configuring Skyrim SE and Steam settings.
---

## Recommended Directory

The entire point of reinstalling Skyrim SE is not only to make sure you have a clean, vanilla setup but also to be able to control where the game is installed on your drive. Here is what you need to keep in mind:

- **Avoid UAC protected folders.** UAC protected folders and their contents have higher security standards than other folders which can cause all kinds of issues for modding tools. To prevent any such issues from occuring in the future, never install any modding tools or the game under `C:\Program Files` or `C:\Program Files x86`.

- **Further considerations:** While it is highly recommend to install the modded game on an SSD for faster loading screens and potential decrease or elimination of stuttering, be aware that a large amount of free space is required. This is because  Skyrim SE and Mod Organizer 2 should be installed on the same drive. While the Skyrim SE base installation reaches around 12.5GB, your MO2 directory will eventually grow well beyond 50GB in size, depending on the amount and types of mods you add. If you can spare 100GB or more of SSD space, it is highly recommended you do so.

> Installing Skyrim SE or any related tools in an UAC protected folder will disqualify from getting support on our Discord server.

## Uninstall Skyrim SE

*Skip this step if you do not have Skyrim SE installed.*

- Open Steam and go to your **Library**.
- Find **The Elder Scrolls V: Skyrim Special Edition** in the list.
- Right-click it and select **Uninstall**.
- Navigate to wherever Skyrim SE was previously installed and delete any left-over files.

## New Steam Library

For the purpose of the guide (to prevent confusion) I will refer to the Library in Steam as the **Game Library**. It is the second of four items in the top menu in Steam and contains a list of all your games.

A **Steam Library** on the other hand is a directory on your hard drive into which your Steam games are installed. By default this would be `C:\Program Files x86\Steam\steamapps\common\`. Since we do not want to have files inside an UAC protected folder like Program Files x86, we should not install Skyrim SE in the default directory. A new **Steam Library** is required.

> It is important to note that Steam only allows one **Steam Library** per hard drive, although there is a workaround. If for instance you already have a **Steam Library** on your C:\ drive, but you want to have your modding files on the same drive, you need to create a new **Steam Library** manually following the instructions [here](https://steamcommunity.com/discussions/forum/1/135511294066324002).

If you already have a separate Steam Library outside the UAC protected folders on the drive you want to install Skyrim SE and Mod Organizer 2 on, skip ahead to section 2.4. Otherwise follow the instructions below to create a new **Steam Library**:

* Open Steam and go into the **Settings**.
* In the **Downloads** tab, select **Steam Library Folders**.
* Click **Add Library Folder**.
* Point it to a location somewhere outside the UAC protected folders.
  * For example: `G:\Steam Library\`
* Close all windows when you’re done.

## Game Language

Non-English installations are not supported. Please make sure Skyrim SE is set to English in Steam.

- Right-click **The Elder Scrolls V: Skyrim Special Edition** in your Steam games library.
- Select **Properties** and switch to the **Language** tab.
- Ensure that the language is set to **English**.

![Skyrim SE English](/Pictures/tpf/initial-setup/skyrim-se-english.png)

## Reinstallation

* Find **The Elder Scrolls V: Skyrim Special Edition** in your Steam games library and click **Install**.
* As location, select the **Steam Library** you just created.
* Wait for Skyrim SE to be downloaded and installed.

## Version Number

Because the Script Extender and certain other mods are version dependent, you must run a specific version of Skyrim SE. That is typically the latest version unless there was an update recently and the community hasn't caught up yet in which case you need to roll back.

The currently supported version of Skyrim SE is: **1.5.97**.

> If you accidentally updated to a newer version, please refer to [this guide here](https://www.nexusmods.com/skyrimspecialedition/mods/19658) in order to roll back.

### How to check version number

* Navigate to your **root** folder.
* Right-click **SkyrimSE.exe** and select **Properties**.
* Switch to the **Details** tab and check under **Product version**.

![Skyrim SE 1.5.97.0](/Pictures/tpf/initial-setup/skyrim-se-1-5-97-0.png)

## Disable Auto Updates

When Skyrim SE receives another update - which, thanks to the Creation Club, happens every once in a while - SKSE64 and all SKSE plugins will need to be updated as well. This usually takes at least a week.

However, you can continue to play the previous version of Skyrim SE with SKSE64 and all your mods by simply setting the game to only update when launching it (through Steam). Since you start the game through the SKSE64 launcher, Steam will never update.

* Open Steam and find **The Elder Scrolls V: Skyrim Special Edition** in your **Game Library**.
* Right-click it, select **Properties** and switch to the **Updates** tab.
* Make sure **Automatic updates** is set to **Only update this game when I launch it**.
* Problem solved!

![Disable Auto Updates](/Pictures/tpf/initial-setup/sse-disable-auto-updates.png)

## Executables Backup

Although Steam will no longer update Skyrim SE automatically, I still recommend keeping backups of the two executables (**SkyrimSE.exe** and **SkyrimSELauncher.exe**), just in case. If you accidentally updated, all you need to do to roll back is replace the executables in your **root** folder with the ones you backed up. This also comes in handy if you had to regenerate INI files or validate game files through Steam for whatever reason and were forced to update.

* Create a new folder: `Your Modding Folder\Backups\Skyrim SE 1.x.x` (enter the current version number).
* Copy the following two files from your **root** folder into the new directory:
  * **SkyrimSE.exe**
  * **SkyrimSELauncher.exe**

## Creations

If you bought anything from the Creation Club (or grabbed "creations" while they were up for free), they will be re-installed alongside Skyrim SE. **The guide does not support Creation Club content** so you will have to move them away from the game files.

- Create a new folder: `Your Modding Folder\Backups\Creation Club`.
- Select all files beginning with **cc** (ESLs and BSAs) in your **Data** folder and hit CTRL+X.
- Navigate to your new **Creation Club** folder and paste them there (CTRL+V)

## Disable Steam Overlay

> **This step is optional.**

While I’ve never had any issues with the Steam Overlay in modded Skyrim SE, that seems to be an exception and it is indeed common practice to disable it as a precaution. Note that after following the instructions below the overlay will only be disabled for Skyrim SE, not for other games.

Since disabling the Steam Overlay will also prevent you from taking screenshots with Steam, I personally keep it enabled. YMMV.

* Open Steam and find **The Elder Scrolls V: Skyrim Special Edition** in your games library.
* Right-click it, select **Properties**.
* Uncheck **Enable the Steam Overlay while in-game**.
* Close the window.

---

#### Continue with the [Creation Kit](/tpf/initial-setup/the-creation-kit/) page.