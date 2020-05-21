![logo](/Media/tpf_logo.png)

**TABLE OF CONTENTS**
- [Error message when trying to launch the Creation Kit.](#error-message-when-trying-to-launch-the-creation-kit)
- [Skyrim immediately crashes after launching it through Mod Organizer 2.](#skyrim-immediately-crashes-after-launching-it-through-mod-organizer-2)
- [Skyrim gets stuck in the main menu.](#skyrim-gets-stuck-in-the-main-menu)
- [Grass looks strangely dull and flat.](#grass-looks-strangely-dull-and-flat)
- [Low FPS when playing on a resolution of 1440p or higher.](#low-fps-when-playing-on-a-resolution-of-1440p-or-higher)
- [Some beards look strange on Elven player characters.](#some-beards-look-strange-on-elven-player-characters)
- [How to redo INI files from scratch.](#how-to-redo-ini-files-from-scratch)
- [Miscellaneous Questions](#miscellaneous-questions)
- [How difficult is combat in Skyrim with The Phoenix Flavour?](#how-difficult-is-combat-in-skyrim-with-the-phoenix-flavour)
- [Future Additions - Will you add X mod?](#future-additions---will-you-add-x-mod)
- [Creation Club](#creation-club)

![separator](../Media/separator.png)

# Error message when trying to launch the Creation Kit.

If by chance you are seeing the error message picture below, it is simply an issue of the required version of Microsoft Visual C++  framework not being installed correctly. To fix this, download the latest **x64** executable [here](https://support.microsoft.com/en-us/help/2977003/the-latest-supported-visual-c-downloads). Run the downloaded executable and follow the prompts through the installation process.

![CK Error VC Missing](Pictures/faq/ck_error_vc_missing.jpg)

![separator](../Media/separator.png)

# Skyrim immediately crashes after launching it through Mod Organizer 2.

#### Is Steam running in the background?

#### Did you select SKSE64 from the drop-down menu and launch it through MO2?

#### Is one of your SKSE plugins outdated?

This one typically appears in the weeks after a Skyrim SE / SKSE64 update and you should have been notified by Mod Organizer 2. One possible cause would be installing Simply Knock and accidentally skipping the updated SKSE64 DLL for it (**Mod Installation, Step 36**). Double-check you have the latest versions of all mods with SKSE plugins installed and configured as per the guide’s instructions.

#### Did you forget to unpack the BSA of a Classic Skyrim mod?

To quickly check for that, expand the Filter in MO2, filter by **Contains Bethesda Archive** and check if there are any mods with SKYRIM instead of SKYRIM SPECIAL EDITION in the Source Game column (check the picture below). If you find any, double-check the guide instructions for the mod in  questions. Chances are you forgot to unpack and/or delete the archive.

![Find Classic Skyrim BSA](Pictures/faq/find_classic_skyrim_bsa.png)

![separator](../Media/separator.png)

# Skyrim gets stuck in the main menu.

One of the more recent updates for the Unofficial Skyrim Special Edition Patch removed an AI package record from Aventus Aretino. None of the mods in the guide that touch Aventus (Prince and the Pauper, Simply Children, Adopt Aventus Aretino) have been updated since to incorporate that fix and they all have an unresolved error instead. This is fixed in the **Conflict Resolution Patch.esp**.

If the main menu won't load, your load order is messed up, or you aren't using the CRP.

![Stuck in Main Menu](Pictures/faq/stuck_in_main_menu.jpg)

![separator](../Media/separator.png)

# Grass looks strangely dull and flat.

Without ENB, grass will unfortunately look much worse. If you are running an ENB preset, make sure Ambient Occlusion and Detailed Shadows are enabled as they really give grass some much needed depth. Be aware that those are both performance hungry settings that are disabled in Lite presets for a reason.

![Example](https://cdn.discordapp.com/attachments/521296280165679119/702036429341065286/enb2020_4_21_00_57_56.jpg)

![separator](../Media/separator.png)

# Low FPS when playing on a resolution of 1440p or higher.

You will experience a significant performance loss when playing on a 1440p resolution (or higher) compared to 1080p, around 20 FPS with TPF in my experience. Therefore I strongly recommend playing on 1080p even if your monitor is capable of a higher resolution. I'm personally doing just that on my 1440p monitor and it looks fine.

In order to change the resolution, go into the **INI Editor** in Mod Organizer 2. Change the following lines in the **SkyrimPrefs.ini**:

```
[Display]
iSize H=1080
iSize W=1920
```

![separator](../Media/separator.png)

# Some beards look strange on Elven player characters.

This is unfortunately a known issue with the beard TRI files in Ethereal Elven Overhaul. Some of them clip into the skin. Fixed TRI files for one beard (HumanBeard25) are packaged with the guide's CRP so that beards on humans look fine but issues remain with some beards on Elven characters. I have no idea to fix this and consider the issue low priority since Elves are rarely bearded anyway.

Check [issue report #8](https://github.com/foreverphoenix/the-phoenix-flavour/issues/8) for details and pictures.

![separator](../Media/separator.png)

# How to redo INI files from scratch.

Re-doing INI files from scratch can be necessary when BethINI got a significant update or when you get a crash upon launch / starting a new game caused by faulty INI edits. This is how to easily re-do INIs on a TPF setup.

- In MO2, click the folder icon to the right of the profiles selection drop-down
- Select **Open Profile folder** (see screenshot).

![Open Profiles folder](Pictures/faq/open_profiles_folder.png)

- Delete the following folder and files:
  - BethINI Cache
  - Skyrim.ini
  - SkyrimPrefs.ini
- Navigate to `C:\Users\Username\Documents\My Games\Skyrim Special Edition`.
- Copy the **Skyrim.ini** and **SkyrimPrefs.ini** located inside this folder, they are completely untouched and vanilla.
- Paste both files into the profiles folder.

Now all you have to do is close Mod Organizer 2, launch BethINI and follow the instructions under [Setup, Step 6.3](https://github.com/foreverphoenix/the-phoenix-flavour/blob/master/The-Phoenix-Flavour-3-2/01-Setup.md#63-bethini-configuration).

![separator](../Media/separator.png)

# Miscellaneous Questions

### I have over 300 plugins active in Mod Organizer 2. Is that intended?

Yes, that is definitely intended. While it's true that Skyrim has a limit of 255 plugins, this applies only to ESP and ESM plugins. Many plugins in TPF are ESL-ified though, and do not count toward the limit. When you hover over the counter above the load order in MO2, you can see how many ESM + ESP plugins you have, and how close you really are to the limit.

### Some plugins in my load order are deactivated. Is that intended?

No, this happens when renaming plugin extensions from ESL to ESP (in order to turn full ESLs into ESP-FE plugins). Make sure to check them again after renaming them. Eventually all plugins should be checked and active in your load order.

### Is ENBoost a thing in Skyrim SE?

No. Because of the 64bit upgrade, Skyrim SE is able to allocate more RAM for itself which is essentially what ENBoost used to do for Classic Skyrim. The current ENB binaries for SE contain no ENBoost features.

### Can I play with a controller instead of mouse and keyboard?

Yep, it's as easy as connecting a controller. The only potential issue would be lack of bindable hotkeys for mods.

### Why don't all Classic Skyrim mods that included meshes have CAO instructions?

This is a good question. Generally, meshes created for LE need to be optimised before they can be used in SE. However, not all meshes actually need optimisation! When running a mod through Cathedral Assets Optimiser, check the **Log** tab to see if there are any changes being made to specific files. If not, there is no need to use CAO on it. This is how I determined which mods need CAO instructions in the guide.

There is also the possibility that I simply forgot to add those instructions to a particular mod in the guide. When in doubt, you may run the mod through CAO with the **Optimise SLE Assets** profile and check the log. If changes are indeed made, the lack of instructions are an oversight in which case I would ask you to report the mod on our Discord!

### Is it still necessary to roll back to an older version of the Creation Kit?

No, this is no longer necessary. You should be running the latest version of the Creation Kit. Go into your **root** folder, right-click **CreationKit.exe**, switch to the **Details** tab and you should have **Product version 1.5.73.0**.

For a time it was necessary to use the executable and DLLs of the previous version (1.5.53) because **CK Fixes** was only working with that version of the Creation Kit. CK Fixes has since been updated.

![Separator](../Media/separator.png)

# How difficult is combat in Skyrim with The Phoenix Flavour?

With 3.0 - unlike previous versions - combat is not much harder than in vanilla. **[Wildcat – Combat in Skyrim](https://www.nexusmods.com/skyrimspecialedition/mods/1368)** helps diversify the behaviours of enemies as well as make combat a lot more interesting with timed blocks, attacks of opportunity and higher Stamina consumption. By adjusting the damage multipliers, users are free to tweak their own combat pacing and lethality. Playing on regular Adept with no custom changes will yield similarly "easy" but overall more enjoyable combat as vanilla.

Some additional, smaller mods that the guide includes help with making combat feel fresh – such as **[Realistic Melee Range](https://www.nexusmods.com/skyrimspecialedition/mods/3378)** which finally allows you to reliably side-step enemy attacks but also requires you to come in close and personal for your own attacks.

Enemy levels will be slightly higher than in vanilla, depending on their type. With SimonMagus' encounter zone overhaul [**Arena**](https://www.nexusmods.com/skyrimspecialedition/mods/33487) you will still be able to comfortably quest in Whiterun in the early game but some enemy types – such as Vampires, Falmer, Draugr lords – will have higher levels than regular bandits and require more preparation and caution on your part.

> Looking for significantly more challenging combat? Try [**Lexy’s Legacy of the Dragonborn**](https://lexyslotd.com/) instead.

![separator](/Media/separator.png)

# Future Additions - Will you add X mod?

### Will you add Legacy of the Dragonborn to The Phoenix Flavour?

No.

### Will you add Ordinator to The Phoenix Flavour?

No.

### Will you add {my favourite mod} to The Phoenix Flavour?

Maybe.

Make sure the mod (or a comparable alternative) is not already part of the guide and that it fits our general Vanilla+ standards. Then check my dedicated **[Trello board](https://trello.com/b/Rv20fMdV/the-phoenix-flavour-additional-mods)** for mods that are already considered as potential additions. If your mod is not included there either, please submit it to our [Mod Suggestions Google Form](https://forms.gle/CeQ4ftmcwy2pQ7xa8)!

### Will The Phoenix Flavour ever include Needs / Survival mods?

Needs mods for Skyrim implement Survival features such as hunger, thirst, and fatigue. There are also mods that add exposure as an additional factor, forcing you to keep dry and warm. Examples are Realistic Needs and Diseases, iNeed, Frostfall and, by extension, Campsite, or the Creation Club’s Survival Mode.

None of these mods are included in the main guide, and it's unlikely that they ever will be.

That being said, it is possible that I will at some point down the line, add these mods to the Customisation section. No promises.

There is a new light-weight survival mod - [**The Frozen North**](https://www.nexusmods.com/skyrimspecialedition/mods/33068) by Parapets - that may eventually be added to the main guide.

![separator](/Media/separator.png)

# Creation Club

### Will The Phoenix Flavour ever support Creation Club content?

While I personally dislike the Creation Club, there may be support for certain "creations" in the Customisation section at some point.

### What do I do if I want to play vanilla with 'creations' if I have TPF installed?

In order to play vanilla, you simply have to launch SkyrimSE.exe through the Default profile in MO2 where no mods are active. You can add your 'creations' like any other mod to MO2 by creating a new folder inside `Mod Organizer 2\mods` and pasting the ESLs and BSAs inside.