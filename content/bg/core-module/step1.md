---
title: "Step 1"
weight: 1
type: docs
description: >
  Skyrim SE and MO2 setup for modding.
---

{{< alert color="info" title="Summary" >}}
> This step covers all aspects of preparing the vanilla game, including creations, for modding with Mod Organizer 2.{{< /alert >}}

## Requirements

The Core Module requires the **Steam** version of **Skyrim Special Edition**. Whether you own the **Anniversary Edition DLC** is irrelevant.

You should have a file archiver like [7ZIP](https://www.7-zip.org/) installed and I also recommend using [Notepad++](https://notepad-plus-plus.org/downloads/) for modifying config files.

### File Name Extensions

Make sure that **file name extensions** are set to visible in Windows Explorer. This will enable you to tell apart files by their extensions which is fairly important.

- To see file name extensions, go into **Windows Explorer**.
- In the **View** tab/ribbon, make sure the **File name extensions** box is ticked.

![File Name Extensions](/Pictures/bg/core-module/file-name-extensions.png)

## Clean Install

Please start by performing a [Clean Install](/bg/additional-modules/clean-install/).

## Nexus Mods

The vast majority of mods and tools (including Mod Organizer 2) are hosted on [Nexus Mods](https://www.nexusmods.com/). The Nexus supports hundreds of games though it should come as no surprise that the six games with the most downloads in total (by a wide margin) are the most recent Bethesda games.

You will download many files from various Nexus pages throughout this guide and we will also talk about the site in general. In order to download mods, you must have an account.

**If you do not have a [Nexus Mods](https://www.nexusmods.com/) account yet, go ahead and create one now.**

{{< alert color="info" >}} Read more about [Nexus Premium](/bg/knowledge-base/nexus-premium/). {{< /alert >}}

## Mod Manager Choice

Learning how to mod Skyrim SE is largely about learning how to use the various tools to your advantage. Now that we have returned Skyrim to a pristine vanilla state, we can move on to installing the most important tool in our tool box.

**Mod Organizer 2 (MO2)** is a mod manager. Like its predecessor, [Mod Organizer](https://www.nexusmods.com/skyrim/mods/1334), it is community-made and open-source, with a wide range of features catering specifically to advanced modders. If you are serious about building an extensive setup of mods, Mod Organizer 2 is going to be your best friend.

**Using Mod Organizer 2 is <u>mandatory</u> for this guide.**

{{< alert color="info" >}}You can check the [Mod Managers](/bg/knowledge-base/mod-managers/) article for more information about available mod managers and why I chose MO2. {{< /alert >}}

Rather than list all the features of MO2 right now, I will slowly introduce them to you as we go. Many of its unique advantages would make very little sense to you before we have established some basic knowledge about modding in general. I will also gradually explain various elements of the UI as we go, so do not feel discouraged or overwhelmed when you first open the tool.

### Mod Organizer 2

Please follow all steps of the [MO2 Setup](/bg/tool-setup/mo2/).

### UI Overview

Now you can get your first look at MO2. **If the interface seems daunting, do not feel discouraged!** You will get used to it faster than you may think. Much of the UI simply makes a great deal of sense which is why it will quickly become easy to navigate.

At this point, we are not going to discuss the purpose of the various parts of MO2's interface: Without context, the details would be difficult to memorise. For now, please have a look at the five primary components of the UI which I will refer to from now on by the names defined below.  

- **(1) The toolbar** allows you quick access to a number of sub menus.
- **(2) The profile drop-down** allows quick switching between MO2 profiles.
- **(3) The executables drop-down** is where you select and run executables like the game or a tool.
- **(4) The left pane** is the mod order. This is where all your mods will appear once installed.
- **(5) The right pane** contains various tabs like the Plugins tab for managing the load order.

{{< alert color="warning" >}}You will also see all Creation Club files that you own in MO2. They will be dealt with in the next step.{{< /alert >}}

![MO2 UI Overview](/Pictures/bg/core-module/mo2-ui-overview.png)

## Creation Club

{{< alert color="info" >}}Read the [Creation Club](/bg/knowledge-base/creation-club/) article for more information.{{< /alert >}}

Since the release of **Skyrim Anniversary Edition**, everyone owns at least the following free creations:

- **ccbgssse001-fish** (Fishing)
- **ccbgssse025-advdsgs** (Saints & Seducers)
- **ccbgssse037-curios** (Rare Curios)
- **ccqdrsse001-survivalmode** (Survival Mode)

<u>These will always be installed alongside the game.</u>

If you bought additional Creations, downloaded them when they were free, or bought the **Anniversary Edition DLC**, they should have been downloaded upon launching the game.

{{< alert color="warning" >}}**Creations are official mods.** We are going to organise them the same way we organise other mods, and for the same reasons.{{< /alert >}}

Right now, the Creations are managed by Mod Organizer 2 just like the official DLC: They are always active and cannot be selectively disabled. Also, the names are verbose. We do not like this.

### Managing Creations

Please follow all steps in the [Managing Creations](/bg/additional-modules/managing-creations/) module.

### Free Creations

Enable the four free creations by checking the boxes in MO2: 

- Creation Club - Survival Mode
- Creation Club - Fishing
- Creation Club - Saints & Seducers
- Creation Club - Rare Curios

{{< alert color="warning" >}}If you own more creations, leave them disabled until after you have completed the Core Module.{{< /alert >}}

## MO2 Separators

Among the most useful features in MO2 for organising your mod order are **separators**. They were highly requested by the community and eventually implemented by the MO2 team. Each separator can be placed anywhere in the mod order, its name and colour can be customised, mods can be grouped below it, and they can be collapsed or expanded at will.

Below, you can see a picture of my visuals-only setup's mod order to get an idea of how separators can help with organising several hundreds of mods:

![Aurora mod order](/Pictures/bg/core-module/aurora-mod-order.png)

### Creating Separators

At the top of our current mod order (left pane), you can see the three DLCs. We can group them under a separator of their own.

- Click the tools icon above the mod order and select **Create separator**.

![Create Separator](/Pictures/bg/mo2-create-separator.png)

- Enter **Official Master Files** as the name and click **OK**.

Your new separator will show up at the bottom of your mod order.

- Drag it up above the three DLC in the right pane.

We can also add a separator for the creations.

- Click the tools icon above the mod order and select **Create separator**.
- Enter **Creation Club** as the name and click **OK**.
- Drag it up below the three DLC and above the creations in the right pane.

### Separator Colours

If you like you can also change the separator's colour. You can do so by right-clicking it and clicking **Select Color**. You can set the separator to any colour you like, it can be changed anytime, and every separator can have a different colour.

Your colour choices should roughly match your MO2 theme for optimal readability: For instance, my colour scheme would be far too bright for anyone using dark mode.

{{< alert color="info" >}} If you are also using the default MO2 theme, I can recommend this nice blue **#A9D5FF** which I am using for my separators here.{{< /alert >}}

### Collapsing Separators

Separators can be collapsed, hiding all the mods that were sorted underneath it. This is incredibly useful for large setups. **Double-click the Creation Club separator to collapse it** - much better, right?

![MO2 Separators](/Pictures/bg/core-module/mo2-separators.png)

---

#### Please continue with [Step 2](/bg/core-module/step2/).