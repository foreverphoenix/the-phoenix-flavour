---
title: "Changelog"
weight: 4
type: docs
description: >
  Update notes for Aurora.
---

## Release 1.5.0

> 05/09/2023

Applied changes from **Skyrim Modding Essentials** 2.6.0 and 2.6.1.

With this update, I am removing AUR-X (the optional mods) from Aurora. Some of them will be part of [[yolviing-a-simonrim-experience]] and/or [[legacy-of-the-kitchensink]] instead.

Aurora now includes some changes to vanilla keybinds. Check the [[ingame-hotkeys]] documentation for details.

Regarding [[ethereal-elven-overhaul]], it became clear that fixing the neck seam issues would require skin colour tweaks (see linked page for details). For vanilla NPCs, these are included in the full EEO plugin, along with various other changes. Concerns about consistency with mod-added NPCs and the possibility of them having neck seams as well caused me to drop the mod.

(Full documentation including changelogs with functional links is available as an [Obsidian MD](https://obsidian.md/) vault on the Aurora Nexus page.)

#### Additions

- Added [[yurils-additional-resources]]
- Added [[photo-mode]]
- Added [[photo-mode-mcm-settings]]
- Added [[sb-fixed-windhelm-entrance]]
- Added [[bloodchill-manor-entrance-fix]]
- Added [[ice-wraith-teeth-collision-fixes]]
- Added [[drengins-blue-palace-mesh-only-replacer]]
- Added [[simple-snow-improvements-solstheim-ruins]]
- Added [[fyx-water-mesh-optimization]]
- Added [[fyx-3d-shack-kit-walls-lux-patch]]
- Added [[fyx-shack-kit-walls-abandoned-shack-and-frokis-shack-fix-lux-patch]]
- Added [[fyx-windhelm-graveyard]]
- Added [[sacks-remodeled]]
- Added [[folded-rag-diversification]]
- Added [[guards-and-stormcloak-armor-retexture]]
- Added [[forsworn-armors-and-weapons-retexture]]
- Added [[stalhrim-armors-and-weapons-retexture]]
- Added [[deathbrand-weapons-and-armor-replacer]]
- Added [[better-female-elks]]
- Added [[default-face-npcs-fixed]]

#### Updates

- Updated [[skyrim-landscape-and-water-fixes]] to 8.0
- Updated [[lod-model-library-for-dyndolod]] to 1.3.2
- Updated [[skyland-aio]] to 4.2
- Updated [[skyland-bits-and-bobs-clutter-overhaul]] to 1.6
- Updated [[skyland-offset-shingles-fixed-aligned-whiterun-roofs]] to 0.3
- Updated [[lux]] to 6.3
- Updated [[embers-xd]] to 2.8.8
- Updated [[diverse-candles-base-object-swapper]] to 1.2
- Updated [[misc-effects-enb-light]] to 1.6
- Updated [[animated-forge-water]] to 0.8
- Updated [[icy-mesh-remaster]] to 2.21
- Updated [[simplicity-of-snow]] to 0.15
- Updated [[cathedral-3d-mountain-flowers-base-object-swapper]] to 0.1.22
- Updated [[unique-markarth-doors]] to 0.4
- Updated [[security-overhaul-skse-lock-addons]] to 0.1.8

#### Removals

- Removed [[dyndolod-solitude-windmill-rotor-smim-patch]]
- Removed [[ethereal-elven-overhaul]]
- Removed [[enb-imod-separator-rudy-obsidian-config]]
- Removed [[hd-road-signs]]
- Removed [[hd-ruined-book-retexture]]
- Removed [[burnt-book-retexture]]
- Removed [[rallys-werewolf-totems]]
- Removed [[rustic-armor-and-weapons-forsworn-armor-and-weapons]]
- Removed [[frankly-hd-stormcloak-and-city-guards]]

#### Other

- Updated download instructions for [[ethereal-elven-overhaul]]
- Updated FOMOD instructions for [[modular-armory]]
- Added **Process Facegen** profile to [[cathedral-assets-optimizer]]
- Moved [[fyx-3d-coal-in-the-shovel]] from **Yuril's Mesh Edits** to **Fires & Candles**
- Moved [[fyx-3d-stockades]] from **Yuril's Mesh Edits** to **Architecture**
- Moved [[fyx-3d-stockades-walls-and-gate]] from **Yuril's Mesh Edits** to **Architecture**
- Moved [[fyx-3d-shack-kit-walls]] from **Yuril's Mesh Edits** to **Architecture**
- Moved [[fyx-3d-shack-kit-roofs]] from **Yuril's Mesh Edits** to **Architecture**
- Moved [[fyx-jorrvaskr]] from **Yuril's Mesh Edits** to **Architecture**
- Moved [[fyx-eastern-empire-company-building]] from **Yuril's Mesh Edits** to **Architecture**
- Moved [[fyx-riften-canal-and-round-posts]] from **Yuril's Mesh Edits** to **Architecture**
- Moved [[alt-markarths-forge]] from **Yuril's Mesh Edits** to **Architecture**
- Moved [[fyx-smooth-wells]] from **Yuril's Mesh Edits** to **Misc Structures**
- Moved [[fyx-row-boat]] from **Yuril's Mesh Edits** to **Misc Structures**
- Moved [[remove-ash-pebbles]] from **Alternative Assets** to **Grass Overhaul**
- [[misc-effects-enb-light-leanwolfs-better-shaped-weapons-patch]] is now installed separately
- Removed an overwritten mesh from [[wall-mounted-dead-animals-fixes]]
- Removed assets from [[skyland-bits-and-bobs-clutter-overhaul]]
- Removed assets from [[ruins-clutter-improved]]
- Removed assets from [[misc-retexture-project]]
- Removed assets from [[misc-effects-enb-light]]
- Removed assets from [[fyx-3d-shack-kit-walls]]
- Removed assets from [[skyrim-3d-misc-dining-set]]
- Removed assets from [[stalhrim-refrozen]]
- Removed assets from [[open-face-guard-helmets]]
- Regenerated [[facegen-helper]] plugin
- Regenerated facegen (and remembered to compress textures / generate mipmaps)

## Release 1.4.0

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