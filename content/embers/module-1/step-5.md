---
title: "Step 5: Essential Mods"
weight: 5
type: docs
description: >
  Installing essential mods using Mod Organizer 2.
---

## SSE Engine Fixes

**SSE Engine Fixes** is a collaboration of some of the most talented coders in the community, including aers, Ryan, Nuukem, meh321, and others. It is the definitive solution to many engine-level bugs, all fixed through a single SKSE plugin, but also includes a memory patch that completely changes the way memory allocation works.

The mod is unusual insofar as that it requires an additional plugin, the **SKSE64 Plugin Preloader** by meh321 and sheson, which allows SKSE plugins to load before the game initialises. This plugin is why the mod is split into two main files as it has to be installed into the **root folder** like the Script Extender.

Some of its features include:

- Ability to unlock Steam achievements with mods loaded (no need to install a [separate mod](https://www.nexusmods.com/skyrimspecialedition/mods/245) to enable them).
- Fixed bug that made tree reflections on water look like big black rectangles ([example](https://cdn03.bethesda.net/forum/uploads/cb978428-9cb1-49eb-9081-e5f74279c78d.jpg) and [discussion on Beth.net](https://bethesda.net/community/topic/31372/issue-with-reflections-in-water?language%5B%5D=en)).
- Fixes changes to sound volume sliders added by mods not being saved across game restarts.
- Various crash fixes like the one that would occur on systems in cities with letters not in the English alphabet.
- Fixes and tweaks by [meh321](https://www.nexusmods.com/skyrim/mods/75951), [Cobb](https://www.nexusmods.com/skyrim/mods/96734), and [lStevieAl](https://www.nexusmods.com/skyrim/users/2232669?tab=user+files&BH=0) ported from Skyrim LE.
- Warning if the user's setup approaches the [reference handle cap](https://www.reddit.com/r/skyrimmods/comments/ag4wm7/psa_the_reference_handle_cap_or_diagnosing_one_of/).

### SKSE64 Preloader

Before we grab the main file, we should install the preloader:

- From the [SSE Engine Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/17230?tab=files) mod page, download the **(Part 2)** main file (click the **Manual Download** button).
- Open the downloaded archive and extract all three plugins (DLLs) into your root folder: `\Mod Organizer 2\Stock Game\`.

![SKSE Preloader Installation](/Pictures/embers/module-1/skse-preloader-installation.png)

### SKSE Plugin

With the required preloader in place, we can now install the other main file. Since this one does belong into the **data folder** we can use Mod Organizer 2 as usual.

- On the [SSE Engine Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/17230) mod page, locate the `1.6.xx` version of the **(Part 1)** main file.
- Click the **Mod Manager Download** button.

For mods that have special requirements such as other mods you will usually be notified of those requirements before the file downloads. SSE Engine Fixes obviously requires SKSE and Address Library which we already installed. It also requires the Visual C++ Redists from Microsoft which we also installed in **Step 2** for Mod Organizer 2.

> When downloading mods on your own later on, remember to pay attention to the requirements window. Also note that mod authors do not always enable this function so you should check the mod description for further installation notes and requirements as well.

![SKSE Preloader Installation](/Pictures/embers/module-1/engine-fixes-requirements.png)

- Click the **Download** button again in the **Mod Requirements** window.
- In Mod Organizer 2, find the downloaded file in the **Downloads** tab and double-click it to install.
- The new mod will now appear at the bottom of your mod order. Check the box to activate it.

### Configuration

Like many other SKSE plugins, SSE Engine Fixes can be customised through a configuration file (though it is a [TOML](https://en.wikipedia.org/wiki/TOML) file instead of [INI](https://en.wikipedia.org/wiki/INI_file)).

- In Mod Organizer 2, double-click **SSE Engine Fixes** in your mod order.
- Switch to the **Text Files** tab.

Configuration files for mods will show up in one of two tabs in Mod Organizer 2: Most have the **INI** file extension and will show up in the **INI Files** tab. While MO2 can also read **TOML** files, those will show up in the **Text Files** tab instead. Functionally, this makes no difference, they can be viewed and edited through the MO2 UI just the same, but it may be confusing at first.

- Select the `SKSE\Plugins\EngineFixes.toml` in the list on the left. This is the primary config file for SSE Engine Fixes.

Here you can see a long list of various fixes and tweaks that are part of the mod. Technically, there is no need to change anything right now, the mod works perfectly fine out of the box.

### Example Edits

> **You do not have to make any of these changes,** but do remember the Notes feature in MO2 and try to get into the habit of leaving notes for yourself when you change something. It is easy to forget small tweaks like these.

Here are two tweaks that I personally enable:

**DisableChargenPrecache** prevents slowdowns and crashes in the character creation menu in heavily modded setups. This fix is already included in [RaceMenu](https://www.nexusmods.com/skyrimspecialedition/mods/19080), a very popular UI overhaul of the character creation menu which is also required for the number one skeleton replacer. Almost everyone uses RaceMenu so they do not need to use the precache killer in Engine Fixes. But since I skip RaceMenu in my personal setup, I do enable it.

**SleepWaitTime** speeds up the wait menu. When you press T to wait in vanilla, the hours tick down slowly, and especially for mod testing this can sometimes be a little frustrating.

- In the `[Patches]` section, set `DisableChargenPrecache =` and `SleepWaitTime =` to `true`.
- Press **CTRL + S** to save your changes and close the window.

> When changing anything in mod config files through MO2, always remember to click save or press CTRL+S as changes are not saved automatically and you will not always be prompted to save them upon closing the window.

This is a pretty minor change and of course I can revert it anytime. However, I am forgetful so I also switch to the **Notes** tab in MO2 and leave a quick reminder for myself (see screenshot below). If in the future I should install RaceMenu after all, I will (hopefully) check my notes on SSE Engine Fixes and disable the precache killer again.

Right now you will only see the note if you double-click the mod and check the **Notes** tab. However, we will soon adjust the MO2 interface so you'll be able to see your notes at a glance.

![Engine Fixes Note](/Pictures/embers/module-1/engine-fixes-note.png)

## SSE Display Tweaks

**SSE Display Tweaks** is another game-changer as far as Skyrim mods go. It consolidates all performance and monitor settings in one place in addition to a highly configurable on-screen-display.

It also enables the game to run (mostly) without issues at a framerate exceeding 60FPS. **In vanilla, the physics engine is tied directly to the framerate.** When unlocking it and going above 60FPS, the game would increasingly bug out to the point where it would become completely unplayable. SSE Display Tweaks fixes that.

> It should be noted that some minor bugs may still occur with increasing frequency at higher framerates. These include small physics bugs, such as objects moving for no reason or "spazzing out" and creatures falling from the sky. However, there should be no more gamebreaking issues.

While this is not the time to talk about performance and hardware, you should be aware that modded Skyrim is unforgiving, particularly on high resolutions. Reaching stable 60FPS at resolutions above 1080p but especially at 4K with many visual mods and an ENB preset will require a very solid modern PC.

For the vast majority of users, **capping the frame rate at 60FPS or 72FPS is appropriate**, both to keep physics strangeness to a minimum as well as to ensure that the framerate does not fluctuate too much.

(Since we already installed several mods, the instructions (download, install, activate) will be briefer from now on.)

- Download and install the latest main file of [SSE Display Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/34705?tab=files).

> SSE Display Tweaks is compatible with any version of Skyrim if Address Library for SKSE is present.

### Custom INI

SSE Display Tweaks comes with an extensive configuration file to customise various settings. Normally this configuration file would be overwritten when downloading an update for the mod so you would have to redo any custom edits you made. 

One solution would be to copy the configuration file to a separate mod folder so it overwrites the default one. However, this would require you to check the main config file for changes with every update and be potentially cumbersome to maintain over time.

Thankfully, there is a better solution: SSE Display Tweaks will recognise a **SSEDisplayTweaks_custom.ini**. Any changes added to that custom INI will override the defaults in the main configuration file without affecting anything else.

Let's create this custom INI:

- In Mod Organizer 2, click the **crossed tools** icon above the mod order (see screenshot below).
- Select the **Open Mods folder** option to quickly get to `/Mod Organizer 2/mods/`.

![MO2 Open Folders](/Pictures/embers/module-1/mo2-open-folders.png)

- Create a new mod folder and name it **SSE Display Tweaks - Custom INI**.
- Inside the new mod folder, create two more folders: `/SSE Display Tweaks - Custom INI/SKSE/Plugins/`.
- In the new **Plugins** folder, right-click and select **New** >> **Text Document**.
- Rename the new file to **SSEDisplayTweaks_Custom.ini** (remember to change the file extension).

![Display Tweaks Custom](/Pictures/embers/module-1/display-tweaks-custom.png)

- Close the window and return to Mod Organizer 2.
- Press F5 to refresh the UI and the new mod will show up in your mod order.
- Check the box to activate it.

### Monitor Configuration

SSE Display Fixes has a large amount of configurable options in its INI file, most of which do not need editing. For instance, VSYNC is enabled by default which it always should be (even if you have a G-SYNC or FreeSync monitor).

Let's take a look at the default configuration file:

- Double-click **SSE Display Tweaks** in your mod order and switch to the **INI Files** tab.
- Select the **SSEDisplayTweaks.ini** file.

Relatively near the top, you'll find the `[Render]` section with options to change the display mode. By default, they are commented out (prefixed with a `#`) so the lines will not take effect.

However, Borderless Fullscreen is required to benefit from the DXGI flip model integration (improving performance). It should be noted that this only works on **Windows 10**, so any Windows 7 or 8.1 users are going to want to use exclusive fullscreen instead.

![Display Tweaks Render](/Pictures/embers/module-1/display-tweaks-render.png)

We can change those settings using the **custom INI** we created. Open it through Mod Organizer 2 and add the following lines to it to force Borderless Fullscreen mode:

```
[Render]
Fullscreen=false
Borderless=true
```

> Note that when adding settings to the custom INI, they need to be grouped below the section they are under in the main config file.

Remember to **save** your changes before closing the window.

![Display Tweaks Render](/Pictures/embers/module-1/display-tweaks-monitor.png)

### Resolution

I also recommend using SSE Display Tweaks to set your resolution by adding the following line to the render section and fill in your resolution. A widescreen resolution is also possible though you will need to install some patches later on for UI mods.

```
Resolution=
```

If you have a very high-res monitor (i.e., 4K) you may want to consider running the game at a lower resolution. Skyrim scales badly and even with powerful hardware, it can be a challenge to achieve 60FPS in a heavily modded game at 1440p. With mid-tier hardware I would recommend going no higher than 1440p.

If you set a resolution in the SSE Display Tweaks custom INI that is LOWER than your monitor's native resolution, you also need to add the following line:

```
BorderlessUpscale=true
```

Any performance adjustments such as this one can also be left for later when you have a better idea of what your modded setup runs like.

### FPS Cap

As noted earlier, you can safely increase the framerate limit beyond 60FPS with SSE Display Tweaks installed. By default, the limit is 240FPS. You should, however, be aware that achieving a framerate above 100FPS with a decently modded game requires very good hardware, especially on resolutions above 1080p.

I personally cap at 60FPS regardless as that is enough for me personally. 

If you would like to change the framerate cap (default is 240FPS), you can do so in the **SSEDisplayTweaks_custom.ini** as well by adding the following with `<framerate>` being the value you want to cap at:

```
FramerateLimit=<framerate>
```

![Display Tweaks INI](/Pictures/embers/module-1/display-tweaks-fps.png)

### Documenting Changes

Finally, I added `Enabled borderless fullscreen. Set resolution. Capped at 60FPS.` in the **Notes** tab for the custom INI.

Always make heavy use of the notes feature in Mod Organizer 2. With all the changes and edits a custom setup has, you will not be able to remember everything by heart, and, thanks to the **Notes** tab, you will not have to.

## Additional Mods

With arguably the most important mods now set up and configured properly, we are going to move on to some more common mods that are not exclusively SKSE plugins.

### Unofficial Skyrim Special Edition Patch

What SSE Engine Fixes is for engine bugs, the **Unofficial Skyrim Special Edition Patch** is for the rest of the game. Usually shortened to **USSEP**, it fixes various issues and serves as the base for most modded setups. Some of its changes have been controversial, but considering how deeply embedded the USSEP is in the general modding scene with countless mods directly requiring it, installing it is highly recommended.

- Download and install the latest main file of the [Unofficial Skyrim Special Edition Patch](https://www.nexusmods.com/skyrimspecialedition/mods/266?tab=files).

After installing and activating the USSEP, you will notice that it is different from the other mods we installed so far. In a way, it is the first "regular" mod that we installed: It includes a plugin (ESP) and a BSA. This plugin should now also show up in the right pane, the load order. We will take a closer look at all of the USSEP's files soon.

But, oh no! Something is clearly wrong because there is a warning flag in the load order and the warning button in MO2's upper right corner has just lit up. We have some missing masters which we will deal with in the next step. For now, let's move on.

### Skyrim Landscape and Water Fixes

Many landscape bugs and oddities that remain unaffected by the USSEP have been addressed in **Skyrim Landscape and Water Fixes** (SLaWF). Interesting for us is also that the mod is contained in a **FOMOD** installer. The acronym hails from the Fallout New Vegas days and stands for **F**all**o**ut **Mod** Archive. It allows for a modular installation which may include picking or skipping optional files, or choosing between various alternatives. Mods with FOMOD installers are common.

- Download the latest main file of [Skyrim Landscape and Water Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/26138?tab=files).

Upon double-clicking the mod in the **Downloads** pane in Mod Organizer 2, the FOMOD installer will open. As you can see at the top, the core files are installed automatically (you cannot uncheck them). In addition, patches are offered for various mods, none of which we have installed right now, so you do not have to check any of them. There is a fix for a specific file (a mesh with a gap on one side) that by default will install a version for vanilla which we also do not need to change.

And finally there are some optional fixes which were separated from the main file for compatibility reasons. For now I recommend you check the **Missing Lights Fix** as well. Later on, you will want to reinstall this mod and select different options based on your other mod choices (we will get to that).

![SLAWF FOMOD Installer](/Pictures/embers/module-1/slawf-fomod-installer.png)

### SkyUI

**SkyUI** is a full interface overhaul for Skyrim, intended to optimise the original console UI for PC. It also adds the Mod Configuration Menu. For those who *really* like the vanilla UI for some reason, there is [Hide SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/12770) which can be installed on top of SkyUI to remove the new interface but retain the MCM functionality.

- Download and install the latest main file of [SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/12604?tab=files).

### More Informative Console

We already had a first look at the console in the previous step when we verified that SKSE was installed correctly. While the console is already useful for mod testing in its vanilla state, **More Informative Console** is a truly invaluable extension of its functionality, turning the console into the best tools to easily track down various issues. 

One of the great features of the mod is the ability to click any object ingame to find out its unique **Form ID**. We will talk more about Form IDs later on, but for now imagine them as "ID cards" of whatever rock, or weapon, or NPC you clicked on. Knowing an object's Form ID makes it infinitely easier to find it in the game files if there is something that needs to be fixed or adjusted, particularly since More Informative Console will also tell you where the object was last edited.

The mod also adds a ton of additional information that can be viewed directly ingame as well as new hotkeys for easier navigation of the console.

- Download and install the latest main file of [More Informative Console](https://www.nexusmods.com/skyrimspecialedition/mods/19250?tab=files).

### Crash Logger

Another debugging tool, **Crash Logger** generates proper crash logs whenever the game is forced to close. These logs are often difficult to read, but they are vital for troubleshooting your own setup and may also be required when reporting bugs in other mods.

- Download and install the latest main file of [Crash Logger](https://www.nexusmods.com/skyrimspecialedition/mods/59596?tab=files).