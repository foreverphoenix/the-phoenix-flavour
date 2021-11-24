---
title: "Step 2: Mod Organizer 2"
weight: 2
type: docs
description: >
  Installing and configuring Mod Organizer 2.
---

## Mod Manager Choice

Learning how to mod Skyrim SE is in large part about learning how to use various tools to your advantage. Now that we have ensured Skyrim is returned to a pristine vanilla state, we can move on to installing the most important tool in our tool box:
 
**Mod Organizer 2** (MO2) is a mod manager. Like its predecessor, Mod Organizer, it is community-made and open-source, with a wide range of features catering specifically to advanced modders. If you are serious about building an extensive setup of mods, Mod Organizer 2 is going to be your best friend.

Of course there are alternatives. Other mod managers include the now deprecated Nexus Mod Manager (NMM) and its successor, Vortex. While Vortex has made great progress over the years and far outclasses its predecessor, its attractiveness for Bethesda games in general has been somewhat diminished by its ambition to accommodate a vast amount of different games, turning the tool into a jack-of-all-trades.

### Why Mod Organizer 2?

Instead of listing all the features of MO2 right now, I will slowly introduce them to you as we start to install and configure mods throughout the upcoming lessons. Many of its unique advantages would make very little sense to you before we have established some basic knowledge about modding in general. I will also gradually explain various elements of the UI as we go, so do not feel discouraged or overwhelmed when you first open the tool.

### Can I use another mod manager?

Technically yes, but I would strongly recommend against it.

Your mod manager is the heart and soul of your setup. The steps you go through in building that setup are very specific to the tool you choose: Vortex is used differently from Mod Organizer 2, particularly with regards to load and mod order management. While **Embers** is intended to teach you the concepts of load and mod order in general, it is also important to learn how maintaining and expanding your setup works in the practical sense. Accommodating multiple different mod managers would require many sections of **Embers** to be written twice.

> The MO2 vs Vortex question is hotly debated in the community. In my personal opinion, there are many good reasons for using Vortex nowadays. However, I also believe that its approach to load and mod order management is critically flawed. In addition to that, many quality of life features that I use daily in Mod Organizer 2 are missing altogether. This is why **Embers** is built around Mod Organizer 2.

## Visual C++ Redist

The Microsoft Visual C++ Redistributable is a basic package required by Mod Organizer 2. You probably already have it installed with Windows but it is best to make sure.

- Open the official [Microsoft Visual C++](https://support.microsoft.com/en-us/topic/the-latest-supported-visual-c-downloads-2647da03-1eea-4433-9aff-95f26a218cc0) website.
- Scroll to the **Visual Studio 2015, 2017 and 2019** section.
- Download the following file: `vc_redist.x64.exe`.
- Run the executable, it will guide you through the installation process.

![VC Redist](/Pictures/tpf/initial-setup/vc-redists.png)

## Nexus Mods

The vast majority of mods and tools (including Mod Organizer 2) are hosted on [Nexus Mods](https://www.nexusmods.com/). The Nexus supports hundreds of games, but it should come as no surprise that the six games with the most downloads in total (by a wide margin) are the most recent Bethesda games. You will download many files from various Nexus pages over the coming lessons and we will also talk about the site in general. In order to download mods, you must have an account.

If you do not have a [Nexus Mods](https://www.nexusmods.com/) account yet, go ahead and create one now.

### About Nexus Premium

[Nexus Premium](https://users.nexusmods.com/register/memberships) is a subscription service that grants certain perks to users, including removal of all ads as well as faster downloads. The Nexus has also added an additional click to the process of downloading a file which includes a countdown and an ad for the Premium membership to further incentivise purchasing a subscription.

I recommend holding off on Premium until you have progressed enough in your modding journey to know that you will stick with it for a while. When building a larger mod setup, paying for a month or so of Premium can be well worth the asking price. It is also a great way of giving back to the Nexus for their service, especially for those of us with ad blockers installed.

> I personally have lifetime Nexus Premium and it is invaluable to me. However, I also use the Nexus almost daily.

### Navigating the Nexus

While the Nexus has separate sections for more than 1,000 games, we are of course largely interested in the [Skyrim Special Edition](https://www.nexusmods.com/skyrimspecialedition) (SSE, 2016) and occasionally the [Skyrim](https://www.nexusmods.com/skyrim) (SLE, 2011) sections (mods can be ported from SLE to SSE, more on that later).

- Open the [Skyrim Special Edition](https://www.nexusmods.com/skyrimspecialedition) part of the Nexus.
- In the search bar at the top, enter "Mod Organizer 2" and select the first result.

You are now looking at the mod page for Mod Organizer 2. All mod pages, whether they are for mods or for tools, have the same layout. There are screenshots near the top and if you scroll down, you will see the description which is typically the first thing you want to check about any mod. It is not necessary to read the description for MO2 right now (although you can if you like), so we can proceed directly to the **Files** section.

![Nexus Files Section](/Pictures/embers/module-1/nexus-files-section.png)

The **Files** section of most mod pages contains various different types of files as well as an archive of old versions. The main file is usually what you are interested in. It is at the top of the page.

- Click the **Manual Download** button for **Mod Organizer 2** under **Main Files**.
- If you do not have Nexus Premium, you will need to click **Download** again on the next page after a brief countdown.

![Nexus Download MO2](/Pictures/embers/module-1/nexus-download-mo2.png)

## Installing MO2

Save the downloaded executable to a convenient location like `\Your Modding Folder\ARCHIVE\` and double-click it.

Windows will likely throw a warning, asking you whether you really want to launch an unrecognised app. Fair enough: Blindly downloading and running executables is not the smartest thing to do.

Thankfully, the Nexus automatically runs all uploaded files (up until a size of 250MB) through Virus Total, a page that allows quickly checking a file for malware. On all mod pages, including the one for Mod Organizer 2, you can click the **green checkmark** (denoting the fact that the file was found to be harmless) to open the Virus Total page.

![Nexus Virus Check](/Pictures/embers/module-1/nexus-virus-check.png)

> Sometimes after an update, Mod Organizer 2 may be flagged by certain antivirus software as potentially malicious. This is because of its VFS, the virtual file system, which we will talk about later on. This can also cause any antivirus software installed on your PC to quarantine parts of MO2, breaking the tool. However, after manual verification the file is usually cleared within a few days to weeks. This is why it is usually best not to immediately update MO2 if you have antivirus software other than Windows Defender.

Now that we have made sure the file is safe, run the Mod Organizer 2 executable again.

If Windows warns you against it, click **More Info** and **Run anyway**.

### Installer Configuration

In the MO2 installer, accept the license agreement and proceed to the next page.

Next up, you will be asked where to install Mod Organizer 2. Selecting an SSD is highly recommended as it will improve load times and ingame performance. However, you should be aware that all your mods will be contained within the MO2 folder, potentially adding up to 100GB and beyond, depending on the size of your setup.

For now, make sure you have at least 50GB of free space on whichever hard drive you choose, that will be enough to get started.

![MO2 Installation Directory](/Pictures/embers/module-1/mo2-installation-directory.png)

For the rest of the installer, you can simply keep clicking **Next** to install the tool with all components into your chosen directory.

Click **Finish** once all files have been extracted. Mod Organizer 2 will be launched automatically so you can proceed with the next step.

### Instance Setup

After the initial installation process, another window with more setup steps will greet you. It will inform you about **Instances** which are one of the tool's most valuable features. 

- Click **Next** in the configuration window.
- Select **Create a portable instance** on the next page.

As the installer explains, portable instances are self-contained. They allow you to run as many copies of Mod Organizer 2 as you like, for various games or different setups. You may have noticed in the screenshot above that my MO2 instance for **Embers** is located under `G:\Mod Organizer 2 Instances\`. I personally run five or more instances at any given time, for both Skyrim SE and Fallout 4. All are contained within that folder, without ever interfering with each other.

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

**(5) The right pane** contains various tabs. The one open now is the *load order* where your plugins will appear.

![MO2 UI Overview](/Pictures/embers/module-1/mo2-ui-overview.png)

## MO2 Settings

Open the **Settings** by clicking the first icon on the right in the toolbar.

### General

Under **Download List**, I highly recommend checking **Show meta information** and **Compact list**. This will affect the Downloads tab in the right pane of MO2 where all downloaded files will appear. As the list grows, a more compact view with information about the file version and type will become invaluable. Check out the [**default settings**](https://i.imgur.com/BW4F4tD.png) versus the [**improved settings**](https://i.imgur.com/eNnzd6p.png).

I personally do not use the **Hide downloads after installation** option. Of course, the list of downloads in my MO2 setups is hundreds of files long, and yes, hiding files after installing them will keep the downloads tab clean. All hidden mods can quickly be made visible again by ticking the **Hidden files** box at the bottom of the downloads tab, and individual files can be hidden and un-hidden at will. But I prefer the simplicity of simply leaving all visible and using the search bar to find what I am looking for. Once you start installing mods later on, you can make your own choice.

Otherwise, I recommend leaving the remaining options at default.

### Themes

While I personally use light mode in the majority of my apps and programs, I realise that my opinion is an unpopular one. Under **Style**, you can try out various other themes. If you are looking for a simple dark theme, I recommend the **1809 Dark Mode** option for now. It is similar to the default light theme and will make following along with my screenshots easier. Make sure to restart MO2 after changing the theme, as some parts of the UI may not update correctly otherwise.

The **Colors** section below affects the colors in which mods and separators will light up in when highlighting them. I highly suggest not tampering with them until you have a proper understanding of mod order and asset conflicts.

### Paths

Since we set up MO2 as a portable instance, all file paths to the various directories are currently within the MO2 installation itself: `/%BASE_DIR%/`, the base directory. We already discussed the potential size of the **mods** folder, which can easily exceed 50GB, but should nevertheless be located on a a fast hard drive, ideally an SSD.

However, the downloaded archives from which the mods are installed do *not* need to be on an SSD. They are only needed for the initial installation and merely serve as backups afterward. Keeping them around is always recommended as you may want to reinstall a mod later on (to choose different options if they come with an installer or simply restore it to the vanilla state if you modified it).

Therefore I personally recommend changing the **Downloads** directory to a different drive. While my Steam Library and MO2 instance are on my gaming SSD `G:\`, I set up my modding folder on a larger HDD, `F:\`. If you recall, we created an **ARCHIVE** folder when setting up **Your Modding Folder** earlier. It was intended for this purpose: Storing any mod archives you download in the future.

- Click the dotted button next to **Downloads** to change the file path.
- Navigate to `\Your Modding Folder\ARCHIVE\`.
- Create a new folder there and name it **MO2 Downloads**.
- Point Mod Organizer 2 to that folder.

![MO2 Downloads Folder](/Pictures/embers/module-1/mo2-downloads-folder.png)

### Nexus

If you have not done so already, you need to connect Mod Organizer 2 to your Nexus account. This will allow you to download mods directly through MO2's interface, saving you a few extra clicks.

- Click **Connect to Nexus**.
- This will open a browser window where you will be asked to confirm.
- Click **Authorise**. You can revoke this any time in your Nexus settings.
- Close the **Settings** window.
- Mod Organizer 2 may ask you to restart. Click **OK**.

![MO2 Nexus Authorisation](/Pictures/tpf/initial-setup/authorise-mo2.png)

---

#### Continue with [Step 3: Root and Data](/embers/module-1/step-3/).