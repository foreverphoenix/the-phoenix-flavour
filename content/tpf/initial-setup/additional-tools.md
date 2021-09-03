---
title: "Additional Tools"
weight: 7
type: docs
description: >
  Setting up additional modding tools.
---

## SSEEdit

* Download [**SSEEdit**](https://www.nexusmods.com/skyrimspecialedition/mods/164/) manually from the Nexus.
* Create a new folder: `Your Modding Folder\Tools\SSEEdit`.
* Open the downloaded archive and extract everything into the new folder.
* Open Mod Organizer 2 and go into the **Executables** settings (Tools >> Executables or CTRL + E).
* Click the tiny blue plus icon to add a new executable and select **Add from file**.
* Navigate to `Your Modding Folder\Tools\SSEEdit` and double-click **SSEEdit.exe**.
* Click **Apply** to save the new executable.

![Add SSEEdit to MO2](/Pictures/tpf/initial-setup/add-sseedit-to-mo2.png)

### SSEEdit Cache Output

Every time a new plugin is loaded into SSEEdit, a refcache file will be generated for it so that the next time it won’t have to processed again: SSEEdit can simply read the cache file, significantly shortening the startup time. Whenever you update SSEEdit, the accumulated refache files will also be wiped (as they should be) and new ones will be generated and stored in the same directory when you next launch SSEEdit without you having to complete any additional steps. 

In order to store the cached files with the program files themselves, we need to add an argument for it:

* Under **Arguments**, enter the following:
  * `-C:"...\Your Modding Folder\Tools\SSEEdit\cache\"`
* Replace the **"…\Your Modding Folder..."** part with the file path on your end. This is what I added:
  * `-C:"F:\Modding\Skyrim SE Mods\Tools\SSEEdit\cache\"`
* Click **Apply** to save. Don't close the window.

> Note that the trailing backslash at the end is required - the file path MUST end on `\cache\`.

### SSEEdit Backups

After editing a plugin in SSEEdit, a backup will automatically be created. With another argument, we can define the location to which these backups will be saved to so that they are out of our way.

- In the **Arguments** line, after the cache argument, press Space once before adding the second command.
- Enter the following line after the first:
  - `-B:"...\Your Modding Folder\Tools\SSEEdit\backups\"`
- Replace the **"…\Your Modding Folder..."** part with the file path on your end. This is what I added:
  - `-B:"F:\Modding\Skyrim SE Mods\Tools\SSEEdit\backups\"`
- Click **Apply** to save. Don't close the window. 

> Again remember that the trailing backslash at the end is required - the file path MUST end on `\backups\`.

![xEdit Arguments](/Pictures/tpf/initial-setup/xedit-arguments.png)

### Disable Warning Window

Upon attempting to edit something for the first time each session, SSEEdit will display a [**warning**](https://tes5edit.github.io/docs/img/EditWarning.jpg) with a 3 second delay before you can close it. However, while the tool has no "undo" button, that does not mean any edits are permanent: They are only applied to the plugin in question if you explicitly save them after closing the tool. For longer sessions, it is advisable to save the plugins you are working on periodically (but this is not something you will need to do during the setup of TPF).

There is a command that you can add in the arguments for SSEEdit in order to disable the warning window. It will speed up the process of making quick edits such as the removal of a few records or flagging a plugin as ESL. I highly recommend adding it in your MO2 instance after the two arguments for backups and cache:

`-IKnowWhatImDoing`

*Screenshot below shows some additional executables that you will not install until later on in the guide.*

![Disable Warning](/Pictures/tpf/initial-setup/xedit-iknowwhatimdoing.png)

### QuickAutoClean

* Click the tiny blue plus icon to add another new executable and select **Add from file**.
* Navigate to `Your Modding Folder\Tools\SSEEdit`and double-click **SSEEditQuickAutoClean.exe**.
* Change the title to something less verbose (like "SSEEdit - Quick Cleaning").
* Under **Arguments**, enter the following:
  * `-DontCache -B:"...\Your Modding Folder\Tools\SSEEdit\backups\"`
* Once again, replace the **"…\Your Modding Folder..."** part with the file path on your end (same as before).
* Click **OK** to save and close the window.

> The **-DontCache** argument will prevent an obscure bug that destroys parts of Apocrypha during the cleaning of Dragonborn.esm.

![Add QuickAutoClean to MO2](/Pictures/tpf/initial-setup/add-qac-to-mo2.png)

## Cathedral Assets Optimizer

Cathedral Assets Optimizer (CAO) by Gk1 is a unified asset processing tool that can be used to extract or create BSAs, optimize assets, compress or resize textures, and more.

### Installation

- Download [**Cathedral Assets Optimizer**](https://www.nexusmods.com/skyrimspecialedition/mods/23316) **5.0.15** manually.
- Create a new folder: `Your Modding Folder\Tools\Cathedral Assets Optimizer`.
- Open the downloaded archive and extract everything into the new folder.
- Follow [these instructions](https://support.microsoft.com/en-us/help/4028485/windows-) to add an exception for CAO to Windows Defender.

You will be using CAO plenty of times during the installation of the guide, so I recommend adding it to your Windows Taskbar for quick access.

### Profiles

Cathedral Assets Optimiser allows you to set up dedicated profiles. I created several profiles for different purposes to be used during the installation of the guide.

- Download the latest version of the [**Cathedral Assets Optimizer - Basic Profiles Pack**](https://www.nexusmods.com/skyrimspecialedition/mods/26092?tab=files) manually from the Nexus.
- Open the downloaded archive.
- Extract all folders to `Your Modding Folder\Tools\Cathedral Assets Optimizer\profiles`.

![CAO Profiles](/Pictures/tpf/initial-setup/cao-profiles.png)

## SSE NIF Optimizer

While the vast majority of SLE meshes can be fixed with Cathedral Assets Optimizer, there are some that will only work properly after running them through the original SSE NIF Optimizer.

* Download [**SSE NIF Optimizer**](https://www.nexusmods.com/skyrimspecialedition/mods/4089) manually from the Nexus.
* Extract the executable into Your Modding Folder. It’s just a single file so no separate directory is required.

---

#### Continue with the [**ESM Cleaning**](/tpf/initial-setup/esm-cleaning/) page.