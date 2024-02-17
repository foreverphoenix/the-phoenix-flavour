---
title: "Step 3"
weight: 3
type: docs
description: >
  Plugin structure: Dependencies, records, layers, and Form IDs. SSEEdit.
---

{{< alert color="info" title="Summary" >}}
> This step covers the basic architecture of Bethesda plugins and how they can be modified.{{< /alert >}}

## Unofficial Skyrim Special Edition Patch

We will start by installing an example mod.

The **Unofficial Skyrim Special Edition Patch** (USSEP) is an ambitious project aiming to squash the various bugs and inconsistencies never addressed by Bethesda. It is probably the single most popular Skyrim mod in existence.

{{< alert color="info" >}}The USSEP is not without controversy. Many of its changes have been criticised for being out-of-scope which is rarely received well by the somewhat eccentric project lead. Nevertheless, I highly recommend the mod, especially to newcomers, because it does fix a lot and because not using it limits your options where other mods are concerned.{{< /alert >}}

### New Separator

First, we will add a new separator:

- [Create a new separator](/Pictures/skyforge/mo2-create-separator.png) in MO2 and name it **Essential Mods**.
- Leave it at the bottom of the left pane, below **Address Library for SKSE Plugins**.

### USSEP Installation

Now go ahead and grab the latest version from the Nexus:

- Download and install the [Unofficial Skyrim Special Edition Patch](https://www.nexusmods.com/skyrimspecialedition/mods/266?tab=files).

{{< alert color="info" >}}The USSEP requires the four free creations which is why earlier instructions ensured they were installed and activated.{{< /alert >}}

## Plugins & Load Order

**Plugins** contain a variety of game data. For example, they determine an NPC's hairstyle, where the NPC is placed in the game world, what it holds in its inventory, and much more.

After enabling the USSEP, a new plugin will appear in the **Plugins** tab in the right pane which is also called the **load order**. Currently, the USSEP is at the bottom of the load order. All other files above are greyed out because they are official game files (vanilla and creations) because their load order position are hardcoded and cannot be changed.

### Dependencies

By adding one plugin as a **master** to another plugin, you can modify its contents. However, the dependent plugin will now require its master to function. All plugins require at least **Skyrim.esm** because most game data is defined in that plugin.

{{< alert color="info">}}Because all mods require one or more of the five vanilla ESMs they are known as the **official master files**.{{< /alert >}}

You can view a plugin's masters by hovering over it in the MO2 UI:

![USSEP Masters](/Pictures/skyforge/beginners-guide/ussep-masters.png)

If a master is missing, MO2 will promptly warn you. Uncheck one of the four free creations in the mod order to trigger the warning.

{{< alert color="warning" >}}A missing master is always a **critical issue** and must be fixed.{{< /alert >}}

(Remember to re-enable the creation.)

![USSEP Missing Masters](/Pictures/skyforge/beginners-guide/ussep-missing-masters.png)

## SSEEdit

In order to understand how plugins are structured, why they are dependent on their masters, and why missing masters are such a big deal, we need to have a proper look at their inner workings.

While plugins can also be created and edited in Bethesda's official modding tool, the **Creation Kit**, the community-made **SSEEdit** is much better suited for beginners to get an idea of how plugins are structured and how load order works.

{{< alert color="info" >}}SSEEdit does not replace the Creation Kit, nor does the Creation Kit replace SSEEdit. The tool to use always depends on the type of plugin you are working on and what you are trying to do. For example, for the vast majority of tweaks, edits, and patches, SSEEdit is the way to go because it is very good at visualising conflicts and interactions.{{< /alert >}}

Set up a [Tools Folder](/skyforge/tool-setup/tools-folder/) and install [SSEEdit](/skyforge/tool-setup/sseedit/).

## The Unwanted Effects Book

Equipped with SSEEdit and an example mod, we can now take a look at a practical example demonstrating how plugins are structured.

Enter the **Unwanted Effects Book**. 

Among vanilla Skyrim's colourful assortment of bugs are certain active effects, applied by spells for instance, that may get "stuck" on the player after they are supposed to expire. The **Unofficial Skyrim Special Edition Patch** fixes these effects, but it also adds an option for the player to rid themselves of any leftovers. Initially, this fix could be accessed through a shrine in the Temple of Kynareth in Whiterun, but was later moved to a book added to the player's inventory upon loading the game. Following complaints about a lack of immersion, a compromise was finally reached by placing the book in the Temple of Kynareth.

Using books or powers in order to access or customise a mod's functionality was rather common before the Script Extender and SkyUI came along, although nowadays such options have largely been moved to dedicated mod configuration menus. With the release of Skyrim SE and the introduction of mods on consoles, many mod authors had to revert to these old workarounds as it is impossible to install files outside the data folder on consoles, and thus impossible to install the Skyrim Script Extender. The USSEP team does not want to move the option to an MCM or make it available only through the (in-game) console as that would not work for the XBOX and Playstation ports of the mod.

However, for us PC players, the book is mostly redundant. If you ever find yourself stuck with an active effect, you can get the book through the console very easily, so there is no need to have it lying around in the game world or lugging it around with you. Does it really break immersion? Some players are vehemently opposed to having any sort mod config items in the world. Others probably never noticed the book in the first place.

**Either way, disabling that book makes for a nice example edit, our first foray into the world of plugins.**

### More Informative Console

When trying to locate and identify an item in the game, **More Informative Console** is invaluable. It expands the console interface (which we already briefly looked at after installing SKSE) with a variety of helpful features that come in handy in the process of building a modded setup.

- Download and install [More Informative Console](https://www.nexusmods.com/skyrimspecialedition/mods/19250?tab=files).
  - *Pay attention and make sure to grab the correct version.*
- Activate the mod in your mod order.

### Finding the Book

Let's go and have a look at that book, shall we?

- Select **Skyrim Script Extender** from the MO2 executables drop-down and click **Run**.
- In the main menu, open the **console** (press the [tilde key](/Pictures/skyforge/tilde.jpg) above TAB on your keyboard).
- Type `coc WhiterunTempleOfKynareth` and press **Enter**.

The `coc` (center on cell) command is incredibly useful for testing. When used from the main menu, it will create a test character in your chosen cell with some basic equipment (check your inventory if you like).

{{< alert color="warning" >}} **The coc command should be used for testing only.** You will run into all kinds of issues if you try to use it for an actual playthrough as skipping the intro this way will cause many of the game's (and mods') scripts to never be properly initialised.{{< /alert >}}

To find the book, go from where you spawned by the entrance to the temple into the sleeping area on the right. There is a bookcase just in front of you with the **USSEP Unwanted Effects Remover** on the floor leaning against its side.

![USSEP Book 1](/Pictures/skyforge/beginners-guide/ussep-book-1.jpg)

![USSEP Book 2](/Pictures/skyforge/beginners-guide/ussep-book-2.jpg)

Now we know where the book is. How does that help us?

The USSEP plugin is big. It contains hundreds upon hundreds of records, and finding a single book among them sounds rather tedious. What you need is the book's **Form ID**, its unique identification number. To figure out that **Form ID**, we installed **More Informative Console**.

- Open the console once again and click on the book.

Here is what you should see:

![USSEP Book 3](/Pictures/skyforge/beginners-guide/ussep-book-3.png)

Everything we could possibly need to know we can see at a glance thanks to the mod. Either take a screenshot (or simply refer to mine), then **save** and **close** the game. It is time to talk about **Form IDs**.

(Yes, a warning popped up in MO2. We will deal with it in due time.)

## Form IDs

Every object, NPC, magic effect, music track, etc, in the game is defined in a unique **record** which is contained in a **plugin**.

{{< alert color="info" >}}For vanilla Skyrim, that is what the **official master files** do: Each of the five plugins contains thousands of records, one for every *thing* in the game: NPCs, magic effects, music tracks, and so forth.{{< /alert >}}

**Every record has a unique Form ID to be identified by. No two Form IDs can ever be identical.**

Form IDs consist of 8 [hexadecimal](https://en.wikipedia.org/wiki/Hexadecimal) numbers (1-9 and A-F), for example `070B1985`.

The first two denote the **Index** which refers to the load order position of the plugin that the record was initially defined in. They change depending on your load order.

The remaining six numbers will always stay the same. This is why there can never be two plugins with duplicate Form IDs: No two plugins can be loaded in the same spot in the load order which means they will <u>always</u> have a different index.

(Unless they are ESLs which all load in slot 254, or FE. But we will get to that later.)

### Base and Ref Form ID

However, if we check the info we grabbed through More Informative Console, we will notice that the book has not one but *two* Form IDs:

![USSEP Book FormID](/Pictures/skyforge/beginners-guide/ussep-book-formid.png)

What's up with that?

The **Base Form ID** is `070B1985` and describes the book itself: It defines which model it uses, what its contents are, and, in this case, what script is attached to it.

From the first two digits of the **Form ID**, the **Index**, you can tell that it is defined in the **Unofficial Skyrim Special Edition Patch.esp** plugin. If you check the load order in Mod Organizer 2, the mod index of the USSEP plugin is `07` which is identical to the index of the book's **Base Form ID**.

![USSEP Plugin Index](/Pictures/skyforge/beginners-guide/ussep-plugin-index.png)

The **Ref Form ID** is `0190001B` and describes the book's placement: That it is located in the `WhiterunTempleofKynareth` cell, that it is enabled, how it is placed, and so on.

The reason a second Form ID is needed is because you may have copies of the same object distributed throughout the game. While the book is unique right now, a Steel Sword would not be. There are dozens of hand-placed Steel Swords in Skyrim. Each of them has a unique REFR (reference) record with its unique Ref Form ID: They refer to the original item defined in the record with the Base Form ID.

{{< alert color="info" >}}Because there are so many REFR records, SSEEdit is caching them to speed up its initial processing of records (RefCache).{{< /alert >}}

### Injected Records

As you may have noticed, the **Index** for the book's **Ref Form ID** `01` actually corresponds to **Update.esm** instead of the USSEP plugin: It is an **injected record**.

This means that while the reference does not originate in Update.esm, another plugin modifying it would not have a missing master if the USSEP were not present as long as Update.esm was there. This is helpful for patchless compatibility.

For example, a mod might change the interior of the Temple of Kynareth in such a way that the USSEP book is suddenly stuck in furniture, or otherwise inaccessible or in the way. The mod author could add the USSEP as a master to their plugin and move the book out of the way, but now their Temple of Kynareth mod would always require the USSEP.

Alternatively, because the REFR record is an injected form, they could copy it into their own plugin and disable it. Record `0190001B` is injected into Update.esm, and *everyone* has Update.esm; hence, there would be no additional requirements. If the USSEP was present, the book would be removed. If the USSEP was not present, nothing would happen and there would be no errors.

{{< alert color="info" >}}Moving the book instead of disabling would not be possible because the base record is not an injected form and cannot be referenced without adding the USSEP as a hard requirement. It would have to be replaced with a dummy item.{{< /alert >}}

Injected records are inherently risky because, unlike with “normal” records, it is possible for duplicates to be present which can cause significant issues. Mod authors will only use injected records if there is no other way to ensure easy compatibility. [There is an (incomplete) list keeping track of them.](https://ck.uesp.net/wiki/Injected_Record_Registry)

## Records & Layers

Armed with all this theoretical knowledge on forms and records, we should fire up SSEEdit.

- Click the **SSEEdit** icon in your toolbar to quickly launch it through MO2.
- If the changelog pops up, check **Don't show again until changed** and click **OK**.
- If the dev message appears, check **Don't show again for a while** and click **Close**.

In the background, MO2 will be locked now. This will always happen when you launch tools through its interface to prevent you from changing anything in the virtual data folder while that is used by another tool.

In **SSEEdit**, you will see your **load order** ("Module Selection"). All plugins should be checked by default, so go ahead and click **OK**.

SSEEdit will begin loading up your plugins which should not take too long since we already generated refcache for the official master files. You can follow the tool's progress in the log. While SSEEdit loads your plugins, it will display random tips.

Once it is done, SSEEdit will ask you about activating **ModGroups**. This is because the USSEP comes with a ModGroup file that was now recognised by the tool. We will talk about ModGroups later; for now, leave the USSEP ModGroup disabled and click **OK**.

The SSEEdit log should now return `Background Loader: finished`, so we can proceed.

### SSEEdit Left Pane

In the left pane of SSEEdit, you can see your list of plugins, the load order.

- Double-click the **Unofficial Skyrim Special Edition Patch.esp** to expand it.

The USSEP is *huge*. You will immediately see a long list of record types unfolding, each of which contains dozens if not hundreds of individual records.

- Double-click the **Book** category to expand it.
- Select the first record in the list, `[00019514] DB07Journal "Cicero’s Journal - Final Volume"`.

![USSEP Book Details](/Pictures/skyforge/beginners-guide/ussep-book-details.png)

From the index `00` we can tell that the record originates in **Skyrim.esm**. We can see the book's full Form ID in the first column in the left pane of SSEEdit.

The second column is the **Editor ID** (EDID) which is `DB07Journal`. This is another way to refer to a record (which is also used in scripts sometimes). Almost all records contain references to other records which consist of their EditorID, their Signature (the record category they belong to), and their Form ID.

The third column displays the **Name** of the record, i.e., `Cicero’s Journal - Final Volume`, which is also the name you will see ingame. Not all records have names. Names are also not unique. They are easier to understand, but not always useful for identifying a record.

![xEdit](/Pictures/skyforge/beginners-guide/sseedit-columns-left.png)

### Layers & Priority

Let's have a look at the right pane now which displays more details.

As you can see, both the right pane side and the record name in the left pane are highlighted in green. **Green means that the original record is overwritten by one or more plugins <u>without</u> creating critical conflicts.**

You can see the original record as defined by Skyrim.esm in the first column, then the USSEP version in the second column. These columns correspond to the plugins and are sorted in the order of the plugins.

{{< alert color="warning" >}}Each of these columns can be thought of as a **layer**. Each layer completely overwrites the earlier ones.{{< /alert >}}

Imagine placing a stack of papers on your desk: You can only read the one on the top. Similarly, the Skyrim engine can only read the final layer that covers up the ones underneath. Here, the USSEP overwrites Skyrim.esm. You could now change anything you wanted in the Skyrim.esm layer; as long as the USSEP overwrote it, you would not see a change ingame.

{{< alert color="warning" >}}Plugins overwrite each other in the order they are loaded in. Skyrim will only read the final plugin.{{< /alert >}}

Later on, with a larger load order, you may have multiple plugins overwriting a single record. Each of them may make a different change, but the engine will only read the one at the bottom of the load order and completely ignore the rest.

**This is why patching is so important: It means consolidating all desired changes in one final layer.**

The actual change in our current example record is in the **Book Text** which is conveniently highlighted in green in the USSEP column. You can double-click it to compare the changes with the original.

![Book Changes](/Pictures/skyforge/beginners-guide/ussep-book-changes.png)

## Disabling the USSEP Book

We can easily find the book that we want to disable by searching for its unique Form ID:

- In the **Form ID** search box above the load order, enter the book's base ID `070B1985` and press **Enter**.

![Search FormID](/Pictures/skyforge/beginners-guide/sseedit-search-formid.png)

You will notice that, unlike the other book records, this one is displayed in white (highlighted blue in my screenshot because it is currently selected). **White records are records that are not overwritten:** The book was newly added by the USSEP, it was defined in its plugin, and no other plugin affects it.

{{< alert color="info" >}}Mod authors frequently prefix their **Editor IDs** with their name or the mod name. This makes them easier to find.{{< /alert >}}

So what are we going to do with the book?

Theoretically we could simply right-click and delete the book's base record. However, the reference record placing the book in the Temple of Kynareth links back to the book's base record and would throw an error if the base record it references was deleted. These kinds of errors can cause crashes and other issues.

![Book Error](/Pictures/skyforge/beginners-guide/ussep-book-error.png)

Instead, it is much better to leave the base record in place and disable the REFR record.

## Finding the REFR

One way to find the REFR record would be to search for the Ref Form ID like we did before. However, there is another way of quickly tracking down referenced records:

- With the **USSEPUnwantedEffectsRemoverBook** record selected, click the **Referenced By (1)** tab at the bottom of the right pane.
- Double-click the one REFR record listed here to immediately switch to it.

![Find REFR](/Pictures/skyforge/beginners-guide/find-refr-records.png)

There we go. Under the blue highlight (because it is currently selected), the record in the left pane has no coloured background (meaning it is new and not overwritten) and in *italics* (meaning it is injected):

![Find REFR](/Pictures/skyforge/beginners-guide/ussep-book-ref.png)

Under **NAME - Base** in the right pane, you can see the full name of the book record (consisting of EDID, Name, Signature, and BaseID). If you scroll further down, there is the **DATA - Position/Rotation** section which defines the book's exact placement. This would best be edited in the Creation Kit where you have a visual preview.

Various other parameters are greyed out because they are unused.

### Creating a new layer

While it is entirely possible to edit the REFR record directly, it would mean that you would have to do it all over again whenever the USSEP updated. For any edit like this (and later on for patches) I highly recommend creating new plugins instead of directly editing the mod(s) in question. It is also much easier to keep track of custom changes if they are in separate plugins.

- Right-click the **Unofficial Skyrim Special Edition Patch.esp** column in the right pane.
- Select **Copy as override into ...** to copy the layer into another plugin.

![Create Layer](/Pictures/skyforge/beginners-guide/sseedit-create-layer.png)

The [warning window](/Pictures/skyforge/beginners-guide/sseedit-warning-window.png) that now appears will always show up the first time you edit anything in an SSEEdit session. It can be turned off and I recommend doing that eventually.

{{< alert color="warning">}}When making changes, it is important to know that **there is no "Undo" button in SSEEdit**. If you make a mistake, you need to restore the previous state manually or close without saving your changes and start over. It is possible to save manually during a longer session.{{< /alert >}}

- Click **Yes I'm absolutely sure** to acknowledge the warning and proceed.
- A new window will pop up with various different plugins that the record can be copied into.
- Check the **\<new file>.esp** option <u>without ESM or ESL</u> and click **OK**.
- Enter **Disable USSEP Book** as the name of the new plugin and click **OK** once more.

![New Plugin](/Pictures/skyforge/beginners-guide/sseedit-new-plugin.png)

A new plugin was created and will appear at the bottom of the plugin list in the left pane.

Scroll down and expand its **Cell** records until you find the REFR record added by the USSEP. As you can see it is highlighted in green since the original record was overwritten now:

![Book ITM](/Pictures/skyforge/beginners-guide/ussep-book-itm.png)

### Identical to Master

In the new plugin, the font colour is grey instead of purple. **That means the record is an ITM, or Identical to Master.**

The master for the REFR record is **Update.esm** (because it is an injected form) and the master for the book referenced in the REFR record is the USSEP (because the book record originates in the USSEP). For that reason, both the USSEP and Update.esm are required. Skyrim.esm is also added as a master to any new plugin.

You can see the full list of masters if you click on **File Header**.

![Book ITM](/Pictures/skyforge/beginners-guide/ussep-book-masters.png)

Because nothing has (yet) been changed in the new layer, it is still *identical to all its masters* and therefore an **ITM**. ITMs are often (but not always) unnecessary and potentially disruptive (because they can override and negate other mods' changes) which is why they usually merit further investigation.

This particular record will, of course, be modified.

### Adding a record flag

In order to disable the book ingame, we can use a **Record Flag**. Scroll up to the top of the record in the right pane to find the **Record Flags** line which is currently empty.

- Right-click the empty space next to **Record Flags** and select **Edit**.

![Add Record Flag](/Pictures/skyforge/beginners-guide/sseedit-add-record-flag.png)

A new window will pop up with a list of options that you can check. Near the top of that list is a **Delete** option which is not the one you should choose. Flagging records as deleted will cause crashes if they are referenced by other records and it is considered best practice to always use the **Initially Disabled** flag instead.

{{< alert color="info">}}**Initially Disabled** means a record can potentially be re-enabled by a script later on. For example, certain coffins are flagged as initially disabled. If an NPC dies, their coffin in the Hall of the Dead of their home city will be enabled and thus become visible to the player.{{< /alert >}}

- Check the box for **Initially Disabled** and click **OK**.

![Disable Flag](/Pictures/skyforge/beginners-guide/initially-disabled-flag.png)

### Saving your changes

Saving changes made in SSEEdit is a slightly unintuitive process: You actually have to *close* the tool to be prompted to save what you changed (unless you save manually).

- Close **SSEEdit** (click the red X in the upper right corner).
- A window with all plugins edited in that session will pop up. Only the **Disable USSEP Book.esp** should be listed here.
- Make sure that the new plugin we created is checked and click **OK**.

## The Overwrite

Whenever a file is generated by a tool that is run through Mod Organizer 2, it will 'catch' these files in a folder called the ***Overwrite***. That, as it happens, is where our new plugin ended up, and it is why [a warning popped up in MO2](/Pictures/skyforge/beginners-guide/overwrite-warning.png).

The ***Overwrite*** is located at the bottom of the mod folder which means its contents will <u>always</u> overwrite the rest of the mod order (hence the name). Because it always overwrites, the ***Overwrite*** should <u>never</u> be more than a temporary location that is cleaned up as soon as possible.

{{< alert color="info">}}The actual location of the ***Overwrite*** accessible through the MO2 UI is `\Mod Organizer 2\overwrite\`.{{< /alert >}}

- Double-click the ***Overwrite*** at the bottom of your mod order to open it.

![Overwrite Contents](/Pictures/skyforge/beginners-guide/overwrite-contents.png)

### Managing Overwrite Files

Since we only have a single file in the ***Overwrite***, we can very easily convert its content into a new mod:

- Close the ***Overwrite*** window again.
- Right-click the ***Overwrite*** and select **Create Mod**.
- Name it **Disable USSEP Book** and click **OK**.
- Move your new mod directly below the **Unofficial Skyrim Special Edition Patch** and activate it.

![Overwrite Contents](/Pictures/skyforge/beginners-guide/overwrite-create-mod.png)

## Ingame Test

Now that we have created our first plugin tweak and cleaned everything up, it is time to jump in-game again to check if the plugin works as intended.

- Launch the **Skyrim Script Extender** through Mod Organizer 2.
- Select **Continue** in the main menu to load your previously created save.

And ... gone!

![Overwrite Contents](/Pictures/skyforge/beginners-guide/ussep-book-removed.jpg)

### Conclusion

You may wonder why we went through the process of digging through SSEEdit to disable a completely inconsequential feature before we even talked about load order and plugin types.

**This step was never about the book.**

With everything we learned about plugins, dependencies, and layers, **load order** should be more than a theoretical concept now. It is a tangible thing that you have seen in action. You looked at records and edits, you created your own overwriting layer to make a change, and you saw the in-game effect.

When we discuss plugin types and load order in the next step, these concepts will hopefully make more sense with the knowledge on plugin structure that we have now gained.

---

#### Please continue with [Step 4](/skyforge/beginners-guide/step4/).