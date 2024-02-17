---
title: "Filter for Conflicts"
weight:
type: docs
description: >
  How to apply a filter for conflicts in SSEEdit.
---

{{< alert color="info" title="Summary" >}}
> This module covers how to create and apply a filter for conflicts in SSEEdit.<p>
> **Prerequisite(s):** [SSEEdit](/skyforge/tool-setup/sseedit/){{< /alert >}}

## SSEEdit Filter

SSEEdit has an indepth, customisable filter system with the ability to save settings as presets. A *filter for conflicts* can be extremely helpful for [Conflict Management](/skyforge/knowledge-base/conflict-management/).

### Conflict Resolution Filter

Conflicts can be identified by applying a filter in SSEEdit.

- Load up your plugins in SSEEdit.
- Right-click anywhere in the left pane and select **Apply Filter**.
- Click the **Add** button at the top to create a new filter.
- Name it **Conflict Resolution** and click **OK**.

Your new filter will be selected automatically. Check the following options:

![CR Filter](/Pictures/skyforge/beginners-guide/cr-filter.png)

{{< alert color="info" >}}The two options near the top will visualise conflicts which makes finding them infinitely easier. Flattening CELL records helps with viewing the Cell and Worldspace categories without having to click through blocks and sub-blocks.{{< /alert >}}

- Click the **Save** button at the top to save the new preset.
- Click the **Filter** button at the bottom to apply it.

This may take several minutes. You can proceed once the log returns `Done: Applying Filter`.

If you wish to remove the filter, right-click in the left pane and select **Remove Filter**.

{{< alert color="warning" >}}The next time you wish to filter for conflicts, right-click in the left pane, select **Apply Filter**, make sure your preset is selected, and click **OK**.{{< /alert >}}
