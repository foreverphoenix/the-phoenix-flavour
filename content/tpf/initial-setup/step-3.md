---
title: "Step 3: Mod Organizer 2"
weight: 3
type: docs
description: >
  Setting up and configuring Mod Organizer 2.
---

## MO2 Setup

Mod Organizer 2 is the king of mod managing software for Bethesda games and TPF heavily relies on its features. Any claims of MO2 being especially difficult to use are complete myths perpetuated by inexperienced users. At the end of the TPF setup, you will be able to confidently handling a large mod setup with MO2.

- Download the latest version of [Mod Organizer 2](https://www.nexusmods.com/skyrimspecialedition/mods/6194?tab=files) from the Nexus page (main file).
- Run the executable to begin the installation.
- Choose **I accept the agreement** and proceed to the next step.

You will be asked where you want to install Mod Organizer 2. The directory is important.

- Mod Organizer must be installed **outside any UAC-protected folders**, like `C:\Program Files`, etc. Ideally you should create a new top level folder like `G:\Mod Organizer 2\` or similar.
- Choose a hard drive with **100GB or more of free space**. The MO2 setup itself will grow well beyond 50GB of mods plus 13GB for the Stock Game folder. The hard drive should ideally be an **SSD** to prevent long loading screens and potential stutter ingame.

Create a suitable installation directory and select it through the MO2 installer.

From now on, simply click **Next** without choosing anything until the installer is done. Once the installation is complete, click **Finish** and MO2 will launch automatically.

### Instance Configuration

Mod Organizer 2 can be installed as a portable instance which we will do. It means that the tool will be entirely self-contained with all related files being saved within its installation directory. This allows you to run as many installation of MO2 / as many modded setups as you want without having them interfere with each other.

- Click **Next** in the Instance configuration and then choose **Create a portable instance**.
- As the game, obviously choose **Skryim Special Edition** which should have been detected automatically.
- Afterwards, click **Next** and **Finish** to complete the configuration.

![MO2 New Instance](/Pictures/tpf/initial-setup/mo2-new-instance.png)

## MO2 Settings

Open the **Settings** menu in Mod Organizer 2 (Tools >> Settings or CTRL + S).

### General

In the **General** tab, under **Download List**, check the boxes for **Show Meta Information** and **Compact List**.

### Paths

In the **Paths** tab, change the **Downloads** directory to `\Your Modding Folder\ARCHIVE\MO2 Downloads\`.

This means that the downloaded mod archives (not the mods themselves which will be extracted when they are installed) will be stored outside of your MO2 folder. They are not needed for actual gameplay so it makes sense to archive them on a different hard drive. SSDs don't grow on trees after all.

### Workarounds

In the **Workarounds** tab, check **Enable archives parsing (experimental)** to allow preview of BSA-packed files. This is incredibly useful even if it is not always completely reliable.

### Plugins

In the **Plugins** tab, scroll down to the **Plugin** section and select the **BSA** Extractor. Double-click **only_alternate_source** and set it to **true**.

This will disable the automatic prompt to unpack BSAs upon installing a mod that contains BSAs *except* for when that mod is from a different source (Skyrim instead of Skyrim Special Edition in this case). Since SLE BSAs must *always* be unpacked that makes sense.

For all other mods with BSAs, we unpack them too rarely to justify having an extra click for each of them. Occasionally the guide will instruct you to unpack a BSA manually after installing the mod.

### Nexus

Almost all mods in TPF are hosted on the [Nexus](https://www.nexusmods.com/). Connecting your Nexus account to MO2 will allow you to quickly download mods through MO2's interface, saving you a lot of time.

In the **Nexus tab**, click **Connect to Nexus**. This should open a browser window where you will be asked to confirm. Click **Authorise** (you can revoke this any time in your Nexus settings).

After closing the **Settings** window, Mod Organizer 2 may ask you to restart. Click **OK**.

![Authorise MO2](/Pictures/tpf/initial-setup/authorise-mo2.png)

## MO2 Interface

You can now configure the UI to your liking. Personally I re-arrange the two panels so that the left one (mod order) is wider and takes up about 75% of space.

- Right-click the **Tool Bar** (coloured icons in the top left).
- Now you may choose which parts of the UI to display. I recommend disabling the **Log** as you will not need it.
- For the main **Tool Bar** you can decide between Icons or Text (or both), and, if you choose Icons, their size. This is up to you.

### Dark Mode

If it’s the middle of the night and you prefer dark mode to go easy on your eyes, open the **Settings** (CTRL + S) and choose a different theme under **Styles**. If I liked dark mode, I'd recommend **1809 Dark Mode**.

All my TPF screenshots will be in light mode. Please direct your complaints to your nearest house plant.

### Mod Order

By right-clicking the top of the left pane, you can choose what to display in your mod order. Enable the following columns:

- **Conflicts**
- **Flags**
- **Content**
- **Version**
- **Source Game**
- **Priority**

![MO2 Customised](/Pictures/tpf/initial-setup/mo2-customised.png)

## MO2 Profile

For TPF we will be creating a custom profile:

- Open the **Profile** settings in MO2 (Tools >> Profiles or CTRL+P).
- The **Default** profile will be selected automatically.
- Click **Create** to set up a new profile and enter **The Phoenix Flavour** as the name.
- Make sure both options at the bottom (profile-specific saves and INIs) are **checked**.
- Click **Select** to close the window and switch to your new profile.

> Using profile specific INIs and saves means that these files will not be stored / edited in the default folder, but within MO2. The saves and config files in your Documents folder will be untouched by TPF.

![MO2 Select New Profile](/Pictures/tpf/initial-setup/mo2-tpf-profile.png)

## MO2 Separators

Mod Organizer 2 offers a separator feature which greatly helps with organising your mod order in the left pane. In the past, the separators were provided by me but I have since been persuaded that users benefit more from learning how to create their own.

- In Mod Organizer 2, click the **Tools** icon above the mod order (see screenshot).
- Select **Create Separator** and enter **UTILITIES** as the name.
- Click **OK** and the new separator will appear at the bottom of your mod order.
- Select your new separator and move it per drag-and-drop above the three DLC.

![MO2 Create Separator](/Pictures/tpf/initial-setup/mo2-create-separator.png)

### Colour Customisation

You can change the colour of your separators at any time. A new separator will always have the colour of the one you created previously. You can also have different colours for different sections. Once you have multiple separators, it is also possible to Shift-Click or Control-Click to select any or all of them, and change the colour for all at once.

To change the colour of your first separator:

- Right-click your **UTILITIES** separator and click **Select color**.
- Change the colour to whatever you want and click **OK**.

---

If you are interested, you can find my personal TPF separator colour palette [here](https://coolors.co/f3f3e2-f1fcd7-edfbc1-ddf8c3-caf0c5-b7e7c6-a8e1df-88c7db-90b8e0-cfe0f2) or check [this preview](/Pictures/tpf/initial-setup/tpf-separator-colours.png) (link opens full size picture).

My colour scheme was made for the default (light) MO2 theme and will likely be too bright for dark mode.

The hex codes are here:

- **#CFE0F2** - version number
- **#90B8E0** - essential / baseline mods
- **#88C7DB** - visual mods in general
- **#A8E1DF** - retextures and mesh replacers
- **#B7E7C6** - gameplay mods
- **#CAF0C5** - major (content) mods
- **#DDF8C3** - overhauled / new locations
- **#EDFBC1** - mods that add content
- **#F1FCD7** - Creation Club and related mods
- **#F3F3E2** - patches and patcher outputs

## MO2 Splash Screen

Now comes the final touch: When you open MO2, you can see the default splash screen (the MO2 name and logo) before the app fully launches. Now ask yourself this: Can we really call ourselves modders if we don't mod this, too?

- Close Mod Organizer 2.
- Download [Mod Organizer 2 Splash Screen - Intro Title Style](https://www.nexusmods.com/skyrimspecialedition/mods/51391?tab=files) manually from the Nexus.
- Open the download archive and double-click the **Splash - TPF** folder inside.
- Drop the **splash.png** into your Mod Organizer 2 installation folder (the one containing ModOrganizer.exe).
- Re-open Mod Organizer 2 to see your cool new splash screen (and to continue with the guide).

> Thanks a ton to **sneaky-witch-thief** who created the splash screens and added a TPF-themed one specifically for us! <i class="fas fa-heart"></i>

---

#### Continue with the [Stock Game Folder](/tpf/initial-setup/step-4/) page.