---
title: "LOOT"
weight:
type: docs
description: >
  How to set up the Load Order Optimisation Tool (LOOT).
---

{{< alert color="info" title="Summary" >}}
> This module covers the installation of the Load Order Optimisation Tool (LOOT).<p>
> **Prerequisite(s):** [Tools Folder](/bg/tool-setup/tools-folder/), [Mod Organizer 2](/bg/tool-setup/mo2){{< /alert >}}

## About LOOT

**LOOT** is a tool for automatically sorting plugins in the load order. Drawing on a masterlist maintained by the community, LOOT attempts to place plugins in a way that minimises unintentional conflicts.

<u>LOOT cannot determine the ideal load order by itself.</u> You **must** use SSEEdit and manually adjust.

{{< alert color="info" >}}Personally, I use LOOT only to quickly find plugins that need "[cleaning](/bg/additional-modules/cleaning-plugins)" as a prerequisite for [generating LODs](/bg/additional-modules/generating-lods/). I summarised my opinion on the tool [here](/bg/knowledge-base/phoenix-on-loot/).{{< /alert >}}

### LOOT & Wabbajack

If you are building a Wabbajack list and you wish to add optional mods that also have plugins, you may want to use Parapets' [LOOT Config Loader](https://www.nexusmods.com/skyrimspecialedition/mods/60864) plugin ([readme](https://github.com/Exit-9B/LOOTConfigLoader/blob/main/README.md)). It allows you to create a custom masterlist for a portable instance of Mod Organizer 2 so that your users only have to click **Sort** to update the load order.

Note that the LOOT Config Loader tool uses the version of LOOT integrated in Mod Organizer 2 which is quite outdated. To use Parapets' plugin with the full version of LOOT, you need to grab [version 0.17.0](https://github.com/loot/loot/releases/tag/0.17.0).

## Installation

LOOT is available on the Nexus.

- Download the installer from the [Nexus page](https://www.nexusmods.com/site/mods/439?tab=files) and run it.
- As the installation location, you can pick your Tools folder if you care about keeping all tools in one place.
- Keep **Download and install the latest masterlists** checked.
- Uncheck **Launch LOOT** before clicking **Finish**.

### MO2 Integration

LOOT requires access to the data folder and must therefore be launched through Mod Organizer 2.

- Open the [executable settings](/Pictures/bg/mo2-executables-settings.png) in Mod Organizer 2.
- Click the small blue plus icon and select **Add from file**.
- Navigate to your **LOOT** folder and double-click **LOOT.exe**.
- Click **OK** to add the executable to Mod Organizer 2.

For improved integration into Mod Organizer 2, I recommend installing the [LOOT Warning Checker](/bg/tool-setup/loot-warning-checker/) plugin.

## MO2 Sort Button

As mentioned in the "LOOT & Wabbajack" section, Mod Organizer 2 has its own, stripped-down version of LOOT integrated which can be run by clicking the [Sort](/Pictures/bg/tool-setup/loot/loot-sort-button.png) button above the load order in the right pane.

**Do not use this button to sort your load order** unless you have a (Wabbajack) setup with the above-mentioned LOOT Config Loader plugin and a *custom* masterlist.

The integrated version of LOOT is <u>outdated</u> and you should use the latest version installed during the previous step if you are planning to use the tool for plugin sorting. 

### Remove Sort Button

If the Sort button annoys you and/or you want to sure you never accidentally press it, you can remove it from the interface with a small CSS snippet.

Users of the default theme can do this by adding a new stylesheet:

- Navigate to `\Mod Organizer 2\stylesheets\`.
- Right-click anywhere and select **New** >> **Text Document**.
- Rename the file to **No Sort Button.qss**.
  - *Remember to change the file extension.*
- Open the new file in a text editor such as Notepad++.
- Paste the following:

```
/* Sort button */
#sortButton {
    qproperty-iconSize:0px;
    min-width:0px;
    width:0px;
    padding: 0 0 0 -30;
}
```

- Save your change and close the file.

Afterwards, you need to [select the new stylesheet](/Pictures/bg/tool-setup/loot/remove-sort-button.png) in the **Themes** tab in the Mod Organizer 2 settings.

If you are using a different theme, you can modify its stylesheet file (.QSS). Open it in a text editor and use CTRL+F to see if it modifies anything about the `#bossButton` component. Add the snippet from above, replacing any other code for the button.
