---
title: "Quick Start"
weight: 2
type: docs
description: >
  Summary of my approach when building a setup.
---

## Preface

On this page I am detailing <u>my process</u> when building a new modded setup. This is a general guideline as opposed to a set of hard-and-fast rules, and how you approach building a setup can (should!) depend heavily on what you specifically intend to create. That being said, I hope it can serve as a blueprint to get you started.

The Quick Start guide is linking to and drawing on various other articles and pages on the site.

<u>This section is a work-in-progress.</u> I am hoping to fill out the various steps with additional links, instructions, and tips as I go, but am focusing on completing the general framework first.

### Limitations

The Quick Start guide is an overview of my process and a blueprint for building a new setup. **It does not provide an introduction to modding basics** and expects you to know how to use SSEEdit, create patches, and modify assets.

{{< alert color="info" >}}If you are more interested in a comprehensive step-by-step guide to modding from start to finish, I recommend checking the [Beginner's Guide](/skyforge/beginners-guide/step1/) instead.{{< /alert >}}

Recommended reading:

- [Asset Basics](/skyforge/knowledge-base/asset-basics/)
- [Asset Management](/skyforge/knowledge-base/asset-management/)
- [Plugin Basics](/skyforge/knowledge-base/plugin-basics/)
- [References](/skyforge/knowledge-base/references/)
- [ESL Plugins](/skyforge/knowledge-base/esl-plugins/)
- [Conflict Management](/skyforge/knowledge-base/conflict-management/)
- [ModGroups](/skyforge/knowledge-base/modgroups/)

## Initial Setup

A new setup always begins with a good amount of spring-cleaning and basic steps.

Use this time to think about mods and themes for the setup you want to build: Are you going for heavily overhauled visuals with tough survival gameplay? Are you interested in EnaiRim extravaganza with Legacy of the Dragonborn? Are you looking to try every quest mod on the Nexus? You still have plenty of time to make up your mind, but think about your general direction while you build the foundation of your setup.

1. Perform a [Clean Install](/skyforge/modding-resources/clean-install/) of Skyrim SE.
   - *Remember to perform a [Skyrim Version Check](/skyforge/modding-resources/skyrim-version-check/) and [downgrade](/skyforge/modding-resources/downgrade-skyrim/) if necessary.*
2. Set up a new instance of [Mod Organizer 2](/skyforge/tool-setup/mo2/).
   - *Also check the [MO2 Plugins](/skyforge/knowledge-base/mo2-plugins/) page for recommended extensions.*
3. [Import your Creations](/skyforge/modding-resources/managing-creations/) into Mod Organizer 2.
    - *If you are on the fence about Creations, read the section below.*
4. **Optional:** Install [Root Builder](/skyforge/tool-setup/root-builder/) for Mod Organizer 2.
    - *Root Builder is required for various modules/articles available here and I highly recommend installing it.*
5. Install the [Skyrim Script Extender](/skyforge/modding-resources/skyrim-script-extender/) and related mods.
6. Set up a [Tools Folder](/skyforge/tool-setup/tools-folder/) and install necessary tools (see section below).

### Creation Club

At this point everyone owns at least the four free Creations (Fishing, Survival, Rare Curios, Saints & Seducers), though not everyone picked up the remaining Creations or the full Anniversary Edition DLC.

Forgoing the AE DLC should not negatively impact your modding experience but skipping the four free Creations is difficult as an increasing amount of mods, including the [Unofficial Skyrim Special Edition Patch](https://www.nexusmods.com/skyrimspecialedition/mods/266), now require them. Skipping the USSEP significantly complicates matters simply because it is in turn required by a vast amount of mods.

Even if you are completely opposed to using the four free Creations, I recommend installing them. Survival Mode can be easily neutralised by [disabling the prompt](https://www.nexusmods.com/skyrimspecialedition/mods/59049) and the mediocre Saints & Seducers quest can be completely replaced with [a full remake](https://www.nexusmods.com/skyrimspecialedition/mods/72772). Finally, the Fishing quests can be removed by installing the [reduced cut](https://www.nexusmods.com/skyrimspecialedition/mods/80379). This may be a good compromise between removing poor quality Creation content from your game while still being able to keep the plugins as master files to dependent mods like the USSEP.

### Tools

The only tool that everyone should install before touching mods is [SSEEdit](/skyforge/tool-setup/). Yes, you need it, no matter what. Most other tools are situational and can be installed later on when they are needed.

For now, I would recommend setting up at least the following:

- [SSEEdit](/skyforge/tool-setup/)
- [Creation Kit](/skyforge/tool-setup/creation-kit/)
- [Cathedral Assets Optimizer](/skyforge/tool-setup/cao/)
- [Bethesda Archive Extractor](/skyforge/tool-setup/bae/)

## Basic Mods

If, at this point, you are still uncertain about central mods and themes for your new setup, there is no need to worry as there is more baseline work to be. What is considered an "essential" mods is actually more subjective and controversial than one might assume which is why I largely give recommendations.

- Recommendations: [SkyUI](/skyforge/mod-recommendations/skyui/)
- Recommendations: [Utilities & Frameworks](/skyforge/mod-recommendations/utilities-frameworks/)
- Recommendations: [Essential Mods](/skyforge/mod-recommendations/essential-mods/)
- Recommendations: [Console Improvements](/skyforge/mod-recommendations/console-improvements/)

As you begin to build up your mod order, try to keep it nice and clean by making heavy use of **separators**. If you do not have a system of your own for sorting mods, you can refer to [mine](/skyforge/mod-recommendations/separators/) for inspiration.

## Standard Procedure

In case it needs to be said:

- Read (or at least skim) the mod page for every mod you install. <u>Check the Requirements tab.</u>
- Check the comment section for pinned comments and read some of the newest comments.
- Check the bugs section.

Every time you add a new mod **determine if the mod does what you want it to do in a way that is sensible.** You should have checked through <u>every single mod</u> you install eventually. Look at the plugins in SSEEdit and the assets in Mod Organizer 2. Manage conflicts when they appear.

### Plugin Management

There is no exact rule on often you should hop into SSEEdit, but doing it every ten or so plugins can be helpful. Remember to [apply a filter](/skyforge/modding-resources/filter-for-conflicts/) to make conflicts better visible, but also remember that conflicts are not the sole cause of issues and that you should look at all records, not just conflicting ones.

When you discover conflicts or potential consistency issues, remember to check the Nexus (including patch collections) for pre-existing patches. If none exist to solve your problem, you can either create it yourself, remove one of the mods, or ignore the problem if it is minor enough.

I highly recommend creating **small patches** and [ModGroups](/skyforge/knowledge-base/modgroups/) as you work through your load order. Keep the 256 ESM/ESP limit in mind and [ESL-ify](/skyforge/modding-resources/creating-esl-plugins/) plugins when possible.

Install [Mod Load Order Checker](/skyforge/tool-setup/mod-load-order-checker/) to keep track of and fix out-of-order plugins.

If you are wondering about **plugin cleaning**, check [the article on the topic](/skyforge/knowledge-base/cleaning-plugins/). Generally, I would only recommend cleaning if you intend to use DynDOLOD NG.

{{< alert color="info" >}}It is also possible to install the majority of your mods first before really diving into SSEEdit, sorting out your current list of plugins by adjusting the load order and creating patches, before adding to it more slowly. Do whatever works best for you.{{< /alert >}}

### Asset Management

### Ingame Testing

Ingame testing to detect problems is never sufficient to build a modded setup. You <u>cannot</u> avoid SSEEdit.

That being said, I highly recommend the occasional `coc riverwood` to ensure that the game properly launches - if not, you should have a limited amount of possible culprits if you do it often enough which may speed up the troubleshooting process.

Ingame testing is crucial for building the visual overhaul of a setup. You will want to spend a good amount of time running around Skyrim to see if you like your current combination of mods.

Otherwise, I recommend ingame testing as one of the last steps in building your setup, long after you have worked through SSEEdit. There are many issues that you will never notice in SSEEdit - mostly related to clipping objects or inconsistencies between mods - that you can best see in the actual game.

## Visual Baseline

If you care at all about visuals, I recommend creating a solid baseline before moving on to the core of your list. Your combination of weather + lighting overhauls with ENB or Community Shaders will determine the overhaul atmosphere and style of the visuals.

The first decisions you will have to make are:

- Decide if you want parallax / complex materials.
- Decide if you want to use ENB or Community Shaders.

### INI Configuration

Install [BethINI](/skyforge/tool-setup/bethini/) and refer to the [INI Configuration](/skyforge/modding-resources/ini-config/) page for instructions to modify the vanilla INI files.

More information can be found in the [INI Files](/skyforge/knowledge-base/ini-files/) and [Resolution](/skyforge/knowledge-base/resolution/) articles.

### Important Mods

Building a visuals setup is obviously a highly subjective affair. My own visuals-only setup clocks in at around 1,000 mods which is, of course, somewhat overkill. However, there are no all-in-one solutions for visual overhauls either and you will always have to do your own mixing and matching.

For the time being, I recommend installing the following:

- [Static Mesh Improvement Mod](https://www.nexusmods.com/skyrimspecialedition/mods/659)
- A major texture pack and/or separate landscape textures
- A water overhaul
- A tree overhaul
- A grass overhaul
- (A) snow and ice overhaul(s)

This will give the landscape of Skyrim a proper glow-up.

You can get approximately 70% of the visual fidelity by installing the mods above, generating LODs, and adding lighting overhauls on top. The remaining 30% mostly consist of handpicked texture and mesh replacers for details.

### First LOD Generation

With trees and landscape textures in place, I recommend generating a temporary set of LODs <u>for the Tamriel worldspace only</u>. This does not take very long and gives you a decent preview of your eventual visual setup as well as the accompanying performance impact that you should expect.

Make sure you have LOD generation resources for landscape textures and optionally 3D trees installed (where available) before generating LODs.

Set up [SSELODGen](/skyforge/tool-setup/sselodgen/) and [DynDOLOD](/skyforge/tool-setup/dyndolod/), then refer to the [LOD & Occlusion](/skyforge/modding-resources/lod-occlusion/) article for generation instructions.

{{< alert color="info" >}}I recommend skipping **Occlusion** for now. You can generate it during the finalisation steps.{{< /alert >}}

Jump ingame and have a look around afterwards. This is a good time to see how well your distant landscape blends (snow in particular can be difficult to perfect) and what your performance with your chosen tree LOD settings or grass overhaul is like.

### Weather & Lighting

The overhauled landscape and improved LODs offer an excellent backdrop for trying various weather and post-processing combinations. You can switch between them painlessly while getting a good idea of what the finished setup will look like.

1. Settle on a lighting overhaul. Load it last during testing and do the conflict resolution later on when you have made your decision.
2. Based on your preferences and the performance you are getting (tested in the previous step) consider whether you want an ENB, Community Shaders and/or ReShade, or no post-processing at all.
3. Try various weather overhauls. If using ENB/CS/ReShade, be sure to pair presets with matching weather (and lighting) overhauls.

**Take your time with this step.**

The weather + lighting + post-processing combination that you choose will largely determine the overall tone and mood of your setup, and finding a combination that is perfect *to you* can be difficult. Remember that any ENB or ReShade preset can be customised to your preferences, provided you are willing to invest some time in trial & error.

{{< alert color="info">}}You can easily swap to a different weather overhaul or post-processing preset should you wish to. However, note that swapping out a lighting overhaul is a great deal more work on account of the required patching.{{< /alert >}}

## List Concept

You have created the skeleton of your setup. Now it is time to put some meat on those bones.

At this point, it is time to consider what specifically you wish to achieve with your setup, picking a concept or theme for your list. Of course, you can also set yourself multiple goals, depending on your modding capabilities.

There are three basic types of setups:

- **Vanilla-like:** A vanilla-like (or "vanilla-plus") setup seeks to improve the vanilla game without changing it significantly. This typically entails many bug fixes, quality of life improvements, lightly overhauled graphics, and the odd gameplay tweak.
- **Consistency:** A setup focused on consistency may go beyond vanilla by adding major overhauls, new gameplay mechanics, and new content, but always does so with an emphasis on consistency with the vanilla game and other mods.
- **New Game:** A setup intended to create an entirely new game drastically changes Skyrim in terms of visuals, gameplay, and/or core theme. This is what most people gravitate to after inevitably growing bored with vanilla.

To give you an example, SimonMagus' gameplay overhauls ("SimonRim") modify vanilla mechanics while focusing on *consistency* with each other and the vanilla game. Meanwhile, EnaiSiaion's gameplay overhauls ("EnaiRim") focus on adding colourful builds that feel like playing a *new game*.

{{< alert color="info" >}} It may help to first consider whether you are trying to improve the vanilla game, overhaul it while staying true to the original theme, or build an entirely new experience.{{< /alert >}}

### Themes

To give you some inspiration, here are a few common themes:

- Specific (modular) gameplay overhauls like Requiem, EnaiRim, or SimonRim.
- Legacy of the Dragonborn, filling the big museum. LOTD is a mod that setups must be built around.
- Survival / immersion, "hardcore" difficulty, slow gameplay with needs and "realistic" mechanics.
- A Nordic or Dark Folk touch with a darker ambience and matching soundtrack and equipment replacers.
- A very particular visual style like near-photorealism, for gameplay or for screenarchery.
- Inspiration from a different game, like Dark Souls combat or Dragon Age roleplaying elements.
- The extremely horny NSFW side of things (I am not judging).

A setup is easier to build if you have clear intentions and ideally a playstyle in mind. For example, there is no point in painstakingly integrating hundreds of new spells and scrolls if you are going to play stealth archer anyway.

Generally, a high degree of thematic coherence and consistency will make for a better setup. On the other hand, there is nothing stopping you from throwing all the coolest mods together to try them all out in a kitchensink list.

{{< alert color="warning" >}}You can do <u>anything</u> but avoid trying to do <u>everything</u>. Picking out a clear goal and intent will greatly increase the chances of achieving a solid setup, especially for beginners. Narrow the scope. Figure out what you want and focus on that.{{< /alert >}}

### Priorities

It should go without saying, but start at the beginning.

If you are building a setup around Legacy of the Dragonborn, install that mod first and think about which content mods with integration patches you wish to add. If you are building a setup focused around visuals then dive straight back into the hand-picking insanity.

Set up the essential mods that will be at the heart of your setup to realise your theme before branching out. Experiment. Try things out. Do not worry too much about SSEEdit until you run into issues that must be fixed first. Jump into the game frequently to check your new combat animations or clover mesh replacer. This is the fun part!

## The Setup

After picking out your central theme(s) and sketching them out, the bulk of the work begins. Once again, how you should approach this segment is highly subjective and I can only give you my personal preferences.

Because building a (big) setup is a lot of work, I recommend breaking it down into bite-sized bits, like:

- Interface mods (unless you are happy with SkyUI)
- A suite of combat mods (which obviously require ingame testing)
- Balancing/gameplay overhauls (lots of SSEEdit work)
- Player and NPC appearance overhaul
- ...

You can refer to [my separator setup](/skyforge/mod-recommendations/separators/) for additional groups of mods.

## Finalisation

The truth is that you will probably never get to "the" end. If you enjoy building a setup, chances are you will keep tinkering indefinitely with some breaks when you inevitably burn out before diving back into it a few weeks or months later. That is the case for myself and many others I know.

On the other hand, there comes a time where you should <u>stop</u> and wrap up if you ever want to play. A number of steps need to be followed after all mods are installed to complete your setup.

**Conflict resolution and consistency patching should be completed at this point.**

1. With all mods installed you can now run [Synthesis](/skyforge/tool-setup/synthesis/) patchers for mods which require them.
2. If you chose to regenerate facegen for all NPCs, this is the time to do it. Instructions are [here](/skyforge/modding-resources/regenerating-facegen/).
3. (Re-)run Nemesis if you installed any mods that add new animations.
4. Regenerate [LODs & Occlusion](/skyforge/modding-resources/lod-occlusion/).