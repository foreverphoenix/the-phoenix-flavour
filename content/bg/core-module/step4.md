---
title: "Step 4"
weight: 4
type: docs
description: >
  Playthrough.
---

{{< alert color="info" title="Summary" >}}
> This step covers {{< /alert >}}

## Plugin Types

You may have noticed that we have plugins with three different extensions in our load order.

- Skyrim.**esm**
- ccBGSSSE037-Curios.**esl**
- Unofficial Skyrim Special Edition Patch.**esp**

{{< alert color="info" >}}**ESP**, **ESM**, and **ESL** files are Bethesda plugins. They share the same basic structure of records with Form IDs arranged in layers and overwrite each other according to their load order.{{< /alert >}}

There are, however, notable differences between them which we will discuss in this step.

## ESP and ESM Plugins

**Elder Scrolls Plugins** (ESP) like our previously created **Disable USSEP Book.esp** are the most common type of plugin. If you create a mod in the Creation Kit, it will be exported in this format and most plugin-based mods use a simple ESP. In the load order in MO2 they will appear without any text decoration (like bold or italic).

**Elder Scrolls Master** plugins (ESM) appear in ***bold italics*** in Mod Organizer 2 - see, for example, the official master files. They will always load above ESPs and therefore ESPs will always overwrite them in case of conflicts. If you try to swap the load order of the USSEP and our modification for it in MO2 you will notice that you cannot place an ESP above an ESM.

### Plugin Limit

**The total number of ESM and ESP plugins in your load order cannot exceed 256 plugins.**

This is due to the hexadecimal system used to define them: Each plugin's **Index** (the first two characters in their form ID) is made up of a combination of two numbers and letters which in turn is based on their load order. The hexadecimal system has 16 unique characters and there are exactly 256 possible combinations for two characters from 00 to FF (see table below).

The hexadecimal **FF** is the decimal **255**, so the maximum amount of plugins from 0 (00) to 255 (FF) is 256.

![Hexadecimal Chart](/Pictures/bg/core-module/hexadecimalchart.png)

In Skyrim LE the plugin limit could be overcome by merging the records of multiple plugins into a single one.

In Skyrim SE plugin merging has become redundant for all but the largest of load orders thanks to the new ESL format of plugins introduced with the 2016 engine update.

## ESL Plugins

**Elder Scrolls Light** plugins (ESL) were initially added for the Creation Club (Fallout 4 and Skyrim SE) and they were a game-changer for the modding scene because the plugin limit for ESLs is about ten times that as for ESPs and ESMs.

All ESL plugins have the index `FE:xxx`. The hexadecimal FE is the decimal 254, so **all ESL plugins load in plugin slot 254.**

This is possible because their index was extended to the third, fourth, and fifth character in their eight character form ID: An ESL's index could be `FE:000` or `FE:08F`. Thus, **the limit for ESLs is a whopping 4096 plugins** - which is why we no longer need to merge plugins.

### Plugin Capacity

The downside of ESLs is that they can store fewer records.

Remember that each record must have a unique Form ID. ESLs only have three digits left for a combination of the 16 hexadecimal characters whereas ESPs and ESMs have six digits. This means every ESL can only store 4096 unique Form IDs of which the first 2048 are reserved by the engine.

The remaining 2048 slots are still more than enough for small- to medium-size mods. Many separate ESL plugins are infinitely easier to handle than a few big plugin merges (imagine having many small drawers for screws of different types and sizes instead of dumping all of them into a single big drawer).

Additionally, this limit only affects <u>new</u> records, i.e., records defined in the ESL plugin. There is no limit on how many records defined in *other* plugins an ESL can hold. Many mods, especially patches, function mostly by editing existing (vanilla or mod-added) records and adding few or no new records of their own. These types of plugins are especially suited to being ESL-ified.

{{< alert color="info" >}}**Summary:** You can install up to <u>4096</u> ESL plugins which can contain up to <u>2048</u> new Form IDs each.{{< /alert >}}

## Plugin Flags

We learned that **ESM** plugins are distinguished in the load order by being displayed in ***bold italics***.

But here is something strange: The **Unofficial Skyrim Special Edition Patch.esp** is displayed in ***bold italics*** in our MO2 load order tab when it actually has the ESP file extension.

So, is it an ESM or an ESP? Actually, it is both. This is where **Plugin Flags** come into play. 

{{< alert color="info" >}}Plugins can either be a full ESP, ESL, or ESM, **OR** they can be any combination of the three.{{< /alert >}}

That sounds a little confusing, so let's break it down.

### ESM-ESL

Imagine you created a mod that is a resource to be used by other mods: It just contains a few keywords, maybe a dozen records. You can easily use the ESL format for this plugin.

However, your resource is also a **master** to various dependent plugins which should be lower in the mod order, so preferably your plugin should load very early. It therefore makes sense to flag it as an ESM to automatically place it in the ESM space at the top of the load order.

The result is an **ESM-ESL** which will show up as ***Example.esl*** in the load order - like ***ccBGSSSE037-Curios.esl***.

### ESM-ESP

Now imagine your example mod is definitely one that should load very early to be overwritten by other mods but you have far too many original Form IDs to use the ESL format.

In that case, you can either opt for a full ESM or an ESP that is flagged as an ESM, that is, an **ESM-ESP** - like the ***Unofficial Skyrim Special Edition Patch.esp***.

{{< alert color="info" >}}To my knowledge, there is no functional difference between a regular ESM and an ESM-ESP.{{< /alert >}}

### ESP-ESL

Finally, you may have a plugin that is just fine to load in ESP space because it is not intended as a sort of baseline or framework. If it does not contain many new Form IDs, you can usually flag the plugin as an ESL, turning it into an **ESP-ESL** or **ESP-FE** (because ESLs always have an Index beginning with FE).

Which plugins can be flagged as ESL and how this can be done will be discussed in the following steps.

## Creating an ESL

Should you ever find yourself reaching the ESP/ESM plugin limit, you will no longer be able to launch the game - try to avoid that.

You can track your plugins via the neat little counter above your load order (hover for details):

![Plugin Counter](/Pictures/bg/core-module/plugin-counter.png)

With 9 plugins currently counting toward the 256 hard limit, we are in no danger of breaking the game anytime soon. Then again, load orders have the tendency to balloon to obscene dimensions so it is tends to be a good idea to ESL-ify as many plugins as possible.

{{< alert color="info" >}}Plugins with few or no original records, like patches that mostly modify other mods, are best suited to the ESL format.{{< /alert >}}

Hey, that sounds like our **Disable USSEP Book.esp** which only modifies a single reference.

- Load up your load order in SSEEdit.

### Plugin Header

Plugin Type is determined by file extension and plugin flags. You can see the file extension in the left pane and plugin flag(s) in the **Plugin Header** which is what you see when you select a plugin in SSEEdit.

Below, you can see the **Plugin Header** of our **Disable USSEP Book.esp**. It is a bog-standard ESP, so there are no plugin flags (or Record Flags as they are called here).

![ESP Plugin Header](/Pictures/bg/core-module/esp-plugin-header.png)

If you select the **Unofficial Skyrim Special Edition Patch.esp**, you will see that it is flagged as an **ESM**.

Two of the CC plugins, **ccBGSSSE037-Curios.esl** and **ccQDRSSE001-SurvivalMode.esl**, are additionally flagged as **ESLs**.

### ESL-Flagging

Going back to our **Disable USSEP Book.esp**, we can now simply turn it into an ESL (that is, an ESP-ESL because it still has the ESP file extension) by adding the flag.

- In the **Plugin Header**, right-click the empty space under **Record Flags** and select **Edit**.
- Confirm when the warning window pops up.
- Check the box for **ESL** and click **OK**.
- Close SSEEdit. Make sure **Disable USSEP Book.esp** is checked and click **OK**.

![ESL Flag](/Pictures/bg/core-module/esl-flag-plugin.png)

Back in MO2, our plugin now appears in *italics* in the load order and the little yellow icon 🟡 that appeared in the **Flags** column for the plugin confirms that it is ESL-flagged. You can also check this by hovering over it. And, of course, you can see the **FE** index.

![ESL Flag](/Pictures/bg/core-module/esl-flag-mo2.png)

## ESM Space and References

A major differences between plugins in ESM and ESP space is how references are handled.

{{< alert color="info" >}}Full ESLs load in ESM space, that is, they are forced to the top of the load order.{{< /alert >}}

### Persistent vs Temporary

There are two types of references:

- **Temporary references** only load into memory when the player is close by and are unloaded when they are no longer needed.
- **Persistent references** are always loaded into memory upon launching the game, regardless of player proximity.