---
title: "Optimising SLE Assets"
weight:
type: docs
description: >
  How to optimise textures, meshes, and animations for Skyrim SE.
---

{{< alert color="info" title="Summary" >}}
> This module covers how to use CAO for porting textures, meshes, and animations to Skyrim SE.<p>
> **Prerequisite(s):** [Cathedral Assets Optimizer](/skyforge/tool-setup/cao/){{< /alert >}}

## Optimising with CAO

You can process textures, meshes, and animations with **Cathedral Assets Optimizer**.

I recommend creating a new profile first.

- Open **Cathedral Assets Optimizer**.
- Click the **New** button to create a new profile and name it **SSE - Optimise SLE Assets**.
- Use the default **SSE** profile as the basis.
- Configure as shown in the pictures below.

![CAO Extract BSA](/Pictures/skyforge/modding-resources/optimising-sle-assets/cao-extract-bsa.png)

![CAO Optimise Meshes](/Pictures/skyforge/modding-resources/optimising-sle-assets/cao-optimise-meshes.png)

![CAO Optimise Textures](/Pictures/skyforge/modding-resources/optimising-sle-assets/cao-optimise-textures.png)

![CAO Optimise Animations](/Pictures/skyforge/modding-resources/optimising-sle-assets/cao-optimise-animations.png)

### Usage

You can run any Skyrim LE mod containing meshes, textures, <u>or</u> animation files through CAO using this profile.

If the assets are still packed in a BSA, they will be extracted and the archive deleted as it would crash Skyrim SE otherwise. You can use the CAO [Create BSA profile](/skyforge/tool-setup/cao/#create-bsa-profile) to repack the assets after processing if you so wish.

Should a mesh still have issues after processing (causing crashes or visual bugs), try using a higher level of optimisation.

