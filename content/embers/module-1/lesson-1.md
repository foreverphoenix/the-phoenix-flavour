---
title: "Lesson 1: Setup"
weight: 1
type: docs
no-list: false
description: >
 Setting up Skyrim and Mod Organizer 2.
---

## Overview

**Welcome to Lesson 1.**

- About modding Skyrim in general.
- The core differences between the available versions of Skyrim.
- Ensuring that you have a 100% vanilla installation of the game ready to go.
- First look at the Nexus where the vast majority of all Skyrim mods are hosted.
- Installation and configuration of Mod Organizer 2, a mod manager.

## About Modding

When we think of modding, Minecraft is often one of the first games that come to mind. Its modding scene is enormous. Installing mods is as simple as installing a mod loader such as Forge and dropping .jar files into a specific folder - plug and play. Interactions between mods are relatively rare and you don't necessarily have to know a whole lot about Java and how Minecraft mods work in order to run a relatively heavily modded setup. Many other moddable games are similarly easy to modify.

Bethesda games are different in this regard.

At first glance installing mods for Skyrim is not so tough either: For the original Skyrim (2011), you could download files from the Steam workshop while for Skyrim Special Edition (2016) there is the ingame mods menu connected to the Beth.net website. You click the download button and go play - it seems rather straightforward. Unfortunately the way modding is presented on the Steam workshop as well as on Bethesda's website with its ostensible simplicity is highly misleading.

The Creation Engine that Skyrim was built in opens up almost unlimited modding capabilities. There are very few games that can boast as many unique mods, from small tweaks to total conversions, as Skyrim, all thanks to that engine. **However, with opportunity comes complexity.** Unlike Minecraft mods, Skyrim mods are not always self-contained: They interact and conflict with the vanilla game files as well as with each other. This means installing a large amount of mods in Skyrim requires an unusual degree of awareness and in-depth knowledge.

In the [**Introduction**](/embers/introduction/) we already spoke about expectations. Deciding to follow Embers means taking the long road and that you will probably not have a playable setup within the next few days - but in my honest opinion it is more than worth it. **Modding Skyrim can be incredibly rewarding**. What is it like to build that dream setup? Assemble your own collection, with hand-picked mods, customised through various tweaks, truly making it your own? There is a reason most of us veteran modders barely play the game anymore - we are too busy modding it.

It is this excitement that will carry you through the progress. Because it can be frustrating. It can be grueling. Sometimes things just do not work and you may not immediately figure out why, and it may take a great deal of experimenting to understand where you went wrong. Remember that this idea of creating your perfect Skyrim is why you are going through all of it.

*Here is a word of warning: In years and years of modding Skyrim I have never reached that elusive peak, the moment of perfection. There is always something else, something that is missing, that is not quite right yet. Modding Skyrim is chasing the dragon. ~~Get out of here while you still can.~~*

## Skyrim Version

Skyrim originally relased all the way in 2011 and after the release of all three DLC, it was repackaged as "Skyrim Legendary Edition", or **SLE** for short. In 2016, Bethesda released the remaster "Skyrim Special Edition", or **SSE** for short. Since then, SSE has slowly overtaken SLE for modding and is the better choice nowadays. Its upgraded 64bit engine is vastly more stable compared to SLE's old 32bit version. All major mods and tools have been ported, and most of them are now developed and updated exclusively for SSE.

In order to follow Embers, you must own [**Skyrim Special Edition**](https://store.steampowered.com/app/489830/) on Steam.

The XBOX Game Pass and VR versions of Skyrim SE will not work.

> There are many more differences between SLE and SSE than noted here. We will talk about them later on.

## Folder Structure

Here's your first piece of advice: Keep your files in order. A well-organised modding directory where all files are consolidated in one place, always easy to find, is a big deal for quality of life. Throughout all lessons, I will be referring to this directory as **Your Modding Folder**. I recommend keeping it on a drive where space is not an issue (such as a general storage HDD). There is no point in wasting SSD space on this as it will not actually contain your mod setup.

- Please create a top-level or near top-level folder such as `F:\Skyrim Modding\`.
- Within that new folder, create several more folders:

![Your Modding Folder](/Pictures/tpf/initial-setup/modding-folder.png)

I will explain the purpose of each of these folders (where it is not obvious) later on.

## Spring Cleaning

Now comes the boring part: Before we install anything, we must make sure that you have no left-over files from previous mod setups. Embers requires you to start from scratch and old mod files may be disruptive. 

If you have absolutely **never modded Skyrim** before, it would be possible to simply go ahead and make sure your installation is in an appropriate directory (or move it using Steam if it is not). However, accounting for that option would overcomplicate the instructions and further bloat this page. Since the game is only about 13GB in size, I believe it is acceptable to ask every user to reinstall it from scratch.

If you do not have Skyrim SE installed right now but you did mod the game at some point, please also follow the instructions below. When uninstalling Skyrim SE through Steam, only the vanilla files in the installation folder will actually be deleted (meaning any mod-added files may still be present).

### Removing Skyrim

First uninstall Skyrim SE through Steam. This will delete all vanilla files. After you have done so, check if any mod-added files remain:

- Navigate to where the game was installed which is probably `C:\Program Files x86\Steam\steamapps\common\`.
- If there is still a **Skyrim Special Edition** folder present, delete it.

### Documents Folder

Next we will take a look at the **Documents** folder.

> If you have never run Skyrim before, this folder will not exist for you and you can skip ahead to the next step, Game Language.

- Navigate to `C:\Users\Your User Name\Documents\My Games\Skyrim Special Edition\`

This directory may contain multiple files and folders: The **Skyrim.ini** and **SkyrimPrefs.ini** are the game's primary configuration files, they will become very relevant later on. There may also be a **saves** folder which, you guessed it, contains your save games. If you have any vanilla saves that you would like to hold on to, move the **saves** folder to `\Your Modding Folder\Backups\` from where you can restore it anytime. Lastly, the Documents folder may also include mod-generated files such as logs.

- Make sure you have backed up any saves you want to keep.
- Delete the entire **Skyrim Special Edition** folder.

The folder and INI files will be freshly regenerated very soon.

That's it. Skyrim SE is now completely removed from your system.

## Game Language

Skyrim supports a bunch of different languages natively, but mods do not. Many do not require translations in the first place and some of the ones that do have third-party translations available so that it is theoretically possible to play modded in Skyrim in a language other than English. However, this will complicate your setup immensely. Translations where available may be outdated or incomplete. They may not cover voice acting. They may not exist for some of your mods at all.

Ultimately, translating any records (and certain textures!) untouched by existing patches plus fixing conflicts between translations and mods will add a hefty amount of work on top of everything else. I do not recommend it, particularly not for a beginner.

If your game is currently set to a language other than English, you can change this quickly in Steam. The English files will be downloaded immediately if you have the game currently installed, or the next time you install the game.

- Right-click **The Elder Scrolls V: Skyrim Special Edition** in your Steam games library.
- Select **Properties** and switch to the **Language** tab.
- Ensure that the language is set to **English**.

![Set language to English](/Pictures/tpf/initial-setup/skyrim-se-english.png)

## Installation Directory

In order to prevent various issues down the line, it is highly recommended not to install the game or any tools in **UAC-protected folders** such as `C:\Program Files\` and `C:\Program Files x86\`. UAC-protected folders in Windows are special because they require admin privileges for read/write permissions which can break various modding tools.

Because of this, you will likely have to create a new **Steam Library**.

> Already familiar with Steam Libraries and have one available outside UAC-protected folders? Skip ahead to the next step.

### Steam Library

A **Steam Library** is a directory on your hard drive designated as an installation folder by Steam; if you install any game, this is where it will be installed to. The default Steam Library is located inside your Steam installation folder. If you installed Steam itself without specifically changing the installation directory, it will now be located within `C:\Program Files x86\Steam\` and your default Steam Library will be `C:\Program Files x86\Steam\steamapps\common\` - exactly where we do not want it to be.

In the Steam settings, any folder can be set as a Steam Library. By default, there can only be one Steam Library per hard drive, however, a workaround exists.

### Conclusion

Skyrim should be installed:

- in a Steam Library outside the UAC-protected folders
- which is ideally on an SSD or otherwise fastest hard drive.

> An SSD is recommended for faster loading times. Depending on its speed, an HDD may also negatively impact overall performance.

If you want to create a new Steam Library on your `C:\` drive but already have your regular Steam installation and its default Steam Library on the same drive, you will need to use [**LostDragonist's Steam Library Setup Tool**](https://github.com/LostDragonist/steam-library-setup-tool/wiki/Usage-Guide) to create a second Steam Library on that drive (follow the link for instructions).

Otherwise, open the settings in Steam, go to the **Downloads** tab, and click the **Steam Library Folders** button. You can choose the drive and folder for your new Steam Library directly through the interface. Once set up, the new Steam Library can be selected upon installing a new game.

## Reinstalling Skyrim

Find the game in your library (in the Steam app) and click the big blue INSTALL button. Make sure to select your new Steam Library as the location to install all files to and wait for the game to be fully downloaded before you proceed.

### First Test Run

At this point, we should see if Skyrim launches properly. Running the game once serves multiple purposes:

- The `\Documents\My Games\Skyrim Special Edition` folder and INI files will be regenerated.
- The registry keys will be set up which is required for modding tools to recognise your installation.
- Certain issues with your vanilla game can be detected now.

In Steam, click the big green **PLAY** button to open the launcher.

- A message box will pop up, informing you that Skyrim SE will now be configured based on your hardware.
- Click **OK** twice to confirm (we will modify the INI files later on).
- Click the **PLAY** option in the launcher and wait until you are in the Skyrim main menu.
- Quit the game from the main menu. Everything appears to be running smoothly so far.

> If Skyrim is unable to detect your hardware, it’s likely because you have a newer AMD card. You can safely ignore this.

![Regenerating INIs](/Pictures/tpf/initial-setup/regenerating-inis.png)

## Mod Manager Choice

As mentioned before, learning how to mod Skyrim is in large part about learning how to use various tools to your advantage. Now that we have ensured Skyrim is returned to a pristine vanilla state, we can move on to installing the most important tool in our tool box:
 
**Mod Organizer 2** (MO2) is a mod manager. Like its predecessor, Mod Organizer, it is community-made and open-source, with a wide range of features catering specifically to advanced modders. If you are serious about building an extensive setup of mods, Mod Organizer 2 is going to be your best friend.

Of course, there are alternatives. Other mod managers include the now deprecated Nexus Mod Manager (NMM) and its successor, Vortex. While Vortex has made great progress over the years and far outclasses its predecessor, its attractiveness for Bethesda games in general has been somewhat dimished by its ambition to accomodate a vast amount of games, turning the tool into a jack-of-all-trades. There are many reasons why NMM, Vortex, and indeed other community-made managers such as Kortex and Wrye Bash are generally inferior to Mod Organizer 2. However, this is not the time nor the place to delve into them.

### Why Mod Organizer 2?

Instead of listing all the features of MO2 right now, I will slowly introduce them as we start to install and configure mods throughout the upcoming lessons. Many of its unique advantages would make very little sense to you before we have established some basic knowledge about modding in general. I will also gradually explain various elements of the UI as we go, so do not feel discouraged or overwhelmed when you first open the tool.

### Can I use another mod manager?

Yes, but I would strongly recommend against it.

Your mod manager is the heart and soul of your setup. The steps you go through in building that setup are very specific to the tool you choose: Vortex is used differently to Mod Organizer 2, particularly with regard to load and mod order management. While Embers is intended to teach you the concepts of load and mod order in general, it is also important to learn how maintaining and expanding your setup works in the practical sense. Accommodating multiple different mod managers would require many sections of Embers to be written twice.

> The MO2 vs Vortex question is hotly debated in the community. In my personal opinion, there are many good reasons for using Vortex in 2021. However, I also believe that its approach to load and mod order management is critically flawed. In addition to that, many quality of life features that I use daily in Mod Organizer 2 are missing altogether. This is why Embers is centered around Mod Organizer 2.

## Nexus Mods

The vast majority of mods and tools (including Mod Organizer 2) are hosted on [**Nexus Mods**](https://www.nexusmods.com/). The Nexus supports hundreds of games, but it should come as no surprise that the six games with the most downloads in total (by a wide margin) are the most recent Bethesda games. You will download many files from various Nexus pages over the coming lessons and we will also talk about the site in general. In order to download mods, you must have an account.

If you do not have a [**Nexus Mods**](https://www.nexusmods.com/) account yet, go ahead and create one now.

### About Nexus Premium

[**Nexus Premium**](https://users.nexusmods.com/register/memberships) is a subscription service that grants certain perks to users, including removal of all ads as well as faster downloads. Somewhat recently, the Nexus has also added on additional click to the process of downloading a file which includes a countdown and an ad for the Premium membership to further incentivise purchasing a subscription.

I recommend holding off on Premium until you have progressed enough in your modding journey to know that you will stick with it for a while. When building a larger mod setup, paying for a month or so of Premium can be worth the asking price. It is also a great way of giving back to the Nexus for their service, especially for those of us with ad blockers installed.

> I personally have lifetime Nexus Premium and it is invaluable to me. However, I also use the Nexus almost daily.

### Navigating the Nexus

While the Nexus has separate sections for more than 1,000 games, we are of course largely interested in the [**Skyrim Special Edition**](https://www.nexusmods.com/skyrimspecialedition) (SSE,2016) and occasionally the [**Skyrim**](https://www.nexusmods.com/skyrim) (SLE, 2011) sections (mods can be ported from SLE to SSE, more on that later).

- Open the [**Skyrim Special Edition**](https://www.nexusmods.com/skyrimspecialedition) part of the Nexus.
- In the search bar at the top, enter "Mod Organizer 2" and select the first result.

You are now looking at the mod page for Mod Organizer 2. All mod pages, whether they are for mods or for tools, have the same layout. There are screenshots near the top and if you scroll down, you will see the description which is typically the first thing you want to check about any mod. It is not necessary to read the description for MO2 right now (although you can if you like), so we can proceed directly to the **Files** section.

![Nexus Files Section](/Pictures/embers/module-1/nexus-files-section.png)

The **Files** section of most mod pages contains various different types of files as well as an archive of old versions. The main file is usually what you are interested in, it is at the top of the page.

- Click the **Manual Download** button for **Mod Organizer 2** under **Main Files**.
- If you do not have Nexus Premium, you will need to click **Download** again on the next page after a brief countdown.

![Nexus Download MO2](/Pictures/embers/module-1/nexus-download-mo2.png)

## Installing MO2

Since we just downloaded Mod Organizer 2, we can continue by running the executable.

Upon double-clicking it, Windows will likely throw a warning, asking you whether you really want to launch an unrecognised app. Fair enough: Blindly downloading and running executables is not the smartest thing to do.

Thankfully, the Nexus automatically runs all uploaded files (up until a size of 250MB) through Virus Total, a page that allows quickly checking a file for malware. On all mod pages, including the one for Mod Organizer 2, you can click the **green checkmark** (denoting the fact that the file was found to be harmless) to open the Virus Total page.

![Nexus Virus Check](/Pictures/embers/module-1/nexus-virus-check.png)

> Sometimes after an update, Mod Organizer 2 may be flagged by certain antivirus software as potentially malicious. This is because of its VFS, the virtual file system, which we will talk about later on. This can also cause any antivirus software installed on your PC to quarantine parts of MO2, breaking the tool. However, after manual verification the file is usually cleared within a few days to weeks. This is why it is usually best not to immediately update MO2 if you have antivirus software other than Windows Defender.

Now that we have made sure the file is safe, run the Mod Organizer 2 executable again.

If Windows warns you against it, click **More Info** and **Run anyway**.

### Installer Configuration

In the MO2 installer, accept the license agreement and proceed to the next page.

You will be asked where to install Mod Organizer 2. Choosing the right directory is important for several reasons:

- Mod Organizer 2 should be installed on the same drive as the base game.
- Mod Organizer 2 should be installed on an SSD for faster loading times.

All your mods will be contained within the MO2 folder, potentially adding up to 100GB and beyond, depending on the size of your setup. For now, make sure you have at least 50GB of free space on whichever hard drive you choose, that will be enough to get started.

![MO2 Installation Directory](/Pictures/embers/module-1/mo2-installation-directory.png)

For the rest of the installer, you can simply keep clicking **Next** to install the tool with all components into your chosen directory.

Click **Finish** once all files have been extracted. Mod Organizer 2 will be launched automatically so you can proceed with the next step.

### Instance Setup

After the initial installation process, another window with more setup steps will greet you. It will inform you about **Instances** which are one of the tool's most valuable features. 

- Click **Next** in the configuration window.
- Select **Create a portable instance** on the next page.

As the installer explains, portable instances are self-contained. They allow you to run as many copies of Mod Organizer 2 as you like, for various games or different setups. You may have noticed in the screenshot above that my MO2 instance for Embers is located under `G:\Mod Organizer 2 Instances\`. I personally run five or more instances at any given time, for both Skyrim SE and Fallout 4. All are contained within that folder, without ever interfering with each other.

- On the next page in the configuration wizard, select **Skyrim Special Edition** (which should be detected automatically).
- Click **Next** again on the following page to confirm using your MO2 installation folder for all sub directories.
- And lastly, click **Finish** to finalise your new MO2 instance.

![MO2 Instance Creation](/Pictures/embers/module-1/mo2-instance-creation.png)

## MO2 Interface

Mod Organizer 2 should now launch automatically, giving you a first look at the tool. If the interface seems daunting at first, do not be discouraged: You will get used to it faster than you may think! Much of the UI simply makes a great deal of sense which is why it will quickly become easy to navigate.

Before we do anything, let us disable the log at the bottom. You are not going to need it (for now).

![MO2 Disable Log](/Pictures/embers/module-1/mo2-disable-log.png)

I also recommend right-click the MO2 icon on your taskbar and **pinning** it for quick access.

### Overview

At this point, we are not going to discuss the meaning of the various parts of MO2's interface: Without context, it would be difficult to remember. For now, please have a look at the five primary components of the MO2 interface which I will refer to from now on by the names defined below.

**(1) The toolbar** allows you quick access to a number of sub menus.

**(2) The profile drop-down** allows to quickly switch between MO2 profiles.

**(3) The executables drop-down** allows to select an executable like the game or a tool. Almost all executables must be run through MO2.

**(4) The left pane** is the *mod order*. This is where all your mods will appear once installed and where they can be managed.

**(5) The right pane** contains various tabs, the one open now is the *load order* where your plugins will appear.

![MO2 UI Overview](/Pictures/embers/module-1/mo2-ui-overview.png)

## MO2 Settings

Open the **Settings** by clicking the first icon on the right in the Toolbar. Note that we will *not* go through all tabs.

### General

Under **Download List**, I highly recommend checking **Show meta information** and **Compact list**. This will affect the Downloads tab in the right pane of MO2 where all downloaded files will appear. As the list grows, a more compact view with information about the file version and type will become invaluable. Check out the [**default settings**](https://i.imgur.com/BW4F4tD.png) versus the [**improved settings**](https://i.imgur.com/eNnzd6p.png).

I personally do not use the **Hide downloads after installation** option. Of course, the list of downloads in my MO2 setups is hundreds of files long, and yes, hiding files after installing them will keep the downloads tab clean. All hidden mods can quickly be made visible again by ticking the **Hidden files** box at the bottom of the downloads tab, and individual files can be hidden and un-hidden at will. But I prefer the simplicity of simply leaving all visible and using the search bar to find what I am looking for. Once you start installing mods later on, you can make your own choice.

Otherwise, I recommend leaving the remaining options at default.

### Themes

While I personally use light mode in the majority of my apps and programs, I realise that my opinion is an unpopular one. Under **Style**, you can try out various other themes. If you are looking for a simple dark theme, I recommend the **1809 Dark Mode** option, but do feel free to have a look at the other options, too. Make sure to restart MO2 after changing the theme, as some parts of the UI may not update correctly otherwise.

The **Colors** section below affects the colors in which mods and separators will light up in when highlighting them. I highly suggest not tampering with them until you have a proper understanding of mod order and asset conflicts.

### Paths

Since we set up MO2 as a portable instance, all file paths to the various directories are currently within the MO2 installation itself: `/%BASE_DIR%/`. We already discussed the potential size of the **mods** folder, which can easily exceed 50GB, but should nevertheless be located on the same drive as the base game, ideally an SSD.

However, the downloaded archives from which the mods are installed do not need to be on an SSD. They are only needed for the initial installation and merely serve as backups afterward.

Therefore I personally recommend changing the **Downloads** directory to a different drive. While my Steam Library and MO2 instance are on my gaming SSD `G:\`, I set up my modding folder on a larger HDD, `F:\`. If you recall, we created an **ARCHIVE** folder when setting up **Your Modding Folder** earlier. It was intended for this purpose: Storing any mod archives you download in the future.

- Click the dotted button next to **Downloads** to change the file path.
- Navigate to `\Your Modding Folder\ARCHIVE\`.
- Create a new folder there and name it **MO2 Downloads**.
- Point Mod Organizer 2 to that folder.

> We are not using the **ARCHIVE** folder itself as we can use it to store files other than MO2 downloads, such as ENB presets, binaries, and other root folder files. This will be discussed later on.

![MO2 Downloads Folder](/Pictures/embers/module-1/mo2-downloads-folder.png)

### Nexus

If you have not done so already, you need to connect your Mod Organizer 2 installation to your Nexus account now. This will allow you to download mods directly through MO2's interface, saving you a few extra clicks.

- Click **Connect to Nexus**.
- This will open a browser window where you will be asked to confirm.
- Click **Authorise**. You can revoke this any time in your Nexus settings.
- Close the **Settings** window.
- Mod Organizer 2 may ask you to restart. Click **OK**.

![MO2 Nexus Authorisation](/Pictures/tpf/initial-setup/authorise-mo2.png)

## Conclusion

**Congratulations, you completed Lesson 1!**

We have now done all the basic preparations necessary before we can dive into actual mod installation. Of course there are many more tools to install and procedures to follow, but they can be addressed later on. Since we have the setup out of the way now, the next lesson will finally deal with mods themselves.