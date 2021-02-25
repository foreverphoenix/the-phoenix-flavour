---
title: "Mod Organizer 2"
weight: 4
type: docs
description: >
  Setting up and configuring Mod Organizer 2.
---

## Installation

Installing MO2 with a portable instance means all of its subdirectories will be located inside the MO2 root folder which is required for some modding tools to work properly.

* Download [Mod Organizer 2](https://www.nexusmods.com/skyrimspecialedition/mods/6194) (the **Archive** version of **2.3.2** under **Old Files**) manually from the Nexus.
* Extract the archive to a new folder on the same hard drive as your Skyrim SE installation, outside the UAC protected folders.
* Run **ModOrganizer.exe**.
* A window will come up - select **Portable** (see picture below).
* Next you will be asked which game to set MO2 up for. Normally it should recognise your Skyrim SE installation automatically.
* Select **Skyrim Special Edition** in the list.
* Confirm when asked to associate NXM links with MO2.
* Click **No** when prompted with the tutorial option.

![MO2 Choose Instance](/Pictures/skyrim-se/initial-setup/mo2-choose-instance.png)

## Configuration

In the mod order (left pane), arrange the DLC as follows:

- **DLC: Dawnguard**
- **DLC: HearthFires**
- **DLC: Dragonborn**

> This is, admittedly, not actually necessary. It just bothers me to no end that they are in the wrong order and this is the order you will see them in in my screenshots.

### Tweaks

* Open the **Settings** (Tools >> Settings or CTRL + S).
* In the **General** tab, check both boxes under **Download List**:
  * Show Meta Information
  * Compact List
* Switch to the **Workarounds** tab and check the following option:
  * Enable parsing of Archives (Experimental Feature)

### Nexus Integration

* Switch to the **Nexus** tab where you need to connect your Nexus account to Mod Organizer 2.
* Click **Connect to Nexus**.
* This will open a Browser window where you will be asked to confirm.
* Click **Authorise**. You can revoke this any time in your Nexus settings.
* Close the **Settings** window.
* Mod Organizer 2 may ask you to restart. Click **OK**.

![Authorise MO2](/Pictures/skyrim-se/initial-setup/authorise-mo2.png)

## Manage Mod Downloads

Most people use the "With Mod Manager" download option on the Nexus and then install the mod through their mod manager’s UI. That is the fastest and simplest way to download and install mods.

Since we installed MO2 as a portable application, all our mod archives would normally be downloaded into a sub-directory of the (MO2) root folder – which in turn may be located on your SSD or otherwise fastest hard drive. These archives are then extracted into their own folders meaning after their installation they only use up space.

On the other hand, keeping the archives as backups is highly recommended as mods are occasionally taken down from the Nexus or in case something goes wrong during the installation.

Here is where our **ARCHIVE** comes into play, the directory inside **Your Modding Folder** we set up to store all the mod files on a hard drive with plenty of free space. We will now configure Mod Organizer 2 to save all downloads to that folder.

* Once again, open the **Settings** in MO2 (Tools >> Settings or CTRL + S).
* Switch to the **Paths** tab.
* Point **Downloads** to `Your Modding Folder\ARCHIVE\MO2 Downloads`.

![MO2 Archive](/Pictures/skyrim-se/initial-setup/mo2-archive.png)

## User Interface

You can now configure the UI to your liking. Personally I re-arrange the two panels so that the left one (mod order) is wider.

* Right-click the **Tool Bar** (coloured icons in the top left).
* Now you may choose which parts of the UI to display. I recommend disabling **Log** and **Status Bar** as you won’t need either.
* For the main **Tool Bar** you can decide between Icons or Text (or both), and, if you choose Icons, their size. This is up to you.

### Dark Mode

If it’s the middle of the night and you prefer dark mode to go easy on your eyes, open the **Settings** (CTRL + S) and choose a different theme under **Styles**. Paper Black Mono or Paper Dark are the obvious choices but there are more options.

### Mod Order

By right-clicking the top of the left pane, you can choose what to display in your mod order. Enable the following columns:

* **Conflicts**
* **Flags**
* **Content**
* **Version**
* **Source Game**
* **Priority**

![MO2 Customized](/Pictures/skyrim-se/initial-setup/mo2-customised.png)

## Custom Profiles

### Vanilla

* Open the **Profile** settings in MO2 (Tools >> Profiles or CTRL+P).
* The **Default** profile will be selected automatically.
* Uncheck the following option at the bottom:
  * `Use profile-specific Game INI Files`
* When asked to delete the existing profile-specific INI files, click **Yes**.

> This profile is completely untouched. It uses the global INI and save files from the INI folder, and running Skyrim SE through it will be exactly like running it from Steam. 

### Modded

* Click **Copy** to set up a second profile based on the **Default** one.
* Enter **The Phoenix Flavour** as the name.
* Select your new profile in the list.
* Check both options at the bottom:
  * `Use profile-specific Save Games`
  * `Use profile-specific Game INI Files`
* Click **Close** to exit the settings.
* In the profile list below the top left menu in MO2, select your new profile to switch to it.

> This new profile is separate from your vanilla install. It uses its own directories for INI and save files.

![MO2 Select New Profile](/Pictures/skyrim-se/initial-setup/mo2-select-new-profile.png)

## Separators

Mod Organizer 2 offers a separator feature which greatly helps with organising your mod order in the left pane. In the past, the separators were provided to me but I have since been persuaded that  users benefit from learning how to create their own.

- In Mod Organizer 2, click the **Tools** icon above the mod order (see screenshot).
- Select **Create Separator** and enter **"OFFICIAL MASTER FILES** as the name.
- Click **OK** and the new separator will appear at the bottom of your mod order.
- Select your new separator and move it per drag-and-drop above the three DLC.

![MO2 Create Separator](/Pictures/skyrim-se/initial-setup/mo2-create-separator.png)

### Colour Customisation

You can change the colour of your separators at any time. A new separator will always have the colour of the one you created previously. You can also have different colours for different sections. Once you have multiple separators, it is also possible to Shift-Click or Control-Click to select any or all of them, and change the colour for all at once.

To change the colour of your first separator:

- Right-click your **OFFICIAL MASTER FILES** separator and click **Select color**.
- Change the colour to whatever you want and click **OK**.

### Essential Mods

While we're at it, we should create another separator which we'll need in the next step.

- Once again, click the **Tools** icon above the mod order.
- Select **Create Separator** and enter **"ESSENTIAL MODS"** as the name.
- Click **OK** and your new separator will appear at the bottom of your mod order where you should leave it for now.

---

#### Continue with the [Skyrim Script Extender](/skyrim-se/initial-setup/skyrim-script-extender/) page.