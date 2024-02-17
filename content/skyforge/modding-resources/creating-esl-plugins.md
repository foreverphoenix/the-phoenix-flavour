---
title: "Creating ESL Plugins"
weight:
type: docs
description: >
  How to create ESL plugins with SSEEdit.
---

{{< alert color="info" title="Summary" >}}
> This module covers how to flag plugins as ESL and compact Form IDs if necessary.<p>
> **Prerequisite(s):** [SSEEdit](/skyforge/tool-setup/sseedit/){{< /alert >}}

## About ESL Plugins

Before starting to ESL-ify plugins in your load order, I strongly suggest familiarising yourself with the format and when/how it should be used. Refer to the [Plugin Basics](/skyforge/knowledge-base/plugin-basics/) and [ESL Plugins](/skyforge/knowledge-base/esl-plugins/) articles.

### ESL Checklist

You can ESL-ify a plugin if:

1. It contains fewer than 2048 new records (or none at all).
2. It contains new records, but the Form IDs only use the final three characters.
3. It does not contain new CELL records.

If a plugin contains new records and the Form IDs use more than the final three characters, they need to be **compacted** first. Remember that compacting Form IDs will break all dependencies.

## ESL-ifying

You can apply the ESL flag to any ESP or ESM plugin in SSEEdit.

- Load your plugins into SSEEdit.

### Form IDs

First, you need to find out whether the plugin's Form IDs are compatible with the ESL format.

- Right-click the plugin you wish to ESL-ify and select **Compact FormIDs for ESL**.
  - *This will trigger the general warning window if you did not disable it.*

If the plugin contains no new Form IDs or only Form IDs that only use the final three characters, SSEEdit will return that there was [nothing to do](/skyforge/modding-resources/creating-esl-plugins/sseedit-nothing-to-do.png). The plugin can be safely ESL-ified.

If the plugin contains new Form IDs that need to be reformatted (compacted), [SSEEdit will notify you](/skyforge/modding-resources/creating-esl-plugins/sseedit-renumber-formids.png) about the amount of records that need their Form IDs renumbered and that this will break dependencies. If you are certain that there are no dependencies or that all dependencies are currently active and loaded, go ahead and click **Yes** to continue.

### ESL Flag

After compacting Form IDs or ensuring that there are no incompatible Form IDs, you can add the ESL flag.

- Select the plugin you wish to ESL-ify to open the **File Header** in the right pane.
- Right-click the empty space next to **Record Flags** and select **Edit**.
- Check **ESL** in the window that pops up and click **OK**.
- Close SSEEdit and save your change(s).

![ESL Flagging](/Pictures/skyforge/beginners-guide/esl-flag-plugin.png)

## Full ESL

Adding the ESL flag to an ESP will create an ESP-FE hybrid that loads in ESP space but does not count toward the 256 ESM/ESP plugin limit. If you want to move the plugin into ESM space, you need to rename its file extension from **.ESP** to **.ESL**. This will create a full ESL.

If the plugin overwrites [references](/skyforge/knowledge-base/references), you <u>must</u> also add the **ESM** flag in SSEEdit to ensure that the list of Overriden Forms is populated and the plugin works as intended. I would generally recommend ESM-flagging full ESLs as they are all meant to load in ESM space and there is no downside to doing this.

{{< alert color="info" >}}Read more about [Overriden Forms](/skyforge/knowledge-base/references/#overriden-forms-onam).{{< /alert >}}