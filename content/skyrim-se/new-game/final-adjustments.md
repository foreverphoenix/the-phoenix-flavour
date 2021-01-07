---
title: "Final Adjustments"
weight: 1
type: docs
description: >
  Preparations and starting a new playthrough.
---

## Timing

Before starting a new playthrough, there are some considerations to make:

Has there been a Skyrim update recently? If so, SKSE64, the mods depending on it as well as the guide may receive an update very soon, and it may be worth it to wait a week or two for everything to catch up before diving into the game.

> Also keep an eye on our Discord server in case a major update for the guide or a mod is imminent.

## MO2 Notifications

Before jumping into the game, go through one final checkup. In Mod Organizer 2, go to **View** >> **Notifications**. If this is greyed out, you are good to go! If not there are multiple different warnings you might encounter:

- **Missing Masters:** One of your plugins is missing a master file. It is marked with an exclamation mark in your load order. This is most likely due to skipping a mod that was not optional or selecting the wrong option in a FOMOD  installer. Go back to the mod’s instructions in the guide and double-check everything.
- **Form 43 Plugin:** You forgot to re-save one or several plugins in the Creation Kit. Re-save them now.
- **Outdated SKSE Plugin:** Check the plugin's mod page to see if there is a new version.
- **Files in your overwrite:** This one is not particularly problematic and you can probably ignore it for the time being.

## New Profile

- In Mod Organizer 2, open the **Profiles** window (Tools > Profiles or CTRL + P).
- Select your **The Phoenix Flavour** and click **Copy**.
- Enter a name for the new profile. Here are some suggestions:
  - `The Phoenix Flavour - {name of the character for the playthrough}`
  - `The Phoenix Flavour - {name of the build or playstyle for the playthrough}`
  - `The Phoenix Flavour - Playthrough 1`
- Click **OK** and select your new profile in the list. Make sure both options at the bottom are checked:
  - Use profile-specific Save Games
  - Use profile-specific Game INI Files
- Close the **Profiles** window.
- Switch to your new profile in Mod Organizer 2.

## New Game

- Run **SKSE** through Mod Organizer 2.
- Select **NEW** in the Skyrim main menu to start your playthrough.