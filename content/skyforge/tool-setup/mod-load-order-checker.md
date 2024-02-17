---
title: "Mod Load Order Checker"
weight:
type: docs
description: >
  How to set up Mod Load Order Checker.
---

{{< alert color="info" title="Summary" >}}
> This module covers the installation of the Mod Load Order Checker plugin for Mod Organizer 2.<p>
> **Prerequisite(s):** [Mod Organizer 2](/skyforge/tool-setup/mo2/){{< /alert >}}

## About Mod Load Order Checker

**Mod Load Order Checker** is a plugin for Mod Organizer 2 which warnings when *plugins* are being loaded out of order, i.e., a patch is placed before its master. Out-of-order plugins can be difficult to track, especially in a large load order, but they create broken dependencies which can prevent the game from launching properly and cause other issues.

### Installation

Mod Load Order Checker is available on the Nexus.

- Download the latest version of [Mod Load Order Checker](https://www.nexusmods.com/site/mods/608?tab=files).
- Use the [shortcut](/Pictures/skyforge/mo2-plugins-folder-shortcut.png) to open the MO2 Plugins folder.
- **Close Mod Organizer 2.**
- Extract the downloaded archive into the **plugins** folder.
- Re-open Mod Organizer 2.

### Example

Without the plugin, there will be no visible error anywhere in Mod Organizer 2 when a plugin is loaded before its master. In SSEEdit, the load order will be fixed automatically, so you will see no errors, but the same does not happen ingame where you *will* have issues.

With the plugin, a warning will show up:

![Out-of-order](/Pictures/skyforge/tool-setup/mod-load-order-checker/out-of-order.png)

![Warning](/Pictures/skyforge/tool-setup/mod-load-order-checker/mo2-warning.png)