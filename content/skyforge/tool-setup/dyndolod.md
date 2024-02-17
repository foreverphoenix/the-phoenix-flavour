---
title: "DynDOLOD"
weight:
type: docs
description: >
  How to set up DynDOLOD.
---

{{< alert color="info" title="Summary" >}}
> This module covers the installation of DynDOLOD.<p>
> **Prerequisite(s):** [Tools Folder](/skyforge/tool-setup/tools-folder/), [Mod Organizer 2](/skyforge/tool-setup/mo2), [Skyrim Script Extender](/skyforge/modding-resources/skyrim-script-extender){{< /alert >}}

## About DynDOLOD

DynDOLOD is a tool for regenerating [distant LODs](/skyforge/knowledge-base/distant-lods/), specifically **Object**, **Tree**, and **Grass LOD**. It can also be used to generate **Occlusion** instead of [SSELODGen](/skyforge/tool-setup/sselodgen/). It consists of multiple parts: The tool DynDOLOD (software), a collection of resources, scripts, and an SKSE plugin.

### Prerequisites

- [ Microsoft Visual C++ Redistributable packages for Visual Studio 2015, 2017, 2019 and 2022](https://learn.microsoft.com/en-US/cpp/windows/latest-supported-vc-redist?view=msvc-170)
  - *Also required for [SSELODGen](/skyforge/tool-setup/sselodgen/).*
- [.NET 6.0](https://dotnet.microsoft.com/en-us/download/dotnet/6.0)
- [SKSE & Address Library for SKSE](/skyforge/modding-resources/skyrim-script-extender/)
- [SkyUI](/skyforge/mod-recommendations/skyui/) for the MCM (optional, but highly recommended)

### DynDOLOD Versions

Though it is still officially in Alpha, **I recommend using DynDOLOD 3 for Skyrim SE.** Instructions for DynDOLOD 2.x will not be provided.

Alternatively, you may choose to use **DynDOLOD 3 NG** which is the newest version with some extra features such as workarounds for the [large reference bug](/skyforge/knowledge-base/large-reference-bug/). As a prequisite, <u>none</u> of your plugins must contain *deleted large references* which is why it is generally recommended to [clean plugins](/skyforge/modding-resources/cleaning-plugins/) before running DynDOLOD NG as this will (among other things) undelete references.

If you have never generated LODs before and would like to avoid issues as much as possible, I recommend sticking with **regular DynDOLOD 3** for now.

## Installation

We start by installing the main tool, DynDOLOD, which can be used with either 3 or 3 NG.

- Download the latest version of [DynDOLOD 3](https://www.nexusmods.com/skyrimspecialedition/mods/68518?tab=files) from the Nexus page.
- Create a folder called **DynDOLOD 3** in your **Tools** folder.
- Open the **DynDOLOD** folder inside the downloaded archive.
- Extract its contents into the new folder.

Both executables, **TexGen** and **DynDOLOD**, must be added to Mod Organizer 2.

- Go into the [executable settings](/Pictures/skyforge/mo2-executables-settings.png) in Mod Organizer 2.
- Click the small blue plus icon and select **Add from file**.
- Navigate to `\Modding Tools\DynDOLOD 3\` and double-click **TexGenx64.exe**.
- Add `-sse` under **Arguments** to ensure TexGen targets the correct game.

<u>Repeat the process for DynDOLODx64.exe.</u>

I recommend adding both executables to the Toolbar in Mod Organizer 2 for quick access.

### DynDOLOD Resources

Next, we need the **DynDOLOD Resources** which can installed as usual through Mod Organizer 2.

If one does not already exist, I recommend creating a **LOD Resources** separator and keeping it high up in the mod order.

- Download the latest version of the [DynDOLOD Resources](https://www.nexusmods.com/skyrimspecialedition/mods/52897?tab=files) from the Nexus and install it through MO2.

<mark>I recommend copying the FOMOD choices pictured below.</mark>

(The first four options are visual improvements. The Low-Res LOD Textures are *very* low res and there are better ways of increasing performance as these already take very little space. Desyncing flying birds is another neat visual feature while the "Holy Cow" is just a meme.)

![Dyn Res FOMOD](/Pictures/skyforge/tool-setup/dyndolod/dyndolod-resources-fomod.png)

### DynDOLOD Scripts & DLL

Finally, an SKSE plugin and a set of scripts is required.

- **DynDOLOD 3:** Download the scripts and the DLL from the [DynDOLOD Nexus page](https://www.nexusmods.com/skyrimspecialedition/mods/DynDOLOD-DLL-SE/57264?tab=files).
  - *You can merge them together in MO2.*
- **DynDOLOD 3 NG:** Download the scripts and the DLL from the [DynDOLOD NG Nexus page](https://www.nexusmods.com/skyrimspecialedition/mods/97720?tab=files).

## Disable Load Screens

DynDOLOD adds two load screens to the game which reference the meme of owing your firstborns to sheson for the miracle of dynamic LODs. If you would prefer not having any meme load screens, you can block them.

{{< alert color="info" >}} The new load screens will only appear after generating LODs with DynDOLOD which adds a set of plugins. However, you can disable the load screens pre-emptively.{{< /alert >}}

<mark>This requires **SSE Display Tweaks**.</mark> Installation instructions can be found [here](/skyforge/mod-recommendations/essential-mods/).

Add the following to the *SSEDisplayTweaks.ini* in **SSE Display Tweaks - Settings**:
 
```
[Miscellaneous]
LoadScreenFilter=true
LoadScreenAllow=
LoadScreenBlock=DynDOLOD.esp
```

Remember to save your changes before closing the window.