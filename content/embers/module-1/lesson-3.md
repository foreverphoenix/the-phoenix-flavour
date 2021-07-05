---
title: "Lesson 3: Essentials"
weight: 3
type: docs
no-list: false
description: >
 Installation and tweaking of essential mods.
---

## Overview

**Welcome to Lesson 3.**

- Installation of SkyUI.
- Installation of the Unofficial Skyrim Special Edition Patch.

## Basic Mods

There are thousands upon thousands of mods on the Nexus, and the vast majority are simply a matter of personal preference. In this step, however, we are going to install and configure those mods that should be part of any modded setup. We will use this opportunity to learn more about mod and load order as well as various types of mod files.

First up, we should create a new separator for the set of mods that we will be installing next. Name it **ESSENTIALS** and place it below the **SCRIPT EXTENDER** mods.

## SSE Engine Fixes

**SSE Engine Fixes** is a collaboration of some of the most talented coders in the community, including aers, Ryan, Nuukem, meh321, and others. It is the definitive solution to most engine-level bugs, all fixed through a single SKSE plugin, but also includes a memory patch that completely changes the way memory allocation works.

The mod is unusual insofar as it requires an additional plugin, the SKSE64 Plugin Preloader by meh321 and sheson, which allows SKSE plugins to load before the game initialises. This plugin is why the mod is split into two main files as it has to be installed into the **root folder** like the Script Extender.

Some of its features include:

- Ability to unlock Steam achievements with mods loaded (no need to install a [separate mod](https://www.nexusmods.com/skyrimspecialedition/mods/245) to enable them).
- Fixed bug that made tree reflections on water look like big black rectangles ([example](https://cdn03.bethesda.net/forum/uploads/cb978428-9cb1-49eb-9081-e5f74279c78d.jpg) and [discussion on Beth.net](https://bethesda.net/community/topic/31372/issue-with-reflections-in-water?language%5B%5D=en)).
- Fixes changes to sound volume sliders added by mods not being saved across game restarts.
- Various crash fixes like the one that would occur on systems in cities with letters not in the English alphabet.
- Fixes and tweaks by [meh321](https://www.nexusmods.com/skyrim/mods/75951), [Cobb](https://www.nexusmods.com/skyrim/mods/96734), and [lStevieAl](https://www.nexusmods.com/skyrim/users/2232669?tab=user+files&BH=0) ported from Skyrim LE.
- Warning if the user's setup approaches the [reference handle cap](https://www.reddit.com/r/skyrimmods/comments/ag4wm7/psa_the_reference_handle_cap_or_diagnosing_one_of/).

### SKSE64 Preloader

Before we grab the main file, let us install the preloader.

- From the [**SSE Engine Fixes**](https://www.nexusmods.com/skyrimspecialedition/mods/17230) mod page, download the **(Part 2)** main file (click the **Manual Download** button).
- Open the downloaded archive and extract all three plugins (DLLs) into your **root folder**.

![SKSE Preloader Installation](/Pictures/embers/module-1/skse-preloader-installation.png)

### SKSE Plugin

With the required preloader in place, we can now install the other main file. Since this one does belong into the **data folder** we can use Mod Organizer 2 as usual.

- From the [**SSE Engine Fixes**](https://www.nexusmods.com/skyrimspecialedition/mods/17230) mod page, download the **(Part 1)** main file (click the **Mod Manager Download** button).
- Click **Download** button again in the **Mod Requirements** window (all dependencies are already installed).
- In Mod Organizer 2, find the downloaded file in the **Downloads** tab and double-click it to install.
- The new mod will now appear in the mod order below the **ESSENTIALS** separator.
- Check the box to activate it.

### Configuration

Like many other SKSE plugins, SSE Engine Fixes can be customised through a configuration file (though it is a [**TOML**](https://en.wikipedia.org/wiki/TOML) file instead of [**INI**](https://en.wikipedia.org/wiki/INI_file)).

- In Mod Organizer 2, double-click **SSE Engine Fixes** in your mod order.
- Switch to the **Text Files** tab.

Configuration files for mods will show up in one of two tabs in Mod Organizer 2: Most have the **INI** file extension and will show up in the **INI Files** tab. While MO2 can also read **TOML** files, they will show up in the **Text Files** tab instead. Functionally, this makes no difference, they can be viewed and edited through the MO2 UI, but it may be confusing at first.

- Select the `SKSE\Plugins\EngineFixes.toml` in the list on the left. This is the primary config file for SSE Engine Fixes.

Here you can see a long list of various fixes and tweaks that are part of the mod. There is no need to change anything right now, the mod works perfectly fine out of the box.

### Example Edits

> **You do not have to make any of these changes.** They are meant as an example. But remember the notes feature in MO2 and try to get into the habit of leaving notes for yourself when you change something. It is easy to forget small tweaks like these.

There are two tweaks that I do personally enable:

**DisableChargenPrecache** prevents slowdowns and crashes in the character creation menu in heavily modded setups. This fix is already included in [**RaceMenu**](https://www.nexusmods.com/skyrimspecialedition/mods/19080), a very popular UI overhaul of the character creation menu which is also required for the number one skeleton replacer. Almost everyone uses RaceMenu so they do not need to use the precache killer in Engine Fixes. But since I skip RaceMenu in my personal setup, I do enable it.

**SleepWaitTime** speeds up the wait menu. When you press T to wait in vanilla, the hours tick down slowly, and especially for mod testing this can sometimes be a little frustrating.

- In the `[Patches]` section, set `DisableChargenPrecache =` and `SleepWaitTime = ` to `true`.
- Press **CTRL + S** to save your changes.

This is a pretty minor change and of course I can revert it anytime. However, I am forgetful so I also switch to the **Notes** tab in MO2 and leave a quick reminder for myself (see screenshot below). If in the future I should install RaceMenu after all, I will (hopefully) check my notes on SSE Engine Fixes and disable the precache killer again.

I put the note into the line at the top which is what is displayed in the **Notes** column in the mod order. If I had changed more, I would have edited the larger space below.

![Engine Fixes Note](/Pictures/embers/module-1/engine-fixes-note.png)

## .NET Script Framework

**.NET Script Framework** (NSF) is another framework and modder's resource, not unlike the Script Extender. While it is a dependency for various other mods, it also brings one of the most important features for any setup to the table: **crash logs**.

For the longest time, Skyrim modders used to enable the debugging functionality of the scripting engine, Papyrus. Unfortunately, the Papyrus logs were difficult to read and rarely helpful in diagnosing a crash which they were never meant for to begin with. NSF crash logs are admittedly not always easy to read, either, but they almost always include relevant information related to the cause of the crash that are genuinely helpful in troubleshooting and fixing it.

- Open the Nexus page for [**.NET Script Framework**](https://www.nexusmods.com/skyrimspecialedition/mods/21294) and download the latest main file through MO2.
- Click **Download** in the mod requirements window.
- Install the mod as usual from the **Downloads** tab in Mod Organizer 2 and activate it in the mod order.

> Instead of the DLL Plugin Loader, the already installed SKSE64 Preloader from SSE Engine Fixes will be loading the mod.

While .NET Script Framework does have configuration files, there is nothing that needs to be edited.

## SSE Display Tweaks

**SSE Display Tweaks** is another game-changer as far as Skyrim mods go. It consolidates all performance and monitor settings in one place, and adds a highly configurable on-screen-display.

It also enables the game to run (mostly) without issues at framerate exceeding 60FPS. **In vanilla, the physics engine is tied directly to the framerate.** When unlocking it and going above 60FPS, the game would increasingly bug out to the point where it would become completely unplayable. SSE Display Tweaks fixes that.

> It should be noted that some minor bugs may still occur with increasing frequency at higher framerates. These include small physics bugs, such as objects moving for no reason or "spazzing out" and creatures falling from the sky.

While this is not the time nor the place to talk about performance and hardware, you should be aware that modded Skyrim is unforgiving, particularly on high resolutions. Reaching stable 60FPS at resolutions above 1080p but especially at 4K with many visual mods and an ENB preset will require a very solid modern PC.

For the vast majority of users, **capping the frame rate at 60FPS or 75FPS is appropriate**, both to keep physics strangeness to a minimum as well as to ensure that the framerate does not fluctuate too much.

### Configuration

*Since we already installed mods, the instructions (download, install, activate) will be briefer from now on.*

- Download and install the latest main file of **SSE Display Tweaks**.

SSE Display Fixes has a large amount of configurable options in its INI file, most of which do not need editing. By default, the game is set to Borderless Fullscreen mode so that you can benefit from the DXGI flip model integration. VSYNC is also enabled which it always should be (even if you have G-SYNC or FreeSync). Feel free to dig through the mod page and configuration page now or later to find out more about the mod's features.

If you just want to cap the framerate, you can do so in the INI file:

- Have a look at the **SSEDisplayTweaks.ini** through Mod Organizer 2 like we did with the **EngineFixes.toml** earlier.
- In **Line 207**, you can set the `FramerateLimit =` to your desired value. Press **CTRL+S** to save your change.
- Consider noting down your change in the mod's **Notes** tab.

## Unofficial Skyrim Special Edition Patch

What SSE Engine Fixes is for engine bugs, the **Unofficial Skyrim Special Edition Patch** is for the rest of the game. Usually referred to as **USSEP**, it fixes a ton of various issues and serves as the base for most modded setups. Some of its changes have been controversial, but considering how deeply embedded the USSEP is in the general modding scene with countless mods directly requiring it, installing it is highly recommended.

- Download and install the latest main file of the [**Unofficial Skyrim Special Edition Patch**](https://www.nexusmods.com/skyrimspecialedition/mods/266).

After installing and activating the USSEP, you will notice that it is different from the other mods we installed so far. In a way, it is the first "regular" mod that we installed: As you can see in the Contents column in Mod Organizer 2, it contains multiple file types, including a plugin. We will take a closer look at these files very soon, but for now there are a few more mods to be installed first.

## More Informative Console

We already had a first look at the console in the previous step when we verified that SKSE was installed correctly. While it is already useful for mod testing in its vanilla state, **More Informative Console** is an invaluable extension of functionality, turning the console into one of the best tools to easily track down various issues. 

One of the best features of the mod is the ability to click any object ingame to find out its unique **Form ID** (base/ref). We will talk more about Form IDs later on, but for now imagine them as "ID cards" of whatever rock, or weapon, or NPC you clicked on. Knowing an object's Form ID makes it infinitely easier to find it in the game files if there is something that needs to be fixed or adjusted, particularly since the mod will also tell you where the object was last edited.

The mod also adds a ton of additional information that can be viewed directly ingame as well as new hotkeys for easier navigation of the console.

- Download and install the latest main file of [**More Informative Console**](https://www.nexusmods.com/skyrimspecialedition/mods/19250).

## SkyUI

As one of the most popular Skyrim mods of all time, **SkyUI** is a staple in almost everyone's load order. It changes Skyrim's very simplistic, controller-optimised interface into a useful and modern-looking alternative that is far better suited for mouse and keyboard (but still works perfectly with a controller).

In addition to overhauling the interface, SkyUI also adds the **Mod Configuration Menu** already mentioned in the previous lesson. The Mod Configuration Menu, or **MCM** for short, is a new option in the Pause menu through which mods with MCM support can be customised. Before SkyUI implemented this option, mods would offer ingame customisation through spells, powers, and other workarounds which was intrusive and limited.

It is because of the Mod Configuration Menus that SkyUI must be considered an essential mod.

- Download and install the latest main file of [**SkyUI**](https://www.nexusmods.com/skyrimspecialedition/mods/12604).