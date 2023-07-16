---
title: "INI Files"
weight:
type: docs
description: >
  About the default INI files.
---

## Vanilla INI Files

Various settings for Skyrim can be configured in a set of INI files:

- Skyrim.ini
- SkyrimPrefs.ini

Both can be found in the `\Documents\My Games\Skyrim Special Edition\` folder.

These INI files were regenerated during the [Clean Install](/bg/additional-modules/clean-install/) and a performance preset (low, medium, high, etc) was applied when opening the launcher for the first time.

There is also a `SkyrimCustom.ini` which does not exist in vanilla but can be created in the same directory to overwrite the other two INIs.

{{< alert color="info" >}}You can restore the set of vanilla INIs in the Documents folder by deleting them and launching the game through Steam. In the Launcher, you will be informed that the game will configure your settings (applying a preset) after which you can quit.{{< /alert >}}

### Valid Settings

Not all settings are valid in all INI files.

- **Skyrim.ini** can modify all settings valid in the game <u>except</u> those specific to the Launcher.
- **SkyrimCustom.ini** can modify all settings valid in the game <u>except</u> those specific to the Launcher.
- **SkyrimPrefs.ini** can modify a limited range of settings ([documented here](https://stepmodifications.org/wiki/SkyrimSE:SkyrimPrefs_INI)).

The catch is that duplicate INI settings are overwritten in the following order:

- **SkyrimPrefs.ini** >> **SkyrimCustom.ini** >> **Skyrim.ini**

{{< alert color="info" >}} For example, if **bFXAAEnabled=** is set to **1** in the **Skyrim.ini** and set to **0** in the **SkyrimPrefs.ini**, the latter will overwrite and FXAA will be off (0) ingame.{{< /alert >}}

### Plugin INIs

INIs can also be attached to **plugins** (ESP, ESL, ESM). Similar to BSAs, they are loaded if they have the same name as the plugin.

Any setting that is <u>not valid</u> in the **SkyrimPrefs.ini** can be added to a plugin INI.

Plugins that load INI files are displayed with a paper clip icon in the load order.

![Plugin with INI](/Pictures/bg/knowledge-base/ini-files/plugin-with-ini.png)

## INI Files and MO2

### Profile-Specific INIs

Going forward, I recommend not bothering at all with the default set of INIs, nor with the Settings in the launcher through which some of their lines can be modified.

Instead, make use of your <u>profile-specific INIs</u> in Mod Organizer 2. Each profile in a MO2 instance can hold a unique set of INIs that will replace the default ones when the game is started with that profile selected.

To enable profile-specific INI files, open the [profile settings](/Pictures/bg/tool-setup/mo2/mo2-profiles-settings.png) and ensure **Use profile-specific Game INI files** is enabled. These INI files will be saved under `\Mod Organizer 2\profiles\<your profile>\`.

[BethINI](/bg/tool-setup/bethini/) is able to target profile-specific INIs.

{{< alert color="info" >}}When *copying* a profile in Mod Organizer 2, the profile-specific INI files will also be copied.{{< /alert >}}

![Profile Specific INIs](/Pictures/bg/knowledge-base/ini-files/mo2-profile-specific-inis.png)

### Modifying INIs through MO2

You can view and edit all INI files through the INI Editor in Mod Organizer 2. It will display the profile-specific set if that option is enabled, and the default set from the Documents folder if it is not.

{{< alert color="info" >}}When modifying INIs through the INI Editor always remember to click the **Save** button at the bottom.{{< /alert >}}

![MO2 Open INI Editor](/Pictures/bg/mo2-open-ini-editor.png)

## INI Configuration

I recommend customising the INI files using the tool **BethINI**. You can find instructions [here](/bg/additional-modules/ini-config/).