---
title: "Step 7: SSEEdit & Form IDs"
weight: 7
type: docs
description: >
  SSEEdit setup and discussing base/ref IDs.
---

## Load Order

Several mod installations later, we have the beginning of a mod order in the left pane. If you switch to the **Plugins** tab in the right pane of Mod Organizer 2, the **load order**, you will also see four new plugins, sorted in the order they were installed in:

![MO2 Load Order](/Pictures/embers/module-1/mo2-load-order.png)

Some of our currently installed plugins are displayed in **bold**, *italics*, or both, which is how Mod Organizer 2 visualises different plugin types in the load order. For the time being, you can simply consider all of them plugins. We will talk about the differences between these plugin types in the next step.

## SSEEdit

While plugins can also be created and edited in Bethesda's official modding tool, the **Creation Kit**, the community-made **SSEEdit** is much better suited for beginners to get an idea of how plugins are structured and how load order works.

However, neither of the two replaces the other, and the tool to use always depends on the type of plugin you are working on. For the vast majority of tweaks, edits, and especially patches, SSEEdit is the way to go because it is very good at visualising conflicts and interactions.

**SSEEdit** is also commonly referred to as **xEdit**. It exists for most Bethesda games, not only Skyrim SE, and its name changes depending on the game: For example, xEdit for Skyrim LE was called TES5Edit. Once you have downloaded the program, you can use it for any game that is supported by either changing the name of the executable or starting it with a specific argument such as `-sse` for Skyrim SE. You will see the tool referred to as **SSEEdit** or **xEdit** interchangeably, it means the same thing.

### Installation

Let's grab SSEEdit from the Nexus:

- Download the latest version of [SSEEdit](https://www.nexusmods.com/skyrimspecialedition/mods/164).

Now we need a new directory for storing SSEEdit (and other modding tools later on). This will be located within the MO2 installation. It is occasionally recommended not to install any tools inside the MO2 folder though plenty of Wabbajack list authors (myself included) have done this for years without any issues that I am aware of.

- Navigate to `\Mod Organizer 2\` and create a new folder called **Tools** inside.
- Inside `\Mod Organizer 2\Tools\` create a new folder called **SSEEdit**.
- Open the downloaded archive and extract everything into the new folder.

### MO2 Integration

Like almost every other tool, **SSEEdit** can only function if it is run through Mod Organizer 2. Otherwise, it would be unable to access the virtual data folder and simply load the official master files and whichever Creations are actually located inside the "real" data folder.

- In Mod Organizer 2, click the gears icon in the Toolbar to open the **Executables** settings.

![MO2 Executables Settings](/Pictures/embers/module-1/mo2-executables-settings.png)

- Click the small blue plus icon and select **Add from file**.
- Navigate to `\Mod Organizer 2\Tools\SSEEdit\` and double-click **SSEEdit.exe**.
- Click **Apply** to add the executable to Mod Organizer 2.

![SSEEdit In MO2](/Pictures/embers/module-1/sseedit-in-mo2.png)

Before SSEEdit works properly with our custom Game Root, we do need to manually set the data folder patch via an argument.

Add the following in the **Arguments** line and make sure to replace `<YourFilePath>` with the correct filepath for your machine:

```
-D:"C:\<YourFilePath>\Game Root\Data"
```

Click **OK** to save your changes and close the Executable settings.

![SSEEdit Data Argument](/Pictures/embers/module-1/sseedit-data-argument.png)

### Tool Bar

SSEEdit should be automatically selected in the executables drop-down. For maximum convenience, I recommend click the **Shortcut** drop-down below the **Run** button and selecting **Toolbar and Menu**.

The SSEEdit icon will now be show up above and clicking it there will be the same as selecting it from the executables drop-down and clicking run. After installing half a dozen tools, it is rather useful to be able to launch everything through that tool bar without having to select it from the drop-down first.

Now that SSEEdit is installed, we need to find ourselves a proper example edit to try out.

![SSEEdit To Toolbar](/Pictures/embers/module-1/sseedit-to-toolbar.png)

## The Unwanted Effects Book

Among vanilla Skyrim's many bugs are certain active effects, applied by spells for instance, that may get "stuck" on the player after they are supposed to expire. The USSEP fixes these effects, but it also adds an option for the player to rid themselves of any leftovers. Initially, this could be accessed through a second shrine in the Temple of Kynareth in Whiterun, but was later moved to a book added to the player's inventory upon loading the game. Following complaints about a lack of immersion, a compromise was finally reached by placing the book in the Temple of Kynareth.

Using books or powers in order to access or customise a mod's functionality was rather common before the Script Extender and SkyUI came along, although nowadays such options have largely been moved to dedicated mod configuration menus. With the release of Skyrim SE and the introduction of mods on consoles, many mod authors had to revert to these old workarounds as it is impossible to install files outside the data folder on consoles, and thus impossible to install the Skyrim Script Extender. The USSEP team does not want to move the option to an MCM or make it available only through the (ingame) console as that would not work for the XBOX and Playstation ports of the mod.

However, for us PC players, the book is entirely redundant. If you ever find yourself stuck with an active effect, you can get the book through the console very easily, so there is no need to have it lying around in the game world or lugging it around with you. Does it really break immersion? Some players are vehemently opposed to having any sort mod config items in the world. Others probably never noticed the book in the first place.

Whatever the case, disabling that book makes for a nice example edit, our first foray into the world of plugins.

### Finding the Book

Let's go and have a look at that book, shall we?

- Select **SKSE** from the MO2 executables drop-down and click **Run**.
- In the main menu, open the **console** (press the *tilde* key above TAB on your keyboard).
- Type `coc WhiterunTempleofKynareth` and press **Enter**.

> Unfortunately, you cannot copy and paste in the console (without additional mods).

The **coc** (**c**enter **o**n **c**ell) command is insanely useful for testing. When used from the main menu, it will create a test character in your chosen cell with some basic equipment (check your inventory if you like). Do note that **coc** is for testing *only*, you will run into all kinds of issues if you try to use it for an actual playthrough as skipping the intro will cause many of the game's scripts to never be properly initialised.

To find the book, go from where you spawned by the entrance to the temple into the sleeping area on the right. There is a bookcase just in front of you with the **USSEP Unwanted Effects Remover** on the floor leaning against its side.

![USSEP Book 1](/Pictures/embers/module-1/ussep-book-1.jpg)

![USSEP Book 2](/Pictures/embers/module-1/ussep-book-2.jpg)

Now we know where the book is. How does that help us?

The USSEP plugin is big. It has hundreds upon hundreds of records, and finding a single book among them sounds rather inconvenient. What you *really* need to know is the book's **Form ID**, its unique identification number. To figure out that Form ID, we installed **More Informative Console**.

- Open the console once again and click on the book.
- Here is what you should see:

![USSEP Book 3](/Pictures/embers/module-1/ussep-book-3.jpg)

Everything we could possibly need to know we can see at a glance thanks to the mod. Either take a screenshot or simply refer to mine, then **save** and **close** the game. It is time to talk about Form IDs.

## Form IDs

Every object, NPC, magic effect, music track, etc, in the game is defined in a unique *record* which is contained in a *plugin*. For vanilla Skyrim, that is what the official master files do: Each of the five plugins contains thousands of **records**, one for every *thing* in the game: For NPCs, magic effects, music tracks, and so forth. Every record has a unique **Form ID** to be identified by. No two Form IDs can ever be identical.

Form IDs consist of 8 [hexadecimal](https://en.wikipedia.org/wiki/Hexadecimal) numbers (1-9 and A-F), for example `050B1985`. The first two denote the **Index** which refers to the load order position of the plugin that the record was initially defined in. They change depending on your load order. The remaining six numbers will always stay the same. This way, there can never be two plugins with duplicate Form IDs: No two plugins can be loaded in the same spot in the load order so they will always have a different index.

### Base and Ref Form ID

However, if we check the info we grabbed through More Informative Console, we will notice that the book has not one but *two* Form IDs:

![USSEP Book FormID](/Pictures/embers/module-1/ussep-book-formid.jpg)

The **Base Form ID** is `050B1985` and describes the book itself: It defines which model it uses, what its contents are, and, in this case, what script is attached to it. From the first two digits of the Form ID, you can tell that it is defined in the **Unofficial Skyrim Special Edition Patch.esp** plugin. If you check the load order in Mod Organizer 2, the mod index of the USSEP plugin is **05** which is identical to the index of the book's Base Form ID.

The **Ref Form ID** is `0190001B` and describes the book's placement: That it is located in the `WhiterunTempleofKynareth` cell, that it is enabled, how it is placed, and so on. The reason a second Form ID is needed is because you may have various copies of the same object distributed throughout the game. While the book is unique right now, a Steel Sword would not be. There are dozens of hand-placed Steel Swords in Skyrim. Each of them has a unique REFR (reference) record with its unique Ref Form ID: They *refer* to the original item defined in the record with the Base Form ID.

**In summary:** `050B1985` is the USSEP Unwanted Effects Remover book and `0190001B` is the copy of it placed in the Temple of Kynareth.

### Injected Forms

As you may have noticed, the index for the book's Ref Form ID `01` actually corresponds to **Update.esm** instead of the USSEP plugin: It is an **injected record**, meaning that while it is not *defined* in Update.esm, another plugin referring to it would not have a missing master if the USSEP were not present as long as Update.esm is there. This is helpful for patchless compatibility.

For example, a mod might change the interior of the Temple of Kynareth in such a way that the USSEP book is suddenly stuck in furniture, or otherwise inaccessible or in the way. The mod author could add the USSEP as a master to their plugin and move the book out of the way, but now their Temple of Kynareth mod would always require the USSEP.

But because the book's REFR record is an injected form, adding the USSEP as a master would not be required in the first place - only Update.esm would have to be added (and everyone has Update.esm). That means the book would be moved if the USSEP was installed, but there would not be a missing master error if it was not.

Armed with all this theoretical knowledge on forms and records, we should fire up SSEEdit.