---
title: "Managing Creations"
weight:
type: docs
description: >
  How to manage the creations with Mod Organizer 2.
---

{{< alert color="info" title="Summary" >}}
> This module covers importing Creations into Mod Organizer 2 with Curation Club.<p>
> **Prerequisite(s):** [Mod Organizer 2](/skyforge/tool-setup/mo2/), [Curation Club](/skyforge/tool-setup/curation-club/){{< /alert >}}

## The Creations

Although the *creations* are official content, they are functionally mods. Most are rather small and consist of one or several archives (BSAs) and a plugin (ESL, rarely ESM). Their load order position is hard-coded.

When the *creations* are kept in the **data folder**, Mod Organizer 2 will treat them as official content: They will always be enabled and you cannot view/manipulate files like you can for other mods.

To simplify their management with Mod Organizer 2 I recommend importing them into the tool by placing them in regular mod folders. This can be automated with the [Curation Club](/skyforge/tool-setup/curation-club/) plugin.

### Importing Creations

Running **Curation Club** through Mod Organizer 2 will import all creations present in your default (Steam) installation **data folder** into Mod Organizer 2 where you can manage them like any other mod.

{{< alert color="warning" >}}Because **Curation Club** moves the creations out of the data folder rather than creating copies, you may want to create a backup first. Just copy all files starting with cc from `\Steam\steamapps\common\Skyrim Special Edition\Data\` to a convenient location.{{< /alert >}}

Run **Curation Club**.
    
![Run CC](/Pictures/skyforge/modding-resources/managing-creations/run-curation-club.png)

The default naming scheme `Creation Club - {creation}` is perfect for me (but feel free to change it to your preferences).

If you are following the Beginner's Guide or are using the [Root Builder](/skyforge/tool-setup/root-builder/) plugin for other reasons, check the box for **Root Builder Support**.

Click **OK** to import your creations.

{{< alert color="success" >}} You can now manage your Creations through Mod Organizer 2.{{< /alert >}}

---

#### If you are currently working through the Beginner's Guide, return to [Step 1](/skyforge/beginners-guide/step1/#free-creations).