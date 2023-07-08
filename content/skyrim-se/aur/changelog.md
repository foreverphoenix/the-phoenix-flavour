---
title: "Changelog"
weight: 4
type: docs
description: >
  Update notes for Aurora.
---

## Release 1.4

> 08/07/2023

Applied changes from **Skyrim Modding Essentials** 2.5.0.

After some deliberation I have decided to switch the *half-size* versions of Xavbio's armors and weapons retextures. As these are half the resolution (4K > 2K, 2K > 1K, etc), they are actually only a *quarter* of the size which means the half-size textures only require a quarter of the disc space and VRAM. IconicDeath recently made a [strong case](https://www.reddit.com/r/skyrimmods/comments/115v86r/4k_textures_for_weapons_and_armor_are_practically/) against 4K textures for armors and weapons as most of the time only the 2K mipmaps are loaded. For *pure gameplay* purposes, 4K textures for armors and weapons are therefore overkill, and Aurora is not a list intended for screenarchery.

Some discussions on the r/skyrimmods Discord convinced me to remove **Fixed Mesh Lighting** for now. If/when I notice overly-bright meshes in the future, I will selectively re-add parts of the mod.

Skin textures were criticised for being too smooth in Aurora and were switched out for a different combination. I also added **Ethereal Elven Overhaul**, an old favourite of mine (though without the individual face edits), and completely regenerated facegen for all NPCs. **Expressive Facial Animations** (male and female) were (at least temporarily) disabled as they seemed to cause issues with EEO.

A lot of individual asset replacers were removed in favour of the new **Skyland Bits and Bobs - Clutter Overhaul**. Since this is a fairly huge package I have not yet reviewed and compared all assets which means a good chunk of it is still currently being overwritten. Mostly, I just cannot decide which asset I prefer, especially when it comes to furniture. Consider it a bit of a work in progress.

#### Additions

- Added [[higher-poly-vanilla-cave-lamps]]
- Added [[fixed-spider-eggs-and-webs-in-solstheim]]
- Added [[dyndolod-solitude-windmill-rotor-smim-patch]]
- Added [[skyland-offset-shingles-fixed-aligned-whiterun-roofs]]
- Added [[skyland-bits-and-bobs-clutter-overhaul]]
- Added [[whiterun-objects-smimed-dragonsreach-stairs]]
- Added **Lux master plugin update** to [[lux]]
- Added [[mesh-patches-for-lux-and-lux-orbis]]
- Added [[diverse-candles-base-object-swapper]]
- Added [[lucid-skin]]
- Added [[vitruvia-skin-texture-overhaul-for-males]]
- Added [[ethereal-elven-overhaul]]
- Added [[butterfly-improved-by-zzjay]]
- Added [[butterfly-improved-by-zzjay-saints-and-seducers-patch]]
- Added [[fluffy-moths]]
- Added [[dwemer-armors-and-weapons-retexture]]
- Added [[modular-armory-dwemer-armors-and-weapons-patch]]
- Added [[chitin-armors-retexture]]
- Added [[bonemold-armors-and-weapons-retexture]]
- Added [[karstaag-the-frost-king-reborn]]
- Added [[sds-lotta-patches]]

#### Updates

- Updated [[skyrim-objects-smimed-noble-furniture]] to 0.5
- Updated [[lux]] to 6.2
- Updated [[embers-xd]] to 2.7.8
- Updated [[cc-camping-embers-xd-patch]] to 1.1
- Updated [[happy-little-logs]] to 1.7
- Updated [[3d-junipers-trees-and-berries]] to 0.2
- Updated [[hq-vanilla-tiny-rocks]] to 2.4.1
- Updated [[cathedral-3d-sword-ferns]] to 4
- Updated [[caveworm-plant-retexture]] (ENB Light Patch) to 1.4
- Updated [[skyrim-remastered-glaciers-and-ice-imr-edition]] to 1.30
- Updated [[icy-mesh-remaster]] to 2.20
- Updated [[stony-af-markarth-and-dwemer-ruins]] to 2.2
- Updated [[iron-armors-and-weapons-retexture]] to 1.1
- Updated [[imperial-armors-and-weapons-retexture]] to 1.2
- Updated [[elven-armors-and-weapons-retexture]] to 1.01
- Updated [[orcish-armors-and-weapons-retexture]] to 1.1
- Updated [[ebony-armors-and-weapons-retexture]] to 1.21
- Updated [[daedric-armors-and-weapons-retexture]] to 1.2
- Updated [[dragon-armors-and-weapons-retexture]] to 1.3

#### Removals

- Removed [[fixed-mesh-lighting]]
- Removed [[fixed-mesh-lighting-cc-backpacks]]
- Removed [[rudy-hq-nordic-ruins-pots-addon]]
- Removed [[tempered-skins-for-females]]
- Removed [[tempered-skins-for-males]]
- Removed [[tempered-racial-textures]]
- Removed [[tempered-racial-textures-ring-of-disrobing]]
- Removed [[afflicted-female-hand-fix]]
- Removed [[simple-sacks]]
- Removed [[skyland-blacksmith-texture-overhaul]]
- Removed [[vanilla-table-replacers]]
- Removed [[fyx-vanilla-table-replacers]]
- Removed [[rustic-furniture]]
- Removed [[rustic-furniture-uv-fix]]
- Removed [[weathered-furniture-common-and-upper-class]]
- Removed [[weathered-bars-and-counters-retexture]]
- Removed [[weathered-bars-and-counters-bar-stools-addon]]
- Removed [[skyland-chests]]
- Removed [[weathered-bucket-retexture]]
- Removed [[hd-better-instruments]]
- Removed [[ruins-tools-retexture]]
- Removed [[torture-tools]]
- Removed [[retexture-for-the-scroll]]
- Removed [[remiros-chitin-armor-hd]]
- Removed [[modular-armory-unique-zephyr]]

#### Other

- Regenerated facegen for all NPCs
- Enabled [[kezymas-root-builder]] support for [[curation-club]]
- Fixed `bFreebiesSeen=1` in the active INIs as well as two backup sets
- Disabled Distant Animated Fogs in the [[mists-of-tamriel-mcm-preset]] for the time being
	- *Should prevent [[embers-xd]] fires from disappearing*
- Updated FOMOD instructions for [[lux]]
- Updated FOMOD instructions for [[modular-armory]]
- Changed download instructions for [[leather-armors-retexture]]
- Changed download instructions for [[ancient-nord-armors-and-weapons-retexture]]
- Changed download instructions for [[iron-armors-and-weapons-retexture]]
- Changed download instructions for [[imperial-armors-and-weapons-retexture]]
- Changed download instructions for [[steel-armors-and-weapons-retexture]]
- Changed download instructions for [[silver-armor-and-weapons-retexture]]
- Changed download instructions for [[wolf-armors-and-weapons-retexture]]
- Changed download instructions for [[elven-armors-and-weapons-retexture]]
- Changed download instructions for [[falmer-armors-and-weapons-retexture]]
- Changed download instructions for [[blades-armors-and-weapons-retexture]]
- Changed download instructions for [[orcish-armors-and-weapons-retexture]]
- Changed download instructions for [[nordic-carved-armors-and-weapons-retexture]]
- Changed download instructions for [[glass-armors-and-weapons-retexture]]
- Changed download instructions for [[ebony-armors-and-weapons-retexture]]
- Changed download instructions for [[daedric-armors-and-weapons-retexture]]
- Changed download instructions for [[dragon-armors-and-weapons-retexture]]
- Removed some overwritten assets from [[whiterun-mesh-fixes]]
- Removed some overwritten assets from [[wiseman-flora-fixes-revamped]]
- Removed some overwritten assets from [[static-mesh-improvement-mod]]
- Removed some overwritten assets from [[markarth-fixed-af]]
- Removed some overwriting assets from [[ruins-clutter-improved]]
- Removed some overwriting assets from [[rudy-hq-nordic-ruins]]
- Removed redundant / overwriting assets from [[misc-retexture-project]]
- Removed an overwritten texture from [[creation-club-content-properly-environment-mapped-dwarven-armored-mudcrab]]
- Removed an overwriting asset from [[weldingmans-smelter-with-enb-light]]
- Removed an overwritten asset from [[skyrim-remastered-glaciers-and-ice-imr-edition]]
- Removed some overwritten assets from [[happy-little-trees]]
- Removed an overwriting asset from [[falmer-pullchain-enb-light]]
- Removed overwriting assets from [[overlooked-dungeon-objects-retextures]]
- Removed overwriting assets from [[hd-meshes-and-textures-for-animal-and-creature-drops]]
- Removed an out-of-scope edit from the [[obsidian-weathers-and-seasons]] plugin
- No longer removing some assets from [[skyrim-objects-smimed-noble-furniture]]
- No longer removing assets from [[3d-junipers-trees-and-berries]]
- No longer removing some assets from [[maris-flora]]
- No longer removing assets from [[rustic-animated-potions-and-poisons]]
- No longer removing an asset from [[high-poly-project-vaerminas-torpor]]