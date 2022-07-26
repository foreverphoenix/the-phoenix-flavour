---
title: "INI Files"
weight: 2
type: docs
description: >
  The WTP INI settings and individual tweaks.
---

## INI Settings

As usual, I have used [BethINI](https://www.nexusmods.com/fallout4/mods/67) to generate the INI files before adding some manual tweaks. The default INI set is based on the **High** preset while the performance INI set uses the **Medium** one.

- **VSYNC** is always turned off, it is forced through High FPS Physics Fix
- **Ambient occlusion** is always turned off, we are using ENB AO instead
- **TAA** is used for anti aliasing (as opposed to FXAA)
- **Godrays** are disabled in the performance INIs only

## Additional Tweaks

### Fallout4.ini

```
[Display]
fPipboyScreenEmitIntensityPA=1.25
fPipboyScreenDiffuseIntensityPA=0.15

[Pipboy]
bPipboyDisableFX=1
bPipboyEffectColorOnLight=0
fPAEffectColorB=0.392
fPAEffectColorG=0.722
fPAEffectColorR=0.376
```

### Fallout4Prefs.ini

```
[Display]
uPipboyTargetHeight=1400
uPipboyTargetWidth=1752

[Interface]
iHUDColorB=100
iHUDColorG=184
iHUDColorR=96

[Pipboy]
fPipboyEffectColorB=0.3920
fPipboyEffectColorG=0.7220
fPipboyEffectColorR=0.3760
```