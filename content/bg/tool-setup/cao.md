---
title: "Cathedral Assets Optimizer"
weight:
type: docs
description: >
  How to set up Cathedral Assets Optimizer.
---

{{< alert color="info" title="Summary" >}}
> This module covers the installation of Cathedral Assets Optimizer and setting up a profile to create BSAs.<p>
> **Prerequisite(s):** None{{< /alert >}}

## About Cathedral Assets Optimizer

**Cathedral Assets Optimizer (CAO)** is an all-in-one asset processing tool for Skyrim (SE/LE) and Fallout (NV/3/4). Among other things, it can create and unpack archives, optimise meshes, and perform some basic texture modifications like changing the resolution, creating mipmaps, or compressing.

## Installation

While CAO is meant to modify mods, it should target separate modding folders as opposed to being run on an entire setup. Do not try to launch it through Mod Organizer 2.

- Download the latest stable version from the [Nexus page](https://www.nexusmods.com/skyrimspecialedition/mods/23316?tab=files).
- Create a folder called **Cathedral Assets Optimizer** in your **Modding Tools** directory.
- Extract the downloaded archive into the new folder.

For quick access, I recommend **pinning** the executable to your taskbar.

### Antivirus Exclusions

The author of CAO recommends creating an exclusion in [Windows Defender](https://support.microsoft.com/en-us/windows/add-an-exclusion-to-windows-security-811816c0-4dfd-af4a-47e4-c301afe13b26) to prevent slowdowns (follow link for instructions).

Third-party antivirus software, if you have any installed, may also cause CAO to not work properly (or at all) and you may need to create an exclusion for them as well. You should be able to find instructions by googling for the name of the antivirus and "exclusion".

## Create BSA Profile

{{< alert color="info" >}}This step is optional.{{< /alert >}}

As CAO has many different use cases for various games, it helps to create custom profiles for them.

Currently, I use the tool largely for creating BSAs while resorting to Octagon and SSE NIF Optimizer for texture and mesh processing, respectively. In the following, I will show you how to set up a profile for creating BSAs.

### Create new profile

- Open **Cathedral Assets Optimizer** and make sure the **SSE** profile is selected at the top.
- Check the option to **Show advanced settings**.

![CAO SSE Profile](/Pictures/bg/tool-setup/cao/cao-sse-profile.png)

- Click the **New** button to create a new profile and click **OK** to the infobox.
- Enter **SSE - Create BSA** as the name.
- Confirm to use the **SSE** profile as the basis.

(When creating a new profile, I recommend using the premade profile for the same game as the base.)

### BSA Tab

In the **BSA** tab, you will want to configure the options as follows:

![BSA Tab BSA](/Pictures/bg/tool-setup/cao/bsa-profile-bsa.png)

**Delete source files** is an option I tend to keep disabled just in case I messed something up. If I did, it is easier to delete the BSA and run CAO again than having to first unpack the created archive(s). Of course, this means you will always have to manually delete the source files after BSA creation. Decide for yourself whether or not to disable this option.

**Maximum Size:** <u>I recommend not changing this option.</u> BSA maximum sizes differ by game (see below) so if you use CAO for different games (i.e., Skyrim SE and Fallout 4), make sure to use separate Create BSA profiles for them.

{{< alert color="info" >}}If memory serves, Skyrim LE BSAs were limited to 2GB while Fallout 4 BSAs can be up to 4GB in size. I am not sure about Skyrim SE BSAs but keeping them below 2GB in size seems like the safest option. None of the vanilla BSAs exceed 2GB.{{< /alert >}}

### Other Tabs

I recommend leaving everything <u>disabled</u> in the other three tabs.

This is because I find it to be generally easier to do one *thing* at a time. Check through one mod at a time, run it through Octagon if you find that its textures are missing mipmaps, then run it through CAO to pack it into a BSA if necessary. Being very deliberate about how you modify files and going step-by-step can help avoid seemingly inexplicable issues down the line.