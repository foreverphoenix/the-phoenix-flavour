---
title: "Mod Config"
weight: 3
type: docs
description: >
  Required and optional MCM tweaks.
---

## MCM Settings

The first thing you should do after escaping Vault 111 is manually save the game. You've successfully completed the introduction and are now free to explore the Wasteland - after configuring your mods. Thanks to the [Mod Configuration Menu](https://www.nexusmods.com/fallout4/mods/21497), many mods can now be tweaked through the MCM which can be accessed through the pause menu.

Hit **ESC** and open the **Mod Configuration**.

## FallUI

This MCM completely replaces WTP's old interface customisation. There is a TON of stuff to change here and everything comes down to personal preference. Feel free to tinker!

## FallUI - Workbench

Once again, lots to tinker like in the base FallUI MCM. However, there are also some mandatory changes.

### Brightness tweak

Items that are currently unavailable for crafting (due to missing components and/or required perks) are greyed out but hard to distinguish with the default settings. Turning down the brightness even further helps with that.

- Switch to the **Workbench list** tab.
- Under **List entries**, reduce **Brightness unavailable item** to 25.

![FallUI Brightness](/Pictures/wtp/mod-config/fallui-workbench-brightness.jpg)

### Disable autocrafting

- Switch to the **Generic settings** tab.
- Under **Crafting**, set **Auto-craft items without cost** to **Off**.

![FallUI Autocraft](/Pictures/wtp/mod-config/fallui-workbench-autocraft.jpg)

### Ultrawide support

You only need to follow these steps if you are playing on **Ultrawide** monitor.

- Switch to the **Generic settings** tab.
- Under **Settings**, change the **(Wide)screen aspect ratio** to match yours.
- If you are on Ultrawide resolutions (2560x1080 or 3440x1440), the aspect ratio is **21:9**.

> If your monitor has an ancient aspect ratio like 5:4 or 4:3, you could fix the UI here as well by entering that instead. However, many other components of the UI would still be mismatched.

![FallUI Ultrawide](/Pictures/wtp/mod-config/fallui-workbench-widescreen.jpg)

## Faster Workshop

- Set a hotkey for starting workshop mode. I prefer **Z** (or **Y** on a QWERTY layout).

![Faster Workshop MCM](/Pictures/wtp/mod-config/faster-workshop-mcm.jpg)

## GCM (Game Configuration Menu)

### DLC

- Loadscreen Rate **1**

This lowers the chance for Automatron-related loading screens to 1% down from the default 20% to match most other loading screens. It replaces [this tweak](https://www.nexusmods.com/fallout4/mods/21163).

![GCM DLC MCM](/Pictures/wtp/mod-config/gcm-dlc-mcm.jpg)

### Experience

- **Workshop:**
  - Base experience **0**
  - Maximum experience **0**
  - Experience multiplier **0**

With all the focus on settlement building including lowered weight for scrap I feel that balance is best served by taking it out of the level-up system entirely. The XP no longer earned by building is somewhat balanced out by the inclusion of PerkPointsPerLevel which grants you 1.2 perks per level up (one additional perk every 5 level ups).

![GCM XP MCM](/Pictures/wtp/mod-config/gcm-xp-mcm.jpg)

### NPCs

- Dodge chance **OFF**

This disables the weird sidestep / dodge that makes it seem like all NPCs can use the Force and feel your bullet coming.

![GCM NPC MCM](/Pictures/wtp/mod-config/gcm-npc-mcm.jpg)

### Skills

- **Hacking:**
  - Hacking min words **1**
  - Hacking max words **1**

This is optional (personal preference) but if you hate hacking as much as I do, this is how you can disable it. Perk requirements still apply for hacking higher-level terminals but only the correct word will be shown.

![GCM Hacking MCM](/Pictures/wtp/mod-config/gcm-hacking-mcm.jpg)

## Immersive HUD

- Main Settings: **Immersive HUD Enabled**
- Settings Holotape **Off**
- AID Toggle Items **Off**
- Hotkey to Toggle HUD: **X** (personal preference)
- Crosshair - Hitmarker: **Always** (personal preference)

The Holotape and AID item are no longer needed with the MCM and ability to set a keybind directly.

![Immersive HUD MCM](/Pictures/wtp/mod-config/immersive-hud-mcm.jpg)

## HoloTime

- Click on **Widget position** and scale the clock down to **0.7** (personal preference).
- Toggle HoloTime Display to **V** (personal preference)

Configuring HoloTime and iHUD can be a little annoying sometimes. Quit the MCM and toggle the HUD on (X), then toggle the clock widget (V). When you toggle off the HUD now, it should also hide the clock. If this doesn't work, try changing the clock scale, then changing it back, or quicksaving, then quickloading the game.

![HoloTime MCM](/Pictures/wtp/mod-config/holotime-mcm.jpg)

## More AGOMBz

### More Attacks

On the **More attacks** page, change the following:

- **Far Harbor creatures:**
  - Allow Far Harbor creatures attacks on The Island **ON**
  - Allow Far Harbor creatures attacks worldwide **OFF**
- **Nuka-World creatures**
  - Allow Nuka-World creatures attacks on Nuka-World **ON**
  - Allow Nuka-World creatures attacks worldwide **OFF**

![More AGOMBz MCM](/Pictures/wtp/mod-config/more-agombz-mcm-1.jpg)

### More ... Disable

On the **More ... Disable** page, change the following:

- Disable radstags attacks **ON**

> This is done for consistency with the mod [Docile Radstags](https://www.nexusmods.com/fallout4/mods/3208).

![More AGOMBz MCM](/Pictures/wtp/mod-config/more-agombz-mcm-2.jpg)

## Photo Mode

In this MCM, you can set a hotkey to go into Photo Mode and change its position in the Pause menu. Feel free to make changes or leave the settings at default.

![Photo Mode MCM](/Pictures/wtp/mod-config/photo-mode-mcm.jpg)

## Photo Mode

In this MCM, you can set a hotkey to go into Photo Mode and change its position in the Pause menu. Feel free to make changes or leave the settings at default.

![Photo Mode MCM](/Pictures/wtp/mod-config/photo-mode-mcm.jpg)

## Workshop Framework

### Settlement Gameplay

- Shelter Mechanic **OFF**

Just build your settlers' beds somewhere below a roof to protect your immersion and ignore this buggy mechanic.

![Workshop Framework MCM 2](/Pictures/wtp/mod-config/workshop-framework-mcm-2.jpg)

### Framework Controls

- Manage Workbench **OFF**

The Manage menu accessible at workbenches is only for scrapping stuff placed by the player and the WF layouts feature. Since TPF Fallout 4 doesn't currently include additional layouts, I would rather people disabled this entirely to prevent confusion. If you are interested in WF layouts, re-enable the Manage Workbench option and watch kinggath's tutorials on [importing](https://www.youtube.com/watch?v=N3MGiari9xc&feature=emb_logo) and [exporting](https://www.youtube.com/watch?v=9OVzgFzjnRw&feature=emb_logo) them. Obviously, downloading and installing layouts counts as adding mods and voids your right to get support for TPF Fallout 4.

![Workshop Framework MCM 1](/Pictures/wtp/mod-config/workshop-framework-mcm-1.jpg)

---

#### Enjoy your playthrough!
