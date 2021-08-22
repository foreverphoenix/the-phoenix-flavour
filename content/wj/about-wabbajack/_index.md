---
title: "About Wabbajack"
weight: 1
type: docs
description: >
  Answering basic questions about the tool Wabbajack.
---

Welcome to my **Introduction to Wabbajack**. This section of the website is not for any guide or setup in particular, but a general introduction to the tool [Wabbajack](https://www.wabbajack.org/#/), how it works, what it can and cannot do, and, most importantly, how to use it. For the most part it assumes minimal modding knowledge in the reader and seeks to explain modding basics to the extent that they are required in order to understand Wabbajack.

These pages largely deal with Wabbajack for Skyrim, and more specifically Skyrim SE. However, most of the general Wabbajack facts apply to all Bethesda games supported by the tool.

If you are already familiar with Wabbajack and are looking only for setup instructions, skip to the [Setup](/wj/wj-sse/game-setup/) page.

## What is Wabbajack?

**Wabbajack** is an auto installer for mod lists. It can be used to duplicate one user's setup on another's PC without reuploading any mod files. The required mods are downloaded from the Nexus by Wabbajack and installed to match the original setup perfectly. This includes file edits of any kind. The installation process is fully automated for Nexus Premium users and requires only a few additional steps before a fully functional modded setup is ready to launch.

### Why should I use Wabbajack?

Wabbajack lists are not simply collections of download links. A great deal of work is required in order to make hundreds of individual mods play well together, including SSSEEdit patching, asset edits, custom generated LOD, etc. Assembling a large, internally consistent setup requires experience and knowledge in modding the game which is why Wabbajack is so popular. In the same way that a concert allows you to appreciate music that somebody else wrote and performs, a Wabbajack list allows you to enjoy an experience that you may not have the time and motivation to create for yourself. In return, the mods and theme of the list are determined by the list author, much like an artist would decide the songs played at a concert.

**Wabbajack lists are for you if:**

- you are more interested in playing the modded game than modding it,
- or if you cannot or do not wish to invest a great deal of time and effort into learning how to mod.

Some advanced users also use Wabbajack lists as a base for their own setups. This is generally not recommended for beginners.

### Is Wabbajack mod piracy?

In the wider Bethesda modding community (for Elder Scrolls and Fallout games), mod sharing and editing permissions have traditionally been very restrictive with few exceptions. In recent years the [Cathedral](http://wryemusings.com/Cathedral%20vs.%20Parlor.html) (essentially open source) approach to modding has gained more support among mod authors. However, repacks of files continue to be highly controversial.

What is usually referred to as "mod packs" in various modding communities like Minecraft's does not exist as such for Skyrim and other Bethesda games. Over the years, some repacks of files have cropped up on various obscure and often non-English sites, but since the files were reshared without permission from the author, they are considered mod piracy and are shunned by the wider community.

Wabbajack was created to eliminate the need for rehosting files. Thanks to the tool, setups can be shared without any repacks of the original files. Those are still downloaded as usual from their mod pages on the Nexus and used to build an exact copy of the list author's setup. **No mods are rehosted without permission, therefore Wabbajack lists do not consitute mod piracy.**

### Are Wabbajack lists inherently unstable?

They are not.

Wabbajack lists are created by experienced modders. Official lists undergo testing and quality control before they are published. Lists without custom conflict resolution, constant crashes, and other glaring issues would never make it onto the Gallery to begin with. Of course Wabbajack list authors are only human, so bugs and issues may always occur, just like mods may ship with issues the author overlooked at first. These issues, when found by the list author or reported to them by users, are then fixed. Thanks to the large amount of talent in the Wabbajack community among the mod and list authors present on the Discord server, getting to the bottom of a problem usually does not take very long.

The myth that Wabbajack lists are inherently unstable has been perpetuated by a handful of people in the past. One of them is Sinitar, a YouTuber and author of a "guide" himself. I have previously discussed the low quality of his "guide" in this [very lengthy essay](https://docs.google.com/document/d/1F1-6lF8dI4i2Zz8iT-bv_Ci1VO9MSU4MiSUrT5JqgHA/edit#heading=h.6al1rti6xsee). The short version is that Sinitar demonstrates in his "guide" that he knows very little about modding. Considering the fact that he makes a living off of modding and how well Wabbajack has been doing since it came out, it is clear that Sinitar considers Wabbajack a direct competitor and threat to his income, hence his dislike of the tool.

Additionally, there are some mod authors who claim that all mod lists are bad. This assertion typically also includes mod guides and Wabbajack lists. It is true that most *mod lists* (actual lists of download links with few or no instructions) are inherently broken unless the user actually goes through the manual editing not covered in the list itself which is where the true challenge in building a setup lies. However, major mod guides such as [Lexy's LOTD](https://lexyslotd.com/) and my own [The Phoenix Flavour](/tpf/introduction/) absolutely do contain manual patches and instructions for every other step required. The same goes for all official Wabbajack lists.

In short, the notion that all mod lists/guides and Wabbajack lists are bad or unstable by definition is a dangerous generalisation and demonstrably wrong for many of the guides and Wabbajack lists it encompasses.

## Using Wabbajack

There is no black magic involved in creating Wabbajack setups. They are built in [Mod Organizer 2](https://www.nexusmods.com/skyrimspecialedition/mods/6194) like any proper manual setup with the help of various additional tools such as the official Creation Kit and SSEEdit. What Wabbajack installs on your PC is exactly the same as what the list author has on theirs.

### Can I have multiple Wabbajack lists at the same time?

Each Wabbajack list is a self-contained portable instance of Mod Organizer 2. You can have as many of them installed at the same time as you wish, so long as each is within its own folder on your hard drive. Since most Wabbajack lists are fairly large (50GB+), the only restriction will eventually be disk space.

Setups do not interfere with each other except for in the root folder (the Skyrim installation folder) where certain files must always be installed. However, these files are typically part of every Wabbajack list (such as the Skyrim Script Extender and the SSE Engine Fixes preloader). If you want to run multiple Wabbajack lists with ENB or ReShade presets, consider using a preset manager to be able to easily swap between them.

### Why are lists under maintenance so much?

On the [Status Dashboard](https://www.wabbajack.org/#/modlists/status) on the Wabbajack website you can check any time which lists are online and which are currently unavailable. Wabbajack lists are frequently taken down my mod updates or removals. Often, the tool will autoheal lists and binary patch the updated copy of the mod in question to be identical with the version in the list author's setup, but this is not always possible.

Because of the high frequency of updates in the Skyrim modding community, a mod list can be outdated within minutes of an update releasing, or be taken down overnight when a mod is removed. Please be patient with the list authors and keep an eye out for updates or announcements (most have their own Discord servers). They will likely already know the list is down and bring it back as soon as they are able to.

### Can I edit Wabbajack lists?

Theoretically, yes.

**Editing a Wabbajack setup voids your right to get any support for it.** This is `!rules11` on the Wabbajack Discord server and applies to all Wabbajack lists with very few exceptions. Similar rules are present in most sub-communities and Discord servers for individual lists.

That being said: It is entirely possible to edit Wabbajack lists. What you install is simply another instance of Mod Organizer 2 with the list set up within it, so you can edit literally everything about it. You can add, tweak, or remove mods however you like *if you know what you are doing*. As mentioned before, advanced users frequently use Wabbajack lists as base for their own setups. However, this requires a good deal of modding experience, at the very least knowing how to edit plugins in SSEEdit and mod order management. Because the vast majority of Wabbajack users does not have this knowledge, the rule against support for modified setups had to be put in place to begin with.

To reiterate: **Wabbajack lists are not simply collections of mods.** They are *heavily* edited. Often included mods were made by the list author from assets sourced from various other mods, binary-patched for the end-user. There is typically no documentation for the edits the list author made as that would be a huge undertaking and all but double the amount of work required. I know this from experience thanks to the modding guide I maintain which does include detailed documentation for every single change. Editing a Wabbajack setup can be quite difficult, in addition to the fact that modding is rather complex to begin with.

In summary, editing Wabbajack lists is possible, but not easy, and there is no support for it.

### Can I use LOOT on Wabbajack lists?

Running LOOT on your load order will count as editing the setup and you will no longer receive support.

LOOT is not a perfect solution for plugin sorting. Most Wabbajack list authors prefer load order manual sorting using SSEEdit which will result in a far better optimised load order than running LOOT. There are some Wabbajack lists that utilise LOOT with custom rules (which are determined, once again, using SSEEdit).

**In most cases, if you run LOOT, all you do is completely mess up the existing load order and likely break the setup.**

There are some exceptions to this: lists that utilise LOOT and custom rules to manage the load order and support optional mods. Please refer to your list's documentation. If it explicitly instructs you to sort with LOOT after enabling optional mods, the rules set up by the list author will ensure all plugins are sorted correctly.