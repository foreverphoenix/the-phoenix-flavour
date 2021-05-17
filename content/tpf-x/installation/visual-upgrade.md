---
title: "Visual Upgrade"
weight: 2
type: docs
description: >
  Additional mods to improve the graphics.
---

## About this section

The main guide has always tried to stay as performance-friendly as possible in its choices of INI settings, mods, ENB, and so forth. Even though I'm lucky enough to own a RTX 3080 now, I wanted to keep base TPF useable for a variety of systems. However, for those with more powerful hardware there are now some additional mods.

There are two sections on this mod page: Grass overhaul (for QW's Grass Patch) and ENB (for Rudy ENB). You can install either, both, or none.

## Grass Overhaul

QW's Grass Patch combines the best of Veydosebrom, Cathedral 3D Pine Grass, and Folkvangr, tweaking grass density to be consistent across the board. The performance impact over default TPF (which only has Veydosebrom) is likely increased.

### **[Folkvangr - Grass and Landscape Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/44899?tab=files)**

An absolutely incredible grass overhaul. Does stray from vanilla quite a bit but I haven't yet found a single place I didn't like. QW's Grass Patch mostly retains Folkvangr's phenomenal pine forest and rift grasses. 

#### Download Instructions

- **Main Files:** Folkvangr - Grass and Landscape Overhaul

#### Additional Instructions

- Delete the following file(s) and / or folder(s):
  - `Folkvangr - Grass and Landscape Overhaul.ini`

### **[Cathedral 3D Pine Grass](https://www.nexusmods.com/skyrimspecialedition/mods/42032?tab=files)**

This is a very performance-friendly and beautiful overhaul for pine grass only. It adds a large number of different grasses, including higher plants that make the Falkreath forest look significantly more dense and overgrown (which is toned down by QW's Grass Patch though).

#### Download Instructions

- **Main Files:** Cathedral - 3D Pine Grass - Full 3D Coverage

#### Additional Instructions

- Delete the following file(s) and / or folder(s):
  - `Cathedral - 3D Pine Grass.ini`

#### INI Tweaks

- Open the **INI Editor** in Mod Organizer 2 (Tools >> Tool Plugins >> INI Editor).
- Switch to the **skyrimcustom.ini** tab.
- Below the existing lines, copy and paste the following:

```
[Display]
fSAOIntensity=7
fWindGrassMultiplier=1.4
```

- Close the window and click **Yes** when asked to save your changes.

### ESL-ifying Plugins

The plugin for QW's Grass Patch will expect all three grass overhauls to have compacted formIDs (otherwise it will throw errors and you will be unable to even launch the game). We already compacted and ESL-ified Veydosebrom for the main guide, but Folkvangr and Cathedral 3D Pine Grass will need the same treatment.

- Make sure both **Folkvangr** and **Cathedral 3D Pine Grass** are active in your mod and load order.
- Launch **SSEEdit** through Mod Organizer 2.
- Click **OK** in the plugin selection window and wait for SSEEdit to finish loading.

Now you can renumber FormIDs for Folkvangr:

- Scroll down to **Folkvangr - Grass and Landscape Overhaul.esp**.
- Right-click the plugin and select **Compact FormIDs for ESL**. 
- A warning will pop up, click **Yes I'm absolutely sure**.
- Click **OK** again for the warning about renumbering FormIDs.
- Wait until SSEEdit returns `Done: Changing FormIDs` (should only take a second).

Since FormIDs are renumbered now for ESL space, you can flag the plugin as ESL:

- At the bottom (below the SSEEdit log) click the **View** tab to see Folkvangr's file header.
- Right-click the empty space to the right of **Record Header** >> **Record Flags**.
- Select **Edit**, check **ESL** in the list, and click **OK**.

Done! Folkvangr is now successfully compacted and ESL-ified.

**Repeat the same process for Cathedral 3D Pine Grass:** Renumber FormIDs, then flag the plugin as ESL.

Once both plugins are done, close SSEEdit. Click **OK** when prompted to save your changes.

### **[QW's Grass Patch](https://www.nexusmods.com/skyrimspecialedition/mods/48689?tab=files)**

This is the patch to rule them all, tweaking various grasses added by Veydosebrom, Folkvangr, and Cathedral 3D Pine Grass as well picking which grasses should appear where.

#### Download Instructions

- **Main Files:** QW's Grass Patch (no DoS)

#### Additional Instructions

- Delete the following file(s) and / or folder(s):
  - `QW's Grass Patch.ini`

### Grass Density

TPF's default grass density is iMinGrassSize=20 which is how Veydosebrom looks best. However, while QW's Grass Patch was also made for the same value, its grass is *very* dense at that setting and you can gain back some valuable frames by increasing iMinGrassSize slightly. I recommend testing your frame rate ingame before deciding to increase iMinGrassSize which will *lower* grass density and *improve* performance.

If you decide that you want a higher frame rate, follow these steps:

- Open the **INI Editor** in Mod Organizer 2 (Tools >> Tool Plugins >> INI Editor).
- Switch to the **skyrimcustom.ini** tab.
- Below the existing lines, copy and paste the following:

```
[Grass]
iMinGrassSize=35
```

- Close the window and click **Yes** when asked to save your changes.

## Rudy ENB

At this time, Rudy ENB is probably the most feature-rich and certainly one of the most impressive ENB presets out there. It has a slew of requirements which we will need to cover also.

If you decide to install Rudy ENB, you need to install all other files from this section as well.

### **[Rudy ENB - Weather Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/39113?tab=files)**

#### Download Instructions

- **Main Files:** Rudy ENB Cathedral Weathers required files Part I
- **Main Files:** Rudy ENB Cathedral Weathers required files Part II >> `merge with the main file`

#### Additional Instructions

- Delete the following file(s) and / or folder(s):
  - `Cathedral Weathers.ini`

### **[Rudy ENB Files](https://www.nexusmods.com/skyrimspecialedition/mods/39113?tab=files)**

#### Download Instructions

- **Main Files:** Rudy ENB SE for Cathedral Weathers

Download the file manually.

#### Installation Instructions

We will extract the required files from the archive before installing them in ENB Man.

- In Windows Explorer, go to your temp folder: `Your Modding Folder\temp`. It should be empty.
- Open the download Rudy ENB archive.
- Go to `Rudy for SSE 4.0a1 CW\! Catherdral Weathers Version\[ Skyrim SE folder ]`.
- Extract both files and the folder to your temp folder.

These are the base ENB files that may now be overwritten by addons.

- Go to `Rudy for SSE 4.0a1 CW\! Catherdral Weathers Version\ADDONS`.
- Double-click the **Lighting mods** folder and then **Normal Game**.
- Open the **If Luminosity is placed after Window Shadows** folder.
- Extract the **enbseries** folder into your temp folder.
- Click **Yes** when asked to merge folders and replace files.

This installed the ENB code for the night eye fix. The matching plugin-based tweaks will be part of the next mod.

- Open **ENB Man**, the preset management tool installed during the main guide.
- Double-click the **Skyrim SE** profile.
- Click the big arrow under **Presets** and select **Blank Preset**.
- Enter **Rudy ENB for Cathedral Weathers** and click the green checkmark.
- Move the folder and both files from the temp folder into ENB Man.
- Under **Binary**, make sure the latest version is selected and checked.
- Click the green checkmark at the bottom to install the preset.
- If asked to update modified files from your previous preset, click the green checkmark.
- Close ENB Man. Rudy ENB is now installed.

### **[Misc Tweaks - Night Eye Redux - ENB Fix](https://www.nexusmods.com/skyrimspecialedition/mods/38348?tab=files)**

A tiny patch for Night Eye Redux, merging the tint color changes from the ENB night eye fix with the changes from NER. This allows you to use night eye with Rudy ENB.

#### Download Instructions

- **Optional Files:** Misc Tweaks - Night Eye Redux - ENB Fix

### **[Bright Snow Fix for ENB](https://www.nexusmods.com/skyrimspecialedition/mods/41737?tab=files)**

Lowers brightness of the snow flake texture so it's not overblown with ENB. Didn't find this necessary with Serio's ENB but it helps with Rudy.

#### Download Instructions

- **Main Files:** Bright Snow Fix

### **[Dynamic Volumetric Lighting and Sun Shadows](https://www.nexusmods.com/skyrimspecialedition/mods/44483?tab=files)**

Synchronises sun and exterior shadows. This mod is a hard requirement for Rudy ENB.

#### Download Instructions

- **Main Files:** Dynamic Volumetric Lighting and Sun Shadows

### Rudy ENB - DVLaSS INI

Rudy comes with its own preset for DLVaSS.

#### Installation Instructions

- In Mod Organizer 2, create a new empty mod: **Rudy ENB - DVLaSS INI**.
- Right-click the new mod and click **Open in Explorer**.
- Open the Rudy ENB archive (with the ENB files) once again.
- Navigate to `Rudy for SSE 4.0a1 CW\! Catherdral Weathers Version\ADDONS`.
- Double-click the **Rudy ENB DVLaSS ini.rar** and open the **Data** folder inside.
- Extract the **SKSE** folder into the mod folder you created before.
- In Mod Organizer 2, press F5 to refresh.

### DynDOLOD - Generate Terrain Underside

While there is a terrain underside mesh available on the DLVaSS mod page, it is recommended to use DynDOLOD to generate one for one's setup. This is a new feature in DynDOLOD 3.0 that you need to enable now. DynDOLOD will be regenerated later on.

#### INI Tweak

- Navigate to `Your Modding Folder\Tools\DynDOLOD\Edit Scripts\DynDOLOD\`.
- Open the **DynDOLOD_SSE.ini** in Notepad++.
- Scroll down to **Line 270** and uncomment it (remove the semicolon `;`).
- Scroll down to **Line 275** and change **TerrainUnderside=** to **1**.
- Save and close the file.