---
title: "Troubleshooting"
weight: 2
type: docs
description: >
  Solutions to common issues.
---

## Error message when trying to launch the Creation Kit.

If by chance you are seeing the error message picture below, it is simply an issue of the required version of Microsoft Visual C++  framework not being installed correctly. To fix this, download the latest **x64** executable [here](https://support.microsoft.com/en-us/help/2977003/the-latest-supported-visual-c-downloads). Run the downloaded executable and follow the prompts through the installation process.

![CK Error VC Missing](/Pictures/faq/ck_error_vc_missing.jpg)

## Skyrim crashes upon launch.

#### Launching the game correctly

- Make sure Steam is running in the background.
- In MO2, select SKSE64 from the drop-down menu and click Run.

#### Outdated SKSE plugins

Skyrim may crash when you attempt to launch it with outdated SKSE plugins. This is a common problem in the weeks after a Skyrim SE and SKSE64 update. Normally there will be an error message as well, notifying you about the plugin in question. Mod Organizer 2 will show a warning as well.

One possible cause would be installing Simply Knock and accidentally skipping the updated SKSE64 DLL for it (**Mod Installation >> Miscellaneous**). Double-check you have the latest versions of all mods with SKSE plugins installed and configured as per the guide’s instructions.

#### Skyrim LE BSA

Skyrim will immediately crash if you attempt to launch it with an active Skyrim LE BSA (compiled with the Skyrim LE Creation Kit). You can find instructions on how to quickly narrow down the culprit in [Resources >> Various Tutorials](https://thephoenixflavour.com/skyrim-se/guide-resources/various-tutorials/).

#### INI Files

If none of the above helped, try regenerating your INI files from scratch. There are instructions under [Resources >> Various Tutorials](https://thephoenixflavour.com/skyrim-se/guide-resources/various-tutorials/).

## Main menu music is playing but the screen is black.

This happens when VSYNC is enabled in enblocal.ini and conflicts with SSE Display Fixes. Open ENB Man and go into the Global Settings. The **enblocal.ini** there should be checked so that it overwrites. Double-click it and make sure that `ForceVSync` under ENGINE is set to false. VSYNC should be forced through SSE Display Fixes instead.

> VSYNC is enabled by default in SSE Display Fixes and disabled in the enblocal.ini so if you run into this issue chances are you messed with settings you do not fully understand.

![Disable VSYNC enblocal.ini](/Pictures/appendix/disable-vsync-enb-man.png)

## Skyrim gets stuck in the main menu.

One of the more recent updates for the Unofficial Skyrim Special Edition Patch removed an AI package record from Aventus Aretino. None of the mods in the guide that touch Aventus (Prince and the Pauper, Simply Children, Adopt Aventus Aretino) have been updated since to incorporate that fix and they all have an unresolved error instead. This is fixed in the **Conflict Resolution Patch.esp**.

If the main menu won't load, your load order is messed up, or you aren't using the CRP.

![Stuck in Main Menu](/Pictures/faq/stuck_in_main_menu.jpg)

## Lower FPS than expected.

#### Playing at a resolution higher than 1080p.

You will experience a significant performance loss when playing on 1440p (or higher) compared to 1080p, around 20 FPS with TPF in my experience. Therefore I strongly recommend playing on 1080p even if your monitor is capable of a higher resolution. I'm personally doing just that on my 1440p monitor and it looks fine to me. Check [Resources >> Various Tutorials](https://thephoenixflavour.com/skyrim-se/guide-resources/various-tutorials/) for instructions on how to quickly change the game's resolution.