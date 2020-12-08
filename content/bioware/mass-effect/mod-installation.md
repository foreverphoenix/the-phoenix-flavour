---
title: "Mod Installation"
weight: 3
type: docs
description: >
  Instructions for ME3TMM and ALOT.
---

## Gameplay Mods

Now that ME3MM is properly set up, we can begin with the installation of some mods. For Mass Effect, the order of installation is extremely important so we are going to install any small gameplay-related mods first and finish up with the big texture packs MEUTIM and ALOT. The mods that we are going to install are primarily quality of life improvements and fixes as I prefer my game to be largely vanilla.

### ME1 Recalibrated

*Collection of tweaks and fixes.*

- Open the [ME1 Recalibrated](https://www.nexusmods.com/masseffect/mods/114?tab=files) mod page.
- Download the **ME1 Recalibrated (Mod Manager Installer)** main file (**Manual Download** button).
- Drag and drop the archive into the ME3TMM window.
- Click **Import mods** and wait for the process to be completed.
- Afterwards, select the **ME1** mod library, click on **ME1 Recalibrated** and press **Apply Mod**.
- Leave the options unchanged (**Missions Timings Module** checked, **Save Lock** unchecked) and click **Install**.

![ME1 Recalibrated](/Pictures/bioware/mass-effect-1/me1-recalibrated.png)

### Recommended Mods

The installation for all other mods is exactly the same as for ME1 Recalibrated. Download the specified file from the Nexus page, drag it into ME3TMM, import it, apply it. Go through the list one by one.

- [Faster Elevators](https://www.nexusmods.com/masseffect/mods/69?tab=files) - *speeds up the elevator rides without breaking dialogue scenes*
- [Faster Airlock](https://www.nexusmods.com/masseffect/mods/109?tab=files) - *speeds up Normandy entrance and exit scenes*
- [XP Rescale](https://www.nexusmods.com/masseffect/mods/180?tab=files) - *allows you to reach level 60 comfortably in one playthrough*
  - I recommend selecting the **Default** or **Completionist** options during the installation.
- [Keepers Finders](https://www.nexusmods.com/masseffect/mods/205?tab=files) - *adds markers for the Keepers during the scanning quest*
  - Select the **with ME1-Recalibrated** option during the installation.
- [Vignette Remover](https://www.nexusmods.com/masseffect/mods/104?tab=files) - *removes the vignette effect as well as the overall blue tint*
  - Do not select the **ME1 Controller version** option during the installation.

### Incompatible Mods

- [Same-Gender Romances for ME1](https://www.nexusmods.com/masseffect/mods/80) is not compatible with ME2 and ME3 Recalibrated.
- [Mass Effect Overwritten](https://www.nexusmods.com/masseffect/mods/139) is not compatible with ME1 Recalibrated.
- [Essential Assignments](https://www.nexusmods.com/masseffect/mods/203) is not compatible with Keepers Finders.
- [No Intro Videos](https://www.nexusmods.com/masseffect/mods/8) is obsolete with A Lot Of Videos (installed later).

*The list of incompatible mods is likely much longer; however, these were mods that I found interesting but skipped specifically due to the abovementioned incompatibilities.*

## Better MAKO Controls

Vanilla controls for the MAKO in Mass Effect 1 are notoriously bad. These tweaks should fix them. They are a combination of the edits for the BIOGame.ini suggested on the mod pages for [Mako - Improved Controls Mod](https://www.nexusmods.com/masseffect/mods/59) and [Improved MAKO](https://www.nexusmods.com/masseffect/mods/115).

- Navigate to `C:\Users\Your User Name\Documents\Bioware\Mass Effect\Config`.
- Open the **BIOGame.ini** file in Notepad++.
- Scroll down to the **[Engine.WorldInfo]** section.
- Change the value for **RBPhysicsGravityScaling** to **1.27**.
- Scroll further to the **[BIOC_Base.BioPlayerController]** section.
- Change the value for **m_bUseCameraRelativeInputForVehicle** to **TRUE**.
- Save and close the file.

To prevent your edits from being reverted, set the file to Read Only:

- Right-click the **BIOGame.ini** file in the Windows Explorer and select **Properties**.
- Check the **Read-only** box at the bottom in the **General** tab and click **OK**.

### Better Keybinds

The [Mako - Improved Controls Mod](https://www.nexusmods.com/masseffect/mods/59) also includes a tweaks for the **BIOInput.ini** file for better MAKO keybinds. Since the file needs to be set to Read-Only to prevent edits from being reverted, you will no longer be able to change keybinds after applying the tweaks. This is why I recommended changing other keybinds a few steps earlier.

- Navigate to `C:\Users\Your User Name\Documents\Bioware\Mass Effect\Config`.
- Open the **BIOInput.ini** file in Notepad++.
- There are two lines that need to be replaced. Use the **Find & Replace** function (CTRL + H).
- Copy the lines below and paste them into the respective fields in Notepad++.
- Click **Replace** to replace the original line with the edited one.
- Do this for both lines.

**Find:**

`Bindings=(Name="LeftControl",InputMode=BIO_INPUT_MODE_NONE,Command="ToggleCrouch",Control=False,Shift=False,Alt=False)`

**Replace:**

`Bindings=(Name="LeftControl",InputMode=BIO_INPUT_MODE_NONE,Command="ToggleCrouch | FireVehicleCannon 1 | OnRelease FireVehicleCannon 0",Control=False,Shift=False,Alt=False)`

**Find:**

`Bindings=(Name="RightMouseButton",InputMode=BIO_INPUT_MODE_NONE,Command="ToggleZoom | OnRelease ZoomOff | InGamePropertyEditorLeftTrigger | MiniGame_LeftTrigger | FireVehicleCannon 1 | OnRelease FireVehicleCannon 0 | GuiKey BIOGUI_EVENT_BUTTON_LT | OnRelease GuiKey BIOGUI_EVENT_BUTTON_LT_RELEASE",Control=False,Shift=False,Alt=False)`

**Replace:**

`Bindings=(Name="RightMouseButton",InputMode=BIO_INPUT_MODE_NONE,Command="ToggleZoom | OnRelease ZoomOff | InGamePropertyEditorLeftTrigger | MiniGame_LeftTrigger | ToggleVehicleZoom | OnRelease VehicleZoomOff | GuiKey BIOGUI_EVENT_BUTTON_LT | OnRelease GuiKey BIOGUI_EVENT_BUTTON_LT_RELEASE",Control=False,Shift=False,Alt=False)`

> If a line cannot be found, it means you edited Toggle Crouch and/or Toggle Zoom when changing key binds earlier. There was an explicit warning not to do this. To fix this, close the INI file, go back ingame to the Controls settings, reset to default, and tweak any keybinds OTHER than Toggle Crouch / Toggle Zoom. Apply your changes, quit the game, and you should be able to find and replace the lines above.

**Do not close the INI file after applying the edits.**

![Mako Controls](/Pictures/bioware/mass-effect-1/mako-controls.png)

## Unlocking Levels 51-60

The Mass Effect 1 level cap is 60; however, levels 51-60 are only unlocked after completing the game at least once (Medal of Honor achievement). In your first playthrough you will no longer advance after level 50.

A quick method to circumvent this requirement is to use the console and unlock the achievement that way. **This step is completely optional.** If you don't want to "cheat" the level cap, you can skip this.

Note that by default, you *cannot* reach level 60 in a single playthrough, even after unlocking the achievement. Thankfully, there is **XP Rescale**, a mod that we already installed earlier which rebalances the XP gain throughout the game, thereby making it possible to achieve the highest level within a single playthrough.

### Enabling the Console

The ingame console is mostly useful for those who never played the game before. By enabling the Medal of Honor achievement (normally granted upon completing a playthrough), you'll unlock levels 51-60 which you can achieve within a single playthrough thanks to **XP Rescale**, a mod that we already installed. 

- Within the **BIOInput.ini** file, find the **[Engine.Console]** section.
- Below the two existing lines, add the following:

```
ConsoleKey=Tilde
TypeKey=Tab
```

> Pressing TAB will open a small, one-line console while TILDE will open a large version. Note that the tilde key's placement varies on different keyboard layouts and may not work properly. You can change the keybinds if you like.

- Save your changes and close **BIOInput.ini**.
- Right-click **BIOInput.ini** in the Windows Explorer and select **Properties**.
- Check the **Read-only** box at the bottom in the **General** tab and click **OK**.

*Source for the instructions was the excellent [Mass Effect Wiki](https://masseffect.fandom.com/wiki/PC_Tweaks#Enabling_The_Console).*

![Enable Console](/Pictures/bioware/mass-effect-1/enable-console.png)

### Medal of Honor Achievement

- Launch **Mass Effect 1** (through ME3TMM, Steam, or Origin).
- In the main menu, press **TAB** to open the small console.
- Type `unlockachievement 1` and press Enter.

Nothing visible will happen but if you check **Options** >> **Achievements**, you will see that **Medal of Honor** and thus levels 51-60 are now unlocked. Achievements are unlocked and saved globally within the `Profile.MassEffectProfile` file located in the Saves directory.

![Unlock MoH](/Pictures/bioware/mass-effect-1/unlock-moh.png)

## Black Blobs Fix

> Skip this step if you own an Intel CPU. This is only required for AMD CPU users.

With recent AMD CPUs (2010 or later), there is a [render bug](https://imgur.com/a/6ROJ4vC) in Mass Effect 1 where characters appear as black pixellated blobs. This was researched extensively and eventually fixed. You can find all the details [here](https://cookieplmonster.github.io/2020/07/19/silentpatch-mass-effect/).

Shadow's plugin patch only fixes Ryzen CPUs. AMD FX / Bulldozer chips are still affected; however, there is another fix that should work for them. **ONLY INSTALL ONE OF THE FIXES**.

### For AMD Ryzen CPUs

- Download the fix [here](https://cookieplmonster.github.io/mods/mass-effect/#silentpatch) (click **Download**).
- Open the downloaded archive and extract the **Binaries** folder into your Mass Effect 1 folder.
- Click **Yes** when asked to merge folders.

### For AMD FX / Bulldozer CPUs

- Download the [Black Blobs Fix for AMD CPU Users](https://www.nexusmods.com/masseffect/mods/181) from the Nexus.
- Import and install it as usual with ME3TMM.

## Graphical Mods

Due to the way that Mass Effect mods work, we need to install graphical mods (texture packs) last. Afterwards it is not possible to install any more gameplay mods as that would break the game.

### A Lot of Textures

ALOT is not only a texture pack, it is also an installer to make multiple graphical mods work together. Its texture pack module is the base which can then be expanded with the Improved Static Lighting module, ALOV which remakes all cutscenes in 4K 60FPS, and the mod MEUITM, another texture pack.

- Open the [A Lot Of Textures (ALOT) for ME1](https://www.nexusmods.com/masseffect/mods/83?tab=files) mod page.
- Download the **ALOT for ME1 12.0** main file.
- Download the **Improved Static Lighting for ME1** optional file.
- Extract the downloaded archive *from the main file* to `Your Modding Folder\Tools\ALOT`.
- Move the download archive for the *optional file* to `Your Modding Folder\Mass Effect 1\Mods`.

> These files are very large. It may be easier to use the provided Torrent versions, especially for people without Nexus Premium.

### MEUITM

- Open the [MEUITM](https://www.nexusmods.com/masseffect/mods/1?tab=files) mod page.
- Download the **MEUITM Anniversary Edition Direct Download** main file.
- Move the archive to `Your Modding Folder\Mass Effect 1\Mods`.

> Using the Torrent download may be faster if you don't have Nexus Premium.

### A Lot of Videos

ALOV is a full remake of all cutscenes in 1080p 60FPS or 2160p 60FPS quality. Please note that the 4K version may come with a performance hit so it is advisable to download the 1080p when playing on a weaker PC.

- Open the [A Lot Of Videos (ALOV) for ME1](https://www.nexusmods.com/masseffect/mods/144?tab=files) mod page.
- Download *either* the **ALOV for ME1 - v2.5 (1080p)** *or* the **ALOV for ME1 - v2.5 (4K)** main file.
- Download the **ALOV for ME1 - ALOT Addon** miscellaneous file.
- Move both downloaded archives to `Your Modding Folder\Mass Effect 1\Mods`.

> Using the Torrent download may be faster if you don't have Nexus Premium.

## ALOT Installer

Now that all relevant files have been downloaded, it is time to install them with ALOT.

- Navigate to `Your Modding Folder\Tools\ALOT` and double-click **ALOTInstaller.exe**.
- If prompted with an update, click **Update** and wait for the process to complete.
- Click **Import assistant** > **Select files to import**.
- Navigate to `Your Modding Folder\Mass Effect 1\Mods` and double-click the **Improved Static Lighting** archive.
- Wait for the ALOT installer to import the mod. Click **Close import assistant** once it's done.

![Improved Static Lighting Imported](/Pictures/bioware/mass-effect-1/improved-static-lighting-imported.png)

### MEUITM and ALOV

Repeat the process detailed above for MEUITM and ALOV for ME1 (1080p or 4K) archives.

### ALOV ALOT Addon

For the ALOV ALOT addon, we will need to use a different method.

- Open the ALOT **Import assistant** and click on **Add files**.
- Navigate to `Your Modding Folder\Mass Effect 1\Mods` and double-click the ALOV ALOT Addon archive.
- Click the **Mass Effect 1** logo to set ME1 as the target game.
- Adding this will only take a second. Click **Close import assistant** once it's done.

## Texture Installation

- Click **Install Textures**, the button in the bottom right corner.
- If you have other ME games installed, you may be asked to select one (Mass Effect 1).
- All options and mods should be enabled by default.
- Feel free to toggle off 4K Texture LODs if you are concerned over performance.
- Click **Begin Installation** once you're ready.
- Configure the available options for **MEUITM**:
  - Asari Face Style **Smooth** ([comparison](https://staticdelivery.nexusmods.com/mods/237/images/1/1-1517990254-647389271.jpeg))
  - Eyes Style **Vanilla** ([comparison](https://staticdelivery.nexusmods.com/mods/237/images/1/1-1517990258-1795931327.jpeg))
  - FemShep Style **CDAMJC Cut** ([comparison](https://staticdelivery.nexusmods.com/mods/237/images/1/1-1517990262-1447692486.jpeg))
  - N7 Armor Style **Vanilla** ([comparison](https://staticdelivery.nexusmods.com/mods/237/images/1/1-1517990245-1076966496.jpeg))
  - Tali Mask Style **Hidden Face** ([comparison](https://staticdelivery.nexusmods.com/mods/237/images/1/1-1517990247-364098756.jpeg))
  - Turian Armor Style **Without C-SEC logo** ([comparison](https://staticdelivery.nexusmods.com/mods/237/images/1/1-1517990262-1828996591.jpeg))
  - Wrex Style **Battle hardened** ([comparison](https://staticdelivery.nexusmods.com/mods/237/images/1/1-1517990253-904168708.jpeg))
  - MEUITM Splash Screen **Don't install**
  - MEUITM ReShade **Don't install**
  - Soft Shadows **Don't install**
- Click **Install with selected options** to proceed.
- Click **I understand, install** when the warning window pops up. This is the point of no return.

The remainder of the installation procedure will now run automatically. This will take a while.

When it's done, click **Continue** and close the ALOT installer.

![ALOT Success](/Pictures/bioware/mass-effect-1/alot-success.png)

## Starting the game

At this point you're all done! Feel free to dive into the game and enjoy the fantastic work of these mod authors, especially the ALOT + ALOV teams who truly delivered a remaster already and make this game feel much younger than it actually is.

You can launch the game either through ME3TMM or Steam/Origin. If you have the Steam version, you may encounter an error when attempting to start the game through ME3TMM (I did) which can potentially be fixed by installing PhysX legacy files or changing the game directory to the default one. The easiest solution is to simply launch it through Steam to begin with. After installing all mods, you don't actually need ME3TMM anymore.