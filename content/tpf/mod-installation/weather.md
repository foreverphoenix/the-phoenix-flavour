---
title: "Weather"
weight: 7
type: docs
description: >
  Overhaul of all vanilla weathers plus additional effects.
---

##### [Dynamic Volumetric Lighting and Sun Shadows](https://www.nexusmods.com/skyrimspecialedition/mods/44483?tab=files)

#### Download Instructions

- **Main Files:** Dynamic Volumetric Lighting and Sun Shadows

#### Additional Instructions

- Double-click **Dynamic Volumetric Lighting and Sun Shadows** in your mod order.
- Switch to the **INI Files** tab and select the **DLVaSS.ini**.
- Delete everything in the INI file and replace it with the following:

```
;----------------------------------------------------------------------------------------------;
;                                   DVLaSS configuration file                                  ;
;                         SKSE64 Plugin for Skyrim SE by LonelyKitsuune                        ;
;----------------------------------------------------------------------------------------------;


;----------------------------------------------------------------------------------------------
; Various time points for value interpolation throughout the day

[TimeOfDay]
DawnHour         = 3.0
SunriseStartHour = 6.5
SunriseEndHour   = 7.5
DayStartHour     = 9.0
DayEndHour       = 17.0
SunsetStartHour  = 18.5
SunsetEndHour    = 21.0
DuskHour         = 22.0


;----------------------------------------------------------------------------------------------
; Value override for "SunDirXExtreme". The higher the setting during sunrise/sunset, the "deeper" the sun shadows can go.
; Lower values will have a lower performance impact on the other hand (not much tho).
; It's recommended to set all values to somewhere between 200 (vanilla) and 1000 to avoid unnecessary instabilities.

[SunDirX]
DefaultValue =  200.0
SunriseValue = 1000.0
DayValue     =  200.0
SunsetValue  = 1200.0


;----------------------------------------------------------------------------------------------
; Fades out volumetric lighting during the night, ignoring any weather provided values.

[VolumetricLighting]
EnableNightFadeOut = false


;----------------------------------------------------------------------------------------------
; Experimental - If you experience problems while saving or loading with DVLaSS installed,
; try enabling this option to revert the SunDirX value to default while saving or loading.

[SaveLoad]
DisableWhileSavingAndLoading = false
```
- Press **CTRL+S** to save your changes and close the window.

> The applied INI settings are specifically tweaked for Rudy ENB.

##### [Cathedral Weathers and Seasons](https://www.nexusmods.com/skyrimspecialedition/mods/24791?tab=files)

#### Download Instructions

- **Main Files:** Cathedral - Weathers

##### [Rudy ENB - Cathedral Weathers](https://www.nexusmods.com/skyrimspecialedition/mods/39113?tab=files)

#### Download Instructions

- **Main Files:** Rudy ENB Cathedral Weathers required files Part I
- **Main Files:** Rudy ENB Cathedral Weathers required files Part II >> `merge with the main file`

> These are edits and additions for Cathedral Weathers specifically made for Rudy ENB.

#### Additional Instructions

- Delete the following file(s) and / or folder(s):
  - `Cathedral Weathers.ini`

##### [Cathedral Weathers MCM](https://www.nexusmods.com/skyrimspecialedition/mods/24940?tab=files)

#### Download Instructions

- **Main Files:** Cathedral Weathers MCM

##### [Skyrim Textures Redone - Enhanced Night Sky](https://www.nexusmods.com/skyrimspecialedition/mods/5561?tab=files)

#### Download Instructions

* **Main Files:** Skyrim Textures Redone- Enhanced Night Sky

#### FOMOD Instructions

* **Stars:** 2K Stars
* **Stars Type:** 2k only small stars
* **Moons:** 2K Moons
* **Nebula:** 4K Nebula
* **Aurora:** 4K Aurora
* **Constellations:** 2K Constellations

##### [Night Skies - Stars and Galaxies](https://www.nexusmods.com/skyrimspecialedition/mods/20301?tab=files)

#### Download Instructions

* **Main Files:** Night Skies - Milky Realism (4K) - CP 1.01

> This will overwrite a different version of the mod included with Cathedral Weathers that looks more vibrant and fantasy-like.

##### [Skygazer Moons - Masser and Secunda](https://www.nexusmods.com/skyrimspecialedition/mods/32057?tab=files)

#### Download Instructions

* **Main Files:** Skygazer Moons SSE 2K - No Glow

##### [Storm Lightning](https://www.nexusmods.com/skyrimspecialedition/mods/29243?tab=files)

#### Download Instructions

* **Main Files:** Storm Lightning for SSE and VR - Fomod Installer

#### FOMOD Instructions

* **Select Game:** Skyrim Special Edition
* **Select SSE Version:** 1.5.97
* **Select Plugin:** ESL Flagged
* **Select Night Time Sheet Halo:** Halo with Dimmer Lightning (Level 0)
* **Select Day Time Sheet Halo:** Halo Dim (Level 2)
* **Select Night Time Fork Halo:** Halo Dimmer (Level 1)
* **Select DayTime Fork Halo:** Halo Dim (Level 2)

##### [Volumetric Mist](https://www.nexusmods.com/skyrimspecialedition/mods/29273?tab=files)

#### Download Instructions

- **Main Files:** Volumetric Mists

#### FOMOD Instructions

- **Select an option:** Balanced Performance
- **Other lands:** Solstheim

##### [Wonders of Weather](https://www.nexusmods.com/skyrimspecialedition/mods/13044?tab=files)

#### Download Instructions

* **Main Files:** Wonders of Weather v1_10

#### FOMOD Instructions

* Change nothing, just click **Install**.

##### [WoW Dragon Mounds CTD Fix](https://www.nexusmods.com/skyrimspecialedition/mods/43188/?tab=files)

#### Download Instructions

- **Main Files:** WoW Dragon Mounds CTD Fix

#### FOMOD Instructions

- **Select version:** BSA + ESL flagged
- **Optional:** ~~Alternative Rain Splash Effect~~

##### [Wonders of Weather - Less Opaque Rain Splashes for ENB](https://www.nexusmods.com/skyrimspecialedition/mods/32062?tab=files)

#### Download Instructions

- **Main Files:** Wonders Of Weather - Less opaque rain splashes for ENB

#### FOMOD Instructions

- **Select Transparency in %:** 80%