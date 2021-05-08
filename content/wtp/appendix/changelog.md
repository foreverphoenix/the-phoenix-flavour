---
title: "Changelog"
weight: 4
type: docs
description: >
  Update notes for all non-Beta versions.
---

## Release 1.6

> TBD

#### Mod Changes

- Added zEdit (I needed it for one merge)
- Added F4 Creation Kit Fixes
- Added Jamaica Plain Navmesh Fix
- Added The Natural Bundle - Masonry Set
- Added The Natural Bundle - Submarine Set
- Added Deathclaws HD Retexture
- Added The Flamer Project
- Added Leafblower Junk Jet
- Added Auto Lockpick
- Added Auto Hack
- Added Better Explosives Redux
- Added Fortune Finder 4 Fix
- Added Workshop Power Pack
- Added River Fix
- Updated Buffout to 1.23.0
- Updated Workshop Framework to 2.0.12a
- Updated Wetness Shader Fix to 3.41
- Updated Companion Stealth Distance Fix to 7.0
- Updated FallUI Confirm Boxes to 2.0.3
- Updated FallUI Workbench to 1.2.4
- Updated Fallout 4 Ultimate Window Overhaul to 3.1
- Updated Visible Idle Markers to 1.6
- Removed Scrolling Doesn't Change PoV
- Removed Detailed Deathclaws
- Removed Fallout 3 NV Feral Ghouls Replacer
- Removed Simple Crafting Station - K-9 Harness Patch
- Reinstalled Fixed Flickering Puddles (was missing one file, may fix lingering issues)
- Rebuilt the Weapons BA2s
- Rebuilt the Creatures BA2s
- Re-added one DEF_INV file (fixes materials showing sorting tags in Workshop menu)
- Regenerated precombines for the area around the new Sanctuary bridge (thanks for talking me through that, Lively!)
- Removed Fortune Finder tweaks from Loot Logic Scrounger Fortune Finder Rebalance
- Added new 'Backpack' tag to DEV_INV_TAGS.xml
- Merged the three music plugins together and removed the separate plugins
- Replaced the now redundant music patch with the merged plugin
- Extracted the Fallout Suite BA2 since there is no longer a plugin to load it
- Fixed some conflicts between Better Explosives Redux and other mods
- Regenerated INI files from scratch

**K-9 Harness**

Until now fadingsignal's K-9 Harness for Dogmeat could be crafted at the crafting station which was the original implementation. I have never been happy with this and in this update I finally did something about it. You can now find exactly *one* K-9 Harness in the world. The location happens to be a police station for obvious reasons - if you want to know where exactly you can find it, double-click the new K-9 Integration Patch in Mod Organizer 2 and check the **Notes** tab.

**Creation Club**

WTP 1.6 adds *optional* support for some "creations". You can find details and instructions [here](/wtp/wtp-resources/creation-club)

#### Website Changes

- **Fallout 4:** Added a link for LostDragonist's Steam Library Setup Tool.
- Removed the Custom Files page. All relevant documentation was moved into Mod Organizer 2 (check the Notes for each mod).

## Release 1.5.2

> 06/04/2021

This update is safe-save. Copy over the GFF into your root folder and overwrite (ENB binaries updated).

#### Mod Changes

- Updated Mod Organizer 2 to 2.4.1
- Re-arranged and re-coloured MO2 separators
- WTP changelogs are no longer available through MO2
- Updated ENBSeries (no version change)
- Updated Buffout 4 to 1.22.0
- Updated PrivateProfileRedirector to 0.5.2
- Updated High FPS Physics Fix to 0.8.3
- Updated What's Your Name to 1.12.0
- Added Less Annoying Water Foam Circles
- Added No Quest Autostart - BoS Fire Support
- Added No Quest Autostart - Automatron
- Added No Quest Autostart - Vault-Tec
- Added No Quest Autostart - Far Harbor
- Added No Quest Autostart - Nuka World
- Removed some unnecessary stuff from the Phoenix Tweaks plugin

#### Website Changes

- **Finalisation:** Shortened the Resolution section and moved Ultrawide tweaks to this page.
- **Ultrawide:** Removed this page.

*Turns out that Wabbajack auto-sets the resolution in the INI files.*

## Release 1.5.1

> 08/03/2021

I fixed some errors in `Power Armor Lore-Friendly Distribution.esp` by reverting the levelled lists for Atom Cats power armor to vanilla. That means they'll be wearing T-60 armor again (instead of T-51). I know I had Atom Cats T-51 armor *somewhere* but it seems to have gotten lost, resulting in these errors. I fully admit that this is a lazy solution but it works and that was always enough for Todd anyway.

While recompiling for WJ, I also updated the links to the website (see below).

## Global Site Update

> 08/03/2021

I finally did some spring cleaning. For the longest time it annoyed me that in my original folder structure I had categorised pages by games, for example the TPF part of the website was called "Skyrim SE" in the top menu. But what if I want to start another SE project? And you don't want to know the chaos in my pictures folder either.

The reason I hesitated for so long to change the folder names is because it breaks every, single, link. And while fixing the internal links and file paths was merely a minor annoyance, fixing all external links is more difficult - especially considering that other people may link to TPF as well and those links are now broken. Of course I also need to recompile both TPF and WTP for Wabbajack to update the links that open automatically upon installing a Wabbajack list.

Well, I finally updated now and I'm very happy with the changes. It likely will take some time for all external links to get fix plus I suspect I may have missing some internal links and file paths.

#### Changes

- Removed the Bioware section (see below).
- Renamed "Skyrim SE" to "The Phoenix Flavour" (link changed from skyrim-se to tpf).
- Renamed "Fallout 4" to "Welcome to Paradise" (link changed from fallout to wtp).
- Updated all internal links and file paths - hopefully.
- Cleaned up my pictures folder to remove any pictures that are no longer in the guide.
- Updated the home page, it has two buttons now and a combination of the TPF and WTP pics.

#### Bioware

The current state of things is that I have published a guide for ME1 with a draft for an ME2 version waiting for revision. But here's the thing: Modding Bioware games is quite different from modding Bethesda games. I've only really dipped my toes in it and wouldn't call myself an expert by any stretch of the imagination. Something I often criticise about various smaller Skyrim modding "guides" is that their authors barely know what they're doing. It occured to me that my Mass Effect "guides" are in essence the same thing ~~with better formatting~~.

To keep a longer story short, I have developed a strong sense of imposter syndrome over those excursions into Bioware land that is causing me a fair amount of stress. Something I've learned over the past couple years is that if you have too many things putting pressure on you at once, cut out everything that's non-essential. Well, this time the scissors are for the Bioware section of the TPF website.

## Release 1.5

> 06/03/2021

#### Mod Changes

- Updated Mod Organizer 2 to 2.4.0
- Tweaked Pipboy INI settings (increased resolution, disabled fx)
- Added Mator's xEdit Patching Framework
- FO4Edit cache is now saved into the Tools\FO4Edit folder
- Updated xSE Plugin Preloader to 0.2.4
- Changed xSE Plugin Preloader load method to OnThreadAttach
- Updated Buffout to 1.20.3
- Updated the Unofficial Fallout 4 Patch to 2.1.2b
- Updated High FPS Physics Fix to 0.8.0
- Removed additional High FPS Physics Fix INIs
- Default settings for WTP are now 60FPS and no VSYNC
- Documentation includes instructions to change the settings
- Reinstalled DEF_UI and only chose DEF_HUD
- Reverted to vanilla DEF_UI profile
- Added FallUI
- Added FallUI Workbench
- Added FallUI Map
- Re-added LooksMenu
- Added Better Confirm Boxes for PC
- Added TRUBY9 ULTRAWIDE DEF_UI Fix
- Added Better Confirm Boxes for PC - Widescreen Patch
- Added Neutral Look Up Tables LUT
- Added Fallout 4 Enhanced Color Correction
- Added Retro Radio Replacer
- Added Classic Wasteland Survival Guide - Magazine Retexture
- Added U.S. Covert Operations Manual - Magazine Retexture
- Added Total Hack - Magazine Retexture
- Added The Hunting Rifle Set
- Added The Ballistic Series
- Added Fixed Creature Death Drops
- Added FO4 Photo Mode
- Updated Workshop Framework to 2.0.10
- Updated Simple Sorting Overhaul to 2.0
- Updated Wetness Shader Fix to 3.3
- Updated Sprint Stuttering Fix to 1.2
- Updated Hazmat Suit Redux to 0.1
- Updated Skeletal Adjustments for CBBE to 2.0
- Updated What's Your Name to 1.11.1
- Updated Fixed and Cleaned Homeplate to 2.1
- Updated LOST Audio Tweaks to 1.6.2
- Updated LOST Audio Tweaks - True Storms and RAO Patch to Beta
- Removed Pip-Boy Dual Color section
- Removed Small Map Markers
- Removed The Humble Hunting Rifle
- Removed ScratchMade - New Combat Shotgun and Rifle Textures 
- Removed The Top-Notch Tommy Gun
- Removed Assault Rifle Retexture 2K
- Removed HUD Customisation stuff
- Repacked the Clutter BA2s
- Repacked the Weapon BA2s
- Changed ENB hotkeys to mirror TPF's

#### Simple Sorting Overhaul

As we have now switched to FallUI from DEF_INV, I updated my INNRs (naming rules) to have the same format as Ruddy's sorting patcher that FallUI was intended for. That means mods for armors and weapons will be displayed in smaller font below the item name.

I did take a look at the [Complex Sorter](https://www.nexusmods.com/fallout4/mods/48826) for FallUI which would be very convenient for me but ultimately I prefer my own icons and INNRs. Plus they already cover my power armor changes and include my preferred power armor naming scheme.

#### Website Changes

I went over all pages and fixed what I thought needed fixing. Screenshots were updated, sentences were rephrased, and instructions were clarified.

- **Finalisation:** Added instructions for the optional LUTs.
- **Finalisation:** Added Controller Fix instructions (required because of an issue with FallUI).
- **Finalisation:** Expanded FPS and VSYNCs instructions (they are DIY now).
- **New Game:** Removed Hotkey instructions. No longer necessary with TPF ENB hotkeys.
- **Mod Configuration:** Added instructions for Photo Mode.
- Renamed the "Documentation" section to "Resources".
- **Ultrawide:** Moved this page to the Resources section.
- **Customisation:** Removed this section. Use the FallUI MCM to customise your UI.
- **Troubleshooting:** Added a note about flickering puddles.

## Release 1.4.1

> 26/11/2020

#### Mod Changes

- Re-enabled Authentic Handmade Weaponry (accidentally disabled the plugin in 1.4)

## Release 1.4

> 23/11/2020

#### Mod Changes

- Added Weapon Debris Crash Fix
- Added Sprint Stuttering Fix
- Added Less Ugly Intercom
- Added The Laser Series
- Added The Plasma Project
- Removed The Lavish Laser Musket
- Removed The Lavish Laser Collection
- Rebuilt the Weapons BA2
- Updated Buffout to 1.17.1
- Updated Wetness Shader Fix to 3.2
- Updated Handmade Turrets to 1.3.2
- Updated Workshop Framework to 2.0.6
- Updated Indubitably Ivy to 0.2
- Updated What's Your Name to 1.10.0
- Updated Skeletal Adjustments for CBBE - Knee Fix to 1.1
- Updated LOST Audio Tweaks to 1.5.1
- Updated custom Sound Slider Tweaks plugin
- Slightly tweaked High FPS Physics Fix presets
- Unhid message box and tutorial messages in my DEF_UI preset

## Release 1.3.1

> 24/10/2020

Just a minor fix and clean-up for yesterday's update.

#### Mod Changes

- Updated Bullet Counted Reload System to 1.05b
- Updated Workshop Framework to 2.0.3
- Added missing ALWAYS INCLUDE flags to High FPS Physics Fix profiles

## Release 1.3

> 23/10/2020

This update fixes a number of issues reported by users (thanks, guys!). I am also officially changing the list name to **Welcome to Paradise**. The website, Discord channels, and Mod Organizer 2 profile have all been edited accordingly.

#### Mod Changes

- Hopefully fixed radio songs not playing for good
- Updated xSE Plugin Preloader to 0.2.3 (XML unchanged, let me know if there are issues)
- Updated Buffout 4 to 1.16.1
- Fixed some untranslated UI bits (missing strings)
- Removed Auto Gamepad Switch (caused some issues)
- Fixed scrap tag for Stogie
- Added High FPS Physics Fix plus pre-configured INIs
- Removed the separate DEF_UI preset, now editing the one packaged with the main mod
- Re-enabled compass markers for locations / Dogmeat / PA in DEF_UI
- Turns out Archive2 is unreliable so I repacked a bunch of BA2s with CAO
- Unpacked custom BA2 for Bleak Beauty, Musical Lore, More Where That Came From, and Elvani's Track Pack
- Fixed some purple cars by reverting them to vanilla, it's a band-aid fix but the best I could do

#### Website Changes

- **Finalisation:** Removed instructions for NVIDIA Inspector.
- **Finalisation:** Added instructions for the newly-added High FPS Physics Fix and my pre-configured INIs.

## Release 1.2.1

> 01/10/2020

#### Mod Changes

- Actually fixed radio tracks not playing
- Updated xSE Plugin Preloader to 0.2

Please delete **xSE PluginPreloader.ini** from your **root** folder. Move the new **xSE PluginPreloader.xml** and updated **IpHlpAPI.dll** into your **root** folder and overwrite when prompted.

## Release 1.2

> 30/09/2020

#### Mod Changes

- Updated Buffout to 1.12.1
- Placed the new Buffout TBB Redist plugin in the Game Folder Files folder
- Removed Achievements (this is now a feature in Buffout)
- Actually fixed the problematic True Nights record instead of bruteforce deleting it
- Updated Classic Hostered Weapons System to 1.04c
- Added Start Me Up - Basic Version
- Added Lively's Start Me Up Tweak
- Resolved a conflict between Start Me Up and the UFO4P
- Inlined Lively's PPPL INI file
- Updated Sweet Roll 5000 and rebuilt Clutter BA2s
- Fixed Diamond City Radio tracks not playing (thanks Archie!)

#### Website Changes

- [Finalisation](/wtp/installation/finalisation/): Added this new page and moved the game resolution instructions here.
- [Finalisation](/wtp/installation/finalisation/): Added instructions on how to force VSYNC and cap the framerate.
- [New Game](/wtp/installation/new-game/): Removed LooksMenu related instructions as that mod was removed.
- [New Game](/wtp/installation/new-game/): Added *seriously* detailed instructions for Start Me Up.

## Release 1.1

> 27/09/2020

#### Mod Changes

- Now using Lively's pppl.ini file
- Updated Buffout to 1.11.0
- Removed one record from True Nights which can cause memory corruption according to Buffout
- Removed LooksMenu (don't really need it anyway)
- Enabled the Classic Holstered Weapons Systems patch in Buffout
- Adjusted loot / interact prompt and window position in my DEF_UI preset
- Switched to the Alternative Version of Fixed Flickering Puddles (hopefully fixing black pre-war Codsworth)
- Removed Skip raiding your own settlements (no time to troubleshoot the compilation error it causes)

#### Website Changes

- [Wabbajack](/wtp/installation/wabbajack/): Added new section on how change the game resolution.
- [Troubleshooting](/wtp/appendix/troubleshooting/): Added this page with a few known issues.

## Release 1.0.1

> 26/09/2020

- Rolled back to **Buffout 4** 1.7.0 as the latest version is causing crashes.

## Release 1.0

> 26/09/2020

Initial release. For more info, check the [Patreon post](https://www.patreon.com/posts/phoenix-flavour-42049352).

*Please rebuilt the site, kthxbye.*