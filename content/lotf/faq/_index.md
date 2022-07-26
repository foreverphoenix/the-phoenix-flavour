---
title: "FAQ"
weight: 9
type: docs
description: >
  Common questions and quick answers.
---

## Why is LOTF as a 'lite' list so big in terms of file size?

There are several reasons for the large file size requirement: Mods are nowhere near as optimised to save space as assets for games usually are. Of course, mod assets can also be compressed and BSA-packed but that makes them significantly more annoying to work with. Where possible, I did pack up bigger mods.

For the biggest files in LOTF - Skyrim Realistic Overhaul and Project Clarity, the texture overhauls - I already deleted all duplicate files and packed the rest in BSAs. The Project Clarity suite of mods (upscaling and tweaking vanilla textures) is still almost 10GB in total. In addition, the various LOD outputs, etc, add another 15GB, partially because there are multiple DynDOLOD outputs.

The total file size also counts the ~3GB (and rising) required for the Creation Club files.

## Are LOTF updates save-safe / can I continue my playthrough?

All LOTF updates will be, for the time being, save-safe and you can continue your playthrough after updating. This is due to the fact that I am myself doing a full playthrough with the setup.

I anticipate that this will last for the entire of the 2.x era during which I am gradually adding all Creation Club content. After that I have some ideas and plans for a 3.0 update which may well require a new game when it comes - but that is quite far in the future.

## How can I improve performance / increase my frame rate?

There are several options.

If you mostly have some issues with frame drops in exteriors, I recommend replacing your INIs with the performance set. You can find instructions for that [here](/lotf/customisation/#performance-inis). If this does not help enough, I recommend swapping to the Performance profile in MO2, although please note that if you were on the CC profile previously, you need to start a new playthrough (switching from the default to the performance profile is fine and you can continue your save).

In case you are using The Truth ENB, you can also try switching to the Lite version of the preset or disable the ENB altogether by removing the files from your Stock Game folder.

## I encountered a bug / issue / inconsistency. What do I do?

Please join us on [Discord](https://discord.gg/xCPxJFbCTS) and grab the **@LOTF** role. Post about what you encountered in the `#lotf-support` channel in the Legends of the Frost section. Add screenshot(s) if appropriate.

If there is no immediate response, please be patient. I or someone else will respond to you when we're around.

## Oh no, the game crashed! What do I do?

Generally speaking, a single random crash is no cause for worry. I usually start investigating if there is a second crash within a few hours or the crash is repeatable. That being said, I have had no crashes at all in some 90 hours of playing LOTF, so any crash reports are welcome.

- To submit crash reports, please join us on [Discord](https://discord.gg/xCPxJFbCTS) and grab the **@LOTF** role.
- Find the `#lotf-support` channel in the Legends of the Frost section.
- Drop your most recent crashlog `Crash-202x-xxxx.txt` into this channel.
- Briefly describe the circumstances under which it happened.

Crash logs can be found inside the `/NetScriptFramework/Crash/` folder in the **Overwrite**. You can find the **Overwrite** by scrolling all the way down in Mod Organizers' left pane.

> Do not report crashes that occured in a modified setup of LOTF (with added / removed mods). **Modified setups are not supported.**

## What is that weird blur / depth of field effect ingame?

Although it is possible to disable Skyrim's questionable depth of field in the INIs, doing so breaks underwater visuals (makes underwater look perfectly clear). However, I still strongly recommend turning down the DOF slider all the way down ingame. If you want a depth of field effect for pretty screenshots, you can enable DOF in The Truth ENB.

![Turn down DOF](/Pictures/lotf/faq/turn-down-dof.jpg)

## Bloom is too strong / snow too bright with The Truth ENB.

The Truth ENB comes with a fairly strong bloom effect by default. This can be decreased by switching to single-pass bloom in the enbbloom.fx file. You can open the ENB GUI ingame by pressing **F10**, then expand the **ENBLOOM.FX** section, and switch from multipass to singlepass bloom. Make sure to click the **SAVE CONFIGURATION** button on the left afterwards.

![Turn down DOF](/Pictures/lotf/faq/enb-decrease-bloom.jpg)

## Can I add my own mods on top of LOTF?

If you're asking, then probably not.

Regardless of whether you are building a custom setup or modifying an existing one (like LOTF), you need to understand how mods function, how they interact, and how they can be edited. Adding mods is not a matter of dropping them in MO2 and doing a cursory ingame check. Issues may not present themselves immediately or you may have inadvertently broken something else.

**There is no support for modifying setups or issues occuring in a modified setup.**

That being said, modding is fun and you should learn it! There are some great resources out there that you can start out with:

- [Tome of xEdit](https://tes5edit.github.io/docs/index.html)
- [Lively's Wiki](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/Main.md)
- [ModdingSkyrim](https://moddingskyrim.com/)
- [Darkfox217](https://www.youtube.com/c/Darkfox127/playlists) (Creation Kit videos)
- GamerPoets: [How to use MO2](https://www.youtube.com/playlist?list=PLlN8weLk86Xh3ue76x2ibqtmMramwQmHB)
- GamerPoets: [How to use xEdit](https://www.youtube.com/playlist?list=PLlN8weLk86XiGXJI4DaRa1QIq1zhDpD8V)