---
title: "ESL Plugins"
weight:
type: docs
description: >
  About Elder Scrolls Light plugins (ESL).
---

## About ESL Plugins

This article summarises some basic knowledge about **ESL Plugins**. 

{{< alert color="info" >}}I recommend reading the article on [Plugin Basics](/skyforge/knowledge-base/plugin-basics/) first.{{< /alert >}}

The **ESL** plugin format was added in the Creation Engine's 64bit upgrade for Fallout 4 and Skyrim Special Edition. It does not work in the 32bit version of the engine that Skyrim LE is running on.

The format was added to allow for dozens, potentially hundreds of new plugins for the official [Creation Club](/skyforge/knowledge-base/creation-club/), but has proved a godsent for the modding community as well. It circumvents the 256 plugin limit by reducing the size of the plugins.

## ESL Form IDs

The Form IDs in ESP and ESM plugins consist of the changeable two-character **Index** and six permanent characters unique to the record. This creates the 256 plugin limit.

Meanwhile, ESL plugins have a five-character **Index:** `FExxx`. The hexadecimal FE is the decimal 254 which means that all ESL plugins load in a single ESP/ESM plugin slot (254).

**A total of 4096 ESLs can be loaded at the same time.**

{{< alert color="info" >}}ESL-ified ESPs are also called ESP-FEs because of the ESL Index.{{< /alert >}}

### Plugin Capacity

The downside of ESLs is that they can store fewer unique Form IDs because they only have three permanent characters as opposed to six in ESPs/ESMs. ~~Every ESL can only store 4096 unique Form IDs of which the first 2048 are reserved by the engine.~~

**Update:** Since the release of Skyrim SE 1.6.1130.0, the range of Form IDs usable by ESL plugins has been doubled to 4096.

{{< alert color="warning" >}}This limit affects only <u>new records</u>. There is no limit on how many records defined in *other* plugins can be copied into an ESL (or any other plugin type for that matter).{{< /alert >}}

## Creating an ESL

Even a moderately-sized load order will quickly reach the 256 ESP/ESM limit, especially through small patches and minor tweaks. Using ESLs is unavoidable (and thankfully many mods now come with ESL plugins right out of the gate).

A plugin can be turned into an ESL by adding the ESL flag to it. Specific instructions can be found [here](/skyforge/modding-resources/creating-esl-plugins/).

### Plugins without new records

If a plugin (ESP or ESM) does <u>not</u> add any new records (Form IDs), it can always be ESL-flagged. This is typically the case for patches of all kinds and minor tweaks for vanilla or other mods.

### Plugins with new records

If a plugin (ESP or ESM) <u>does</u> add new records (Form IDs), they may need to be compacted before ESL-flagging.

Think about the differences in the Form ID format: While an ESP/ESM Form ID can have six character (+Index), an ESL can only have three (+Index). If there are Form IDs in the mod you wish to ESL-ify that extend beyond the final three characters, they have to be renumbered first to make room for the ESL Index.

**Remember that a plugin can only be ESL-ified if it has less than ~~2048~~ 4096 new records.**

Notably, not <u>all</u> plugins with new records need compacting. For example, in SkyUI_SE.esp, the new Form IDs only use the final three characters which means the first five characters are already freed up for the ESL Index and no change is required before adding the ESL flag:

![SkyUI Forms](/Pictures/skyforge/knowledge-base/esl-plugins/skyui-forms.png)

{{< alert color="info" >}}**Never ESL-ify a plugin that adds a new interior CELL** or you will [completely break it](/Pictures/skyforge/beginners-guide/myrwatch-broken.jpg) as soon as another plugin attempts to modify it in any way.{{< /alert >}}

## Compacting Form IDs

When ESL-ifying a plugin that contains new record, you must compact its Form IDs first. This carries a risk:

{{< alert color="warning" >}} By renumbering Form IDs you will break the plugins's dependencies. Any plugin that requires it as a *master* will be unable to find the original records that it is modifying, resulting in a wave of errors that will probably crash the game.{{< /alert >}}

You can avoid this by doing the following:

1. Avoid compacting Form IDs in plugins that are likely a master to many other plugins (i.e., that have many patches).
2. Compact Form IDs in plugins only when all of their dependent plugins are also present in SSEEdit at the time.

In the latter case, those dependent plugins would be updated automatically.

## ESL or ESP-FE

When should you create a full ESL and when is an ESP-FE sufficient?

The difference lies in the fact that a full ESL loads in ESM space. It handles [references](/skyforge/knowledge-base/references/) differently and will always be forced to the top of the load order.

If a given plugin does not contain CELL records with (temporary) references and does not need to load early because of dependencies or to be overwritten by other mods, creating an **ESP-FE** is sufficient.

Otherwise, create a **full ESL**.

{{< alert color="info" >}}Also remember that a full ESL will load in ESM space. For a plugin that happens to have a master that is an ESP, it would be impossible to load below the master as a full ESL, so it can only be turned into an ESP-FE.{{< /alert >}}