---
title: "Known Issues"
weight: 3
type: docs
description: >
  Bugs currently present in WTP.
---

## Nate/Nora is invisible in the cryo pod

When skipping the pre war prologue, you may find your spouse's body is invisible in their cryo pod. You can still interact with them to get their wedding ring. The problem is caused by Start Me Up and Previs Repair Pack and unfortunately I haven't yet figured out how to fix it. Either the way, it's a minor issue and definitely not gamebreaking.

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

This is a persistent issue with cubemaps. We have a fix for it, [Fixed flickering puddles](https://www.nexusmods.com/fallout4/mods/46787), ~~but the bug still occurs and I'm honestly clueless.~~ I fixed the fix in WTP 1.6 and it should be fine now although the flickering does still seem to happen during rain storms for whatever reason.

Puddles were removed altogether by [Clarity - A Visual Overhaul](https://www.nexusmods.com/fallout4/mods/31991) which was added in WTP 2.0 and should eliminate the issue for good.