---
title: "ESM Cleaning"
weight: 8
type: docs
description: >
  Cleaning the official master files with SSEEdit.
---

## About ESM Cleaning

With the release of SSEEdit 4.0, the process of cleaning plugins has been simplified substantially. Beginning with **Update.esm**, we are going to clean the following four ESMs, Bethesda’s official master files, **one at a time**.

* **Update.esm**
* **Dawnguard.esm**
* **HearthFires.esm**
* **Dragonborn.esm**

> Do **not** attempt to process Skyrim.esm this way.

## Export Files to MO2

Since we want to keep the vanilla files wholly untouched, we are going to copy over the four ESMs that we will clean into a MO2 mod folder. They will then overwrite the original ESMs from your **Data** folder (which are displayed at the top of your load order).

This method has the added benefit of keeping the vanilla files available as backup. Should something go wrong during the cleaning process (which is unlikely), you will be able to wipe the MO2 mod folder and copy the vanilla files again to start over.

- Open the `Mod Organizer 2\mods` folder and create a new folder inside called **Official Master Files – Cleaned**.
- Navigate to your **Data** folder and copy the following files:
  - **Update.esm**
  - **Dawnguard.esm**
  - **HearthFires.esm**
  - **Dragonborn.esm**
- Paste them into your new **Official Master Files - Cleaned** folder.
- In Mod Organizer 2, press F5 to refresh and your new "mod" will appear at the bottom of the mod order.
- Drag it up below **DLC: Dragonborn** in your mod order and activate it.

## Automated Cleaning Process

### Update.esm

* Select **SSEEdit - Quick Cleaning** in the executables list and hit **Run**.
* The plugin selection window will come up next.
* Check only **Update.esm** and click **OK**.

Now the cleaning process will begin automatically. It takes a few minutes, so simply sit back and let SSEEdit do its thing until you see `Quick Clean mode finished` in the log. Then you can close SSEEdit.

### Dawnguard.esm

* Run **SSEEdit - Quick Cleaning** through MO2.
* Check only **Dawnguard.esm** in the plugin selection window and click **OK**.
* Wait until the cleaning procedure is completed.
* Close SSEEdit.

### HearthFires.esm

* Run **SSEEdit - Quick Cleaning** through MO2.
* Check only **HearthFires.esm** in the plugin selection window and click **OK**.
* Wait until the cleaning procedure is completed.
* Close SSEEdit.

### Dragonborn.esm

* Run **SSEEdit - Quick Cleaning** through MO2.
* Check only **Dragonborn.esm** in the plugin selection window and click **OK**.
* Wait until the cleaning procedure is completed.
* Close SSEEdit.

![Update ESM Cleaned](/Pictures/skyrim-se/initial-setup/update-esm-cleaned.png)

## Manual Cleaning - Dawnguard ESM

There are [additional instructions written up by alt3rn1ty](https://forums.nexusmods.com/index.php?/topic/5381485-guide-manual-cleaning-skyrim-and-skyrim-special-edition-master-files/) to manually clean some dirty edits that won’t be caught by SSEEdit’s quick cleaning procedure. Only one of the edits can affect actual gameplay though, so we won’t bother with removing the other two which are simply left-over test records.

### Apply Filter

* Run **SSEEdit** through Mod Organizer 2 (do not use the Quick Cleaning version).
* In the plugin selection window, right-click and **Select None**.
* Check only **Dawnguard.esm** and hit **OK** (its masters, Skyrim.esm and Update.esm, will be loaded automatically).
* Once SSEEedit returns the message `Background Loader: finished`, you may proceed.
* Right-click anywhere in the left pane and select **Apply Filter**.
* Make sure the **Basic Conflict Resolution** filter preset is selected (check the screenshot below).
* Click **Filter** to start the process.
* This will take a moment and you need to wait until it is done.

![ESM Cleaning - Apply Filter](/Pictures/skyrim-se/initial-setup/xedit-apply-filter.png)

### Delete conflicting sub-record

* Proceed once SSEEdit returns `Done: Applying Filter`.
* Double-click **Dawnguard.esm** (now displayed in orange), then double-click **Cell**.
* Find the following cell (highlighted in red) in the list and select it:
  * `00016BCF RiftenRaggedFlagon`
* Scroll down in the right pane to the bottom until you can see the conflict in the line marked red.
* Right-click `RiftenRatwayZone [ECZN:0009FBB9]` in **Dawnguard.esm** and select **Remove** (see picture below).
* There will be a warning, simply click **Yes I’m absolutely sure**.

![ESM Cleaning - Manual Edit](/Pictures/skyrim-se/initial-setup/esm-cleaning-manual-edit.png)

### Save Changes

* Close SSEEdit.
* When asked to save your changes, only **Dawnguard.esm** should appear in the list.
* Make sure **Dawnguard.esm** is checked, then click **OK**.
* You’re done!

---

#### Continue with the [Instructions](/skyrim-se/mod-installation/instructions/) page.