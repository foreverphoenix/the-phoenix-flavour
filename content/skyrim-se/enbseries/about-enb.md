---
title: "About ENB"
weight: 1
type: docs
description: >
  Introduction to ENBSeries with a list of advantages and disadvantages.
---

## What is ENBSeries?

ENBSeries is a post-processing injector by Boris Vorontsov. Unlike ReShade, it is not universal but built for specific games and hooks directly into the engine. Effects are therefore highly advanced and specific to each games. ENB is also capable of fixing bugs and improving performance plus it offers additional features such as VSYNC, a screenshot hotkey, and a toggleable FPS counter.

The effects vary in their performance impact. A full preset, especially when Skyrim is run on high resolutions, can bring even high-end PCs to their knees. Fortunately, Skyrim SE with its generally improved performance runs a great deal better with ENBSeries presets and 60FPS+ on a reasonable resolution (1080p) are comfortably attainable on most machines.

|            | Advantages and Disadvantages of ENBSeries                    |
| ---------- | ------------------------------------------------------------ |
| <span style= "color: green"><i class="fas fa-plus-circle"></i></span> | The visual improvements are immense. They can profoundly change the atmosphere of Skyrim. |
| <span style= "color: green"><i class="fas fa-plus-circle"></i></span> | Everything can be customised. The performance impact can be dampened by turning off hard-hitters such as Ambient Occlusion. |
| <span style= "color: green"><i class="fas fa-plus-circle"></i></span> | You can tweak or swap presets, or completely uninstall ENBSeries at any time. Saves are not affected. |
| <span style= "color: red"><i class="fas fa-minus-circle"></i></span> | ENBSeries presets can noticably impact performance, especially on low end machines. |
| <span style= "color: red"><i class="fas fa-minus-circle"></i></span> | Editing ENB presets beyond toggling options is not always easy and may take a solid amount of trial & error. |
| <span style= "color: red"><i class="fas fa-minus-circle"></i></span> | Some presets do not support vanilla image space, they will not work with the Night Eye and other effects. |

**Installing ENBSeries is completely optional. You can skip this entire section and continue with the Finalisation if you like.** However, it should be noted that I do NOT recommend skipping it as there are many mods included specifically for ENB in TPF, primarily meshes with adjusted brightness or support for the complex particle lights feature. Not installing an ENB means you WILL be missing out.

## ENB Basics

### Versions

ENBSeries for Skyrim SE is still updated with new features every once in a while. It has not yet achieved the same level of complexity that the Classic Skyrim version boasts, although it is coming very close. Presets for past versions usually work fine with new updates. Boris (creator of ENBSeries) occasionally updates without incrementing the version number and it's generally difficult to track updates since the ENB binaries (the core files that are always required) are not available on the Nexus.

> For users of TPF there are usually notifications on the Discord server when ENBSeries was updated.

### Core Files

The binaries are the core files that are always required to run ENBSeries. They consist of two plugins, `d3d11.dll` and `d3dcompiler_46e.dll`, that belong into your **root** folder.

The `enblocal.ini` stores your personal settings and it’s completely independent from your preset. Settings you can control through the INI file are hotkeys, forcing VSYNC and/or frame lock, preset shader cache, some fixes and additional graphical options such as antialiasing.

Having these files installed can have a small performance impact, even without a preset.

> The ENBSeries binaries may not be shared on the Nexus. They can only be acquired from the official website.

### Preset Files

Presets are primarily shared on the Nexus and range from subtle improvements to feature-rich packages. The bulk of the preset-specific settings are stored in the `enbseries.ini` file. All general features can be tweaked or toggled on or off here. This INI is unique to its preset and also belongs into your **root** folder.

This folder should be located in your **root** folder and it includes all additional effect files (INI files and additional folders). The included effects vary from preset to preset, depending on what the author is utilising. In rare cases, the effect INIs are outside the **enbseries** folder and kept in the **root** folder as well.

### ENB Manager

Many users tend to switch back and forth between different ENB presets which is simplified by ENB managers. They are essentially mod managers for ENB presets that allow you to quickly set up global settings and deploy them alongside the ENB binaries and saved preset files. My personal favourite is ENB Man so that's what all instructions are written for. If you are experienced with handling ENBSeries, you are free to use any other manager of your choice or install files manually.

ENB Man has a single problem which is that files need to be extracted from their archive before they can be imported into the program, otherwise files occasionally get skipped resulting in visual bugs and the preset not functioning correctly. This is a minor issue and easily worked around.

### ENB Helper

The [ENB Helper](https://www.nexusmods.com/skyrimspecialedition/mods/23174) is a SKSE plugin that enables unique settings per weather. It is required by many presets and was already installed as part of the Utilities section in the main guide. If you are not running any preset, the plugin will simply do nothing.