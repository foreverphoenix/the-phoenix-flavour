---
title: "Step 6: Creation Club"
weight: 6
type: docs
description: >
  Managing Creations with Mod Organizer 2.
---

## USSEP Requirements

Let's go back into MO2 and take a look at the error which popped up when we installed the Unofficial Skyrim Special Edition Patch. When the warning button in MO2 lights up, you can click on it to see the message. Do that now.

![Missing Master Error](/Pictures/embers/module-1/missing-master-error.png)

This one's a classic: Missing master. Plugins often rely on other plugins which are **master files** and if those masters are not present, they cannot load. Though SSE no longer immediately crashes with missing masters, it is still imperative to fix them. In this case, the USSEP requires four Creations: Fishing, Survival Mode, Saints & Seducers, and Rare Curios.

Rather than painstakingly modify the USSEP to remove those dependencies, we are going to install them for now.

## Creation Club

The Creation Club is a much-discussed and often controversial addition to Skyrim SE (and Fallout 4). Content made by Bethesda and hired modders is sold in the ingame microtransaction shop, or now bundled together in the Anniversary Edition DLC. The quality of these Creations ranges wildly from excellent to subpar.

For all intents and purposes, Creations are mods and should be dealt with as such. I highly recommend picking and choosing from them like you would from mods on the Nexus (though you can do this at a later time).

Since patch 1.6 everyone owns at least the four free Creations which are bundled with the main installation, these are the ones required by the USSEP.

### Managing Creations

Skyrim handles Creations like DLCs: If you own them, they are automatically downloaded, placed in the Data folder, and always active ingame. Earlier we chose to skip the Creations when duplicating the vanilla game into our **Game Root** folder with the intention of handling them later on.

Instead of dumping all Creations into the **data folder** where we have no control over them and cannot disable them, we will import them into Mod Organizer 2 instead. For that, we *could* manually create mod folders for each Creation and move the files over, but that would take a minute and we ain't got no time. Fortunately, the Creation Organizer exists.

## Creation Organizer

Okay, bear with me here: There are three kinds of plugins that are relevant in Skyrim modding. The first is the kind that requires SKSE and ends on `.dll`. The second is the kind that holds game data for Bethesda games and ends on `.esp`. Neither of these are related to Mod Organizer 2 plugins which are simply extensions for MO2, adding new functionality.

**Creation Organizer** is a highly configurable plugin for Mod Organizer 2 which automatically imports Creations from the (default) **data folder** into MO2.

- Download the latest main file of [Creation Organizer](https://www.nexusmods.com/skyrimspecialedition/mods/66329?tab=files) (click Manual Download).
- Download the **Creation Club Organizer Default JSON** from the **Optional Files** section (click Manual Download).

Now we need to extract the files into the MO2 directory:

- Open the **Creation Organizer** archive.
- Extract the folder inside to `\Mod Organizer 2\plugins\`.

Then add the customisation JSON:

- Open the **Default JSON** archive.
- Extract the JSON to `\Mod Organizer 2\plugins\creation_organizer\`.

Finally, **restart** Mod Organizer 2.

### Importing Creations

Running Creation Organizer through Mod Organizer 2 will now import all Creations *that you own* from your default installation folder into Mod Organizer 2 where you can manage them like any other mod. 

- Run Creation Organizer.

![Run Creation Organizer](/Pictures/embers/module-1/run-creation-organizer.png)

Importing the Creations will take a moment. If you have many of them (or all with the AE DLC), Mod Organizer 2 will lock for a few minutes, just let it do its thing.

When it's done you may have plenty of new mods in Mod Organizer 2, or at least the four free Creations.

- Uncheck ALL Creations except for **Fishing**, **Survival Mode**, **Saints & Seducers**, and **Rare Curios**.

With the four free Creations being active, the error message in MO2 should have disappeared.

> What you do with the rest of the Creations is up to you, but please leave them disabled while you are following **Embers**. The guide will cover CC integration at a later point.

## MO2 Separators

Now that we have all these new Creations installed in MO2, they really clutter up the interface...

The single most useful feature in MO2 to organise your mod order is **separators**. They were highly requested by the community and ultimately implemented by the MO2 team. Each separator can be placed anywhere in the mod order, its name and colour can be customised, mods can be grouped below it, and they can be collapsed or expanded at will.

Check out [this picture](/Pictures/embers/module-1/tpf-mod-order.png) of an older TPF mod order to get an idea of how separators can help with organising several hundreds of mods.

### Master Files Separator

At the top of your **mod order**, you can see three "mods" prefixed with **DLC**. Obviously, these are the three official DLC by Bethesda which appear in Mod Organizer 2 like any mod because, structurally, that is exactly what they are. Upon clicking on either of the three DLC files, the corresponding ESM (master plugin) will light up in the load order (right pane). This is very useful, especially with a larger setup later on: Clicking a mod in the left pane will always highlight any plugins that belong to it in the right pane, making them easy to find.

I personally drag the **DLC: Dawnguard** above the **DLC: HearthFires** in the mod order to mirror the order in which the DLC were released which is also the order in which they should overwrite each other. Technically, their mod order is irrelevant so this is purely a cosmetic change. It just bothers me to see them in the wrong order.

Now to create a separator for the official master files:

- Click the tools icon above the mod order and select **Create separator**:

![MO2 Create Separator](/Pictures/embers/module-1/mo2-create-separator.png)

- Enter **Official Master Files** as the name and click **OK**.
- Your new separator will show up at the bottom of your mod order.
- Drag it up above the three **DLC** in the right pane.

If you like you can also change the separator's colour. You can do so by right-clicking it and clicking **Select Color**. You can set the separator to any colour you like, it can be changed anytime, and every separator can have a different colour. Your colour choices should roughly match your MO2 theme (for instance, mine would be far too bright for anyone using dark mode).

### SKSE & Essential Mods Separators

Now that you know how to create separators in Mod Organizer 2, add two more for the mods we installed so far.

How you organise your mods is ultimately up to you. Any sort of system or naming scheme will be the most helpful to you if you came up with it yourself. However, for now I recommend going along with my choices until you have a better idea of what kind of setup you are going to build.

- Create a second separator and name it **Script Extender**.
- Drag it below **DLC: Dragonborn** and above **SKSE Scripts**.
- Create a third separator and name it **Essential Mods**.
- Drag it below **Address Library for SKSE Plugins** and above **SSE Engine Fixes**.

### CC Separator

And finally create a fourth separator to stow away the newly added Creations.

- In Mod Organizer 2, click the Tools icon above the right pane (see picture below).

Separators can be collapsed, hiding all the mods that were sorted underneath it. This is incredibly useful for large setups. Double-click the **Creation Club** separator - that's much better, right?

![MO2 First Separators](/Pictures/embers/module-1/mo2-first-separators.png)