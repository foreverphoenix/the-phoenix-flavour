---
title: "Custom Files"
weight: 2
type: docs
description: >
  All files created specifically for this setup.
---

## Console Commands

This is a custom plugin that loads an INI file which in turn fires a BAT file upon loading a save game. A number of mods can be replaced with the console commands that are then executed. The BAT contains the following lines:

- `gr quality 3` >> decreases godrays performance impact.
- `gr grid 12` >> decreases godrays performance impact.
- `gr scale .8` >> decreases godrays performance impact.
- `gr maxcascade 1` >> decreases godrays performance impact.
- `cl off` >> disables rim lighting.
- `setgs iTerminalDisplayRate 600` >> speeds up terminal display speed (10x).
- `setgs fWorkshopWireMaxLength 2200` >> increases maximum length of power lines.
- `setgs fGunShellLifetime 150` >> bullet shells are visible for longer.
- `setgs fGunShellCameraDistance 12800` >> bullet shells are visible for longer.
- `setgs iDebrisMaxCount 375` >> bullet shells are visible for longer.
- `setgs iRemoveExcessDeadComplexCount 50` >> less dead actors at once.
- `setgs iRemoveExcessDeadCount 50` >> less dead actors at once.
- `setgs iRemoveExcessDeadComplexTotalActorCount 65` >> less dead actors at once.
- `setgs iRemoveExcessDeadTotalActorCount 50` >> less dead actors at once.
- `setgs iDeathDropWeaponChance 0` >> prevents enemies from dropping their weapons upon death.
- `setfog 0 100000` >> disables fog seemingly "following" the player.

### Changelog

- **1.0** Initial release.

### Replaced Mods

- [Longer Power Lines](https://www.nexusmods.com/fallout4/mods/2241/)
- [Faster Terminal Displays](https://www.nexusmods.com/fallout4/mods/937)
- [Shell Rain](https://www.nexusmods.com/fallout4/mods/870)
- [No Weapon Clutter](https://www.nexusmods.com/fallout4/mods/12825)

### Credits

- [BiRaitBec](https://www.nexusmods.com/fallout4/mods/23556) for the idea and most of the lines.
- [AUGSpeed](https://www.nexusmods.com/fallout4/mods/39996) for the fog tweak.
- [SloppyPooBag](https://www.nexusmods.com/fallout4/mods/15211) for the God Rays tweak.
- [Puma361](https://www.nexusmods.com/fallout4/users/13815465) for  Longer Power Lines.
- [OldNick](https://www.nexusmods.com/fallout4/users/443246) for Faster Terminal Displays.
- [pauderek](https://www.nexusmods.com/fallout4/users/1739196) for Shell Rain.
- [SmithyPete](https://www.nexusmods.com/fallout4/users/34353495) for the No Weapon Clutter tweak.

## DEF_HUD - Phoenix Preset

This is just my personal DEF_HUD preset, downsizing most elements and moving the compass to the top. It's included in the main DEF_UI mod folder.

![DEF_HUD Preset](/Pictures/fallout/documentation/def-hud-preset.png)

## Keywords, Crafting, Sorting

### Simple Keyword Resource

I'm not a fan of the feature creep that the standard keyword resource, [Armor and Keyword Community Resource (AWKCR)](https://www.nexusmods.com/fallout4/mods/6091), has been suffering from in recent years. This custom ESM contains ONLY keywords. They are required for my sorting overhaul tweaks.

### Simple Crafting Station

Thanks to [Simple Immersive Chem Benches](https://www.nexusmods.com/fallout4/mods/44691), Chem Benches will appear more like general crafting stations. My plugin renames them appropriately and adds new categories for item recipes. This makes sense since even in vanilla, they are used for more than just chems.

### Simple Sorting Overhaul

While I'm using [Valdacil's Item Sorting](https://www.nexusmods.com/fallout4/mods/3877) for most items, I created custom sorting rules for weapons, armor, and power armor in order to circumvent the AWKCR dependency. I am also not a fan of VIS' changes to mod-affected items and kept mostly the vanilla names. Cosmetic mods are denoted at the end of the item name, like "X-01 Left Leg Mk. 3 (Minutemen)". The sorting plugin comes with a DEF_INV_TAGS.xml for the new tags and icons.

## Custom Tweaks

### Plugin Tweaks

- The Minutemen quest "Taking Independence" (retaking the Castle) will not appear until the player has reached level 25.
- Removed the Pip-Boy entry from the Armor Workbench since it's only there for the CC paint jobs.
- Doubled the size of the moon (yes, seriously).

### Dismemberment Tweaks

Disabled dismemberment of limbs for certain weapons:

- Baseball Bat
- Security Baton
- Board
- Knife
- Knuckles
- Lead Pipe
- Pipe Wrench
- Rolling Pin
- Tire Iron
- Pole Hook
- 10mm Pistol
- .44 Pistol
- Hunting Rifle
- Assault Rifle
- Combat Rifle
- Deliverer
- Gamma Gun
- Institute Laser Gun
- Laser Gun
- Laser Musket
- Pipe Bolt Action Gun
- Pipe Gun
- Pipe Revolver
- Submachine Gun
- Alien Blaster
- Handmade Rifle
- Radium Rifle
- Flare Gun
- Plasma Gun
- Paintball Gun
- Acid Soaker
- Thirst Zapper
- Paddle Ball
- Baseball Grenade
- Bottlecap Mine
- Cryo Grenade
- Cryo Mine
- Pulse Grenade
- Pulse Mine

The idea comes from Hoosteen's [Disable Dismemberment by Weapon](https://www.nexusmods.com/fallout4/mods/16541). My plugin covers mostly the same weapons although I kept dismemberment for most heavy weapons and disabled it for some weapons the original mod didn't edit.

## Main Menu Music Replacer

I converted my favourite piece from the official Fallout 4 soundtrack by Inon Zur, [Wandering the Foothills Pt. 3](https://www.youtube.com/watch?v=sur7u3HiGZs), using [MultiXWM](https://www.nexusmods.com/fallout4/mods/3663). It matches my chosen menu background better than the main theme.

## Power Armor Tweaks

### Power Armor Lore-Friendly Distribution

This is a quick levelled list edit, replacing T-60 sets in the world with T-45 sets and X-01 sets with T-51 sets. This makes sense from a lore point of view as well as limit T-60 armor to the Brotherhood and X-01 to a few hand-placed pieces.

### Power Armor Paint Jobs

This plugin is primarily an extension of [Consistent Power Armor Overhaul](https://www.nexusmods.com/fallout4/mods/11234), equalizing crafting requirements for paint jobs (2 steel, 2 oil, matching the CC paint jobs) as well as removing additional non-cosmetic effects from paint jobs to make them strictly cosmetic-only.

## Workshop Rearranged - Disable Auto Closing Doors

Since auto closing doors after a few settings can be enabled and customised through the [Workshop Framework](https://www.nexusmods.com/fallout4/mods/35004) MCM, I saw no point in keeping the Auto Close versions of the Workshop Rearranged doors. This plugin disables them (prevents them from appearing in the settlement menu).

## Sound / Music Tweaks

### Sound Slider Tweaks

This is a very tiny plugin, re-enabling the True Storms sliders and renaming the RAO sliders to have a similar name.

### Merged Music Patch

Simply merges the music tracks added by the previous three mods together so that all of them can play.

## BAT Files

BAT files can contain console commands that can be batch-executed ingame by typing `bat <file name>` in the console. My personal BAT files are for testing and somewhat specific but I still decided to include them. For example, typing `bat crafting` will instantly put you in god mode, give you 1000 of each scrap type, and unlock all crafting perks which is very useful for modding weapons/armor and figuring out naming rules.

## Custom Patches

### Sorting Patches

These patches add sorting tags to various mod-added items, primarily holotapes.

### Simple Crafting Station

These patches tweak the crafting recipes primarily for config holotapes, moving them into the MOD CONFIG category at the crafting station as well as removing the scrap requirements.

### Conflict Resolution Patch

The final patch to resolve all remaining conflicts.