---
title: "SSELODGen"
weight:
type: docs
description: >
  How to set up SSELODGen.
---

{{< alert color="info" title="Summary" >}}
> This module covers the installation of SSELODGen.<p>
> **Prerequisite(s):** [Tools Folder](/bg/tool-setup/tools-folder/), [Mod Organizer 2](/bg/tool-setup/mo2){{< /alert >}}

## About SSELODGen

SSELODGen is a tool for regenerating [Terrain LOD](/bg/knowledge-base/distant-lods/) and **Occlusion**. Because it is based on [SSEEdit](/bg/tool-setup/sseedit/), the tool is typically abbreviated to **xLODGen** as it can be used with a variety of Creation Engine games, not just Skyrim.

### Prerequisites

- [ Microsoft Visual C++ Redistributable packages for Visual Studio 2015, 2017, 2019 and 2022](https://learn.microsoft.com/en-US/cpp/windows/latest-supported-vc-redist?view=msvc-170)
  - *Also required for [DynDOLOD](/bg/tool-setup/dyndolod/).*

## Installation

SSELODGen can be downloaded from MEGA. A link is provided on the STEP Forum.

- Open the [xLODGen](https://stepmodifications.org/forum/topic/13451-xlodgen-terrain-lod-beta-98-for-fnv-fo3-fo4-fo4vr-tes5-sse-tes5vr-enderal-enderalse/) post on the STEP Forums.
- Locate the download link for the latest version and download it from MEGA.

![Download SSELODGen](/Pictures/bg/tool-setup/sselodgen/download-sselodgen.png)

- Create a folder called **SSELODGen** in your **Tools** folder.
- Open the  folder inside the downloaded archive.
- Extract its contents into the new folder.

### MO2 Integration

The executable must be added to Mod Organizer 2.

- Go into the [executable settings](/Pictures/bg/mo2-executables-settings.png) in Mod Organizer 2.
- Click the small blue plus icon and select **Add from file**.
- Navigate to `\Modding Tools\SSELODGen\` and double-click **xLODGenx64.exe**.

### Arguments

You need to set additional Arguments in the executable settings to define the target game and the output directory.

**The output directory <u>must</u> be outside your MO2 folder.** I recommend using a top-level folder. After generation of LOD has been completed, you will move the output folder back into Mod Organizer 2.

```
-sse -o:"Drive:\Path\To\Output\"
```

![SSELODGen Arguments](/Pictures/bg/tool-setup/sselodgen/sselodgen-arguments.png)

## SSE-Terrain-Tamriel ESM

To allow SSELODGen to generate Terrain LOD for the unreachable edges of the world (which are still visible from a distance), you should enable the **SSE-Terrain-Tamriel.esm** before LOD generation.

- Download the **SSE Terrain Tamriel Extend** main file from the [Nexus page](https://www.nexusmods.com/skyrimspecialedition/mods/54680?tab=files).
- Install it as usual in Mod Organizer 2.
  - *I recommend placing it under the **LOD Resources** separator.*

The ESM should only be active when generating Terrain LOD.