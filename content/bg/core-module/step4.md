---
title: "Step 4"
weight: 4
type: docs
description: >
  Plugin types: ESP, ESM, ESP. Plugin limit. Managing ESLs.
---

{{< alert color="info" title="Summary" >}}
> This step covers the three plugin types (ESP, ESM, ESL), their differences, and how one can be converted to another with special emphasis on creating ESLs.{{< /alert >}}

## Plugin Types

You may have noticed that we have plugins with three different extensions in our load order.

- Skyrim.**esm**
- ccBGSSSE037-Curios.**esl**
- Unofficial Skyrim Special Edition Patch.**esp**

**ESP**, **ESM**, and **ESL** files are Bethesda plugins. They share the same basic structure of records with Form IDs arranged in layers and overwrite each other according to their load order.

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

{{< alert color="info" >}}**Summary:** You can install up to <u>4096</u> ESL plugins which can contain up to <u>2048</u> new records / Form IDs each.{{< /alert >}}

## Hybrid Plugins

We learned that **ESM** plugins are distinguished in the load order by being displayed in ***bold italics***.

But here is something strange: The **Unofficial Skyrim Special Edition Patch.esp** is displayed in ***bold italics*** in our MO2 load order tab when it actually has the ESP file extension.

So, is it an ESM or an ESP? Actually, it is both. This is where **Plugin Flags** come into play. 

{{< alert color="info" >}}Plugins can either be a full ESP, ESL, or ESM, **OR** they can be any combination of the three.{{< /alert >}}

That sounds a little confusing, so let's break it down.

### ESM-ESL

Imagine you created a mod that is a resource to be used by other mods: It just contains a few keywords, maybe a dozen records. You can easily use the ESL format for this plugin.

However, your resource is also a **master** to various dependent plugins which should be lower in the mod order, so preferably your plugin should load very early. It therefore makes sense to flag it as an ESM to automatically place it in the ESM space at the top of the load order.

The result is an **ESM-ESL** which will show up as ***Example.esl*** in the load order - like ***ccBGSSSE037-Curios.esl***.

{{< alert color="info" >}}ESM-ESL plugins are also called **Light Masters**. Most creations use this format, with the exception of those that require for Form IDs which are full ESMs instead.{{< /alert >}}

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

{{< alert color="info" >}}Full ESLs are always ESM-flagged and therefore load in ESM space.{{< /alert >}}

### Persistent vs Temporary

There are two types of references:

- **Temporary references** only load into memory when the player is close by and are unloaded when they are no longer needed.
- **Persistent references** are always loaded into memory upon launching the game, regardless of player proximity.

![Refs](/Pictures/bg/core-module/temporary-persistent-refs.png)

The cap for references that are active at the same time is 1048576, anything above that will cause issues and instability.

The way references are handled is the most important difference between plugins in ESP space (.ESP with or without ESL flag) and plugins in ESM space (any plugin with ESM-flag: ESM, ESL, ESM-ESP). **Temporary references in ESP space are actually handled like persistent references and always loaded at the start of the game.** You can see how adding a great number of temporary references to ESP plugins could quickly bring the overall amount of active references closer to the cap.

Temporary references defined in ESM space but overwritten by a plugin in ESP space will also be always active. This makes sense if you think about how layers work and how the game only really cares about the one that overwrites.

{{< alert color="info" >}}Large mods that add their own worldspaces and / or overhaul the vanilla ones by adding or modifying many references should be ESM-ified so that their considerable number of temporary references is not always active.{{< /alert >}}

(There is a mod which will warn you when you approach the active references cap, we will install it later.)

### Moving into ESM Space

The book disabled in our custom plugin is a temporary reference. While I am not sure if an *initially disabled* reference is still being loaded, we are going to pretend it is for the sake of the argument.

Right now, our plugin is an ESP-FE so all references it contains are loaded, regardless of whether they are temporary or persistent.

Since it is already flagged as an ESL, the only missing piece to make it a full ESL is the file extension.

- Double-click **Disable USSEP Book** in your mod order and switch to the **Filetree** tab.

(This view is where you can see the contents of the mod folder.)

- Rename the file extension of the plugin to **.esl**.

![ESP to ESL](/Pictures/bg/core-module/esp-to-esl.png)

After renaming a plugin (name or file extension), MO2 will disable in the load order, so make sure to enable it again.

The plugin is now being recognised as a full ESL which means it belongs in ESM space. Where before you were unable to change its load order position, you can now drag it above the USSEP which is also in ESM space. Of course, the book plugin should stay <u>below</u> the USSEP plugin because it requires that as a master and plugins must always load below their masters.

Let's hop into the game to make sure this worked. You know the drill: Use `coc whiteruntempleofkynareth` from the main menu to quickly jump to the correct cell, then check the room to the left.

But, oh no! The book is back. What could possibly have gone wrong?

### ONAM Records

Turning an ESL-flagged ESP into a full ESL by changing the file extension works in 99% of cases - unless the plugin overwrites a reference. When that is the case, the affected references have to be added to the list of **Overriden Forms (ONAM)** in the plugin header.

If you create an ESM space plugin or flag a plugin as ESM in SSEEdit, this happens automatically. Unfortunately, we cheated a little by simply changing the file name extension so we are actually missing the ONAM entries which means the game skips our plugin's modification to the temporary reference.

- Load up your plugins in SSEEdit.
- Select the **Disable USSEP Book.esl** to view its **Plugin Header**.

Here, you can see that the ONAM sub record is empty.

![Missing ONAMs](/Pictures/bg/core-module/missing-onams.png)

The solution to the problem is manually ESM-flagging the plugin SSEEdit so the ONAM list is populated. The plugin will still be an ESL and not count toward the 256 plugin limit, so there is no downside to doing this.

- Right-click the **Record Flags** and also check the box for **ESM** in addition to the **ESL** flag.

![ESL ESM](/Pictures/bg/core-module/esl-esm.png)

We now have an ESM-flagged ESL. Close SSEEdit and save your change.

When you re-open the plugin in SSEEdit and check the **Plugin Header**, you will see that SSEEdit automatically added the affected temporary ref to the list.

![ONAM Added](/Pictures/bg/core-module/onam-added.png)

Finally, jump back into the game, `coc whiteruntempleofkynareth`, and, sure enough, the plugin works again.

## ESLs and Cells

Any plugin can be turned into an ESL (ESP-FE or full ESL) <u>with one exception</u>. A demonstration is in order.

{{< alert color="warning" >}}Unfortunately, for this example the easiest option is to simply use the **Myrwatch Tower** creation, so if you happen to not own it, you will only be to read this section as opposed to following along.{{< /alert >}}

- Double-click the **Creation Club** separator in MO2 and enable the **Myrwatch** creation.
- Load up your plugins in **SSEEdit** and double-click **cceejsse002-tower.esl** to expand it.

### CELL Records

In the Myrwatch plugin, you can see two types of records: **Cells** (interior locations) and **Worldspaces** (the outside world). Both consist of **CELL** records populated by persistent and temporary references.

- Expand the **Cell** record category and navigate to **Block 7** >> **Sub-Block 0** >> `[FE00183B] ccEEJSSE002MageTowerMain "Myrwatch"`.

This is a CELL record (see the **Signature** at the top).

![CELL Record](/Pictures/bg/core-module/myrwatch-cell-record.png)

We will use this CELL as our guinea pig. Remember that you can quickly jump to any cell using the `coc` command if you have the cell's **Editor ID** which is `ccEEJSSE002MageTowerMain` in this case.

- Launch the game and run `coc ccEEJSSE002MageTowerMain` through the console.

Yep, we are in the tower. It looks really comfy, I hope nothing bad will happen to it.

- Quickly close the game by running `qqq` through the console.

![Myrwatch](/Pictures/bg/core-module/myrwatch.jpg)

### Creating Apple.esl

Now it is time to horribly break the CELL for demonstration purposes.

- Jump back into SSEEdit and find the `ccEEJSSE002MageTowerMain` CELL record again.
  - *Tip: Search for the Form ID to quickly focus on the record.*
- Expand the **CELL** record and look at the **Temporary** references inside.
- Select the random `FoodApple02 "Green Apple" [ALCH:00064B2F]` near the top.

An apple a day is important and all that, but what if you prefer red over green apples? We can easily switch that out.

- Right-click the top of the **cceejsse002-tower.esl** in the right pane and select **Copy as override into**.
- Confirm when the warning window pops up.

![CELL Record](/Pictures/bg/core-module/myrwatch-cell-new-layer.png)

So, given that we are modifying a single record, using the ESL format seems appropriate. When creating an ESL plugin through SSEEdit, it will automatically be given the ESM flag as well so that any modifying temporary refs are added to the ONAM list.

- Pick the bottom option, **\<new file>.esl**, and name your new plugin **Apple** (or something equally creative).

In our new **Apple.esl** layer we can now modify the base object placed in this temporary reference.

- Double-click the `FoodApple02 "Green Apple" [ALCH:00064B2F]` base object in the new layer.
- Click the little arrow to expand the drop-down menu and select `FoodApple "Red Apple" [ALCH:00064B2E]` from the list.
- Close SSEEdit and save your new plugin.

![CELL Record](/Pictures/bg/core-module/change-base-record.png)

### Gazing into the abyss

Back in MO2, the ***Overwrite*** will have caught your new plugin. Since we are (spoiler alert) not going to keep it, you can leave it in its temporary location, but do remember to activate the plugin in the load order.

Once again, jump ingame and `coc ccEEJSSE002MageTowerMain`.

Oh, no.

![Myrwatch](/Pictures/bg/core-module/myrwatch-broken.jpg)

### Conclusion

After closing the game with `qqq`, you can delete **Apple.esl** from your ***Overwrite*** simply because it could never work. Also remember to disable **Myrwatch** again in the mod order.

{{< alert color="warning" >}}Modifying a CELL that is created in an ESL utterly breaks that CELL. This is unfixable.{{< /alert >}}

In other words, while a CELL record <u>can</u> be created in an ESL, it <u>cannot</u> be overwritten. This has important implications when ESL-ifying plugins to circumvent the 256 ESP/ESM limit because it means that you should generally **avoid ESL-ifying any plugin in which a new CELL is created**.

{{< alert color="info" >}}There is a [mod](https://www.nexusmods.com/skyrimspecialedition/mods/64108) which duplicates all Myrwatch CELLs in a regular ESM which is used by mods modifying the tower to circumvent the problem. The only creations that add new CELLs as full ESLs are Myrwatch and Sunder & Wraithguard.{{< /alert >}}

## Renumbering Form IDs

One final concern about ESL plugins concerns the Form ID format. This is only an issue when <u>converting</u> a regular ESM or ESP into an ESL. Remember that an ESP has a Form ID with six out of eight unique characters, i.e., `xx03A88F`, while an ESL's Index extends to the fifth character, i.e., `xxxxx88F`.

When you want to turn <u>an ESP that adds new Forms</u> into an ESL, you have to **compact Form IDs** before you can add the ESL flag.

We need an example mod for this:

- Create a new separator in Mod Organizer 2 and name it **Grass Overhaul**.
- Leave it at the bottom of the mod order.
- Download and install [No Grass In Caves](https://www.nexusmods.com/skyrimspecialedition/mods/12431?tab=files).
  - *Grab the first main file, without compatibility for lighting mods.*

{{< alert color="info" >}}This mod removes grass from caves (duh) because grass mods tend to increase the density. More grass also means more grass in very dark areas where the lack of ambient light causes the grass to look black.{{< /alert >}}

### Compacting Form IDs 1

After installing and activating the new mod, another plugin (a normal ESP) will show up in the load order.

**Go ahead and load up your plugins in SSEEdit.**

Checking our new mod, we will notice that it not only removes grass, but also adds new flora to make up for that. Statics like these plants are lit differently from grass (they can be affected by point lighting, cast by, for example, a torch and will not look black in low ambient light areas).

As we would expect, the Form IDs for the temporary references added by the mod begin with the plugin's two-character Index, `08`.

![ESP Forms](/Pictures/bg/core-module/esp-form-ids.png)

Trying to add the ESL flag and save the plugin would cause SSEEdit to throw the following error:

```
[00:00] Saving: NoGrassINCaves.esp.save.2023_07_04_10_44_50
[00:00] Error saving NoGrassINCaves.esp.save.2023_07_04_10_44_50: Record [REFR:080148ED] (places TreeSwordFern01 [TREE:000B73B8] in GRUP Cell Temporary Children of BlindCliffCaveCOC [CELL:00021EFA] (in BlindCliffCaveWorld "Blind Cliff Cave" [WRLD:00020DCB] at -36,4)) has invalid ObjectID 0148ED for a light module. You will not be able to save this file with ESL flag active
[00:00] Errors have occured. At least one file was not saved.
```

The Form IDs are, in other words, not the correct format for ESL space. Thankfully, this is something SSEEdit can adjust for us.

- Right-click the plugin in the left pane and click **Compact FormIDs for ESL**.
- Confirm when the warning window pops up.

![Compact Form IDs](/Pictures/bg/core-module/compact-form-ids.png)

### Risks of Compacting

Another warning will follow and this one merits some discussion.

Remember that records are identified by their Form IDs, also by other plugins. If we renumber the Form IDs here and later install a mod that touches the hand-placed flora from No Grass In Caves that second mod would dissolve into a mess of errors because it would be unable to locate the original records it was trying to edit. For example, it was looking for `08002FE7` but that Form is now `FE00381E`.

{{< alert color="info" >}}Compacting a plugin's Form IDs will break any plugins that it is a master for.{{< /alert >}}

There are two possible solutions:

1. Avoid compacting Form IDs in plugins that are likely a master to many other plugins (i.e., that have many patches).
2. Compact Form IDs in plugins only when their dependent plugins are also present in SSEEdit at the time.

In the latter case, those dependent plugins would be updated automatically.

### Compacting Form IDs 2

Since I never encountered a mod that modifies No Grass In Caves' hand-placed flora, I will go ahead and click **Yes** to the warning about changing Form ID. The process will only take a few seconds.

Afterwards, you can add the ESL flag in the **Plugin Header**. Close SSEEdit and save your changes.

### Documenting Changes

ESL-flagging a plugin (regardless of whether Form IDs are compacted) obviously always requires modifying the original plugin which is something we could so far avoid by overwriting with new plugins. Of course, any changes you make to a given plugin are lost upon updating.

This does not necessarily mean that you should never change an original plugin (though try to do it only if there is no other option), but I recommend documenting the changes you made.

{{< alert color="info" >}}**This step is optional.** I understand that I am unusually obsessed with documenting everything, but I do strongly believe that it is worth the effort. You cannot possibly remember all your custom edits for several hundreds or thousands of mods.{{< /alert >}}

Mod Organizer 2 features a very helpful **Notes** tab for each mod.

- Double-click **No Grass In Caves** in your mod order and switch to the **Notes** tab on the far right.

There are two empty spaces here for notes. The bottom one offers ample room for detailed jottings, whatever you are looking to document, while the top one is better suited to a few short keywords which will be visible at a glance in the mod order's **Notes** column.

- Add `Compacted Form IDs and ESL-flagged the plugin.` to the space at the top.

Once you close the window, the note will show up in your mod order.

![Compact Form IDs](/Pictures/bg/core-module/ngic-mo2-note.png)

---

#### Please continue with [Step 5](/bg/core-module/step5/).