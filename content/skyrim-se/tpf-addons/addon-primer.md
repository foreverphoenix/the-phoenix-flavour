---
title: "Addon Primer"
weight: 1
type: docs
description: >
  Read this before installing anything.
---

## About TPF Addons

Once upon a time, The Phoenix Flavour used to be modular. It also had optional mods. The idea was to give the user choices wherever possible and mark mods that are easy to swap as such. However, over time this proved to be enormously cumbersome to maintain on our end. After removing all traces of optional mods and modularity, the overall quality of the guide (and my own motivation to work on it) sky-rocketed. Needless to say, it was the right decision and we'll never go back to the pre-3.0 structure.

That being said, we've found a way to allow for some customisation without having to split my own attention between various possible installations. The Phoenix Flavour as the main setup will be completely unaffected by this section and any support for users of either manual guide or Wabbajack version will remain restricted to those with unedited setups.

**Addons** are extensions for the base TPF setup, made primarily by third parties - fellow users. I am also working on an Addon of my own. They are to be installed on top of existing and **unedited** TPF installations, and feature a variety of new mods or integration patches. Addons are **incompatible** with each other, you can only install one.

**If you are interested in using Addons:**

- Install The Phoenix Flavour first, ideally by following the manual guide.
- Test your setup. Play a little. Get help for any issues you may encounter.
- Only THEN should you consider installing an Addon.

If you run into issues after installing an Addon, you may ask for help in the dedicated TPF Addons section on the Discord server where the authors of the various Addons provide support for their tweaks.

> You should start a new character after installing an Addon.

### Wabbajack Users

- There is no Wabbajack version of any Addons.
- Wabbajack users are not *supposed* to install Addons.

Of course Wabbajack users can *in theory* follow the manual instructions for Addons like anyone else but I highly recommend against it. If you did not install TPF manually and have no or little prior modding experience, you are likely to make mistakes or simply miss crucial steps. It's not like I can stop you from installing Addons anyway but I'd consider it a bad idea.

## Mod Organizer Profiles

One of the best features that Mod Organizer 2 brings to the table is **profiles**. They allow you to keep different mod and load orders with specific INI settings as well as separate save files. The base **The Phoenix Flavour** profile in Mod Organizer 2 shouldn't be edited by anything other than official updates so it remains clean. Addons should be installed on separate profiles.

- In Mod Organizer 2, press **CTRL+C** open the **Profiles** window.
- Make sure the base **The Phoenix Flavour** profile is selected and click **Copy** to create a clone.
- Enter an appropriate name for the new profile, for example the name of the Addon you will be installing.
- Click **OK** and select your new profile in the list.
- Both options at the bottom should be **enabled** (the third will always be greyed out).
- Click **Close** to exit the profile settings.

> From now on I will be referring to the original profile as the **base profile** and the new one for the Addon as the **customised profile**.

### Profile-Specific Saves

Since you **copied** the base profile, your customised profile will have the same INI files (a set tweaked with BethINI earlier in the Initial Setup section) and any saves you may have created with it. If you want to remove those saves (after installing an Addon, you should start a new character anyway), you can go to the **Saves** tab in the right pane of Mod Organizer and delete them there. They will ONLY be deleted in the new profile. When you return to the base TPF profile and run the game through that, they will still be available there.

## Sync Mod Order

When juggling multiple setups, deorder's **Sync Mod Order** plugin for Mod Organizer 2 comes in incredibly handy. Since the order of mods is specific to a profile, it may be annoying to apply base TPF updates to a customised profile. The plugin helps greatly with that.

> If you installed TPF with Wabbajack, deorder's Sync Mod Order is already installed.

- Download the latest version of deorder's [MO2 plugins](https://github.com/deorder/mo2-plugins/releases) from Github.

![Download Deorder's Plugins](/Pictures/skyrim-se/tpf-addons/download-deorders-plugins.png)

### Installation

- Make sure **Mod Organizer 2** is closed.
- Navigate to your **Mod Organizer 2** installation and double-click the **plugins** folder.
- Open the downloaded archive and extract the **deorder_plugins** folder into the MO2 **plugins** folder.
- The resulting file path should be: `Mod Organizer 2\plugins\deorder_plugins\`.

> This will also install the other plugin, Merge Plugins Hide, which we will not be using.

## In Summary

- Installing an Addon **disqualifies** you from getting support on Discord in the `#tpf-guide-support` channel.
- Creators provide **support** for their addon(s) in the `#tpf-addon-help` channels, and only there.
- Addons require **experience** gained during the manual installation for TPF and are not recommended for WJ users.
- Addons should be installed in a **separate** MO2 profile.
- Addons are **not compatible** with each other. You can only install one.
- To update a customised profile, follow [these instructions](/skyrim-se/tpf-addons/updating-addons).

#### Available Addons and further information can be found [here](/skyrim-se/tpf-addons/available-addons).