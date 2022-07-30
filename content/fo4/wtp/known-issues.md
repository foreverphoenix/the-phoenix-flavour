---
title: "Known Issues"
weight: 6
type: docs
description: >
  Various issues currently present in WTP.
---

## Performance Issues

WTP is a performance friendly setup and should run well for most users. In fact, thanks to the **Previsibines Repair Pack**, it should run better than vanilla in some places. While WTP includes some 4K retextures, the Fallout 4 engine is actually capable of loading lower resolution versions of these when running out of VRAM. Almost all loose assets are packed into BA2 archives for better performance. I also took care not to include mods with long levelled lists containing new face presets as these can significant performance issues.

That being said, Fallout 4 is prone to performance issues, especially stuttering. For performance in general please keep in mind that resolutions above 1080p can incur a sizeable frame loss. 4K does not scale well. Having the game and/or MO2 installed on an HDD instead of an SSD may similarly cause frame drops or some stuttering.

If you are struggling with frame drops I would first recommend swapping to the **Performance INIs**. You can find instructions [here](/fo4/wtp/installation/#performance-inis).

If you are still unhappy about your framerate, you can delete the **d3d11.dll** from your Fallout 4 root folder to disable ENB.

## Nate and Nora have brown faces in the character creation

If Nate and Nora have brown faces in the character creation, you missed [this step](/fallout-4/wtp/installation/#official-high-resolution-texture-pack) instructing you NOT to install the Official High Resolution Texture Pack. Go back to the linked section, remove the HD DLC, and the issue will be gone.

![Brown Faces](/Pictures/wtp/brown-faces-issue.png)

## Nate/Nora is invisible in the cryo pod

~~When skipping the pre war prologue, you may find your spouse's body is invisible in their cryo pod. You can still interact with them to get their wedding ring. The problem is caused by Start Me Up and Previs Repair Pack and unfortunately I haven't yet figured out how to fix it. Either the way, it's a minor issue and definitely not gamebreaking.~~

**Should be fixed in more recent versions of PRP.**

![Invisible Spouse](/Pictures/wtp/appendix/invisible-spouse.jpg)

## Getting stuck when interacting with a terminal

*This is not a WTP-specific issue.*

Occasionally you may get stuck when attempting to access a terminal. This can be fixed by opening the console (tilde key, right above TAB on your keyboard) and typing in `tcl`. Upon closing the console (hitting tilde again), you should be able to use the terminal. Remember to open the console and type in `tcl` again to re-enable collision.

![Stuck Terminal](/Pictures/wtp/appendix/stuck-terminal.jpg)

## Subtitles get stuck during first Minutemen quest

*This is not a WTP-specific issue.*

When talking to Preston and Sturges in the Museum of Freedom, the subtitles usually get stuck for a time during the conversation. This happens in vanilla too and cannot be fixed as far as I know.

![Subtitles Stuck](/Pictures/wtp/appendix/subtitles-stuck.jpg)

## Issues with the Pip-Boy map when playing with a controller

By default, the Pip-boy UI is of a [pitifully low resolution](https://staticdelivery.nexusmods.com/mods/1151/images/48758/48758-1609598190-107962601.jpeg). Unfortunately, increasing it will cause a bug when playing with a controller that restrict the cursor to the upper left corner on the Pip-boy map.

You can work around this by turning off your controlling, opening your map, then turning it back on again.

The alternative is to revert the high resolution tweak in the INI files. To do so, follow these instructions:

- Open the **INI Editor** in Mod Organizer 2.
- Click on the **fallout4prefs.ini** tab.
- Scroll down to the `[Display]` section.
- Revert the values for the Pip-boy height and width to the default (see below).

```
uPipboyTargetHeight=700
uPipboyTargetWidth=876
```

- Click the **Save** button at the bottom and close the window.

![Map Cursor Stuck](/Pictures/wtp/appendix/map-gamepad.jpg)

## Flickering puddles

~~This is a persistent issue with cubemaps. We have a fix for it, [Fixed flickering puddles](https://www.nexusmods.com/fallout4/mods/46787), ~~but the bug still occurs and I'm honestly clueless.~~ I fixed the fix in WTP 1.6 and it should be fine now although the flickering does still seem to happen during rain storms for whatever reason.~~

~~Puddles were removed altogether by [Clarity - A Visual Overhaul](https://www.nexusmods.com/fallout4/mods/31991) which was added in WTP 2.0 and should eliminate the issue for good.~~

**As of WTP 2.5, puddles were re-enabled and should no longer flicker!** This is possible thanks to [fadingsignal's fix](https://www.nexusmods.com/fallout4/mods/62207?) and an update to ENB.

## Load screens appear frozen

In loading screens, there is no spinning object and the loading symbol is not animated. This is actually not a bug, but a feature. Disabling animations in loading screens apparently increases load times. It was done in the High FPS Physics Fix custom INI file.