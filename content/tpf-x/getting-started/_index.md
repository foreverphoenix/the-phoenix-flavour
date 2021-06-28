---
title: "Getting Started"
weight: 2
type: docs
no-list: true
description: >
  Preparations for the installation of TPF-X.
---

## Mod Organizer Profiles

One of the best features that Mod Organizer 2 brings to the table is **profiles**. They allow you to keep different mod and load orders with specific INI settings as well as separate save files. The base **The Phoenix Flavour** profile in Mod Organizer 2 shouldn't be edited by anything other than official updates so it remains clean. Like any other addon, TPF-X should be installed on a separate profile.

- In Mod Organizer 2, press **CTRL+C** open the **Profiles** window.
- Make sure the base **The Phoenix Flavour** profile is selected and click **Copy** to create a clone.
- Enter **The Phoenix Flavour - Extended** as the name and click **OK**.
- Select your new profile in the list and make sure that both options at the bottom are **checked** (the third will always be greyed out).
- With the new profile highlighted, click **Select** to switch to it.

### Profile-Specific Saves

Since you **copied** the base TPF profile, your TPF-X profile will have the same INI files (a set tweaked with BethINI earlier in the Initial Setup section) and any saves you may have created with it. If you want to remove those saves (after installing TPF-X, you have to start a new character anyway), you can go to the **Saves** tab in the right pane of Mod Organizer and delete them there.

The saves will ONLY be deleted from the TPF-X profile. When you return to the base TPF profile and run the game through that, they will still be available there.

## Sync Mod Order

When juggling multiple setups, deorder's **Sync Mod Order** plugin for Mod Organizer 2 comes in incredibly handy. Since the order of mods is specific to a profile, it may be annoying to apply base TPF updates to a customised profile. The plugin helps greatly with that.

> If you installed TPF with Wabbajack, deorder's Sync Mod Order is already installed.

- Download the latest version of deorder's [MO2 plugins](https://github.com/deorder/mo2-plugins/releases) from Github.

![Download Deorder's Plugins](/Pictures/tpf/tpf-addons/download-deorders-plugins.png)

### Installation

- Make sure **Mod Organizer 2** is closed.
- Navigate to your **Mod Organizer 2** installation and double-click the **plugins** folder.
- Open the downloaded archive and extract the **deorder_plugins** folder into the MO2 **plugins** folder.
- The resulting file path should be: `Mod Organizer 2\plugins\deorder_plugins\`.

> This will also install the other plugin, Merge Plugins Hide, which we will not be using.

## MO2 Separators

For the mods in TPF-X we will need some new separators in Mod Organizer 2. Feel free to give them different colours so they are easier to distinguish from base TPF separators. As usual, I recommend creating one separator per page and grouping all mods below that separator. Of course you don't need all separators in TPF-X if you decide to skip some modules (pages) altogether. Just adapt as needed.

This is what the TPF-X section in my Mod Organizer 2 instance looks like:

![Separators](/Pictures/tpf-x/getting-started/separators.png)

> You won't have the "Phoenix' Little Helpers" and "Facegen Plugins" separators. They contain mods I need when working on TPF.

## Final Notes

**TPF-X is more advanced than TPF**. I have abbreviated many instructions and you need to read *very carefully* so you don't miss anything. Because TPF-X is modular, it's tempting to skip over sections but I strongly urge you not to do that. Many mods have additional, complementary mods that should be installed alongside or patches that are required. Since you "graduated" from base TPF, I have higher expectations of you.

### Load Order

Because of the modular nature of TPF-X there is no **loadorder.txt** provided so you have to sort your plugins yourself. If you look at the base TPF load order you will notice that I have mirrored the mod order for the most part and only when conflicts could be resolved simply by moving a plugin did I deviate from that. Please do the same thing for the TPF-X plugins and sort the plugins in the order you installed them in.

- Group all TPF-X plugins below **XPMSE.esp** and above **RealisticWaterTwo.esp**.
- Group all **The Phoenix Flavour - <Mod\> Patch.esp** plugins below **The Phoenix Flavour - Conflict Resolution Patch**.
- Creation Club content will always be sorted to the top automatically. You do not need to move them manually.
- Some plugins have specific load order instructions that override the general "place in installation order" rule.

> The screenshot does NOT show all TPF-X plugins, only my personal selection.

![Separators](/Pictures/tpf-x/getting-started/load-order.png)

#### **INSTALLATION:** Get started with the [Interface](/tpf-x/installation/interface/) page.