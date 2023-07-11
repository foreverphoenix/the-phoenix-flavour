---
title: "Building a setup"
weight:
type: docs
description: >
  About my process when building a setup.
---

## Preface

On this page I am detailing my process when building a new modded setup. This is more intended as a general guideline rather than a set of hard-and-fast rules and how you approach building a setup can (should!) depend heavily on what you specifically intend to create. That being said, I hope this can serve as a blueprint in case you are unsure how to proceed.

## Initial Setup

A new setup always begins with a good amount of spring-cleaning and basic steps.

Use this time to think about mods and themes for the setup you want to build: Are you going for heavily overhauled visuals with tough survival gameplay? Are you interested in EnaiRim extravaganza with Legacy of the Dragonborn? Are you looking to try every quest mod on the Nexus? You still have plenty of time to make up your mind.

1. Perform a [Clean Install](/bg/additional-modules/clean-install/) of Skyrim SE.
2. Set up a new instance of [Mod Organizer 2](/bg/tool-setup/mo2/).
3. [Import your Creations](/bg/additional-modules/managing-creations/) into Mod Organizer 2.
    - *If you are on the fence about Creations, read the section below.*
4. **Optional:** Install [Root Builder](/bg/additional-modules/root-builder/) for Mod Organizer 2.
    - *Root Builder is required for various modules/articles available here and I highly recommend installing it.*
5. Install the [Skyrim Script Extender](/bg/additional-modules/skyrim-script-extender/) and related mods.
6. Set up a [Tools Folder](/bg/tool-setup/tools-folder/) and install necessary tools (see section below).

### Creation Club

At this point everyone owns at least the four free Creations (Fishing, Survival, Rare Curios, Saints & Seducers), though not everyone picked up the remaining Creations or the full Anniversary Edition DLC.

Forgoing the AE DLC should not negatively impact your modding experience but skipping the four free Creations is difficult as nn increasing amount of mods, including the [Unofficial Skyrim Special Edition Patch](https://www.nexusmods.com/skyrimspecialedition/mods/266), now require them. Skipping the USSEP significantly complicates matters simply because it is in turn required by a vast amount of mods.

Even if you are completely opposed to using the four free Creations, I recommend installing them. Survival Mode can be easily neutralised by [disabling the prompt](https://www.nexusmods.com/skyrimspecialedition/mods/59049) and the mediocre Saints & Seducers quest can be completely replaced with [a full remake](https://www.nexusmods.com/skyrimspecialedition/mods/72772). Finally, the Fishing quests can be removed by installing the [reduced cut](https://www.nexusmods.com/skyrimspecialedition/mods/80379). This may be a good compromise between removing poor quality Creation content from your game while still being able to keep the plugins as master files to dependent mods like the USSEP.

### Tools

The only tool that everyone should install before touching mods is [SSEEdit](/bg/tool-setup/). Yes, you need it, no matter what. Most other tools are situational and can be installed later on when they are needed.

For now, I would recommend setting up at least the following:

- [SSEEdit](/bg/tool-setup/)
- [Creation Kit](/bg/tool-setup/creation-kit/)
- [Cathedral Assets Optimizer](/bg/tool-setup/cao/)
- [Bethesda Archive Extractor](/bg/tool-setup/bae/)

## Basic Mods

If, at this point, you are still uncertain about central mods and themes for your new setup, there is no need to worry as there is more baseline work to be. What is considered an "essential" mods is actually more subjective and controversial than one might assume which is why I largely give recommendations.

- Recommendations: [Utilities & Frameworks](/bg/recommended-mods/utilities-frameworks)
- Recommendations: [Essential Mods](/bg/recommended-mods/essential-mods)

As you begin to build up your mod order, try to keep it nice and clean by making heavy use of **separators**. If you do not have a system of your own for sorting mods, you can use [mine](/bg/recommended-mods/separators/) for inspiration.

## Standard Procedure

In case it needs to be said:

- Read (or at least skim) the mod page for every mod you install. <u>Check the Requirements tab.</u>
- Check the comment section for pinned comments and read some of the newest comments.
- Check the bugs section.

Every time you add a new mod **determine if the mod does what you want it to do in a way that is sensible.** You should have checked through <u>every single mod</u> you install eventually. Look at the plugins in SSEEdit and the assets in Mod Organizer 2.  Manage conflicts when they appear.

### Plugin Management

There is no exact rule on often you should hop into SSEEdit, but doing it every ten or so plugins can be helpful.

When you discover conflicts or potential consistency issues, remember to check the Nexus (including patch collections) for pre-existing patches. If none exists to solve your problem, you can either create it yourself, remove one of the mods, or ignore the problem if it is minor enough.

I highly recommend creating **small patches** and **ModGroups** as you work through your load order.

{{< alert color="info" >}}It is also possible to install the majority of your mods first before really diving into SSEEdit, sorting out your current list of plugins by adjusting the load order and creating patches, before adding to it more slowly. Do whatever works best for you.{{< /alert >}}

### Asset Management

### Ingame Testing

Ingame testing is never sufficient to build a modded setup. You <u>cannot</u> avoid SSEEdit.

That being said, I highly recommend the occasional `coc riverwood` to ensure that the game properly launches - if not, you should have a limited amount of possible culprits if you do it often enough which may speed up the troubleshooting process.

Ingame testing is crucial for building the visual overhaul of a setup. You will want to spend a good amount of time running around Skyrim to see if you like your current combination of mods.

Otherwise, I recommend ingame testing as one of the last steps in building your setup, long after you have worked through SSEEdit. There are many issues that you will never notice in SSEEdit - mostly related to clipping objects or inconsistencies between mods - that you can best see in the actual game.

## Visual Baseline

If you care at all about visuals, I recommend creating a nice baseline before moving on to the core of your list. Your combination of weather + lighting overhauls with ENB or Community Shaders will determine the overhaul atmosphere and style of the visuals.

The first decisions you will have to make are:

- Decide if you want parallax / complex materials.
- Decide if you want to use ENB or Community Shaders.

### INI Configuration

## Central Theme