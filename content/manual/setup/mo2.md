---
title: "Mod Organizer 2"
weight: 3
type: docs
description: >
  How to install, configure, and extend Mod Organizer 2.
---

## Why Mod Organizer 2?

{{< alert color="info" >}}If you are already familiar with Mod Organizer 2 and its virtual file system, feel free to skip ahead to [the next section]((/manual/setup/mo2#mo2-installation)).{{< /alert >}}

Your mod manager is your workspace where you install, view, and modify your mods. It is the heart and soul of your setup and -- if you enjoy tinkering -- you will probably spend more time here than in-game. That's why it's important to choose the right tool.

There are two viable mod managers for Skyrim SE: [Vortex](https://www.nexusmods.com/about/vortex) and [Mod Organizer 2](https://www.nexusmods.com/skyrimspecialedition/mods/6194) (MO2).

- **Vortex** is the official mod manager of the Nexus. It takes a jack-of-all-trades approach and works with most of the moddable games supported by the website.
- By contrast, **Mod Organizer 2** was specifically designed for modding Bethesda games. While Vortex is perfectly fine for simple modded setups with minimal custom edits, MO2's at-a-glance interface and its approach to file management make it the superior tool for building complex setups for Skyrim and other Bethesda games.

That is why TPF is built in Mod Organizer 2.

### MO2's Virtual File System

Arguably the best feature of Mod Organizer 2 is the **Virtual File System**, for VFS for short. Here is how it works:

When you install a mod through MO2, the files are not extracted into the data folder directly but into separate, self-contained mod folders. From these files MO2 builds a **virtual data folder** at runtime. Files from different mods never actually conflict with or overwrite each other.

Your folder structure will look like this:

```
\Mod Organizer 2\mods\Mod 1\<files from mod 1>
\Mod Organizer 2\mods\Mod 2\<files from mod 2>
\Mod Organizer 2\mods\Mod 3\<files from mod 3>
```

The separation of mod files creates the concept of a **mod order**: If two mods contain the same files, the one placed lower in the mod order will be overwritten in the virtual data folder. Since the files never actually conflict, you can adjust the mod order via drag-and-drop at any time.

Additionally, you can review and compare files without having to reinstall and overwrite, and you will always know which mod any given file belongs to. In this way, the virtual data folder vastly simplifies file management.

And that is why Mod Organizer 2 is going to be our best friend. Cherish it!

## MO2 Installation

### Prerequisites

Mod Organizer 2 has two prerequisites. It is possible that you already have them installed, but I recommend (re)installing them just to be sure:

- Download [.NET Framework 4.8](https://dotnet.microsoft.com/download/dotnet-framework/thank-you/net48-web-installer) and follow the instructions in the installer.
- Download the [Microsoft Visual C++ Redistributable](https://aka.ms/vs/16/release/vc_redist.x64.exe) and follow the instructions in the installer.

To finalise the installation you may be required to restart your PC.

### Downloading MO2

Mod Organizer 2 is hosted on the Nexus and on Github. Dev builds for testing are available on [Discord](https://discord.com/invite/ewUVAqyrQX).

- Open the [Mod Organizer 2](https://www.nexusmods.com/skyrimspecialedition/mods/6194) Nexus page.
- Switch to the **Files** tab.
- Click the **Manual Download** button for Mod Organizer 2 under **Main Files**.

If you do not have Nexus Premium, you will need to click **Download** again on the next page after a brief countdown.

![Download MO2]

### Installer Configuration

- Save the downloaded executable to a convenient location and double-click it.
- If there is a Windows warning, click **More Info** and **Run anyway**.*
- In the MO2 installer, accept the license agreement and proceed to the next page.

<font size=2>\* All files uploaded to the Nexus (barring those that are too big in size) are automatically run through the [VirusTotal](https://www.virustotal.com/gui/home/upload) check. You can view the report by clicking the checkmark next to the mod name ([screenshot](/Pictures/manual/nexus-virus-check.png)).</font size>

You will be asked where to install Mod Organizer 2. There are two things you need to keep in mind when selecting a location:

- It is highly recommended to install MO2 on an **SSD** to improve load times and in-game performance. However, be aware that all your mods and downloads will be contained within the MO2 folder. TPF currently requires a total of <mark>placeholder GB</mark> of disk space, so the drive you select with need at least that much free space.
- It is highly recommended to install MO2 on the same harddrive as the game.
- Do not install MO2 into a UAC-protected folder such as `C:\Program Files\`.

![MO2 Directory]

### Instance Manager

After the initial installation process, the **Instance Manager** will open where we will create a new **portable instance**. Instances are self-contained and allow you to create as many copies of Mod Organizer 2 as you need for various games or different setups.

- Click **Next** and **Create a portable instance** to proceed.
- Select **Skyrim Special Edition**.
- Select the **Steam** version.
- Configure the **profile settings** as follows:
    - Enable *Use profile-specific game INI files*.
    - Enable *Use profile-specific save games*.
- Disable **Automatic archive invalidation** (unnecessary for Skyrim SE).
- Leave the location for data files unchanged.
- Check the summary and click **Finish**.

![MO2 Instance]

### First Launch

Mod Organizer 2 should launch automatically.

- You will be prompted to view the tutorial -- you can skip this and rely on the guide.
- If asked whether MO2 should handle NXM links, click **Yes**.
- If asked about the **Category Setup**, select **Do Nothing**.

Mod Organizer 2 will now open properly.

{{< alert color="warning" >}}I recommend right-clicking the MO2 icon on your taskbar and pinning it for quick access.{{< /alert >}}

### SSL Error Fix

After a recent Nexus API update, Mod Organizer 2 throws an SSL error when attempting to download mods. We can fix this by deleting a file:

- Close Mod Organizer 2.
- Navigate to the MO2 installation directory.
- Delete the `libssl-3-x64.dll`.
- Restart Mod Organizer 2.

## MO2 Interface

Now we get our first look at MO2. If the interface seems daunting, do not feel discouraged! You will get used to it faster than you may think. Much of the UI simply makes a great deal of sense which is why it will quickly become easy to navigate.

At this point, I am not going to discuss the purpose of the various parts of MO2's interface -- without context, the details would be difficult to memorise. For now, please have a look at the five primary components of the UI which I will refer to from now on using the terms given below.

- **(1) The toolbar** allows you quick access to a number of sub menus.
- **(2) The profile drop-down** allows quick switching between MO2 profiles.
- **(3) The executables drop-down** is where you select and run executables like the game or a tool.
- **(4) The left pane** is the mod order. This is where all your mods will appear once installed.
- **(5) The right pane** contains various tabs like the Plugins tab for managing the load order.

{{< alert color="info" >}}You will also see all Creation Club files that you own in MO2. They will be dealt with in the next step.{{< /alert >}}

![MO2 UI Overview]

### Interface Adjustments

I always make some minor modifications to the MO2 interface and I do recommend you follow along with this step.

- First, I always disable the log at the bottom. I have never needed it and it takes up space.

![Disable MO2 Log]

The <mark>right pane</mark> of Mod Organizer 2 features a number of tabs, none of which require much space to properly display. I typically reduce the right pane to take up about a fourth of the window. Leave the columns in the **Plugins** tab be for now -- we will install a plugin that adds more in a little while.

The <mark>left pane</mark> of Mod Organizer 2 represents the **mod order**. This is where all your mods will show up.

- Right-click the columns at the top to configure which columns are displayed.

![Modify Mod Order Columns]

- ✔️**Conflicts:** Displays little icons to show overwrites.
- ✔️**Flags:** Not necessary but recommended. Shows if notes are appended to a mod.*
- ✔️**Content:** Very helpful because it shows you which types of assets are contained in a mod.
- ❌**Category:** Uses Nexus categories by default. Separators are better for sorting.**
- ❌**Nexus ID:** The ID of the respective mod (which is the combination of numbers at the end of its URL).
- ❌**Source Game:** Somewhat useful when mixing Skyrim LE and Skyrim SE mods which is not very common anymore.
- ✔️**Version:** Mostly helpful for tracking updates.
- ❌**Installation:** Displays the date of installation. Not sure what you would need this for.
- ✔️**Priority:** Shows the position in the mod order. This is what the right pane should always be sorted by.***
- ✔️**Notes:** See short notes at a glance. (AKA my favourite thing about MO2.)

<font size=2>* There are also flags to remind you to endorse mods and to show the tracking status. The tracking feature never worked properly for me and the only mods I have not endorsed are my own, so I typically disable both **Endorsement Integration** and **Tracking Integration** in the MO2 settings (Nexus tab). Disable these features or leave them active -- it is up to you.</font size>

<font size=2>** You can also create a set of custom categories (instructions forthcoming).</font size>

<font size=2>*** If your mod order ever gets completely messed up for no apparent reason, it's probably because you (accidentally) clicked a different column. When that happens, just click the **Priorities** column to restore the mod order.</font size>

## MO2 Settings

- Open the **Settings** by clicking the first icon on the right in the toolbar.

![MO2 Open Settings]

### Settings: General

Under **Download List**, I highly recommend checking **Show meta information** and **Compact list**. This will affect the Downloads tab in the right pane of MO2 where all downloaded files will appear. As the list grows, a more compact view with information about the file version and type will become invaluable.

{{< alert color="info" >}}Check out the [default settings](https://i.imgur.com/BW4F4tD.png) versus the [compact settings](https://i.imgur.com/eNnzd6p.png).{{< /alert >}}

### Settings: Themes

While I personally prefer light mode in the majority of my apps and programs, I realise that my opinion is rather unpopular. Under **Style**, you can try out various other themes. If you are looking for a simple dark theme, I recommend the **1809 Dark Mode** option for now. It is similar to the default light theme and will make following along with my screenshots easier.

{{< alert color="warning" >}}Always restart MO2 after changing the theme.{{< /alert >}}

### Settings: Paths (*)

Since we set up MO2 as a portable instance, all file paths to the various directories are currently within the MO2 installation itself: `/%BASE_DIR%/`, the base directory. However, if you are short on disk space, you can move the downloads folder to a different drive. This can even be an HDD although this will slightly slow down the mod installation.

![Downloads Folder]

## MO2 Profiles

Among MO2's many lovely features is the ability to create an indefinite amount of self-contained **profiles**.

Every profile has its own:

- Load order
- Mod order
- Saves (optional)
- INI Files (optional)

### Create New Profile

- Open the MO2 profiles settings by clicking the ID card icon in the **Toolbar**.

![MO2 Profiles Settings]

- Click the **Create** button and enter **The Phoenix Flavour** as the new name.

{{< alert color="info" >}}Whether  **Default Game INI Settings** is checked is irrelevant. We will deal with the INIs later.{{< /alert >}}

- Click **OK** to create your new profile.
- Click on your new profile in the list and check both **Use profile-specific Save Games** and **Use profile-specific Game INI Files**.
- Click **Select** to quickly switch to your new profile.

## MO2 Plugins




---

<font size=4>Continue with [Mod Organizer 2](/manual/setup/mo2/).</font size>