---
title: "01 About ENB"
weight: 1
type: docs
description: >
  Introduction to ENBSeries with a list of advantages and disadvantages.
---

## 1.1 What is ENBSeries?

ENBSeries is a post-processing injector by Boris Vorontsov. Unlike ReShade, it is not universal but built for specific games and hooks directly into the engine. Effects are therefore highly advanced and specific to each games. ENB is also capable of fixing bugs and improving performance plus it offers additioanl features such as VSYNC, a screenshot hotkey, and a toggleable FPS counter.

The effects vary in their performance-intensity. A full preset, especially when Skyrim is run on high resolutions, can bring high-end PCs to their knees. Fortunately, Skyrim SE with its generally improved performance runs a great deal better with ENBSeries presets and 60FPS+ on a reasonable resolution (1080p) are comfortably attainable on most machines.

- <span style= "color: green"><i class="fas fa-plus-circle"></i></span> The visual improvements are immense. They can profoundly change the feel of Skyrim.
- <span style= "color: green"><i class="fas fa-plus-circle"></i></span> Everything. The performance impact can be dampened by turning off hard-hitters such as Ambient Occlusion.
- <span style= "color: green"><i class="fas fa-plus-circle"></i></span> You can tweak or swap presets, or uninstall ENBSeries entirely at any time. It does not affect savegames at all.
- <span style= "color: red"><i class="fas fa-minus-circle"></i></span> Most ENB presets come with a performance impact that is especially noticeable on low end machines.
- <span style= "color: red"><i class="fas fa-minus-circle"></i></span> Editing ENB presets beyond toggling options is not easy and may take a solid amount of trial & error.
- <span style= "color: red"><i class="fas fa-minus-circle"></i></span> Some presets do not support vanilla image space, they will not work with the Night Eye and other effects.

**Installing ENBSeries is completely optional. You can skip this entire section and continue with the Finalisation if you like.**

## 1.2 Versions

ENBSeries for Skyrim SE is still updated with new features every once in a while. It has not yet achieved the same level of complexity that the Classic Skyrim version boasts, although it is coming closer. Presets for past versions usually work fine with new updates. Boris occasionally updates without incrementing the version number and it's generally difficult to track updates since the ENB binaries (the core files that are always required) are not available on the Nexus.

> For users of TPF, there are usually pings on the Discord server when ENBSeries was updated.

## 1.3 Core Files

The binaries are the core files that are always required to run ENBSeries. They consist of two plugins, `d3d11.dll` and `d3dcompiler_46e.dll`, that belong into your **root** folder.

The `enblocal.ini` stores your personal settings and it’s completely independent from your preset. Settings you can control through the INI file are hotkeys, forcing VSYNC and/or frame lock, preset shader cache, some fixes and additional graphical options such as antialiasing.

> These files may not be shared on the Nexus or elsewhere. They can only be acquired from the official website.

## 1.4 Preset Files

Presets are primarily shared on the Nexus and range from subtle improvements to feature-rich packages. The bulk of the preset-specific settings are stored in the `enbseries.ini` file. All general features can be tweaked or toggled on or off here. This INI is unique to its preset and also belongs into your **root** folder.

This folder should be located in your **root** folder and it includes all additional effect files (INI files and additional folders). The included effects vary from preset to preset, depending on what the author is utilising. In rare cases, the effect INIs are outside the **enbseries** folder and kept in the **root** folder as well (this is the case for the guide’s preset, Visceral ENB).

## 1.5 ENB Manager

Many users tend to switch back and forth between different ENB presets which is simplified by ENB managers. They are essentially mod managers for ENB presets that allow you to quickly set up global settings and deploy them alongside the ENB binaries and saved preset files. My personal favourite is ENB Man so that's what all instructions are written for. If you are experienced with handling ENBSeries, you are free to use any other manager of your choice or install files manually.

ENB Man has a single problem which is that files need to be extracted from their archive before they can be imported into the program, otherwise files occasionally get skipped resulting in visual bugs and the preset not functioning correctly. This is a minor issue and easily worked around.

## 1.6 ENB Helper

The [ENB Helper](https://www.nexusmods.com/skyrimspecialedition/mods/23174) is a SKSE plugin that enables unique settings per weather. It is required by many presets and was already installed as part of the Utilities section in the main guide. If you are not running any preset, the plugin will simply do nothing.

## 1.7 Complex Particle Lights

Newer versions of ENBSeries include an effect called Complex Particle Lights. Meshes edited to support it emit light that can even affect grass or the player character. The ENB Light mod primarily implements this feature, but there is also rudy's More Lights for ENB collection of mods which add lights to all kinds of objects such as soul gems and certain plants. As these effects require an active ENB preset with Complex Particle Lights enabled, they are not included in the main guide. You can install them in 05 Related Mods.

Please note that the Complex Particle Lights feature does come with a small performance impact. Users with lower-end machines might want to disable it and skip the related mods.