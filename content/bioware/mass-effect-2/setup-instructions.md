---
title: "Setup Instructions"
weight: 2
type: docs
description: >
  Game installation and configuration.
---

## Game Installation

The first thing you need to do is make sure you have a 100% vanilla copy of the game installed. If the game is already installed but has never been modded, you are good to go. If you did mod the game previously and wish to start over with this guide, I recommend uninstalling it through Steam or Origin, then manually removing any remaining files from the game folder.

I recommend adding a **shortcut** to the Mass Effect 2 folder to your modding folder.

## Mass Effect 2 DLC

Mass Effect 2 has rather a lot more DLC than the first game did (there's a list [on the fan wiki](https://masseffect.fandom.com/wiki/Downloadable_Content)) and they are not so easy to acquire. While the installers can be downloaded for free from the [EA website](https://help.ea.com/en-us/help/faq/dlc-for-classic-games/#masseffect), there have been reports that installing them does not automatically unlock them. Additionally, there are also a number of different versions of the game on Origin and Steam, making it difficult to figure out how to get all DLC.

As far as I can tell, this is the difference between the versions:

- **Origin:** Currently available are the Standard Edition and the DLC Pack. Buying both will get you all DLC. Origin keys for the N7 Deluxe Edition are also rather cheaply available from other stores; however, that version doesn't seem to include all DLC.
- **Steam:** Currently available are the Standard Edition and the N7 Digital Deluxe Edition. The latter does not appear to include all DLC; however, it comes with extra keys for Origin (N7 Deluxe Edition, Promo, Cerberus) which will unlock the game with all DLC on Origin. Your Steam installation will be detected and downloading the DLC through Origin will install them alongside it.

So what does all that mean? The easiest method to get the game with all DLC is buying Mass Effect 2 and the Mass Effect 2 DLC Pack on Origin. If you are a Steam collector (like me) and willing to (re)buy the games on Steam to play them there (like I did), you can use Origin to unlock all DLC by activating keys provided after purchasing the N7 Digital Deluxe Edition on Steam.

There is also a "ME2 DLC Unlocker" which you can probably find with a quick Google search. Apparently it's going to quickly unlock the DLC for your Steam copy. Might not be terribly legal though. There is more information [here](https://steamcommunity.com/sharedfiles/filedetails/?id=866343696), be sure to check the comments section as well.

## DLC for Steam

Quick note: I bought the Mass Effect trilogy in a store, boxed, a LONG time ago. Apparently it contained keys for the regular editions and some but not all DLC. As far as I can tell, entering the keys from Steam unlocked the missing DLC as well as the Digital Deluxe Edition as a separate game in my Origin library. I am assuming that the fact that I already owned some of the DLC was irrelevant but there is no way to know for sure. Suffice it to say that I'm extremely confused and have developed a new hatred for EA's DLC policies.

**Follow the instructions below if you own the game on Steam and want to unlock all DLC.**

### Origin Keys

After buying the Mass Effect 2 N7 Digital Deluxe Edition on Steam, you will be provided with additional keys for Origin. You'll now need an EA account and the Origin app installed locally (although it might work, too, if you activate the keys on the EA website).

- Find **Mass Effect 2** in your Steam library.
- Right-click it or click the cog icon on the game page to open the context menu.
- Go to **Manage** > **CD Keys** and a window will open with the three keys.

![Manage CD Keys Steam](/Pictures/bioware/mass-effect-2/manage-cd-keys-steam.png)

### Key Redemption

The keys can be redeemed on Origin.

- Open the Origin app and go to **My Game Library**.
- Click the **ADD A GAME** button at the top right and select **Redeem Product Code**.
- Copy the three codes from Steam and redeem them here one after the other.
- Select the new **Mass Effect 2 Digital Deluxe Edition** in your library and let it update.
- If it doesn't update automatically, right-click it and select **Update Game**.

Now you should be able to select the game in your Origin library, go to **Extra Content**, and find all DLC unlocked. Now you can simply go through and click **Download** for each of the DLC. The **Cerberus Network** pack was shown as "Unlocked" to me without a Download button so hopefully it is already included with the main game and only needed to be unlocked.

### Verify Game Files

Afterwards, you need to verify the files in Steam as the game won't launch otherwise.

- Return to your Steam library and find Mass Effect 2.
- Right-click the game cover or click the cog icon to open the context menu.
- Select **Properties** and go to **LOCAL FILES**.
- Click **Verify integrity of game files** and wait until it's finished.

![Verify Game Files](/Pictures/bioware/mass-effect-2/verify-game-files.png)

## Origin Tweaks

For the Origin version of Mass Effect 2, you need to adjust some settings in the Origin app. If you have the game on Steam but unlocked it on Origin as well in order to access all DLC, you also need to follow this step.

### Disable Client Updates

Automatic game updates must be disabled in Origin as the app would otherwise delete mod-added files upon launch.

- Open Origin and navigate to **Origins** >> **Application Settings**.
- Scroll down to the **Client update** section and disable **Automatic game updates**.

![Origin Disable Game Updates](/Pictures/bioware/mass-effect-1/origins-disable-game-updates.png)

### Disable Origin Overlay

The Origin overlay can cause severe performance issues which is why it is recommended to turn it off.

- Right-click **Mass Effect 2** in your Origin games library and select **Game Properties**.
- Uncheck the **Enable Origin In Game for Mass Effect 2 Digital Deluxe Edition** option and click **Save**.

*If you own the Standard version, it works the same way but the option will have a different name.*

![Origin Disable Overlay](/Pictures/bioware/mass-effect-2/origin-disable-overlay.png)

## Game Backup

The mod manager that we will be installing in a moment requires a full backup of the vanilla game. Having an untouched copy of the game available is also very helpful in case something goes wrong during the installation of any mods.

- Navigate to your Steam/Origin Mass Effect 2 installation folder.
- Copy everything from that folder (around 19GB after the installation of all DLC).
- Paste everything to `Your Modding Folder\Mass Effect 2\Vanilla Game Backup`.

![Mass Effect Backup](/Pictures/bioware/mass-effect-2/vanilla-game-backup.png)

## ME Configuration Utility

While the mod ALOT is going to automatically apply several INI tweaks, there are some settings you should tweak now.

- Navigate to your Mass Effect 2 installation (`steam\steamapps\common\Mass Effect 2`).
- Open the **Binaries** folder and double-click the **MassEffect2Config.exe** inside.
- In the **Video** tab, I recommend setting the game to **Fullscreen** and **Borderless**.
- Also feel free to crank up / enable the remaining settings (unless your PC is truly ancient).

### Monitor Setting

For this part, you need to be aware of your monitor's aspect ratio and resolution. The majority of monitors nowadays have an aspect ratio of 16:9 with a resolution of **1080p** (1920x1080) or **1440p** (2560x1440) but there are also other options are available.

> The configuration tool does not offer a **2160p** (3840×2160) option. It should be possible to play Mass Effect 2 at 4K but I am not aware of any way to do so and do not own a 4K monitor to figure it out.

- Change the **Aspect Ratio** to match your monitor (eg 16:9).
- Change the **Resolution** to match your monitor (eg 1920x1080).

### Save Changes

- Close the window.
- Click **Yes** when prompted to save your changes.

## NVIDIA Profile Inspector

> Skip this step if you have an AMD GPU. An NVIDIA GPU is required for the tool.

Instructions were adapted from [this excellent guide](https://gist.github.com/starkgate/70b8ee9e45f49d9576451aaee3dae053#file-nvidia-md). You can skip the installation of the Profile Inspector if you followed my ME1 guide during which it was already installed.

- Open the Github release page for the [NVIDIA Profile Inspector](https://github.com/Orbmu2k/nvidiaProfileInspector/releases).
- Under the latest release, expand the **Assets** section and click on the **nvidiaProfileInspector.zip** to download the tool.
- Extract the archive to `Your Modding Folder\NVIDIA Profile Inspector`.
- Double-click **nvidiaProfileInspector.exe** to start the tool.
- In the **Profiles** drop-down near the top, select **Mass Effect 2** (you can type to find it faster).

### Add Executable

The profile in the Inspector tool has not had a specific executable associated with it, causing changes not to apply. The executable has to be added to it manually.

- Once in the **Mass Effect 2** profile, click the **"Add application button to current profile** in the top bar (see screenshot).
- In the window that opens, navigate to your Steam/Origin installation of Mass Effect 2.
- Open the **Binaries** folder, select **ME2Game.exe**, and click **Open** to add it to the profile.

![Add Exe to Profile Inspector](/Pictures/bioware/mass-effect-2/add-exe-profile-inspector.png)

### Profile Settings

Change the following settings:

- Under **Compatibility**, set **Antialiasing compatibily** to `0x080000C1`.
- Under **Antialiasing**, set **Antialiasing - Gamma correction** to `Off`.
- Under **Antialiasing**, set **Antialiasing - Mode** to `Override any application setting`.
- Under **Antialiasing**, set **Antialiasing - Setting** to `4x [4x Multisampling]`.
- Under **Antialiasing**, set **Antialiasing - Transparency Multisampling** to `Disabled`.
- Under **Antialiasing**, set **Antialiasing - Transparency Supersampling** to `4x Sparse Grid Supersampling`.

Click the **Apply Changes** button (top right) and close the tool.

> Ambient occlusion can apparently cause [visual glitches](https://imgur.com/a/wfcgMiy) and is not recommended for regular gameplay.

![NVIDIA Profile Inspector](/Pictures/bioware/mass-effect-1/nvidia-profile-inspector.png)

## ME3Tweaks Mod Manager

Mgamerz's ME3Tweaks Mod Manager is compatible with all three Mass Effect games and still being updated in 2020. We are going to use it to install a number of gameplay-related mods. If you followed my ME1 guide, you already have it installed and can skip ahead to the next step, Configuration.

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

### ME2 Backup

- ME3MM will throw a warning about a missing backup for Mass Effect 2.
- Click **Open Backup Manager** and click the drop-down for **Mass Effect**.
- Select the **Link to an existing backup** option and click **Back up**.
- Click **OK** again in the link warning window.
- Navigate to `Your Modding Folder\Mass Effect 2\Vanilla Game Backup\Binaries`.
- Double-click **MassEffect2.exe** to confirm the installation as the backup.
- Click **Close** to exit out of the Backup manager and close ME3TMM.

![ME3Tweaks Backup](/Pictures/bioware/mass-effect-2/backup-manager.png)

## Test Launch

After all changes we have now applied, please take the time to launch the game once to ensure it's running fine. If it is, feel free to continue with the next step.