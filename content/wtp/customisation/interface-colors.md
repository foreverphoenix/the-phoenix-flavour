---
title: "Interface Colors"
weight: 1
type: docs
description: >
  Customising the HUD and Pip-Boy colors.
---

In the INTERFACE section in Mod Organizer 2 you will find several separators with options to customise your interface, specifically the HUD colors. These options will be covered here. All of this is optional and can be skipped / ignored entirely. You can change any of these options at any point, they will not affect your save.

### HUD Color

The main HUD (heads-up display, the compass, health bar, etc) can be tweaked as usual ingame through the Settings menu. Unfortunately they are defined in the Fallout4Prefs.ini so it is not possible to tweak them through plugin INIs so you will have to either change the color ingame or edit the **Fallout4Prefs.ini** file. I actually recommend the latter.

- In order to change the color in the INI, open the INI editor through Mod Organizer 2.

> Editing the INI files under `C:\Username\Documents\My Games\Fallout4` will not work as we have profile-specific INI files in MO2.

![Open INI Editor](/Pictures/fallout/customisation/mo2-ini-editor.png)

- Switch to the **fallout4prefs.ini** tab and scroll down to the [Interface] section.
- Replace the following three lines with a set from the list below:
  - `iHUDColorB=`
  - `iHUDColorG=`
  - `iHUDColorR=`
- Click **Save** and close the window.

**Fallout 4 Green (Vanilla Default):**

```
iHUDColorB=21
iHUDColorG=255
iHUDColorR=18
```

**Pure White (TPF Default):**

```
iHUDColorB=255
iHUDColorG=255
iHUDColorR=255
```

**Fallout 3 Green:**

```
iHUDColorB=26
iHUDColorG=255
iHUDColorR=128
```

**Power Armor Amber:**

```
iHUDColorB=105
iHUDColorG=209
iHUDColorR=255
```

You can also use any other color combination you wish. Use the [Google color picker](https://www.google.com/search?q=color+picker) to choose your color and copy over the RGB values. Note that the order is **BGR** in the Fallout 4 INI files.

### Pip-Boy Flashlight Color

By default, the color of the flashlight (activated by holding TAB) will be the same as your HUD. Check the **Always White** option to decouple it from your chosen HUD color.

### Power Armor HUD Color

Unlike the main HUD color, the color for the power armor HUD is defined in the Fallout4.ini file which means it can be changed through plugin INIs. A pre-made set of plugin INIs is available for you to choose from, the colors corresponding to those listed above under HUD Color. In order to change the color, uncheck the previous option and check the one you prefer.

There is also a "Custom" option where you can paste your own RGB values. Use [this guide](https://drive.google.com/file/d/0B6ioBcQsnDXDV0JScWtubkRvSzQ/view) to find the correct values for the corresponding RGB numbers.

### Pip-Boy Dual Colors

This section features the mod [Pip-Boy Dual Colors](https://www.nexusmods.com/fallout4/mods/43338). Two of its options are included, the FO4 green and the FO3 green. The colors are identical to the corresponding HUD and power armor HUD colors. If there is demand, I will look into creating alternatives for the "Power Armor Amber" color and any other popular choices.

Note that Pip-Boy Dual Colors will overwrite the [Small Map Markers](https://www.nexusmods.com/fallout4/mods/13400) mod; however, its interface tweaks also include smaller markers so all this does is display a silver arrow next to SMM to show that the mod is being overwritten entirely.

If you want to use one of the Pip-Boy Dual Color options, you will also have to disable FX in the Pip-Boy. This will mostly disable the "holo" effect for item previews, displaying instead the inventory model directly. It will also remove the blur and scanlines effects. The setting `bPipboyDisableFX=1` is forced by the **CHECK THIS TO ENABLE DUAL COLOR** option which you obviously have to check / enable before activating one of the Pip-Boy Dual Color options.