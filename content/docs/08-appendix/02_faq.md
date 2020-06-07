---
title: "Frequently Asked Questions"
weight: 2
type: docs
description: >
  Various guide-related questions & answers.
---

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