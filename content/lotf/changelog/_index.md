---
title: "Changelog"
weight: 6
type: docs
description: >
  Update notes for Legends of the Frost.
---

## Release 1.5.1

> TBD

#### Mod Changes

- Added SkyUI Ghost Bug Fix
- Updated NPC AI Process Position Fix to 4.06

#### Website

- **Installation:** Added Microsoft .NET 5.0 to the requirements section
- **Installation:** Updated instructions for the downgrade patcher (now only an EXE)

## Release 1.5

> 13/11/2021

This is mostly a maintenance update although I did add the fantastic **CoMAP** by Jelidity and Parapets as well as a brand-new installation guide. It is much shorter than the previous one on account of the Stock Game Folder system allowing us to skip several steps. It also accounts for the AE downgrade patcher.

Please for the love of Talos don't ask me when LOTF will get AE support.

#### Mod Changes

- Added Common Marker Addon Project (CoMAP)
- Updated SSEEdit to 4.0.4
- Updated SSE Display Tweaks to 0.4.17
- Updated NET Script Framework to 18
- Updated Skyrim Landscape and Water Fixes to 6.4.1
- Updated Assorted Mesh Fixes to 0.32.3
- Updated Static Mesh Improvement Mod Improvement Mod to 1.3.0
- Updated powerofthree's Tweaks to 1.3.3
- Updated Radiant - Candles to 2.2.0
- Updated Enhanced Vanilla Trees (no version change)
- Removed SMIM - Assorted Mesh Fixes Patch (redundant)
- Actually included the Blended Roads - Simplicity of Snow Patch

#### Website Changes

- **Installation:** Newly added with all instructions for LOTF, including the AE downgrade patcher
- **Screenshots:** Added new screenshots and headings for the side bar so the page is easier to navigate

## Release 1.4.2

> 24/10/2021

The butterfly update: In LOTF 1.4.2, I am adding some mods that improve critters in the world, how they move and where they can land. Did you know that Monarch butterfly wings were [upside down](https://staticdelivery.nexusmods.com/mods/110/images/54485-2-1401481905.jpg) in vanilla?

Also you no longer get my custom keybinds. I fixed that.

#### Mod Changes

- Added Umgak's Hanging Elves Ear Mesh Fix
- Added Wiseman303's Critter Fixes
- Added Butterflies Land True
- Added Butterflies Unchained
- Added Simplicity of Snow - Blended Roads Patch
- Updated Assorted Mesh Fixes to 0.32
- Updated Radiant - Candles to 2.1.0
- Updated DynDOLOD to 3 Alpha 53 (LOD was not regenerated)
- Fixed a dumb typo in the WABBAJACK_IGNORE_FILES.txt file name

## Release 1.4.1

> 16/10/2021

After yesterday's larger update, I have some fixes and previously missed mod updates for you today. Save safe, etc.

#### Mod Changes

Note that I only updated DynDOLOD and the DynDOLOD Resources, but did not regenerate LODs.

- Updated Skyrim Landscape and Water Fixes to 6.3
- Updated DynDOLOD Resources to Alpha 15
- Updated Shadows of Sunlight to 0.5
- Updated Simplicity of Snow to 0.4
- Updated ENBSeries (no version change)
- Updated DynDOLOD to 3 Alpha 48
- Added fixed moreHUD Settings Loader script (moreHUD MCM should no longer fail to initialise)
- Added my ControlMap_Custom.txt to the list of files ignored by Wabbajack so my keybinds are no longer applied to users' setups 

## Release 1.4

> 15/10/2021

This update brings a number of new addition that fit nicely within the scope of LOTF. I found that I could absolutely not live without **moreHUD** and added the mod along with a custom preset. You will now be able to see whether you already read a book, whether a book is a skill book and, if it is, which skill it improves. For enemies, their level and soul type is now displayed next to their health bar. When hovering over items that can be picked up, there will now be an indicator in the bottom right corner, informing you about your current carry capacity, how much weight the items would add, and whether you already have any items of the same type.

**Please note:** The moreHUD preset is applied automatically only in *new games*. In your ongoing playthroughs, please load it manually via the mod's MCM.

Visually, LOTF 1.4 adds the following improvements:

- Thanks to the new **Radiant - Candles** mod, candles now give off proper light and illuminate surrounding objects. You can find a comparison slider [here](https://imgsli.com/NzcwMjA). Note that this feature required me to enable Complex Particle Effects in ENB as well as increase the particle count INI setting which may cause a slight performance drop on low-end systems. However, I did not enable the Big Range setting so there will be no noticeable FPS loss on most PCs.
- The vanilla woven fences were notorious for their flickering which the Static Mesh Improvement Mod addresses but does not fully fix. I chose to add Mathy's meshes instead, **Skyrim 3D Misc - Woven Fence**, which are a lot more loose and should fix the flickering completely. There is a comparison slider [here](https://imgsli.com/NzcwMjE).
- Various assets related to spiders were fixed and improved by the mod **WEBS**. The titular spider webs are of higher quality and should no longer appear overbright. The mod also replaces the meshes for webbed dead bodies as some of them were outright broken in vanilla.
- **Simplicity of Snow** vastly improves the visuals and logic of projected snow on various objects. As a lightweight replacement for the more involved Better Dynamic Snow and No Snow Under Rooftops mods, it is well suited for LOTF's lightweight nature.

**The latest version of the .NET 5.0 Runtime is required.** This is because of the Scrambled Bugs update which now relies upon this. Please download it from [the official website](https://dotnet.microsoft.com/download/dotnet/5.0/runtime) and install it before updating LOTF.

#### Mod Changes

- Added WEBS
- Added High Gate Ruins Puzzle Reset Fix
- Added Static Mesh Improvement Mod Improvement Mod
- Added High Hrothgar - Fixed
- Added Skyrim 3D Misc - Woven Fence
- Added moreHUD
- Added Radiant - Candles
- Added Enhanced Vanilla Trees - Shrine to Peryite Nest Fix
- Added Simplicity of Snow
- Added Volcanic Tundra - Heat Wave Effects
- Added Misc Dialogue Edits
- Added Unofficial Material Fix - Improved Traps Patch
- Removed Wiseman303's Flora Fixes - Revamped - SMIM Patch (replaced by Static Mesh Improvement Mod Improvement Mod)
- Removed hank's gamepad and controller fixes
- Updated Spell Perk Item Distributor to 5.0.4
- Updated Scrambled Bugs to 14
- Updated DynDOLOD Resources to 3 Alpha 13
- Updated Assorted Mesh Fixes to 0.30.1
- Updated Relighting Skyrim to 1.2.1
- Updated College of Winterhold Quest Start Fixes to 0.2-1
- Updated DynDOLOD to 3 Alpha 47
- Updated ENBSeries (no version change)
- Temporarily set the hangingelvesear01.nif mesh (Skyrim Particle Patch) to hidden to fix a bug
- Enabled and tweaked ENB complex particle light effects
- Increased particle count (iMaxDesired) to 7500 in the SkyrimPrefs.ini
- Roboto Font Replacer is now disabled by default
- Fixed a few minor plugin conflicts
- Regenerated DynDOLOD

#### Website Changes

- **Introduction:** Added a warning about the new requirement of the .NET 5.0 Runtime.
- **Customisation:** Updated font replacer instructions, Roboto is now *disabled* by default
- **Documentation:** Updated accordingly for the recent mod changes.

## Release 1.3.1

> 19/09/2021

Just a quick update to fix the current issues with downloading ENB and some outputs.

#### Mod Changes

- Updated ENBSeries binaries to 0.463
- Updated Spell Perk Item Distributor to 5.0.3
- Updated Fixed Mesh Lighting to 1.4.2
- Updated NPC AI Process Position Fix to 4.05d
- Fixed TexGen and DynDOLOD output links

## Release 1.3

> 15/09/2021

This is a smaller update and will likely be the last one for the time being. I fixed the message when trying to drop a quest message so it does not just now show the raw string (was missing a dependency), removed the mod causing the purple waterfalls (couldn't be bothered to find the missing texture), updated a bunch of mods, and regenerated TexGen, DynDOLOD, and Occlusion with the latest version of DynDOLOD. I believe LOTF is in a pretty good place for now.

#### Mod Changes

- Added Scaleform Translation Plus Plus
- Added LeanWolf's Dawnbreaker ENB meshes
- Updated .NET Script Framework to 17
- Updated Disable USSEP Book to 1.1
- Updated Assorted Mesh Fixes to 0.26
- Updated College of Winterhold Quest Start Fixes to 0.2
- Updated DynDOLOD Resources to Alpha-12
- Updated Simple Horse Tweaks to 1.3
- Updated the Blacksmith Forge Water Patch Script and regenerated the patch
- Updated DynDOLOD to Alpha 41 and regenerated all LODs
- Removed horse walk movement tweak from the CRP
- Removed DynDOLOD Bright LOD Waterfall Fix
- Disabled the floating pot in High Hrothgar
- xLODGen is no longer packaged with the installer

## Release 1.2

> 10/09/2021

After some deliberation, I swapped out the previous skin overhauls (Lucid and Vitruvia) for the Tempered Skins combination. They are closer to vanilla and look better with LOTF's lighting.

I also fixed the purple waterfalls and improved the [book interface](https://imgsli.com/NzAzOTc).

#### Mod Changes

- Added ENB Helper
- Added Realistic Paper
- Added Blacksmith Forge Water Patch xEdit Script
- Added Convenient Reading
- Added Tempered Skins for Males
- Added Tempered Skins for Females
- Updated Minimal ENB for Obsidian Weathers to 1.2
- Updated Scrambled Bugs to 13
- Updated Enhanced Vanilla Trees to 2.2.1
- Removed Vitruvia - Skin Texture Overhaul for Males
- Removed Lucid Skin
- Tweaked the updated ENB preset
- Classic Sprinting Redone is now optional and disabled by default
- Generated the Blacksmith Forge Water Patch
- Regenerated TexGen and DynDOLOD

#### Website Changes

- **Customisation:** Added "Change sprinting from toggle to hold" option
- **Documentation:** Updated accordingly for the recent mod changes.
- **Screenshots:** Added a few more new screenshots.

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