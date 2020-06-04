---
title: "Removing ENB"
weight: 10
type: docs
description: >
  Instructions to completely uninstall ENBSeries.
---

## Considerations

#### Performance

There are two reasons for removing ENBSeries: Either your machine has such low specs you cannot possibly run a preset while preserving an acceptable framerate, or you are among the few preferring vanilla visuals. Either way, by removing ENB you will most likely improve the game’s performance significantly.

Keep in mind that it is possible to tweak ENB presets or swap to a less performance-hungry preset like The Truth ENB.

You can also use the hotkey ingame to disable ENB completely without removing it outright. This will give you an idea of how the game would look and feel like without it. The default hotkey to toggle the effect is F12.

#### What you will miss out on

The obvious disadvantage of removing ENB is the improved visuals, snappier shadows, much improved Ambient Occlusion, more saturated colours and a bunch of ENB-exclusive features.

One of those features is Complex Particle Lighting which is required for mods such as **ENB Light** and Rudy’s **More Lights for ENB** series of which most are included in The Phoenix Flavour. On the upside, you will also be able to lower the particle count when no longer using ENB Light which may improve performance further.

#### Personal recommendation

If you are considering to remove ENB because of the performance impact, I would definitely urge you to try other presets or tweak your  own to tone down the FPS loss. On all except the weakest systems, you should be able to reach mostly stable 60FPS with a (tweaked) ENB preset.

## Uninstalling ENBSeries

* Open **ENB Man** (which we used to set up ENBSeries).
* Double-click the **Skyrim SE** profile to open it.
* Click the red button **Ø** at the bottom to remove all ENB related files (binaries, INIs, preset) from your root folder.
* Close ENB Man.

## Related Mods

Disable the following mods in your mod order:

- ENB Light – QuickLight Patch
- Rudy HQ – More Lights for ENB SE – Soul Gems for RUSTIC
- Rudy HQ – More Lights for ENB SE – Moths
- Rudy HQ – More Lights for ENB SE – Deathbells and Nirnroots
- Rudy HQ – More Lights for ENB SE – Chaurus Eggs and Sacs
- Rudy HQ – More Lights for ENB SE – Bthardamz
- ENB Particle Lights – Dwemer Lanterns
- ENB Helper SE

> ENB Light cannot be disabled as it is required by the CRP. 
>
> The Skyrim Particle Patch (aka ENB Particle Patch) contains many improvements that you will benefit from with or without ENB which is why it should not be deactivated.

## INI Tweaks

#### INI Editor

Without ENBSeries, there are several graphical enhancements that can be forced directly in the game. These will give better performance (with lower quality) than similar effects that could be forced through ENB.

In Mod Organizer 2, go to **Tools** > **INI Editor** in order to edit your INI files directly through MO2’s interface.

#### Ambient Occlusion

You now have the option to use Skyrim’s inbuilt Ambient  Occlusion (which has a performance impact of its own and does not look as good as ENB AO). Enabling Ambient Occlusion may result in a performance loss but not nearly as much as enabling ENB with AO would.

In the [Display] section of your **SkyrimPrefs.ini**, change the following:

`bSAOEnable=1`

#### Particles

ENB Light (and meshes utilising the ENB Complex Particle Lights  feature in general) required you to increase your particle count for  better visuals which may also potentially impact performance so we will reverse this.

In the [Particles] section of your **SkyrimPrefs.ini**, change the following:

`iMaxDesired=2000`

## Potential Replacements

#### IMAGINATOR

Even without ENBSeries there are ways to tweak the lighting and colours in your game to your liking. With the default guide setup, you can use the **Obsidian Weathers** MCM to tweak the general tone and colour settings. There are several presets to choose from.

There is also the mod [IMAGINATOR](https://www.nexusmods.com/skyrimspecialedition/mods/4577) by Gopher, created to replace the colour customisation ENB offers. While it should not have a performance impact at all, it is not comparable to ENBSeries. For some people it may still be worth the performance gain. Feel free to try it out.

Please note that IMAGINATOR is a not officially included in the guide, meaning I will provide no installation instructions and no support for issues with the mod.

#### ReShade

Unlike ENBSeries, ReShade was not specifically created for Skyrim SE and has no way to interact with the engine for advanced effects. It is however a very capable, customisable and performance-friendly FX injector that may replace ENBSeries for those with weaker hardware (or different preferences with regards to visuals).

The [ReShade Framework](https://reshade.me/) is easy enough to install, however depending on your chose preset, you may require a certain version of it, or a specific set of shaders. To find presets, just search for **Reshade** on the  Special Edition Nexus. A word of warning though: There are still plenty of ENB-ReShade presets floating around which were made for both ENBSeries and ReShade to complement each other. Take care and read the mod page before installing.

Creating your own preset is arguably easier to do than it is with ENBSeries. ReShade can also be edited and customised ingame.
