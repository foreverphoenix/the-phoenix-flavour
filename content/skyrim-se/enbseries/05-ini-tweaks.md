---
title: "INI Tweaks"
weight: 5
type: docs
description: >
  Required and recommended INI tweaks.
---

## Editing INIs in MO2

Just as a reminder: You can edit INI files for your profile directly through the Mod Organizer 2 interface.

- Go to **Tools** >> **Tool Plugins** >> **INI Editor** or click the puzzle icon and select INI Editor from the drop-down menu.
- Make your edits in the correct INI file (either Skyrim.ini or SkyrimPrefs.ini).
- When you're done, click the **Save** button and close the window.

![Open INI Editor](/Pictures/enbseries/mo2-edit-inis.png)

## Ambient Occlusion

ENBSeries includes ambient occlusion which can be toggled off in favour of Skyrim's usually more performance-friendly in-built ambient occlusion effect. ENB AO is more customisable and looks arguably better, and I recommend using it over the vanilla version. If you want to use ENB AO, disable the Vanilla AO to avoid unnecessary performance drops.

To disable vanilla AO, edit the following line in your **skyrimprefs.ini** file:

```
[Display]
bSAOEnable=0
```

## Particle Count

For Complex Particle Lights, increasing the amount of particles that can be displayed at once is recommend. This will make meshes with Complex Particle Light effects look better. For lower-end machines there can be a performance impact in foggy weather or magic combat situations. You can skip this if you skipped the **Related Mods** section.

Edit the following line in your **skyrimprefs.ini** file to increase the particle count to the recommended value:

```
[Particles]
iMaxDesired=7500
```

## Volumetric Lighting

For Rudy ENB, it is recommended (but not required) to enable Volumetric Lighting aka godrays. Please note that there is a noticeable performance impact, especially on weaker machines.

Edit the following line in your **skyrimprefs.ini** to enable godrays:

```
[Display]
bVolumetricLightingEnable=1
```