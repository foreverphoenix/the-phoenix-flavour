![logo](/Media/tpf_logo.png)

**TABLE OF CONTENTS**
- [TROUBLESHOOTING](#troubleshooting)
  - [When trying to launch the Creation Kit, I encounter an error message.](#when-trying-to-launch-the-creation-kit-i-encounter-an-error-message)
  - [Skyrim immediately crashes when I launch it through Mod Organizer 2.](#skyrim-immediately-crashes-when-i-launch-it-through-mod-organizer-2)
  - [Skyrim launches fine but the main menu doesn't load.](#skyrim-launches-fine-but-the-main-menu-doesnt-load)
- [PERFORMANCE](#performance)
  - [Playing on a resolution of 1440p or higher.](#playing-on-a-resolution-of-1440p-or-higher)
- [MISC QUESTIONS](#misc-questions)
  - [Is ENBoost a thing in Skyrim SE?](#is-enboost-a-thing-in-skyrim-se)
  - [Can I play with a controller instead of mouse and keyboard?](#can-i-play-with-a-controller-instead-of-mouse-and-keyboard)
  - [Why don't all Classic Skyrim mods that included meshes have CAO instructions?](#why-dont-all-classic-skyrim-mods-that-included-meshes-have-cao-instructions)
  - [Is it still necessary to roll back to an older version of the Creation Kit?](#is-it-still-necessary-to-roll-back-to-an-older-version-of-the-creation-kit)
- [GAMEPLAY](#gameplay)
  - [How difficult is combat in Skyrim with The Phoenix Flavour?](#how-difficult-is-combat-in-skyrim-with-the-phoenix-flavour)
- [FEATURED MODS](#featured-mods)
  - [Will you add Legacy of the Dragonborn to The Phoenix Flavour?](#will-you-add-legacy-of-the-dragonborn-to-the-phoenix-flavour)
  - [Will you add Ordinator to The Phoenix Flavour?](#will-you-add-ordinator-to-the-phoenix-flavour)
  - [Will you add {my favourite mod} to The Phoenix Flavour?](#will-you-add-my-favourite-mod-to-the-phoenix-flavour)
  - [Does The Phoenix Flavour include Needs / Survival mods?](#does-the-phoenix-flavour-include-needs--survival-mods)

![separator](../Media/separator.png)

# TROUBLESHOOTING

## When trying to launch the Creation Kit, I encounter an error message.

If by chance you are seeing the error message picture below, it is simply an issue of the required version of Microsoft Visual C++  framework not being installed correctly. To fix this, download the latest **x64** executable [here](https://support.microsoft.com/en-us/help/2977003/the-latest-supported-visual-c-downloads). Run the downloaded executable and follow the prompts through the installation process.

![CK Error VC Missing](Pictures/faq/ck_error_vc_missing.jpg)

## Skyrim immediately crashes when I launch it through Mod Organizer 2.

### Is Steam running in the background?

### Did you select SKSE64 from the drop-down menu and launch it through MO2?

### Is one of your SKSE plugins outdated?

This one typically appears in the weeks after a Skyrim SE / SKSE64 update and you should have been notified by Mod Organizer 2. One possible cause would be installing Simply Knock and accidentally skipping the updated SKSE64 DLL for it (**Mod Installation, Step 36**). Double-check you have the latest versions of all mods with SKSE plugins installed and configured as per the guide’s instructions.

### Did you forget to unpack the BSA of a Classic Skyrim mod?

To quickly check for that, expand the Filter in MO2, filter by **Contains Bethesda Archive** and check if there are any mods with SKYRIM instead of SKYRIM SPECIAL EDITION in the Source Game column (check the picture below). If you find any, double-check the guide instructions for the mod in  questions. Chances are you forgot to unpack and/or delete the archive.

![Find Classic Skyrim BSA](Pictures/faq/find_classic_skyrim_bsa.png)

## Skyrim launches fine but the main menu doesn't load.

One of the more recent updates for the Unofficial Skyrim Special Edition Patch removed an AI package record from Aventus Aretino. None of the mods in the guide that touch Aventus (Prince and the Pauper, Simply Children, Adopt Aventus Aretino) have been updated since to incorporate that fix and they all have an unresolved error instead. This is fixed in the **Conflict Resolution Patch.esp**.

If the main menu won't load, your load order is messed up, or you aren't using the CRP.

![separator](../Media/separator.png)

# PERFORMANCE

## Playing on a resolution of 1440p or higher.

You will experience a significant performance loss when playing on a 1440p resolution (or higher) compared to 1080p, around 20 FPS with TPF in my experience. Therefore I strongly recommend playing on 1080p even if your monitor is capable of a higher resolution. I'm personally doing just that on my 1440p monitor and it looks fine.

In order to change the resolution, go into the **INI Editor** in Mod Organizer 2. Change the following lines in the **SkyrimPrefs.ini**:

```
[Display]
iSize H=1080
iSize W=1920
```

![separator](../Media/separator.png)

# MISC QUESTIONS

## Is ENBoost a thing in Skyrim SE?

No. Because of the 64bit upgrade, Skyrim SE is able to allocate more RAM for itself which is essentially what ENBoost used to do for Classic Skyrim. The current ENB binaries for SE contain no ENBoost features.

## Can I play with a controller instead of mouse and keyboard?

Yep, it's as easy as connecting a controller. The only potential issue would be lack of bindable hotkeys for mods.

## Why don't all Classic Skyrim mods that included meshes have CAO instructions?

This is a good question. Generally, meshes created for LE need to be optimised before they can be used in SE. However, not all meshes actually need optimisation! When running a mod through Cathedral Assets Optimiser, check the **Log** tab to see if there are any changes being made to specific files. If not, there is no need to use CAO on it. This is how I determined which mods need CAO instructions in the guide.

There is also the possibility that I simply forgot to add those instructions to a particular mod in the guide. When in doubt, you may run the mod through CAO with the **Optimise SLE Assets** profile and check the log. If changes are indeed made, the lack of instructions are an oversight in which case I would ask you to report the mod on our Discord!

## Is it still necessary to roll back to an older version of the Creation Kit?

No, this is no longer necessary. You should be running the latest version of the Creation Kit. Go into your **root** folder, right-click **CreationKit.exe**, switch to the **Details** tab and you should have **Product version 1.5.73.0**.

For a time it was necessary to use the executable and DLLs of the previous version (1.5.53) because **CK Fixes** was only working with that version of the Creation Kit. CK Fixes has since been updated.

![Separator](../Media/separator.png)

# GAMEPLAY

## How difficult is combat in Skyrim with The Phoenix Flavour?

With 3.0 - unlike previous versions - combat is not much harder than in vanilla. **[Wildcat – Combat in Skyrim](https://www.nexusmods.com/skyrimspecialedition/mods/1368)** helps diversify the behaviours of enemies as well as make combat a lot more interesting with timed blocks, attacks of opportunity and higher Stamina consumption. By adjusting the damage multipliers, users are free to tweak their own combat pacing and lethality. Playing on regular Adept with no custom changes will yield similarly "easy" but overall more enjoyable combat as vanilla.

Some additional, smaller mods that the guide includes help with making combat feel fresh – such as **[Realistic Melee Range](https://www.nexusmods.com/skyrimspecialedition/mods/3378)** which finally allows you to reliably side-step enemy attacks but also requires you to come in close and personal for your own attacks.

Enemy levels will be slightly higher than in vanilla, depending on their type. With SimonMagus' encounter zone overhaul [Arena](https://www.nexusmods.com/skyrimspecialedition/mods/33487) you will still be able to comfortably quest in Whiterun in the early game but some enemy types – such as Vampires, Falmer, Draugr lords – will have higher levels than regular bandits and require more preparation and caution on your part.

> Looking for significantly more challenging combat? Try [Lexy’s Legacy of the Dragonborn](https://lexyslotd.com/) instead.

![separator](/Media/separator.png)

# FEATURED MODS

## Will you add Legacy of the Dragonborn to The Phoenix Flavour?

No.

## Will you add Ordinator to The Phoenix Flavour?

No.

## Will you add {my favourite mod} to The Phoenix Flavour?

Maybe.

Make sure the mod (or a comparable alternative) is not already part of the guide and that it fits our general Vanilla+ standards. Then check my dedicated **[Trello board](https://trello.com/b/Rv20fMdV/the-phoenix-flavour-additional-mods)** for mods that are already considered as potential additions. If your mod is not included there either, you are free to share it in our **#mod-suggestions** channel on Discord, preferably with an explanation as to why you would like to see it in the guide!

## Does The Phoenix Flavour include Needs / Survival mods?

Needs mods for Skyrim implement Survival features such as hunger, thirst, and fatigue. There are also mods that add exposure as an additional factor, forcing you to keep dry and warm. Examples are Realistic Needs and Diseases, iNeed, Frostfall and, by extension, Campsite, or the Creation Club’s Survival Mode.

None of these mods are included in the main guide, and they never will be.

That being said, it is possible that I will at some point down the line, add these mods to the Customisation section. No promises.

There is a new light-weight survival mod - [The Frozen North](https://www.nexusmods.com/skyrimspecialedition/mods/33068) by Parapets - that may eventually be added to the mian guide.