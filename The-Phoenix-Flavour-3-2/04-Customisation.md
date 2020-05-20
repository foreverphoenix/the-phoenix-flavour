![logo](../Media/tpf_logo.png)

**TABLE OF CONTENTS**
- [Preparations](#preparations)
  - [Notes and Warning](#notes-and-warning)
  - [New Profile](#new-profile)
  - [Customisation](#customisation)
- [Main Menu Mods](#main-menu-mods)
  - [General Notes](#general-notes)
  - [Some Recommendations](#some-recommendations)
- [Font Replacer](#font-replacer)
  - [Notes](#notes)
  - [Mod Order](#mod-order)
  - [Recommendations](#recommendations)
- [SkyUI Icon Replacer](#skyui-icon-replacer)
  - [Notes](#notes-1)
  - [Mod Order](#mod-order-1)
  - [Inventory Category Icon Replacer](#inventory-category-icon-replacer)
  - [Active Effects Icon Replacer](#active-effects-icon-replacer)
- [Widescreen Support](#widescreen-support)
  - [Notes](#notes-2)
  - [Complete Widescreen Fix](#complete-widescreen-fix)
  - [Remove QuickSave Button (optional)](#remove-quicksave-button-optional)
- [Misc Mods](#misc-mods)
  - [SkyUI Config Tweak - Equipped Items On Top (optional)](#skyui-config-tweak---equipped-items-on-top-optional)
  - [Winterhold Statue - Animated with Light (optional)](#winterhold-statue---animated-with-light-optional)
  - [DirtCliff Remaster (optional)](#dirtcliff-remaster-optional)
  - [Trifle From Hiro – The Gate Solitude (optional)](#trifle-from-hiro--the-gate-solitude-optional)
- [rougeshot's Skeleton Replacer](#rougeshots-skeleton-replacer)
  - [About the mods](#about-the-mods)
  - [Mod Order](#mod-order-2)
  - [Already included](#already-included)
  - [Can be added](#can-be-added)
  - [Do not add](#do-not-add)
- [Tree Tweaks](#tree-tweaks)
  - [Notes](#notes-3)
  - [Enhanced Vanilla Trees Tweaks](#enhanced-vanilla-trees-tweaks)
  - [Green Aspen Trees](#green-aspen-trees)
  - [Solstheim 3D Trees](#solstheim-3d-trees)
  - [Whiterun Forest Borealis](#whiterun-forest-borealis)
- [Arthmoor's New Towns](#arthmoors-new-towns)
  - [The Dilemma](#the-dilemma)
  - [Helarchen Creek (optional)](#helarchen-creek-optional)
  - [Keld-Nar (optional)](#keld-nar-optional)
  - [Simple Children - Keld-Nar Patch (optional)](#simple-children---keld-nar-patch-optional)
  - [Telengard (optional)](#telengard-optional)
  - [The Fall of Granite Hill (optional)](#the-fall-of-granite-hill-optional)
  - [Oakwood (optional)](#oakwood-optional)
  - [Landscape Fixes for Grass Mods - Oakwood (optional)](#landscape-fixes-for-grass-mods---oakwood-optional)
  - [Arthmoor's Towns - Patch Pack](#arthmoors-towns---patch-pack)
- [Plugin Edits](#plugin-edits)
  - [Dwemer Spectres - Remove Beards](#dwemer-spectres---remove-beards)
- [Removing ENB](#removing-enb)
  - [Considerations](#considerations)
  - [Getting rid of ENBSeries](#getting-rid-of-enbseries)
  - [Related Mods](#related-mods)
  - [INI Tweaks](#ini-tweaks)
  - [Potential Replacements](#potential-replacements)
- [DynDOLOD](#dyndolod)
  - [Preparations](#preparations-1)
  - [Running DynDOLOD](#running-dyndolod)
  - [DynDOLOD Output](#dyndolod-output)

![separator](../Media/separator.png)

# Preparations

## Notes and Warning

Considering the size of the main guide, there is a limit to how many additional options we can support. The Customisation section was written mostly to cover simple additions and tweaks so the amount of issues one can run into here should be minimal. First we will create a new profile to work with during this section so that the main guide installation is preserved in its original form. If you do run into issues, you can revert back to it anytime.

Of course the Customisation sections is completely optional. You are free to skip it entirely, and move on to the **New Game** section now.

## New Profile

- In Mod Organizer 2, open the **Profiles** window (Tools > Profiles or CTRL + P).
- The guide profile should be selected by default (**The Phoenix Flavour**).
- Click **Copy** and enter **The Phoenix Flavour - Customised** as the name.
- Close the **Profiles** window.
- Switch to the new profile in MO2 and only edit this one during the Customisation section.

> This way your original profile remains untouched and you can go back to your default TPF setup anytime.

## Customisation

You are now free to go through the Customisation steps. Pick and choose 

![separator](../Media/separator.png)

# Main Menu Mods

## General Notes

### About

Everytime you start the game, you will spend approximately three seconds in the main menu (which is how long it takes to press NEW GAME or CONTINUE). That's why you should definitely mod it in some way.

With ReCleaned menu (an optional mod which is part of the main guide), the main menu has already been decluttered and freed of any Creation Club ads. The background smoke has been removed as well (through another optional mod) which will look much better with custom main menu replacers.

The two types of mods for main menus are music replacers and background replacers. Sometimes both are packaged together. The file names and paths are:

- `Data\music\mus_maintheme.xwm`
- `Data\textures\interface\objects\mainmenuwallpaper.dds `

Any other files packaged with a main menu replacer you can safely delete. If you want only the music track or the background image, delete the other file.

### Monitor Proportions

Most menu replacers are made for 16:9 resolutions (1920x1080, 2560x1440, 3840x2160) unless stated otherwise. Keep that in mind when selecting a background replacer. Ultra widescreen monitors are not usually supported by background replacer mods. While 16:10 are extremely rare nowadays, MistValkyrie offers versions for those propertions in Mist's Anthology Menus. 

### Do-It-Yourself

It is fairly easy to convert any song to XWM and use it as a background track. Creating a custom background wallpaper is a little more involved but not complex at all. I will elaborate on this in the future.

### Main Menu Randomizer

If you just cannot settle for one main menu replacer, why not randomize them so you get a different one every time you launch the game? With [Main Menu Randomizer](https://www.nexusmods.com/skyrimspecialedition/mods/33574) you can do just that. Note that I haven't written instructions for it yet so you'll have to figure out how to use it on your own. Standard main menu replacers will have to have their file paths and names updated to work properly with the Randomizer.

### Mod Order

Completely irrelevant but as usual I would recommend grouping main menu replacers with the **INTERFACE** separator.

## Some Recommendations

- [DRELDYN's Original Main Menu Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/6992?tab=files)
  - My personal favourite and the one I usually use. I do delete the sound file though, and keep the vanilla theme.
- [Mist's Anthology Menus](https://www.nexusmods.com/skyrimspecialedition/mods/744?tab=files) 
  - Beautiful collection by MistValkyrie. Includes both music tracks and wallpapers.
- [Main Menu and Music Replacer](https://www.nexusmods.com/skyrimspecialedition/mods/30144?tab=files)
- [Relaxing Main Menu Replacer](https://www.nexusmods.com/skyrimspecialedition/mods/11675?tab=files)
- *Or search the Nexus for more.*

![separator](../Media/separator.png)

# Font Replacer

## Notes

Changing the primary font in Skyrim is not quite as simple as replacing `fonts_en2.swf `, you also need to edit the `fontconfig.txt `. Through this config file you can define separate fonts for the console, books, notes and the general UI. Thankfully, font replacement mods always come with this file tweaked accordingly.

The most popular and comprehensive font overhaul mod is **Sovngarde** which was created specifically for Skyrim SE. Before Sovngarde was released, I used and loved the **Fertigo Pro** font replacer and currently I am enjoying the simplicity of the **Roboto** font.

I have compiled a list of font replacers that I like although you can find more on the Nexus. **You can only use one of them at a time.**

[Monospace fonts](https://en.wikipedia.org/wiki/Monospaced_font) are preferable since otherwise perk and inventory descriptions might be cut off. 

## Mod Order

Irrelevant. I recommend grouping font replacers with the **INTERFACE** separator.

## Recommendations

- [Sovngarde - Mist's Font Replacer](https://www.nexusmods.com/skyrimspecialedition/mods/386?tab=files) - I highly recommend the "Light" version
- [Main Font Replacement](https://www.nexusmods.com/skyrimspecialedition/mods/14356?tab=files) - I recommend only the "Fertigo Pro" option
- [Roboto Font Replacer](https://www.nexusmods.com/skyrimspecialedition/mods/1779?tab=files) - very clean, my current favourite
- *Or search for more on the Nexus.*

![separator](../Media/separator.png)

# SkyUI Icon Replacer

## Notes

To further customise your interface, or, more specifically, SkyUI, ElSopa created a whole collection of icon replacers. There are some for the inventory categories as well as the active effects displayed in the HUD. While they are standalone, you might want to match your choice of icon replacers for inventory categories and active effects.

Since they overwrite each other, you can only have one of each active at a time (one replacer for the inventory category items, and one for the active effects).

## Mod Order

Irrelevant. I recommend grouping font replacers with the **INTERFACE** separator.

## Inventory Category Icon Replacer

- [SkyUI Colored Category Icons](https://www.nexusmods.com/skyrimspecialedition/mods/23193)
- [ElSopa - Animated Celtic Icons for SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/22938)
- [Colored and Animated Celtic Icons for SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/23054)
- [Oblivionesque Category Icons for SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/29773)

## Active Effects Icon Replacer

- [ElSopa - Colored SkyUI Active Effect Icons](https://www.nexusmods.com/skyrimspecialedition/mods/23897)
- [ElSopa - Animated Colored SkyUI Widgets](https://www.nexusmods.com/skyrimspecialedition/mods/24420)
- [SkyUI Widgets Animated Black and White](https://www.nexusmods.com/skyrimspecialedition/mods/24736)
- [Oblivionesque Active Effects for SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/29682)

![separator](../Media/separator.png)

# Widescreen Support

## Notes

For owners of widescreen monitors (resolutions of 2560x1080 or 3440x1440), there are compatible versions of all modded interface files that you will need to install in addition to or instead of the original ones. Place the widescreen versions or patches below the original mods in the mod order (they should not be overwritten).

Because I do not own a widescreen monitor, I can't download and test these files. You will have to figure it out yourself.

## [Complete Widescreen Fix](https://www.nexusmods.com/skyrimspecialedition/mods/1778?tab=files)

This should cover the majority of affected mods from the guide. Download and install the following:

- **Main File** - Widescreen Fix for SkyUI 5.2 SE Alpha - 2560x1080
- **Optional File** - Better Dialogue Control Widescreen Fix `replaces the original mod`
- **Optional File** - Better MessageBox Control Widescreen Fix `replaces the original mod`
- **Optional File** - Extended UI - Widescreen Fix `optional in the guide`
- **Optional File** - Race Menu SE - WIdescreen Fix
- **Optional File** - SkyHud - High Resolution Widescreen Fix
- **Optional File** - Wider MCM Menu for SkyUI - Widescreen Fix `optional in the guide`

## [Remove QuickSave Button](https://www.nexusmods.com/skyrimspecialedition/mods/28334?tab=files) (optional)

Download the **Remove QuickSave Button - UltraWide** main file and replace the original mod with it. This mod is also optional in the guide.

![separator](../Media/separator.png)

# Misc Mods

## [SkyUI Config Tweak - Equipped Items On Top](https://www.nexusmods.com/skyrimspecialedition/mods/32711?tab=files) (optional)

### Download Instructions

- **Main File** - SkyUI Config Tweak - Equipped Items On Top

### Mod Order

- Place below the **INTERFACE** separator.

### About the mod

It keeps the equipped items "stickied" to the top of the inventory page. Personally I find it very annoying but it's an easy addition for those who like it.

## Winterhold Statue - Animated with Light (optional)

In late  2019 there was a remesh of the Winterhold College statue published which added features like ENB Particle Light for the orbs that it is holding. Unfortuntely the mod has been hidden for a while now. If you still have a copy of it on your hard drive (of version 1.1) and you are running ENBSeries, feel free to add it to the **ENB PARTICLE LIGHTS** section in your mod order.

If you "found" the file elsewhere on the internet, make sure it is the SE version (not LE).

[**Original (hidden) mod.**](https://www.nexusmods.com/skyrimspecialedition/mods/29478)

## DirtCliff Remaster (optional)

This is the first and the last mod by LupusHegemonia to ever be mentioned in the guide. LH himself is an asset thief and drama queen  extraordinaire with many of his mods being cheap rip-offs and upscaled textures. With his DirtCliff remaster however he published one I liked. Quite a bit actually. Since LH was banned from the Nexus for thievery and impossibly rude behaviour, you will have to acquire the files elsewhere.

* LH’s HD DirtCliff Remaster 2K 1.5
* LH’s HD DirtCliff Remaster – Solstheim 2K 1.5
* LH’s HD DirtCliff Remaster – SMIM 2K 1.5
* [LH’s HD DirtCliff Remaster – Majestic Mountains Complementary Texture](https://www.nexusmods.com/skyrimspecialedition/mods/18790)

The final file was created by someone else and is still available on the Nexus. Check its mod page for preview pictures of the retexture.

Place all four files right below **Landscapes - Cathedral Concept** in your mod order.

## [Trifle From Hiro – The Gate Solitude](https://www.nexusmods.com/skyrim/mods/59235) (optional)

### Download Instructions

* **Main Files** – Trifle from Hiro the Gate Solityyud

### Installation Instructions

This mod was not packaged correctly.

* Double-click **Gate Solitude from Hiro**.
* Right-click the **4096** (4K textures) folder and select **Set data directory**.
* Click **OK**.

### Mod Order

- Place the mod below the **ARCHITECTURE** separator in the mod order (below HQ Solitude if you installed that).

### About the mod

This texture is quite different from the (ugly) vanilla one and the (much better) Noble Skyrim alternative. I uploaded a direct comparison slider [here](https://imgsli.com/NDI1Mg).

![separator](../Media/separator.png)

# rougeshot's Skeleton Replacer

## About the mods

Mod author [rougeshot](https://www.nexusmods.com/skyrimspecialedition/users/20882614) has been publishing many skeleton overhauls for creatures that are quite popular. While I personally don’t like most of them, they are easy additions and can be dropped into a TPF setup anytime.

## Mod Order

All of the skeleton replacers have to be below **XPMSSE** (XP32 Maximum Skeleton Special Edition) in the mod order to overwrite.

## Already included

* [Immersive Dragons](https://www.nexusmods.com/skyrimspecialedition/mods/18957)
* [Supreme Vampire Lord](https://www.nexusmods.com/skyrimspecialedition/mods/19706) (XP32 Version)

## Can be added

* [Savage Bear](https://www.nexusmods.com/skyrimspecialedition/mods/16343)
* [Immersive Smilodon](https://www.nexusmods.com/skyrimspecialedition/mods/18429)
* [Nightmare Chaurus](https://www.nexusmods.com/skyrimspecialedition/mods/21488)
* [Marvelous Mudcrabs](https://www.nexusmods.com/skyrimspecialedition/mods/21685)
* [Grave Gargoyles](https://www.nexusmods.com/skyrimspecialedition/mods/21907)
* [Heartland Horses](https://www.nexusmods.com/skyrimspecialedition/mods/22083)
* [Supreme Chaurus Hunters](https://www.nexusmods.com/skyrimspecialedition/mods/22263)
* [Heinous Ash Hoppers](https://www.nexusmods.com/skyrimspecialedition/mods/22409)
* [Bristleback Boars](https://www.nexusmods.com/skyrimspecialedition/mods/22578)
* [Riekling Roughriders](https://www.nexusmods.com/skyrimspecialedition/mods/22765)
* [Riekling Reavers](https://www.nexusmods.com/skyrimspecialedition/mods/22948)
* [Looming Lurkers](https://www.nexusmods.com/skyrimspecialedition/mods/23122)
* [Supreme Seekers](https://www.nexusmods.com/skyrimspecialedition/mods/23349)
* [Sinister Spriggans](https://www.nexusmods.com/skyrimspecialedition/mods/23502)
* [Tyrannical Trolls](https://www.nexusmods.com/skyrimspecialedition/mods/23665)
* [Grandiose Giants](https://www.nexusmods.com/skyrimspecialedition/mods/23889)
* [Absolute Arachnophobia](https://www.nexusmods.com/skyrimspecialedition/mods/24058)
* [Mighty Mammoths](https://www.nexusmods.com/skyrimspecialedition/mods/24237)
* [Sickening Skeevers](https://www.nexusmods.com/skyrimspecialedition/mods/24428)
* [Astonishing Frost Atronarchs](https://www.nexusmods.com/skyrimspecialedition/mods/24641)
* [Astounding Flame Atronarchs](https://www.nexusmods.com/skyrimspecialedition/mods/24836)
* [Honored Hounds](https://www.nexusmods.com/skyrimspecialedition/mods/25563)
* [Gritty Goats](https://www.nexusmods.com/skyrimspecialedition/mods/26665)
* [Dreaded Dwarven Spiders](https://www.nexusmods.com/skyrimspecialedition/mods/27047)
* [Hardy Hares](https://www.nexusmods.com/skyrimspecialedition/mods/27366)
* [Salty Slaughterfish](https://www.nexusmods.com/skyrimspecialedition/mods/28005)
* [Hulking Horkers](https://www.nexusmods.com/skyrimspecialedition/mods/28383)
* [Notorious Netches](https://www.nexusmods.com/skyrimspecialedition/mods/29323)
* [Infamous Ice Wraiths](https://www.nexusmods.com/skyrimspecialedition/mods/29712)
* [Dramatic Deer](https://www.nexusmods.com/skyrimspecialedition/mods/31010)
* [Bullish Bovine](https://www.nexusmods.com/skyrimspecialedition/mods/33888)
* [Callous Dwemer Centurions](https://www.nexusmods.com/skyrimspecialedition/mods/34395)

## Do not add

- [Savage Wolves](https://www.nexusmods.com/skyrimspecialedition/mods/21075) - might not work properly with the new meshes from True Wolves of Skyrim
- [Wicked Werewolves](https://www.nexusmods.com/skyrimspecialedition/mods/31757) - would overwrite or be overwritten by Werewolf Claws Affect Spider Webs
- [Feral Foxes](https://www.nexusmods.com/skyrimspecialedition/mods/21298) - contains a plugin and potentially conflicts
- [Hellish Hounds](https://www.nexusmods.com/skyrimspecialedition/mods/30344) - contains a plugin and potentially conflicts

> While the two replacers with plugins may work perfectly fine with TPF, you would probably need to resolve conflicts with Mortal Enemies and/or other mods. I simply do not care enough about rougeshot's mods to provide instructions for that.

![separator](../Media/separator.png)

# Tree Tweaks

## Notes

There are a number of tweaks and mods you can add to customise the trees and landscape that are all easy to do except they require you to re-run DynDOLOD. We will go through these tweaks and generate new tree LOD afterwards. To clarfiy: **If you follow any of the steps in this section, you must regenerate DynDOLOD.**

Each step is optional but you do need to follow all instructions if you choose one.

## Enhanced Vanilla Trees Tweaks

### Reinstallation

While the guide includes my default recommended options for EVT, there are plenty of customisation options in the FOMOD, so we will go through them one by one. Find **Enhanced Vanilla Trees** in your mod order, right-click it and select **Reinstall**.

When you go through the FOMOD options, add your changes to the mod name. This will have two advantages: one, you won't overwrite your default installation of EVT, and two, you can easily see which option you used later on. For example I entered:

`Enhanced Vanilla Trees - Custom Large, Branches 2, RAT`

### FOMOD Choices

- **Mesh Options:**
  - Enhanced Darker Meshes `I always recommend this as the trunks can look strange and bright with the first version`
- **Select a tree option:**
  - *The guide recommends the "Lush Trees (small)" option here which is a solid upgrade over the vanilla option. If you have frames to spare, I highly recommend the (large) options (either Lush or Custom). They make the world feel larger and the woods seem like actual forests. Because of their size, shadows will be larger as well which will impact performance.*
  - Enhanced 'Vanilla' Trees `if you struggle with performance`
  - Lush Trees (small) `the guide's default choice`
  - Custom Trees (large) `performance-intense but looks amazing`
- **Clutter:**
  - Enhanced Tree Clutter (recommended)
  - ~~Firewood Textures~~ `I dislike the textures personally and prefer Tree Bark in HD (Installed in the main guide)`
- **Skyrim Flora Overhaul - Branches:**
  - *These new branch textures change Skyrim more than you would probably expect. I love Option 4 which is the guide's default choice. Option 2 is lovely as well. Take a good look at them all and make your own choice.*
- **Alternative Trees:**
  - Realistic Aspen Trees `choose this if you want RAT (differently coloured aspens) OR green aspens (will be covered later)`
  - SFO Snowy Pine Trees `default choice in the guide, they just look amazing`
- **Greener Bark Texture:**
  - *Depending on the options you chose, this might not appear. Personally I just skip all options here. If you'd like to try the different bark textures, tick the All-in-one option.*

### Mod Order

After redoing the FOMOD and installing the customised version of EVT, move it up in your mod order below the original EVT installation (below the **FLORA** separator) and activate it. Disable the original EVT version. Since these changes were made on your **The Phoenix Flavour - Customised** profile, they won't affect your default installation on the main profile.

## Green Aspen Trees

### Notes

If you chose the **Realistic Aspen Trees** option in the EVT FOMOD, you can now use the **Green Aspen Trees for EVT** optional module from Enhanced Landscapes.

You can find some pictures in the [image section](https://www.nexusmods.com/skyrimspecialedition/mods/18162?tab=images) of the Enhanced Landscapes mod page.

### Instructions

- Create an empty mod in Mod Organizer 2 and name it **Enhanced Landscapes - Green Aspen Trees for EVT**.
- Right-click it and select **Open in Explorer**.
- Go to `Your Modding Folder\ARCHIVE\MO2 Downloads` and find the following archive:
  - Main File v1.65-18162-1-65.7z
- Open the archive and double-click the **3 - AspenGreeEVT** file inside.
- Extract the **textures** folder to `Mod Organizer 2\mods\Enhanced Landscapes - Green Aspen Trees for EVT`.
- Close the archive and the Explorer window.

### Mod Order

- Go back to Mod Organizer 2 and press F5 to refresh.
- Move the new mod below **Enhanced Vanilla Trees - Vurts Light Snow Tree Replacer** in your mod order and activate it.

### Aspen Leaves

If you installed [Rudy HQ - Falling Leaves and Needles](https://www.nexusmods.com/skyrimspecialedition/mods/25939) during the main guide, follow these instructions:

- Download the following file from the [Rudy HQ - Falling Leaves and Needles](https://www.nexusmods.com/skyrimspecialedition/mods/25939?tab=files) Nexus page:
  - Rudy HQ - Falling Leaves and Needles SE - Green Leaves Texture 1K
- Place it below **Rudy HQ - Falling Leaves and Needles (ENB)** in your mod order and activate it.

## Solstheim 3D Trees

### Requirements

Enhanced Landscapes contains an optional set of textures and LOD files for improved ash trees on Solstheim. Unfortunately, **the LOD files only support 3D tree LOD**. If you have more than 4GB VRAM and some frames to spare, I highly recommend installing these textures and generating 3D tree LOD later on. Otherwise skip this step.

### Instructions

- Create an empty mod in Mod Organizer 2 and name it **Enhanced Landscapes - Solstheim 3D Trees**.
- Right-click it and select **Open in Explorer**.
- Go to `Your Modding Folder\ARCHIVE\MO2 Downloads` and find the following archive:
  - Main File v1.65-18162-1-65.7z
- Open the archive and double-click the **3 - Solstheim3DTrees** file inside.
- Extract the **textures** and **meshes** folders to `Mod Organizer 2\mods\Enhanced Landscapes - Solstheim 3D Trees`.
- Close the archive and the Explorer window.
- Go back to Mod Organizer 2 and press F5 to refresh.
- Move the new mod below **Enhanced Vanilla Trees - Vurts Light Snow Tree Replacer** in your mod order and activate it.

![Solstheim Trees Installation](Pictures/customisation/solstheim_tree_installation.png)

### Mod Order

- Go back to Mod Organizer 2 and press F5 to refresh.
- Move the new mod above **Enhanced Landscapes - Oaks Standalone (Mixed Greens)** in your mod order and activate it.

## Whiterun Forest Borealis

### About

This mod will turn the Whiterun tundra into a boreal forest. It will change the familiar valley into a completely different place. Be sure to watch [hodilton's video showcase](https://youtu.be/bntU_zFPWzg) first before you decide whether or not to install it. Note that the distant terrain with TPF will look a good deal better than hodilton's in the video.

### Installation

- Download and install the following file from the [Whiterun Forest Borealis](https://www.nexusmods.com/skyrimspecialedition/mods/11343?tab=files) Nexus page:
  - Whiterun Forest Borealis v2.1.2
- Place the mod below **Bent Pines II** in the mod order and activate it.
- Move the plugin below **BentPines.esp** in the load order and make sure it's checked.

![separator](../Media/separator.png)

# Arthmoor's New Towns

## The Dilemma

The five additional town mods by Arthmoor were removed from the main guide in the 3.2 update. The primary reason for that was that the majority of the userbase felt they detracted from immersion rather than adding to it due to the fact that the NPCs have only generic dialogue. They will not interact with the player in any way, there are no location specific comments or quests. The towns feel like props, cardboard cutout stand-ins, rather than actual settlements.

A smaller part of the userbase argued however that even as pretend-towns, they add to the world of Skyrim. Without Arthmoor's Oakwood, the hold of Falkreath has zero villages beyond its capital. Oakwood is also conveniently close to Lakeview Manor, the Hearthfire player home overlooking Lake Ilinalta, connecting the Manor to civilisation. 

It is therefore up to the individual user to decide what is more immersion-breaking: Towns where nobody interacts with you, or no towns at all.

## [Helarchen Creek](https://www.nexusmods.com/skyrimspecialedition/mods/4043?tab=files) (optional)

### Download Instructions

- **Main File** - Helarchen Creek

### Mod & Load Order

- Place the mod below **Provincial Courier Service** in the mod order and active it.
- Move the plugin below **Provincial Courier Service.esp** in your load order.

## [Keld-Nar](https://www.nexusmods.com/skyrimspecialedition/mods/14353?tab=files) (optional)

### Download Instructions

- **Main File** - Keld-Nar

### Mod & Load Order

- Place the mod below **Provincial Courier Service** (or previous Arthmoor Town Mods) in the mod order and active it.
- Move the plugin below **Provincial Courier Service.esp** (or previous Arthmoor Town Mods) in your load order.

### Additional Instructions

- Run **SSEEdit** through Mod Organizer 2.
- In the plugin selection window, click **OK** to load all plugins.
- Wait until SSEEdit has finished loading.
- Find **Keld-Nar.esp** in the left pane and double-click it.
- Navigate to `Dialogue Topic\PerkInvestorBranch1Topic1`.
- Right-click and remove the following record:
  - `000B1FE9`
- Click **Yes, I am sure** when the warning window pops up and confirm to delete.
- Close SSEEdit. Click **OK** to save your changes.

> The record contains only one edit that is already made in the USSEP but overrides another one from Trade & Barter. The simplest solution is to just delete it.

![Keld-Nar - Delete Record](Pictures/customisation/keldnar_delete_record.png)

## Simple Children - Keld-Nar Patch (optional)

### Download Instructions

- You already downloaded the necessary file during the main guide.

> **Mod Dependency:** Only install this mod if you installed **Keld-Nar**. Otherwise skip it.

### Installation Instructions

- Find **Simple Children - Patches** in your mod order, right-click it and select **Reinstall**.
- In the FOMOD, unselect everything except the **Keld-Nar** option on the second page.
- On the third page, set the **Prince and Pauper** and **Adopt Aventus Aretino** options both to **None**.
- After clicking **Install**, select **Rename** (we do not want to replace the original file).
- Rename the file to ==Simple Children - Keld-Nar Patch== and click **OK**.

### Mod & Load Order

- Place the mod below **Simple Children - Patches** in the mod order and active it.
- Move the plugin below **3D_FacegenForKids.esp** in your load order.

## [Telengard](https://www.nexusmods.com/skyrimspecialedition/mods/17423?tab=files) (optional)

### Download Instructions

- **Main File** - Telengard

### Mod & Load Order

- Place the mod below **Provincial Courier Service** (or previous Arthmoor Town Mods) in the mod order and active it.
- Move the plugin below **Provincial Courier Service.esp** (or previous Arthmoor Town Mods) in your load order.

## [The Fall of Granite Hill](https://www.nexusmods.com/skyrimspecialedition/mods/22512?tab=files) (optional)

### Download Instructions

- **Main File** - The Fall of Granite Hill

### Mod & Load Order

- Place the mod below **Provincial Courier Service** (or previous Arthmoor Town Mods) in the mod order and active it.
- Move the plugin below **Provincial Courier Service.esp** (or previous Arthmoor Town Mods) in your load order.

## [Oakwood](https://www.nexusmods.com/skyrimspecialedition/mods/27564?tab=files) (optional)

### Download Instructions

- **Main File** - Oakwood

### Mod & Load Order

- Place the mod below **Provincial Courier Service** (or previous Arthmoor Town Mods) in the mod order and active it.
- Move the plugin below **Provincial Courier Service.esp** (or previous Arthmoor Town Mods) in your load order.

## Landscape Fixes for Grass Mods - Oakwood (optional)

### Download Instructions

- You already downloaded the necessary file during the main guide.

> **Mod Dependency:** Only install this mod if you installed **Oakwood**. Otherwise skip it.

### Installation Instructions

- Find **Landscape Fixes For Grass Mods - Patches for Arthmoor's Town** in your mod order, right-click it and select **Reinstall**.
- In the FOMOD, select only the **Patch for Oakwood** option.
- After clicking **Install**, select **Rename** (we do not want to replace the original file).
- Rename the file to ==Landscape Fixes for Grass Mods - Oakwood Patch== and click **OK**.

### Mod & Load Order

- Place the mod below **Landscape Fixes For Grass Mods - Patches for Arthmoor's Town** in the mod order and active it.
- Move the plugin below **Landscape For Grass Mods -Provincial Courier PATCH.esp** in your load order.

## [Arthmoor's Towns - Patch Pack](https://www.nexusmods.com/skyrimspecialedition/mods/26092?tab=files)

### Download Instructions

- **Main File** - Arthmoor's Towns - Patch Pack

### FOMOD Instructions

- Since both **Realistic Water Two** and **Trade & Barter** are required mods in the guide, you will need to select the patches for all town mods that you have installed.

### Mod & Load Order

- Place the mod below **Morrowloot Ultimate - INIGO Patch** in the mod order and active it.
- Move all plugins below **MLU - Inigo.esp** in your load order.

![separator](../Media/separator.png)

# Plugin Edits

## Dwemer Spectres - Remove Beards

By default, Dwemer Spectres includes the beards from [this mod](https://www.nexusmods.com/skyrim/mods/30062). Personally, I dislike these beards a lot and I recommend removing the 'Playable' flag from them so that they no longer appear in the character creation menu. This is easy to do in xEdit.

- Run SSEEdit through Mod Organizer 2.
- Click **OK** to load all your plugins and wait for SSEEdit to return `Background loader: finished`.
- Double-click **DwemerSpectresLegendary.esp** in the left pane.
- Expand the Head Part section. The records you need to edit are numbered.
- Click on `1. Dwemer Beard: Basic`. Under **DATA - Flags (sorted)**, right-click and select **Edit**.
- Click **Yes I'm absolutely sure** when the warning window pops up.
- Uncheck **Playable** in the list that pops up and click **OK** (see picture below).
- Repeat this process for the remaining records:
  - `3. Dwemer Beard: Lower `
  - `11. Dwemer Beard: Morrowind`
  - `5. Dwemer Beard: Lower Braids + Moustache`
  - `2. Dwemer Beard: Basic + Moustache`
  - `13: Dwemer Beard: Morrowind No Sideburns`
  - `14. Dwemer Beard: Morrowind No Sideburns or Moustache`
  - `12. Dwemer Beard: Morrowind No Moustache`
  - `9. Dwemer Beard - Full Braided Goatee`
  - `4. Dwemer Beard: Lower Braids + Sideburns`
  - `6. Dwemer Beard: Lower Braids + Moustache + Sideburns`
  - `7. Dwemer Beard: Lower Braids Goatee`
  - `10. DWemer Beard: Full Braided Goatee + Moustache`
  - `8. Dwemer Beard: Lower Braids Goatee + Moustache`
  - `15. Dwemer Beard: Nordic Style`
- When you're done, close SSEEdit and click **OK** to save your changes.

![Dwemer Spectres Remove Beards](Pictures/customisation/dwemer_spectres_remove_beards.png)

![separator](../Media/separator.png)

# Removing ENB

## Considerations

### Performance

There are two reasons for removing ENBSeries: Either your machine has such low specs you cannot possibly run a preset while preserving an acceptable framerate, or you are among the few preferring vanilla visuals. Either way, by removing ENB you will most likely improve the game’s performance significantly.

Keep in mind that it is possible to tweak ENB presets or swap to a less performance-hungry preset like The Truth ENB.

You can also use the hotkey ingame to disable ENB completely without removing it outright. This will give you an idea of how the game would look and feel like without it. The default hotkey to toggle the effect is F12.

### What you will miss out on

The obvious disadvantage of removing ENB is the improved visuals, snappier shadows, much improved Ambient Occlusion, more saturated colours and a bunch of ENB-exclusive features.

One of those features is Complex Particle Lighting which is required for mods such as **ENB Light** and Rudy’s **More Lights for ENB** series of which most are included in The Phoenix Flavour. On the upside, you will also be able to lower the particle count when no longer using ENB Light which may improve performance further.

### Personal recommendation

If you are considering to remove ENB because of the performance impact, I would definitely urge you to try other presets or tweak your  own to tone down the FPS loss. On all except the weakest systems, you should be able to reach mostly stable 60FPS with a (tweaked) ENB preset.

## Getting rid of ENBSeries

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

### INI Editor

Without ENBSeries, there are several graphical enhancements that can be forced directly in the game. These will give better performance (with lower quality) than similar effects that could be forced through ENB.

In Mod Organizer 2, go to **Tools** > **INI Editor** in order to edit your INI files directly through MO2’s interface.

### Ambient Occlusion

You now have the option to use Skyrim’s inbuilt Ambient  Occlusion (which has a performance impact of its own and does not look as good as ENB AO). Enabling Ambient Occlusion may result in a performance loss but not nearly as much as enabling ENB with AO would.

In the [Display] section of your **SkyrimPrefs.ini**, change the following:

`bSAOEnable=1`

### Particles

ENB Light (and meshes utilising the ENB Complex Particle Lights  feature in general) required you to increase your particle count for  better visuals which may also potentially impact performance so we will reverse this.

In the [Particles] section of your **SkyrimPrefs.ini**, change the following:

`iMaxDesired=2000`

## Potential Replacements

### IMAGINATOR

Even without ENBSeries there are ways to tweak the lighting and colours in your game to your liking. With the default guide setup, you can use the **Obsidian Weathers** MCM to tweak the general tone and colour settings. There are several presets to choose from.

There is also the mod [IMAGINATOR](https://www.nexusmods.com/skyrimspecialedition/mods/4577) by Gopher, created to replace the colour customisation ENB offers. While it should not have a performance impact at all, it is not comparable to ENBSeries. For some people it may still be worth the performance gain. Feel free to try it out.

Please note that IMAGINATOR is a not officially included in the guide, meaning I will provide no installation instructions and no support for issues with the mod.

### ReShade

Unlike ENBSeries, ReShade was not specifically created for Skyrim SE and has no way to interact with the engine for advanced effects. It is however a very capable, customisable and performance-friendly FX injector that may replace ENBSeries for those with weaker hardware (or different preferences with regards to visuals).

The [ReShade Framework](https://reshade.me/) is easy enough to install, however depending on your chose preset, you may require a certain version of it, or a specific set of shaders. To find presets, just search for **Reshade** on the  Special Edition Nexus. A word of warning though: There are still plenty of ENB-ReShade presets floating around which were made for both ENBSeries and ReShade to complement each other. Take care and read the mod page before installing.

Creating your own preset is arguably easier to do than it is with ENBSeries. ReShade can also be edited and customised ingame.

![separator](../Media/separator.png)

# DynDOLOD

## Preparations

### Old Output

If you installed anything from **Tree Tweaks** or **Arthmoor's Towns**, you MUST re-generate LOD with DynDOLOD - either with 3D or regular tree LOD.

- Re-running TexGen is **not required** so you can keep your **TexGen_Output** active.
- Uncheck **DynDOLOD ({Preset})** in your mod order.

### Empty Cache

- Navigate to `Your Modding Folder\Tools\DynDOLOD\Edit Scripts\DynDOLOD\cache`.
- Delete everything inside (CTRL+A and DEL).

### Tree LOD Type

- Navigate to `Your Modding Folder\Tools\DynDOLOD\Edit Scripts\DynDOLOD\`.
- Open **DynDOLOD_SSE.ini** in Notepad++.
- Find the following line: ==TreeLOD=<value>==.
  - Set to 1 for regular tree LOD.
  - Set to 0 for 3D tree LOD.

## Running DynDOLOD

* Launch **DynDOLOD** through Mod Organizer 2.
* A window will come up, click **Advanced**.
* You can see a list of all worldspaces at the top. Right-click inside and **Select all**.
* Select a preset:
  * **Low** if you already struggle with performance.
  * **Medium** as the default option plus regular tree LOD.
  * **High** for modern machines and 3D tree LOD.
* Under **Load rules for** check both **Candles** and **FXGlow**.
* Double-check with the picture below that everything is configured correctly, then click **OK**.

**Step away from your PC while DynDOLOD is working.**

![DynDOLOD Settings](Pictures/finalisation/dyndolod_settings.png)

## DynDOLOD Output

* Once DynDOLOD is done, click **Save & Exit**.
* Go to `Your Modding Folder\Tools\DynDOLOD`.
* Cut (CTRL+X) the **DynDOLOD_output** folder and paste it (CTRL+V) to `Mod Organizer 2\mods`.
* Refresh Mod Organizer 2 (F5) and it will appear at the bottom of your load order.
* Rename the file and add the preset you selected, eg: `DynDOLOD - Customisation (Medium)`.
* Place it last below the (deactivated) `DynDOLOD ({Preset})` and activate it.
* Move **DynDOLOD.esm** below your other ESMs at the top of your load order.
* Leave **DynDOLOD.esp** at the very bottom as the last plugin.