---
title: "Changelog"
weight: 5
type: docs
description: >
  Changelog for LOTF.
---

## Release 1.1

> 06/09/2021

**Fixing the intro dialogue:**

So apparently increasing horse speed will mess up the intro carriage ride because the horses are too fast for the dialogue - who would have thought? I reverted *only* the forward walk speed tweak from Simple Horse Tweaks to vanilla which should fix it.

**New ENB preset:**

I also added an **ENB** preset in this update. If The Truth was still on the Nexus, it would have been part of the initial release, but with things as they are I had elected not to use an ENB at all. However, after some playing I realised that vanilla ambient occlusion crushes blacks on the character and some shadows to the point where it's just ugly as hell.

Thankfully, @Shade088 from our Discord server recommended [Minimal ENB for Obsidian Weathers](https://www.nexusmods.com/skyrimspecialedition/mods/37098) which turns out to be the perfect alternative. It does not affect colours (so you can also use it with any weather mod), but implements all those little improvements that ENB can bring to the table such as ambient occlusion. @Shade088 also provided tweaked water values to hide the distant water seams so I didn't even have to figure these out myself.

Since LOTF is using the Stock Game folder system, ENB is already installed for you and you do not have to move any files.

**This update is save-safe.**

#### Mod Changes

- Added deorder's MO2 plugins (largely for myself)
- Added Minimal ENB for Obsidian Weathers
- Added ENBSeries binaries
- Added Skyrim Particle Patch for ENB
- Added Skyrim Particle Patch for ENB - Assorted Mesh Fixes - Solitude Mesh Fixes Patch
- Added DynDOLOD Bright LOD Waterfall Fix
- Added Time Format Changer (disabled by default)
- Added Menu and Load Smoke Removed for ENB
- Added No Lockpicking (disabled by default)
- Removed Loading Screen Smoke Removed
- Disabled ambient occlusion in the INI files
- Replaced the MO2 splash screen with one specifically made for LOTF
- Actually hid the terrain LOD files overwriting AQWM

#### Website Changes

- **Introduction:** Removed LOTF in numbers section. No point maintaining this.
- **Introduction:** Added ENB Hotkeys section.
- **Introduction:** Fixed MCM instructions referencing removed mods.
- **Introduction:** Moved the customisation section to the new dedicated page.
- **Customisation:** Added new "Enable 24h time format" option.
- **Customisation:** Added new "Skip Lockpicking" option.
- **Documentation:** Added notes on the new ENB preset and my tweaks for it

## Release 1.0

> 04/09/2021

**First public release of LOTF.**

#### Mod Changes

- Now using the Stock Game folder system
- Now packaging all tools with the WJ installer
- Added NPC AI Process Position Fix
- Added Modern Clap Bug Fix
- Added Quality Cubemaps - HD Cube Maps
- Added Cathedral Night Sky
- Added Waymark - A Road Signs Mod
- Added HD Vanilla Tree Bark - ESRGAN AI Upscale
- Added Cathedral - Plants
- Added Cathedral - Mushrooms
- Added LOOT Preventifier
- Added Project Clarity - Architecture Textures Redone
- Added Project Clarity - Dungeon Textures Redone
- Added Project Clarity - Landscape Textures Redone
- Added Project Clarity - Clutter Textures Redone
- Added Project Clarity - Weapon Textures Redone
- Added Project Clarity - Armor Textures Redone
- Added Project Clarity - Clothing and Jewelry Textures Redone
- Added Project Clarity - Creature Textures Redone
- Added Project Clarity - Effect Textures Redone
- Added Simple Horse Tweaks
- Added Unequip Quiver
- Added Auto Input Switch
- Added Terrain Tamriel Extend
- Updated .NET Script Framework to 16
- Updated MCM Helper to 1.3.0
- Updated Assorted Mesh Fixes to 0.25
- Updated Fixed Mesh Lighting to 1.4.1
- Updated Landscape Fixes For Grass Mods to 4.9
- Updated Enhanced Vanilla Trees to 2.2.0
- Removed Base Coat
- Removed Animated Forge Water
- Removed Point the Way
- Removed Arena - An Encounter Zone Overhaul
- Removed Apothecary - An Alchemy Overhaul
- Removed Radiant Requirements MCM
- Removed Radiant Requirements MCM - TPF Preset
- Removed Apothecary as a master from the CRP
- Fixed a conflict between Simple Horse Tweaks and Audio Overhaul for Skyrim
- Regenerated INI files with BethINI
- Regenerated terrain LOD, TexGen, DynDOLOD, Occlusion
- New colour theme for the MO2 separators
- New MO2 splash screen replacer

#### Website Changes

- Updated the Introduction (noted that LOTF uses the Stock Game folder system)
- Updated the Documentation (removal of Apothecary and Arena, etc).
- Added one new screenshot to the showcase page.

## Wabbajack Test

> 22/08/2021

- Initial release for Wabbajack testing.


*hi i'm a test you can ignore me*