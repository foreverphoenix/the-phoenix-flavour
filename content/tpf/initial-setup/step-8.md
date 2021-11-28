---
title: "Step 8: Additional Tools"
weight: 8
type: docs
description: >
  Setting up additional modding tools.
---

## SSEEdit

SSEEdit is a tool for viewing and editing plugins, and better suited to patching and small tweaks than the Creation Kit would be.

- Download the latest version of [SSEEdit](https://www.nexusmods.com/skyrimspecialedition/mods/164/) manually from the Nexus.
- Open the archive and extract the folder inside to `\Mod Organizer 2\Tools\`.
- In Mod Organizer 2, go into the **Executables** settings (gears icon in the Toolbar).
- Click the tiny blue plus icon to add a new executable and select **Add from file**.
- Navigate to `\Mod Organizer 2\Tools\SSEEdit 4.0.4\` and double-click **SSEEdit.exe**.
- Click **Apply** to save the new executable.

![Add SSEEdit to MO2](/Pictures/tpf/initial-setup/add-sseedit-to-mo2.png)

### Stock Game Folder

SSEEdit will not be able to recognise the Stock Game folder by default, even when run through Mod Organizer 2. We need to define it as the root folder manually by adding the following Argument to the executable settings:

```
-D:"Filepath"
```

Replace **Filepath** with the path to your Stock Game folder. For me that would be:

`-D:"G:\Mod Organizer 2 Instances\Mod Organizer 2 - The Phoenix Flavour\Stock Game\Data"`

![SSEEdit Directory Argument](/Pictures/tpf/initial-setup/sseedit-directory-argument.png)

### SSEEdit Cache Output

Every time a new plugin is loaded into SSEEdit, a refcache file will be generated for it so that the next time it won’t have to processed again: SSEEdit can simply read the cache file, significantly shortening the startup time.

In order to store the cached files with the program files themselves, we need to add an argument for it:

```
-C:"Filepath"
```

Replace **Filepath** with the path to a cache folder within your SSEEdit folder. For me that would be:

`-C:"G:\Mod Organizer 2 Instances\Mod Organizer 2 - The Phoenix Flavour\Tools\SSEEdit 4.0.4\cache\"`

> Note that the trailing backslash at the end is required. The file path MUST end on `\cache\`.

![SSEEdit Cache Argument](/Pictures/tpf/initial-setup/sseedit-cache-argument.png)

### SSEEdit Backups

After editing a plugin in SSEEdit, a backup will automatically be created. With another argument, we can define the location to which these backups will be saved to so that they are out of our way:

```
-B:"Filepath"
```

Replace **Filepath** with the path to a backups folder within your SSEEdit folder. For me that would be:

`-B:"G:\Mod Organizer 2 Instances\Mod Organizer 2 - The Phoenix Flavour\Tools\SSEEdit 4.0.4\backups\"`

> Again remember that the trailing backslash at the end is required. The file path MUST end on `\backups\`.

![SSEEdit Backups Argument](/Pictures/tpf/initial-setup/sseedit-backups-argument.png)

### Disable Warning Window

Upon attempting to edit something for the first time each session, SSEEdit will display a [**warning**](https://tes5edit.github.io/docs/img/EditWarning.jpg) with a 3 second delay before you can close it. However, while the tool has no "undo" button, that does not mean any edits are permanent: They are only applied to the plugin in question if you explicitly save them after closing the tool. For longer sessions, it is advisable to save the plugins you are working on periodically (but this is not something you will need to do during the setup of TPF).

There is a command that you can add in the arguments for SSEEdit in order to disable the warning window. It will speed up the process of making quick edits such as the removal of a few records or flagging a plugin as ESL. I highly recommend adding it in your MO2 instance after the other arguments:

```
-IKnowWhatImDoing
```

![SSEEdit Expert Argument](/Pictures/tpf/initial-setup/sseedit-expert-argument.png)

**Click APPLY to save your changes so far.**

## SSEEdit QuickAutoClean

The SSEEditQuickAutoClean executable is included with SSEEdit and can perform some general clean-up tasks on plugins such as undeleting records and marking them as Initially Disabled instead. This saves some time over doing it manually.

- Add the **SSEEditQuickAutoClean.exe** as an executable to Mod Organizer 2 like you did with the main SSEEdit.exe before.

The following arguments are required to define the game and backups folders as well as disable caching:

```
-D:"Filepath" -B:"Filepath" -DontCache
```

For me this would be:

`-D:"G:\Mod Organizer 2 Instances\Mod Organizer 2 - The Phoenix Flavour\Stock Game\Data" -B:"G:\Mod Organizer 2 Instances\Mod Organizer 2 - The Phoenix Flavour\Tools\SSEEdit 4.0.4\backups\" -DontCache`

![SSEEdit QAC Arguments](/Pictures/tpf/initial-setup/sseedit-qac-arguments.png)

**Click APPLY to save your changes and close the EXECUTABLES window.**

## Cathedral Assets Optimizer

Cathedral Assets Optimizer (CAO) by Gk1 is a unified asset processing tool that can be used to extract or create BSAs, optimize assets, compress or resize textures, and more.

- Download the latest version of [Cathedral Assets Optimizer](https://www.nexusmods.com/skyrimspecialedition/mods/23316) manually.
- Extract the archive to a new **Cathedral Assets Optimizer** folder in `\Mod Organizer 2\Tools\`.
- Follow [these instructions](https://support.microsoft.com/en-us/help/4028485/windows-) to add an exception for CAO to Windows Defender.

You will be using CAO plenty of times during the installation of the guide, so I recommend adding it to your Windows Taskbar for quick access.

### TPF Profiles

Cathedral Assets Optimiser allows you to set up dedicated profiles. I created several profiles for different purposes to be used during the installation of the guide.

- Download the latest version of the [Cathedral Assets Optimizer - Basic Profiles Pack](https://www.nexusmods.com/skyrimspecialedition/mods/26092?tab=files) manually from the Nexus.
- Open the downloaded archive and extract all folders to `\Mod Organizer 2\Tools\Cathedral Assets Optimizer\profiles\`.

![CAO Profiles](/Pictures/tpf/initial-setup/cao-profiles.png)

## SSE NIF Optimizer

While the vast majority of SLE meshes can be fixed with Cathedral Assets Optimizer, there are some that will only work properly after running them through the original SSE NIF Optimizer.

- Download [SSE NIF Optimizer](https://www.nexusmods.com/skyrimspecialedition/mods/4089) manually from the Nexus.
- Extract the archive to a new **SSE NIF Optimizer** folder in `\Mod Organizer 2\Tools\`.

## NifSkope

NifSkope is a great tool that allows you to quickly edit meshes in various ways (although not create new ones).

- Download [NifSkope](https://github.com/niftools/nifskope/releases/tag/v2.0.dev7) from Github (scroll down to **Assets** and click the archive).
- Create a new folder: `\Your Modding Folder\Tools\NifSkope\`.
- Open the downloaded archive and extract its contents into the new folder.

In Mod Organizer 2, add **NifSkope.exe** as an executable like you did before with SSEEdit. No additional arguments are required.

![Download NifSkope](/Pictures/tpf/initial-setup/download-nifskope.png)

---

#### Continue with the [Mod Installation](/tpf/mod-installation-1/) page.