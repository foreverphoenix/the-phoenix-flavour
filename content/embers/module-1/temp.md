---
title: "temp"
weight: 5
type: docs
no-list: false
description: >
 SSEEdit and understanding load order.
---

### ESM vs ESP

Curiously, two of the four new plugins are displayed in ***bold italics*** while the others are not.

This is how Mod Organizer 2 distinguishes between plugin types in the load order. If you look at the official master files (**Skyrim.esm**, etc) they are greyed out because they cannot be disabled, but they are also in ***bold italics***. That is what **ESM** (Elder Scrolls Master) plugins look like. They are different from **ESP** (Elder Scrolls Plugin) files in multiple ways.

**One important difference is that ESM plugins will *always* load above ESP plugins.**

However, as you may already have noticed, the two ESM plugins actually have the **.esp** file extension rather than **.esm**. Why then are they marked as ESM plugins in Mod Organizer 2?

This is where matters get complicated: There are hybrid file types. Using a program called **SSEEdit** (which we are going to install shortly), one can *flag* an ESP as ESM to force it to load above all other ESPs. In the case of the USSEP and SLAWF, this is helpful because they are intended to overwrite the official game files, but then in turn be overwritten by various other mods. As **ESM-ified ESPs**, the USSEP and SLAWF plugins can always be at the very top of your load order, right below the official master files.

> Technically, the SLAWF plugin is a hybrid of ESM, ESP, and a third plugin type, the **ESL** plugin. We will talk about ESLs later on.

### Plugin Order

As we already established, ESM plugins (which include ESM-ified ESPs) always load above ESP plugins. If you try to drag the **Unofficial Skyrim Special Edition Patch.esp** below **SkyUI_SE.esp**, it will simply not work. However, you can freely change the order of the two ESM-ified ESPs via drag-and-drop.

**Plugins overwrite each other in the order they are placed in.** A plugin that is lower in the load order will overwrite plugins higher in the load order. That is why the official master files are right at the top, to be overwritten by any plugin placed after them.

> Plugin order and load order are the same thing.

### Dependencies

Often plugins directly depend not only on official master files but also on other plugins. This is the case with **Landscape and Water Fixes.esp** which depends on the **Unofficial Skyrim Special Edition.esp**. If you uncheck the USSEP's plugin in the load order, Mod Organizer 2 will instantly warn you about the missing master. The notification in the upper right corner will light up and show the warning if you click on it.

![SLAWF Missing Master](/Pictures/embers/module-1/slawf-missing-master.png)

Alternatively, you can hover over the **Landscape and Water Fixes.esp** which has now been marked with a small warning sign icon to see all its dependencies and which master is missing.

Since the SLAWF plugin requires the USSEP plugin directly, we know that it must be placed *below* it in the load order as plugins are always placed below their masters. Be sure to re-enable the USSEP plugin and to place it above the SLAWF plugin before we proceed with the next step.

> It should be noted that Skyrim SE, unlike Skyrim LE, does not *always* immediately crash on launch when a master is missing. However, a missing master error must still be fixed.
