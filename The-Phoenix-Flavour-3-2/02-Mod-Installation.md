![Logo](../Media/tpf_logo.png)

**TABLE OF CONTENTS**
- [01. Essential Mods](#01-essential-mods)
  - [1.1 Address Library for SKSE Plugins](#11-address-library-for-skse-plugins)
  - [1.2 SSE Engine Fixes](#12-sse-engine-fixes)
  - [1.3 .NET Script Framework (NSF)](#13-net-script-framework-nsf)
  - [1.4 SSE Display Tweaks](#14-sse-display-tweaks)
  - [1.5 Autorun Console Commands (ACC)](#15-autorun-console-commands-acc)
  - [1.6 Performance Optimized Textures for SSE](#16-performance-optimized-textures-for-sse)
  - [1.7 Unofficial High Definition Audio Project (optional)](#17-unofficial-high-definition-audio-project-optional)
  - [1.8 Unofficial Skyrim Special Edition Patch (USSEP)](#18-unofficial-skyrim-special-edition-patch-ussep)
  - [1.9 Alternate Start - Live Another Life (AS LAL)](#19-alternate-start---live-another-life-as-lal)
  - [1.10 Skyrim Particle Patch](#110-skyrim-particle-patch)
  - [1.11 Static Mesh Improvement Mod (SMIM)](#111-static-mesh-improvement-mod-smim)
- [02. Fixes](#02-fixes)
  - [2.1 Weapons, Armor, Clothing and Clutter Fixes (WACCF)](#21-weapons-armor-clothing-and-clutter-fixes-waccf)
  - [2.2 Wiseman303's Flora Fixes - Revamped](#22-wiseman303s-flora-fixes---revamped)
  - [2.3 Weapon Speed Effects Fix](#23-weapon-speed-effects-fix)
  - [2.4 Quests Are In Skyrim](#24-quests-are-in-skyrim)
  - [2.5 Tavern AI Fix (optional)](#25-tavern-ai-fix-optional)
  - [2.6 Skyrim Landscape and Water Fixes](#26-skyrim-landscape-and-water-fixes)
  - [2.7 Landscape Fixes for Grass Mods](#27-landscape-fixes-for-grass-mods)
  - [2.8 No Animals Report Crimes (NARC)](#28-no-animals-report-crimes-narc)
  - [2.9 Raven Rock - Fix Exit on Horseback (optional)](#29-raven-rock---fix-exit-on-horseback-optional)
  - [2.10 Dawnguard Don't Hunt Cured Vampires (optional)](#210-dawnguard-dont-hunt-cured-vampires-optional)
  - [2.11 Charge Dialogue Fix (optional)](#211-charge-dialogue-fix-optional)
  - [2.12 Rude Imperial Soldiers Escort Prisoner Fix (optional)](#212-rude-imperial-soldiers-escort-prisoner-fix-optional)
  - [2.13 Mannequins Stay Put (optional)](#213-mannequins-stay-put-optional)
  - [2.14 Eye Normal Map Fix (optional)](#214-eye-normal-map-fix-optional)
  - [2.15 Skyrim Ultimate Eyemeshes Ruhmastered](#215-skyrim-ultimate-eyemeshes-ruhmastered)
  - [2.16 Eyes AO Clipping Fix (optional)](#216-eyes-ao-clipping-fix-optional)
  - [2.17 ENB Brow Fix (optional)](#217-enb-brow-fix-optional)
  - [2.18 Double Sided Vertex Human Mouth Fix (optional)](#218-double-sided-vertex-human-mouth-fix-optional)
  - [2.19 WoodElf - MaleHair - Fix (optional)](#219-woodelf---malehair---fix-optional)
  - [2.20 Sound Hammering Sounds (optional)](#220-sound-hammering-sounds-optional)
  - [2.21 Dragon Stalking Fix (optional)](#221-dragon-stalking-fix-optional)
  - [2.22 Serana's Hood Fix (optional)](#222-seranas-hood-fix-optional)
  - [2.23 Bug Fixes](#223-bug-fixes)
  - [2.24 Actor Limit Fix](#224-actor-limit-fix)
- [03. Tweaks](#03-tweaks)
  - [3.1 Run For Your Lives](#31-run-for-your-lives)
  - [3.2 Dwemer Gates Don't Reset (optional)](#32-dwemer-gates-dont-reset-optional)
  - [3.3 Calcelmo Has Standards (optional)](#33-calcelmo-has-standards-optional)
  - [3.4 Move It Dammit (optional)](#34-move-it-dammit-optional)
  - [3.5 NPCs Run and Walk at Your Pace (optional)](#35-npcs-run-and-walk-at-your-pace-optional)
  - [3.6 No More Standing Too Close (optional)](#36-no-more-standing-too-close-optional)
  - [3.7 Realistic Conversations (optional)](#37-realistic-conversations-optional)
  - [3.8 No NPC Greetings (optional)](#38-no-npc-greetings-optional)
  - [3.9 Don't Talk With Your Mouth Full (optional)](#39-dont-talk-with-your-mouth-full-optional)
  - [3.10 Random Encounter Tweaks (optional)](#310-random-encounter-tweaks-optional)
  - [3.11 Morrowloot Miscellania - Better Ancient Knowledge (optional)](#311-morrowloot-miscellania---better-ancient-knowledge-optional)
  - [3.12 Merchants and Citizens Have No Lockpicks (optional)](#312-merchants-and-citizens-have-no-lockpicks-optional)
  - [3.13 No Spinning Death Animation (optional)](#313-no-spinning-death-animation-optional)
  - [3.14 Improved Weapon Impact Effects (optional)](#314-improved-weapon-impact-effects-optional)
  - [3.15 Simply Smaller Wolves (optional)](#315-simply-smaller-wolves-optional)
  - [3.16 Quiet Dog (optional)](#316-quiet-dog-optional)
  - [3.17 Skeletons Don't Breathe (optional)](#317-skeletons-dont-breathe-optional)
  - [3.18 Remove Sneak Attack Sound (optional)](#318-remove-sneak-attack-sound-optional)
  - [3.19 Bard Instrumentals Mostly - Sing Rarely (optional)](#319-bard-instrumentals-mostly---sing-rarely-optional)
  - [3.20 No Crime Teleport (optional)](#320-no-crime-teleport-optional)
  - [3.21 Better Dialogue Controls (optional)](#321-better-dialogue-controls-optional)
  - [3.22 Better MessageBox Controls (optional)](#322-better-messagebox-controls-optional)
  - [3.23 Better Stealing (optional)](#323-better-stealing-optional)
  - [3.24 Uninterrupted Invisibility (optional)](#324-uninterrupted-invisibility-optional)
  - [3.25 Uninterrupted Ethereal Form (optional)](#325-uninterrupted-ethereal-form-optional)
- [04. Interface](#04-interface)
  - [4.1 SkyUI](#41-skyui)
  - [4.2 Fix Note Icon for SkyUI (optional)](#42-fix-note-icon-for-skyui-optional)
  - [4.3 Remove Quicksave Button from SkyUI Systems Menu (optional)](#43-remove-quicksave-button-from-skyui-systems-menu-optional)
  - [4.4 Wider MCM Menu for SkyUI (optional)](#44-wider-mcm-menu-for-skyui-optional)
  - [4.5 Favorite Things - Extended Favorites Menu for SkyUI (optional)](#45-favorite-things---extended-favorites-menu-for-skyui-optional)
  - [4.6 Stay At The System Page (optional)](#46-stay-at-the-system-page-optional)
  - [4.7 RaceMenu](#47-racemenu)
  - [4.8 Immersive HUD - iHUD](#48-immersive-hud---ihud)
  - [4.9 SkyHUD](#49-skyhud)
  - [4.10 Undiscovered Means Unknown (optional)](#410-undiscovered-means-unknown-optional)
  - [4.11 moreHUD (optional)](#411-morehud-optional)
  - [4.12 moreHUD - Inventory Edition (optional)](#412-morehud---inventory-edition-optional)
  - [4.13 A Matter of Time - A Clock HUD Widget (optional)](#413-a-matter-of-time---a-clock-hud-widget-optional)
  - [4.14 A Matter of Time - Phoenix Preset (optional)](#414-a-matter-of-time---phoenix-preset-optional)
  - [4.15 Shouts in the Dragon Tongue (SIDT) (optional)](#415-shouts-in-the-dragon-tongue-sidt-optional)
  - [4.16 Extended UI (optional)](#416-extended-ui-optional)
  - [4.17 Skyrim SE Skill Interface Retexture (SSIRT) (optional)](#417-skyrim-se-skill-interface-retexture-ssirt-optional)
  - [4.18 No More Laser-Printed Book (optional)](#418-no-more-laser-printed-book-optional)
  - [4.19 Immersive Bookreading and Lockpicking (optional)](#419-immersive-bookreading-and-lockpicking-optional)
  - [4.20 JS Lockpicking UI (optional)](#420-js-lockpicking-ui-optional)
  - [4.21 A Quality World Map](#421-a-quality-world-map)
  - [4.22 Dynamic Snow for Map (optional)](#422-dynamic-snow-for-map-optional)
  - [4.23 Dawnguard Map Markers (optional)](#423-dawnguard-map-markers-optional)
  - [4.24 Smaller Vanilla Cursor (optional)](#424-smaller-vanilla-cursor-optional)
  - [4.25 ReCleaned Menu (optional)](#425-recleaned-menu-optional)
  - [4.26 Loading Screen Smoke Removed (optional)](#426-loading-screen-smoke-removed-optional)
  - [4.27 KenMOD - Time on Loading Screen (optional)](#427-kenmod---time-on-loading-screen-optional)
- [05. Main Visual Mods](#05-main-visual-mods)
  - [5.1 Skyrim Realistic Overhaul (SRO)](#51-skyrim-realistic-overhaul-sro)
  - [5.2 DynDOLOD Resources](#52-dyndolod-resources)
  - [5.3 HD LODs Textures](#53-hd-lods-textures)
  - [5.4 Noble Skyrim Mod HD-2K (NSM)](#54-noble-skyrim-mod-hd-2k-nsm)
  - [5.5 Ruins Clutter Improved (RCI)](#55-ruins-clutter-improved-rci)
  - [5.6 Ruins Clutter Improved - Fixes](#56-ruins-clutter-improved---fixes)
  - [5.7 Revamped Assets Skyrim](#57-revamped-assets-skyrim)
  - [5.8 High Poly Project (optional)](#58-high-poly-project-optional)
  - [5.9 aMidianBorn Book of Silence - Dragonborn DLC (optional)](#59-amidianborn-book-of-silence---dragonborn-dlc-optional)
  - [5.10 Caliente's Beautiful Bodies Enhancer (CBBE)](#510-calientes-beautiful-bodies-enhancer-cbbe)
- [06. Weather](#06-weather)
  - [6.1 Obsidian Weathers and Seasons](#61-obsidian-weathers-and-seasons)
  - [6.2 Obsidian Weathers and Seasons MCM Patch (optional)](#62-obsidian-weathers-and-seasons-mcm-patch-optional)
  - [6.3 Smooth Sky Mesh (optional)](#63-smooth-sky-mesh-optional)
  - [6.4 ETHEREAL CLOUDS (optional)](#64-ethereal-clouds-optional)
  - [6.5 Skyrim Textures Redone - Enhanced Night Sky (optional)](#65-skyrim-textures-redone---enhanced-night-sky-optional)
  - [6.6 Night Skies - Stars and Galaxies (optional)](#66-night-skies---stars-and-galaxies-optional)
  - [6.7 Skygazer Moons - Masser and Secunda (optional)](#67-skygazer-moons---masser-and-secunda-optional)
  - [6.8 Storm Lightning (optional)](#68-storm-lightning-optional)
  - [6.9 Yee - A New Snowflake Mod (optional)](#69-yee---a-new-snowflake-mod-optional)
  - [6.10 Wonders of Weather (optional)](#610-wonders-of-weather-optional)
  - [6.11 Wonders of Weather - Less Opaque Rain Splashes for ENB (optional)](#611-wonders-of-weather---less-opaque-rain-splashes-for-enb-optional)
- [07. Lighting](#07-lighting)
  - [7.1 Relighting Skyrim](#71-relighting-skyrim)
  - [7.2 Relighting Skyrim - No Player Homes](#72-relighting-skyrim---no-player-homes)
  - [7.3 Luminosity Lighting Overhaul](#73-luminosity-lighting-overhaul)
  - [7.4 Luminosity - A Quality World Map Patch](#74-luminosity---a-quality-world-map-patch)
  - [7.5 Interior Floating Fog Remover (optional)](#75-interior-floating-fog-remover-optional)
  - [7.6 Smoking Torches and Candles (STAC)](#76-smoking-torches-and-candles-stac)
  - [7.7 Embers HD](#77-embers-hd)
  - [7.8 Inferno - Fire Effects Redux](#78-inferno---fire-effects-redux)
  - [7.9 KD - Realistic Fireplaces](#79-kd---realistic-fireplaces)
  - [7.10 Charred Logs for KD - Realistic Fireplaces (optional)](#710-charred-logs-for-kd---realistic-fireplaces-optional)
- [08. Visual FX](#08-visual-fx)
  - [8.1 Frozen Electrocuted Combustion (FEC) (optional)](#81-frozen-electrocuted-combustion-fec-optional)
  - [8.2 Frozen Electrocuted Combustion - Extra Crispy Retexture (optional)](#82-frozen-electrocuted-combustion---extra-crispy-retexture-optional)
  - [8.3 Enhanced Blood Textures](#83-enhanced-blood-textures)
  - [8.4 GORECAP (optional)](#84-gorecap-optional)
  - [8.5 Deadly Spell Impacts](#85-deadly-spell-impacts)
  - [8.6 Arctic - Frost Effects Redux (optional)](#86-arctic---frost-effects-redux-optional)
  - [8.7 Refracting Ice Form Debris (optional)](#87-refracting-ice-form-debris-optional)
  - [8.8 Voltage (optional)](#88-voltage-optional)
  - [8.9 ElSopa HD - Dirt Blast (optional)](#89-elsopa-hd---dirt-blast-optional)
  - [8.10 Reduced Glow FX (optional)](#810-reduced-glow-fx-optional)
  - [8.11 Fire Halo Remover (optional)](#811-fire-halo-remover-optional)
  - [8.12 Subtle Wind FX (optional)](#812-subtle-wind-fx-optional)
  - [8.13 Glow Be Gone - Updated (optional)](#813-glow-be-gone---updated-optional)
- [09. Landscape](#09-landscape)
  - [9.1 Majestic Mountains](#91-majestic-mountains)
  - [9.2 Landscapes - Cathedral Concept](#92-landscapes---cathedral-concept)
  - [9.3 The Elder Scrolls - Veydosebrom (optional)](#93-the-elder-scrolls---veydosebrom-optional)
  - [9.4 Cathedral Landscapes - Veydosebrom Swamp Grass Addon (optional)](#94-cathedral-landscapes---veydosebrom-swamp-grass-addon-optional)
  - [9.5 Pfuscher's Rapid Rocks](#95-pfuschers-rapid-rocks)
  - [9.6 Majestic Mountains - Northside (optional)](#96-majestic-mountains---northside-optional)
  - [9.7 Realistic Water Two (RW2)](#97-realistic-water-two-rw2)
  - [9.8 Skyrim SE Improved Puddles (optional)](#98-skyrim-se-improved-puddles-optional)
  - [9.9 Better Dynamic Snow](#99-better-dynamic-snow)
  - [9.10 Better Dynamic Majestic Mountains](#910-better-dynamic-majestic-mountains)
  - [9.11 Skyrim 3D Icefloes (optional)](#911-skyrim-3d-icefloes-optional)
  - [9.12 Better Dynamic Ash](#912-better-dynamic-ash)
  - [9.13 Enhanced Landscapes - Dead Marsh](#913-enhanced-landscapes---dead-marsh)
  - [9.14 Enhanced Landscapes - Dead Marsh Fixes](#914-enhanced-landscapes---dead-marsh-fixes)
  - [9.15 Rorikstead Basalt Cliffs (optional)](#915-rorikstead-basalt-cliffs-optional)
  - [9.16 Rorikstead Basalt Cliffs Patches (optional)](#916-rorikstead-basalt-cliffs-patches-optional)
  - [9.17 Ashbound - Solstheim Enhanced](#917-ashbound---solstheim-enhanced)
  - [9.18 Point The Way](#918-point-the-way)
  - [9.19 Lanterns of Skyrim II](#919-lanterns-of-skyrim-ii)
  - [9.20 Manor Roads (optional)](#920-manor-roads-optional)
  - [9.21 Immersive Dawnguard Dayspring Pass (IDDP)](#921-immersive-dawnguard-dayspring-pass-iddp)
- [10. Flora](#10-flora)
  - [10.1 Enhanced Vanilla Trees (EVT)](#101-enhanced-vanilla-trees-evt)
  - [10.2 Enhanced Vanilla Trees – Vurts Light Snow Trees](#102-enhanced-vanilla-trees--vurts-light-snow-trees)
  - [10.3 Tree Bark in High Definition (optional)](#103-tree-bark-in-high-definition-optional)
  - [10.4 Enhanced Landscapes – Oaks Standalone](#104-enhanced-landscapes--oaks-standalone)
  - [10.5 Bent Pines II (optional)](#105-bent-pines-ii-optional)
  - [10.6 Sacred Trees (optional)](#106-sacred-trees-optional)
  - [10.7 Rudy HQ – Falling Leaves and Needles (optional)](#107-rudy-hq--falling-leaves-and-needles-optional)
  - [10.8 Cathedral Plants (optional)](#108-cathedral-plants-optional)
  - [10.9 Realistic HD Mushrooms Remastered (optional)](#109-realistic-hd-mushrooms-remastered-optional)
  - [10.10 Less Ugly Tundra Grass (optional)](#1010-less-ugly-tundra-grass-optional)
  - [10.11 Immersive Fallen Trees (optional)](#1011-immersive-fallen-trees-optional)
  - [10.12 Immersive Fallen Trees Patch (optional)](#1012-immersive-fallen-trees-patch-optional)
- [11. Architecture](#11-architecture)
  - [11.1 MD's Farmhouses (optional)](#111-mds-farmhouses-optional)
  - [11.2 The Streets of Whiterun HD (optional)](#112-the-streets-of-whiterun-hd-optional)
  - [11.3 Riften in High Definition (optional)](#113-riften-in-high-definition-optional)
  - [11.4 Marvelous Windhelm Gate (optional)](#114-marvelous-windhelm-gate-optional)
  - [11.5 Windhelm Enhanced – HD Metalwork (optional)](#115-windhelm-enhanced--hd-metalwork-optional)
  - [11.6 RUSTIC MONUMENTS AND TOMBSTONES (optional)](#116-rustic-monuments-and-tombstones-optional)
  - [11.7 HQ Solitude (optional)](#117-hq-solitude-optional)
  - [11.8 Pfuscher’s Manhole Texture (optional)](#118-pfuschers-manhole-texture-optional)
  - [11.9 Skyland – Winterhold (optional)](#119-skyland--winterhold-optional)
  - [11.10 Skyrim 3D Misc – Winterhold Gate (optional)](#1110-skyrim-3d-misc--winterhold-gate-optional)
  - [11.11 Skyrim Textures Redone – High Hrothgar (optional)](#1111-skyrim-textures-redone--high-hrothgar-optional)
  - [11.12 Skyrim 3D High Hrothgar Steps (optional)](#1112-skyrim-3d-high-hrothgar-steps-optional)
  - [11.13 Pilgrim’s Delight – High Hrothgar Shrine Retexture](#1113-pilgrims-delight--high-hrothgar-shrine-retexture)
  - [11.14 Skyrim Textures Redone – Skyhaven (optional)](#1114-skyrim-textures-redone--skyhaven-optional)
  - [11.15 Spice of Life – Orc Strongholds (optional)](#1115-spice-of-life--orc-strongholds-optional)
  - [11.16 Sovngarde HD (optional)](#1116-sovngarde-hd-optional)
  - [11.17 Dawnguard Fortress Improved (optional)](#1117-dawnguard-fortress-improved-optional)
  - [11.18 Castle Volkihar Reborn (optional)](#1118-castle-volkihar-reborn-optional)
  - [11.19 Soul Cairn HD (optional)](#1119-soul-cairn-hd-optional)
  - [11.20 Arri’s Snow Elf Ruins Retexture (optional)](#1120-arris-snow-elf-ruins-retexture-optional)
- [12. Misc Structures](#12-misc-structures)
  - [12.1 Fences of Skyrim (optional)](#121-fences-of-skyrim-optional)
  - [12.2 Skyrim Landscape Overhaul – Stone Walls (optional)](#122-skyrim-landscape-overhaul--stone-walls-optional)
  - [12.3 Skyrim 3D Signs (optional)](#123-skyrim-3d-signs-optional)
  - [12.4 SkyFix – HD Blacksmith Signs (optional)](#124-skyfix--hd-blacksmith-signs-optional)
  - [12.5 RUSTIC EAST EMPIRE COMPANY SIGNAGE (optional)](#125-rustic-east-empire-company-signage-optional)
  - [12.6 Ennead – Shadowmarks (optional)](#126-ennead--shadowmarks-optional)
  - [12.7 ElSopa HD – Glorious Dummies (optional)](#127-elsopa-hd--glorious-dummies-optional)
  - [12.8 Stunning Statues of Skyrim (optional)](#128-stunning-statues-of-skyrim-optional)
  - [12.9 LeanWolf’s Better-Shaped Talos Statue (optional)](#129-leanwolfs-better-shaped-talos-statue-optional)
  - [12.10 Astral Aspects – Standing Stones (optional)](#1210-astral-aspects--standing-stones-optional)
- [13. Vanilla Locations](#13-vanilla-locations)
  - [13.1 JK’s Cities – Lite](#131-jks-cities--lite)
  - [13.2 Arthmoor’s Dawnstar](#132-arthmoors-dawnstar)
  - [13.3 Arthmoor’s Falkreath](#133-arthmoors-falkreath)
  - [13.4 Arthmoor’s Dragon Bridge](#134-arthmoors-dragon-bridge)
  - [13.5 Arthmoor’s Ivarstead](#135-arthmoors-ivarstead)
  - [13.6 Arthmoor’s Rorikstead](#136-arthmoors-rorikstead)
  - [13.7 Arthmoor’s Kynesgrove](#137-arthmoors-kynesgrove)
  - [13.8 Arthmoor’s Karthwasten](#138-arthmoors-karthwasten)
  - [13.9 Arthmoor’s Darkwater Crossing](#139-arthmoors-darkwater-crossing)
  - [13.10 Arthmoor’s Shor’s Stone](#1310-arthmoors-shors-stone)
  - [13.11 Arthmoor’s Soljund’s Sinkhole](#1311-arthmoors-soljunds-sinkhole)
  - [13.12 Arthmoor’s Whistling Mine](#1312-arthmoors-whistling-mine)
  - [13.13 Obscure’s College of Winterhold](#1313-obscures-college-of-winterhold)
- [14. Interiors](#14-interiors)
  - [14.1 RUSTIC WINDOWS](#141-rustic-windows)
  - [14.2 Hall of the Dead - Stained Glass Windows (optional)](#142-hall-of-the-dead---stained-glass-windows-optional)
  - [14.3 Ennead – Banners (optional)](#143-ennead--banners-optional)
  - [14.4 PELTAPALOOZA (optional)](#144-peltapalooza-optional)
  - [14.5 RUGNAROK (optional)](#145-rugnarok-optional)
  - [14.6 Medieval Candlehorns and Sconces (optional)](#146-medieval-candlehorns-and-sconces-optional)
  - [14.7 Skyrim 3D Cooking (optional)](#147-skyrim-3d-cooking-optional)
  - [14.8 RUSTIC ALCHEMY AND ENCHANTING TABLES (optional)](#148-rustic-alchemy-and-enchanting-tables-optional)
  - [14.9 JS Shrines of the Divines (optional)](#149-js-shrines-of-the-divines-optional)
- [15. Dungeons](#15-dungeons)
  - [15.1 Underground – A Dungeon Texture Overhaul](#151-underground--a-dungeon-texture-overhaul)
  - [15.2 Rudy HQ – Nordic Ruins](#152-rudy-hq--nordic-ruins)
  - [15.3 Ice Cave Parallax Improved (optional)](#153-ice-cave-parallax-improved-optional)
  - [15.4 Gecko’s Dwarven Ruins Textures (optional)](#154-geckos-dwarven-ruins-textures-optional)
  - [15.7 RUSTIC WORD WALLS (optional)](#157-rustic-word-walls-optional)
  - [15.9 4K Nordic Murals (optional)](#159-4k-nordic-murals-optional)
  - [15.10 CC’s Enhanced Ore Veins (optional)](#1510-ccs-enhanced-ore-veins-optional)
  - [15.11 CC's Enhanced Ore Veins - Fixed Iron Ore Cubemap (optional)](#1511-ccs-enhanced-ore-veins---fixed-iron-ore-cubemap-optional)
  - [15.12 Metallurgy – Ingots and Ore HD (optional)](#1512-metallurgy--ingots-and-ore-hd-optional)
  - [15.13 Ancient Pottery (optional)](#1513-ancient-pottery-optional)
  - [15.14 ElSopa HD – Realistic Dark Elf Urns (optional)](#1514-elsopa-hd--realistic-dark-elf-urns-optional)
  - [15.15 Ancient Dwemer Metal (optional)](#1515-ancient-dwemer-metal-optional)
  - [15.16 HD Lava for Dawnguard (optional)](#1516-hd-lava-for-dawnguard-optional)
- [16. Clutter](#16-clutter)
  - [16.1 Forgotten Retex Project](#161-forgotten-retex-project)
  - [16.2 Aetherial Crown by Saerileth – Plugin Replacer](#162-aetherial-crown-by-saerileth--plugin-replacer)
  - [16.3 Skyrim 3D Misc (optional)](#163-skyrim-3d-misc-optional)
  - [16.4 RUSTIC CLUTTER COLLECTION (optional)](#164-rustic-clutter-collection-optional)
  - [16.5 Rudy HQ – Miscellaneous (optional)](#165-rudy-hq--miscellaneous-optional)
  - [16.6 Frankly HD Dragon Bones (optional)](#166-frankly-hd-dragon-bones-optional)
  - [16.7 Medieval Silverworks (optional)](#167-medieval-silverworks-optional)
  - [16.8 Book Covers Skyrim (BCS)](#168-book-covers-skyrim-bcs)
  - [16.9 Realistic Paper (optional)](#169-realistic-paper-optional)
  - [16.10 MAPS (optional)](#1610-maps-optional)
  - [16.11 Business Ledger HD Retexture (optional)](#1611-business-ledger-hd-retexture-optional)
  - [16.12 JS Dragon Claws (optional)](#1612-js-dragon-claws-optional)
  - [16.13 JS Dragon Claws – Patches (optional)](#1613-js-dragon-claws--patches-optional)
  - [16.14 RUSTIC SOULGEMS](#1614-rustic-soulgems)
  - [16.15 RUSTIC AZURAS STAR (optional)](#1615-rustic-azuras-star-optional)
  - [16.16 ElSopa HD – Meridia’s Beacon (optional)](#1616-elsopa-hd--meridias-beacon-optional)
  - [16.17 RUSTIC ELDERSCROLL (optional)](#1617-rustic-elderscroll-optional)
  - [16.18 RUSTIC ANIMATED POTIONS AND POISONS (optional)](#1618-rustic-animated-potions-and-poisons-optional)
  - [16.19 Rally's Werewolf Totems (optional)](#1619-rallys-werewolf-totems-optional)
  - [16.20 BLOODSTONE CHALICE REBORN (optional)](#1620-bloodstone-chalice-reborn-optional)
- [17. Food & Ingredients](#17-food--ingredients)
  - [17.1 High Quality Food and Ingredients SE (optional)](#171-high-quality-food-and-ingredients-se-optional)
  - [17.2 Medieval Spirits (optional)](#172-medieval-spirits-optional)
  - [17.3 Boiled Creme Treat Sweet Roll and Pie (optional)](#173-boiled-creme-treat-sweet-roll-and-pie-optional)
  - [17.4 Honey Pot (optional)](#174-honey-pot-optional)
  - [17.5 HD Sabre Cat Tooth (optional)](#175-hd-sabre-cat-tooth-optional)
  - [17.6 Falmer Ear and Hagraven Claw (optional)](#176-falmer-ear-and-hagraven-claw-optional)
  - [17.7 ElSopa HD – Briar Heart (optional)](#177-elsopa-hd--briar-heart-optional)
- [18. Clothes & Jewellery](#18-clothes--jewellery)
  - [18.1 RUSTIC CLOTHING](#181-rustic-clothing)
  - [18.2 Prince and the Pauper](#182-prince-and-the-pauper)
  - [18.3 Gemling Queen Jewelry (optional)](#183-gemling-queen-jewelry-optional)
  - [18.4 JS Circlet Replacer (optional)](#184-js-circlet-replacer-optional)
  - [18.5 The Divine Amulets Retexture (optional)](#185-the-divine-amulets-retexture-optional)
  - [18.6 Better Looking Amulets (optional)](#186-better-looking-amulets-optional)
  - [18.7 ElSopa HD – Akatosh Amulet (optional)](#187-elsopa-hd--akatosh-amulet-optional)
  - [18.8 ElSopa HD – Bonehawk Amulet (optional)](#188-elsopa-hd--bonehawk-amulet-optional)
  - [18.9 JS Barenziah (optional)](#189-js-barenziah-optional)
- [19. Weapons & Armour](#19-weapons--armour)
  - [19.1 RUSTIC ARMOR AND WEAPONS (RAW) (optional)](#191-rustic-armor-and-weapons-raw-optional)
  - [19.2 Practical Female Armors (optional)](#192-practical-female-armors-optional)
  - [19.3 Warmth – Light Armor Replacer (optional)](#193-warmth--light-armor-replacer-optional)
  - [19.4 aMidianBorn of Silence – Armors](#194-amidianborn-of-silence--armors)
  - [19.5 aMidianBorn Blade Armor SSE Patch](#195-amidianborn-blade-armor-sse-patch)
  - [19.6 aMidianBorn Book of Silence – Weapons](#196-amidianborn-book-of-silence--weapons)
  - [19.7 Frankly HD Silver Sword](#197-frankly-hd-silver-sword)
  - [19.8 LeanWolf’s Better-Shaped Weapons](#198-leanwolfs-better-shaped-weapons)
  - [19.9 Open Face Guard Helmets (optional)](#199-open-face-guard-helmets-optional)
  - [19.10 Open Face Guard Helmets – Plugin Replacer (optional)](#1910-open-face-guard-helmets--plugin-replacer-optional)
  - [19.11 Frankly HD Stormcloaks and City Guards (optional)](#1911-frankly-hd-stormcloaks-and-city-guards-optional)
  - [19.12 aMidianBorn Stormcloak Officer Armour (optional)](#1912-amidianborn-stormcloak-officer-armour-optional)
  - [19.13 Frankly HD Imperial Armor and Weapons](#1913-frankly-hd-imperial-armor-and-weapons)
  - [19.14 Frankly HD Dawnguard Armor and Weapons (optional)](#1914-frankly-hd-dawnguard-armor-and-weapons-optional)
  - [19.15 Iron Things (optional)](#1915-iron-things-optional)
  - [19.16 Elven Weapons for Silence (optional)](#1916-elven-weapons-for-silence-optional)
  - [19.17 CC’s HD Dwemer Weapons and Armor (optional)](#1917-ccs-hd-dwemer-weapons-and-armor-optional)
  - [19.18 Frankly HD Thieves Guild Armor (optional)](#1918-frankly-hd-thieves-guild-armor-optional)
  - [19.19 Frankly HD Shrouded Armor (optional)](#1919-frankly-hd-shrouded-armor-optional)
  - [19.20 Falmer Weapons for aMidianBorn Book of Silence (optional)](#1920-falmer-weapons-for-amidianborn-book-of-silence-optional)
  - [19.21 Outlandish Stalhrim (optional)](#1921-outlandish-stalhrim-optional)
  - [19.22 Outlandish Chitin Armour (optional)](#1922-outlandish-chitin-armour-optional)
  - [19.23 Ebony Weapons 2017 Retexture (optional)](#1923-ebony-weapons-2017-retexture-optional)
  - [19.24 Frankly HD Dragonbone and Dragonscale (optional)](#1924-frankly-hd-dragonbone-and-dragonscale-optional)
  - [19.25 Sunhallowed and Bloodcursed Arrows – HD Retexture](#1925-sunhallowed-and-bloodcursed-arrows--hd-retexture)
  - [19.26 Dragon Priest Weapons Improved (optional)](#1926-dragon-priest-weapons-improved-optional)

# 01. Essential Mods

## 1.1 [Address Library for SKSE Plugins](https://www.nexusmods.com/skyrimspecialedition/mods/32444?tab=files)

### Download Instructions

- **Main File** - All in one

## 1.2 [SSE Engine Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/17230?tab=files)

### Download Instructions

- **Main File** - (Part 1) Engine Fixes

### Preloader

- Download the following file manually:
  * **(Part 2) Engine Fixes - skse64 Preloader and TBB Lib**
- Open the downloaded archive.
- Extract the following files into your **root** folder:
  * **d3dx9_42.dll**
  * **tbb.dll**
  * **tbbmalloc.dll**
- Click **Yes** when asked to overwrite.

### Engine Fixes INI

* Double-click **SSE Engine Fixes** in your mod order.
* Switch to the **INI-Files** tab and select the **EngineFixes.ini**.
* Edit the following line:
  * `SleepWaitTime = true`
* Close the window and click **Yes** when asked to save your change.

## 1.3 [.NET Script Framework (NSF)](https://www.nexusmods.com/skyrimspecialedition/mods/21294?tab=files)

### Download Instructions

- **Main File** - NetScriptFramework SkyrimSE v13

## 1.4 [SSE Display Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/34705?tab=files)

### Download Instructions

- **Main File** - SSE Display Tweaks

## 1.5 [Autorun Console Commands (ACC)](https://www.nexusmods.com/skyrimspecialedition/mods/24919?tab=files)

### Download Instructions

- **Main File** - ACC - Autorun Console Commands

## 1.6 [Performance Optimized Textures for SSE](https://www.nexusmods.com/skyrimspecialedition/mods/21166?tab=files)

### Download Instructions

- **Main File** - performance textures max res 1024 min res 512 v8

## 1.7 [Unofficial High Definition Audio Project](https://www.nexusmods.com/skyrimspecialedition/mods/18115?tab=files) (optional)

### Download Instructions

- **Main File** - Music - HQ
- **Main File** - Voices EN - Part 1
- **Main File** - Voices EN - Part 2

## 1.8 [Unofficial Skyrim Special Edition Patch (USSEP)](https://www.nexusmods.com/skyrimspecialedition/mods/266?tab=files)

### Download Instructions

- **Main File** - Unofficial Skyrim Special Edition Patch

### Additional Instructions

- Delete the following file(s) and/or folder(s):
  * `Unofficial Skyrim Special Edition Patch.modgroups`

## 1.9 [Alternate Start - Live Another Life (AS LAL)](https://www.nexusmods.com/skyrimspecialedition/mods/272?tab=files)

### Download Instructions

- **Main File** - Alternate Start - Live Another Life

## 1.10 [Skyrim Particle Patch](http://enbseries.enbdev.com/forum/viewtopic.php?t=1499)

### Installation Instructions

- Find the **SPECIAL EDITION** section in the forum post linked above and click the **GOOGLE DRIVE** link (see picture).
- Download the archive from Google Drive and move it manually to `Your Modding Folder\ARCHIVE\MO2 Downloads`.
- Go to the **Downloads** tab and double-click the mod to install it as usual.
- I recommend renaming it simply to **Skyrim Particle Patch** after the installation.

![Skyrim Particle Patch download link](Pictures/mod_installation/skyrim_particle_patch_download.png)

### Additional Instructions

- Delete the following file(s) and/or folder(s):
  * `Particle Patch for ENB SSE.esp`

> The plugin is not needed. Its functionality was replaced by ENB Helper.

## 1.11 [Static Mesh Improvement Mod (SMIM)](https://www.nexusmods.com/skyrimspecialedition/mods/659/?tab=files)

### Download Instructions

- **Main File** - SMIM SE 2-08

### FOMOD Instructions

- **Main Installer Choice:** Skyrim 2016 Special Edition: Everything

### Additional Instructions

- Delete the following file(s) and/or folder(s):
  * `meshes\architecture\farmhouse\walkway\walkwaycwall01.nif`
  * `meshes\architecture\solitude\doors\sgatedoor.nif`

> The first mesh will be replaced either by the fixed version contained in Skyrim Landscape and Water Fixes or by Real Walls 3D.  Deleting the second mesh will allow you to use a different retexture for the gate.

![separator](../Media/separator.png)

# 02. Fixes

## 2.1 [Weapons, Armor, Clothing and Clutter Fixes (WACCF)](https://www.nexusmods.com/skyrimspecialedition/mods/18994?tab=files)

### Download Instructions

- **Main File** - Weapons Armor Clothing and Clutter Fixes

### Additional Instructions

- Delete the following file(s) and/or folder(s):
  * `WACCF_BashedPatchLvlListFix.esp`
  * `Weapons Armor Clothing & Clutter Fixes.modgroups`

## 2.2 [Wiseman303's Flora Fixes - Revamped](https://www.nexusmods.com/skyrimspecialedition/mods/28197?tab=files)

### Download Instructions

- **Main File** - WM’s Flora Fixes - Revamped
- **Optional File** - WM’s Flora Fixes - SMIM Patch

## 2.3 [Weapon Speed Effects Fix](https://www.nexusmods.com/skyrimspecialedition/mods/27677?tab=files)

### Download Instructions

- **Main File** - Weapon Speed Effects Fix

## 2.4 [Quests Are In Skyrim](https://www.nexusmods.com/skyrimspecialedition/mods/18416?tab=files)

### Download Instructions

- **Main File** - QuestsAreInSkyrim_USSEP_1_2_reupload

## 2.5 [Tavern AI Fix](https://www.nexusmods.com/skyrimspecialedition/mods/23107?tab=files) (optional)

### Download Instructions

- **Main File** - TavernAIFix

---

### Additional Instructions

The mod comes with two optional console commands to customise it.  Fortunately we have Autorun Console Commands to easily set and forget them. This is optional and you can add one or both of the commands (personally I only use the second one to finally stop innkeepers from showing me to my room).

* Double-click **Autorun Console Commands** in your mod order.
* In the **Textfiles** tab, select **Autorun.txt** and add one or both of the following lines:
  * `set TAIF_ServePlayerEveryTime to 1`
  * `set TAIF_ShowRoomNeverShow to 1`
* Close the window and click **Yes** when asked to save.

The commands will now be executed automatically when you start a new game or load your save.

## 2.6 [Skyrim Landscape and Water Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/26138?tab=files)

### Download Instructions

- **Main File** - Skyrim Landscape and Water Fixes - FOMOD Installer

### FOMOD Instructions

- **Main Plugin:** ESM
- **Patches:** *select nothing*
- **Walkway Wall FIX:** Walkway Wall FIX SMIM

## 2.7 [Landscape Fixes for Grass Mods](https://www.nexusmods.com/skyrimspecialedition/mods/9005?tab=files)

### Download Instructions

- **Main File** - Landscape Fixes For Grass Mods
- **Optional File** - z Vanilla Military Camps
- **Optional File** - Patches for Arthmoor’s Town add-ons

### Download Instructions - Patches for Arthmoor's Towns

- **Select options:**
  * Patch for Alternate Start - Live Another Life
  * ~~Patch for Cutting Room Floor~~
  * Patch for Arthmoor’s Dragon Bridge
  * Patch for Arthmoor’s Shor’s Stone
  * Patch for Arthmoor’s Falkreath
  * Patch for Arthmoor’s Rorikstead
  * Patch for Arthmoor’s Ivarstead
  * Patch for Provincial Courier
  * ~~Patch for Oakwood~~

### Mod Order Instructions

- Place **Landscape Fixes for Grass Mods - Arthmoor’s Towns Patches** below the **PATCHES** separator.

## 2.8 [No Animals Report Crimes (NARC)](https://www.nexusmods.com/skyrimspecialedition/mods/17946?tab=files)

### Download Instructions

- **Main File** - NARC Remade 1.0.1 - Standard edition

### FOMOD Instructions

- **Select core file:**
  - NARC
- **Select patches:**
  - ~~Patch for Beyond Reach~~
  - ~~Patch for Beyond Skyrim - Bruma~~
  - ~~Patch for Blaze of Eventide~~
  - ~~Patch for Convenient Horses~~
  - ~~Patch for Darkend~~
  - Patch for The Forgotten City
  - ~~Patch for The Gray Cowl of Nocturnal~~
  - ~~Patch for Immersive Horses~~
  - ~~Patch for Skyrim Immersive Creatures~~

## 2.9 [Raven Rock - Fix Exit on Horseback](https://www.nexusmods.com/skyrimspecialedition/mods/14075?tab=files) (optional)

### Download Instructions

- **Main File** - Raven Rock - Fix Exit on Horseback SE

## 2.10 [Dawnguard Don't Hunt Cured Vampires](https://www.nexusmods.com/skyrimspecialedition/mods/5471?tab=files) (optional)

### Download Instructions

- **Main File** - Dawnguard Dont Hunt Cured Vampires 1_0

## 2.11 [Charge Dialogue Fix](https://www.nexusmods.com/skyrimspecialedition/mods/17716) (optional)

### Download Instructions

- **Main File** - Charge Dialogue Fix

## 2.12 [Rude Imperial Soldiers Escort Prisoner Fix](https://www.nexusmods.com/skyrimspecialedition/mods/894?tab=files) (optional)

### Download Instructions

- **Main File** - ImperialSoldiersEscortFix_v10

### Porting Instructions

- Resave **ImperialSoldiersEscortFix.esp** in the Creation Kit.

## 2.13 [Mannequins Stay Put](https://www.nexusmods.com/skyrimspecialedition/mods/6414?tab=files) (optional)

### Download Instructions

- **Main File** - Mannequin Stay Put

## 2.14 [Eye Normal Map Fix](https://www.nexusmods.com/skyrimspecialedition/mods/5445?tab=files) (optional)

### Download Instructions

- **Optional File** - Eye Normal Map Fix SSE BC7

## 2.15 [Skyrim Ultimate Eyemeshes Ruhmastered](https://www.nexusmods.com/skyrimspecialedition/mods/18147?tab=files)

### Download Instructions

- **Main File** - SUEMR SSE v3.0 Meshes
- **Main File** - SUEMR v3.0 Simple Vampire Fixes SSE
- **Optional File** - SUEMR Optional Red Vampire Eye Meshes SSE

### Additional Instructions

- Double-click **Skyrim Ultimate Eye Meshes Ruhmastered - Simple Vampire Fixes** in your mod order.
- Switch to the **Filetree** tab and rename the following file:
  * SimpleVampFixesSSE.**esp**

> This changes the plugin from ESL to ESP-Lite in order to allow us to manipulate its load order position.

## 2.16 [Eyes AO Clipping Fix](https://www.nexusmods.com/skyrimspecialedition/mods/25753?tab=files) (optional)

### Download Instructions

- **Optional File** - Eyes AO Clipping Fix - Ruhmastered

### Additional Instructions

* Delete the following file(s) and/or folders:
  * `meshes\actors\character\character assets\eyesmalevampire.nif`
  * `meshes\actors\character\character assets\eyesfemalevampire.nif`

> These meshes conflict with SUEMR - Vampire Eye Glow.

## 2.17 [ENB Brow Fix](https://www.nexusmods.com/skyrimspecialedition/mods/18783?tab=files) (optional)

### Download Instructions

- **Main File** - ENB Brow Fix SE 1.2

## 2.18 [Double Sided Vertex Human Mouth Fix](https://www.nexusmods.com/skyrimspecialedition/mods/25938?tab=files) (optional)

### Download Instructions

- **Main File** - Double Sided Human Mouth Fix SSE

## 2.19 [WoodElf - MaleHair - Fix](https://www.nexusmods.com/skyrimspecialedition/mods/9271?tab=files) (optional)

### Download Instructions

- **Main File** - WoodElf - MaleHair - Fix

## 2.20 [Sound Hammering Sounds](https://www.nexusmods.com/skyrimspecialedition/mods/5592?tab=files) (optional)

### Download Instructions

- **Main File** - Sound Hammering Sounds

## 2.21 [Dragon Stalking Fix](https://www.nexusmods.com/skyrimspecialedition/mods/14060?tab=files) (optional)

### Download Instructions

- **Main File** - Dragon Stalking Fix

### Additional Instructions

- Unpack **DragonStalkingFix.bsa** through Mod Organizer 2.
- Delete the following file(s) and/or folder(s):
  * `DragonStalkingFix.esp`
  * `DragonStalkingFix.bsa`

> The plugin is empty and only serves to load the archive which is now unpacked.

## 2.22 [Serana's Hood Fix](https://www.nexusmods.com/skyrimspecialedition/mods/20243?tab=files) (optional)

### Download Instructions

- **Main File** - Serana’s Hood Fix

### FOMOD Instructions

* **Choose Version:** Realistic

## 2.23 [Bug Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/33261?tab=files)

### Download Instructions

- **Main File** - Bug Fixes SSE v2

## 2.24 [Actor Limit Fix](https://www.nexusmods.com/skyrimspecialedition/mods/32349?tab=files)

### Download Instructions

- **Main File** - ActorLimitPlugin v2

![separator](../Media/separator.png)

# 03. Tweaks

## 3.1 [Run For Your Lives](https://www.nexusmods.com/skyrimspecialedition/mods/2272?tab=files)

### Download Instructions

- **Main File** - Run For Your Lives

## 3.2 [Dwemer Gates Don't Reset](https://www.nexusmods.com/skyrimspecialedition/mods/26331?tab=files) (optional)

### Download Instructions

- **Main File** - Dwemer Gates Don't Reset

### FOMOD Instructions

- **Versions:** Dwemer Only USSEP

## 3.3 [Calcelmo Has Standards](https://www.nexusmods.com/skyrimspecialedition/mods/26503?tab=files) (optional)

### Download Instructions

- **Main File** - Calcelmo Has Standards SE

## 3.4 [Move It Dammit](https://www.nexusmods.com/skyrimspecialedition/mods/752?tab=files) (optional)

### Download Instructions

- **Main File** - Move it Dammit - for Skyrim Special Edition v1.1.0b (Installation Script)

### FOMOD Instructions

- **Custom:** Move it Dammit

## 3.5 [NPCs Run and Walk at Your Pace](https://www.nexusmods.com/skyrimspecialedition/mods/2482?tab=files) (optional)

### Download Instructions

- **Main File** - Run and Walk at your Pace

## 3.6 [No More Standing Too Close](https://www.nexusmods.com/skyrimspecialedition/mods/4784) (optional)

### Download Instructions

- **Main File** - No More Standing Too Close SSE

## 3.7 [Realistic Conversations](https://www.nexusmods.com/skyrimspecialedition/mods/1717?tab=files) (optional)

### Download Instructions

- **Main File** - Realistic Conversations

## 3.8 [No NPC Greetings](https://www.nexusmods.com/skyrimspecialedition/mods/1044?tab=files) (optional)

### Download Instructions

- **Main File** - No NPC Greetings (Special Edition) - NMM FOMOD Installer

### FOMOD Instructions

- **Select an Option:** Reduced Distance (Recommended)

## 3.9 [Don't Talk With Your Mouth Full](https://www.nexusmods.com/skyrimspecialedition/mods/17715?tab=files) (optional)

### Download Instructions

- **Main File** - Don’t Talk With Your Mouth Full

## 3.10 [Random Encounter Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/16804?tab=files) (optional)

### Download Instructions

- **Main File** - Random Encounter Tweaks

## 3.11 [Morrowloot Miscellania - Better Ancient Knowledge](https://www.nexusmods.com/skyrimspecialedition/mods/27094?tab=files) (optional)

### Download Instructions

- **Main File** - Morrowloot Miscellania - Better Ancient Knowledge

## 3.12 [Merchants and Citizens Have No Lockpicks](https://www.nexusmods.com/skyrimspecialedition/mods/2798?tab=files) (optional)

### Download Instructions

- **Main File** - Merchants and Citizens Have No Lockpicks SE

## 3.13 [No Spinning Death Animation](https://www.nexusmods.com/skyrimspecialedition/mods/1432?tab=files) (optional)

### Download Instructions

- **Main File** - No Spinning Death Animation MERGED

## 3.14 [Improved Weapon Impact Effects](https://www.nexusmods.com/skyrimspecialedition/mods/8936?tab=files) (optional)

### Download Instructions

- **Main File** - Sparkles

## 3.15 [Simply Smaller Wolves](https://www.nexusmods.com/skyrimspecialedition/mods/10935?tab=files) (optional)

### Download Instructions

- **Main File** - Simply Smaller Wolves

> The file is actually called Simply Bigger Wolves. Don’t be confused, this is a mistake on the part of the author.

### Additional Instructions

Simply Smaller Wolves conflicts with the USSEP. We will resolve these conflicts manually.

* Run **SSEEdit** through Mod Organizer 2.
* Click **OK** in the plugin selection window to load all your mods.
* Wait until SSEEdit returns `Background loader: finished`.
* Double-click **SimplySmallerWolfs2.esp** in the left pane to expand the plugin.
* Double-click **Non-Player Character (Actor)** and select the **EncC06WolfSpirit** record inside.
* Drag and drop all edits highlighted red from the **Unofficial Skyrim Special Edition Patch.esp** column into **SimplySmallerWolfs2.esp**.
* When asked, click **Yes I'm absolutely sure**.
* Once both conflicts are resolved, the record will be displayed in green.
* Close SSEEdit. Click **OK** to save your changes and quit.

![Simply Smaller Wolves 1](Pictures/mod_installation/simply_smaller_wolves_conflict_1.png)

![Simply Smaller Wolves 2](Pictures/mod_installation/simply_smaller_wolves_conflict_2.png)

## 3.16 [Quiet Dog](https://www.nexusmods.com/skyrimspecialedition/mods/6066?tab=files) (optional)

### Download Instructions

- **Main File** - Quiet Dog - Sit

## 3.17 [Skeletons Don't Breathe](https://www.nexusmods.com/skyrimspecialedition/mods/18542?tab=files) (optional)

### Download Instructions

- **Main File** - skeletons don’t breathe SSE loose files version

## 3.18 [Remove Sneak Attack Sound](https://www.nexusmods.com/skyrimspecialedition/mods/17496?tab=files) (optional)

### Download Instructions

- **Main File** - Remove Sneak Attack Sound - Loose

## 3.19 [Bard Instrumentals Mostly - Sing Rarely](https://www.nexusmods.com/skyrimspecialedition/mods/10927?tab=files) (optional)

### Download Instructions

- **Main File** - Bard Instrumentals Mostly - Sing Rarely

## 3.20 [No Crime Teleport](https://www.nexusmods.com/skyrimspecialedition/mods/13109?tab=files) (optional)

### Download Instructions

- **Main File** - No Crime Teleport

## 3.21 [Better Dialogue Controls](https://www.nexusmods.com/skyrimspecialedition/mods/1429?tab=files) (optional)

### Download Instructions

- **Main File** - Better Dialogue Controls v1_2

## 3.22 [Better MessageBox Controls](https://www.nexusmods.com/skyrimspecialedition/mods/1428?tab=files) (optional)

### Download Instructions

- **Main File** - Better MessageBox Controls v1_2

## 3.23 [Better Stealing](https://www.nexusmods.com/skyrimspecialedition/mods/32295?tab=files) (optional)

### Download Instructions

- **Main File** - BetterStealing v2

## 3.24 [Uninterrupted Invisibility](https://www.nexusmods.com/skyrimspecialedition/mods/21729?tab=files) (optional)

### Download Instructions

- **Main File** - Uninterrupted Invisibility v2

## 3.25 [Uninterrupted Ethereal Form](https://www.nexusmods.com/skyrimspecialedition/mods/21765?tab=files) (optional)

### Download Instructions

- **Main File** - Uninterrupted Ethereal Form v2

![separator](../Media/separator.png)

# 04. Interface

## 4.1 [SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/12604?tab=files)

### Download Instructions

- **Main File** - SkyUI_5_2_SE

### Additional Instructions

- Run SSEEdit through Mod Organizer 2.
- Click **OK** in the plugin selection window to load all plugins.
- Wait for your mods to be loaded up before you proceed.
- Right-click **SkyUI_SE.esp** in the left pane and select **Add Masters**.
- Check **Skyrim.esm** and click **OK**.
- Click **Yes, I’m sure** when the warning comes up.
- Close SSEEdit and click **OK** to save your changes.

> The plugin had no masters assigned to it which causes errors. Every plugin needs to have at least Skyrim.esm as a master.

## 4.2 [Fix Note Icon for SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/32561/?tab=files) (optional)

### Download Instructions

- **Main File** - FixNotesForSkyUI SKSE64 2.0.17

## 4.3 [Remove Quicksave Button from SkyUI Systems Menu](https://www.nexusmods.com/skyrimspecialedition/mods/28334?tab=files) (optional)

### Download Instructions

- **Optional File** - Remove QuickSave and Help Buttons (1)

> While optional, I highly recommend installing this mod as it also contains the [Flashing Savegame Fix](https://www.nexusmods.com/skyrimspecialedition/mods/20406) for SkyUI which solves a very annoying issue.

### About the mod

While quicksaving is not actually broken as the mod page claims ([more about that here](https://www.reddit.com/r/skyrimmods/comments/7bkazq/whats_the_real_deal_with_quicksavesautosaves/)), I personally like the re-ordering and decluttering of the Pause menu. It will look as follows:

- MCM
- Save
- Load
- Settings
- Controls
- Quit

## 4.4 [Wider MCM Menu for SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/22825?tab=files) (optional)

### Download Instructions

- **Main File** - Opt. 1 - Wider MCM Menu for SkyUI

> You can download any one of the main files. Check the GIFs and choose your preferred version.

## 4.5 [Favorite Things - Extended Favorites Menu for SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/27177?tab=files) (optional)

### Download Instructions

- **Main File** - Opt. 1 - Modified Vanilla Favorites

> You can download any one of the main files. Check the pictures and choose your preferred version.

## 4.6 [Stay At The System Page](https://www.nexusmods.com/skyrimspecialedition/mods/19832?tab=files) (optional)

### Download Instructions

- **Main File** - Stay At System Page

## 4.7 [RaceMenu](https://www.nexusmods.com/skyrimspecialedition/mods/19080?tab=files)

### Download Instructions

- **Main File** - RaceMenu Special Edition v0-4-12

### Additional Instructions

- Delete the following file(s) and/or folder(s):
  * `RaceMenuPlugin.esp`

## 4.8 [Immersive HUD - iHUD](https://www.nexusmods.com/skyrimspecialedition/mods/12440?tab=files)

### Download Instructions

- **Main File** - Immersive HUD - iHUD

## 4.9 [SkyHUD](https://www.nexusmods.com/skyrimspecialedition/mods/463?tab=files)

### Download Instructions

- **Main File** - SkyHUD v090B v4
- **Update Files** - Patch - SkyHUD v090B ==merge with the main file==

### FOMOD Instructions

* **Install:** Loose Files
* **Preset:** Vanilla Small
* **Optional:** Install iHUD compatibility patch

### Additional Instructions

**This is optional.**

* Double-click **SkyHUD** in your mod order.
* In the **Text Files** tab, select the **skyhud.txt**.
* Edit the following lines:
  * `bAltArrow=1`
  * `bAltCompass=1`
  * `bDotCrosshair=1`
* Close the window and confirm when asked to save.

> This will change the compass to a slimmer one and improve the arrow display. The crosshair will be turned into a simple dot.

## 4.10 [Undiscovered Means Unknown](https://www.nexusmods.com/skyrimspecialedition/mods/9762?tab=files) (optional)

### Download Instructions

- **Main File** - Undiscovered Means Unknown - Compass and Map Markers

### FOMOD Instructions

* **Main:**
  * Both the Compass and the Map
* **Do you wish for the player's location to be marked on the map?**
  * Yes
* **SkyUI**:
  * Yes
* **Have you installed a HUD-altering mod?**
  * SkyHUD
* **Have you installed the mod Customizeable UI Replacer?**
  * No
* **Font choice:**
  * Custom font
* **Which colored map marker mod have you installed?**
  * Default - Skyrim SE
* **Do you wish for enemies to be visible in the compass?**
  * Yes (*this can easily be disabled in SkyHUD in the future*)
* **Which icon do you wish to use for undiscovered locations?**
  * Nothing

## 4.11 [moreHUD](https://www.nexusmods.com/skyrimspecialedition/mods/12688?tab=files) (optional)

### Download Instructions

- **Main File** - moreHUD SE Light Master

### Additional Instructions

- Double-click **moreHUD** in your mod order.
- Switch to the **Filetree** tab.
- Rename the following file:
  * AHZmoreHUD.**esp**

> This is faster than ESL-ifying the ESP.

## 4.12 [moreHUD - Inventory Edition](https://www.nexusmods.com/skyrimspecialedition/mods/18619?tab=files) (optional)

### Download Instructions

- **Main File** - moreHUD Inventory Edition

### Additional Instructions

- Double-click **moreHUD - Inventory Edition** in your mod order.
- Switch to the **Filetree** tab.
- Rename the following file:
  * AHZmoreHUDInventory.**esp**

> This is faster than ESL-ifying the ESP.

## 4.13 [A Matter of Time - A Clock HUD Widget](https://www.nexusmods.com/skyrimspecialedition/mods/12937?tab=files) (optional)

### Download Instructions

- **Main File** - AMatterOfTime_v3_0_0_alpha_4

## 4.14 [A Matter of Time - Phoenix Preset](https://www.nexusmods.com/skyrimspecialedition/mods/26092?tab=files) (optional)

### Download Instructions

- **Main File** - A Matter of Time - Phoenix Preset

> **Mod Dependency:** Only install this mod if you installed A Matter of Time. Otherwise skip it.

### About the mod

This is my personal preset for AMOT. It uses the slim clock widget to match the slim compass from SkyHUD and has a small 24h clock with the ingame time centered below. You can change the clock to 12h through the MCM at any time.

Even if you have the preset installed, you can configure the AMOT settings to your liking. It will only be applied if you load it through the MCM specifically.

Preview below:

![My AMOT Preset Preview](Pictures/mod_installation/amot_preset_preview.jpg)

## 4.15 [Shouts in the Dragon Tongue (SIDT)](https://www.nexusmods.com/skyrimspecialedition/mods/5515?tab=files) (optional)

### Download Instructions

- **Main File** - SIDT - Words Only

## 4.16 [Extended UI](https://www.nexusmods.com/skyrim/mods/57873?tab=files) (optional)

### Download Instructions

- **Main File** - Extended UI

### Porting Instructions

- Resave **Extended UI.esp** in the Creation Kit.
- Unpack **Extended UI.bsa** through Mod Organizer 2.

> Don't forget to delete the BSA after unpacking it.

## 4.17 [Skyrim SE Skill Interface Retexture (SSIRT)](https://www.nexusmods.com/skyrimspecialedition/mods/1523?tab=files) (optional)

### Download Instructions

- **Main File** - SSIRT SE v4.1

### FOMOD Instructions

Below are my personal choices. Feel free to make your own!

- **Background:**
  - Background - Irradiant Stars - HDR Nebula
- **Perk Lines:**
  - Default
- **Perk Line Colour:**
  - Default
- **Constellations:**
  - HD Default
- **Perk Stars:**
  - Option 2
- **Dawnguard:**
  - HD Masser and Secunda and More Stars
- **Vampire Background:**
  - HDR Nebula

##  4.18 [No More Laser-Printed Book](https://www.nexusmods.com/skyrimspecialedition/mods/462?tab=files) (optional)

### Download Instructions

- **Main File** - No More Laser-Printed Book

## 4.19 [Immersive Bookreading and Lockpicking](https://www.nexusmods.com/skyrimspecialedition/mods/4541?tab=files) (optional)

### Download Instructions

- **Main File** - Immersive Bookreading
- **Main File** - Immersive Lockpicking

## 4.20 [JS Lockpicking UI](https://www.nexusmods.com/skyrimspecialedition/mods/22160?tab=files) (optional)

### Download Instructions

- **Main File** - 2k Textures

## 4.21 [A Quality World Map](https://www.nexusmods.com/skyrimspecialedition/mods/5804?tab=files)

### Download Instructions

- **Main File** - 8.4 A Quality World Map - Classic with All Roads

### Additional Instructions, Part 1

* Unpack **icepenguinworldmapclassic - textures.bsa** through Mod Organizer 2.
* Delete the following file(s) and/or folder(s):
  * `icepenguinworldmapclassic.esp`

> The BSA is deleted in order to allow A Quality World Map to overwrite some LOD files from Cathedral Landscapes. The plugin only contains one record which is completely overwritten by the AQWM+Luminosity lighting patch and it is no longer needed to load the BSA so it is redundant.

### Additional Instructions, Part 2

* Double-click **A Quality World Map** in your mod order.
* Switch to the **Filetree** tab.
* Rename the following file:
  * `icepenguinworldmapclassic.ini` >>> `maplightfix.ini`

> Since we just deleted the plugin, it can no longer load the INI file. By renaming it, the INI will now be loaded by the Luminosity map lighting patch (installed later on).

## 4.22 [Dynamic Snow for Map](https://www.nexusmods.com/skyrim/mods/29877?tab=files) (optional)

### Download Instructions

- **Main File** - Type 1

## 4.23 [Dawnguard Map Markers](https://www.nexusmods.com/skyrimspecialedition/mods/20931?tab=files) (optional)

### Download Instructions

- **Main File** - Dawnguard Map Markers

## 4.24 [Smaller Vanilla Cursor](https://www.nexusmods.com/skyrimspecialedition/mods/20617?tab=files) (optional)

### Download Instructions

- **Main File** - Smaller Vanilla Cursors

### FOMOD Instructions

* **Step 1:** Right

> If you are left-handed, feel free to select the "Left" option.

## 4.25 [ReCleaned Menu](https://www.nexusmods.com/skyrimspecialedition/mods/26680?tab=files) (optional)

### Download Instructions

- **Main File** - ReCleanedMenus

## 4.26 [Loading Screen Smoke Removed](https://www.nexusmods.com/skyrimspecialedition/mods/4634?tab=files) (optional)

### Download Instructions

- **Main File** - Loading Screen Smoke Removed v1.0

## 4.27 [KenMOD - Time on Loading Screen](https://www.nexusmods.com/skyrim/mods/98?tab=files) (optional)

### Download Instructions

- **Main File** - Time on loading v5

![separator](../Media/separator.png)

# 05. Main Visual Mods

## 5.1 [Skyrim Realistic Overhaul (SRO)](https://www.moddb.com/mods/skyrim-realistic-overhaul)

### Download Instructions

- **Main File** - This mod has already been installed.

## 5.2 [DynDOLOD Resources](https://www.nexusmods.com/skyrimspecialedition/mods/32382?tab=files)

### Download Instructions

- **Main File** - DynDOLOD Resources SE

### FOMOD Instructions

- **Visual Options:**
  * Whiterun Exterior
  * Solitude Exterior
  * High Hrothgar Window Glow
  * DLC2 Vvardenfell 3D Plume
- **Performance Options:**
  * ~~Low-Res LOD Textures~~
- **Misc Options:**
  * Desync Birds of Prey
  * ~~Holy Cow~~

## 5.3 [HD LODs Textures](https://www.nexusmods.com/skyrimspecialedition/mods/3333?tab=files)

### Download Instructions

- **Main File** - HD Lods Textures SE 1K V9.3 - DynDOLOD ONLY VERSION

## 5.4 [Noble Skyrim Mod HD-2K (NSM)](https://www.nexusmods.com/skyrimspecialedition/mods/21423?tab=files)

### Download Instructions

- **Main File** - A. Noble Skyrim - FULL PACK_2K
- **Update File** - NSM - SMIM Patch

## 5.5 [Ruins Clutter Improved (RCI)](https://www.nexusmods.com/skyrimspecialedition/mods/5870/?tab=files)

### Download Instructions

* **Main Files** - Ruins_Clutter_Improved_SE_NMM_v3-1
* **Update Files** - Falmer Temple Chandelier ==merge with the main file==

### FOMOD Instructions

* **Options:**
  * Custom
* **Custom:**
  * High Resolution Candles
  * HD Catacomb Candles
  * HD Enchanting Stations
  * HD Spider Eggs
  * HD Pots
  * Improved Ruins Doors
  * ~~Improved Dragonclaws~~
  * ~~Subliminal Traps~~
  * ~~Lantern~~

## 5.6 [Ruins Clutter Improved - Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/21031?tab=files)

### Download Instructions

* **Main File** - Ruins Clutter Improved - Fixes 1.1

## 5.7 [Revamped Assets Skyrim](https://www.nexusmods.com/skyrim/mods/75380?tab=files)

### Download Instructions

- **Main File** - Revamped Assets Skyrim - High (FOMOD Package)

### FOMOD Instructions

- **Installation:**
  * Custom Install
- **Architecture:**
  * ~~Install All~~
- **Armor:**
  * ~~Install All~~
  * Mystic Tuning Gloves
- **Clothes:**
  * ~~Install All~~
  * ~~Clavicus Vile Mask~~
- **Clutter:**
  * ~~Install All~~
  * Clutter General
  * Bones
  * Dead Animals
  * Display Cases
  * ~~Firewood~~
  * Pelagius Hipbone
  * ~~Silver~~
  * ~~Sovngarde~~
  * ~~Statues~~
  * Weapon Rack
- **Furniture:**
  * Install All
- **Traps:**
  * Install All
- **Display Cases:**
  * Light

### Porting Instructions

* Run the mod through Cathedral Assets Optimizer (**Optimise SLE Assets**).

## 5.8 [High Poly Project](https://www.nexusmods.com/skyrimspecialedition/mods/12029?tab=files) (optional)

### Download Instructions

- **Main File** - High Poly Project

### FOMOD Instructions

- **Installation Type:**
  - ~~Install Everything~~
  - Custom Installation
- **Page 1:**
  - Hearthfire Breads
  - Vanilla Breads
  - ~~Farmhouse Stonewalls~~
  - ~~Solitude Ropes~~
  - Tents
  - ~~Whiterun Clutter~~
  - Windhelm Throne
  - Bones
  - Burnt Corpses
  - ~~Candles~~
- **Page 2:**
  - Common Clutter
  - Dragon Parts
  - ~~Food~~
  - Hagraven
  - Hay
  - Horker Tusk
  - Ingredients
  - ~~Shrines~~
  - ~~Silverware~~
  - Smelter Coal
- **Page 3:**
  - ~~Statues~~
  - ~~Wine Bottles~~
  - ~~Dungeons~~
  - ~~Funiture~~
  - ~~Plants~~
  - ~~Riften 3D Leaves~~
- **No Snow Under the Roof Patch:**
  - ~~Statues~~

## 5.9 [aMidianBorn Book of Silence - Dragonborn DLC](https://www.nexusmods.com/skyrim/mods/24909/?tab=files) (optional)

### Download Instructions

- **Main File** - aMidianBorn book of silence_DRAGONBORN DLC

> There is no need to download and install the Bonemold Hotfix since it is included in the aMidianBorn Content Addon which will be installed later on.

### FOMOD Instructions

* **Options:**
  * Custom
* **Custom:**
  * Nordic Carved Armor: None
  * Bonemold Armor
  * Acolyte Masks
  * Dragon Priest Acolytes
  * Hulking Draugr
  * Ash Spawn
  * Ash Guardian

> We are not installing any retexture for the Nordic Carved Armor because the aMidianBorn Content Addon will add all three varieties.

### Additional Instructions

* Double-click **aMidianBorn - Dragonborn** in your mod order.
* Switch to the **Filetree** tab.
* Find the following folder:
  * `textures\actors\dlc02\ash`
* Rename the **ash** folder to **ashman**.
* The resulting folder structure should be:
  * `textures\actors\dlc02\ashman`

## 5.10 [Caliente's Beautiful Bodies Enhancer (CBBE)](https://www.nexusmods.com/skyrimspecialedition/mods/198?tab=files)

### Download Instructions

- **Main File** - Caliente's Beautiful Bodies Enhancer - v1.5.6

### FOMOD Instructions

* **Body Shape:**
  * Vanilla Shape
* **Underwear Options:**
  * NeverNude
* **Outfit Options:**
  * Vanilla Outfits
* **Face Options:**
  * Face Pack
  * ~~Dirt to Beauty Marks~~
* **Eyebrow Options:**
  * None
* **Miscellaneous:**
  * ~~Pubic Hair~~
* **SKEE (RaceMenu):**
  * ~~RaceMenu Morphs (BodyMorph)~~
* **Morph Files:**
  * ~~Morph Files (Body)~~
  * ~~Morph Files (Outfits)~~

![separator](../Media/separator.png)

# 06. Weather

## 6.1 [Obsidian Weathers and Seasons](https://www.nexusmods.com/skyrimspecialedition/mods/12125?tab=files)

### Download Instructions

* **Main File** - Obsidian Weathers - 1.07

## 6.2 [Obsidian Weathers and Seasons MCM Patch](https://www.nexusmods.com/skyrimspecialedition/mods/20209?tab=files) (optional)

### Download Instructions

* **Main File** - Obsidian Weathers and Seasons MCM ESP-ESL

## 6.3 [Smooth Sky Mesh](https://www.nexusmods.com/skyrimspecialedition/mods/18350?tab=files) (optional)

### Download Instructions

* **Main File** - Smooth Sky Mesh 0_262

## 6.4 [ETHEREAL CLOUDS](https://www.nexusmods.com/skyrimspecialedition/mods/2393?tab=files) (optional)

### Download Instructions

* **Main File** - ETHEREAL CLOUDS - Special Edition - 2K

## 6.5 [Skyrim Textures Redone - Enhanced Night Sky](https://www.nexusmods.com/skyrimspecialedition/mods/5561?tab=files) (optional)

### Download Instructions

* **Main File** - Download and install the main file.

### FOMOD Instructions

* **Stars:**
  * 2K Stars
* **Stars Type:**
  * 2k only small stars
* **Moons:**
  * 2K Moons
* **Nebula:**
  * 4K Nebula
* **Aurora:**
  * 4K Aurora
* **Constellations:**
  * 2K Constellations

## 6.6 [Night Skies - Stars and Galaxies](https://www.nexusmods.com/skyrimspecialedition/mods/20301?tab=files) (optional)

### Download Instructions

* **Main File** - Night Skies - Milky Realism (4K) - CP 1.01

## 6.7 [Skygazer Moons - Masser and Secunda ](https://www.nexusmods.com/skyrimspecialedition/mods/32057?tab=files)(optional)

### Download Instructions

* **Main File** - Skygazer Moons SSE 2K - GLOW

## 6.8 [Storm Lightning](https://www.nexusmods.com/skyrimspecialedition/mods/29243?tab=files) (optional)

### Download Instructions

* **Main File** - Storm Lightning for SSE and VR - Fomod Installer

### FOMOD Instructions

* **Select Game** - Skyrim Special Edition
* **Select SSE Version -** 1.5.97
* **Select Plugin:** ESL Flagged

The next couple settings are depend on your choice of ENB as well as personal preferences. I selected the “Halo Dimmer” options and will add my personal recommendations here after more testing.

## 6.9 [Yee - A New Snowflake Mod](https://www.nexusmods.com/skyrimspecialedition/mods/21559?tab=files) (optional)

**DOWNLOAD INSTRUCTIONS**

* **Main File** - Ultra Realistic Snowfall

> Ignore the warning about the mod being outdated. It still works perfectly with Obsidian Weathers.

## 6.10 [Wonders of Weather](https://www.nexusmods.com/skyrimspecialedition/mods/13044?tab=files) (optional)

### Download Instructions

* **Main File** - Wonders of Weather v1_10

### FOMOD Instructions

* Change nothing, just click **Install**.

##  6.11 [Wonders of Weather - Less Opaque Rain Splashes for ENB](https://www.nexusmods.com/skyrimspecialedition/mods/32062?tab=files) (optional)

### Download Instructions

* **Main File** - Wonders Of Weather - Less opaque rain splashes for ENB

### FOMOD Instructions

- **Select Transpareny:** 95% (Personal Choice)

![separator](../Media/separator.png)

# 07. Lighting

## 7.1 [Relighting Skyrim](https://www.nexusmods.com/skyrimspecialedition/mods/8586?tab=files)

### Download Instructions

* **Main Files** - Relighting Skyrim SSE v1.1.0

## 7.2 [Relighting Skyrim - No Player Homes](https://www.nexusmods.com/skyrimspecialedition/mods/26538?tab=files)

### Download Instructions

* **Main Files** - Relighting Skyrim SSE - No Player Homes

## 7.3 [Luminosity Lighting Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/16830?tab=files)

### Download Instructions

* **Main Files** - Luminosity - Lightweight Lighting

## 7.4 [Luminosity - A Quality World Map Patch](https://www.nexusmods.com/skyrimspecialedition/mods/30162?tab=files)

### Download Instructions

* **Main Files** - A Quality Worldmap - Luminosity Compatibility Patch

### Mod Order Instructions

* Place the mod below the **PATCHES** separator

## 7.5 [Interior Floating Fog Remover](https://www.nexusmods.com/skyrimspecialedition/mods/4298?tab=files) (optional)

### Download Instructions

* **Main Files** - No Floating Fog

## 7.6 [Smoking Torches and Candles (STAC)](https://www.nexusmods.com/skyrimspecialedition/mods/8607?tab=files)

### Download Instructions

* **Main Files** - Smoking Torches and Candles

### FOMOD Instructions

* **Main Component:**
  * Smoking Torches (Classic)
* **Smoking Candles:**
  * Max Quality
* **Plugin Selection:**
  * ESPFE
  * ~~ESP~~
  * ~~ESL~~

## 7.7 [Embers HD](https://www.nexusmods.com/skyrimspecialedition/mods/14368?tab=files)

### Download Instructions

* **Main Files** - Embers HD

### FOMOD Instructions

* **Main Component:**
  * Embers HD 2K
* **Embers HD Fireplaces:**
  * Fireplaces Add-On
* **Add-On Component:**
  * Forges Add-On
  * Lava Crater Add-On
* **Compatibility Patches:**
  * ~~Campfire Patch~~
  * ~~Realistic HD Blacksmith Patch~~
  * ~~Realistic Lighting Overhaul Patch~~
  * ~~Smoking Torches Patch~~

### Additional Instructions

* Delete the following file(s) and/or folder(s):
  * `meshes\furniture\workbenches\`
  * `meshes\furniture\alchemyworkbench.nif`
  * `meshes\furniture\alchemyworkstation.nif`

## 7.8 [Inferno - Fire Effects Redux](https://www.nexusmods.com/skyrimspecialedition/mods/29316?tab=files)

### Download Instructions

* **Main Files** - Inferno - Fire Effects Redux - AIO

### FOMOD Instructions

* **Inferno Textures Resolution:**
  * Lite
* **Glow Options:**
  * Brighter
* **Color Options:**
  * Freesia
* **Flame Tile:**
  * New
* **Flame Size:**
  * Regular
* **Optional Patches:**
  * KD - Realistic Fireplaces + Ember HD
* **Optional Patches:**
  * Smoking Torches and Candles
* **Optional Plugin:**
  * Flame Meshes Patch (ESL-Tagged)

## 7.9 [KD - Realistic Fireplaces](https://www.nexusmods.com/skyrimspecialedition/mods/28877?tab=files)

### Download Instructions

* **Main Files** - KD - Realistic Fireplaces SE - V3

### FOMOD Instructions

* **Necessary Information:**
  * I have read it all!
* **Cut Wire:**
  * Yellow wire
* **Installation core setting:**
  * ESP Version(Highly Recommended)
* **Texture Resolution Options:**
  * KD - Realistic Fireplaces 2K
* **Realistic Pulsating Glow Options:**
  * KD - Fire Glow (Recommended)
* **Implement Complex Particle Lights for ENB?:**
  * Yes (Highly recommended if you are using ENB)
* **Intensity of Complex Particle Lights:**
  * Sweet Spot(Recommended)
* **Compatibility Patches:**
  * Embers HD Patch
* **Embers HD Patch:**
  * I trust Kenan’s taste.(Recommended)

## 7.10 [Charred Logs for KD - Realistic Fireplaces](https://www.nexusmods.com/skyrimspecialedition/mods/29376?tab=files) (optional)

### Download Instructions

* **Optional Files** - KD - Realistic Fireplaces - Charred Logs 2K

![separator](../Media/separator.png)

# 08. Visual FX

## 8.1 [Frozen Electrocuted Combustion (FEC)](https://www.nexusmods.com/skyrimspecialedition/mods/3532?tab=files) (optional)

### Download Instructions

- **Main File** - Frozen Electrocuted Combustion - 3.3

## 8.2 [Frozen Electrocuted Combustion - Extra Crispy Retexture](https://www.nexusmods.com/skyrimspecialedition/mods/25127?tab=files) (optional)

### Download Instructions

- **Main File** - Frozen Electrocuted Combustion - Extra Crispy Retexture

> **Mod Dependency:** Only install this mod if you installed **Frozen Electrocuted Combustion**. Otherwise skip it.

## 8.3 [Enhanced Blood Textures](https://www.nexusmods.com/skyrimspecialedition/mods/2357?tab=files)

### Download Instructions

* **Main File** - Enhanced Blood Textures SE

### FOMOD Instructions

- **Compatibility Patch:**
  - ~~Immersive Creatures~~
- **Effects Distance:**
  - Medium
- **Blood Size:**
  -  None
- **Wounds:** 
  - Reduced Wound Size (Optional)
- **Textures:**
  -  Reduced Res / Default Color
- **Blurry Screen Blood:**
  - ~~EBT Blurry Screen Blood (Optional)~~
- **Alternate Textures:**
  -  Reduced Res / Default Color

## 8.4 [GORECAP](https://www.nexusmods.com/skyrimspecialedition/mods/16440?tab=files) (optional)

### Download Instructions

* **Main Files** - GORECAP

## 8.5 [Deadly Spell Impacts](https://www.nexusmods.com/skyrimspecialedition/mods/12939?tab=files)

### Download Instructions

* **Main Files** - Deadly Spell Impacts v1_70

### FOMOD Instructions

* **Options:**
  * Custom
* **Custom:**
  * One Fire Impact (Default)
* **Fire:**
  * Alternate 1
* **Frost:**
  * Default
* **Lightning:**
  * Alternate 1

## 8.6 [Arctic - Frost Effects Redux](https://www.nexusmods.com/skyrimspecialedition/mods/29817?tab=files) (optional)

### Download Instructions

* **Main Files** - Arctic - Frost Effects Redux - AIO

### FOMOD Instructions

* **Resolution Options:** Lite
* **Color Options:** Realistic Hue
* **Icicles Size:** x.5
* **Icicles Style:** Transparent
* **Optional Plugin:** Frost Meshes Patch (ESL-Tagged)

## 8.7 [Refracting Ice Form Debris](https://www.nexusmods.com/skyrimspecialedition/mods/18384?tab=files) (optional)

### Download Instructions

* **Main Files** - Refracting Ice Form Debris - SSE - 1.1

## 8.8 [Voltage](https://www.nexusmods.com/skyrimspecialedition/mods/15565?tab=files) (optional)

### Download Instructions

* **Optional Files** - Voltage 2K

## 8.9 [ElSopa HD - Dirt Blast](https://www.nexusmods.com/skyrimspecialedition/mods/22342?tab=files) (optional)

### Download Instructions

* **Main Files** - 1K ElSopa HD - Dirt Blast

## 8.10 [Reduced Glow FX](https://www.nexusmods.com/skyrimspecialedition/mods/20691?tab=files) (optional)

### Download Instructions

* **Main Files** - Reduced Glow FX SE

## 8.11 [Fire Halo Remover ](https://www.nexusmods.com/skyrimspecialedition/mods/28381?tab=files)(optional)

### Download Instructions

* **Main Files** - Fire Halo Remover

## 8.12 [Subtle Wind FX](https://www.nexusmods.com/skyrimspecialedition/mods/24395?tab=files) (optional)

### Download Instructions

* **Main Files** - Subtle Wind FX

## 8.13 [Glow Be Gone - Updated](https://www.nexusmods.com/skyrimspecialedition/mods/34148?tab=files) (optional)

### Download Instructions

* **Main Files** - GlowBeGoneSSE-Updated

![separator](../Media/separator.png)

# 09. Landscape

## 9.1 [Majestic Mountains](https://www.nexusmods.com/skyrimspecialedition/mods/11052?tab=files)

### Download Instructions

* **Main Files** - 1. Majestic Mountains Main File

> The LOD Pack is not required as the same textures are already packaged with HD LOD Textures which we installed in Step 5.

### FOMOD Instructions

* **Snow Mountain Type:**
  * Snow Mountain New version ESL
* **Optionals:**
  * ~~Landscape Textures~~
  * Moss Rocks ESL Version
  * ~~Moss Rocks ESP Version~~
* **Sun Direction:**
  * None
* **Compatibility Patches:**
  * SMIM

## 9.2 [Landscapes - Cathedral Concept](https://www.nexusmods.com/skyrimspecialedition/mods/21954?tab=files)

### Download Instructions

* **Main Files** - Landscapes - Cathedral Concept

### FOMOD Instructions

* **Select Install:** Full Install, Brown Tundra
* **Select Roads:** REALly Blended Roads

### Additional Instructions

* Delete the following file(s) and/or folder(s):
  * `textures\landscape\coastbeach01.dds`
  * `textures\landscape\coastbeach01_n.dds`
  * `textures\landscape\coastbeach02.dds`
  * `textures\landscape\coastbeach02_n.dds`
  * `textures\landscape\coastbeachgrass01.dds`
  * `textures\landscape\coastbeachgrass01_n.dds`
  * `textures\landscape\coastoceanfloor01.dds`
  * `textures\landscape\coastoceanfloor01_n.dds`
  * `textures\plants\`

> Cath Landscapes' **coast textures** unfortunately have extremely bad tiling.
> **Plants** will be covered by another mod later on.

### INI Tweak

* Double-click **Landscapes - Cathedral Concept** in your mod order.
* Switch to the **INI-Files** tab and select the **Cathedral Landscapes.ini**.
* Edit the following line:
  * `iMinGrassSize=40`
* Close the window and confirm when asked to save.

> A lower value means higher grass density and potentially decreased FPS.  You may want to experiment with it a little to find your sweet spot.

## 9.3 [The Elder Scrolls - Veydosebrom](https://www.nexusmods.com/skyrimspecialedition/mods/26293?tab=files) (optional)

### Download Instructions

* **Main File** - The Elder Scrolls - Veydosebrom

### FOMOD Instructions

* **Veydosebrom - Grasses and Groundcover:**
  * Packed
* **Choose your season:**
  * Vanilla Season
* **Choose your INI:**
  * None
* **Choose your landscape:**
  * Vanilla Landscape
* **Choose your quality:**
  * 1k Quality
* **BSA Archive:**
  * 1k Full

### About the mod

While Cathedral Landscape features incredibly performance friendly grasses, the type growing in the Morthal swamp area is famously ugly. Unfortunately, no other grass overhaul really features silver-white swamp grass. Veydosebrom's grass is somewhat desatured and looks great except it won't blend as well as Cath grass in the distance. Users will have to decide for themselves whether they consider much better looking grass overall worth the more noticeable grass fade-in.

I uploaded a comparison slider [here](https://imgsli.com/MTQ2OTc).

Be aware that Vey is not built for performance like Cath Landscapes so especially people playing on weaker machines may notice a drop in the swamp area (which is already notoriously performance intense).

## 9.4 [Cathedral Landscapes - Veydosebrom Swamp Grass Addon](https://www.nexusmods.com/skyrimspecialedition/mods/26092?tab=files) (optional)

### Download Instructions

* **Main File** - The Elder Scrolls - Veydosebrom

> **Mod Dependency:** Only install this mod if you installed **The Elder Scrolls - Veydosebrom**. Otherwise skip it.

## 9.5 [Pfuscher's Rapid Rocks](https://www.nexusmods.com/skyrimspecialedition/mods/26532?tab=files)

### Download Instructions

* **Main File** - Dark grey Rapid Rocks
* **Main File** - Update for both versions ==merge with the main file==

## 9.6 [Majestic Mountains - Northside](https://www.nexusmods.com/skyrimspecialedition/mods/27981?tab=files) (optional)

### Download Instructions

* **Main File** - Majestic Mountains - Northside

### FOMOD Instructions

* **Mountain Textures:**
  * Northside
* **Normal Maps:**
  * Default Normal Maps
* **Wet Rocks:**
  * Tweaked Wet Rock Meshes
  * Tweaked Rapid Rocks Textures
* **Northside Tweaks:**
  * ~~Northside Tweaks for (Majestic Mountains ESP version)~~
  * Northside Tweaks for (Majestic Mountains ESL version)

## 9.7 [Realistic Water Two (RW2)](https://www.nexusmods.com/skyrimspecialedition/mods/2182?tab=files)

### Download Instructions

* **Main File** - Realistic Water Two v2.2.2

### FOMOD Instructions

* Change nothing. Click **Next** and **Install**.

> On the second page (Mod Patches) the patch for Landscape Fixes for Grass Mods will automatically be ticked. This is intended.

### Additional Instructions

* Delete the following file(s) and/or folder(s):
  * `meshes\effects\fxrapidsrocks01.nif`

> The mesh is overwriting Pfuscher's new one included with Rapid Rocks.

## 9.8 [Skyrim SE Improved Puddles](https://www.nexusmods.com/skyrimspecialedition/mods/1462?tab=files) (optional)

### Download Instructions

* **Main Files** - Skyrim SE Improved Puddles FOMOD v1-4 for ENB users

### FOMOD Instructions

* **Textures:** 2048×2048 Resolution

## 9.9 [Better Dynamic Snow](https://www.nexusmods.com/skyrimspecialedition/mods/9121?tab=files)

### Download Instructions

* **Main Files** - Better Dynamic Snow SE v2.10.0

### FOMOD Instructions

* **Meshes:**
  * SMIM
* **Optional Addons:**
  * Snowy Farmhouses
* **Patches:**
  * ~~No Snow Under the Roof~~

## 9.10 [Better Dynamic Majestic Mountains](https://www.nexusmods.com/skyrimspecialedition/mods/20102?tab=files)

### Download Instructions

* **Main Files** - Better Dynamic Majestic Mountains - MM ESL Version

## 9.11 [Skyrim 3D Icefloes](https://www.nexusmods.com/skyrimspecialedition/mods/20101?tab=files) (optional)

### Download Instructions

* **Main Files** - Skyrim 3D Icefloes

## 9.12 [Better Dynamic Ash](https://www.nexusmods.com/skyrimspecialedition/mods/14644?tab=files)

### Download Instructions

* **Main Files** - Better Dynamic Ash SE

## 9.13 [Enhanced Landscapes - Dead Marsh](https://www.nexusmods.com/skyrimspecialedition/mods/18162?tab=files)

### Download Instructions

* **Main File** - Main File v1.65

### FOMOD Instructions

* **Optional Files**: Dead Marsh

### Additional Instructions

* Delete the following file(s) and/or folder(s):
  * `DynDOLOD\`
  * `Enhanced Landscapes.esp`
  * `Enhanced Landscapes - Dead Marsh.esp`

Rename the mod to “**Enhanced Landscapes - Dead Marsh**” to indicate that only that module is installed.

## 9.14 [Enhanced Landscapes - Dead Marsh Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/9951?tab=files)

### Download Instructions

* **Main Files** - Enhanced Landscapes - Dead Marsh Fixes

## 9.15 [Rorikstead Basalt Cliffs](https://www.nexusmods.com/skyrimspecialedition/mods/25718?tab=files) (optional)

### Download Instructions

* **Main Files** - Rorikstead Basalt Cliffs

## 9.16 [Rorikstead Basalt Cliffs Patches ](https://www.nexusmods.com/skyrimspecialedition/mods/31981?tab=files)(optional)

### Download Instructions

* **Main Files** - Rorikstead Basalt Cliffs Patches

> Install this mod if you installed Rorikstead Basalt Cliffs. Otherwise skip it.

### FOMOD Instructions

* **Patches:** Rorikstead Basalt Cliffs + Alternate Start - Live Another Life + Landscape Fixes for Grass Mods

### Mod Order

* Place the mod below the **PATCHES** separator.

## 9.17 [Ashbound - Solstheim Enhanced](https://www.nexusmods.com/skyrimspecialedition/mods/14663?tab=files)

### Download Instructions

* **Main Files** - Ashbound 1.1

## 9.18 [Point The Way](https://www.nexusmods.com/skyrimspecialedition/mods/352?tab=files)

### Download Instructions

* **Main Files** - Point The Way

## 9.19 [Lanterns of Skyrim II](https://www.nexusmods.com/skyrimspecialedition/mods/30817?tab=files)

### Download Instructions

* **Main Files** - Lanterns Of Skyrim II - FOMOD

### FOMOD Instructions

* **Addons:**
  * ~~LoS II - Lantern Workers Addon~~
  * ~~LoS II - Tamriel Master Lights (No Cities) Addon~~
  * ~~LoS II - Tamriel Master Lights (Cities version) Addon~~
* **Main Patches:**
  * LoS II - SMIM patch
  * ~~LoS II TML - Guards Armor Replacer patch~~
* **Patches (A):**
  * ~~LoS II - Beginner’s Shack in Riverwood patch~~
  * ~~LoS II - Blackthorn Manor patch~~
  * ~~LoS II - Bruma patch~~
  * ~~LoS II - Camp Argentum patch~~
  * ~~LoS II - Camp Varglya patch~~
  * ~~LoS II - City Entrances Overhaul - Windhelm patch~~
  * ~~LoS II - Convenient Bridges -Beta- patch~~
  * ~~LoS II - Eli’s Breezehome patch~~
  * ~~LoS II - Enhanced Solitude SSE patch~~
  * ~~LoS II - JK’s Skyrim patch~~
  * ~~LoS II - Northern Marsh Bridges patch~~
  * ~~LoS II - Old Hroldan Ruins SE patch~~
  * ~~LoS II - Overstead SE patch~~
  * ~~LoS II - Solitude Expansion patch~~
* **Patches (B):**
  * ~~LoS II - Expanded Towns and Cities (SSE) patch~~
  * ~~LoS II - Hunters Cabin of Riverwood SE patch~~
  * ~~LoS II - Legacy of the Dragonborn V5 patch~~
  * ~~LoS II - Run of the Mill Inn patch~~
  * ~~LoS II - Settlements Expanded patch~~
  * ~~LoS II - Solitude Docks patch~~
  * ~~LoS II - Umbra Island SSE patch~~
  * ~~LoS II - Weathered Road Signs patch~~
* **Patches (C):**
  * LoS II - Darkwater Crossing patch
  * LoS II - Dragon Bridge patch
  * LoS II - Falkreath patch
  * ~~LoS II - Helarchen Creek patch~~
  * LoS II - Ivarstead patch
  * LoS II - Karthwasten patch
  * LoS II - Kynesgrove patch
  * ~~LoS II - Oakwood patch~~
  * LoS II - Provincial Courier Service patch
  * LoS II - Shor’s Stone patch
  * LoS II - Soljund’s Sinkhole patch
  * ~~LoS II - Telengard patch~~
  * ~~LoS II - The Fall of Granite Hill patch~~
  * LoS II - Whistling Mine patch

## 9.20 [Manor Roads](https://www.nexusmods.com/skyrimspecialedition/mods/24715?tab=files) (optional)

### Download Instructions

* **Main Files** - Manor Roads

## 9.21 [Immersive Dawnguard Dayspring Pass (IDDP)](https://www.nexusmods.com/skyrimspecialedition/mods/4126?tab=files)

### Download Instructions

* **Main Files** - Immersive Dawnguard Dayspring Pass (IDDP)

![separator](../Media/separator.png)

# 10. Flora

## 10.1 [Enhanced Vanilla Trees (EVT)](https://www.nexusmods.com/skyrimspecialedition/mods/11008?tab=files)

### Download Instructions

* **Main File** – Enhanced Vanilla Trees SE v1.9.0

------

==**FOMOD INSTRUCTIONS**==

* **Mesh Options:**
  * Enhanced Darker Meshes
* **Tree Options:**
  * Lush Trees (small)
* **Clutter:**
  * Enhanced Tree Clutter (recommended)
  * ~~Firewood Textures~~
* **SFO Branch Textures:**
  * SFO Branch Textures - Version 4
* **Alternative Trees:**
  * ~~Realistic Aspen Trees~~
  * SFO Snowy Pine Trees

## 10.2 [Enhanced Vanilla Trees – Vurts Light Snow Trees](https://www.nexusmods.com/skyrim/mods/76086?tab=files)

### Download Instructions

* **Optional File** – Light Snow Trees Replacer (for Vurts snow tree option users)

### FOMOD Instructions

* Resave **EVT_LightSnowTrees_Replacer (For Vurts).esp** in the Creation Kit.

## 10.3 [Tree Bark in High Definition](https://www.nexusmods.com/skyrimspecialedition/mods/20336?tab=files) (optional)

### Download Instructions

* **Main File** - Tree Bark in High Definition

> While tree bark retextures are generally incompatible with the new meshes from EVT, this retexture, even though it wasn't made for EVT, looks perfectly fine. There are no textures cut off, or stretching.

### Additional Instructions

* Delete the following file(s) and/or folder(s):
  * `textures\landscape\trees\treeaspenbarkcomp.dds`
  * `textures\landscape\trees\treeaspenbarkcomp_n.dds`

> I prefer the aspen bark textures from Enhanced Vanilla Trees.

## 10.4 [Enhanced Landscapes – Oaks Standalone](https://www.nexusmods.com/skyrimspecialedition/mods/27367?tab=files)

### Download Instructions

* **Main File** – ELOS Oaks mixed greens

## 10.5 [Bent Pines II](https://www.nexusmods.com/skyrimspecialedition/mods/8306?tab=files) (optional)

### Download Instructions

* **Main File** – Bent Pines II

## 10.6 [Sacred Trees](https://www.nexusmods.com/skyrimspecialedition/mods/26214?tab=files) (optional)

### Download Instructions

* **Main File** – Sacred Trees

## 10.7 [Rudy HQ – Falling Leaves and Needles](https://www.nexusmods.com/skyrimspecialedition/mods/25939?tab=files) (optional)

### Download Instructions

* **Main File** - Rudy HQ - Falling Leaves and Needles for ENB SE

## 10.8 [Cathedral Plants](https://www.nexusmods.com/skyrimspecialedition/mods/26104?tab=files) (optional)

### Download Instructions

* **Main File** – Cathedral - Plants

## 10.9 [Realistic HD Mushrooms Remastered](https://www.nexusmods.com/skyrimspecialedition/mods/21996?tab=files) (optional)

### Download Instructions

* **Main File** – Realistic HD Mushrooms Remastered

## 10.10 [Less Ugly Tundra Grass](https://www.nexusmods.com/skyrimspecialedition/mods/26740?tab=files) (optional)

### Download Instructions

* **Main File** – Less Ugly Tundragrass – Redder Variant

> I am recommending the "Redder Variant" because we are not using any green Whiterun tundra mods.

## 10.11 [Immersive Fallen Trees](https://www.nexusmods.com/skyrimspecialedition/mods/8767?tab=files) (optional)

### Download Instructions

* **Main File** – Immersive Fallen Trees SSE

## 10.12 [Immersive Fallen Trees Patch](https://www.nexusmods.com/skyrimspecialedition/mods/27834?tab=files) (optional)

### Download Instructions

* **Main File** – Immersive Fallen Trees Patch

> Install this mod if you installed Immersive Fallen Trees. Otherwise skip it.

![separator](../Media/separator.png)

# 11. Architecture

## 11.1 [MD's Farmhouses](https://www.nexusmods.com/skyrimspecialedition/mods/32160?tab=files) (optional)

### Download Instructions

* **Main File** – MD's Farmhouses - 2K

## 11.2 [The Streets of Whiterun HD](https://www.nexusmods.com/skyrimspecialedition/mods/20396?tab=files) (optional)

### Download Instructions

* **Main Files** – The Streets of Whiterun in HD – 2k Mossier

## 11.3 [Riften in High Definition](https://www.nexusmods.com/skyrimspecialedition/mods/20296?tab=files) (optional)

### Download Instructions

* **Main Files** – Riften in High Definition 2K

## 11.4 [Marvelous Windhelm Gate](https://www.nexusmods.com/skyrimspecialedition/mods/24349?tab=files) (optional)

### Download Instructions

* **Main Files** – Marvelous Windhelm Gate SE 4K

## 11.5 [Windhelm Enhanced – HD Metalwork](https://www.nexusmods.com/skyrim/mods/74830?tab=files) (optional)

### Download Instructions

* **Optional Files** – Windhelm Enhanced Metalwork 2k

### Porting Instructions

* Run the mod through Cathedral Assets Optimizer (**Optimsise SLE Assets**).

## 11.6 [RUSTIC MONUMENTS AND TOMBSTONES](https://www.nexusmods.com/skyrim/mods/68884/?tab=files) (optional)

### Download Instructions

* **Main Files** – RUSTIC MONUMENTS and TOMBSTONES V2.6

### FOMOD Instructions

* **Monument Textures:** 2k
* **Tomb Textures:** 4k
* **Meshes:** SMIM

## 11.7 [HQ Solitude](https://www.nexusmods.com/skyrimspecialedition/mods/23937?tab=files) (optional)

### Download Instructions

* **Main File** – HQ Solitude – 2K
* **Optional File** - 4K Blue Palace Floor

### Additional Instructions

* Delete the following files:
  * `textures\architecture\solitude\sdoorgate01.dds`
  * `textures\architecture\solitude\sdoorgate01_n.dds`

 > The gate retexture included with **Noble Skyrim** looks much better.

## 11.8 [Pfuscher’s Manhole Texture](https://www.nexusmods.com/skyrimspecialedition/mods/19799?tab=files) (optional)

### Download Instructions

* **Main Files** – Super duper manhole

## 11.9 [Skyland – Winterhold](https://www.nexusmods.com/skyrimspecialedition/mods/22757?tab=files) (optional)

### Download Instructions

* **Main Files** – Skyland – Winterhold

## 11.10 [Skyrim 3D Misc – Winterhold Gate](https://www.nexusmods.com/skyrimspecialedition/mods/20829?tab=files) (optional)

### Download Instructions

* **Main Files** – Skyrim 3D Misc – Winterhold Gate

## 11.11 [Skyrim Textures Redone – High Hrothgar](https://www.nexusmods.com/skyrimspecialedition/mods/13621?tab=files) (optional)

### Download Instructions

* **Main Files** – STR – High Hrothgar 2K

## 11.12 [Skyrim 3D High Hrothgar Steps](https://www.nexusmods.com/skyrimspecialedition/mods/19905?tab=files) (optional)

### Download Instructions

* **Main Files** – Skyrim 3D High Hrothgar Steps

## 11.13 [Pilgrim’s Delight – High Hrothgar Shrine Retexture](https://www.nexusmods.com/skyrimspecialedition/mods/3273?tab=files)

### Download Instructions

* **Main Files** – Pilgrim’s Delight

## 11.14 [Skyrim Textures Redone – Skyhaven](https://www.nexusmods.com/skyrimspecialedition/mods/10375?tab=files) (optional)

### Download Instructions

* **Main Files** – STR – SkyHaven 2K

## 11.15 [Spice of Life – Orc Strongholds](https://www.nexusmods.com/skyrimspecialedition/mods/22178?tab=files) (optional)

### Download Instructions

* **Main Files** – Spice of Life – Orc Longhouses

### FOMOD Instructions

* **Core Files:**
  * 2k Textures
* **Optional Extras:**
  * LODs 512

## 11.16 [Sovngarde HD](https://www.nexusmods.com/skyrimspecialedition/mods/15891?tab=files) (optional)

### Download Instructions

* **Main File** – Sovngarde HD 2K

## 11.17 [Dawnguard Fortress Improved](https://www.nexusmods.com/skyrimspecialedition/mods/9221?tab=files) (optional)

### Download Instructions

* **Main File** – Dawnguard Fortress Improved SE v1.0

## 11.18 [Castle Volkihar Reborn](https://www.nexusmods.com/skyrimspecialedition/mods/10729?tab=files) (optional)

### Download Instructions

* **Main File** – CC’s Castle Volkihar Reborn – 2K – 2.0

## 11.19 [Soul Cairn HD](https://www.nexusmods.com/skyrimspecialedition/mods/15481?tab=files) (optional)

### Download Instructions

* **Main File** – Soul Cairn HD 2K

## 11.20 [Arri’s Snow Elf Ruins Retexture](https://www.nexusmods.com/skyrimspecialedition/mods/7292?tab=files) (optional)

### Download Instructions

* **Main File** – SSE 2K Textures

![separator](../Media/separator.png)

# 12. Misc Structures

## 12.1 [Fences of Skyrim](https://www.nexusmods.com/skyrimspecialedition/mods/5664?tab=files) (optional)

### Download Instructions

* **Optional Files** – Fences of Skyrim – Weathered Edition 2K

## 12.2 [Skyrim Landscape Overhaul – Stone Walls](https://www.nexusmods.com/skyrim/mods/76359?tab=files) (optional)

### Download Instructions

* **Main Files** – Skyrim Landscape Overhaul – Stone Walls (All-In-One FOMOD Installer)

### FOMOD Instructions

* **Optionals:**
  * New Ivy
  * ~~ENHANCED LANDSCAPES PATCH~~
  * ~~New Farm Walls Plugin (and Meshes)~~
  * New Terrace Stone Walls
* **Stone Wall Textures:**
  * Texture Variant 2 – Med
* **New Ivy Textures:**
  * Low
* **New Terrace Textures:**
  * Med

### Porting Instructions

* Run the mod through Cathedral Assets Optimizer (**SSE – Optimise SLE Assets**).

### About the mod

While it is optional, I do highly recommend this mod. If you skip it, the new mesh and, more importantly, the new textures from High Poly Project will be used ingame for the stone walls, and they don't look quite as good.

## 12.3 [Skyrim 3D Signs](https://www.nexusmods.com/skyrimspecialedition/mods/21338?tab=files) (optional)

### Download Instructions

* **Main Files** – Skyrim 3D Signs

## 12.4 [SkyFix – HD Blacksmith Signs](https://www.nexusmods.com/skyrimspecialedition/mods/10606?tab=files) (optional)

### Download Instructions

* **Main Files** – SkyFix SE – HD Blacksmith Signs 1.0

## 12.5 [RUSTIC EAST EMPIRE COMPANY SIGNAGE](https://www.nexusmods.com/skyrim/mods/68196?tab=files) (optional)

### Download Instructions

* **Main Files** – RUSTIC EAST EMPIRE COMPANY SIGNAGE – Dark Version

## 12.6 [Ennead – Shadowmarks](https://www.nexusmods.com/skyrimspecialedition/mods/9264?tab=files) (optional)

### Download Instructions

* **Main Files** – Sekmet Shadowmarks 1K

## 12.7 [ElSopa HD – Glorious Dummies](https://www.nexusmods.com/skyrimspecialedition/mods/20865?tab=files) (optional)

### Download Instructions

* **Optional Files** – Desaturated Glorious Dummies

### FOMOD Instructions

* **Resolution:** 2K

## 12.8 [Stunning Statues of Skyrim](https://www.nexusmods.com/skyrimspecialedition/mods/3375?tab=files) (optional)

### Download Instructions

* **Main Files** – SSoS – Installer Fix

### FOMOD Instructions

* **Choose your statues:**
  * Bella Dibella
  * Neat Nocturnal
  * Astonich Azura
  * ~~Terrific Talos~~
  * Ysterical Ysgramor
  * Melancholic Meridia
  * Madness Malacath
  * Wakened Winterhold
  * Clever Clavicus
  * Bucolic Boethiah
  * Necrotic Namira
  * Magnetic Mara
  * Malefic Mehrunes
  * Vehement Vaermina
  * ~~Spicy Skyforge~~
  * Fancy Falmer
  * ~~Sweet Sovngarde~~
* **Bella Dibella:**
  * HD Meshe
  * Dibella 2k
* **Neat Nocturnal:**
  * HD Meshe
  * Nocturnal 2k
* **Astonich Azura:**
  * HD Meshe
  * Azura 2k
* **Ysterical Ysgramor:**
  * HD Meshe
  * Ysgramor 2k
* **Melancholic Meridia:**
  * HD Meshe
  * Meridia white 4k
* **Madness Malacath:**
  * HD Meshe No Glow (for stone texture)
  * Malacath Stone 2k
* **Wakened Winterhold:**
  * HD Meshe
  * Winterhold 4k
* **Clever Clavicus:**
  * HD Meshe Default Mask
  * Clavicus 2k
* **Bucolic Boethiah:**
  * HD Meshe
  * Boethiah 4k
* **Necrotic Namira:**
  * HD Meshe
  * Namira 2k
* **Magnetic Mara:**
  * HD Meshe
  * Mara 2k
* **Malefic Mehrunes:**
  * HD Meshes
  * Mehrunes Green 2k
* **Vehement Vaermina:**
  * HD Meshe
  * Vaermina 4k
* **Fancy Falmer:**
  * HD Meshe
  * Falmer Rusty Copper 4k

## 12.9 [LeanWolf’s Better-Shaped Talos Statue](https://www.nexusmods.com/skyrimspecialedition/mods/4752?tab=files) (optional)

### Download Instructions

* **Main Files** – LeanWolf’s Better-Shaped Talos with Greatsword SE

### FOMOD Instructions

* **Talos Statue:** High-Poly Statue
* **Weapon:** Nord Hero Greatsword
* **Patches:** ~~No Snow Under the Roof~~

## 12.10 [Astral Aspects – Standing Stones](https://www.nexusmods.com/skyrimspecialedition/mods/18098?tab=files) (optional)

### Download Instructions

* **Main Files** – Astral Aspect – 2K – 1.4

![separator](../Media/separator.png)

# 13. Vanilla Locations

## 13.1 [JK’s Cities – Lite](https://www.nexusmods.com/skyrim/mods/71018?tab=files)

### Download Instructions

* **Main Files** – JKs Cities – Lite and SuperLite – Installer – 1.3

### FOMOD Instructions

* **Main:** LITE – Merged
* **Optional:** None
* **JKs Lite - Towns:** ~~Towns - BETA - READ DESCRIPTION ON THE LEFT~~

### Porting Instructions

* Resave **JKs LITE – Cities.esp** in the Creation Kit.

## 13.2 [Arthmoor’s Dawnstar](https://www.nexusmods.com/skyrimspecialedition/mods/13607?tab=files)

### Download Instructions

* **Main File** – Dawnstar

## 13.3 [Arthmoor’s Falkreath](https://www.nexusmods.com/skyrimspecialedition/mods/21266?tab=files)

### Download Instructions

* **Main Files** – Falkreath

## 13.4 [Arthmoor’s Dragon Bridge](https://www.nexusmods.com/skyrimspecialedition/mods/8683?tab=files)

### Download Instructions

* **Main Files** – Dragon Bridge

## 13.5 [Arthmoor’s Ivarstead](https://www.nexusmods.com/skyrimspecialedition/mods/349?tab=files)

### Download Instructions

* **Main Files** – Ivarstead

## 13.6 [Arthmoor’s Rorikstead](https://www.nexusmods.com/skyrimspecialedition/mods/16881?tab=files)

### Download Instructions

* **Main Files** – Rorikstead

## 13.7 [Arthmoor’s Kynesgrove](https://www.nexusmods.com/skyrimspecialedition/mods/351?tab=files)

### Download Instructions

* **Main Files** – Kynesgrove

## 13.8 [Arthmoor’s Karthwasten](https://www.nexusmods.com/skyrimspecialedition/mods/350?tab=files)

### Download Instructions

* **Main Files** – Karthwasten

## 13.9 [Arthmoor’s Darkwater Crossing](https://www.nexusmods.com/skyrimspecialedition/mods/326?tab=files)

### Download Instructions

* **Main Files** – Darkwater Crossing

## 13.10 [Arthmoor’s Shor’s Stone](https://www.nexusmods.com/skyrimspecialedition/mods/354?tab=files)

### Download Instructions

* **Main Files** – Shor’s Stone

## 13.11 [Arthmoor’s Soljund’s Sinkhole](https://www.nexusmods.com/skyrimspecialedition/mods/358?tab=files)

### Download Instructions

* **Main Files** – Soljund’s Sinkhole

## 13.12 [Arthmoor’s Whistling Mine](https://www.nexusmods.com/skyrimspecialedition/mods/367?tab=files)

### Download Instructions

* **Main Files** – Whistling Mine

## 13.13 [Obscure’s College of Winterhold](https://www.nexusmods.com/skyrimspecialedition/mods/20514?tab=files)

### Download Instructions

* **Main Files** – Obscure’s College of Winterhold

### FOMOD Instructions

* **Immersive College NPCs:**
  - Immersive College NPCs Integration
* **Optional Lighting Adjustments:**
  - Recommended Interiors
* **Music Options:**
  - New Music Plus Vanilla Music
* **Other Files:**
  - ~~Hall of Diligence FPS Help~~
* **Recommendations:**
  - Mannequins Stay Put Detected
* **iNeed:**
  * ~~iNeed - Food Water and Sleep~~
  * ~~iNeed - Extended~~
* **Lighting:**
  - ~~Enhanced Lights and FX~~
  - ~~ELFX - Exteriors~~
  - Relighting Skyrim
  - ~~Lanterns of Skyrim II - Tamriel Master Lights~~
* **The Lost Library:**
  - Book Covers Skyrim
  - ~~Book Covers Skyrim - Lost Library~~
  - ~~Legacy of the Dragonborn~~
* **Map Markers:**
  * ~~Atlas Map Markers (port by SlaterMan)~~
  * ~~Atlas Map Markers (port by kryptopyr)~~
  * ~~Map Markers Complete~~
* **Morrowloot:**
  - Morrowloot Miscellania - Item Distribution
* **Quest Mods:**
  - Quests are in Skyrim
* **Sound Mods:**
  - Audio Overhaul
  - ~~Sounds of Skyrim Complete (SE port by Arthmoor)~~
  - ~~Sounds of Skyrim Complete (SE port by tonycubed2)~~
* **Various Mods:**
  - ~~Arcanum - A New Age of Magic~~
  - ~~Artifacts - The Tournament of the Ten Bloods~~
  - ~~BadGremlin's Collection~~
  - Better Dynamic Snow
  - ~~Better Spell Learning~~
  - ~~Black Mage Armor~~
  - ~~Blacksmith Forge Water Fix~~
  - ~~College Modifications~~
  - ~~Cutting Room Floor~~
  - ~~Dynamic Firewood Stacks~~
  - ~~Enlightened College of Winterhold~~
  - ~~Equippable Spell Tomes~~
  - ~~Female Mannequins~~
  - ~~Flora Respawn Fix~~
  - ~~Humans, Mer, and Beastfolk~~
  - ~~Immersive Laundry~~
  - Immersive NPCs
  - ~~Konahrik's Accountrements~~
  - ~~Lootable Wood Piles~~
  - ~~M'rissi's Tails of Troubles~~
  - ~~Mystic Condenser~~
  - Mysticism - A Magic Overhaul
  - ~~Scrollwriting in Skyrim~~
  - ~~Skyrim 3D Trees and Plants~~
  - ~~Snazzy Furniture and Clutter Overhaul~~
  - ~~Spell Crafting in Skyrim~~
  - ~~Spell Research~~
  - ~~Tamrielic Culture~~
  - ~~The Midden - Expanded (Lite)~~
  - The Tools of Kagrenac
  - ~~Viewable Faction Ranks~~
  - WACCF - Armor and Clothing Extension
  - Weapons Armor Clothing and Clutter Fixes 2.0+
* **Readme:**
  * Readme
* **Winterhold City:**
  * ~~Realistic Winterhold~~
  * ~~The Great Cities - Minor Cities and Towns~~
  * ~~The Great City of Winterhold~~
  * ~~The People of Skyrim 2 Full~~
  * ~~The People of Skyrim 2 Partial~~
  * ~~Winterhold Restored 2.x~~
  * ~~Winterhold Restored 2.x - JK's Skyrim Patch Patch~~
* **Arch-Mage's Quarters:**
  * None
* **Asset Patches:**
  - ~~Rudy HQ Misc. for Superior Silverware~~
  - ~~Improved Eyes Complete - Only Default~~
* **Solitude Temple Frescoes:**
  - ~~Solitude Temple Frescoes 2019~~
  - ~~Solitude Temple Frescoes 2019 - ESL Flagged~~
  - ~~Solitude Temple Frescoes 2019 (No Lanters) - ESL Flagged~~

![separator](../Media/separator.png)

# 14. Interiors

## 14.1 [RUSTIC WINDOWS](https://www.nexusmods.com/skyrimspecialedition/mods/1937?tab=files)

### Download Instructions

* **Main Files** – RUSTIC WINDOWS – Special Edition – 2K

## 14.2 [Hall of the Dead - Stained Glass Windows](https://www.nexusmods.com/skyrimspecialedition/mods/30066?tab=files) (optional)

### Download Instructions

* **Main Files** – WiZkiD - Hall of the Dead Stained Glass Windows

## 14.3 [Ennead – Banners](https://www.nexusmods.com/skyrimspecialedition/mods/10564?tab=files) (optional)

### Download Instructions

* **Main Files** – Ennead – Banners 2K
* **Miscellaneous Files** – Ennead Banners – 2K Riften Silver

## 14.4 [PELTAPALOOZA](https://www.nexusmods.com/skyrimspecialedition/mods/5442?tab=files) (optional)

### Download Instructions

* **Main Files** – PELTAPALOOZA Special Edition – FULL

## 14.5 [RUGNAROK](https://www.nexusmods.com/skyrimspecialedition/mods/5436?tab=files) (optional)

### Download Instructions

* **Main Files** – RUGNAROK – Special Edition – 2K

## 14.6 [Medieval Candlehorns and Sconces](https://www.nexusmods.com/skyrimspecialedition/mods/24324?tab=files) (optional)

### Download Instructions

* **Main Files** – Download and install the main file.

### FOMOD Instructions

* **Smoke Effect:** Smoke Effect (STAC Compatible)
* **Lantern:** Version_1

## 14.7 [Skyrim 3D Cooking](https://www.nexusmods.com/skyrimspecialedition/mods/23007?tab=files) (optional)

### Download Instructions

* **Main Files** – Skyrim 3D Cooking

## 14.8 [RUSTIC ALCHEMY AND ENCHANTING TABLES](https://www.nexusmods.com/skyrim/mods/62328?tab=files) (optional)

### Download Instructions

* **Optional Files** – Retex of Revamped Alchemy Lab HD – 2K

## 14.9 [JS Shrines of the Divines](https://www.nexusmods.com/skyrimspecialedition/mods/33394?tab=files) (optional)

### Download Instructions

* **Main Files** – JS Shrines of the Divines SE – 2K

![separator](../Media/separator.png)

# 15. Dungeons

## 15.1 [Underground – A Dungeon Texture Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/14365?tab=files)

### Download Instructions

* **Main Files** – Underground FOMOD

> There is no need to download the Whiterun Tower Fix because regenerating DynDOLOD later on will correct the issue.

### FOMOD Instructions

* **Main Options:**
  * Custom installation
* **Options:**
  * 00 Caves
  * 01 Mines
  * 02 Nordic
  * ~~03 Dwemer~~
  * 04 Imperial
  * 05 Riften
  * 06 Apocrypha

### Additional Instructions

- Delete the following file(s) and/or folder(s):
  - `textures\dlc02\dungeons\apocrypha\apocryphabanner01.dds`
  - `textures\dlc02\dungeons\apocrypha\apocryphabanner01_g.dds`
  - `textures\dlc02\dungeons\apocrypha\apocryphabanner01_n.dds`
  - `textures\dungeons\riften\ratwaywood01.dds`
  - `textures\dungeons\riften\ratwaywood01_n.dds`

## 15.2 [Rudy HQ – Nordic Ruins](https://www.nexusmods.com/skyrimspecialedition/mods/19365?tab=files)

### Download Instructions

* **Main File** - Rudy HQ - Nordic Ruins SE version
* **Optional File** - Chests addon
* **Optional File** - Ruin Levers addon SE version

### Additional Instructions

- Delete the following file(s) and/or folder(s):
  - `meshes\clutter\ruins\ruinscandlesconceoff01.nif`
  - `meshes\clutter\ruins\ruinscandlesconceon01.nif`
  - `meshes\clutter\ruins\ruinscandlesconceon02.nif`
  - `meshes\clutter\ruins\ruinsfloorcandlelampmidoff.nif`
  - `meshes\clutter\ruins\ruinsfloorcandlelampmidoff02.nif`
  - `meshes\clutter\ruins\ruinsfloorcandlelampmidon.nif`
  - `meshes\clutter\ruins\ruinsfloorcandlelampmidon02.nif`
  - `meshes\clutter\ruins\ruinsfloorcandlelampsmoff.nif`
  - `meshes\clutter\ruins\ruinsfloorcandlelampsmoff02.nif`
  - `meshes\clutter\ruins\ruinsfloorcandlelampsmon.nif`
  - `meshes\clutter\ruins\ruinsfloorcandlelampsmon02.nif`
  - `textures\effects\`

## 15.3 [Ice Cave Parallax Improved](https://www.nexusmods.com/skyrimspecialedition/mods/24987?tab=files) (optional)

### Download Instructions

* **Main File** – Ice Cave Parallax Improved 1.4.1

## 15.4 [Gecko’s Dwarven Ruins Textures](https://www.nexusmods.com/skyrimspecialedition/mods/10738?tab=files) (optional)

### Download Instructions

* **Main File** – Gecko’s Dwarven Ruins Textures

## 15.7 [RUSTIC WORD WALLS](https://www.nexusmods.com/skyrim/mods/68561?tab=files) (optional)

### Download Instructions

* **Main File** – RUSTIC WORD WALLS 2K

## 15.9 [4K Nordic Murals ](https://www.nexusmods.com/skyrimspecialedition/mods/32379?tab=files)(optional)

### Download Instructions

* **Main File** – 4K Nordic Murals

## 15.10 [CC’s Enhanced Ore Veins](https://www.nexusmods.com/skyrimspecialedition/mods/1306?tab=files) (optional)

### Download Instructions

* **Main File** – Enhanced Ore Veins – 2K – 7.2

### FOMOD Instructions

* **Stone Color:** Grey
* **Type:** Normal
* **Mined Ores:** Keep Old Ones
* **Ingots:** No new ingots
* **Patches:** Hearthfire
* **Format:** ESL

### Additional Instructions

* Double-click **CC’s Enhanced Ore Veins** in your mod order.
* Switch to the **Filetree** tab.
* Rename the plugin’s file extension:
  * CC’sEnhancedOreVeinsSSE-HearthfirePatch.**esp**

> This is faster than ESL-ifying the ESP version.

## 15.11 [CC's Enhanced Ore Veins - Fixed Iron Ore Cubemap](https://drive.google.com/open?id=14VxEEE08WmlO4fjPzwuUH68K0pmAfYU8) (optional)

### Installation Instructions

* Download **CC's Enhanced Ore Veins - Fixed Iron Ore Cubemap** from Google Drive.
* Move the file to `Your Modding Folder\ARCHIVE\MO2 Downloads`.
* In Mod Organizer 2, press F5 to refresh and the file will appear in your **Downloads** tab.
* Double-click the file to install it as usual.

> Unfortunately the issue persists in the latest version of CC's Enhanced Ore Veins. I uploaded a direct [comparison](https://imgsli.com/MTMyOTE) - before and after installing the fixed cube map.

## 15.12 [Metallurgy – Ingots and Ore HD ](https://www.nexusmods.com/skyrimspecialedition/mods/30738?tab=files)(optional)

### Download Instructions

* **Main File** – Metallurgy – Ingots and Ore HD 1K (LOOSE)

## 15.13 [Ancient Pottery](https://www.nexusmods.com/skyrimspecialedition/mods/24039?tab=files) (optional)

### Download Instructions

* **Main File** – Ancient Pottery

## 15.14 [ElSopa HD – Realistic Dark Elf Urns](https://www.nexusmods.com/skyrimspecialedition/mods/21717?tab=files) (optional)

### Download Instructions

* **Main File** – HD Dark Elf Urns 2k

## 15.15 [Ancient Dwemer Metal](https://www.nexusmods.com/skyrim/mods/75610?tab=files) (optional)

### Download Instructions

* **Main File** - Ancient Dwemer Metal 2K

## 15.16 [HD Lava for Dawnguard](https://www.nexusmods.com/skyrimspecialedition/mods/7285?tab=files) (optional)

### Download Instructions

* **Main File** - HD Lava (4k)

![separator](../Media/separator.png)

# 16. Clutter

## 16.1 [Forgotten Retex Project](https://www.nexusmods.com/skyrimspecialedition/mods/7849?tab=files)

### Download Instructions

* **Main Files** – Forgotten Retex Project

### FOMOD Instructions

* **Optional Files:** Draw Knife – with Carvings
* **Optional Files:** Silver Mold – with Silver Frame

### Additional Instructions

* Delete the following file(s) and/or folder(s):
  * `meshes\clutter\deadanimals\salmonmeat01.nif`
  * `meshes\clutter\food\cookedsalmonsteak01.nif`
  * `meshes\clutter\ingredients\beefmeatcooked.nif`
  * `meshes\clutter\ingredients\pie01.nif`
  * `meshes\clutter\kitchen\`
  * `meshes\furniture\blacksmithforgemarker.nif`
  * `meshes\furniture\blacksmithforgemarkerwr.nif`
  * `meshes\furniture\blacksmithingskyforgemarker.nif`

> The first five meshes conflict with and overwrite the arguably superior ones from Skyrim 3D Cooking.
> The final three meshes overwrite Embers HD and prevent its forge textures from being applied.

## 16.2 [Aetherial Crown by Saerileth – Plugin Replacer](https://www.nexusmods.com/skyrimspecialedition/mods/23631?tab=files)

### Download Instructions

* **Main Files** – Aetherial Crown – Plugin Replacer

> The original mod is not required because the textures are included in Forgotten Retex Project.

## 16.3 [Skyrim 3D Misc](https://www.nexusmods.com/skyrimspecialedition/mods/20829?tab=files) (optional)

### Download Instructions

* **Main Files** – Skyrim 3D Misc – Giant Mortar and Pestle
* **Main Files** – Skyrim 3D Misc – Mammoth Cheese
* **Main Files** – Skyrim 3D Misc – Markarth Cage
* **Main Files** – Skyrim 3D Misc – Tanning Rack
* **Main Files** – Skyrim 3D Misc – Traps

## 16.4 [RUSTIC CLUTTER COLLECTION](https://www.nexusmods.com/skyrimspecialedition/mods/5795?tab=files) (optional)

### Download Instructions

* **Main Files** – RUSTIC CLUTTER COLLECTION – Special Edition – 2K

## 16.5 [Rudy HQ – Miscellaneous](https://www.nexusmods.com/skyrimspecialedition/mods/19867?tab=files) (optional)

### Download Instructions

* **Main Files** – Rudy HQ – Misc SE – The Rest

## 16.6 [Frankly HD Dragon Bones](https://www.nexusmods.com/skyrimspecialedition/mods/25099?tab=files) (optional)

### Download Instructions

* **Main Files** – Frankly HD Dragonbones 4k-2k

## 16.7 [Medieval Silverworks](https://www.nexusmods.com/skyrimspecialedition/mods/23938?tab=files) (optional)

### Download Instructions

* **Main Files** – Medieval Silverworks
* **Miscellaneous Files** – Medieval Silverworks STAC Patch

## 16.8 [Book Covers Skyrim (BCS)](https://www.nexusmods.com/skyrimspecialedition/mods/901?tab=files)

### Download Instructions

* **Main Files** – Book Covers Skyrim SE – Desaturated

## 16.9 [Realistic Paper](https://www.nexusmods.com/skyrim/mods/937?tab=files) (optional)

### Download Instructions

* **Main Files** – Realistic Paper MAIN

### Additional Instructions

* Delete the following file:
  * `textures\clutter\books\largebookpaper01.dds`

> A much better texture is included with Book Covers Skyrim.

## 16.10 [MAPS](https://www.nexusmods.com/skyrim/mods/66819?tab=files) (optional)

### Download Instructions

* **Main Files** – MAPS 2K

## 16.11 [Business Ledger HD Retexture](https://www.nexusmods.com/skyrim/mods/38389?tab=files) (optional)

### Download Instructions

* **Main Files** – Business Ledger HD Retexture

## 16.12 [JS Dragon Claws ](https://www.nexusmods.com/skyrimspecialedition/mods/1394?tab=files)(optional)

### Download Instructions

* **Main Files** – 1k Textures

## 16.13 [JS Dragon Claws – Patches](https://www.nexusmods.com/skyrimspecialedition/mods/23833?tab=files) (optional)

### Download Instructions

* **Main Files** – JS Dragon Claws – Amethyst Patch

> Only install this mods if you installed **JS Dragon Claws**. Otherwise skip it.

## 16.14 [RUSTIC SOULGEMS](https://www.nexusmods.com/skyrimspecialedition/mods/5785?tab=files)

### Download Instructions

* **Main Files** – RUSTIC SOULGEMS – Special Edition – FOMOD – English Only

### FOMOD Instructions

* **Texture Resolution:**
  * 1k Textures
* **Plugin:**
  * Sorted + ESL + GIST Patch

## 16.15 [RUSTIC AZURAS STAR](https://www.nexusmods.com/skyrimspecialedition/mods/18345) (optional)

### Download Instructions

* **Main Files** – RUSTIC AZURA’S STAR – SSE – 2K

## 16.16 [ElSopa HD – Meridia’s Beacon](https://www.nexusmods.com/skyrimspecialedition/mods/22046) (optional)

### Download Instructions

* **Main Files** – 1K HD Meridias Beacon

## 16.17 [RUSTIC ELDERSCROLL](https://www.nexusmods.com/skyrimspecialedition/mods/17757) (optional)

### Download Instructions

* **Main Files** – RUSTIC ELDERSCROLL – Special Edition – 2K
* **Optional Files** – ELDERSCROLL SSE – FX – 1K

## 16.18 [RUSTIC ANIMATED POTIONS AND POISONS](https://www.nexusmods.com/skyrimspecialedition/mods/2276/) (optional)

### Download Instructions

* **Main Files** – RUSTIC ANIMATED POTIONS and POISONS 1K
* **Update Files** – SSE Meshes

## 16.19 [Rally's Werewolf Totems](https://www.nexusmods.com/skyrimspecialedition/mods/28882) (optional)

### Download Instructions

* **Main Files** – Rallys Werewolf Totems HQ 2K-1K

## 16.20 [BLOODSTONE CHALICE REBORN](https://www.nexusmods.com/skyrim/mods/63551/) (optional)

### Download Instructions

* **Main Files** – BLOODSTONE CHALICE REBORN 1K

![separator](../Media/separator.png)

# 17. Food & Ingredients

## 17.1 [High Quality Food and Ingredients SE](https://www.nexusmods.com/skyrimspecialedition/mods/10897?tab=files) (optional)

### Download Instructions

* **Main Files** – High Quality Food And Ingredients SE

### FOMOD Instructions

* **Select One:**
  * Custom
* **Options:**
  * Baked Potatoes
  * ~~Boiled Creme Treat~~
  * ~~Bone Meal~~
  * ~~Bread~~
  * ~~Cabbage~~
  * Carrots
  * Charred Skeever Hide and Meat
  * Chicken Breast
  * ~~Chicken~~
  * Cooked Beef
  * Dead Hare
  * Dead Pheasant
  * Eider Cheese
  * ~~Garlic~~
  * Goat Cheese
  * ~~Green Apple~~
  * Grilled Chicken Breast
  * Grilled Leaks
  * Honey Nut Treat
  * Long Taffy Treat
  * ~~Mead~~
  * ~~Moon Sugar~~
  * ~~Mora Tapinella~~
  * ~~Pie~~
  * ~~Potatoes~~
  * ~~Powdered Mannoth Tusk~~
  * ~~Raw Beef~~
  * ~~Red Apples~~
  * Salmon Meat
  * Salmon
  * Salmon Steak
  * ~~Salt Pile~~
  * ~~Scaly Photiota~~
  * Seared Slaugterfish
  * Slaughterfish Scales
  * ~~Sweet Roll~~
  * Venison Chop
  * Venison
  * ~~Void Salts~~

## 17.2 [Medieval Spirits](https://www.nexusmods.com/skyrimspecialedition/mods/24243?tab=files) (optional)

### Download Instructions

* **Main Files** – Medieval Spirits

## 17.3 [Boiled Creme Treat Sweet Roll and Pie](https://www.nexusmods.com/skyrimspecialedition/mods/9034?tab=files) (optional)

### Download Instructions

* **Main Files** – Sweet Roll Boiled Creme Treat and Pie
* **Optional Files** – MeatPie

> The optional file retextures meat pies added by the USSEP which are not in fact vanilla food items.

## 17.4 [Honey Pot](https://www.nexusmods.com/skyrimspecialedition/mods/3036?tab=files) (optional)

### Download Instructions

* **Main Files** – Honey pot 1.3b Special Edition

### FOMOD Instructions

* **Core:** Honey dripped mesh
* **Texture size:** 1k Texture

## 17.5 [HD Sabre Cat Tooth](https://www.nexusmods.com/skyrimspecialedition/mods/9640?tab=files) (optional)

### Download Instructions

* **Main Files** – Main File 1.0 (fixed normals thanks to renthal311 )

## 17.6 [Falmer Ear and Hagraven Claw](https://www.nexusmods.com/skyrim/mods/74792?tab=files) (optional)

### Download Instructions

* **Main Files** – Hagraven Claw
* **Optional Files** – Falmer Ear 512

## 17.7 [ElSopa HD – Briar Heart](https://www.nexusmods.com/skyrimspecialedition/mods/27983?tab=files) (optional)

### Download Instructions

* **Main Files** – ElSopa HD – Briarheart Red 512

![separator](../Media/separator.png)

# 18. Clothes & Jewellery

## 18.1 [RUSTIC CLOTHING](https://www.nexusmods.com/skyrimspecialedition/mods/4703?tab=files)

### Download Instructions

* **Main Files** – RUSTIC CLOTHING – Special Edition – 2K

## 18.2 [Prince and the Pauper](https://www.nexusmods.com/skyrimspecialedition/mods/8354?tab=files)

### Download Instructions

* **Main Files** – Prince and the Pauper SE 4.1

### FOMOD Instructions

* **Texture Options:** Rustic Clothing

## 18.3 [Gemling Queen Jewelry](https://www.nexusmods.com/skyrimspecialedition/mods/4294?tab=files) (optional)

### Download Instructions

* **Main Files** – Gemling Queen Jewelry SE

### FOMOD Instructions

* **Main Modules:**
  * Amulets
  * ~~Circlets~~
  * Rings
* **DLC Addons:**
  * Dawnguard Addon
  * Dawnguard Addon – Unobtainable Items
* **Amulet Textures:**
  * Gamwich Amulet Textures – 512
* **Ring Texture Options:**
  * Gamwich Ring Textures – Combined – 1k
* **Optional Mesh Packs:**
  * None
* **Optional Mesh Packs Dawnguard:**
  * ~~Vampire Beast Blood Ring Left Hand~~

### FOMOD Instructions

The plugin contains one unnecessary edit to a scroll that can potentially conflict with other mods. We will delete the change.

* Run **SSEEdit** through Mod Organizer 2.
* Click **OK** in the plugin selection window to load all your mods.
* Wait until SSEEdit returns `Background loader: finished`.
* Find and double-click **GQJ_DG_vampireamuletfix.esp** in the left pane to expand the plugin.
* Right-click **Scroll** and select **Remove**.
* Close SSEEdit and click **OK** to save your changes.

![Gemling Queen Jewelry - Delete Records in xEdit](..\Pictures\Mod Installation\Gemling Queen Jewelry - Delete Records in xEdit.png)

## 18.4 [JS Circlet Replacer](https://www.nexusmods.com/skyrimspecialedition/mods/8686?tab=files) (optional)

### Download Instructions

* **Main Files** – JS Circlet Replacer

### Additional Instructions

* Downsize the mod’s textures with Cathedral Assets Optimizer (**SSE – Downsize Textures**).

## 18.5 [The Divine Amulets Retexture](https://www.nexusmods.com/skyrim/mods/31731?tab=files) (optional)

### Download Instructions

* **Optional Files** – The Divine Amulets Retexture – Dragonborn Amulets Final Version

### Additional Instructions

* Delete the following file(s) and/or folder(s):
  * `textures\dlc02\armor\amulets\eastempirecompany\`

## 18.6 [Better Looking Amulets](https://www.nexusmods.com/skyrimspecialedition/mods/10893?tab=files) (optional)

### Download Instructions

* **Main Files** – Better Looking Amulets

## 18.7 [ElSopa HD – Akatosh Amulet](https://www.nexusmods.com/skyrimspecialedition/mods/24092?tab=files) (optional)

### Download Instructions

* **Main Files** – ElSopa HD – Akatosh Amulet 512

## 18.8 [ElSopa HD – Bonehawk Amulet](https://www.nexusmods.com/skyrimspecialedition/mods/21862?tab=files) (optional)

### Download Instructions

* **Main Files** – HS Bonehawk Amulet

## 18.9 [JS Barenziah](https://www.nexusmods.com/skyrimspecialedition/mods/22990?tab=files) (optional)

### Download Instructions

* **Main Files** – JS Barenziah SE – 2K Textures

### Additional Instructions

* Delete the following file(s) and/or folder(s):
  * `JS Barenziah SE – Johnskyrim.esp`

### About the mod

 A similarly beautiful retexture of Barenziah’s Crown and the stones (made by Gamwich and Saerileth) is already included in Forgotten Retex Project. You can find screenshots of it [here on its original mod page](https://www.nexusmods.com/skyrim/mods/63902). Skip JS Barenziah if you prefer Gamwich and Saerileth’s retexture which you already have installed.

 ![separator](../Media/separator.png)

 # 19. Weapons & Armour

## 19.1 [RUSTIC ARMOR AND WEAPONS (RAW)](https://www.nexusmods.com/skyrimspecialedition/mods/19666?tab=files) (optional)

### Download Instructions

* **Main Files:** RAW SSE 2K

## 19.2 [Practical Female Armors](https://www.nexusmods.com/skyrimspecialedition/mods/2628?tab=files) (optional)

### Download Instructions

* **Main Files:** Practical Female Armors SE – All-In-One Installer – NMM BAIN

### FOMOD Instructions

* **Skyrim:**
  * Steel Plate Armor
  * Elven Light Armor
  * Elven Armor
  * Glass Armor
  * ~~Dragon Scale Armor~~
  * ~~Orcish Armor~~
  * Ebony Armor
  * Ebony Mail
  * ~~Dragon Plate Armor~~
  * ~~Ancient Nord Armor~~
  * ~~Stormcloak Officer Armor~~
  * Wolf Armor
  * ~~Imperial Heavy Armor~~
* **Dawnguard:**
  * ~~Vampire Armor~~
* **Dragonborn:**
  * Chitin Heavy Armor
  * Nordic Carved Armor
* **Compatibility Patches:**
  * ~~aMidianBorn Glass Variants~~
  * ~~aMidianBorn Differently Ebony~~
  * ~~Gilded Nordic Carved Armor~~
  * ~~Bodyslide Presets~~
  * ~~Ebony Armor Edit~~
  * ~~aMidianBorn Content Addon~~
  * ~~Sleeved Imperials~~

## 19.3 [Warmth – Light Armor Replacer](https://www.nexusmods.com/skyrimspecialedition/mods/2959?tab=files) (optional)

### Download Instructions

* **Main Files:** Warmth – Light Armor Replacer

### FOMOD Instructions

* **Main:** Replace all armours.

> There is no need to select the individual options at the bottom.

## 19.4 [aMidianBorn of Silence – Armors](https://www.nexusmods.com/skyrim/mods/24909?tab=files)

### Download Instructions

* **Main Files:** aMidianBorn book of silence_ARMORS

### FOMOD Instructions

* **Options:** Custom
* **Iron and Banded:** Iron – White Fur
* **Steel:** Steel
* **Steel Plate:** Steel Plate
* **Leather:** Leather
* **Hide and Studded:** Hide
* **Fur:** Fur
* **Elven:** Elven – None
* **Dwarven:** ~~Dwarven~~
* **Ancient Nord:** Ancient Nord
* **Orcish:** Orcish – Brighter
* **Scaled:** Scaled – Brighter
* **Wolf:** Wolf – Brown Fur
* **Glass:** Glass – None
* **Ebony:** Ebony – None
* **Blades:** Blades
* **Falmer:** Falmer

> The Elven, Glass and Ebony options are skipped as they will be covered by the aMidianBorn Book of Silence – Content Addon later on.

## 19.5 [aMidianBorn Blade Armor SSE Patch](https://www.nexusmods.com/skyrimspecialedition/mods/12963?tab=files)

### Download Instructions

* **Main Files:** aMidianBorn Blades Armor SSE Patch

## 19.6 [aMidianBorn Book of Silence – Weapons](https://www.nexusmods.com/skyrim/mods/24909?tab=files)

### Download Instructions

* **Main Files:** aMidianBorn book of silence_WEAPONS

### FOMOD Instructions

* **Options:**
  * Custom
* **Weapons:**
  * Draugr
  * ~~Dwarven~~
  * Iron
  * Orcish
  * ~~Silver~~
  * ~~Skyforge~~
  * Staves
  * Steel

### Additional Instructions

- Delete the following file(s) and/or folder(s):
  - `meshes\`

> The meshes folder is completely empty but will cause MO2 to display that the mod contains meshes which may be confusing.

## 19.7 [Frankly HD Silver Sword](https://www.nexusmods.com/skyrim/mods/29563?tab=files)

### Download Instructions

* **Optional Files:** UHSS – Main File Mid Res – 2k

> No optimisation necessary as all meshes will be overwritten by the next mod.

## 19.8 [LeanWolf’s Better-Shaped Weapons](https://www.nexusmods.com/skyrimspecialedition/mods/2017?tab=files)

### Download Instructions

* **Main Files:** LeanWolfs Better-Shaped Weapons Installer v2.1.03 SE

### FOMOD Instructions

- **All or Custom:**
  - Install everything (default)
- **Sheath Options:**
  - Onehanded Sheaths
  - Greatsword Sheaths
- **Variants and Patches:**
  - FrankFamily HD Imperial Armor and Weapons
  - FrankFamily Ultra HD Silver Sword
  - ~~Scimitar Bling~~
  - Keening with Refraction
  - ~~Runed Nord Hero Weapons~~
- **Glass Refraction Options:**
  - No Refraction
- **Stalhrim Refraction Options:**
  - No Refraction
- **Dawnbreaker:**
  - Dawnbreaker Sheath Elf
- **Dawnbreaker ENB Option:**
  - Dawnbreaker for ENB
- **Dragonbone Options:**
  - DragonBoring Weapons
- **Left-hand Meshes:**
  - No Dual Sheath

## 19.9 [Open Face Guard Helmets](https://www.nexusmods.com/skyrimspecialedition/mods/13943?tab=files) (optional)

### Download Instructions

* **Main Files:** Open Face Guard Helmets

## 19.10 [Open Face Guard Helmets – Plugin Replacer](https://www.nexusmods.com/skyrimspecialedition/mods/26092?tab=files) (optional)

### Download Instructions

* **Main Files:** Open Face Guard Helmets – Replacer Plugin

> Install this mod if you installed Open Face Guard Helmets. Otherwise skip it.

## 19.11 [Frankly HD Stormcloaks and City Guards](https://www.nexusmods.com/skyrim/mods/42404?tab=files) (optional)

### Download Instructions

* **Main Files:** UltraHD – Stormcloak and City Guards 2K version
* **Optional Files:** Fix by SpriterSan for 2k version --- `merge with the main file`

## 19.12 [aMidianBorn Stormcloak Officer Armour](https://www.nexusmods.com/skyrim/mods/45692?tab=files) (optional)

### Download Instructions

* **Main Files:** aMidianBorn Stormcloak officer

## 19.13 [Frankly HD Imperial Armor and Weapons](https://www.nexusmods.com/skyrimspecialedition/mods/20848?tab=files)

### Download Instructions

* **Main Files:** Frankly HD Imperial Armor And Weapons 2k
* **Optional Files:** Frankly HD Imperial Armor And Weapons – Sleeves and Pants Edition

### Additional Instructions

- Delete the following file(s) and/or folder(s):
  - `meshes\weapons\`

## 19.14 [Frankly HD Dawnguard Armor and Weapons](https://www.nexusmods.com/skyrimspecialedition/mods/19663?tab=files) (optional)

### Download Instructions

* **Main Files:** FranklyHD Dawnguard Armor and Weapons
* **Optional Files:** Frankly HD Dawnguard Armor CBBE SE

### FOMOD Instructions

* **Texture Resolution:** 2K Resolution

## 19.15 [Iron Things](https://www.nexusmods.com/skyrimspecialedition/mods/26947?tab=files) (optional)

### Download Instructions

* **Main Files:** Iron Things SE 1.2

### Additional Instructions

**This is optional.**

Personally I prefer aMidianBorn’s retextures for the iron weapons for consistency’s sake, but I do like the Iron Things bow retexture (Imperial Bow) very much. The main file of Iron Things contains a fixed mesh for the bow. To use only the bow, follow the instructions below.

* Delete the following file(s) and/or folder(s):
  * `meshes\armor\`
  * `meshes\weapons\iron\1stpersonironbattleaxe.nif`
  * `meshes\weapons\iron\1stpersonironclaymore.nif`
  * `meshes\weapons\iron\1stpersonirondagger.nif`
  * `meshes\weapons\iron\1stpersonlongsword.nif`
  * `meshes\weapons\iron\ironbattleaxe.nif`
  * `meshes\weapons\iron\ironclaymore.nif`
  * `meshes\weapons\iron\irondagger.nif`
  * `meshes\weapons\iron\longsword.nif`

> There is no need to delete the textures as well. They are in a custom directory that will only be accessed by the mod’s meshes and won’t overwrite any vanilla files or other retextures.

## 19.16 [Elven Weapons for Silence ](https://www.nexusmods.com/skyrimspecialedition/mods/27994?tab=files)(optional)

### Download Instructions

* **Optional Files:** Leanwolf Elven – Default Silver

## 19.17 [CC’s HD Dwemer Weapons and Armor ](https://www.nexusmods.com/skyrimspecialedition/mods/32384?tab=files)(optional)

### Download Instructions

* **Main Files:** CC’s HD Dwemer Weapons and Armor – 2K – 1.0

## 19.18 [Frankly HD Thieves Guild Armor](https://www.nexusmods.com/skyrimspecialedition/mods/19953?tab=files) (optional)

### Download Instructions

* **Main Files:** Frankly HD Thieves Guild Armors

### FOMOD Instructions

* **Texture Resolution:** 2K Resolution

## 19.19 [Frankly HD Shrouded Armor](https://www.nexusmods.com/skyrimspecialedition/mods/18785?tab=files) (optional)

### Download Instructions

* **Main Files:** Frankly HD Shrouded Armor _ 1.1

### FOMOD Instructions

* **Texture Resolution:** 2K Resolution
* **Options:** ~~Oblivion Style~~

## 19.20 [Falmer Weapons for aMidianBorn Book of Silence](https://www.nexusmods.com/skyrim/mods/83950?tab=files) (optional)

### Download Instructions

* **Main Files:** falmerweapons4BoS

## 19.21 [Outlandish Stalhrim](https://www.nexusmods.com/skyrimspecialedition/mods/19562?tab=files) (optional)

### Download Instructions

* **Main Files:** Outlandish Stalhrim SSE
* **Optional Files:** Outlandish Stalhrim SSE – Better Shaped Weapons Patch

> If you want the vanilla blue colour back for Stalhrim armor, download the **Blue Cubemap** file from the Miscellaneous section.

## 19.22 [Outlandish Chitin Armour](https://www.nexusmods.com/skyrim/mods/70681?tab=files) (optional)

### Download Instructions

* **Main Files:** Outlandish Chitin Armour

## 19.23 [Ebony Weapons 2017 Retexture ](https://www.nexusmods.com/skyrimspecialedition/mods/30029?tab=files)(optional)

### Download Instructions

* **Main Files:** Special Ebony Shiny Reflective Refractive Reshlective 2k 4k 5k 144Hz Immersive Overhaul Retexture Pack Collection Suite

## 19.24 [Frankly HD Dragonbone and Dragonscale](https://www.nexusmods.com/skyrimspecialedition/mods/25110?tab=files) (optional)

### Download Instructions

* **Main Files:** Frankly HD Dragonbone and Dragonscale 2k
* **Optional Files:** Frankly HD Dragonbone and Dragonscale - Mesh patch --- `merge with the main file`

## 19.25 [Sunhallowed and Bloodcursed Arrows – HD Retexture](https://www.nexusmods.com/skyrim/mods/58118?tab=files)

### Download Instructions

* **Optional Files:** bloodcursed arrows 1k
* **Optional Files:** Sunhallowed arrows 1k

------

### Porting Instructions

* Run **Sunhallowed Arrows** through Cathedral Assets Optimizer (**SSE – Optimise SLE Assets**).

## 19.26 [Dragon Priest Weapons Improved](https://www.nexusmods.com/skyrim/mods/60075?tab=files) (optional)

### Download Instructions

* **Main Files:** Dragon Priest Weapon Improved
* **Update Files:** Quick Update --- `merge with the main file`

### Porting Instructions

* Run the mod through SSE NIF Optimizer.

> Processing the meshes with CAO results in the staff 3rd person mesh being invisble ingame. Not processing causes the dagger 1st and 3rd person meshes to be invisible. Only SSE NIF Optimizer reliable fixes all meshes.