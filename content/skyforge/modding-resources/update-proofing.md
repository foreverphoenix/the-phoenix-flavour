---
title: "Update Proofing"
weight:
type: docs
description: >
  How to update-proof Skyrim.
---

{{< alert color="info" title="Summary" >}}
> This module covers how to prevent Skyrim from automatically updating.<p>
> **Prerequisite(s):** [Clean Install](/skyforge/modding-resources/clean-install){{< /alert >}}

The version-specific nature of SKSE and related mods makes forced updates of the base game quite disruptive. They can completely break a modded setup, potentially rendering you unable to play until the modding scene has caught up.

Fortunately, update-proofing Skyrim is simple:

- In your games library in Steam, right-click **The Elder Scrolls V: Skyrim Special Edition**.
- Select **Properties** and switch to the **Updates** tab.
- Make sure **Automatic updates** are set to **Only update this game when I launch it**.

![update proofing](/Pictures/skyforge/modding-resources/update-proofing.png)

{{< alert color="warning" >}}Of course, this would still force you to update whenever you attempt to launch the game through its default executables. However, SKSE comes with its own launcher which you must always use to launch the game for it to work properly. Launching the game through SKSE will <u>not</u> prompt Steam to update, meaning you can stay on an older version of the game for as long as you desire.{{< /alert >}}