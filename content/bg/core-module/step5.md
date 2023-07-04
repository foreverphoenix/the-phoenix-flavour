---
title: "Step 5"
weight: 5
type: docs
description: >
  Plugin conflicts and conflict resolution.
---

{{< alert color="info" title="Summary" >}}
> This step covers the three types of conflicts between plugins and how to address them.{{< /alert >}}

## Understanding Conflicts

Plugins interact with each other in various ways. As we have learned, if multiple plugins modify the same record, the game will only consider the changes from the plugin which loads last.

{{< alert color="warning" >}}Multiple plugins making different changes to the same record create a **conflict**.{{< /alert >}}

A load order must always be checked for conflicts and many conflicts need to be addressed in some way in a process that is known as conflict resolution. This process can be *partially* automated; however, that is not something I will cover in this guide. If you understand manual conflict resolution, you will automatically (hah!) be able to figure out automation tools.

{{< alert color="info" >}}Conflict resolution is one of the most important and most time-consuming steps in building a modded setup, alongside consistency patching and asset management.{{< /alert >}}

In this step we will discuss three types of conflicts, when and why they arise, how to recognise and assess them, and how to address them. In order to do so, we need to install a few additional mods first which will provide us with examples.

## Example Mods for CR

### MO2 Separators

Because we like doing things systematically and in a clean fashion, we will start by adding a few new separators in Mod Organizer 2 to sort the mods that will be added in the next step:

**Create the following separators in Mod Organizer 2:**

- Lighting
- Water

Move both above the **Grass Overhaul** separator in the mod order.

### Realistic Water Two

Realistic Water Two is one of the most popular water overhauls and happens to be my personal favourites. Installing it now does not tether you to RW2, you can always uninstall it and use something else later on.

- Download and install [Realistic Water Two](https://www.nexusmods.com/skyrimspecialedition/mods/2182?tab=files).

Wait, what is that?

We are looking at our first **FOMOD installer**. The acronym hails from the Fallout New Vegas days and stands for **F**allout **Mod** Archive. It allows for a modular installation which may include optional files like patches. Mods with FOMOD installers are common.

- For the time being, simply click **Next** and **Install**.
- Drop the mod below the **Water** separator and activate it.

### Relighting Skyrim

Relighting Skyrim is a low-impact lighting overhaul focusing on fixing light sources and adding new ones where vanilla is missing them. Once again, you are free to replace it with a different mod later on.

- Download and install [Relighting Skyrim](https://www.nexusmods.com/skyrimspecialedition/mods/8586?tab=files).

Here is another FOMOD installer.

- Click **Install** to keep the default selections (full version with USSEP support).
- Drop the mod below the **Lighting** separator and activate it.

### Mod Order

- **Official Master Files**
- **Creation Club**
- **Script Extender**
- **Essential Mods**
- **Lighting**
  - Relighting Skyrim
- **Water**
  - Realistic Water Two
- **Grass Overhaul**

### Load Order

Plugins highlighted in <mark>green</mark> are new additions.

- (Official Master Files + Creations)
- ***Unofficial Skyrim Special Edition Patch.esp***
- ***Disable USSEP Book.esl***
- <mark>***RealisticWaterTwo - Resources.esm***</mark>
- <mark>RealisticWaterTwo.esp</mark>
- *NoGrassINCaves.esp*
- <mark>RelightingSkyrim_SSE.esp</mark>

<font size=2>*Yes, this load order is terrible. That will be the point of the exercise!*</font>

## Finding Conflicts

Conflicts can be identified by applying a filter in SSEEdit.

- Load up your plugins in SSEEdit.
- Right-click anywhere in the left pane and select **Apply Filter**.
- Click the **Add** button at the top to create a new filter.
- Name it **Conflict Resolution** and click **OK**.

Your new filter will be selected automatically. We will want to check the following options:

![CR Filter](/Pictures/bg/core-module/cr-filter.png)

{{< alert color="info" >}} The two options near the top will visualise conflicts which makes finding them infinitely easier. Flattening CELL records helps with viewing the Cell and Worldspace categories without having to click through blocks and sub-blocks.{{< /alert >}}

- Click the **Save** button at the top to save the new preset.
- Click the **Filter** button at the bottom to apply it.

This will take about a minute. You can proceed once the log returns `Done: Applying Filter`.

## Harmless Conflicts

As you can see, our load order is very colourful now, meaning there are a lot of conflicts.

{{< alert color="warning" >}}Plugin interactions (conflicts) are common and not all conflicts are harmful. In fact, most conflict are fully intentional. The process of reviewing conflicts is not about making everything "green" in SSEEdit, but assessing which conflicts are <u>not</u> intentional.{{< /alert >}}

Conflict resolution therefore requires an understanding of <u>why</u> a given plugin is making certain changes and you will run into situations where you simply do not know what an edit means. In such cases, use common sense, refer to the mod page, or ask in the comments.

Let’s have a look at a harmless conflict that is intentional and requires no intervention:

- In SSEEdit, search for the **Form ID** `000695BC`.

![Find Harmless Conflict](/Pictures/bg/core-module/find-harmless-conflict.png)

SSEEdit will take us to the matching record which is a reference defined in *Skyrim.esm* placing a copy of the static **IceCandleLight01** in a cell in the [Kilkreath Ruins](https://en.uesp.net/wiki/Skyrim:Kilkreath_Ruins) dungeon.

{{< alert color="info" >}}This record and others are highlighted in red in the left pane because they contain conflicts.{{< /alert >}}

Specifically, changes from **Update.esm** are being overwritten by **RelightingSkyrim_SSE.esp**:

![Find Harmless Conflict](/Pictures/bg/core-module/rs-update-conflict.png)

So what in Talos' name means "Unknown" which is where the conflict is located? Nobody knows. Most record types have some of these "unknown" values and they can be largely ignored. They are data in the plugin which are not decoded / defined in SSEEdit, presumably something generated by the CK.

Common sense tells us that conflicts between mods and their master files are generally intentional. They would not require the master if they were not trying to change something about it.

It also tells us that **Relighting Skyrim** probably has good reasons for modifying data related to light as that is within the scope of the mod. For example, the records below our current example are four copies of `IceTorch01NS_FastDesat` placed in the same cell where **Update.esm** changes the `Fade 1.35+/-` value, and this change is overwritten once again by **RelightingSkyrim_SSE.esp**. That is obviously intentional.

Finally, we can tell that the reference object (the candle) is being disabled anyway, so even if **Update.esm** were making relevant changes (i.e. to the position of the candle) it would not matter as it would not show up in game at all. 

{{< alert color="success" >}}In conclusion: The conflict is harmless and intentional. There is no cause for action.{{< /alert >}}

## Conflicts requiring load order changes

As for conflicts which require intervention, there are two subtypes: One can be fixed by changing the load order, the other requires a patch.

Let us first look at a conflict that can be resolved by adjusting the load order.

- In SSEEdit, search for the FormID `002C965`.

This will take us to the parent record for the Darkwater Pass worldspace, highlighted in bright red. A conflict!

![Worldspace Conflict](/Pictures/bg/core-module/worldspace-conflict.png)

### CELL Record ITMs

If you look at the **RelightingSkyrim_SSE.esp** layer, you will see the grey font and recognise it as an **ITM** record (identical to master). That means it is a copy of the same record from **Skyrim.esm** with zero modifications. It currently overwrites **RealisticWaterTwo.esp**, negating its change to `NAM2 - Water`.

Does that mean Relighting Skyrim is a "bad" mod because it includes an ITM?

No. In fact, this ITM is perfectly normal.

Previously, we discussed that the **Cell** and **Worldspace** categories consist of **CELL** records which in turn contain references.

{{< alert color="info" >}}When a plugin edits a reference it will also contain a copy of the CELL record which the reference is located in.{{< /alert >}}

This copy is typically an ITM as nothing is changed within it. A good example is our previously created **Disable USSEP Book.esl**:

![Cell Record ITMs](/Pictures/bg/core-module/cell-record-itms.png)

### Late Loaders

Though CELL record ITMs records are common, the implications are important to understand: Even if a plugin only makes a tiny adjustment to a pebble in a stream somewhere in the Falkreath forest, it <u>will</u> contain ITM copies of the CELL and the worldspace's parent record where it potentially overwrites other plugins that actually modify the parent record.

That is exactly what is happening in our initial example, `002C965`, where Relighting Skyrim contains an ITM copy of the parent record of the Darkwater Pass worldspace and unnecessarily reverts the Realistic Water Two edit back to vanilla.

{{< alert color="info" >}}Fortunately, the amount of plugins modifying CELL parent records is comparatively small. They are usually found in water, lighting, audio, and map mods.{{< /alert >}}

**Realistic Water Two** is one such mod with numerous edits to parent records. We can easily resolve most potential conflicts by loading the plugin very late in the load order, below other mods which are more likely to contain only ITMs of the same parent records. That way, no conflicts will arise to begin with.

{{< alert color="info" >}}Plugins that are supposed to be placed late in the load order to avoid unnecessary conflicts are referred to as **late loaders**.{{< /alert >}}

### Load Order Adjustment

Our example conflict between **Relighting Skyrim** and **Realistic Water Two** - and a second one in the *Frostmere Depths* worldspace - can thus be resolved by simply adjusting the load order.

The same is true for current conflicts between **Relighting Skyrim** and **No Grass In Caves** which you can see if you expand the latter mod's Worldspace section. It adds the **No Grass** flag to multiple parent records which is negated by ITMs in RS. Switching their load order will allow NGIC to overwrite RS and solve the problem.

<font size=2>*As you may have noticed, NGIC also has conflicts with RW2 that are not so easily resolved. We will consider those soon.*</font>

- Close **SSEEdit**.
- Drag and drop **NoGrassINCaves.esp** <u>below</u> **RelightingSkyrim_SSE.esp**.
- Drag and drop **RealisticWaterTwo.esp** to the bottom of your load order.

![Load Order Adjustment](/Pictures/bg/core-module/load-order-adjustment.png)

- Reopen SSEEdit.
- Double-click **RealisticWaterTwo.esp** and check the **Worldspace** category.

Both *Darkwater Pass* and *Frostmere Depths* are now highlighted in yellow, meaning that Realistic Water Two modified the original records without creating conflicts. The *BlindCliffCaveWorld* and *FallowstoneCaveWorldStart* worldspace parent records have conflicts which will be addressed in the next step.

Finally, the conflict in *DLC2SolstheimWorld* is caused by the Fishing creation which modified, probably accidentally, the parent record. That is annoying, but since the changes are reverted back to vanilla by later plugins, it does not matter.*

<font size=2>\**If you cannot see the conflict with the Fishing creation, you probably enabled the USSEP ModGroup.*</font>

## Conflicts requiring patches

Finally, there are conflicts of the type which are unintentional and can only be resolved by a patch.

This is the case when multiple plugins modify the same record and you wish to retain changes from several of them: An additional layer must be created where all these changes are consolidated, creating a **patch**.

- Double-click **NoGrassInCaves.esp** in the left pane.
- Expand the **Worldspace** category.

Here we can see that nearly all parent records in this plugin have conflicts though it is winning most of them without creating conflicts (green font on yellow background). If you check the green records, you can see that No Grass In Caves is also a typical late loader as it does modify the parent records and is correctly overwriting the ITMs in other plugins.

However, conflicts do appear in two of the parent records: *BlindCliffCaveWorld* and *FallowstoneCaveWorldStart*. Looking at these records, you will notice that both No Grass In Caves and Realistic Water Two are making relevant changes, but Realistic Water Two is winning the conflict because it is placed lower in the load order. If the positions were reversed, No Grass In Caves would win, but then the water changes would not appear in game.

**In order for both mods to function as intended, a patch is required.**

### Creating a patch

Just as we did earlier to disable the USSEP book, we need to create a new layer (a new plugin) to apply our changes to.

- Select one of the two worldspace parent records containing a conflict.
- Right-click the **RealisticWaterTwo.esp** layer (column) in the right pane.
- Select **Copy as override into** and confirm when the warning pops up.
- In the plugin selection window, select the **\<new file>.esp** template <u>with the ESL flag</u> and click **OK**.

At this point, we have two options: Either we create a **Conflict Resolution Patch.esp** where this and future conflicts are collected and resolved. This is a common practice and one that I used for a long time. However, I have since come to the conclusion that it is better to create many separate patches instead.

Why is that?

**Separate patches are much easier to manage.** When mods are removed, you do not have to modify one big plugin, removing references and cleaning masters. You only have to disable the specific patches for it. They are also easier to update when a mod was updated.

Because we can ESL-flag these small patches, we can literally create hundreds and thousands of tiny patches without ever having to merge them together.

{{< alert color="warning" >}}In conclusion: I strongly recommend creating <u>separate</u> patches to address conflicts between different mods.{{< /alert >}}

- Name your new plugin **Realistic Water Two - No Grass In Caves Patch** and click **OK**.

Of course, there is still a conflict in our newly created patch. To resolve this, simply drag (forward) the changes under `DATA - Flags (sorted)` from the **NoGrassInCaves.esp** column into our new patch:

![Resolve Worldspace Conflict](/Pictures/bg/core-module/resolve-worldspace-conflict.png)

The record should now be displayed in green. (The copy in the expanded **NoGrassInCaves.esp** plugin is still red, but that is because the UI does not update everywhere. If you click on it, the conflict is shown as resolved there, too).

Now repeat the process for the second conflicting parent record. When choosing where to create a new layer, do not select a new plugin, but use the existing patch instead.

![Resolve Worldspace Conflict](/Pictures/bg/core-module/copy-into-patch.png)

Finally, forward the remaining edit in the second record into the patch plugin. All is pretty and green now.

Close **SSEEdit** and click **OK** to save your new plugin.

### Cleanup

As usual, the Mod Organizer 2 caught our new plugin.

- Right-click the ***Overwrite*** and select **Create Mod**.
- Enter **Realistic Water Two - No Grass In Caves Patch** as the name and click **OK**.
- Leave the new mod <u>below</u> **Realistic Water Two** and activate it.

In the load order, the new plugin will appear at the bottom automatically, located below both its masters.

In the **Notes** tab in MO2, I added a quick `Resolves minor worldspace parent record conflicts.` for the new patch to remind myself of what it does. Once you have a couple hundred custom patches flying around you will be very grateful to your past self for having some documentation, trust me on that.

## A Note on LOOT

{{< alert color="info" >}}The following section discusses my views on a tool called LOOT. Feel free to move on to [Step 6](/bg/core-module/step6/) if you are not interested.{{< /alert >}}

By now, you may have been wondering when I was going to mention LOOT. Is that not how load order is managed? 

Okay, here is the thing.

**Figuring out the ideal load order is hard, actually.** It is time-consuming, especially for large load orders - TPF has well over 1,000 plugins, and it is far from the biggest setup out there. I spend a lot of time, hours upon hours, in SSEEdit, looking at conflicts to figure out which are harmless, which can be resolved through load order adjustments, and which require patches.

It is thus unsurprising that efforts have been made to automate this process. The tool BOSS was made for sorting plugins in the Oblivion modding days; it has since been superseded by LOOT. 

Drawing on a user-created masterlist, LOOT attempts to sort your plugins in a way that minimises conflicts. This is inherently imperfect as it would be impossible to create a database accounting for every single mod and possible conflict.

{{< alert color="warning" >}}LOOT is capable of one thing: Solving load order conflicts <u>if</u> the conflict in question is on the masterlist. LOOT cannot create patches or even discover conflicts by itself.{{< /alert >}}

That does not mean LOOT is bad, period.

**What is bad is the widespread notion that modding = installing mods >> running LOOT >> playing the game.**

You can observe the result of this idea every day on the Skyrim modding subreddit, in Nexus comments, on various Discord servers. It is unfortunately reinforced by many mod authors who recommend running LOOT on their mod pages without clarifying that simply running LOOT does not a functional modded setup make. Plenty of "modding guides" further perpetuate this idea.

👏 **LOOT will not fix your load order.** 👏

That being said, LOOT <u>can</u> speed up the process of fixing your load order by improving your baseline. Some of the most talented mod authors and list curators I know are using LOOT with a multitude of custom rules to manage their load order and consider this the most efficient way.

<font size=2>*I do want to stress that LOOT was never <u>marketed</u> as this magical fix-all solution. It is the community hivemind that has portrayed it as such.*</font>

{{< alert color="info" >}}This guide will use LOOT later on, though not for load order management. I personally do not consider custom LOOT sorting rules, groups, etc worth the effort which is my <u>subjective opinion based on my own experiences</u> and not an objective fact. However, since I happen to be writing this guide, my subjective opinions *are* relevant.{{< /alert >}}

---

#### Please continue with [Step 6](/bg/core-module/step6/).