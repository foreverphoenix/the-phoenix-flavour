![Logo](Pictures/Logo%20Mockup%202.png)

Table of Contents
- [Preface](#preface)
- [Introduction to Modding](#introduction-to-modding)
  - [What are mods?](#what-are-mods)
  - ["Modding"](#modding)
  - [Skyrim LE vs Skyrim SE](#skyrim-le-vs-skyrim-se)
  - [The Script Extender](#the-script-extender)
  - [A Note on Consoles](#a-note-on-consoles)
  - [The Creation Club](#the-creation-club)

# Preface

SkyPlus is intended as a comprehensive introduction for newcomers to the Skyrim modding scene, supplying you with all the basic modding knowledge as well as the first stable foundation to build your own setup on top. It is required for my full guide, The Phoenix Flavour, but works perfectly fine as a base for a personal setup or any other guide that was based on it.

We will begin with a quick **Introduction to Modding** that describe modding for Skyrim SE in broad strokes. Technical details follow in the **Modding Basics** section. The **SkyPlus Setup** contains the actual instructions so that you can get started.

> **You need to read everything.** Later sections will expect you to know about facts established in earlier ones.

# Introduction to Modding

## What are mods?

Mods are fan-made modifications that change or add to the original game. It can do anything from changing the texture of apples to adding a massive new worldspace.

On the [Nexus](https://www.nexusmods.com/), the primary hub for mods, there are around **85.000** mods available for Skyrim and Skyrim Special Edition (including duplicates). Some of them are absolutely essential, for some better alternatives exist, some are very specific patches, some are redundant, outdated or outright broken. Some require the Script Extender or other mods. Some need additional steps to be completed before they work properly.

Navigating the sheer amount of mods out there requires time, patience and some understanding of how mods work - or a modding guide that takes you through the process.

## "Modding"

The term "modding" is a fairly ambiguous one: It can mean both “**creating mods**” as well as “**installing mods**”. 

- **Creating mods** is fairly complex. The Creation Kit (Bethesda's official modding tool) is notoriously clunky and prone to crashes (until at least the Skyrim SE version got fixed by a modder). Writing scripts in the engine’s scripting language Papyrus requires a good deal of prior coding experience. Script extender plugins are written in C++. Tinkering with textures requires at least basic skills in Photoshop, Gimp or a similar program. Modelling (editing or creating new meshes) requires very specific software like Blender which is extremely complex and cannot be learned overnight.

- **Installing mods** is quite a bit easier and certainly more accessible - in fact, when it comes down to it, the only hard requirement is the ability to read closely. "Casual" modding - installing perhaps five or ten interesting mods - does not really require any extra steps, it is enough to drop all files into a certain folder. Depending on what these five or ten mods do, this may work out perfectly, but for anything more than that, you will have to go the extra mile, and you will have to invest time.

In order to learn how to create mods, one needs to know how mods work, what components they are made of and how they can be edited. On the other hand, installing mods is not usually a matter of "plug and play" as some instructions would have you believe, at least not if you are using more than three or four mods. Eventually the line between the two will blur, and the better you get at installing mods and making them work together, the closer you get to actually making mods yourself.

## Skyrim LE vs Skyrim SE

The original game released in 2011 – **The Elder Scrolls V: Skyrim** – was re-released later as the **Legendary Edition** packaged with all three DLCs (Dawnguard, Hearthfire, Dragonborn). This version of the game is known as **Skyrim LE**, Classic Skyrim or Oldrim, built on an older 32-bit version of the Creation Engine.

In 2016, Skyrim was re-released in remastered form as **The Elder Scrolls V: Skyrim - Special Edition**, now based on an updated and improved 64-bit version of the Creation Engine with marginally better visuals and substantially improved stability. It is referred to as **Skyrim SE** and was released alongside the dreaded Creation Club but revitalised the modding scene in spite of initial doubts.

Several years after the release of the Special Edition, the modding community has long caught up. With many new mods available exclusively for this version of the game as well as stability being much so easier to achieve, Skyrim Special Edition is beyond a doubt the way to go.

## The Script Extender

The most important tool / resource / mod available for Skyrim is the **Skyrim Script Extender**, or **SKSE** for short. The Script Extender for Skyrim Special Edition is usually referred to as **SKSE64**.

While the Creation Kit allows modders to work with a tool set similar to what the developers used, the Script Extender goes a step further and hooks directly into the engine. In order for it to function properly, the game must be run through the Script Extender executable instead of the original launcher. As the name suggests, it "extends scripts", or more specifically the available functions modders can call in their custom scripts. It is not exactly a mod but rather a modder’s resource.

Through the added functionality of the Script Extender, mods like the interface overhaul **SkyUI** and its **Mod Configuration Menu** component are made possible in the first place. Many features that would otherwise be difficult to implement can be realised through Script Extender plugins such as the mod **SSE Engine Fixes** which rewrites sections of the Creation Engine itself.

The Script Extender and any SKSE plugin is **version dependent** and only works with the game version it was made for. For example, SKSE64 2.0.17 is only compatible with Skyrim SE 1.5.97, and will not work with any other version of the game.

## A Note on Consoles

Since Skyrim Special Edition (and Fallout 4) modding is "supported" on consoles (XBOX One and Playstation 4) through Bethesda’s own platform. However, the available options as far as mod installation and configuration go are so severely limited on consoles that it isn’t even comparable to what is possible on PC.

To give a few examples:

* **No assets on PS4.** Thanks to Sony, only plugins (a central component of many mods) can be installed on Playstations. Without the ability to include scripts, textures, meshes or other loose files, mod authors are severely limited in their options.
* **No script extender.** Most complex mods will never work for consoles because they require SKSE. Others need workarounds and extremely jarring ingame items for their configuration. You cannot install any mods that fix engine bugs.
* **No tweaking of mods.** There is no way to remove or edit files from a mod (unless you are the author and repackage it on PC), or edit the INI files of either the game or mods.
* **Limited space.** If memory serves, there is about 5GB of space for mods on the XBOX. Compare this to a decent modded setup on PC which easily cracks 100GB.
* **Limited hardware.** Graphic improvements are possible but only on a very small scale due to hardware restrictions. Post processing injectors like ENBSeries or even ReShade cannot be installed.

If you truly intend to get into modding, you need a PC. There is simply no way around it. And yes, you can play modded Skyrim with a controller on PC.

## The Creation Club

For all the engine improvements we enjoy on the Special Edition, there is a catch and it's called "Creation Club". Additional content for Skyrim SE made by Bethesda devs or independent contractors (many of them well-known modders) is sold for "credits" which must be bought with real-world money. While Beth goes through great pains to argue that these "creations" are not in fact paid mods, they are certainly micro transactions in a single-player game.

The most immediate problem with the Creation Club is that nobody can ignore it. Even those who are totally uninterested in buying micro DLC for Skyrim will be affected every time the shop is updated with more content as these updates (for reasons unknown) require Bethesda to update the game executable (SkyrimSE.exe). This in turn requires the Script Extender and all SKSE plugins to be updated, a huge inconvenience for all mod authors involved.