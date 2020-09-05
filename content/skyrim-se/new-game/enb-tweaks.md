---
title: "ENB Tweaks"
weight: 3
type: docs
description: >
  Customisation help for ENBSeries.
---

Open the ENB GUI by pressing Shift+Enter. You can tweak the presets there and most changes will be visible instantly. Click **SAVE CONFIGURATION** after changing anything.

This page currently only includes instructions for Serio's ENB. If you are using another preset (such as the default Rudy ENB), you can still tweak anything you like through the UI, but there are no instructions / recommendations at this time.

## Serio's ENB

### Detailed Shadows

I personally find grass to be better looking when the Detailed Shadows effect is disabled. You can do so by going to **EFFECT** and unchecking **EnableDetailedShadows**.

![Serios Disable Detailed Shadows](/Pictures/skyrim/new-game/serios-disable-detailed-shadows.png)

### Interior Brightness

Serio's was tuned for the ELE lighting overhaul and will be too bright for Luminosity. Go into an interior and tweak the following values:

```
[ENVIRONMENT]
AmbientLightingIntensityInteriorDay=0.85
AmbientLightingIntensityInteriorNight=0.75
```

> The exact values are merely suggestions. Feel free to tweak the brightness as you see fit.

![Serios Interior Brightness](/Pictures/skyrim/new-game/serios-tweak-interior-lighting.png)

### LUTs

LUTs are different color grading tables that change the overall tone of the image. Serio's features eleven different LUTs that you can enable and switch between at will.

- Open the **ENBEFFECTPOSTPASS.FX** section in the right pane.
- Check the **Enable LUT** option and cycle through the available LUTs under **Gradient Tint Type**.
- By customising the **Gradient Tint Amount**, you can tweak how strong the color adjustment should be.

> In the PostPassFX section you can also toggle other effects such as Film Grain, Vignette, and Letterbox.

![Serios LUT](/Pictures/skyrim/new-game/serios-switch-lut.png)

