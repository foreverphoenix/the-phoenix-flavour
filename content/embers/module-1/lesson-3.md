---
title: "Lesson 3: Plugins, Pt 1"
weight: 3
type: docs
no-list: false
description: >
 Installation of essential mods, and plugin basics.
---

## Overview

**Welcome to Lesson 3.**

- Installation of a number of essential mods.
- Installation of SSEEdit.

## Workbase

Before we can have a look at Skyrim plugins, we need to install a few mods first.

There are thousands upon thousands of mods on the Nexus, and the vast majority are simply a matter of personal preference. In this step, however, we are going to install and configure some of those mods that should be part of any modded setup. They will serve as a workbase, to be put in place before we even start to think about going ingame.

First up, we should create a new separator for the set of mods that we will be installing next. Name it **ESSENTIALS** and place it below the **SCRIPT EXTENDER** mods.

![Lesson 3 Separator](/Pictures/embers/module-1/lesson-three-separator.png)

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
- The new mod will now appear in the mod order below the **ESSENTIALS** separator.
- Check the box to activate it.

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

I put the note into the line at the top which is what is displayed in the **Notes** column in the mod order. If I had changed more, I would have edited the larger space below.

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

In addition, we are going to install four more mods to serve as examples during the second part of this lesson where we talk about plugins and load order. All four of these mods can also be counted as essentials so you would want to install them either way.

### Unofficial Skyrim Special Edition Patch

What SSE Engine Fixes is for engine bugs, the **Unofficial Skyrim Special Edition Patch** is for the rest of the game. Usually shortened to **USSEP**, it fixes a ton of various issues and serves as the base for most modded setups. Some of its changes have been controversial, but considering how deeply embedded the USSEP is in the general modding scene with countless mods directly requiring it, installing it is highly recommended.

- Download and install the latest main file of the [**Unofficial Skyrim Special Edition Patch**](https://www.nexusmods.com/skyrimspecialedition/mods/266).

After installing and activating the USSEP, you will notice that it is different from the other mods we installed so far. In a way, it is the first "regular" mod that we installed: As you can see in the Contents column in Mod Organizer 2, it contains multiple file types, including a plugin. This plugin should now also show up in the right pane, the load order. We will take a closer look at all of the USSEP's files very soon, but for now there are a few more mods to be installed first.

### Skyrim Landscape and Water Fixes

Many landscape bugs and oddities that remain unaffected by the USSEP have been addressed in **Skyrim Landscape and Water Fixes** (SLaWF). Interesting for us is also that the mod is contained in a **FOMOD** installer. The acronym hails from the Fallout New Vegas days and stands for **F**all**o**ut **Mod** Archive. It allows for a modular installation which may include picking or skipping optional files, or choosing between various alternatives. Mods with FOMOD installers are common.

- Download the latest main file of the [**Skyrim Landscape and Water Fixes**](https://www.nexusmods.com/skyrimspecialedition/mods/26138).

Upon double-clicking the mod in the **Downloads** pane in Mod Organizer 2, the FOMOD installer will open. As you can see at the top, the core files are installed automatically (you cannot uncheck them). In addition, patches are offered for various mods, none of which we have installed right now, so you do not have to check any of them. There is a fix for a specific file (a mesh with a gap on one side) that by default will install a version for vanilla which we also do not need to change.

And finally there are some optional fixes which were separated from the main file for compatibility reasons. For now I recommend you check the **Missing Lights Fix** as well (although you may need to remove it down the line if you choose to install ELFX or Tamriel Master Lights).

Since we do not need any of the compatibility options, we can simply click **Install** now to install the mod.

![SLAWF FOMOD Installer](/Pictures/embers/module-1/slawf-fomod-installer.png)

### More Informative Console

We already had a first look at the console in the previous step when we verified that SKSE was installed correctly. While it is already useful for mod testing in its vanilla state, **More Informative Console** is a truly invaluable extension of its functionality, turning the console into the best tools to easily track down various issues. 

One of the great features of the mod is the ability to click any object ingame to find out its unique **Form ID**. We will talk more about Form IDs later on, but for now imagine them as "ID cards" of whatever rock, or weapon, or NPC you clicked on. Knowing an object's Form ID makes it infinitely easier to find it in the game files if there is something that needs to be fixed or adjusted, particularly since More Informative Console will also tell you where the object was last edited.

The mod also adds a ton of additional information that can be viewed directly ingame as well as new hotkeys for easier navigation of the console.

- Download and install the latest main file of [**More Informative Console**](https://www.nexusmods.com/skyrimspecialedition/mods/19250).

### SkyUI

As one of the most popular Skyrim mods of all time, **SkyUI** is a staple in almost everyone's load order. It changes Skyrim's very simplistic, controller-optimised interface into a useful and modern-looking alternative that is far better suited for mouse and keyboard (but still works perfectly with a controller).

In addition to overhauling the interface, SkyUI also adds the **Mod Configuration Menu** already mentioned in the previous lesson. The Mod Configuration Menu, or **MCM** for short, is a new option in the Pause menu through which mods with MCM support can be customised. Before SkyUI implemented this option, mods would offer ingame customisation through spells, powers, and other workarounds which was intrusive and inconvenient.

It is because of the Mod Configuration Menus that SkyUI must be considered an essential mod.

- Download and install the latest main file of [**SkyUI**](https://www.nexusmods.com/skyrimspecialedition/mods/12604).

> If you are on an ultrawide monitor (21:9 resolution), you will need an additional patch. I will cover widescreen support later on, so you are likely best off keeping SkyUI disabled for the time being.

## Plugin Basics

Several mod installations later, we have the beginning of a mod order in the left pane. If you switch to the **Plugins** tab in the right pane of Mod Organizer 2, the load order, you will also see three new plugins, sorted in the order in which they were installed:

![Lesson 3 Plugins](/Pictures/embers/module-1/lesson-three-plugins.png)

> If they are not automatically arranged this way, you can drag them around to match the image.

### ESM vs ESP

Curiously, two of the four new plugins are displayed in ***bold italics*** while the others are not.

This is how Mod Organizer 2 distinguishes between plugin types in the load order. If you look at the official master files (**Skyrim.esm**, etc) they are greyed out because they cannot be disabled, but they are also in ***bold italics***. That is what **ESM** (Elder Scrolls Master) plugins look like. They are different from **ESP** (Elder Scrolls Plugin) files in multiple ways.

**One important difference is that ESM plugins will *always* load above ESP plugins.**

However, as you may already have noticed, the two ESM plugins actually have the **.esp** file extension rather than **.esm**. Why then are they marked as ESM plugins in Mod Organizer 2?

This is where matters get complicated: There are hybrid file types. Using a program called **SSEEdit** (which we are going to install shortly), one can *flag* an ESP as ESM to force it to load above all other ESPs. In the case of the USSEP and SLAWF, this is helpful because they are intended to overwrite the official game files, but then in turn be overwritten by various other mods. As **ESM-ified ESPs**, the USSEP and SLAWF plugins can always be at the very top of your load order, right below the official master files.

> Technically, the SLAWF plugin is a hybrid of ESM, ESP, and a third plugin type, the **ESL** plugin. We will talk about ESLs later on.

### Plugin Order

As we already established, ESM plugins (which include ESM-ified ESPs) always load above ESP plugins. If you try to drag the **Unofficial Skyrim Special Edition Patch.esp** below **SkyUI_SE.esp**, it will simply not work. However, you can freely change the order of the two ESM-ified ESPs via drag-and-drop.

**Plugins overwrite each other in the order they are placed in.** A plugin that is lower in the load order will overwrite plugins higher in the load order. That is why the official master files are right at the top, to be overwritten by any plugin placed after them.

> Plugin order and load order are the same thing.

### Dependencies

Often plugins directly depend not only on official master files but also on other plugins. This is the case with **Landscape and Water Fixes.esp** which depends on the **Unofficial Skyrim Special Edition.esp**. If you uncheck the USSEP's plugin in the load order, Mod Organizer 2 will instantly warn you about the missing master. The notification in the upper right corner will light up and show the warning if you click on it.

![SLAWF Missing Master](/Pictures/embers/module-1/slawf-missing-master.png)

Alternatively, you can hover over the **Landscape and Water Fixes.esp** which has now been marked with a small warning sign icon to see all its dependencies and which master is missing.

Since the SLAWF plugin requires the USSEP plugin directly, we know that it must be placed *below* it in the load order as plugins are always placed below their masters. Be sure to re-enable the USSEP plugin and to place it above the SLAWF plugin before we proceed with the next step.

> It should be noted that Skyrim SE, unlike Skyrim LE, does not *always* immediately crash on launch when a master is missing. However, a missing master error must still be fixed.

## The Unwanted Effects Book

Among vanilla Skyrim's many bugs are certain active effects, applied by spells for instance, that may get "stuck" on the player after they are supposed to expire. The USSEP fixes these effects, but it also adds an option for the player to rid themselves of any leftovers. Initially, this could be accessed through a second shrine in the Temple of Kynareth in Whiterun, but was later moved to a book added to the player's inventory upon loading the game. Following complaints about a lack of immersion, a compromise was finally reached by placing the book in the Temple of Kynareth.

Using books or powers in order to access or customise a mod's functionality was rather common before the Script Extender and SkyUI came along, although nowadays such options have largely been moved to dedicated mod configuration menus. With the release of Skyrim SE and the introduction of mods on consoles, many mod authors had to revert to these old workarounds as it is impossible to install files outside the Data folder on consoles, and thus impossible to install the Skyrim Script Extender. The USSEP team does not want to move the option to an MCM or make it available only through the (ingame) console as that would not work for the XBOX and Playstation ports of the mod.

However, for us PC players, the book is entirely redundant. If you ever find yourself stuck with an active effect, you can get the book through the console very easily, so there is no need to have it lying around in the game world or lugging it around with you. Does it really break immersion? Some players are vehemently opposed to having any sort mod config items in the world. Others probably never noticed the book in the first place.

Whatever the case, disabling that book makes for a nice example edit, our first foray into the world of plugins.

### Finding the Book

Let's go and have a look at that book, shall we?

- Launch **SKSE** through Mod Organizer 2.
- In the main menu, open the **console** (press the *tilde* key above TAB on your keyboard).
- Type `coc WhiterunTempleofKynareth` and press **Enter**.

> Unfortunately, you cannot copy and paste in the console (without additional mods).

The **coc** (**c**enter **o**n **c**ell) command is insanely useful for testing. When used from the main menu, it will create a test character in your chosen cell with some basic equipment (check your inventory if you like). Do note that **coc** is for testing *only*, you will run into all kinds of issues if you try to use it for an actual playthrough as skipping the intro will cause many of the game's scripts to never be properly initialised.

To find the book, go from where you spawned by entrance to the temple into the sleeping area on the right. There is a bookcase just in front of you with the **USSEP Unwanted Effects Remover** on the floor leaning against its side.

![USSEP Book 1](/Pictures/embers/module-1/ussep-book-1.jpg)

![USSEP Book 2](/Pictures/embers/module-1/ussep-book-2.jpg)

Now we know where the book is. How does that help us?

The USSEP plugin is big. It has hundreds upon hundreds of records, and finding a single book among them sounds rather inconvenient. What you *really* need to know is the book's **Form ID**, its unique identification number. To figure out that Form ID, we installed **More Informative Console**.

- Open the console once again and click on the book.
- Here is what you should see:

![USSEP Book 3](/Pictures/embers/module-1/ussep-book-3.jpg)

Everything we could possibly need to know we can see at a glance thanks to the mod. Either take a screenshot or simply refer to mine, then **save** and **close** the game. It is time to talk about Form IDs.

## About Form IDs

Every object, NPC, magic effect, music track, etc, in the game is defined in a unique *record* which is contained in a *plugin*. For vanilla Skyrim, that is what the official master files do: Each of the five plugins contains thousands of **records**, one for every *thing* in the game, for NPCs, magic effects, music tracks, and so forth. Every record has a unique **Form ID** to be identified by. No two Form IDs can ever be identical.

Form IDs consist of 8 [hexadecimal](https://en.wikipedia.org/wiki/Hexadecimal) numbers (1-9 and A-F). The first two denote the **Index** which refers to the load order position of the plugin that the record was initially defined in. They change depending on your load order. The remaining six numbers will always stay the same. This way, there can never be two plugins with duplicate Form IDs: No two plugins can be loaded in the same spot in the load order so they will always have a different index.

### Base and Ref Form ID

However, if we check the info we grabbed through More Informative Console, we will notice that the book has not one but *two* Form IDs:

![USSEP Book FormID](/Pictures/embers/module-1/ussep-book-formid.jpg)

The **Base Form ID** is `050B1985` and describes the book itself: It defines which model it uses, what its contents are, and, in this case, what script is attached to it. From the first two digits of the Form ID, you can tell that it is defined in the **Unofficial Skyrim Special Edition Patch.esp** plugin. If you check the load order in Mod Organizer 2, the mod index of the USSEP plugin is **05** which is identical to the index of the book's Base Form ID.

The **Ref Form ID** is `0190001B` and describes the book's placement: That it is located in the `WhiterunTempleofKynareth` cell, that it is enabled, how it is placed, and so on. The reason a second Form ID is needed is because you may have various copies of the same object distributed throughout the game. While the book is unique right now, a Steel Sword would not be. There are dozens of hand-placed Steel Swords in Skyrim. Each of them has a unique REFR (reference) record with its unique Ref Form ID: They *refer* to the original item defined in the record with the Base Form ID.

**In short:** `050B1985` is the USSEP Unwanted Effects Remover book and `0190001B` is the copy of it placed in the Temple of Kynareth.

### Injected Forms

As you may have noticed, the index for the book's Ref Form ID actually corresponds to **Update.esm** instead of the USSEP plugin. It is an **injected record**, meaning that while it is not *defined* in Update.esm, another plugin referring to it would not have a missing master if the USSEP were not present as long as Update.esm is there. This is helpful for patchless compatibility.

For example, a mod might change the interior of the Temple of Kynareth in such a way that the USSEP book is suddenly stuck in furniture, or otherwise inaccessible or in the way. The mod author could add the USSEP as a master to their plugin and move the book out of the way, but now their Temple of Kynareth mod would always require the USSEP.

Because the book's REFR record is an injected form though, adding the USSEP as a master would not be required in the first place - only Update.esm would have to be added (and everyone has Update.esm). That means the book would be moved if the USSEP was installed, but there would not be a missing master error if it was not.

## Conclusion