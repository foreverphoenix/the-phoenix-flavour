---
title: "Step 8: Plugin Basics"
weight: 8
type: docs
description: >
  Understanding plugins, records, and layers.
---

## Opening SSEEdit

Let's go find the book in SSEEdit.

- Click the **SSEEdit** icon in your tool bar to quickly launch it through MO2.
- If the changelog pops up, check **Don't show again until changed** and click **OK**.
- If the the dev message appears, check **Don't show again for a while** and click **Close**.

In the background, MO2 will be locked now. This will always happen when you launch tools through its interface to prevent you from changing anything in the virtual data folder while that is used by another tool.

In **SSEEdit**, you will now see your load order ("Module Selection"). All plugins should be checked by default, so go ahead and click **OK**. Next, you will be asked about **ModGroups**. We will talk about modgroups later on, for now, please check the one for the USSEP and click **OK**.

SSEEdit will begin loading up your plugins which will take a moment. You can follow the tool's progress in SSEEdit and, spoiler alert, we are going to speed this process up in the future. While SSEEdit loads your plugins, it will display random tips.

After a while, SSEEdit will ask you about activating **ModGroups**. This is because the USSEP comes with a ModGroup file that was now recognised by the tool. We will talk about ModGroups and their functionality later, for now leave the USSEP ModGroup disabled and just click **OK**.

The SSEEdit log should now return `Background Loader: finished`, so we can proceed.

### Plugin Records

In the left pane of SSEEdit, you can see your list of plugins, the load order.

- Double-click the **Unofficial Skyrim Special Edition Patch.esp** to expand it.

The USSEP is huge. You will immediately see a long list of record types unfolding, each of which contains dozens if not hundreds of individual records.

- Double-click the **Book** category to expand it.
- Select the first record in the list, `[00015475] DB06Schedule`.

![USSEP Book Record](/Pictures/embers/module-1/ussep-book-record.png)

From the index `00` we can tell that the record originates in **Skyrim.esm**. We can see the book's full Form ID in the first column in the left pane of SSEEdit.

The second column is the **EditorID**, abbreviated as EDID. This is another way to refer to a record (which is also used in scripts sometimes). Almost all records contain references to other records which consist of their EditorID, their Signature (the record category they belong to), and their Form ID.

For our current book, that would be: `DB06Schedule [BOOK:00015475]`.

The third column will display the **Name** of the record which is also the name you will see ingame. Not all records have names. Names are also not unique. They are easier to understand, but not useful for identifying a record.

### Layers and Priority

Let's have a look at the right pane now which displays more details:

![USSEP Book Record Details](/Pictures/embers/module-1/ussep-book-record-details.png)

As you can see, both the right pane side and the record name in the left pane are highlighted in green. This means that the record is overwritten by another plugin, but the overwriting plugin did not remove anything from the original.

You can see the original record as defined by **Skyrim.esm** in the first column, then the USSEP version in the second column. These columns correspond to the plugins and are sorted in the order of the plugins.

Each of these columns is a **layer** and completely overwrites the earlier ones. Imagine placing a stack of papers on your desk: You can only read the one on the top. Similarly, the Skyrim engine can only read the final layer that covers up all that were placed before it. You could now change anything you wanted in the **Skyrim.esm** layer; as long as the USSEP overwrote it, you would not see a change ingame.

Later on with a longer load order, you may have multiple plugins overwriting a single record. Each of them may make a different change, but the engine will only read the one at the bottom of the load order and completely ignore the rest. This is why *patching* is so important: It means consolidating all desired changes in one final layer.

The actual change in the above example is in the **Book Text** which is conveniently highlighted in green in the USSEP column. You can double-click it to compare the changes with the original.

## Disabling the USSEP Book

We can easily find the book that we want to disable by searching for its unique Form ID:

- In the **Form ID** search box above the load order, enter the book's base ID `050B1985` and press **Enter**.

![Search FormID](/Pictures/embers/module-1/sseedit-search-formid.png)

You will notice that, unlike the other book records, this one is displayed in white (blue in my screenshot because it is currently selected). White records are records that are not overwritten at all: The book was newly added by the USSEP, it was *defined* in its plugin. Very often mod authors prefix their **EditorIDs** with their name or the mod name like you can see here. This makes them easier to find.

So what are we going to do with it?

Theoretically we could simply right-click and delete the book's base record. However, the reference record placing the book in the Temple of Kynareth links back to the book's base record and would throw an error if it were just deleted. These kinds of errors can cause crashes and other issues.

![USSEP Book Error](/Pictures/embers/module-1/ussep-book-error.png)

Instead, it is much better to simply leave the base record in place and *disable* the object in the ref record.

### Finding the REFR

One way to find the ref record would be to search for the RefID like we did before. However, there is another way of quickly tracking down referenced records:

- With the **USSEPUnwantedEffectsRemoverBook** record selected, click the **Referenced By (1)** tab at the bottom of the right pane.
- Double-click the one ref record listed here to immediately switch to it.

![Find Ref Records](/Pictures/embers/module-1/find-ref-records.png)

And there we go. The record in the left pane is shown in white (new and not overwritten) and in *italics* (meaning it is injected):

![USSEP Book Ref](/Pictures/embers/module-1/ussep-book-ref.png)

Under **NAME - Base** in the right pane, you can see the full name of the book record (consisting of EDID, Name, Signature, and BaseID). If you scroll further down, there is the **DATA - Position/Rotation** section which defines the book's exact placement. This would best be edited in the Creation Kit where you have a visual preview. Various other parameters are greyed out because they are unused.

### Creating a new layer

While it is entirely possible to edit the ref record directly, it would mean that you would have to do it all over again whenever the USSEP updated. For any edit like this and later on for patches I highly recommend creating new plugins instead of directly editing the mod(s) in question. It is also much easier to keep track of custom changes if they are in separate plugins.

- Right-click the **Unofficial Skyrim Special Edition Patch.esp** column in the right pane.
- Select **Copy as override into ...** to copy the layer into another plugin.

![SSEEdit Create Layer](/Pictures/embers/module-1/sseedit-create-layer.png)

The warning window that now appears will always show up the first time you edit anything in an SSEEdit session. It can be turned off and I recommend doing that eventually. When changing anything in SSEEdit, it is important to keep in mind that there is no "Undo" button; if you make a mistake, you need to restore the previous state manually or close without saving your changes and start over. It is also possible to save manually during a longer session. However, this is mostly irrelevant for now.

- Click **Yes I'm absolutely sure** to acknowledge the warning and proceed.
- A new window will pop up with various different plugins that the record can be copied into.
- Check the third **\<new file>.esp** option (with ESL) and click **OK**.
- Enter **Disable USSEP Book** as the name of the new plugin and click **OK** once more.

![New ESPFE Plugin](/Pictures/embers/module-1/new-espfe-plugin.png)

The new plugin was created and will appear at the bottom of the plugin list in the left pane. Scroll down and expand its **Cell** records until you find the ref record added by the USSEP. As you can see it is highlighted in green since the original record was overwritten now:

![USSEP Book ITM](/Pictures/embers/module-1/ussep-book-itm.png)

In the new plugin, the font colour is grey instead of purple. That means the record is an **ITM**, or Identical to Master. The master is the USSEP because that is where the original ref record was defined in and the new plugin requires the USSEP for that reason. And of course it does not (yet) contain any changes, so it is identical to it.

### Adding a record flag

In order to make the book not show up ingame, we can use a **Record Flag**. Scroll up to the top of the record in the right pane to find the **Record Flags** line which is currently empty.

- Right-click the empty space next to **Record Flags** and select **Edit**.

A new window will pop up with a list of options that you can check. Near the top of that list is a **Delete** option which is *not* the one you should choose. Flagging records as deleted will cause crashes if they are referenced by other records and it is considered best practice to always use the **Initially Disabled** flag instead.

- Check the box for **Initially Disabled** and click **OK**.

![Add Record Flag](/Pictures/embers/module-1/add-record-flag.png)

> **Initially Disabled** means a record can potentially be re-enabled by a script later on. For example, certain coffins are flagged as initially disabled. If an NPC dies, their coffin in the Hall of the Dead of their home city will be enabled and thus become visible to the player.

### Saving your changes

Saving changes made in SSEEdit is a slightly unintuitive process: You actually have to *close* the tool to be prompted to save what you changed (unless you save manually).

- Close **SSEEdit** (click the red X in the upper right corner).
- A window with all plugins edited in that session will pop up. Only the **Disable USSEP Book.esp** should be listed here.
- Make sure that the plugin is checked and click **OK**.

## The New Mod

Back in Mod Organizer 2, you will notice that the new plugin is already showing up in the load order. If you click on it, the ***Overwrite*** at the bottom of your mod order will light up, which means that is where your new plugin is currently located.

![Plugin in Overwrite](/Pictures/embers/module-1/plugin-in-overwrite.png)

So what is the ***Overwrite***?

### MO2 Overwrite

We already established that, by default, Skyrim mod files are placed in the data folder, but that Mod Organizer 2 has a virtual file system to circumvent this. Some modding tools will attempt to place their own files into the data folder. MO2 will catch these files and deposit them in the ***Overwrite*** folder at the bottom of your mod order instead.

The folder is named that because it does overwrite: Mod order, like plugin order, is priority-based. In case of conflicts, files that are placed lower win and overwrite. Files in the ***Overwrite*** will always be loaded in the virtual data folder and overwrite everything else so it is important to keep track of its contents.

MO2 will even warn you if there are files in that folder: The warning icon in the top right (above the executables) will have lit up. There are various potential issues that MO2 is capable of detecting, but if you click on the icon now, it will be reminding you about files in your ***Overwrite***.

So let's check what we have:

- Double-click the ***Overwrite*** folder at the bottom of your mod order.

![Lesson Four Overwrite](/Pictures/embers/module-1/ussep-book-overwrite.png)

Among the files here is, predictably, our newly created plugin. The **SSEEdit Cache** folder contains refcache files which we will take care of in just a second.

### Creating a new mod folder

For the new plugin, we are going to create a new **mod folder** in Mod Organizer 2. Remember, all the mods displayed in the mod order right now are just folders within `\Mod Organizer 2\mods\` that contain mod files.

- Click the tools icon above your mod order and select **Create empty mod**.
- Name your new mod **Disable USSEP Book** and click **OK**.

![Create empty mod](/Pictures/embers/module-1/create-empty-mod.png)

Functionally, all this did was create a new folder under `\Mod Organizer 2\mods\Disable USSEP Book\` and you could simply move the plugin from `\Mod Organizer 2\overwrite\` into that new folder manually. Of course, it is much faster to just move the file directly through the MO2 UI, but it is good to know how the tool works behind the curtains.

- In Mod Organizer 2, drag the **Disable USSEP Book.esp** from the ***Overwrite*** into the new **Disable USSEP Book** mod.

![Overwrite To Mod](/Pictures/embers/module-1/overwrite-to-mod.png)

- For now, simply delete the **SSEEdit Cache** folder in the ***Overwrite*** (we will regenerate it).
- Drag the new **Disable USSEP Book** below the USSEP in your mod order and activate it.

### Renaming the plugin

In the next step we are going to need a plugin with a very specific format for demonstration purposes. Don't worry about the implications of this change yet, it will be explained soon. For now, follow these instructions to turn the plugin into a full ESL:

- Double-click **Disable USSEP Book** in your mod order.
- Switch to the **Filetree** tab (furthest on the right).
- Select the plugin and press F2 to rename it.
- Only change the file extension from **ESP** to **ESL**.
- Once done, close the window again.

![Custom Plugin ESL](/Pictures/embers/module-1/custom-plugin-esl.png)

The plugin will now be disabled and placed at the bottom of your load order in the right pane. This is normal. Re-enable it (check the box) and manually place it below **Landscape and Water Fixes.esp**.

## SSEEdit Ref Cache

We already talked about reference records: They define the placement of various objects in the world. These objects may include books like the USSEP one, but also other items (such as food or weapons), furniture, NPCs, light sources, or invisible triggers (that fire scripts when you cross them). Every single dead shrub in Skyrim has its unique ref record. There are a *lot* of dead shrubs in Skyrim.

In order to save time loading all those thousands upon thousands of references, SSEEdit creates **.refcache** files upon loading a plugin for the first time. These file store the Ref Form IDs, and they *significantly* speed up load times when opening large load orders in the tool (cutting it down from several minutes to 20 seconds or less).

By default these refcache files would be stored in `\Skyrim Special Edition\Data\SSEEdit Cache\` if Mod Organizer 2 didn't catch them in its Overwrite. However, the Overwrite is not really an ideal place to store these files. One alternative would be placing them in a mod folder, but then you would have to manually move the new refcache files every time you added a plugin.

Fortunately, there is a far more elegant solution.

### Define Output

With the `-c` argument, we can set an output folder for the refcache files generated by SSEEdit. I personally prefer simply generating those files into the tool's installation directory. If you delete its contents before updating to a newer version, the old refcache files will be deleted as well and regenerated the first time you open your load order with the updated version of SSEEdit. 

- In Mod Organizer 2, once again click the gears icon in the Toolbar to open the **Executables** settings.

![MO2 Executable Settings](/Pictures/embers/module-1/mo2-executables-settings.png)

- Select **SSEEdit** in the list of executables.
- Under **Arguments**, add a space at the end and then the `-c:"filepath"` argument along with the file path.

The file path will obviously depend on where you set up **Your Modding Folder**. It should end in a `\cache\` folder. This folder does not have to exist, it will be created by SSEEdit upon generating the first cache files. For me, the argument looks like this:

- `-c:"D:\Modding\Embers\Tools\SSEEdit\cache\"`

Once you have entered the argument with the correct file path for your system, click **OK**.

> Note that the file path **must** end on a trailing backslash `\`. Otherwise it simply will not work, and Mod Organizer 2 will continue to place the refcache files into the Overwrite.

![SSEEdit Cache Argument](/Pictures/embers/module-1/sseedit-cache-argument.png)

The next time you open your load order in SSEEdit will once again take a while as refcache for the official master files and all plugins installed so far will be generated, but after that the load times should be much shorter.

## Ingame Test

Now that we have created our first plugin tweak and cleaned everything up, it is time to jump ingame again to check if the plugin works as intended.

- Launch **SKSE** through Mod Organizer 2.
- Select **Continue** in the main menu to load your previously created save.

And ... gone!

![USSEP Book Removed](/Pictures/embers/module-1/ussep-book-removed.jpg)

You may wonder why we went through the process of digging through SSEEdit to disable a completely inconsequential feature before we even talk about load order and plugin types.

This step was not about the book. It was about plugin structure: About records and form IDs and layers. Load order should be more than a theoretical idea now, it's a tangible concept that you have seen in action. You have seen overwrites, you have created your own overwriting layer to make a change, and you made sure that it works.

When we discuss plugin types and load order in the next step, these concepts will make a great deal more sense with the knowledge on plugin structure we gained in this one.