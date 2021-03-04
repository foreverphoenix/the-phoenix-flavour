---
title: "Instructions"
weight: 1
type: docs
description: >
  General instructions for the mod installation steps.
---

After completing the Setup, you are equipped with a correctly installed and configured instance of Mod Organizer 2 that is properly set up with the Skyrim Script Extender as well as all required tools. It is now time to dive into the by far longest section in the guide - the mod installation.

The mods themselves are split up into thirty-four categories which correspond to the separators of the same names installed in MO2. Each set of mods must be installed in the order they are listed in and grouped below their respective separator.

It may be faster to download all mods of a page first, then install them, and finally go through the post-installation instructions.

**Do not attempt to launch Skyrim SE before you are instructed to**. During the installation you will have missing dependencies and unresolved conflicts fixed later by additional mods and our CRP.

**ALL MODS ARE REQUIRED AND MUST BE INSTALLED. ALL INSTRUCTIONS MUST BE FOLLOWED.**

> Keep this page open in a separate tab so you can refer back to it.

## Additional Separators

We already went over how to create separators back on the [Mod Organizer 2](/skyrim-se/initial-setup/mod-organizer-2/) page. As you can see in the sidebar on the left, there are plenty of pages in the mod installation section. Each of them will correspond to a separator in Mod Organizer 2.

- Create a new separator for every page in the Mod Installation section as you go through them.
- Enter the page's title as the name for the separator (eg **FIXES** or **INTERFACE**).
- The first one, **ESSENTIAL MODS**, is already present of course.

In case you're not sure how to create a new separator anymore:

![MO2 Create Separator](/Pictures/skyrim-se/initial-setup/mo2-create-separator.png)

## Installation Instructions

Each mod has its own section with the following instructions:

- **Download Instructions:** Lists files to download and the Nexus link which will directly bring you to the Files section.
- **Porting Instructions:** Brief instructions if necessary for proper porting of a LE mod to SSE with the Creation Kit or CAO.
- **Additional Instructions:** May contain INI edits, file deletions or edits, rarely SSEEdit tweaks.

Not all mods strictly follow this template. Some have sections unique to them with extra explanations or instructions. Just follow those instructions one by one and to the letter. Sometimes they are optional (which is then clearly stated) and you can skip them.

### Download Instructions

* Almost all mods are hosted on the Nexus.
* The link to the mod's file section is in the **Download Instructions** header (CTRL+Click to open in new tab.)
* The files listed under **Download Instructions** are marked with the respective section you can find them in on the Nexus:
  * Main Files
  * Update Files
  * Optional Files
  * Miscellaneous Files
  * Old Files
* Download the file(s) by clicking **Mod Manager Download**. It will automatically be downloaded through Mod Organizer 2. If a mod has special requirements, they are listed in a pop-up window where you will have to click the **Download** button again. Don’t worry about these requirements, they are included in the guide or otherwise taken care of.

### Mod Installation

* After downloading a mod, switch to the **Downloads** tab in the right pane of Mod Organizer 2 and double-click the file(s) to install.
* This may open a FOMOD installer if the mod includes one. **FOMOD Instructions** are provided in the guide.

After installing a mod you can rename it to reflect the version you downloaded or options you selected in the FOMOD.

- For retextures, it is useful to add the texture resolution: `Embers HD 2K`.
- If there are different versions, note down which one you downloaded: `Less Ugly Tundragrass - Redder Variant`.

Occasionally you will be instructed to download multiple files from the same page (usually the main mod with updates or patches). When installing them, always install the main file first. The second file will by default have the same name and MO2 will ask how you want to proceed:

* Unless otherwise specified in the guide's instructions, always select **Rename** and give the file a unique name so that it doesn't overwrite the main file. For instance, if the main file was `Simple Children` and you install the patch pack from the same mod page, click **Rename** and enter `Simple Children - Patches`.
* Rarely, you will be told to "merge with the main file" in which case you select the **Merge** option. This will move all installed files into the mod folder of the main file, overwriting existing files.
* Only when updating mods to a new version should you select **Replace** which, of course, replaces all original files.

### Basic Instructions

Certain procedures - such as resaving a plugin or running a mod through the Cathedral Assets Optimizer - are repeated many times throughout the guide. After going through them for a few times, you will know them by heart but until then, please refer to the [Basic Instructions](/skyrim-se/guide-resources/basic-instructions/) page (keep it open in a separate tab).

The linked page includes detailed explanations for the following instructions:

- "Resave Example.esp in the Creation Kit."
- "Clean Example.esp with SSEEdit."
- "Unpack Example.bsa through Mod Organizer 2."
- "Run the mod through Cathedral Assets Optimizer."
- "Run the mod through SSE NIF Optimizer."
- "Downsize the textures with Cathedral Assets Optimizer."

You will also be instructed to delete, rename, or move files through the MO2 interface frequently. This is very simple:

- Double-click the mod in your mod order (left pane of Mod Organizer 2).
- Switch to the **Filetree** tab and find the files you need to delete/rename/move.
- Right-click to remove/rename or move them per drag-and-drop.