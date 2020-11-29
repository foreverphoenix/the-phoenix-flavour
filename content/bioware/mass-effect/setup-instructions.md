---
title: "Setup Instructions"
weight: 2
type: docs
description: >
  Game installation and configuration.
---

## Game Installation

The first thing you need to do is make sure you have a 100% vanilla copy of the game installed. If the game is already installed but has never been modded, you are good to go. If you did mod the game previously and wish to start over with this guide, I recommend uninstalling it through Steam or Origins, then manually removing any remaining files from the game folder.

If you have to (re)install the game, **make sure to launch it once** after it is downloaded. This will complete the installation and set up registry keys required later on. You can quit from the main menu. *This is definitely required for the Steam version, I'm not sure about Origins.*

I recommend adding a **shortcut** to the Mass Effect folder to your modding folder.

> Although the game is quite old, installing Mass Effect on an SSD is recommended. The game loads sounds and textures at the same time which may cause audio to cut off during dialogue when high resolution textures are installed. A fast hard drive should eliminate that problem ([source](https://www.nexusmods.com/masseffect/mods/83)).

## Mass Effect DLC

> Skip this step if you own the game on Origins. It is only required for Steam users.

There are two DLC packs for Mass Effect 1, [Bring Down the Sky](https://masseffect.fandom.com/wiki/Bring_Down_the_Sky) and [Pinnacle Station](https://masseffect.fandom.com/wiki/Pinnacle_Station). Unfortunately, neither of them are included with the Steam download and must be installed separately ([source](https://steamcommunity.com/sharedfiles/filedetails/?id=519913125)).

- Open the download page for [classic EA games DLC](https://help.ea.com/en-us/help/faq/dlc-for-classic-games/).
- Scroll down to and expand the **Mass Effect** section.
- Download the files marked in the screenshot below.
- Move the downloaded executables to `Your Modding Folder\Mass Effect 1\Official DLC`.

![DLC Download](/Pictures/bioware/mass-effect-1/download-dlc.png)

### DLC Installation

Double-click the executables and follow the installation instructions. If they fail to automatically detect your Mass Effect 1 installation, you probably forgot to launch the game at least once after downloading it.

Should you be asked for a product key during the installation of **Pinnacle Station**, enter the following code: `5GUCXRFPQNBMTJBD3L5J`. You can simply copy and paste.

![DLC Download](/Pictures/bioware/mass-effect-1/pinnacle-station-code.png)

## Origins Tweaks

> Skip this step if you own the game on Steam. It is only required for Origins users.

For the Origins version of Mass Effect 1, you need to adjust some settings in the Origins app.

### Disable Client Updates

Automatic game updates must be disabled in Origins as the app would otherwise delete mod-added files upon launch.

- Open Origins and navigate to **Origins** >> **Application Settings**.
- Scroll down to the **Client update** section and disable **Automatic game updates**.

![Origins Disable Game Updates](/Pictures/bioware/mass-effect-1/origins-disable-game-updates.png)

### Disable Origins Overlay

The Origins overlay can cause severe performance issues which is why it is recommended to turn it off ([source](https://www.nexusmods.com/masseffect/mods/83)).

- Right-click **Mass Effect** in your Origins games library and select **Game Properties**.
- Uncheck the **Enable Origin In Game for Mass Effect** option and click **Save**.

![Origins Disable Overlay](/Pictures/bioware/mass-effect-1/origins-disable-overlay.png)

## Game Backup

The mod manager that we will be installing in a moment requires a full backup of the vanilla game. Having an untouched copy of the game available is also very helpful in case something goes wrong during the installation of any mods.

- Navigate to your Steam/Origins Mass Effect 1 installation folder.
- Copy everything from that folder (around 10GB after the installation of the DLC).
- Paste everything to `Your Modding Folder\Mass Effect 1\Vanilla Game Backup`.

![Mass Effect Backup](/Pictures/bioware/mass-effect-1/mass-effect-backup.png)

### Config Files Backup

Since we are going to edit the game's configuration files later on, it is highly recommended to back them up now so that you can revert to vanilla at any time.

- Navigate to `C:\Users\Your User Name\Documents\Bioware\Mass Effect\Config`.
- Copy all INI files within that folder.
- Paste the INI files to `Your Modding Folder\Mass Effect 1\Config Files Backup`.

## ME Configuration Utility

While the mod ALOT is going to automatically apply several INI tweaks, there are some settings you should tweak now.

- Navigate to your Mass Effect 1 installation (`steam\steamapps\common\Mass Effect`).
- Open the **Binaries** folder and double-click the **MassEffectConfig.exe** inside.
- Click on **Video**.

### Monitor Setting

For this part, you need to be aware of your monitor's aspect ratio and resolution. The majority of monitors nowadays have an aspect ratio of 16:9 with a resolution of **1080p** (1920x1080) or **1440p** (2560x1440) but there are also other options are available.

> The configuration tool does not offer a **2160p** (3840×2160) option. It should be possible to play Mass Effect 1 at 4K but I am not aware of any way to do so and do not own a 4K monitor to figure it out.

- Change the **Aspect Ratio** to match your monitor.
- Change the **Resolution** to match your monitor.

### Vertical Synchronisation

VSYNC is a technique that syncs frames to your monitor's refresh rate (hence the name) and thus prevent screentearing. It will also cap the frame rate to your monitor's refresh rate. Unless your monitor supports G-Sync or FreeSync, you should check the VSYNC box.

### Other Settings

Feel free to crank up the remaining graphical settings. You should be able to set all to maximum unless you have very old hardware.

- Set **Particle Effects** to **High**.
- Set **Texture Detail** to **Ultra High**.
- Set **Filtering Mode** to **Anisotropic**.
- Enable **Dynamic Shadows**.

### Save Changes

- Close the window.
- Click **Yes** when prompted to save your changes.

![Config Save](/Pictures/bioware/mass-effect-1/config-save.png)

## NVIDIA Profile Inspector

> Skip this step if you have an AMD GPU. An NVIDIA GPU is required for the tool.

Instructions were adapted from [this excellent guide](https://gist.github.com/starkgate/70b8ee9e45f49d9576451aaee3dae053#file-nvidia-md).

- Open the Github release page for the [NVIDIA Profile Inspector](https://github.com/Orbmu2k/nvidiaProfileInspector/releases).
- Under the latest release, expand the **Assets** section and click on the **nvidiaProfileInspector.zip** to download the tool.
- Extract the archive to `Your Modding Folder\NVIDIA Profile Inspector`.

### Antialiasing

- Double-click **nvidiaProfileInspector.exe** to start the tool.
- In the **Profiles** drop-down near the top, select **Mass Effect** (you can type to find it faster).

Change the following settings:

- Under **Compatibility**, set **Antialiasing compatibility** to `0x080100C5 (Mass Effect 2, Mass Effect 3)`.
- Under **Antialiasing**, set **Antialiasing - Mode** to `Override any application setting`.
- Under **Antialiasing**, set **Antialiasing - Settings** to `4x [4x Multisampling]`.
- Under **Antialiasing**, set **Antialiasing - Transparency Multisampling** to `Enabled`.
- Under **Antialiasing**, set **Antialiasing - Transparency Supersampling** to `Off / Multisampling`.

Click **Apply Changes** and close the tool.

> Ambient occlusion can apparently cause [visual glitches](https://imgur.com/a/wfcgMiy) and is not recommended for regular gameplay.

![NVIDIA Profile Inspector](/Pictures/bioware/mass-effect-1/nvidia-profile-inspector.png)

## Keybind Tweaks

After editing the BIOInput.ini file later on, you will no longer be able to adjust keybinds as the file will be set to Read-only to prevent the edits from being reverted. Thus, I recommend starting up the game now and applying any keybind changes you want.

> This is completely optional. If you are happy with vanilla keybinds, feel free to skip this step.

- Launch Mass Effect 1 through Steam. It should now run with the previously configured monitor resolutionö
- Go to **Options** >> **Settings** >> **Controls**.
- Change any keybinds you wish.

These are my personal changes:

- Interact to **F**
- Quick Save to **F5**
- Change Zoom Level to **F**
- First Aid to **E**

> Do **not** change the keybinds for Toggle Crouch or Toggle Zoom. This would make instructions later on more complicated.

Afterwards click **Apply**, return to the main menu, and quit the game.

## ME3Tweaks Mod Manager

Mgamerz's ME3Tweaks Mod Manager is compatible with all three Mass Effect games and still being updated in 2020. We are going to use it to install a number of gameplay-related mods.

The name will be abbreviated with **ME3TMM** from now on as it is otherwise quite a mouthful.

- Download the latest version of the [ME3Tweaks Mod Manager](https://www.nexusmods.com/masseffect/mods/149?tab=files) from the Nexus page.
- Run the downloaded EXE file.
- Point the extractor to `Your Modding Folder\Tools` and click **OK**.

### Configuration

- A new explorer window with the extracted file will pop up.
- Double-click **AME3TweaksModManager.exe** to launch it.
- In the settings pop-up, select your preferred language and theme.
- Don't change the **Mod library location** for now.
- Click on **Authenticate to NexusMods** to link ME3TMM to your Nexus account.
- You will be redirected to a new browser window.
- Make sure you are logged in on the correct Nexus account and click **Authorise**.
- Back in ME3TMM click **Close** to exit out of the initial config window.

After clicking **Close**, a tutorial window will pop up. Feel free to click through it to familiarise yourself with the tool and its UI.

![ME3Tweaks Config](/Pictures/bioware/mass-effect-1/me3tweaks-config.png)

### ME1 Backup

- ME3MM will throw a warning about a missing backup for Mass Effect 1.
- Click **Open Backup Manager** and click the drop-down for **Mass Effect**.
- Select the **Link to an existing backup** option and click **OK**.
- Click **OK** again in the link warning window.
- Navigate to `Your Modding Folder\Mass Effect 1\Vanilla Game Backup\Binaries`.
- Double-click **MassEffect.exe** to confirm the installation as the backup.
- Click **Close** to exit out of the Backup manager.

![ME3Tweaks Backup](/Pictures/bioware/mass-effect-1/me3tweaks-backup.png)