![Logo](../Media/tpf_logo.png)

**TABLE OF CONTENTS**
- [01. Getting Started](#01-getting-started)
  - [1.1 Requirements](#11-requirements)
  - [1.2 Show File Extensions](#12-show-file-extensions)
  - [1.3 Your Modding Folder](#13-your-modding-folder)
  - [1.4 Monitor Calibration](#14-monitor-calibration)
  - [1.5 Further Instructions](#15-further-instructions)
  - [1.5.2 Terminology](#152-terminology)
- [02. Skyrim SE](#02-skyrim-se)
  - [2.1 Recommended Directory](#21-recommended-directory)
  - [2.2 Uninstall Skyrim SE](#22-uninstall-skyrim-se)
  - [2.3 New Steam Library](#23-new-steam-library)
  - [2.4 Reinstallation](#24-reinstallation)
  - [2.5 Version Number](#25-version-number)
  - [2.6 Disable Auto Updates](#26-disable-auto-updates)
  - [2.7 Binaries Backup](#27-binaries-backup)
  - [2.8 Disable Steam Overlay](#28-disable-steam-overlay)
- [03. The Creation Kit](#03-the-creation-kit)
  - [3.1 Acquisition](#31-acquisition)
  - [3.2 Installation](#32-installation)
  - [3.3 Disable Auto Updates](#33-disable-auto-updates)
  - [3.4 Custom INI](#34-custom-ini)
  - [3.5 Creation Kit Fixes](#35-creation-kit-fixes)
  - [3.6 Vanilla Scripts](#36-vanilla-scripts)
- [04. Mod Organizer 2](#04-mod-organizer-2)
  - [4.1 Installation](#41-installation)
  - [4.2 Configuration](#42-configuration)
  - [4.3 Manage Mod Downloads](#43-manage-mod-downloads)
  - [4.4 User Interface](#44-user-interface)
  - [4.5 Custom Profiles](#45-custom-profiles)
  - [4.6 Deorder's MO2 Plugins](#46-deorders-mo2-plugins)
  - [4.7 Separators](#47-separators)
- [05. Skyrim Script Extender](#05-skyrim-script-extender)
  - [5.1 Download](#51-download)
  - [5.2 Installation](#52-installation)
  - [5.3 SKSE INI](#53-skse-ini)
  - [5.4 SKSE Launcher](#54-skse-launcher)
  - [5.5 Verify Installation](#55-verify-installation)
- [06. INI Files](#06-ini-files)
  - [6.1 Generate Fresh INI Files](#61-generate-fresh-ini-files)
  - [6.2 Install BethINI](#62-install-bethini)
  - [6.3 BethINI Configuration](#63-bethini-configuration)
  - [6.4 Save Changes](#64-save-changes)
- [07. Additional Tools](#07-additional-tools)
  - [7.1 SSEEdit](#71-sseedit)
  - [7.2 zEdit](#72-zedit)
  - [7.4 Cathedral Assets Optimizer (CAO)](#74-cathedral-assets-optimizer-cao)
  - [7.5 SSE NIF Optimizer](#75-sse-nif-optimizer)
  - [7.6 Modwatch](#76-modwatch)
- [08. ESM Cleaning](#08-esm-cleaning)
  - [8.1 About ESM Cleaning](#81-about-esm-cleaning)
  - [8.2 Export Files to MO2](#82-export-files-to-mo2)
  - [8.3 Automated Cleaning Process](#83-automated-cleaning-process)
  - [8.4 Manual Cleaning - Update ESM](#84-manual-cleaning---update-esm)
  - [8.5 Manual Cleaning - Dawnguard ESM](#85-manual-cleaning---dawnguard-esm)
- [09. Skyrim Realistic Overhaul](#09-skyrim-realistic-overhaul)
  - [9.1 Download](#91-download)
  - [9.2 File Extraction](#92-file-extraction)
  - [9.3 Processing with CAO](#93-processing-with-cao)
  - [9.4 Installation](#94-installation)
- [10. Mod Installation Instructions](#10-mod-installation-instructions)
  - [10.1 Overview](#101-overview)
  - [10.2 General Instructions](#102-general-instructions)
  - [10.3 Special Instructions](#103-special-instructions)

# 01. Getting Started

## 1.1 Requirements

- [Skyrim Special Edition](https://store.steampowered.com/app/489830/The_Elder_Scrolls_V_Skyrim_Special_Edition/) on Steam.
- A legit Windows 7 / 8 / 8.1 / 10 installation (64bit).
- The editing software [Notepad++](https://notepad-plus-plus.org/) (freeware).
- An archiving tool like [7zip](https://www.7-zip.org/download.html) or [WinRAR](https://www.win-rar.com/start.html?&L=0).
- Latest drivers for your GPU ([NVIDIA](https://www.nvidia.de/Download/index.aspx) or [AMD](https://www.amd.com/en/support)).
- A free (or Premium) account on [Nexus Mods](https://www.nexusmods.com/).

> With a **Nexus Premium** subscription you will be able to complete the guide in significantly less time since you will benefit from the uncapped download speeds (which obviously depend on your internet connection as well). A one month subscription costs £2.99, giving you more than enough time to complete the guide.

## 1.2 Show File Extensions

By default file extensions (such as EXE, PNG or ESP) are hidden in the Windows Explorer. Since it's fairly important to be able to see them during the installation of the guide, I recommend double-checking that you have them set to visible.

- Open the Windows Explorer.
- Click the **View** tab at the top.
- Make sure **File name extensions** is checked.

![File Extensions Visible](Pictures/Setup/file_extensions_visible.png)

## 1.3 Your Modding Folder

In order to keep all files related to modding Skyrim SE in one place, we will create a dedicated directory. It will serve as a hub for all tools, downloaded mod archives, custom files, notes, backups, screenshots and whatever else you can think of.

Throughout the guide I will refer to this folder as **Your Modding Folder**.

### 1.3.1 Main Directory

- Create a new folder anywhere on an HDD with at least 200GB of free space. Don't waste SSD space on this.
- Name it whatever you like, for example **Skyrim SE Modding**.
- Add several more new folders inside as shown below:

![Modding Folder](Pictures/Setup/modding_folder.png)

### 1.3.2 Mod Archive

Proper organisation is key when modding Skyrim. You will come back many times to update or reinstall mods, or selectively extract files without installing the whole package. This is where the previously created **ARCHIVE** comes into play - it will contain the majority of downloaded mod archives.

- Create several more folders inside the **ARCHIVE** folder:

![Archive Folder](Pictures/Setup/archive_folder.png)

## 1.4 Monitor Calibration

### 1.4.1 Gamma and Brightness

Assuming you already have your monitor configured with your preferred settings for resolution and refresh rate (in my case that is 60Hz and 1920x1080), you might still want to adjust the brightness and / or gamma either through your graphics card control panel or Windows' inbuilt calibration tool.

> Your monitor should have been running for at least 30 minutes before you adjust it.

- **WINDOWS:** Control Panel > Colour Management > Advanced > Calibrate display
- **NVIDIA:** Control Panel > NVIDIA Control Panel > Adjust Desktop Color Settings
- **AMD:** Unfortunately I do not own an AMD GPU and never have so I cannot give advice here. Use the inbuilt Windows calibration tool.

To help you find the sweet spot for your monitor, check out these resources:

- [CLF ENB - monitor calibration help](https://i.imgur.com/k1v8p1M.png)
- [Photo Friday Monitor Calibration Tool](https://www.photofriday.com/info/calibrate)
- [Lagom: LCD monitor test images](http://www.lagom.nl/lcd-test/)

### 1.4.2 Dynamic Range

It is recommended that you ensure your monitor's **Dynamic Range** to "Full" if it is connected to your PC via DisplayPort or HDMI. Instructions for both NVIDIA and AMD based systems can be found [here](https://pcmonitors.info/articles/correcting-hdmi-colour-on-nvidia-and-amd-gpus/).

It turns out I actually had my monitor set to "Limited" for many years and grew so used to it that setting the Dynamic Range to "Full" only irritated me. Eventually I set it back to "Limited" with no regrets. Your mileage may vary.

## 1.5 Further Instructions

### 1.5.1 Rules

Before we finally jump into the actual guide, here are some critical pieces of information that I urge you to read **carefully** before  continuing:

- **Which parts are required?** All instructions and mods are mandatory unless they are clearly marked otherwise. A large portion of mods is marked as(optional) and you may safely skip them. **Do not skip required mods**. There are instructions for all mods with FOMOD installers and you are expected to follow them.

- **About additional mods:** Please wait until **after** you finished and tested your setup before adding more mods, otherwise you will no longer be eligible to receive support on our Discord server should you need it. We do not - and cannot - offer support for setups that are not 100% TPF. This includes **Creation Club** content.

## 1.5.2 Terminology

The difference between these folders is significant. Do not confuse them.

| Name            | File Path                                             | Content                  |
| --------------- | ----------------------------------------------------- | ------------------------ |
| **root folder** | `Steam/steamapps/common/Skyrim Special Edition/`      | contains the executables |
| **data folder** | `Steam/steamapps/common/Skyrim Special Edition/Data/` | contains the game files  |

![separator](../Media/separator.png)

# 02. Skyrim SE

## 2.1 Recommended Directory

The entire point of reinstalling Skyrim SE is not only to make sure you have a clean, vanilla setup but also to be able to control where the game is installed on your drive. Here is what you need to keep in mind:

- **Avoid UAC protected folders.** UAC protected folders and their contents have higher security standards than other folders which can cause all kinds of issues for modding tools. To prevent any such issues from occuring in the future, never install any modding tools or the game under `C:\Program Files` or `C:\Program Files x86`.

- **Further considerations:** While it is highly recommend to install the modded game on an SSD for faster loading screens and potential decrease or elimination of stuttering, be aware that a large amount of free space is required. This is because  Skyrim SE and Mod Organizer 2 should be installed on the same drive. While the Skyrim SE base installation reaches around 12.5GB, your MO2 directory will eventually grow well beyond 50GB in size, depending on the amount and types of mods you add. If you can spare 100GB or more of SSD space, it is highly recommended you do so.

> Installing Skyrim SE or any related tools in an UAC protected folder will disqualify from getting support on our Discord server.

## 2.2 Uninstall Skyrim SE

**Skip this step if you do not have Skyrim SE installed.**

- Open Steam and go to your **Library**.
- Find **The Elder Scrolls V: Skyrim Special Edition** in the list.
- Right-click it and select **Uninstall**.
- Wait for the process to complete before you continue.

## 2.3 New Steam Library

For the purpose of the guide - in order to prevent confusion - I will refer to the Library in Steam as the **Game Library**. It is the second of four items in the top menu in Steam and contains a list of all your games.

A **Steam Library** on the other hand is a directory on your hard drive into which your Steam games are installed. By default this would be `C:\Program Files x86\Steam\steamapps\common\`. Since we do not want to have files inside an UAC protected folder like Program Files x86, we should not install Skyrim SE in the default directory. A new **Steam Library** is required.

> It is important to note that Steam only allows one **Steam Library** per hard drive, although there is a workaround. If for instance you already have a **Steam Library** on your C:\ drive, but you want to have your modding files on the same drive, you need to create a new **Steam Library** manually following the instructions [here](https://steamcommunity.com/discussions/forum/1/135511294066324002).

If you already have a separate Steam Library outside the UAC protected folders on the drive you want to install Skyrim SE and Mod Organizer 2 on, skip ahead to section 2.4. Otherwise follow the instructions below to create a new **Steam Library**:

* Open Steam and go into the **Settings**.
* In the **Downloads** tab, select **Steam Library Folders**.
* Click **Add Library Folder**.
* Point it to a location somewhere outside the UAC protected folders.
  * For example: `G:\Steam Library\`
* Close all windows when you’re done.

## 2.4 Reinstallation

* Open Steam and go into your **Game Library**.
* Find **The Elder Scrolls V: Skyrim Special Edition** in the list and click **Install**.
* As location, select the Steam Library you just created.
* Wait for Skyrim SE to be downloaded and installed.

## 2.5 Version Number

Because the Script Extender and certain other mods are version dependent, you must run a specific version of Skyrim SE. That is typically the latest version unless there was an update recently and the community hasn't caught up yet in which case you need to roll back.

The currently supported version of Skyrim SE is: **1.5.97**.

> If you accidentally updated to a newer version, please refer to [this guide here](https://www.nexusmods.com/skyrimspecialedition/mods/19658) in order to roll back.

### 2.5.1 How to check version number

* Navigate to your **root** folder.
* Right-click **SkyrimSE.exe** and select **Properties**.
* Switch to the **Details** tab and check under **Product version**.

![Skyrim SE 1.5.97.0](Pictures/Setup/skyrim_se_1_5_97_0.png)

## 2.6 Disable Auto Updates

When Skyrim SE receives another update – which happens regularly because of the Creation Club – SKSE64 and all SKSE plugins will need to be updated as well. This usually takes around a week at least.

However you can continue playing the previous version with SKSE64 and all your mods by simply setting Skyrim SE to only update when launching the game – since you start the game through the SKSE64 launcher, Steam will never update.

* Open Steam and find **The Elder Scrolls V: Skyrim Special Edition** in your **Game Library**.
* Right-click it, select **Properties** and switch to the **Updates** tab.
* Make sure **Automatic updates** is set to **Only update this game when I launch it**.
* Problem solved!

![Disable Auto Updates](Pictures/Setup/sse_disable_auto_updates.png)

## 2.7 Binaries Backup

Although Steam will no longer update Skyrim SE automatically, I still recommend keeping backups of the two executables (**SkyrimSE.exe** and **SkyrimSELauncher.exe**), just in case. If you accidentally updated, all you need to do to roll back is replace the executables in your **root** folder with the ones you backed up. This also comes in handy if you had to regenerate INI files or validate game files through Steam for whatever reason and were forced to update.

* Create a new folder: `Your Modding Folder\Backups\Skyrim SE 1.x.x` (enter the current version number).
* Copy the following two files from your **root** folder into the new directory:
  * **SkyrimSE.exe**
  * **SkyrimSELauncher.exe**

## 2.8 Disable Steam Overlay

**This step is optional.**

While I’ve personally never had any issues with the Steam Overlay in modded Skyrim SE, that seems to be an exception and it is indeed common practice to disable it as a precaution. Note that we will only disable it for Skyrim SE. The overlay will still work as usual for all other games.

Since disabling the Steam Overlay will also prevent you from taking screenshots with Steam, I keep it enabled - as I said, without problems so far.

* Once again, open Steam.
* Find **The Elder Scrolls V: Skyrim Special Edition** in your Library.
* Right-click it and select **Properties**.
* Uncheck **Enable the Steam Overlay while in-game**.
* Close the window.

![separator](../Media/separator.png)

# 03. The Creation Kit

## 3.1 Acquisition

With the release of Skyrim SE, Bethesda also published a new version of their official tool kit, the Creation Kit (or CK for short), updated for the new 64bit engine. Unfortunately the CK 2.0 can no longer be downloaded directly from Steam but requires the Bethesda Launcher and a Beth.net account.

> The Bethesda Launcher is not required beyond installing the Creation Kit and you can safely uninstall it after that is done.

- Go to Bethesda.net, the official website.
- Scroll all the way down to the footer (bottom of the page).
- Click the **Download** button in the **Bethesda Launcher** section.
- Double-click the downloaded executable.

![Download Beth Launcher](Pictures/Setup/download_beth_launcher.png)

## 3.2 Installation

* Let the executable guide you through the installation process.
* When that is done, you must log-in with your Beth.net account or register a new one.
* Once you’re logged in, check the list of game icons on the left.
* Click the two arrows `>>` at the top to open the full list.
* Select **Creation Kit: Skyrim** (with the white icon) and click **Install**.
* The CK should be installed directly into your **root** folder (see picture).
* Wait for the files to download.

![Creation Kit Installation Path](Pictures/Setup/ck_installation_path.png)

## 3.3 Disable Auto Updates

* In the Bethesda Launcher, go to **Game Options**.
* Toggle off **Auto Updates**.
* Close the Bethesda Launcher.

![Disable Auto Updates](Pictures/Setup/ck_disable_auto_updates.png)

## 3.4 Custom INI

The custom INI file will allow you to load mods with multiple master files as well as fix some Creation Kit issues and crashes.

* Download this tweaked **[Creation Kit Custom INI](https://www.nexusmods.com/skyrimspecialedition/mods/19817)** (the main file) manually from the Nexus.
* Extract the INI file into your **root** folder.

## 3.5 Creation Kit Fixes

It’s Bethesda, what did you expect?

- Download **[SSE Creation Kit Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/20061)** (CK64 Fixes release 2.x) manually from the Nexus.
- Extract the three DLL files and the INI into your **root** folder.
- **Optional:** Move the archive to `Your Modding Folder\ARCHIVE\CK Fixes` to keep as a backup.

> We are not downloading the other CK Fixes main file because it is not needed for anyone except mod authors.

## 3.6 Vanilla Scripts

The Creation Kit installation includes a **Scripts.zip** which contains all source files for the vanilla Skyrim scripts. With these source files it is possible to edit and recompile vanilla scripts. This is usually unnecessary unless you plan on tinkering with the scripts themselves which we are in fact going to do at the very end of the guide.

### 3.6.1 Unpacking Scripts.zip

* Navigate to your **root** folder and launch **CreationKit.exe** from there.
* You will be asked to unpack **Scripts.zip**, click **Yes**.
* Once that is done, you can close the Creation Kit.

### 3.6.2 Fixing Filepaths

- Rename the **Source** folder in your **Data** folder to **Scripts**.
- Double-click the **Scripts** folder.
- Rename the **Scripts** folder inside to **Source**.
- The resulting filepath should be:
  - `Skyrim Special Edition\Data\Scripts\Source`

![separator](../Media/separator.png)

# 04. Mod Organizer 2

## 4.1 Installation

Installing MO2 with a portable instance means all of its subdirectories will be located inside the MO2 root folder which is required for some modding tools to work properly.

* Download **[Mod Organizer 2](https://www.nexusmods.com/skyrimspecialedition/mods/6194)** (the **Archive** version) manually from the Nexus.
* Extract the archive to a new folder on the same hard drive as your Skyrim SE installation, outside the UAC protected folders.
* Run **ModOrganizer.exe**.
* A window will come up – select **Portable** (see picture below).
* Next you will be asked which game to set MO2 up for. Normally it should recognise your Skyrim SE installation automatically.
* Select **Skyrim Special Edition** in the list.
* Confirm when asked to associate NXM links with MO2.
* Click **No** when prompted with the tutorial option.

![MO2 Choose Instance](Pictures/Setup/mo2_choose_instance.png)

## 4.2 Configuration

### 4.2.1 Mod Order Fix

- In the mod order (left pane), arrange the DLC as follows:
  - **DLC: Dawnguard**
  - **DLC: HearthFires**
  - **DLC: Dragonborn**

### 4.2.2 Tweaks

* Open the **Settings** (Tools > Settings or CTRL + S).
* In the **General** tab, check both boxes under **Download List**:
  * Show Meta Information
  * Compact List
* Switch to the **Workarounds** tab and check the following option:
  * Enable parsing of Archives (Experimental Feature)

### 4.2.3 Nexus Integration

* Switch to the **Nexus** tab where you need to connect your Nexus account to Mod Organizer 2.
* Click **Connect to Nexus**.
* This will open a Browser window where you will be asked to confirm.
* Click **Authorise**. You can revoke this any time in your Nexus settings.
* Mod Organizer 2 may ask you to restart. Click **OK**.

![Authorise MO2](Pictures/Setup/authorise_mo2.png)

## 4.3 Manage Mod Downloads

Most people use the "With Mod Manager" download option on the Nexus and then install the mod through their mod manager’s UI. That is the fastest and simplest way to download and install mods.

Since we installed MO2 as a portable application, all our mod archives would normally be downloaded into a sub-directory of the (MO2) root folder – which in turn may be located on your SSD or otherwise fastest hard drive. These archives are then extracted into their own folders meaning after their installation they only use up space.

On the other hand, keeping the archives as backups is highly recommended as mods are occasionally taken down from the Nexus or in case something goes wrong during the installation.

Here is where our **ARCHIVE** comes into play, the directory inside **Your Modding Folder** we set up to store all the mod files on a hard drive with plenty of free space. We will now configure Mod Organizer 2 to save all downloads to that folder.

* Once again, open the **Settings** in MO2 (Tools > Settings or CTRL + S).
* Switch to the **Paths** tab.
* Point **Downloads** to `Your Modding Folder\ARCHIVE\MO2 Downloads`.

![MO2 Archive](Pictures/Setup/mo2_archive.png)

## 4.4 User Interface

### 4.4.1 Components

You can now configure the UI to your liking. Personally I re-arrange the two panels so that the left one (mod order) is wider.

* Right-click the **Tool Bar** (coloured icons in the top left).
* Now you may choose which parts of the UI to display. I recommend disabling **Log** and **Status Bar** as you won’t need either.
* For the main **Tool Bar** you can decide between Icons or Text (or both), and, if you choose Icons, their size. This is up to you.

### 4.4.2 Dark Mode

If it’s the middle of the night and you prefer dark mode to go easy on your eyes, open the **Settings** (CTRL + S) and choose a different theme under **Styles**. Paper Black Mono or Paper Dark are the obvious choices but there are more options.

### 4.4.3 Mod Order

By right-clicking the top of the left pane, you can choose what to display in your mod order. Enable the following columns:

* **Conflicts**
* **Flags**
* **Content**
* **Version**
* **Source Game**
* **Priority**

![MO2 Customized](Pictures/Setup/mo2_customised.png)

## 4.5 Custom Profiles

### 4.5.1 Vanilla

* Open the **Profile** settings in MO2 (Tools > Profiles or CTRL+P).
* The **Default** profile will be selected automatically.
* Uncheck the following option at the bottom:
  * Use profile-specific Game INI Files
* When asked to delete the existing profile-specific INI files, click **Yes**.

> This profile is completely untouched. It uses the global INI and save files from the INI folder, and running Skyrim SE through it will be exactly like running it from Steam. 

### 4.5.2 Modded

* Click **Copy** to set up a second profile based on the **Default** one.
* Enter **"The Phoenix Flavour"** as the name.
* Select your new profile in the list.
* Check both options at the bottom:
  * Use profile-specific Save Games
  * Use profile-specific Game INI Files
* Click **Close** to exit the settings.
* In the profile list below the top left menu in MO2, select your new profile to switch to it.

> This new profile is separate from your vanilla install. It uses its own directories for INI and save files.

## 4.6 Deorder's MO2 Plugins

Removing and re-activating plugins included in a merge can be more than a little annoying. Fortunately there is a plugin by Deorder to hide and unhide those plugins at any time directly through the MO2 UI.

Bundled with Merge Plugins Hide comes another useful plugin, Sync Mod Order. This one allows you to update one profile's mod order to mirror another's.

### 4.6.1 Installation

* Open the Github page for [deorder’s MO2 Plugins](https://github.com/deorder/mo2-plugins/releases).
* Download the latest version by clicking on **Source code (zip)**.
* Open the downloaded archive and double-click the folder inside.
* Navigate to `Mod Organizer 2\plugins`.
* Extract the following folder and files from the archive into the **plugins** folder:
  * **data**
  * **pyMergePluginsHide.py**
  * **pySyncModOrder.py**
* Confirm when asked to merge the **data** folders.

![Install Deorders Plugins](Pictures/Setup/install_deorders_plugins.png)

### 4.6.2 Configuration

- Close and re-open Mod Organizer 2.
- Open the **Settings** (Tools > Settings or CTRL+S).
- Switch to the **Plugins** tab and select **Merged Plugins Hide** in the list.
- Double-click **hide-type** and enter **optional**.
- Click OK to save and close the window.

> This will, instead of adding the extension .mohidden to the plugins, move them to a separate directory (a folder called "Optional" located inside the mod folder.

## 4.7 Separators

* Download the **[The Phoenix Flavour - MO2 Separator Pack](https://www.nexusmods.com/skyrimspecialedition/mods/14223)** manually from the Nexus.
* Open the downloaded archive.
* Extract all folders ending on **_separator** to `Mod Organizer 2\mods`.
* Switch back to Mod Organizer 2 and press F5 to refresh. The new separators will now appear in your mod order.
* They are numbered but should be sorted in the correct order automatically:
  * *DLC: Dawnguard*
  * *DLC: HearthFires*
  * *DLC: Dragonborn*
  * **01 ESSENTIAL MODS**
  * **02 FIXES**
  * **…**

![separator](../Media/separator.png)

# 05. Skyrim Script Extender

## 5.1 Download

* Download **[SKSE64](http://skse.silverlock.org/)**. You need build ==**2.0.17**== for the current version of Skyrim SE.
* Save the downloaded archive to `Your Modding Folder\ARCHIVE\SKSE64`.

If on the main page for SKSE there is a different version number than the one noted above, Skyrim and the Script Extender were likely updated and you need to download the previous version from the archive page (see picture below).

![SKSE Download](Pictures/Setup/skse_download.png)

## 5.2 Installation

### 5.2.1 Binaries

* Extract the archive’s contents to `Your Modding Folder\temp`.
* Move the following three files into your Skyrim SE **root** folder:
  * **skse64_**skyrim version number**.dll**
  * **skse64_loader.exe**
  * **skse64_steam_loader.dll**

### 5.2.2 Scripts

* Go back to your **temp** folder with the remaining files.
* Rename the **Data** folder to **SKSE – Data 2.0.x** (where x is the current version number).
* Move the new folder to `Mod Organizer 2\mods`.
* Switch back to Mod Organizer 2.
* Press F5 to refresh and the new mod will show up at the bottom of your mod order.
* Move it up below the **01 ESSENTIAL MODS** separator and activate it.
* Delete all remaining files inside your **temp** folder.

## 5.3 SKSE INI

* Download [SKSE64 INI PRE DOWNLOAD v1.2](https://www.nexusmods.com/skyrimspecialedition/mods/1651) from the Nexus (click "Mod Manager Download").
* Back to Mod Organizer 2, switch to the **Downloads** tab.
* Double-click the mod there and click **OK** to install it.
* Move it below **SKSE64 – Data v2.0.x** in the mod order and activate it.

> This will be the only time downloading and installing a mod through MO2 is explained. You will be expected to do this on your own from now on.

## 5.4 SKSE Launcher

* Restart Mod Organizer 2.
* The SKSE Launcher executable will now be automatically added to the executables list in MO2.
* Select **SKSE** in the list and click **Run**.

> At this point (and when testing later on) you’ll benefit a lot from having this page open on a secondary monitor or alternatively your phone or tablet in order to avoid having to tab out.

## 5.5 Verify Installation

* Once you are in the Skyrim SE main menu, bring up the console by pressing the tilde key on your keyboard (above TAB, next to 1).
* Type in ``getskseversion`` and hit Enter. It should return the version number of your SKSE64 installation.
* After confirming that SKSE64 was installed correctly, type **qqq** in the console and hit Enter to quickly close the game.

![Verify SKSE64](Pictures/Setup/verify_skse64.jpg)

![separator](../Media/separator.png)

# 06. INI Files

## 6.1 Generate Fresh INI Files

The basic game settings are saved in two INI files, **Skyrim.ini** and **SkyrimPrefs.ini**, and split up (somewhat arbitrarily) between them. In order to ensure that your INIs are completely untouched and vanilla, we will regenerate them before optimising them.

### 6.1.1 Remove old files

If you had Skyrim SE installed previously, follow these steps:

* Locate your default INI files in the following directory:
  * `C:\Users\{USERNAME}\My Games\Skyrim Special Edition`
* If you have old save games you wish to keep, back up the **saves** folder now.
* Delete everything inside the **Skyrim Special Edition** folder.

### 6.1.2 Generate new INIs

Continue with regenerating the INI files from scratch:

* Open Steam and find **The Elder Scrolls V: Skyrim Special Edition** in your Game Library.
* Hit **Play** to open the regular launcher.
* A window will come up, informing you that Skyrim SE will now be configured based on your hardware.
* Click **OK** twice to confirm and hit **Exit** once it’s done.

![Regenerating INIs](Pictures/Setup/regenerating_inis.png)

## 6.2 Install BethINI

* Download the latest version of **[BethINI](https://www.nexusmods.com/skyrimspecialedition/mods/4875)** manually from the Nexus.
* Extract the downloaded archive to `Your Modding Folder\Tools\BethINI`.
* Close Mod Organizer 2.
* Double-click **BethINI.exe**.

## 6.3 BethINI Configuration

### 6.3.1 BethINI - Setup

* After starting BethINI, you will be prompted with a window asking you to choose your game.
* Select **Skyrim Special Edition** from the drop-down menu.
* Once BethINI has loaded up, go to the first tab, **Setup**.
* All filepaths should be configured correctly out of the box, however it’s best to double-check:
  * **Game Path** should point at your **root** folder, `steamapps\common\Skyrim Special Edition`.
  * **Mod Organizer** should point at your MO2 folder, `{Your File Path}\Mod Organizer 2`.
  * **INI Path** should point at your MO2 profile: ==ModOrganizer 2 > The Phoenix Flavour==.

> Changing the INI Path will prompt BethINI to restart. Click No when asked about using the skyrimcustom.ini file.

### 6.3.2 BethINI - Basic

Continue with the second tab, **Basic**.

- Set **Resolution** to the correct value for your monitor.
- Make sure to check **Recommended Tweaks**.
- **BethINI** presets should be toggled automatically.
- Select the **Medium** preset.
- Disable both **VSYNC** and **Lock Frame Rate**.

### 6.3.3 BethINI - Interface

Continue with the fifth tab, **Interface**.

- I prefer my **Lock Sensitivity** at ==**0.0450**== but this will come down to personal taste and your mouse configuration.
- **Dialogue Subtitles** and **General Subtitles** are unchecked by default, toggle them on if you need them.

> You can always turn on the subtitles in the ingame settings as well.

### 6.3.4 BethINI - Detail

Continue with the sixth tab, **Detail**.

- **Decal Quantity:** Set to `High`.
- **Godrays**: I recommend setting them to `None`, they don’t look great and eat frames for breakfast.
- **Field of View:** Increase this if you prefer a wider FoV.
- **Particles:** Set to `7500` (which is the recommended value for Complex Particle Lights, an ENB feature).
- **Lens Flare:** Matter of taste. Personally I disable this.
- **Anamorphic Lens Flare:** Looks ugly, recommended to be turned off.
- **Shadow Resolution:** Set to `2048` (unless your CPU is a slow dual core).
- **Ambient Occlusion:** Recommended to set this to `None` in favour of ENB AO.

### 6.3.5 BethINI - View Distance

Continue with the seventh tab, **View Distance**.

- **Grass Fade:** Set to `15000` or higher.

### 6.3.6 BethINI - Visuals

Continue with the eighth tab, **Visuals**.

- Set **Contrast** to `-0.1800`.

> This should eliminate the "black crush" some people are experiencing in Skyrim SE.

### 6.3.7 BethINI - Custom

Continue with the ninth tab, **Custom**.

* Select the following:
  * **Section:** General
  * **Setting:** bModManagerMenuEnabled
* Change the value to `0`.
* Click **Save**.

> This will disable the **MODS** entry in the ingame pause menu. You should not be using the in-built Bethesda mod manager or Beth.net platform at all. The Creation Club shenanigans will be hidden by mods later on.

![Disable Mod Manager Menu](Pictures/Setup/bethini_disable_mod_manager_menu.png)

## 6.4 Save Changes

- Return to the second tab, **Basic**, and click `Save and Exit`.
- Restart Mod Organizer 2.
- You might be notified about the missing skyrimcustom.ini in which case you can just click **OK**.

![separator](../Media/separator.png)

# 07. Additional Tools

## 7.1 SSEEdit

### 7.1.1 Installation

* Download **[SSEEdit ](https://www.nexusmods.com/skyrimspecialedition/mods/164/)**manually from the Nexus.
* Create a new folder: `Your Modding Folder\Tools\SSEEdit`.
* Open the downloaded archive and extract everything into the new folder.
* Open Mod Organizer 2 and go into the **Executables** settings (Tools > Executables or CTRL + E).
* Click the tiny blue plus icon to add a new executable and select **Add from file**.
* Navigate to `Your Modding Folder\Tools\SSEEdit`and double-click **SSEEdit.exe**.
* Click **Apply** to save the new executable.

![Add SSEEdit to MO2](Pictures/Setup/add_sseedit_to_mo2.png)

### 7.1.2 SSEEdit Cache Output

Every time a new plugin is loaded into SSEEdit, a refcache file will be generated for it so that the next time it won’t have to processed again – SSEEdit can simply read the cache file, significantly shortening the startup time.

In order to store the cached files with the program files themselves, we need to add an argument for it:

* Under **Arguments**, enter the following:
  * `-C:"...\Your Modding Folder\Tools\SSEEdit\cache\"`
* Replace the **"…\Your Modding Folder..."** part with the file path on your end. This is what I added:
  * `-C:"F:\Modding\Skyrim SE Mods\Tools\SSEEdit\cache\"`
* Click **Apply** to save.

> Whenever you update SSEEdit, the accumulated refache files will also be wiped (as they should be) and new ones will be generated and stored in the same directory when you next launch SSEEdit without you having to complete any additional steps. 

### 7.1.3 QuickAutoClean

* Click the tiny blue plus icon to add another new executable and select **Add from file**.
* Navigate to `Your Modding Folder\Tools\SSEEdit`and double-click **SSEEditQuickAutoClean.exe**.
* **Optional:** Change the title to something less verbose (like "SSEEdit – Quick Cleaning").
* Under **Arguments**, enter the following:
  * `-DontCache`
* Click **OK** to save and close the window.

> The **-DontCache** argument will prevent an obscure bug that destroys parts of Apocrypha during the cleaning of Dragonborn.esm.

![Add QuickAutoClean to MO2](Pictures/Setup/add_quickautoclean_to_mo2.png)

## 7.2 zEdit

### 7.2.1 Installation

* Download the latest version of [zEdit](https://github.com/z-edit/zedit/releases) from Github:
  * zEdit_v0.6.5_-_Portable_x64.7z
* Create a new folder: `Your Modding Folder\Tools\zEdit`.
* Open the downloaded archive and extract everything into the new folder.
* Switch back to Mod Organizer 2 and open the **Executables** settings (Tools > Exectuables or CTRL + E).
* Click the tiny blue plus icon to add a new executable and select **Add from file**.
* Navigate to `Your Modding Folder\Tools\zEdit` and double-click **zEdit.exe**.
* Click **OK** to close the window.

![zEdit Download](Pictures/Setup/zedit_download.png)

### 7.2.2 Configuration

* Run zEdit through Mod Organizer 2.
* Click the gears icon to open the **Profile** settings.
* Make sure **Path** (for Skyrim SE) correctly points to your Skyrim SE **root** folder.
* Close the profile settings window.

### 7.2.3 zMerge Settings

* Select **zMerge** from the drop-down menu in zEdit and hit **Start Session**.
* Click the gears icon in the top right to open the settings.
* Switch to the **Integration Settings** tab and apply these settings:
  * **Mod manager:** Mod Organizer 2
  * **MO2 instance:** portable
  * **Mod manager path:** `{Your File Path}\Mod Organizer 2`
  * **Mod manager mods path:** `{Your File Path}\Mod Organizer 2\mods`
* Switch to the **Merge Settings** tab:
  * **Merge output path:** `{Your File Path}\Mod Organizer 2\mods`
  * **Integration:** uncheck **Disable plugins** and **Disable mods**
* Once you have made sure everything is configured correctly, hit **OK** and close zEdit.

## 7.4 Cathedral Assets Optimizer (CAO)

### 7.4.1 Installation

* Download the latest version of [Cathedral Assets Optimizer](https://www.nexusmods.com/skyrimspecialedition/mods/23316) manually from the Nexus.
* Create a new folder: `Your Modding Folder\Tools\Cathedral Assets Optimizer`.
* Open the downloaded archive and extract everything into the new folder.

> You will be using CAO plenty of times during the installation of the guide, so I recommend adding it to your Windows Taskbar for quick access.

### 7.4.2 Profiles

With the latest versions of CAO, you can set up dedicated profiles to switch between the two primary uses of CAO at will. I created several profiles for different purposes to be used during the installation of  the guide.

* Download [The Phoenix Flavour - CAO Profiles Pack](https://www.nexusmods.com/skyrimspecialedition/mods/14223) from the guide’s Nexus page.
* Open the downloaded archive.
* Extract all folders to `Your Modding Folder\Tools\Cathedral Assets Optimizer\profiles`.

## 7.5 SSE NIF Optimizer

While the vast majority of SLE meshes can be fixed with Cathedral Assets Optimizer, there are some that will only work properly after running them through the original SSE NIF Optimizer.

### 7.5.1 Installation

* Download [SSE NIF Optimizer](https://www.nexusmods.com/skyrimspecialedition/mods/4089) manually from the Nexus.
* Extract the executable into Your Modding Folder. It’s just a single file so no separate directory is required.

## 7.6 Modwatch

* Download [Modwat.ch](https://www.nexusmods.com/skyrim/mods/56640) manually from the Nexus.
* Create a new folder: `Your Modding Folder\Tools\Modwat.ch`.
* Open the downloaded archive and double-click the "Modwatch-win32-ia32" folder within.
* Extract everything into the new folder.

![separator](../Media/separator.png)

# 08. ESM Cleaning

## 8.1 About ESM Cleaning

With the release of SSEEdit 4.0, the process of cleaning plugins has been simplified quite a bit. Beginning with **Update.esm**, we are going to clean the following four ESMs, Bethesda’s official master files, **one at a time**.

* **Update.esm**
* **Dawnguard.esm**
* **HearthFires.esm**
* **Dragonborn.esm**

> Do **not** attempt to process Skyrim.esm this way.

## 8.2 Export Files to MO2

Since we want to keep the vanilla files wholly untouched, we are going to copy over the four ESMs that we will clean into a MO2 mod folder. They will then overwrite the original ESMs from your **Data** folder (which are displayed at the top of your load order).

This method has the added benefit of keeping the vanilla files available as backup. Should something go wrong during the cleaning process (which is unlikely), you will be able to wipe the MO2 mod folder and copy the vanilla files again to start over.

- Open the `Mod Organizer 2\mods` folder and create a new folder inside called **Official Master Files – Cleaned**.
- Navigate to your **Data** folder and copy the following files:
  - **Update.esm**
  - **Dawnguard.esm**
  - **HearthFires.esm**
  - **Dragonborn.esm**
- Paste them into your new **Official Master Files – Cleaned** folder.
- In Mod Organizer 2, press F5 to refresh and your new "mod" will appear at the bottom of the mod order.
- Drag it up above **SKSE – Data 2.0.x** in your mod order and activate it.

## 8.3 Automated Cleaning Process

### 8.3.1 Update.esm

* Select **SSEEdit – Quick Cleaning** in the executables list and hit **Run**.
* The plugin selection window will come up next.
* Check only **Update.esm** and click OK.

Now the cleaning process will begin automatically. It takes a few minutes, so simply sit back and let SSEEdit do its thing until you see `Quick Clean mode finished` in the log. Then you can close SSEEdit.

### 8.3.2 Dawnguard.esm

* Run **SSEEdit – Quick Cleaning** through MO2.
* Check only **Dawnguard.esm** in the plugin selection window and click **OK**.
* Wait until the cleaning procedure is completed.
* Close SSEEdit.

### 8.3.3 HearthFires.esm

* Run **SSEEdit – Quick Cleaning** through MO2.
* Check only **HearthFires.esm** in the plugin selection window and click **OK**.
* Wait until the cleaning procedure is completed.
* Close SSEEdit.

### 8.3.4 Dragonborn.esm

* Run **SSEEdit – Quick Cleaning** through MO2.
* Check only **Dragonborn.esm** in the plugin selection window and click **OK**.
* Wait until the cleaning procedure is completed.
* Close SSEEdit.

## 8.4 Manual Cleaning - Update ESM

### 8.4.1 Source

With 1.5.97, Bethesda changed the navmeshes in Solitude for their latest "creation", Saints & Seducers ([source](https://www.reddit.com/r/skyrimmods/comments/dzvg03/teardown_of_the_1597_update/?utm_source=share&utm_medium=web2x)). Some mods however still rely on the old navmesh and they will crash if it's missing (namely Interesting NPCs). Therefore we will revert the deletion of the old navmesh.

Instructions are copied with permission from Lexy's LOTD.

### 8.4.2 Instructions

- Run SSEEdit through Mod Organizer 2 (==do **not** use the Quick Cleaning version==).
- In the plugin selection window, right-click and **Select None**.
- Check only **Update.esm** and hit **OK**.
- Once SSEEedit returns the message `Background Loader: finished`, you may proceed.
- Double-click **Update.esm** and navigate to the following section:
  - `Worldspace \ 0000003C Tamriel \ Block 1, -1 \ Sub-Block 5, -4 \ 0000BDC9 \ Temporary`
- Double-click **Temporary** and delete the following record:
  - `00106EAA Navigation Mesh`
- Close SSEEdit.
- When asked to save your changes, only **Update.esm** should appear in the list.
- Make sure **Update.esm** is checked, then click **OK**.
- You’re done!

## 8.5 Manual Cleaning - Dawnguard ESM

### 8.5.1 Source

There are [additional instructions written up by alt3rn1ty](https://forums.nexusmods.com/index.php?/topic/5381485-guide-manual-cleaning-skyrim-and-skyrim-special-edition-master-files/) to manually clean some dirty edits that won’t be caught by SSEEdit’s quick cleaning procedure. Only one of the edits can affect actual gameplay though, so we won’t bother with removing the other two which are simply left-over test records.

### 8.5.2 Apply Filter

* Run **SSEEdit** through Mod Organizer 2 (==do not use the Quick Cleaning version==).
* In the plugin selection window, right-click and **Select None**.
* Check only **Dawnguard.esm** and hit **OK**.
* Once SSEEedit returns the message `Background Loader: finished`, you may proceed.
* Right-click anywhere in the left pane and select **Apply** **Filter**.
* Change nothing in the window that comes up next, but simply click **Filter** to confirm.
* This will take a moment and you need to wait until it is done.

### 8.5.3 Delete conflicting sub-record

* Proceed once SSEEdit returns `Done: Applying Filter`.
* Double-click **Dawnguard.esm** (now displayed in orange), then double-click **Cell**.
* Find the following cell (highlighted in red) in the list and select it:
  * ==00016BCF RiftenRaggedFlagon==
* Scroll down in the right pane to the bottom until you can see the conflict in the line marked red.
* Right-click `RiftenRatwayZone [ECZN:0009FBB9]` in **Dawnguard.esm** and select **Remove** (see picture below).
* There will be a warning, simply click **Yes I’m absolutely sure**.

![ESM Cleaning - Manual Edit](Pictures/Setup/esm_cleaning_manual_edit.png)

### 8.5.4 Save Changes

* Close SSEEdit.
* When asked to save your changes, only **Dawnguard.esm** should appear in the list.
* Make sure **Dawnguard.esm** is checked, then click **OK**.
* You’re done!

![separator](../Media/separator.png)

# 09. Skyrim Realistic Overhaul

## 9.1 Download

Skyrim Realistic Overhaul is the most comprehensive texture overhaul out there, over 10GB in size and covering nearly every single texture in the game. We will use it as a base retexture for our setup.

Unfortunately SRO is not on the Nexus and we will have to download it from ModDB. Because the files are so large, the download may take a while (depending on your internet connection) and it may be advisable to let them load overnight.

Otherwise you can also continue with the Mod Installation section for now as the installation of SRO can be completed anytime.

* Open the [Skyrim Realistic Overhaul](https://www.moddb.com/mods/skyrim-realistic-overhaul/downloads) page on ModDB and download the following files:
  * `Skyrim Realistic Overhaul Part 1`
  * `Skyrim Realistic Overhaul Part 2`
  * `Skyrim Realistic Overhaul Part 3`
  * `Skyrim Realistic Overhaul 1.8 Update`

**Do not download the file for Original Skyrim (SLE).**

> It is  technically not necessary to download the **Update** file as it will be overwritten completely with the full TPF installation. I have included it anyway for the sake of completeness as well as for people skipping many of the other retextures.

## 9.2 File Extraction

* Create a new folder inside `Your Modding Folder\temp` and name it **Skyrim Realistic Overhaul**.
* Extract the **textures** folders from all downloaded SRO archives into the new **Skyrim Realistic Overhaul** folder in this order:
  * Part 1
  * Part 2
  * Part 3
  * Update
* This will take a while. **Make sure to merge and overwrite when asked.**
* Eventually you will have a single **textures** folder with the size of a solid **10.2GB**.

![SRO Textures Folder](Pictures/Setup/sro_textures_folder.png)

## 9.3 Processing with CAO

In order to be able to control the mod order of SRO and ensure it can be overwritten by other retexture mods, we will also pack the textures in BSAs (archives) and load the matching plugins high up in the load order. All packed up, the entirety of SRO will be reduced to 8.32GB this way.

**If you have 3GB of VRAM or less:** Use the **SSE – Skyrim Realistic Overhaul (Performance)** profile. In addition to repacking the textures, CAO will also half their resolution (all 4k textures to 2k, all 2k textures to 1k) which will help save VRAM. Note that this will take more time and result in less plugins and archives.

- Run **Cathedral Assets Optimizer** (do not open it through Mod Organizer 2.)
- From the **Profiles** drop-down menu, select one of the **SSE – Skyrim Realistic Overhaul** profiles (Quality / Performance).
- Click **Open Directory** and point it at the `Your Modding Folder\temp\Skyrim Realistic Overhaul` folder.
- Click **Run** to start the process. Click **Yes to All** if asked to save changes.
- This will take a while! You can monitor the progress in the **Logs** tab.
- Wait until the CAO log returns: `[INFO] Process completed`.

![Process SRO in CAO](Pictures/Setup/process_sro_in_cao.png)

## 9.4 Installation

* Navigate to `Your Modding Folder\temp\Skyrim Realistic Overhaul` which now contains several ESPs and BSAs:
  * **Quality:** 6 ESPs+BSAs, 8.33GB in total
  * **Performance:** 2 ESPs+BSAs, 2.29GB in total
* Move the **Skyrim Realistic Overhaul** folder containing the packed files to `Mod Organizer 2\mods`.
* Back in Mod Organizer 2, press F5 to refresh.
* **Skyrim Realistic Overhaul** should now appear at the bottom of your mod order.
* Drag it up all the way below the **MAIN VISUAL MODS** separator and activate it.

![separator](../Media/separator.png)

# 10. Mod Installation Instructions

## 10.1 Overview

### 10.1.1 Guideline

After completing the Setup, you are equipped with a correctly installed and configured instance of Mod Organizer 2 that is set up for the Skyrim Script Extender. It is now time to dive into the by far longest section in the guide - the mod installation.

- The mods themselves are split up into forty categories which correspond to the separators of the same names installed for MO2 in the Setup. **Each set of mods must be installed in the order they are listed in** and grouped below their respective separator.
- Instructions for which file(s) to download as well as any further steps are listed below the mod name. These detailed instructions are **mandatory** and must be followed.
- All listed mods are **required** and must be installed unless they are clearly flagged as **(optional)** in which case you may skip them. Whether or not a mod is optional is typically determined by interactions with other mods (patches and dependencies).
- Occasionally a mod will have further steps noted under **Additional Instructions** or **Porting Instructions** such as “Resave Example.esp in the Creation Kit”. You can find detailed instructions further down on this page.
- It may be faster to download all mods of one page first, then install them and finally go through all additional instructions.

**Do not attempt to launch Skyrim SE before you are instructed to**. During the installation you will have missing dependencies and unresolved conflicts fixed later by additional mods.

### 10.1.2 Mod Installation

You can find all mod installation instructions in the [02_Mod_Installation.md](/The-Phoenix-Flavour-3-2/02-Mod-Installation.md). I highly recommend opening it in a new tab or window while keeping the current document so that you are able to refer to the instructions detailed below while installing the mods.

## 10.2 General Instructions

### 10.2.1 Downloading Mods

* Almost all mods are hosted on the Nexus.
* CTRL-clicking a mod’s name will take you immediately to its Nexus page.
* The files listed under **Download Instructions** are marked with the respective section you can find them in on the Nexus:
  * Main Files
  * Update Files
  * Optional Files
  * Miscellaneous Files
  * Old Files
* In the **Files** section on the mod page, download the file(s) by clicking "Mod Manager Download".
  * When a mod has special requirements, they are then listed in a pop-up window where you will have to click the **Download** button again.
  * Don’t worry about these requirements, they are included in the guide or otherwise taken care of.

### 10.2.2 Installing Mods

* After downloading a mod, switch to the **Downloads** tab in the right pane of Mod Organizer 2 and double-click the file(s) to install.
* This may open a FOMOD installer if the mod includes one. In this case you need to follow the **FOMOD Instructions** listed in the guide.
* After installing a mod you may want to rename it in order to reflect the version you downloaded or options you selected in the FOMOD:
  * For retextures it is useful to add the texture resolution: **Embers HD 2k**.
  * If there are different versions, note down which one you downloaded: **Less Ugly Tundragrass - Redder Variant**.
* When installing more than one file from the same mod page, always click **Rename** when prompted and give the file a unique name to install it separately. **Do not select Merge or Replace**.

### 10.2.3 FOMOD Instructions

Some mods come with a FOMOD Installer in which case instructions are provided. Occasionally the choices do not have to be strictly followed (particularly when they are related to texture resolution or variations) however there are some FOMODs that you have to install exactly as indicated in the instructions. Please do follow the provided instructions.

### 10.2.4 Deleting Files

* When instructed to delete one or several files, double-click the mod in your mod order.
* Switch to the **Filetree** tab and find the files you need to remove.
* Simply right-click them and select **Remove** (or select them and hit DELETE on your keyboard).

### 10.2.5 Manual Editing Instructions

Very rarely you will be instructed to edit a plugin directly in SSEEdit. If you never touched this program before, it may be somewhat  confusing at first. The edits you will be asked to make are quite simple and straight-forward however. Mods with such instructions are always optional and may be skipped.

## 10.3 Special Instructions

### 10.3.1 Convert Plugin

> "Resave Example.esp in the Creation Kit."

Plugins with Form Version 43 (typically downloaded from the Classic Skyrim Nexus) must be re-saved in the CK.

* Run the **Creation Kit** through Mod Organizer 2.
* Once it is loaded up, go to **File > Data**.
* Select the plugin you need to convert in the list and click **Set as Active File**.
* Click **OK** and wait for the Creation Kit to load up the plugin.
* Go to **File > Save**. There will be a small confirmation message (**Saving… done!**) at the bottom of the window.
* Close the Creation Kit.
* Afterwards, you can right-click the mod in MO2 and select **Mark converted/working**.

### 10.3.2 Clean Plugin

> "Clean Example.esp with SSEEdit."

Very rarely a plugin may contain “dirty edits” or deleted records in  which case you need to run it through the QuickAutoClean version of  SSEEdit (just like we did with the official master files).

* Run **SSEEdit - QuickAutoClean** through Mod Organizer 2.
* Check only the plugin you were instructed to clean in the plugin list.
* Click **OK** and wait for the process to complete (`Quick Clean mode finished`).
* Close SSEEdit.

### 10.3.3 Extract BSA

> "Unpack Example.bsa through Mod Organizer 2.

Occasionally you will be instructed to unpack an archive, either because it was packed with the 32bit CK, or because we need the files  loose to overwrite or selectively delete.

* Switch to the **Archives** tab in the right pane of Mod Organizer 2.
* Find the archive you need to unpack and right-click it (it will only show up if the mod is checked in the mod and load order).
* Navigate to `Mod Organizer 2\mods`, click on the mod folder the archive belongs to and click **Select Folder**.
* After unpacking the files, press F5 to refresh Mod Organizer 2.
* Double-click the mod the archive is part of in your mod order.
* Switch to the **Filetree** tab and right-click > delete the BSA.

Deleting the BSA after extracting it is extremely important. Your game may crash on launch otherwise.

### 10.3.4 Optimise SLE Assets

> "Run the mod through Cathedral Assets Optimiser."

Skyrim LE meshes often need to be fixed and optimised by Cathedral Assets Optimizer before they can be used in SE. We will also use CAO on mods to optimise (compress) included textures sometimes. If a Classic Skyrim mod does not have instructions to run it through CAO this is because I already did so and found that no meshes or textures needed optimising.

* Run **Cathedral Assets Optimizer** (do not launch it through Mod Organizer 2).
* Select the **SSE - Optimise SLE Assets** profile from the drop-down menu.
* Click **Open Directory** and navigate to `Mod Organizer 2\mods`.
* Click on the folder of the mod you wish to optimise and hit **Select Folder**.
* Back in CAO, click **Run** and wait for the process to complete.
* Afterwards, you can right-click the mod in MO2 and select **Mark converted/working**.

### 10.3.5 Fix Meshes

> “Run the mod through SSE NIF Optimizer.”

Very few mods in the guide need to be run through SSE NIF Optimizer instead of Cathedral Assets Optimizer to fix their meshes.

* Double-click **SSE NIF Optimizer.exe** which should be located inside Your Modding Folder.
* Click **Browse** and navigate to `Mod Organizer 2\mods`.
* Click on the folder of the mod you wish to optimise and hit **Select Folder**.
* Click **Optimise** and wait until the process is finished.
* Close **SSE NIF Optimizer**.

### 10.3.6 Resize Textures

>"Downsize the textures with Cathedral Assets Optimizer."

At times (re)textures are only available in a size unreasonably large for regular gameplay, potentially impacting performance for those with low VRAM. In those cases we will utilise CAO to reduce the texture resolution by half.

* Run **Cathedral Assets Optimizer**.
* Select the **SSE - Downsize Textures** profile from the drop-down menu.
* Click **Open Directory** and navigate to `Mod Organizer 2\mods`.
* Click on the mod containing the textures and **Select folder**.
* Back in CAO, click **Run** and wait for the process to be completed.