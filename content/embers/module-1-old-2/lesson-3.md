---
title: "Lesson 3: Essential Mods"
weight: 3
type: docs
no-list: false
description: >
 Installation of essential mods and how to organise them in MO2.
---

## Workbase

Before we start diving into the specifics of Skyrim plugins and our first tweaks in SSEEdit, we need to establish a solid baseline of essential mods that should be part of every setup. Some of the mods that we will install in this lesson will also provide plenty of practical examples for us to look at in the next lessons.

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

- From the [SSE Engine Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/17230) mod page, download the **(Part 2)** main file (click the **Manual Download** button).
- Open the downloaded archive and extract all three plugins (DLLs) into your **root folder**.

![SKSE Preloader Installation](/Pictures/embers/module-1/skse-preloader-installation.png)

### SKSE Plugin

With the required preloader in place, we can now install the other main file. Since this one does belong into the **data folder** we can use Mod Organizer 2 as usual.

- From the [SSE Engine Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/17230) mod page, download the **(Part 1)** main file (click the **Mod Manager Download** button).
- Click **Download** button again in the **Mod Requirements** window (all dependencies are already installed).
- In Mod Organizer 2, find the downloaded file in the **Downloads** tab and double-click it to install.
- The new mod will now appear at the bottom of your mod order. Check the box to activate it.

### Configuration

Like many other SKSE plugins, SSE Engine Fixes can be customised through a configuration file (though it is a [TOML](https://en.wikipedia.org/wiki/TOML) file instead of [INI](https://en.wikipedia.org/wiki/INI_file)).

- In Mod Organizer 2, double-click **SSE Engine Fixes** in your mod order.
- Switch to the **Text Files** tab.

Configuration files for mods will show up in one of two tabs in Mod Organizer 2: Most have the **INI** file extension and will show up in the **INI Files** tab. While MO2 can also read **TOML** files, those will show up in the **Text Files** tab instead. Functionally, this makes no difference, they can be viewed and edited through the MO2 UI just the same, but it may be confusing at first.

- Select the `SKSE\Plugins\EngineFixes.toml` in the list on the left. This is the primary config file for SSE Engine Fixes.

Here you can see a long list of various fixes and tweaks that are part of the mod. There is no need to change anything right now, the mod works perfectly fine out of the box.

### Example Edits

> **You do not have to make any of these changes.** They are meant as an example. But remember the notes feature in MO2 and try to get into the habit of leaving notes for yourself when you change something. It is easy to forget small tweaks like these.

Here are two tweaks that I personally enable:

**DisableChargenPrecache** prevents slowdowns and crashes in the character creation menu in heavily modded setups. This fix is already included in [RaceMenu](https://www.nexusmods.com/skyrimspecialedition/mods/19080), a very popular UI overhaul of the character creation menu which is also required for the number one skeleton replacer. Almost everyone uses RaceMenu so they do not need to use the precache killer in Engine Fixes. But since I skip RaceMenu in my personal setup, I do enable it.

**SleepWaitTime** speeds up the wait menu. When you press T to wait in vanilla, the hours tick down slowly, and especially for mod testing this can sometimes be a little frustrating.

- In the `[Patches]` section, set `DisableChargenPrecache =` and `SleepWaitTime =` to `true`.
- Press **CTRL + S** to save your changes.

This is a pretty minor change and of course I can revert it anytime. However, I am forgetful so I also switch to the **Notes** tab in MO2 and leave a quick reminder for myself (see screenshot below). If in the future I should install RaceMenu after all, I will (hopefully) check my notes on SSE Engine Fixes and disable the precache killer again.

![Engine Fixes Note](/Pictures/embers/module-1/engine-fixes-note.png)

## .NET Script Framework

**.NET Script Framework** is another framework and modder's resource, not unlike the Script Extender. While it is a dependency for various other mods, it also brings one of the most important features for any setup to the table: **crash logs**.

For the longest time, Skyrim modders used to enable the debugging functionality of the scripting engine, Papyrus. Unfortunately, the Papyrus logs were difficult to read and rarely helpful in diagnosing a crash which they were never meant for to begin with. This mod's crash logs are admittedly not always easy to read either, but they usually include relevant information related to the cause of the crash that are genuinely helpful in troubleshooting and fixing it.

- Open the Nexus page for [**.NET Script Framework**](https://www.nexusmods.com/skyrimspecialedition/mods/21294) and download the latest main file through MO2.
- Click **Download** in the mod requirements window.
- Install the mod as usual from the **Downloads** tab in Mod Organizer 2 and activate it in the mod order.

> Instead of the DLL Plugin Loader, the already installed SKSE64 Preloader from SSE Engine Fixes will be loading the mod.

While .NET Script Framework does have configuration files, there is nothing that needs to be edited.

## SSE Display Tweaks

**SSE Display Tweaks** is another game-changer as far as Skyrim mods go. It consolidates all performance and monitor settings in one place, and adds a highly configurable on-screen-display.

It also enables the game to run (mostly) without issues at framerate exceeding 60FPS. **In vanilla, the physics engine is tied directly to the framerate.** When unlocking it and going above 60FPS, the game would increasingly bug out to the point where it would become completely unplayable. SSE Display Tweaks fixes that.

> It should be noted that some minor bugs may still occur with increasing frequency at higher framerates. These include small physics bugs, such as objects moving for no reason or "spazzing out" and creatures falling from the sky.

While this is not the time to talk about performance and hardware, you should be aware that modded Skyrim is unforgiving, particularly on high resolutions. Reaching stable 60FPS at resolutions above 1080p but especially at 4K with many visual mods and an ENB preset will require a very solid modern PC.

For the vast majority of users, **capping the frame rate at 60FPS or 72FPS is appropriate**, both to keep physics strangeness to a minimum as well as to ensure that the framerate does not fluctuate too much.

(Since we already installed several mods, the instructions (download, install, activate) will be briefer from now on.)

- Download and install the latest main file of [**SSE Display Tweaks**](https://www.nexusmods.com/skyrimspecialedition/mods/34705).

### Configuration

> While the settings changed here can also be configured in the default Skyrim INI files, it is easier, for the purposes of this guide, to simply use SSE Display Tweaks now, and discuss Skyrim INI settings later on.

SSE Display Fixes has a large amount of configurable options in its INI file, most of which do not need editing. By default, VSYNC is enabled which it always should be (even if you have G-SYNC or FreeSync). Feel free to dig through the mod page and configuration page now or later to find out more about the mod's features.

We do want to make sure the game is set to Borderless Fullscreen mode so that you can benefit from the DXGI flip model integration (improving performance). It should be noted that this only works on **Windows 10**, so any Windows 7 or 8.1 users are going to want to use exclusive fullscreen instead.

SSE Display Tweaks has options to overwrite the game's settings, but they are currently commented out. If lines are commented out in a configuration file that means they are prefixed with a symbol like a semicolon `;` or, in this case, a number sign `#` so that they are not recognised and therefore not used.

Uncommenting a setting simply means removing whichever symbol it was prefixed with to disable it.

- Have a look at the **SSEDisplayTweaks.ini** through Mod Organizer 2 like we did with the **EngineFixes.toml** earlier.
- Uncomment `Fullscreen=false` and `Borderless=true` in the **Render** section (near the top).

You can also use SSE Display Tweaks to set your resolution:

- Uncomment `Resolution=` and, if you are not playing at 1080p, change the value to your monitor's resolution.

> Do not uncomment the ResolutionScale line. It enables down-scaling which is a great way to improve performance, but we will discuss it more indepth later on.

If you would like to change the framerate cap (default is 240FPS), you can do so in the SSEDisplayTweaks.ini as well.  Once again, I recommend **60** or **72** for the aforementioned reasons.

- Scroll down to find the `FramerateLimit=` line and change the value to your desired framerate cap.

After making all desired changes, press **CTRL+S** to save them.

Finally, I added `Enabled borderless fullscreen. Capped framerate at 60FPS.` in the mod's **Notes** tab. Always make heavy use of that feature in Mod Organizer 2. With all the changes and edits a custom setup has, you will not be able to remember everything by heart, and, thanks to the **Notes** tab, you will not have to.

![Display Tweaks INI](/Pictures/embers/module-1/display-tweaks-ini.png)

## Additional Basic Mods

With SSE Engine Fixes, NET Script Framework, and SSE Display Tweaks, the most vital of mods are now in place.

In addition, we are going to install four more mods to serve as examples in the next lesson where we talk about plugins and load order. All four of these mods can also be counted as essentials so you would want to install them either way.

### Unofficial Skyrim Special Edition Patch

What SSE Engine Fixes is for engine bugs, the **Unofficial Skyrim Special Edition Patch** is for the rest of the game. Usually shortened to **USSEP**, it fixes a ton of various issues and serves as the base for most modded setups. Some of its changes have been controversial, but considering how deeply embedded the USSEP is in the general modding scene with countless mods directly requiring it, installing it is highly recommended.

- Download and install the latest main file of the [Unofficial Skyrim Special Edition Patch](https://www.nexusmods.com/skyrimspecialedition/mods/266).

After installing and activating the USSEP, you will notice that it is different from the other mods we installed so far. In a way, it is the first "regular" mod that we installed: As you can see in the **Contents** column in Mod Organizer 2, it contains multiple file types, including a plugin. This plugin should now also show up in the right pane, the load order. We will take a closer look at all of the USSEP's files very soon, but for now there are a few more mods to be installed first.

### Skyrim Landscape and Water Fixes

Many landscape bugs and oddities that remain unaffected by the USSEP have been addressed in **Skyrim Landscape and Water Fixes** (SLaWF). Interesting for us is also that the mod is contained in a **FOMOD** installer. The acronym hails from the Fallout New Vegas days and stands for **F**all**o**ut **Mod** Archive. It allows for a modular installation which may include picking or skipping optional files, or choosing between various alternatives. Mods with FOMOD installers are common.

- Download the latest main file of the [Skyrim Landscape and Water Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/26138).

Upon double-clicking the mod in the **Downloads** pane in Mod Organizer 2, the FOMOD installer will open. As you can see at the top, the core files are installed automatically (you cannot uncheck them). In addition, patches are offered for various mods, none of which we have installed right now, so you do not have to check any of them. There is a fix for a specific file (a mesh with a gap on one side) that by default will install a version for vanilla which we also do not need to change.

And finally there are some optional fixes which were separated from the main file for compatibility reasons. For now I recommend you check the **Missing Lights Fix** as well (although you may need to remove it down the line if you choose to install ELFX or Tamriel Master Lights).

Since we do not need any of the compatibility options, we can simply click **Install** now to install the mod.

![SLAWF FOMOD Installer](/Pictures/embers/module-1/slawf-fomod-installer.png)

### More Informative Console

We already had a first look at the console in the previous step when we verified that SKSE was installed correctly. While it is already useful for mod testing in its vanilla state, **More Informative Console** is a truly invaluable extension of its functionality, turning the console into the best tools to easily track down various issues. 

One of the great features of the mod is the ability to click any object ingame to find out its unique **Form ID**. We will talk more about Form IDs later on, but for now imagine them as "ID cards" of whatever rock, or weapon, or NPC you clicked on. Knowing an object's Form ID makes it infinitely easier to find it in the game files if there is something that needs to be fixed or adjusted, particularly since More Informative Console will also tell you where the object was last edited.

The mod also adds a ton of additional information that can be viewed directly ingame as well as new hotkeys for easier navigation of the console.

- Download and install the latest main file of [More Informative Console](https://www.nexusmods.com/skyrimspecialedition/mods/19250).

### SkyUI

As one of the most popular Skyrim mods of all time, **SkyUI** is a staple in almost everyone's load order. It changes Skyrim's very simplistic, controller-optimised interface into a useful and modern-looking alternative that is far better suited for mouse and keyboard (but still works perfectly with a controller). Even Todd Howard loves SkyUI!

In addition to overhauling the interface, SkyUI also adds the **Mod Configuration Menu** already mentioned in the previous lesson. The Mod Configuration Menu, or **MCM** for short, is a new option in the Pause menu through which mods with MCM support can be customised. Before SkyUI implemented this option, mods would offer ingame customisation through spells, powers, and other workarounds which was intrusive and inconvenient.

It is because of the Mod Configuration Menus that SkyUI must be considered an essential mod.

- Download and install the latest main file of [SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/12604).

> If you are on an ultrawide monitor (21:9 resolution), you will need an additional patch from [this mod page](https://www.nexusmods.com/skyrimspecialedition/mods/1778). Be sure to grab the one for SkyUI 5.2 SE Alpha.

## Taking Stock

We have installed our first set mods which now show up in the left pane, the **mod order**. All mods will appear here after they are installed, but they will only be loaded in MO2's virtual data folder if they are checked. Unchecking a mod here is functionally the same thing as uninstalling it altogether.

However, you may have noticed that only a few plugins have shown up in the right pane, the **load order**. Here, we only see Skyrim's five official master files at the top and, below them, plugins from the USSEP, SLAWF, and SkyUI, respectively. Clearly, not every mod we installed has a corresponding plugin in the load order.

A common misconception among modding beginners is that "mods" and "plugins" can be used interchangeably. **However, mods and plugins are not the same thing.** Plugins can be  *part* of a mod. Some mods achieve their effect exclusively through a plugin (or several). Other mods do not include any plugins at all.

Speaking of plugins ...

### Plugin Types

We have been using the word "plugin" for two different file types now, so it may get confusing. Here is the gist of it:

**Plugins** are files with an `.ESP`, `.ESM`, or `.ESL` file extension. They appear in the load order (you can see some of them right now). Plugins, their interactions, and the order they are loaded in are going to be extremely relevant. As file types they are also unique to Creation Engine games like Skyrim.

**SKSE Plugins** with the `.DLL` extension on the other hand use SKSE functions to make Engine-level edits to the game. They are far more rare and cannot easily be viewed or edited. [DLL plugins](https://en.wikipedia.org/wiki/Dynamic-link_library) are a common file type and not specific to Skyrim.

**Always assume I'm talking about ESP/ESM/ESL files when I mention "plugins".** Otherwise, I will specify the files in question as "SKSE Plugins". These two types of files are wildly different in what they do and how they function, so the distinction is very important.

We are going to talk more about (non-SKSE) plugins in the next lesson.

## Mod Order Columns

While the left pane is looking rather tame right now, it is easy to become completely disoriented after installing a hundred or so mods. Thankfully, Mod Organizer 2 has many features and options to simplify managing your mod order which we will look at now.

First up, I recommend adjusting the columns at the top of the left pane. Several are already enabled and several more can be added. By clicking any one of the columns you can sort by whatever is displayed in it: For example, clicking the **Mod Name** column will sort all your mods alphabetically. By default the mod order is sorted by **Priority** which is what you want 99% of the time - after all, the point of the left pane is to show you the order in which your mods are loaded.

You can toggle each column separately by right-clicking any one of them and checking or unchecking the respective boxes:

![MO2 Column Options](/Pictures/embers/module-1/mo2-column-options.png)

These are the columns that are available:

- **Conflicts:** Displays asset conflicts (overwrites/overwritten). Highly recommended.
- **Flags:** Displays various additional information (whether a mod has notes attached, files hidden, etc). Recommended.
- **Content:** Displays the kinds of files contained in a mod (e.g. SKSE plugins, BSAs, Scripts, etc). Highly recommended.
- **Category:** Displays the Nexus category. Not recommended, separators are a better way to sort your mods.
- **Nexus ID:** Displays the mod's ID (which is part of its unique Nexus link). Not recommended, no practical use.
- **Source Game:** Displays whether a mod is from the Skyrim LE or Skyrim SE Nexus. Highly recommended.
- **Version:** Displays the version number of the mod as defined on the Nexus page. Highly recommended.
- **Installation:** Displays the date and time of installation. Not recommended, no practical use.
- **Priority:** Displays where the mod is loaded in the order. Absolutely essential.
- **Notes:** Displays any notes in the note header (not the extended notes). Recommended.

Which of these columns you use is entirely up to you. As you become familiar with Mod Organizer 2, you should absolutely customise its interface however seems most sensible to you. Some people prefer adding the version number to the mod name instead of using the dedicated column, some use the Categories column for better sorting and even define custom categories. I personally find it much easier to sort mods by separator than category.

For now, please make sure that at least the following columns are enabled:

- Conflicts
- Flags
- Content
- Source Game
- Priority

If you do not have enough space to fit all columns comfortably, change the ratio of the panes in Mod Organizer 2. I personally like the left pane to take up about two thirds of space and the right pane one third.

Below you can see what I prefer my mod order to look like. However, you can absolutely come up with your own layout, there is no need to copy mine.

![MO2 My Columns](/Pictures/embers/module-1/mo2-my-columns.png)

## MO2 Separators

The single most useful feature in MO2 to organise your mod order is **separators**. They were highly requested by the community and ultimately implemented by the MO2 team. Each separator can be placed anywhere in the mod order, its name and colour can be customised, mods can be grouped below it, and they can be collapsed or expanded at will.

Check out [**this picture**](/Pictures/embers/module-1/tpf-mod-order.png) of the TPF mod order to get an idea of how separators can help with organising several hundreds of mods.

### Master Files Separator

At the top of your **mod order**, you can see three "mods" prefixed with **DLC**. Obviously, these are the three official DLC by Bethesda which appear in Mod Organizer 2 like any mod because, structurally, that is exactly what they are. Upon clicking on either of the three DLC files, the corresponding ESM (master plugin) will light up in the load order (right pane). This is very useful, especially with a larger setup later on: Clicking a mod in the left pane will always highlight any plugins that belong to it in the right pane, making them easy to find.

I personally drag the **DLC: Dawnguard** above the **DLC: HearthFires** in the mod order to mirror the order in which the DLC were released which is also the order in which they should overwrite each other. For the master files, the mod order is irrelevant so this is purely a cosmetic change. It just bothers me to see them in the wrong order.

Now to create a separator for the official master files:

- Click the tools icon above the mod order and select **Create separator**:

![MO2 Create Separator](/Pictures/embers/module-1/mo2-create-separator.png)

- Enter **OFFICIAL MASTER FILES** as the name and click **OK**.
- Your new separator will show up at the bottom of your mod order.
- Drag it up above the three **DLC** "mods".

If you like you can also change the separator's colour. You can do so by right-clicking it and clicking **Select Color**. You can set the separator to any colour you like, it can be changed anytime, and every separator can have a different colour. Which colour you should choose also depends on your MO2 theme (my colour scheme would be far too bright for anyone using dark mode).

### SKSE & Essentials Separators

Now that you know how to create separators in Mod Organizer 2, add two more for the mods we installed so far.

How you organise your mods is ultimately up to you. Any sort of system or naming scheme will be the most helpful to you if you came up with it yourself. However, for now I recommend going along with my choices until you have a better idea of what kind of setup you are going to build.

- Create a second separator and name it **SCRIPT EXTENDER**.
- Drag it below **DLC: Dragonborn** and above **SKSE Scripts**.
- Create a third separator and name it **ESSENTIALS**.
- Drag it below **Address Library for SKSE Plugins** and above **SSE Engine Fixes**.

Your new separators can now be collapsed whenever you like so that the left pane does not become too cluttered.

At this point, your mod order should look something like this:

![Lesson 3 Mods](/Pictures/embers/module-1/lesson-three-mods.png)

---

#### Continue with [Lesson 4](/embers/module-1/lesson-4/).