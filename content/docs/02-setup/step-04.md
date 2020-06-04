---
title: "Mod Organizer 2"
weight: 4
type: docs
description: >
  Setting up and configuring Mod Organizer 2.
---

## 4.1 Installation

Installing MO2 with a portable instance means all of its subdirectories will be located inside the MO2 root folder which is required for some modding tools to work properly.

* Download [Mod Organizer 2](https://www.nexusmods.com/skyrimspecialedition/mods/6194) (the **Archive** version) manually from the Nexus.
* Extract the archive to a new folder on the same hard drive as your Skyrim SE installation, outside the UAC protected folders.
* Run **ModOrganizer.exe**.
* A window will come up – select **Portable** (see picture below).
* Next you will be asked which game to set MO2 up for. Normally it should recognise your Skyrim SE installation automatically.
* Select **Skyrim Special Edition** in the list.
* Confirm when asked to associate NXM links with MO2.
* Click **No** when prompted with the tutorial option.

![MO2 Choose Instance](/Pictures/setup/mo2_choose_instance.png)

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

![Authorise MO2](/Pictures/setup/authorise_mo2.png)

## 4.3 Manage Mod Downloads

Most people use the "With Mod Manager" download option on the Nexus and then install the mod through their mod manager’s UI. That is the fastest and simplest way to download and install mods.

Since we installed MO2 as a portable application, all our mod archives would normally be downloaded into a sub-directory of the (MO2) root folder – which in turn may be located on your SSD or otherwise fastest hard drive. These archives are then extracted into their own folders meaning after their installation they only use up space.

On the other hand, keeping the archives as backups is highly recommended as mods are occasionally taken down from the Nexus or in case something goes wrong during the installation.

Here is where our **ARCHIVE** comes into play, the directory inside **Your Modding Folder** we set up to store all the mod files on a hard drive with plenty of free space. We will now configure Mod Organizer 2 to save all downloads to that folder.

* Once again, open the **Settings** in MO2 (Tools > Settings or CTRL + S).
* Switch to the **Paths** tab.
* Point **Downloads** to `Your Modding Folder\ARCHIVE\MO2 Downloads`.

![MO2 Archive](/Pictures/setup/mo2_archive.png)

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

![MO2 Customized](/Pictures/setup/mo2_customised.png)

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

![Install Deorders Plugins](/Pictures/setup/install_deorders_plugins.png)

### 4.6.2 Configuration

- Close and re-open Mod Organizer 2.
- Open the **Settings** (Tools > Settings or CTRL+S).
- Switch to the **Plugins** tab and select **Merged Plugins Hide** in the list.
- Double-click **hide-type** and enter **optional**.
- Click OK to save and close the window.

> This will, instead of adding the extension .mohidden to the plugins, move them to a separate directory (a folder called "Optional" located inside the mod folder.

## 4.7 Separators

* Download the [The Phoenix Flavour - MO2 Separator Pack](https://www.nexusmods.com/skyrimspecialedition/mods/14223) manually from the Nexus.
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