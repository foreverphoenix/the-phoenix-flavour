---
title: "Step 5: Essential Mods"
weight: 5
type: docs
description: >
  Installing essential mods using Mod Organizer 2.
---

## SSE Engine Fixes

**SSE Engine Fixes** is a collaboration of some of the most talented coders in the community, including aers, Ryan, Nuukem, meh321, and others. It is the definitive solution to most engine-level bugs, all fixed through a single SKSE plugin, but also includes a memory patch that completely changes the way memory allocation works.

The mod is unusual insofar as it requires an additional plugin, the **SKSE64 Plugin Preloader** by meh321 and sheson, which allows SKSE plugins to load before the game initialises. This plugin is why the mod is split into two main files as it has to be installed into the **root folder** like the Script Extender.

Some of its features include:

- Ability to unlock Steam achievements with mods loaded (no need to install a [separate mod](https://www.nexusmods.com/skyrimspecialedition/mods/245) to enable them).
- Fixed bug that made tree reflections on water look like big black rectangles ([example](https://cdn03.bethesda.net/forum/uploads/cb978428-9cb1-49eb-9081-e5f74279c78d.jpg) and [discussion on Beth.net](https://bethesda.net/community/topic/31372/issue-with-reflections-in-water?language%5B%5D=en)).
- Fixes changes to sound volume sliders added by mods not being saved across game restarts.
- Various crash fixes like the one that would occur on systems in cities with letters not in the English alphabet.
- Fixes and tweaks by [meh321](https://www.nexusmods.com/skyrim/mods/75951), [Cobb](https://www.nexusmods.com/skyrim/mods/96734), and [lStevieAl](https://www.nexusmods.com/skyrim/users/2232669?tab=user+files&BH=0) ported from Skyrim LE.
- Warning if the user's setup approaches the [reference handle cap](https://www.reddit.com/r/skyrimmods/comments/ag4wm7/psa_the_reference_handle_cap_or_diagnosing_one_of/).

### SKSE64 Preloader

Before we grab the main file, we should install the preloader:

- From the [**SSE Engine Fixes**](https://www.nexusmods.com/skyrimspecialedition/mods/17230) mod page, download the **(Part 2)** main file (click the **Manual Download** button).
- Open the downloaded archive and extract all three plugins (DLLs) into your **root folder**.

![SKSE Preloader Installation](/Pictures/embers/module-1/skse-preloader-installation.png)

### SKSE Plugin

With the required preloader in place, we can now install the other main file. Since this one does belong into the **data folder** we can use Mod Organizer 2 as usual.

- From the [**SSE Engine Fixes**](https://www.nexusmods.com/skyrimspecialedition/mods/17230) mod page, download the **(Part 1)** main file (click the **Mod Manager Download** button).
- Click **Download** button again in the **Mod Requirements** window (all dependencies are already installed).
- In Mod Organizer 2, find the downloaded file in the **Downloads** tab and double-click it to install.
- The new mod will now appear at the bottom of your mod order. Check the box to activate it.

### Configuration

Like many other SKSE plugins, SSE Engine Fixes can be customised through a configuration file (though it is a [**TOML**](https://en.wikipedia.org/wiki/TOML) file instead of [**INI**](https://en.wikipedia.org/wiki/INI_file)).

- In Mod Organizer 2, double-click **SSE Engine Fixes** in your mod order.
- Switch to the **Text Files** tab.

Configuration files for mods will show up in one of two tabs in Mod Organizer 2: Most have the **INI** file extension and will show up in the **INI Files** tab. While MO2 can also read **TOML** files, those will show up in the **Text Files** tab instead. Functionally, this makes no difference, they can be viewed and edited through the MO2 UI just the same, but it may be confusing at first.

- Select the `SKSE\Plugins\EngineFixes.toml` in the list on the left. This is the primary config file for SSE Engine Fixes.

Here you can see a long list of various fixes and tweaks that are part of the mod. There is no need to change anything right now, the mod works perfectly fine out of the box.

### Example Edits

> **You do not have to make any of these changes.** They are meant as an example. But remember the notes feature in MO2 and try to get into the habit of leaving notes for yourself when you change something. It is easy to forget small tweaks like these.

Here are two tweaks that I personally enable:

**DisableChargenPrecache** prevents slowdowns and crashes in the character creation menu in heavily modded setups. This fix is already included in [**RaceMenu**](https://www.nexusmods.com/skyrimspecialedition/mods/19080), a very popular UI overhaul of the character creation menu which is also required for the number one skeleton replacer. Almost everyone uses RaceMenu so they do not need to use the precache killer in Engine Fixes. But since I skip RaceMenu in my personal setup, I do enable it.

**SleepWaitTime** speeds up the wait menu. When you press T to wait in vanilla, the hours tick down slowly, and especially for mod testing this can sometimes be a little frustrating.

- In the `[Patches]` section, set `DisableChargenPrecache =` and `SleepWaitTime =` to `true`.
- Press **CTRL + S** to save your changes.

This is a pretty minor change and of course I can revert it anytime. However, I am forgetful so I also switch to the **Notes** tab in MO2 and leave a quick reminder for myself (see screenshot below). If in the future I should install RaceMenu after all, I will (hopefully) check my notes on SSE Engine Fixes and disable the precache killer again.

![Engine Fixes Note](/Pictures/embers/module-1/engine-fixes-note.png)
