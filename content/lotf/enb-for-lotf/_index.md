---
title: "ENB for LOTF"
weight: 4
type: docs
description: >
  How to install The Truth ENB for Legends of the Frost.
---

**The Truth ENB** is a fantastic preset. The only reason it is not shipped with LOTF by default is because its author left the Nexus for AFKMods which unfortunately does not have the server capacity to support Wabbajack. Thus, the preset needs to be downloaded manually by any user wishing to install it.

I personally believe that the extra steps required for the Truth ENB are more than worth it as the preset looks amazing, especially with Obsidian Weathers (though it looks good with Wander as well).

Check the [Screenshots](/lotf/screenshots/) page for examples. The LOTF Obsidian section has pictures taken with Truth ENB.

## Download The Truth ENB

The preset can be downloaded from AFKMods:

- Create an account on the [AFKMods](https://www.afkmods.com/) website.
- Open the page for the [Truth ENB](https://www.afkmods.com/index.php?/files/file/2241-the-truth-enb/) preset and click the **Download this file** button.

![Truth ENB 1](/Pictures/lotf/customisation/truth-enb-1.png)

### Regular vs Lite

ENB is inherently performance-hungry and the regular version of The Truth can certainly have a considerable impact on weaker systems. If you are worried about performance, consider selecting the lite preset instead. You can pair it with the performance INIs for even better performance at the cost of visual quality.

- Download either the regular or the lite preset.

![Truth ENB Preset Choice](/Pictures/lotf/customisation/truth-preset-choice.png)

## Preset Installation

Install the preset to the LOTF Stock Game folder:

- Navigate to `/Legends of the Frost/Stock Game/` (this is LOTF's copy of the base game).
- Open the downloaded The Truth ENB archive.
- Extract the **enbseries** folder and **enbseries.ini** file into your Stock Game folder.

![ENB Preset Installation](/Pictures/lotf/customisation/enb-preset-installation.png)

### ENB Binaries

In order for any ENB preset to work, you also need the binaries which I have included in the LOTF installation. You simply need to move them into the root of your Stock Game folder.

- Navigate to `/Legends of the Frost/Stock Game/ENB Binaries`.
- Copy all three files into the `/Stock Game/` folder.

> The **enblocal.ini** contains my personal configuration, including more convenient hotkeys.

![ENB Binaries Installation](/Pictures/lotf/customisation/enb-binaries-installation.png)

## Preset Customisation

Most basic ENB features and settings can be configured within the **enbseries.ini** which you can find in your **Stock Game** folder.

- Open **enbseries.ini** in a text editor such as Notepad or Notepad++.

### New Features

In recent updates, some new features were added to ENBSeries, one of which is **Complex Grass** which unfortunately may be activated by default. To prevent that, simply add the new settings to the configuration file as disabled.

- In the **enbseries.ini**, scroll to the **[EFFECT]** section.
- Add the following two lines at the bottom (below `EnableReflection`):

```
EnableTerrainParallax=false
EnableComplexGrass=false
```

- Press **CTRL** + **S** to save your change.

### Wet Surfaces

I am personally not a fan of the 'rainy wet surfaces' feature enabled in Truth ENB. Check the preview pictures on the mod page or try it ingame and come to your own conclusion. If you want to disable it, here is how you do it:

- In the **enbseries.ini**, scroll to the **[EFFECT]** section.
- Change `EnableRainWetSurfaces=` to `false`.
- Press **CTRL** + **S** to save your change.

## INI Adjustments

To better accommodate the new ENB preset, we need to tweak some INI settings. This can most easily be done through MO2.

- Open the **INI Editor** in Mod Organizer 2:

![Open INI Editor](/Pictures/lotf/customisation/open-ini-editor.png)

### 64bit Render Target

This is a recommended tweak for The Truth ENB.

- In the **SkyrimPrefs.ini** tab, scroll to the **[Display]** section.
- Change `bUse64bitsHDRRenderTarget=` to `1`.
- Click the **Save** button at the bottom.

### Ambient Occlusion

> **Skip this if you are using the LITE preset.** It does not have Ambient Occlusion enabled.

LOTF's INIs (Default and Performance) both have Ambient Occlusion enabled. In the regular version of The Truth ENB, the superior (albeit more performance-hungry) ENB version of Ambient Occlusion is enabled and should replace Skyrim's.

- In the **SkyrimPrefs.ini** tab, scroll to the **[Display]** section.
- Change `bSAOEnable=` to `0`.
- Click the **Save** button at the bottom.

### Volumetric Lighting

> **Skip this if you are using the performance INIs.** They do not have volumetric lighting enabled.

In LOTF's default INIs, volumetric lighting, or godrays, is enabled. It is recommend to disable the feature in favour of The Truth's better looking ENB godrays.

- In the **SkyrimPrefs.ini** tab, scroll to the **[Display]** section.
- Change `bVolumetricLightingEnable=` to `0`.
- Click the **Save** button at the bottom.

## Better Candle Light

> **Skip this if you are using the LITE preset.** It does not have Complex Particle Lights enabled.

The mod [Radiant - Candles](https://www.nexusmods.com/skyrimspecialedition/mods/55856) uses the Complex Particle Lights feature from ENB to substantially improve candle light. If you installed the regular version of The Truth ENB, you can now enable the mod.

- In Mod Organizer 2, double-click the **WEATHER & LIGHTING** separator to expand it.
- Enable the **Radiant - Candles** mod.

![ENB Candle Lights](/Pictures/lotf/customisation/enb-candle-lights.jpg)