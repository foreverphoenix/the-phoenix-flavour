---
title: "Lesson 1"
weight: 2
type: docs
no-list: false
description: >
 Understanding Skyrim modding.
---

## Overview

**Welcome to Lesson 1.**

- We will talk about modding Skyrim in general.
- We will talk briefly about the differences between the available versions of Skyrim.
- We will make sure you have a 100% vanilla installation of the game ready to go.

## About Modding

When we think of modding, Minecraft is often one of the first games that come to mind. Its modding scene is enormous. Installing mods is as simple as installing a mod loader such as Forge and dropping .jar files into a specific folder - plug and play. Interactions between mods are relatively rare and you don't necessarily have to know a whole lot about Java and how Minecraft mods work in order to run a relatively heavily modded setup. Other moddable games are similarly easy to modify.

Bethesda games are different in this regard.

Sure, at first glance installing mods for Skyrim isn't so tough either: For the original Skyrim (2011), you could download files from the Steam workshop while for Skyrim Special Edition (2016) there is the ingame mods menu connected to the Beth.net website. You click the download button and go play - it seems rather straightforward. Unfortunately the way modding is presented on the Steam workshop as well as on Bethesda's website with its ostensible simplicity is highly misleading.

The Creation Engine that Skyrim was built in opens up almost unlimited modding capabilities. There are very few games that can boast as many unique mods, from small tweaks to total conversions, as Skyrim, all thanks to that engine. **However, with opportunity comes complexity.** Unlike Minecraft mods, Skyrim mods are not always self-contained: They interact and conflict with the vanilla game files as well as with each other. This means installing a large amount of mods in Skyrim requires an unusual degree of awareness and in-depth knowledge.

In the [**Introduction**](/embers/introduction/) we already spoke about expectations. Deciding to follow Embers means taking the long road and that you probably won't have a playable setup within the next few days - but in my honest opinion it is more than worth it. **Modding Skyrim can be incredibly rewarding**. What is it like to build that dream setup? Assemble your own collection, with hand-picked mods, customised through various tweaks, truly making it your own? There is a reason most of us veteran modders barely play the game anymore - we are too busy modding it.

It is this excitement that will carry you through the progress. Because it be frustrating. It can be grueling. Sometimes things just don't work and you don't understand why, and it takes a great deal of experimenting to figure out where you went wrong. Remember that this idea of creating your perfect Skyrim is why you're going through all of it.

*Although here's a word of warning: In years and years of modding Skyrim I have never reached that elusive peak, the moment of perfection. There is always something else, something that's missing, that isn't quite right yet. Modding Skyrim is chasing the dragon. ~~Get out of here while you still can.~~*

## Skyrim Version

Skyrim originally relased all the way in 2011 and after the release of all three DLC, it was repackaged as "Skyrim Legendary Edition" or **SLE** for short. In 2016, Bethesda release the remaster "Skyrim Special Edition", or **SSE** for short. Since then, SSE has slowly overtaken SLE for modding and is the better choice nowadays. Its upgraded 64bit engine is vastly more stable compared the SLE's old 32bit version. All major mods and tools have been ported, and most development is exclusively for SSE nowadays.

In order to follow Embers, you must own [**Skyrim Special Edition**](https://store.steampowered.com/app/489830/) on Steam.

The XBOX Game Pass and VR versions of Skyrim SE will not work.

## Folder Structure

Here's your first piece of advice: Keep your files in order. A well-organised modding directory where all files are consolidated in one place, always easy to find, is a big deal for quality of life. Throughout all lessons, I will be referring to this directory as **Your Modding Folder**. I recommend keeping it on a drive where space is not an issue (such as a general storage HDD). There is no point in wasting SSD space on this as it will not actually contain your mod setup.

- Please create a top-level or near top-level folder such as `F:\Skyrim Modding`.
- Within that new folder, create several more folders:

![Your Modding Folder](/Pictures/tpf/initial-setup/modding-folder.png)

I will explain the purpose of each of these folders (where it is not obvious) later on.

## Spring Cleaning

Now comes the boring part: Before we install anything, we must make sure that you have no left-over files from previous mod setups. Embers requires you to start from scratch and old mod files may be disruptive. 

If you have absolutely **never modded Skyrim** before, you may skip this and move on to the next step.

### Removing Skyrim

- First uninstall Skyrim SE through Steam.
- Navigate to where the game was installed which is probably `C:\Program Files x86\Steam\steamapps\common\`.
- If there is still a **Skyrim Special Edition** folder present, delete it.

When uninstalling the game through Steam, only vanilla files will be removed while mod-added files will stay put. That's why I recommend double-checking manually whether the installation folder is fully wiped.

Next we will take a look at the **Documents** folder. If you have never run Skyrim before, this folder will not exist for you and you can skip ahead to the next step.

- Navigate to `C:\Users\Your User Name\Documents\My Games\Skyrim Special Edition\`

This directory may contain multiple files and folders: The **Skyrim.ini** and **SkyrimPrefs.ini** are the game's primary configuration files, they will become very relevant later on. There may also be a **saves** folder which, you guess it, contains your save games. If you have any vanilla saves that you would like to hold on to, move the **saves** folder to `Your Modding Folder\Backups\` from where you can restore it anytime. Lastly the Documents folder may include mod-generated files such as logs.

- Make sure you have backed up any saves you want to keep.
- Delete the entire **Skyrim Special Edition** folder.

That's it. Skyrim SE is now completely removed from your system.

## Game Language

Skyrim supports a bunch of different languages natively, but mods typically don't. Many mods don't require translations in the first place and some of the ones that do have third-party translations available so that it's theoretically possible to play modded in Skyrim in a language other than English. However, this will complicate your setup immensely. Translations where available may be outdated or incomplete. They may not cover voice acting. They may not exist for some of your mods at all.

Ultimately translating any records (and certain textures!) untouched by existing patches plus fixing conflicts between translations and mods will add a hefty amount of work on top of everything else. I don't recommend it.

If your game is currently set to a language other than English, you can change this quickly in Steam. The English files will be downloaded immediately if you have the game currently installed, or the next time you install the game.

- Right-click **The Elder Scrolls V: Skyrim Special Edition** in your Steam games library.
- Select **Properties** and switch to the **Language** tab.
- Ensure that the language is set to **English**.

![Set language to English](/Pictures/tpf/initial-setup/skyrim-se-english.png)

## Installation Directory

