---
title: "MO2 Setup"
weight:
type: docs
description: >
  How to set up Mod Organizer 2.
---

{{< alert color="info" title="Summary" >}}
> This module covers the installation and basic configuration of Mod Organizer 2.<p>
> **Prerequisite(s):** [Clean Install](/bg/additional-modules/clean-install/){{< /alert >}}

## MO2 Prerequisites

Mod Organizer 2 has two prerequisites.

While you may already have them install, I recommend (re)installing them to be sure:

- Download [.NET Framework 4.8](https://dotnet.microsoft.com/download/dotnet-framework/thank-you/net48-web-installer) and follow the instructions in the installer.
- Download the [Microsoft Visual C++ Redistributable](https://aka.ms/vs/16/release/vc_redist.x64.exe) and follow the instructions in the installer.
    
To finalise the installation you may be required to restart your PC.

## Downloading MO2

Mod Organizer 2 is hosted on the Nexus and on Github.

- Open the [Mod Organizer 2](https://www.nexusmods.com/skyrimspecialedition/mods/6194) Nexus page.
- Switch to the **Files** tab.
- Click the **Manual Download** button for **Mod Organizer 2** under **Main Files**.

> If you do not have **Nexus Premium**, you will need to click **Download** again on the next page after a brief countdown.

![Download MO2](/Pictures/bg/mo2-setup/download-mo2.png)

## Installing MO2

Save the downloaded executable to a convenient location and double-click it.

If there is a Windows warning, click **More Info** and **Run anyway**.

{{< alert >}} Worried about catching a virus? Read about the [Nexus Virus Check](/bg/knowledge-base/nexus-virus-check/).{{< /alert >}}

### Installer Configuration

In the MO2 installer, accept the license agreement and proceed to the next page.

You will be asked where to install Mod Organizer 2.

- Once again, **selecting an SSD or NVME is highly recommended** as it will improve load times and in-game performance.
- **The MO2 folder will contain all your mods** which may add up to **100GB** and more.
  
For now, make sure you have <u>at least 50GB of free space</u> on whichever hard drive you choose. That will be sufficient to get started.

![MO2 Installation Directory](/Pictures/bg/mo2-setup/mo2-installation-directory.png)

For the rest of the installer, you can simply keep clicking **Next** to install the tool with all components into your chosen directory.

Click **Finish** once all files have been extracted. Mod Organizer 2 will be launched automatically so you can proceed with the next step.

### Instance Setup

After the initial installation process, the **Instance Manager** will open where we will create a new **portable instance**. These are self-contained and allow you to run as many copies of Mod Organizer 2 as you like, for various games or different setups.

(I personally run five or more instances at any given time, for both Skyrim SE and Fallout 4, none of which interfere with each other.)

Click the **Create new instance** button to proceed.

![MO2 New Instance](/Pictures/bg/mo2-setup/mo2-new-instance.png)
  
- Click **Next** in the configuration window.
- Select **Create a portable instance** on the next page.
- On the next page in the configuration wizard, select **Skyrim Special Edition**.
- Click **Next** again on the following page to confirm using your MO2 installation folder for all sub directories.
- Click **Connect to Nexus**\* and switch to the browser to authorise MO2 to connect your account.
	- In the MO2 installer, you should see: **Linked with Nexus successfully**.
- Proceed to the next step and click **Finish** to finalise your new MO2 instance.

<font size="2">\**If you are not prompted to connect MO2 to the Nexus, you have likely already done this for a previous MO2 installation.*</font>

### First Launch

Mod Organizer 2 should launch automatically.

- Click **No** when asked to see the tutorial.
	- We will go over the various parts of MO2 in this guide.
- If asked whether MO2 should handle NXM links, click **Yes**.
	- This allows automatic downloads from the Nexus through MO2.

Before we do anything else, let's disable the log at the bottom. We are not going to need it.

![disable mo2 log](/Pictures/bg/mo2-setup/disable-mo2-log.png)

> I also recommend right-clicking the MO2 icon on your taskbar and **pinning** it for quick access.

## MO2 Settings

Open the **Settings** by clicking the first icon on the right in the toolbar.

![MO2 Open Settings](/Pictures/bg/mo2-setup/mo2-open-settings.png)

### Settings: General

Under **Download List**, I highly recommend checking **Show meta information** and **Compact list**. This will affect the Downloads tab in the right pane of MO2 where all downloaded files will appear. As the list grows, a more compact view with information about the file version and type will become invaluable.

>Check out the [default settings](https://i.imgur.com/BW4F4tD.png) versus the [compact settings](https://i.imgur.com/eNnzd6p.png).

I personally do not use the **Hide downloads after installation** option. Of course, the list of downloads in my MO2 setups is hundreds of files long, and yes, hiding files after installing them would keep the downloads tab clean. All hidden mods can quickly be made visible again by ticking the **Hidden files** box at the bottom of the **Downloads** tab, and individual files can be hidden and unhidden at will. Personally, I prefer the simplicity of simply leaving everything visible and using the search bar to find what I am looking for. Once you start installing mods, you should make your own choice.

### Settings: Themes

While I personally prefer light mode in the majority of my apps and programs, I realise that my opinion is rather unpopular. Under **Style**, you can try out various other themes. If you are looking for a simple dark theme, I recommend the **1809 Dark Mode** option for now. It is similar to the default light theme and will make following along with my screenshots easier.

>Make sure to restart MO2 after changing the theme.

The **Colors** section below affects the colors in which mods and separators will light up when highlighting them. I strongly suggest not tampering with them until you have a proper understanding of mod order and asset conflicts.

### Settings: Paths

Since we set up MO2 as a portable instance, all file paths to the various directories are currently within the MO2 installation itself: `/%BASE_DIR%/`, the base directory. We already discussed the potential size of the mods folder, which can easily exceed 50GB, but should nevertheless be located on a fast drive, ideally an SSD.

However, **the downloaded archives from which the mods are installed do NOT need to be on an SSD**. They are only required for the initial installation and merely serve as backups afterwards.

Keeping the archives is nevertheless recommended as you may want to reinstall a mod later on to choose different options if they come with an installer, or simply to restore it to the vanilla state if you modified it. Hence, I recommend changing the **Downloads** directory to a different drive. Pick the hard drive with the most amount of space; any HDD will do.\*

<font size="2">\**It should be noted that keeping downloaded archives on a faster drive may speed up mod installation, including for Wabbajack list. Nevertheless, SSD / NVME space is precious and I personally prefer to use it for more mods or other games.*</font>

{{< alert color="warning" >}} This is a recommendation, not a requirement. Manage your disk space as you see fit. {{< /alert >}}

![Downloads Folder](/Pictures/bg/mo2-setup/mo2-downloads-folder.png)

---

{{< alert color="success" >}}If you are currently working through the Core Module, return to [Step 1](/bg/core-module/step1/#ui-overview). {{< /alert >}}