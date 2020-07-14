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

One possible cause would be installing Simply Knock and accidentally skipping the updated SKSE64 DLL for it (**Mod Installation, Step 36**). Double-check you have the latest versions of all mods with SKSE plugins installed and configured as per the guide’s instructions.

#### Skyrim LE BSA

Skyrim will immediately crash if you attempt to launch it with an active Skyrim LE BSA (compiled with the Skyrim LE Creation Kit). You can find instructions on how to quickly narrow down the culprit in Resources > Quick Tutorials.

#### INI Files

If none of the above helped, try regenerating your INI files from scratch. There are instructions under Resources > Quick Tutorials.

## Skyrim gets stuck in the main menu.

One of the more recent updates for the Unofficial Skyrim Special Edition Patch removed an AI package record from Aventus Aretino. None of the mods in the guide that touch Aventus (Prince and the Pauper, Simply Children, Adopt Aventus Aretino) have been updated since to incorporate that fix and they all have an unresolved error instead. This is fixed in the **Conflict Resolution Patch.esp**.

If the main menu won't load, your load order is messed up, or you aren't using the CRP.

![Stuck in Main Menu](/Pictures/faq/stuck_in_main_menu.jpg)

## Grass looks strangely dull and flat.

Without ENB, grass will unfortunately look much worse. If you are running an ENB preset, make sure **Ambient Occlusion** and **Detailed Shadows** are enabled as they really give grass some much needed depth. Be aware that those are both performance hungry settings that are disabled in Lite presets for a reason.

![Example](https://cdn.discordapp.com/attachments/521296280165679119/702036429341065286/enb2020_4_21_00_57_56.jpg)

## Lower FPS than expected.

#### Playing at a resolution higher than 1080p.

You will experience a significant performance loss when playing on 1440p (or higher) compared to 1080p, around 20 FPS with TPF in my experience. Therefore I strongly recommend playing on 1080p even if your monitor is capable of a higher resolution. I'm personally doing just that on my 1440p monitor and it looks fine to me. Check Resources > Quick Tutorials for instructions on how to quickly change the game's resolution.

## Some beards look strange on Elven player characters.

This is unfortunately a known issue with the beard TRI files in Ethereal Elven Overhaul. Some of them clip into the skin. Fixed TRI files for one beard (HumanBeard25) are packaged with the guide's CRP so that beards on humans look fine but issues remain with some beards on Elven characters. I have no idea to fix this and consider the issue low priority since Elves are rarely bearded anyway.

Check [issue report #8](https://github.com/foreverphoenix/the-phoenix-flavour/issues/8) for details and pictures.