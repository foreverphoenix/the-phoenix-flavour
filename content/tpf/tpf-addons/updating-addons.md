---
title: "Updating Addons"
weight: 2
type: docs
description: >
  Instructions for updating TPF with an Addon.
---

## The Problem

Here is the catch: Addons make updating the base TPF setup more difficult since that doesn't take any added mods into account. When TPF updates, the load order typically changes so you download and apply a new `loadorder.txt` to sort it again. This in turn will deactivate any plugins not in the txt (like those added by an Addon) and place them at the bottom of your load order.

Additionally, most Addons will ask you to deactivate a number of mods from the base setup, either because they are not compatible or because the creator doesn't like them. This further complicates updating TPF and a customised setup.

### Addon Updates

When an Addon is updated, you should be able to apply the changes to your customised MO2 profile by following its changelog. Rerun any patchers when required (this should also be mentioned in the Addon's changelog). If it is marked as "save-safe" you can continue your playthrough with the new version.

## Updating Customised TPF

Applying an official TPF update to a customised profile is a little more involved unfortunately. When an update to the base setup dropped, follow the instructions below to update it.

**Before updating a customised TPF profile, first check if your Addon is compatible with the new version of base TPF.**

If it is, follow these instructions:

- Switch back to your base `The Phoenix Flavour` profile in Mod Organizer 2.
- Update as usual using the TPF changelog.
- If your Addon requires redoing a patcher (LOD, Nemesis, etc) and the TPF update does as well, skip that for now.

> It would be pointless to rerun DynDOLOD etc for base TPF if you have to rerun them for an Addon in the customised profile anyway.

### Sync Mod Order

The [Addon Primer](/tpf/tpf-addons/addon-primer) included installation instructions for deorder's **Sync Mod Order** plugin. This is where it will come in handy:

- Ensure you are still on the **base profile** after updating to the newest TPF version.
- Click the **Puzzle** icon and select **Sync Mod Order** (see picture below).
- Right-click the profile you want to sync to (your customised profile) and select **Sync current profile mod order to**.

Mod Organizer 2 will refresh automatically when you close the window. Your customised profile now has the same mod order as your base one, ensuring all changes or additions are also in place there (otherwise you would have to manually move mods that were added or placed elsewhere in the mod order).

![Sync Mod Order](/Pictures/tpf/tpf-addons/sync-mod-order.png)

### Mod Order Check

One thing to know about deorder's plugin is that it only syncs the *order of mods* (in the left pane of Mod Organizer 2). It does not activate or deactivate mods. Generally this is great since the whole purpose of MO2 profiles is to have different setups where some mods are only active in certain profiles. However, in our case it also means that any mods added in the new TPF update to your base profile will still be deactivated on your customised profile even after syncing. These should be enabled now.

When re-enabling mods, remember that some mods may have been deactivated for compatibility with your Addon. If you are not certain which mods you need to keep unchecked for your Addon, check the Addon instructions.

- Scroll through the mod order in your customised profile.
- Enable any disabled mods from the base TPF setup that are compatible with your Addon.

### Load Order

The load order will have a similar problem as the mod order when updating but is thankfully much easier to fix. Addons have their own custom `loadorder.txt` files that you can apply instead of the official TPF one.

- Apply your Addon's `loadorder.txt` to your customised profile.

### Patchers

Depending on the nature of the TPF update and your Addon, you may need to rerun some of the patchers (Facgen, Nemesis, AllGUD, TexGen, DynDOLOD, xLODGen). This should always be stated in the update notes.

If your Addon requires you to rerun any patchers and the TPF update does as well, you can simply skip updating them for your base profile and only update your customised profile. If you aren't playing on your base profile, there is no real reason to keep their patcher outputs up-to-date.

> Remember to rename your outputs as your Addons instruct you to. For instance you should leave your original **Nemesis Output** for base TPF untouched and disabled on your customised profile. For your Addon, you should create a new folder called something like **Nemesis Output - Addon Name** so you can keep both and differentiate between them.

### Checklist

*This is a TL;DR for experienced users.*

- TPF updated!
- Check if your Addon is compatible with the new version of TPF.
- Update your base setup and sync it to your customised one.
- Re-enable disabled mods that are compatible with your Addon.
- Apply the Addon's `loadorder.txt` to your customised profile.
- Update any patchers required to be rerun by the TPF or Addon update.
- If TPF / Addon update were save-safe, continue your playthrough.