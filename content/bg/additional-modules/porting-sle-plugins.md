---
title: "Porting SLE Plugins"
weight:
type: docs
description: >
  How to port Skyrim LE plugins to Skyrim SE.
---

{{< alert color="info" title="Summary" >}}
> This module covers how to use the Creation Kit and SSEEdit for porting plugins.<p>
> **Prerequisite(s):** [Creation Kit](/bg/tool-setup/creation-kit/), [SSEEdit](/bg/tool-setup/sseedit/){{< /alert >}}

## Form Version

All plugins that were created for Skyrim LE should at least be resaved in the Skyrim SE Creation Kit.

In Skyrim SE, some records in the vanilla game files have the new **form version 44** as opposed to the previous **form version 43** and it has been discovered that the form version of user-made SLE plugins changes from 43 to 44 when resaving them in the Creation Kit. If this is not done, the plugin <u>may</u> cause issues when loaded in Skyrim SE (including save game corruption and apparently crashes).

{{< alert color="info" >}}Form version 43 in SSE plugins are not always problematic. Refer to this [excellent article](https://davidjcobb.github.io/skyrim-writings/articles/form-versions-43-and-44.html) by DavidJCobb if you are interested in learning about the difference between form versions and when it matters.{{< /alert >}}

### MO2 Warning

Mod Organizer 2 will detect plugins with Form Version 43 when they are present in the load order. Again, this does not necessarily mean that the plugin contains corrupted data, but it should be resaved to be safe.

Using xEdit scripts to check for wrong form versions in your load order is unnecessary given the MO2 warning.

![MO2 Warning](/Pictures/bg/additional-modules/porting-sle-plugins/mo2-form-43-warning.png)

### SSEEdit Plugin Header

You can see a plugin's form version in the **Plugin Header** in SSEEdit:

![Wrong Form Version](/Pictures/bg/additional-modules/porting-sle-plugins/form-version-43.png)

### Resaving Plugins

Converting a plugin is as easy as opening and saving it in the SSE Creation Kit. This should be done with [SSE Creation Kit Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/20061) installed as the CK still misses some forms that require conversion. 

- Run the **Creation Kit** through Mod Organizer 2.
- Click the little folder icon in the toolbar to open a plugin.

![CK Open Plugin](/Pictures/bg/additional-modules/porting-sle-plugins/ck-open-plugin.png)

You can only ever load one active plugin in the Creation Kit. If you have multiple SLE plugins, resave them one at a time.

- Select the plugin you wish to resave and click **Set as Active File**.
- Click **OK** to load the plugin.

This will load the plugin and its masters. Wait until the CK says "done".

![CK Done](/Pictures/bg/additional-modules/porting-sle-plugins/ck-done-loading.png)

- Click the [Save icon](/Pictures/bg/additional-modules/porting-sle-plugins/ck-save-plugin.png) in the toolbar.
- Close the Creation Kit.

{{< alert color="success" >}} And that's it! The plugin has been resaved successfully.{{< /alert >}}

![Correct Form Version](/Pictures/bg/additional-modules/porting-sle-plugins/form-version-44.png)

## Water Flow

## Landscape