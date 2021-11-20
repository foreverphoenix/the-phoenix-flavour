---
title: "Gameplay"
weight: 4
type: docs
description: >
  WTP's important changes and additions.
---

## Visual Changes

Fallout 4 was never a particularly beautiful game, but it has solid graphics. Compared to older Fallout titles, it is a great deal more colourful and "cartoonish", no green filter like in Fallout 3 and no distinct dusty hue like in Fallout New Vegas.

In my changes for WTP, I have decided to stay faithful to the vanilla colours and style, opting to focus largely on improving texture quality. Any more profound changes such as a tree overhaul would have susbstantially increased the list's complexity due to FO4's precombine system which is the only thing that keeps performance from turning into a slide show.

### Weather & Lighting

Welcome to Paradise does not feature a fully-fledged weather overhaul, but it does include the popular [True Storms](https://www.nexusmods.com/fallout4/mods/4472) by fadingsignal to improve the various rain, dust, and rad storm variations that haunt the Commonwealth. You can view fadingsignal's own video showcase of his mod [here](https://www.youtube.com/watch?v=InJwn_Y71n8).

![Misty Rain](/Pictures/wtp/documentation/misty-rain.jpg)

I paired True Storms with [True Nights](https://www.nexusmods.com/fallout4/mods/9253) which gives nights in the Commonwealth an incredibly murky, moody atmosphere. Nights are darker than vanilla so remember to use your Pip-Boy flashlight which can be activated by pressing and holding the Pip-Boy button (TAB by default). However, nights should not be pitch-black (if they are, you may need to check your monitor configuration.)

Finally, I added the beautiful [Subtle ENB](https://www.nexusmods.com/fallout4/mods/5885) which looks particularly amazing with True Storms and True Nights, but does not majorly impact performance or deviate from the original look. I disabled the depth of field (DOF) effect so you don't blurred / out of focus during conversations. DOF is often not practical for gameplay in general.

![Diner At Night](/Pictures/wtp/documentation/diner-at-night.jpg)

### Landscape & Textures

In keeping with the pledge to stick with the vanilla style, I added [Lush Landscapes](https://www.nexusmods.com/fallout4/mods/9292) (the "Dried" edition) as the grass overhaul which does a good job at improving vanilla's sparse vegetation. Water was greatly improved by [Water Enhancement Textures](https://www.nexusmods.com/fallout4/mods/20775) and [Wave Animation Vanilla Enhanced](https://www.nexusmods.com/fallout4/mods/41568). With [Vehicle Overhaul](https://www.nexusmods.com/fallout4/mods/18732) you will find a greater variety of pre-war cars and trucks around Boston.

As for textures, Fallout 4 is limited in that it greatly favours files packed in BA2s (basically ZIP archives for the Creation Engine). A large amount of loose textures will noticably impact not only load times but also ingame performance. On the other hand, higher resolution textures are among the best visual improvements this game can receive.

For WTP, I created five separate texture packs: Clutter, Apparel, Power Armors, Weapons, and Creatures. These include textures (and occasionally meshes and/or material files) by various amazing authors, neatly packed up so as not to ruin performance. These repacks are NOT redistributed with WTP. Wabbajack will download them from the original Nexus page for you and recreate the BA2s from my setup locally on your PC.

You can find the full list of retextures featured in WTP [here](/wtp/wtp-resources/texture-packs/).

## Gameplay Changes

### Quality of Life

- [Start Me Up](https://www.nexusmods.com/fallout4/mods/18946): The Basic version of this mod included in WTP allows you to skip the pre-war part of the Prologue.
- [Simple Wait Anywhere](https://www.nexusmods.com/fallout4/mods/55597): You only need to be out of combat to open the Wait menu. Sitting is no longer required.
- [Automatically Lowered Weapons](https://www.nexusmods.com/fallout4/mods/20093): Player automatically lowers their weapon when not in combat.

### Quest Adjustments

[No Quest Autostart series](https://www.nexusmods.com/fallout4/users/2652197?tab=user+files): The DLC quests will no longer start automatically upon reaching the required level. You will need to either listen to the associated radio broadcast or actively go to the related location. Note that the level requirements was not removed, but the quests will no longer be automatically added to your quest log.

[Keep Radiants in the Commonwealth](https://www.nexusmods.com/fallout4/mods/25934): Any radiant quests received in the Commonwealth will now always send you to locations within the Commonwealth (as opposed to DLC areas which they previously could).

[Preston Garvey No Radiant Settlement Quests](https://www.nexusmods.com/fallout4/mods/24940): After taking the Castle for the Minutemen, Preston Garvey will no longer give you radiant quests with the exception of those that you cannot get through the Radio Freedom broadcasts.

[Whose Quest Is It Anyway](https://www.nexusmods.com/fallout4/mods/51979): Upon attempting to remove a quest item from your inventory, you will now be notified which quest the item is locked by.

### Photo Mode

WTP includes the amazing [Photo Mode](https://www.nexusmods.com/fallout4/mods/49997) by reg2k. It's the perfect tool for screenarchers, pause the game and find the perfect angle for a great picture. You can access it through ESCAPE menu or define a hotkey in the associated MCM (**P** by default).

## Power Armor

While WTP touches little on the gameplay side of things, I did change how power armors were distributed and how their paint jobs work to be quite different from vanilla.

### Distribution

Quick summary of the changes:

- You will find fewer full power armors sets and more separate pieces.
- T-45 and Raider power armor pieces will be more commonly found.
- T-51 power armor pieces will be more commonly found.
- T-60 power armor pieces can be found exclusively on Brotherhood troops.
- X-01 power armor pieces are rare. There are only two full sets in the Commonwealth.

In vanilla, one may be forgiven to think that before the bombs dropped every citizen of Boston had a set of power armor stored in their backyard. There are just so bloody many of them! In order to cut down the amount of armors you find, I added [Some Assembly Required](https://www.nexusmods.com/fallout4/mods/12050) for its hand-placed power armor pieces (and removed everything else it did). In most locations where before there was a power armor frame often with a full set, you will now find separate pieces or other rare loot. Additionally, pieces of Raider, T-45, or (rarely) T-51 power armor were hand-placed in various locations around the Commonwealth.

Since this change means there will be far fewer frames found in the world, I added [Restore Power Armor Frames](https://www.nexusmods.com/fallout4/mods/20890) which will allow you to extract the frames from dead NPCs.

According to lore, **T-60 power armor** had not yet replaced the T-51 in the standard army loadout before the bombs dropped and did not enter mass-production until the Brotherhood of Steel procured the means to do so much later on. As such it makes no sense for T-60 sets to be significantly more common than T-51 in the Commonwealth. In WTP, T-60 sets are given exclusively to Brotherhood troops. Atom Cats now wear T-45 power armor sets instead of T-60. The only T-60 set you can find outside of the Brotherhood is the [Tesla](https://fallout.fandom.com/wiki/Tesla_T-60_armor) variant from the Automatron DLC.

There is one full set of T-51 power armor including frame and fusion core in a heavily fortified location. See the SPOILER SECTION at the bottom if you want to know where to find it.

In the levelled lists, T-60 pieces were replaced by T-45 pieces and X-01 pieces were replaced by T-51 pieces.

As for **X-01 power armor**, there are only two full sets to be found: One of them is the [Quantum X-01](https://fallout.fandom.com/wiki/Quantum_X-01_power_armor) from the Nuka World DLC. The second consists of regular X-01 pieces you will have to gather from various locations around the Commonwealth. Scroll to the bottom of this page to the SPOILER SECTION to find out where exactly those six pieces can be found.

### Paint Jobs

In vanilla, many paint jobs also have non-cosmetic effects such as stat increases. The mod [Power Armor Materials AND Paints](https://www.nexusmods.com/fallout4/mods/4619) separates these two so you can control the paint job and "material" (the non-cosmetic buffs) separately. This required some integration patching with other power armor mods added in WTP.

Paint jobs now all cost 2 oil and 2 steel to apply (matching the Creation Club paint jobs). They no longer increase weight or value of the armor piece and will not yield a loose mod upon swapping to a different one.

Additionally, paint jobs were made available for a greater variety of power armor pieces by [Consistent Power Armor Overhaul](https://www.nexusmods.com/fallout4/mods/11234) and [Minutemen Paint Job](https://www.nexusmods.com/fallout4/mods/28029). Both of those mods are supported by the amazing [Power Armors Redone Extended](https://www.nexusmods.com/fallout4/mods/28033) so the new paint job variants are of the same style and quality as the vanilla power armors retextured by [Power Armors Redone](https://www.nexusmods.com/fallout4/mods/27917).

| Paint Jobs           | T-45 | T-51 | T-60 | X-01 |
| -------------------- | ---- | ---- | ---- | ---- |
| Factory              | x    | x    | x    | x    |
| Winterized (white)   | x    | x    | x    | x    |
| Military (olive)     | x    | x    | x    | x    |
| Brotherhood of Steel | x    | x    | x    | x    |
| Minutemen            | x    | x    | x    | x    |
| Vault-Tec            | x    | x    | x    | x    |
| Railroad             | -    | x    | -    | -    |
| Institute            | -    | -    | -    | x    |
| Atom Cats            | x    | x    | x    | x    |
| Hot Rod Flames       | x    | x    | x    | x    |
| Hot Rod Shark        | x    | x    | x    | x    |
| Hot Rod Hot Pink     | x    | x    | x    | x    |
| Vim!                 | -    | x    | -    | -    |
| Vim! Refresh         | -    | x    | -    | -    |
| Sugar Bombs          | -    | x    | -    | -    |
| Abraxo               | -    | x    | -    | -    |

> The Brotherhood of Steel paint job has multiple variants for any PA Left Arm pieces to display your rank insignia (Knight, Sentinel, Paragon). For all other pieces, there is only a single "Brotherhood of Steel" paint job as there are no rank-specific decals for them.

The **Abraxo** and **Sugar Bombs** paint jobs for the T-51 (added by the Contraptions DLC) will no longer be available by default. You need to find special promotional holotapes for each to unlock the paint jobs. Their locations are listed in the SPOILER SECTION at the bottom of this page.

The **Vault-Tec** paint job for the T-45, T-51, T-60, and X-01 power armors is similarly disabled at the start of the game and can be unlocked by a holotape. You can find it in the Overseer's office of any vault.

### Other Changes

[Power Armor Animation Changes](https://www.nexusmods.com/fallout4/mods/4408) makes entering and exiting your power armor out of combat much faster. Upon exiting your power armor frame, your fusion core will immediately be placed in your inventory thanks to [Take Your Cores](https://www.nexusmods.com/fallout4/mods/14773). This saves you from having to grab them manually. If you leave the cores in, NPCs like your settlers may decide to take your power armor for a walk and they don't always return it either.

## Settlement Building

The building system was generally improved by the following mods:

- [Place Everywhere](https://www.nexusmods.com/fallout4/mods/9424) removes the dreaded red outlines. You can now build anywhere and have much finer movement controls.
- [New Infinite Settlement Budget Plugin](https://www.nexusmods.com/fallout4/mods/16939) significantly increases the building budget (so be careful).
- [Visible Idle Markers](https://www.nexusmods.com/fallout4/mods/46453) helps prevent building objects on idle markers which NPCs would clip through to reach the marker.

> The more objects you place in a settlement (or technically the higher the overall polycount of all object gets), the more performance will degrade. With the expanded building budget it is now up to the player to using objects sparingly and mind the framerate.

## Keybinds

In addition to the vanilla keybinds there are a number of additional keybinds you can set through the various mods' configuration menus.

In the MCM for the [Configurable Hotkeys](https://www.nexusmods.com/fallout4/mods/46419) mod, you can define custom keybinds for functions such as quickly using Stimpaks or RadAway, immediately opening the Workshop, toggling the radio, or separating Throw Grenade / Melee (which are forced to the same key in vanilla).

> Note that WTP includes a mod that allows you to wait without having to sit down. It is not necessary to assign a hotkey for the Show Wait Menu option in Configurable Hotkeys for that.

### WTP Default Keybinds

- **V** Toggle HUD (Immersive HUD)
- **F8** Toggle Place Everywhere (Place Everywhere)

## New Content

### Additional Music

WTP both adds new tracks to the background music as well as to the Diamond City radio. The new additions were carefully selected to match the vanilla atmosphere so as not pull you out of the game.

The following mods expand the game's soundtrack:

- [Musical Lore - Wasteland Edition](https://www.nexusmods.com/fallout4/mods/14531)
- [Fallout Suite - Soundtrack Extension for Fallout 4](https://www.nexusmods.com/fallout4/mods/15870)
- [Bleak Beauty - A Fallout 4 Fan Made OST](https://www.nexusmods.com/fallout4/mods/9663)

> The music mods' individual plugins were replaced by a patched and merged one.

The following mods expand the Diamond City radio tracklist:

- [Elvani's Track Pack for Diamond City Radio](https://www.nexusmods.com/fallout4/mods/5467)
- [More Where That Came From - Diamond City Radio Edition](https://www.nexusmods.com/fallout4/mods/637)

### Pip-Boy Color Variations

[Pip Boy Retextured](https://www.nexusmods.com/fallout4/mods/47858) adds eight new colour variations (paint jobs) for the Pip Boy like the Creation ones but for free. You can change your Pip Boy's paint job whenever you like at any Armor Workbench.

### K-9 Harness

I'm a huge fan of fadingsignal's [K-9 Harness](https://www.nexusmods.com/fallout4/mods/17686) for Dogmeat so I had to add it to WTP. Instead of it being craftable, I have placed one harness in a location that fits thematically. Either trust that you will find it naturally on your travels or check the SPOILER SECTION at the bottom of this page if you want to know where it is.

### CC Modular Military Backpack

Also by fadingsignal is the [Modular Military Backpack](https://fallout.fandom.com/wiki/Modular_military_backpack) which matches the K-9 Harness beautifully. It is a Creation so you will need to buy it from the Creation Club. There are instructions for installing the Creation in WTP on the [Creation Club](/wtp/wtp-resources/creation-club/) page.

Note that the backpack will no longer be given to you upon leaving Vault 111 and it will not be distributed either. You can find a single one within Vault 111 that you can pick up at the start of the game.

## SPOILER SECTION

### X-01 Power Armor

You can find X-01 power armor pieces in the following locations:

- [The Prydwen](https://fallout.fandom.com/wiki/The_Prydwen): X-01 Helmet (vanilla)
- [Old Gullet Sinkhole](https://fallout.fandom.com/wiki/Old_Gullet_sinkhole): X-01 Left Arm
- [Boxing Gym](https://fallout.fandom.com/wiki/Boxing_gym): X-01 Right Armor
- [Museum of Witchcraft](https://fallout.fandom.com/wiki/Museum_of_Witchcraft): X-01 Torso
- [Greenetech Genetics](https://fallout.fandom.com/wiki/Greenetech_Genetics): X-01 Left Leg
- [O'Neill Family Manufacturing](https://fallout.fandom.com/wiki/O%27Neill_Family_Manufacturing): X-01 Right Leg

### Full T-51 Set

There is a full suit of T-51 on the rooftop of the [35 Court](https://fallout.fandom.com/wiki/35_Court) in the Financial District, downtown Boston.

### PA Paint Jobs

You can find holotapes to unlock certain power armor paint jobs in the following locations:

- [Super-Duper Mart](https://fallout.fandom.com/wiki/Super_Duper_Mart_(Fallout_4)): Sugar Bombs paint job (T-51)
- [Charlestown Laundry](https://fallout.fandom.com/wiki/Charlestown_laundry): Abraxo paint job (T-51)

### K-9 Harness

Can be found at the [Malden police station](https://fallout.fandom.com/wiki/Malden_police_station), upstairs.