---
title: "Documentation"
weight: 4
type: docs
description: >
  Mods and features included in Legends of the Frost.
---

**Legends of the Frost** contains all of the most important baseline mods, including:

- [Unofficial Skyrim Special Edition Patch](https://www.nexusmods.com/skyrimspecialedition/mods/266): A ton of bug and consistency fixes of all kinds.
- [SSE Engine Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/17230): Enables achievements with mods, fixes lip sync as well as many other bugs and crashes.
- [SSE Display Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/34705): Decouples physics engine and framerate. Improves performance in borderless-fullscreen.
- [Weapons Armor Clothing and Clutter Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/18994): Fixes a ton of issues and inconsistencies in gear progression and related assets.
- [Skyrim Landscape and Grass Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/26138): Closes many gaps in the landscape and eliminates many other visual bugs.

In addition to these, there are several dozen other bug fix mods including many mesh fixes as well as a bunch of tweaks.

### Weather & Lighting

After some testing, I settled on [Wander - A Weather Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/24439) which turned out to be an incredible mod with some serious improvements to vanilla weathers. The mod's weathers, their colours and variance are spot on. Nights are darker, but not unplayable. I decreased the strength of the fog obscuring distant terrain, one of the mod's main features, as it looks infinitely better than in vanilla with LOTF's regenerated terrain, tree, and object LODs.

I played without an ENB preset initially, but quickly realised that the visual improvements of a lightweight preset were simply too good to miss out on. Since The Truth ENB is no longer on the Nexus, I added [Minimal ENB for Obsidian Weathers](https://www.nexusmods.com/skyrimspecialedition/mods/37098) which is perfectly suited for any weather overhaul on account of the fact that it does not change any colours. Water settings were tweaked to better hide the distant seams (thanks Shade!).

As of LOTF 1.4, ENB complex particle light (*without* the performance-intense Big Range setting) was re-enabled for the [Radiant - Candles](https://www.nexusmods.com/skyrimspecialedition/mods/55856) mod. You can find a comparison slider showing off the effect [here](https://imgsli.com/NzcwMjA).

For interiors I combined [Relighting Skyrim](https://www.nexusmods.com/skyrimspecialedition/mods/8586) with its lightbulb adjustments and fixes with [Ambiance](https://www.nexusmods.com/skyrimspecialedition/mods/46383). Together these two mods tone down vanilla's often overly bright interiors, again without making them unplayable, as well as reduce the ambient light without actual sources.

### Textures & Meshes

This section was the hardest one for me to limit myself. In my personal opinion, there are two choices when starting to replace textures in Skyrim: Either stick strictly to the vanilla style using primarily upscaled textures, or go all in with hundreds of hand-made, high-quality textures. Naturally, I went with the latter for Legends of the Frost and chose [Project Clarity](https://www.nexusmods.com/skyrimspecialedition/users/34739755?tab=user+files) and [Skyrim Realistic Overhaul](https://www.moddb.com/mods/skyrim-realistic-overhaul) to make up the bulk of the replaced textures (and the overall filesize).

(If you are wondering why vanilla textures were not an option, watch [this video](https://youtu.be/nHkCJcUJkTM).)

Beyond these major overhauls, I elected to add only those mods that I consider absolutely essential for fixing various eye sores. This includes [Static Mesh Improvement Mod](https://www.nexusmods.com/skyrimspecialedition/mods/659) and [Blended Roads](https://www.nexusmods.com/skyrimspecialedition/mods/8834) as well as [Majestic Mountains](https://www.nexusmods.com/skyrimspecialedition/mods/11052). Water was hugely improved by [Cathedral Water Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/22962).

Most flora-related textures are covered by [Cathedral - Plants](https://www.nexusmods.com/skyrimspecialedition/mods/26104) and [Cathedral - Mushrooms](https://www.nexusmods.com/skyrimspecialedition/mods/26103). I did add [Enhanced Vanilla Trees](https://www.nexusmods.com/skyrimspecialedition/mods/11008) to the mix, using the lush version for improved meshes and textures, and vastly improved LOD resources, but with the same colours as vanilla trees. With [HD Vanilla Tree Bark - ESRGAN AI Upscale](https://www.nexusmods.com/skyrimspecialedition/mods/37890), their bark textures were significantly improved.

I considered sticking with vanilla grass, but eventually opted for [Skyrim Flora Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/2154) grass instead. It is close in style to vanilla (more sparse than most other grass overhauls) while looking noticably better in many places.

### Character Appearance

NPC faces (and hair) in Skyrim were never particularly appealing so I added a number of mods to freshen them up. Both males and females now have higher poly hands and feet instead of the [vanilla abominations](https://i.redd.it/0wp849fgwcv01.png). I added [Tempered Skins for Females](https://www.nexusmods.com/skyrimspecialedition/mods/8505)  and [Tempered Skins for Males](https://www.nexusmods.com/skyrimspecialedition/mods/7902). For eyes, both meshes and textures were improved by [Skyrim Ultimate Eyemeshes Ruhmastered](https://www.nexusmods.com/skyrimspecialedition/mods/18147) and [Authentic Eyes](https://www.nexusmods.com/skyrimspecialedition/mods/36063) respectively.

Thanks to [Natural Hair Colors](https://www.nexusmods.com/skyrimspecialedition/mods/46299), blonde hair will no longer have a sickly green tinge. [High Poly Vanilla Hair](https://www.nexusmods.com/skyrimspecialedition/mods/41863) and [Superior Lore-Friendly Hair](https://www.nexusmods.com/skyrim/mods/36510) offer further improvements. Retextures for brows as well as tintmasks (scars, warpaint, and dirt) are included in [Xenius Character Enhancements](https://www.nexusmods.com/skyrimspecialedition/mods/36985). The tintmasks are largely in 2K which you will be able to see in game thanks to a modified **SKSE.ini** enabling higher resolution tintmasks.

Lastly, [Simple Children](https://www.nexusmods.com/skyrimspecialedition/mods/22789) was installed alongside the TRI files from [TK Children](https://www.nexusmods.com/skyrimspecialedition/mods/5916) for less potato-headed offspring.

**Facegen was regenerated for all NPCs.** That means not only will they have twice the vanilla resolution (512 > 1024), but all previously installed mods will apply to NPCs as well. Premade facegen for children is included with Simple Children.

### Interface & Controls

Beyond the general lighting, there is one other aspect of vanilla Skyrim that I wanted thoroughly overhauled: The console-optimised interface. [SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/12604) is absolutely essentially for many reasons, but primarily because it hugely improves the various menus visually and functionally. It also works perfectly fine with a controller.

Speaking of controllers, I added [Auto Input Switch](https://www.nexusmods.com/skyrimspecialedition/mods/54309) which allows you to use your keyboard while your controller is connected. [Better MessageBox Controls](https://www.nexusmods.com/skyrimspecialedition/mods/1428) and [Better Dialogue Controls](https://www.nexusmods.com/skyrimspecialedition/mods/1429) further improve controls. [Stay At The System Page](https://www.nexusmods.com/skyrimspecialedition/mods/19832) brings back Skyrim LE behaviour where pressing ESCAPE would bring you to the Systems menu instead of the Journal.

Because the vanilla cursor looks a tad oversized, I added [Smaller Vanilla Cursor](https://www.nexusmods.com/skyrimspecialedition/mods/20617) and [SkyHUD](https://www.nexusmods.com/skyrimspecialedition/mods/463) (with the Vanilla Small preset) to shrink it a little. When riding your horse you will be able to see its Stamina drain with [Horse Stamina HUD](https://www.nexusmods.com/skyrimspecialedition/mods/47076). Thanks to [Immersive HUD](https://www.nexusmods.com/skyrimspecialedition/mods/12440), you can toggle your entire HUD whenever you wish.

[moreHUD](https://www.nexusmods.com/skyrimspecialedition/mods/12688) adds various new elements to the UI: For example, you will be able to see your enemy's level as well as the size of their soul for potential capturing. Read books will be marked with a special icon and upon hovering over skill books, you will see a preview of the skill they improve. The book interface itself looks [better](https://imgsli.com/NzAzOTc) now thanks to [Convenient Reading UI](https://www.nexusmods.com/skyrimspecialedition/mods/50202) and [Realistic Paper](https://www.nexusmods.com/skyrim/mods/937).

[A Quality World Map](https://www.nexusmods.com/skyrimspecialedition/mods/5804) greatly improves the quality and usability of the world map. The game will no longer prompt you with a message box asking if you're sure when crafting certain items or exiting crafting menus thanks to [Yes Im Sure](https://www.nexusmods.com/skyrimspecialedition/mods/24898) and when attempting to drop quest items [Whose Quest Is It Anyway](https://www.nexusmods.com/skyrimspecialedition/mods/23581) will notify you which quest is binding the item to your inventory.

As background in the main menu you will see one of my favourite replacers: [DRELDYN's Original Main Menu Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/6992). The menu was reduced to only the necessary options by [ReCleaned Menu](https://www.nexusmods.com/skyrimspecialedition/mods/26680), and [Loading Screen Smoke Removed](https://www.nexusmods.com/skyrimspecialedition/mods/4634) removes the ugly background smoke effect. [KenMOD Time On Loading Screen](https://github.com/KenneyNL/Skyrim-Mods/tree/main/Time%20On%20Loading%20Screen) adds a tiny clock with your current system time to the loading screens. For my fellow Europeans, I added [Time Format Changer](https://www.nexusmods.com/skyrimspecialedition/mods/28921) which is an optional mod (disabled by default) and can be enabled to change the 12h clock to a 24h one.

### Gameplay & Difficulty

There is only a single major gameplay overhaul included in Legends of the Frost: [Blade and Blunt - A Combat Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/34549) greatly enhances combat so that resource management (specifically Stamina) becomes central to every fight. I did add the vanilla damage modifiers addon so that combat does not become significantly harder. Please refer to the mod page for up-to-date details on everything the mod does. I also added [Dragon War - A Dragon Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/51310) for its dragon AI improvements only.

**Perks, standing stones, and racial traits remain vanilla.** That means any vanilla character builds will most likely work fine in LOTF. (Please note that some smithing perks were adjusted by WACCF.)

With [Improved Traps](https://www.nexusmods.com/skyrimspecialedition/mods/17592) traps now create detection events when they are triggered (meaning they can alert enemies) and you have additional ways to disarm traps. Fortunately, followers will no longer trigger traps thanks to [Follower Trap Safety](https://www.nexusmods.com/skyrimspecialedition/mods/2755).

Because of [Scrambled Bugs](https://www.nexusmods.com/skyrimspecialedition/mods/43532), you will no longer be able to underfill soul gems: For instance, if you have no Empty Lesser Soul Gems in your inventory, a captured lesser soul will be lost rather than placed in an Empty Greater Soul Gem. The same mod will also make it so your *best* arrows or bolts are equipped upon switching to a ranged weapon instead of your *worst* (which is vanilla behaviour).

And finally horses were improved by [Simple Horse Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/50250). Most horses are set them to Cowardly and Protected, meaning they flee combat and can only be killed if the player deals the killing blow. Speed, stamina, and handling were also improved.

### Quests & NPCs

Radiant quests picked up in Skyrim will no longer have a chance to be on Solstheim with [Quests Are In Skyrim](https://www.nexusmods.com/skyrimspecialedition/mods/18416).

The following quests are also affected by mods:

- [Silence Is Golden](https://www.nexusmods.com/skyrimspecialedition/mods/50581): You have the option to lie to Lucan about finding the Golden Claw and keeping it instead.
- [Stones of Barenziah with Quest Markers](https://www.nexusmods.com/skyrimspecialedition/mods/22395): You can now enable quest markers for the Stones of Barenziah in the SSoB MCM.
- [No Thieves Guild Grind](https://www.nexusmods.com/skyrimspecialedition/mods/4382): The amount of radiant quests required to fully upgrade the Ragged Flaggon was reduced from 125 to 12.
- [The Paarthurnax Resolution](https://www.nexusmods.com/skyrimspecialedition/mods/43766): The Paarthurnax quest will now have a proper conclusion if you choose not to obey the Blades.

AS for NPCs, I added some general quality of life fixes. They will flee dragon and vampire attackes thanks to [Run For Your Lives](https://www.nexusmods.com/skyrimspecialedition/mods/2272). Various lines of dialogue were improved by [Misc Dialogue Edits](https://www.nexusmods.com/skyrimspecialedition/mods/28904) which largely adds conditions to make them more appropriate to the situation. [Tavern AI Fix](https://www.nexusmods.com/skyrimspecialedition/mods/23107) prevents innkeepers from showing you to your room unless you specifically ask them to. 
### Miscellaneous

- [Simple Player Home Improvements](https://www.nexusmods.com/skyrimspecialedition/mods/37236): Various visual and quality of life changes and additions for all vanilla player homes.
- [Faster Mining Plus](https://www.nexusmods.com/skyrimspecialedition/mods/2656): Mining now requires only one strike per ore (instead of three).
- [Night Eye Redux](https://www.nexusmods.com/skyrimspecialedition/mods/38348): The Night Eye power for Khajiit now lasts until turned off manually instead of 60s/day.
- [No Starting Spells](https://www.nexusmods.com/skyrimspecialedition/mods/38348): You will no longer have spells added to your character at the start of the game.
- [NPCs Run and Walk At Your Pace](https://www.nexusmods.com/skyrimspecialedition/mods/2482): NPCs walking speed now matches your own instead of being *slightly* slower.
- [Bard Instrumentals Mostly - Sing Rarely](https://www.nexusmods.com/skyrimspecialedition/mods/10927): Bards in inns will mostly play instrumentals unless you request a song.
- [Mannequin Management](https://www.nexusmods.com/skyrimspecialedition/mods/38221): This *should* fix the mannequins' creepy habit of moving around when you are not looking.