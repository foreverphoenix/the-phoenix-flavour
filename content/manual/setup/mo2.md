---
title: "Mod Organizer 2"
weight: 3
type: docs
description: >
  In this step, we will install and configure Mod Organizer 2, set up a custom profile, and add a few useful MO2 plugins.
---

## Why Mod Organizer 2?

{{< alert color="info" >}}If you are already familiar with Mod Organizer 2 and its virtual file system, feel free to skip ahead to [the next section](/manual/setup/mo2/#mo2-installation).{{< /alert >}}

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

![Download MO2](/Pictures/manual/setup/mo2/download-mo2.png)

### Installer Configuration

Now we can run the installer.

- Save the downloaded executable to a convenient location and double-click it.
- If there is a Windows warning, click **More Info** and **Run anyway**.*
- In the MO2 installer, accept the license agreement and proceed to the next page.

<font size=2>\* All files uploaded to the Nexus (barring those that are too big in size) are automatically run through [VirusTotal](https://www.virustotal.com/gui/home/upload). You can view the report by clicking the checkmark next to the mod name ([screenshot](/Pictures/manual/nexus-virus-check.png)).</font size>

You will be asked where to install Mod Organizer 2. There are two things you need to keep in mind when selecting a location:

- It is highly recommended to install MO2 **on the same harddrive as the game**.
- That harddrive should ideally be an **SSD** to improve load times and in-game performance. However, be aware that all your mods will be contained within the MO2 folder. TPF currently requires a total of <mark>placeholder GB</mark> of disk space, so the drive you select with need at least that much free space (plus the recommended ~10-20% that should be kept empty).*
- Do <u>not</u> install MO2 into a UAC-protected folder such as `C:\Program Files\`.

<font size=2>\* By default, all downloads will likewise be kept inside the MO2 directory, requiring space equal to ~80% of the size of all mods. However, the downloads folder can be moved to a different drive if diskspace is a concern (instructions follow later on this page).</font size>

- Select a suitable folder as the installation directory and proceed.

![MO2 Directory](/Pictures/manual/setup/mo2/mo2-directory.png)

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

![MO2 Instance](/Pictures/manual/setup/mo2/mo2-instance.png)

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

{{< alert color="info" >}}You will also see all Creation Club files that you own in MO2. They will be dealt with shortly.{{< /alert >}}

![MO2 UI Overview](/Pictures/manual/setup/mo2/mo2-ui-overview.png)

## Interface Adjustments

I always make some minor modifications to the MO2 interface and I do recommend you follow along with this step.

### MO2 Log

First, I disable the log at the bottom. I have never needed it and it takes up space.

- Open the **View** menu and unselect **Log**.

![Disable MO2 Log](/Pictures/manual/setup/mo2/disable-mo2-log.png)

### Right Pane

The <mark>right pane</mark> of Mod Organizer 2 features a number of tabs, none of which require much space to properly display. I typically reduce the right pane to take up about a fourth of the window. Leave the columns in the **Plugins** tab be for now -- we will install a plugin that adds more columns in a little bit.

- Adjust the proportions of the two panes so that the right pane takes up between a third and a fourth of the window.

### Left Pane

The <mark>left pane</mark> of Mod Organizer 2 represents the **mod order**. This is where all your mods will show up.

- Right-click the columns at the top to configure which columns are displayed.
- I recommend enabling all columns marked with a ✔️ in the list below and matching their order as well (you can drag-and-drop columns to sort them).

The **Notes** column is optional. I keep it quite small and use it as a custom field to mark whether a mod is `modified` or `custom` but this is probably not very useful if you are just following the guide. You can always re-enable the column later if you decide to take notes.

![Mod Order Columns](/Pictures/manual/setup/mo2/mod-order-columns.png)

- ✔️**Conflicts:** Displays little icons to show overwrites.
- ✔️**Flags:** Not necessary but recommended. Shows if notes are appended to a mod.*
- ✔️**Content:** Very helpful because it shows you which types of assets are contained in a mod.
- ❌**Category:** Uses Nexus categories by default. Separators are better for sorting.**
- ❌**Nexus ID:** The ID of the respective mod (which is the combination of numbers at the end of its URL).
- ❌**Source Game:** Somewhat useful when mixing Skyrim LE and Skyrim SE mods which is not very common anymore.
- ✔️**Version:** Mostly helpful for tracking updates.
- ❌**Installation:** Displays the date of installation. Not sure what you would need this for.
- ✔️**Priority:** Shows the position in the mod order. This is what the left pane should always be sorted by.***
- ❌**Notes:** See short notes at a glance.

<font size=2>* There are also flags to remind you to endorse mods and to show the tracking status. The tracking feature never worked properly for me and the only mods I have not endorsed are my own, so I typically disable both **Endorsement Integration** and **Tracking Integration** in the MO2 settings (Nexus tab). Disable these features or leave them active -- it is up to you.</font size>

<font size=2>** You can also create a set of custom categories (instructions forthcoming).</font size>

<font size=2>*** If your mod order ever gets completely messed up for no apparent reason, it's probably because you (accidentally) clicked a different column. When that happens, just click the **Priorities** column to restore the mod order.</font size>

## MO2 Settings

Next, we are going to modify a few settings. All recommended changes in this step are optional.

- Open the **Settings** by clicking the first icon on the right in the toolbar.

![MO2 Open Settings](/Pictures/manual/setup/mo2/mo2-open-settings.png)

### Settings: General (*)

Under **Download List**, I highly recommend checking **Show meta information** and **Compact list**. This will affect the Downloads tab in the right pane of MO2 where all downloaded files will appear. As the list grows, a more compact view with information about the file version and type will become invaluable.

{{< alert color="info" >}}Check out the [default settings](https://i.imgur.com/BW4F4tD.png) versus the [compact settings](https://i.imgur.com/eNnzd6p.png).{{< /alert >}}

### Settings: Themes (*)

While I personally prefer light mode in the majority of my apps and programs, I realise that my opinion is rather unpopular. Under **Style**, you can try out various other themes. If you are looking for a simple dark theme, I recommend the **1809 Dark Mode** option for now. It is similar to the default light theme and will make following along with my screenshots easier.

{{< alert color="warning" >}}Always restart MO2 after changing the theme.{{< /alert >}}

### Settings: Mod List (*)

By default, the left pane in MO2 is cluttered with the various creations. There are several ways in which we can deal with them, including copying them over into MO2 to be managed as mods (because that is fundamentally what they are). However, I prefer to treat the creations like the official master files and leave them untouched in the **data folder**.

To remove a bit of clutter, I then hide external mods in MO2. Since we will not ever install files into the actual data folder, this will merely remove the official master files and creations from the MO2 UI. Alternatively, you could move those files under their own separator (we will discuss the creation of separators later on). 

![Hide external mods](/Pictures/manual/setup/mo2/hide-external-mods.png)

### Settings: Paths (*)

Since we set up MO2 as a portable instance, all file paths to the various directories are currently within the MO2 installation itself: `/%BASE_DIR%/`, the base directory. This includes the **downloads** folder which will contain all downloaded mod archives.

If you are short on disk space, you can move this folder to a different drive. This can even be an HDD although installing mods from an HDD will be slightly slower.

![Downloads Folder](/Pictures/manual/setup/mo2/downloads-folder.png)

### Settings: Workarounds (*)

Optionally, you can enable archive parsing. This will allow MO2 to read the contents of BSA files and show file conflicts between loose and packed files. While archive parsing can slow down MO2, the impact is not too noticeable.

If you are just following the guide, you won't need to worry about asset conflicts and can leave this setting disabled.

- Check the box for **Enable archives parsing (experimental)**.

![Archive Parsing](/Pictures/manual/setup/mo2/archive-parsing.png)

## MO2 Profiles

Among MO2's many lovely features is the ability to create an indefinite amount of self-contained **profiles**.

Every profile has its own:

- Load order
- Mod order
- Save Files (optional)
- INI Files (optional)

### Create New Profile

- Open the MO2 profiles settings by clicking the ID card icon in the **Toolbar**.

![MO2 Profiles Settings](/Pictures/manual/setup/mo2/mo2-profiles-settings.png)

- Click the **Create** button and enter **The Phoenix Flavour** as the new name.
- Make sure that **Default Game INI Settings** is checked.
- Click **OK** to create your new profile.
- Click on your new profile in the list and check both **Use profile-specific Save Games** and **Use profile-specific Game INI Files**.
- Click **Select** to quickly switch to your new profile.

## MO2 Plugins

While Mod Organizer 2 is already excellent on its own, we can further improve it with third-party extensions. For now, we will install two basic plugins; more will be added later.

{{< alert color="warning" >}}MO2 plugins must always be installed into the  `\Mod Organizer 2\plugins\` folder. When extracting the files, please pay attention to the folder structure in the downloaded archive. If there is already a `\plugins\` folder, open *that* folder and extract its contents.{{< /alert >}}

### MO2 Nexus Downloads Renamer

In June 2026, the Nexus changed how downloaded archives are named. The file names now no longer contain the mod's Nexus ID and version number. Unfortunately, this doesn't work well with Mod Organizer 2 and will cause updated versions of the same mod or different mods with the same file names to overwrite each other in the downloads folder. We will install a plugin that fixes this.

- Download the latest main file from the [mod page](https://www.nexusmods.com/site/mods/1998?tab=files).

{{< alert color="info" >}}This is the first file we are downloading from the [Modding Tools](https://www.nexusmods.com/games/site) section of the Nexus where most MO2 plugins (as well as Vortex extensions and other tools) can be found. It is worth checking on occasion.{{< /alert >}}

- Open the archive and extract its contents to `\Mod Organizer 2\plugins\`.
- Restart Mod Organizer 2.

### Bethesda Plugin Manager

Parapets' [Bethesda Plugin Manager](https://www.nexusmods.com/skyrimspecialedition/mods/111236) adds certain features from the left pane (mod order) to the right pane (load order). This includes the ability to group plugins under separators, view conflicts, and more. We are going to use [Alaxouche's updated version](https://www.nexusmods.com/skyrimspecialedition/mods/175385) of the plugin which expands features from the base plugin (for example, separators can now be coloured) and adds a few features of his own (such as the ability to add notes to plugins).

- Download the **Bethesda Plugin Manager - Extended 2.5.2** main file from the [mod page](https://www.nexusmods.com/skyrimspecialedition/mods/175385?tab=files).
  - *We need this version because it matches the current stable version of Mod Organizer 2 (2.5.2).*
- Open the archive and extract its contents to `\Mod Organizer 2\plugins\`.
- Restart Mod Organizer 2.

### BPM: Columns

As you can see, the **Plugins** tab in the right pane of Mod Organizer 2 now has a few new columns:

- ❌**Conflicts:** Visualises conflicts (overwrites/overwritten) between plugins.
- ✔️**Flags:** Shows whether an INI file or BSA is attached to a plugin, or whether it is flagged as an ESM or ESL.
- ✔️**Mod Index:** The plugin index -- `xx` for ESMs and ESPs, `FE:xxx` for ESLs.
- ✔️**Priority:** Shows the position in the load order. This is what the right pane should always be sorted by.
- ✔️**Notes:** Custom field to add a short note.
- ❌**Records:** The number of records contained in a plugin.

I recommend that you enable the same columns as in the screenshot.

The **Notes** column is very optional. I use it very occasionally to leave myself little reminders when a plugin deviates from my standard load order (mirroring the mod order). If you are simply going to follow the guide and not deviate or continue modifying it afterwards, you do not need to worry about the load order and don't need to take any notes.

![BPM Columns](/Pictures/manual/setup/mo2/bpm-columns.png)

### BPM: Settings (*)

Lastly, I recommend turning off two features in BPM. This is optional.

- Open the Mod Organizer 2 settings by clicking the cross-tools icon above the right pane.
- Switch to the **Plugins** tab and scroll down to **Bethesda Plugin Manager**.
- Turn off either one or both of the following options (details below):
  - `enable_plugin_conflict_management`
  - `enable_sort_button`

**Plugin conflict management** is a major feature of BPM which allows you to preview plugin conflicts directly in MO2, similar to how asset conflicts are visualised in the right pane. Without this feature, conflicts are only visible in the tool SSEEdit. I personally find the visual clutter in the load order more annoying than helpful, so I turn this feature off. You won't need it either if you just follow the guide and make no modifications of your own.

The **Sort button** is intended for the tool LOOT, which sorts the load order based on pre-defined or custom rules. TPF does not use LOOT, so this button is redundant and should not be pressed. Thus, I strongly recommend disabling it.

![BPM Settings](/Pictures/manual/setup/mo2/bpm-settings.png)

---

<font size=4>Continue with [INI Configuration](/manual/setup/ini-config/).</font size>