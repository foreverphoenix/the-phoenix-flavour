---
title: "Step 2: Essential Mods"
weight: 2
type: docs
description: >
  Basic mods and fixes.
---

##### [SSE Engine Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/17230?tab=files)

#### Download Instructions

- **Main Files:** (Part 1) SSE Engine Fixes for 1.5.39 - 1.5.97

#### Preloader

SSE Engine Fixes requires the SKSE64 Preloader by meh and sheson. Download the **(Part 2) Engine Fixes - skse64 Preloader and TBB Lib** main file manually from the mod page.

Open the archive and extract the following files into your **Stock Game** folder:

- **d3dx9_42.dll**
- **tbb.dll**
- **tbbmalloc.dll**

Click **Yes** when asked to overwrite.

##### [SSE Display Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/34705?tab=files)

#### Download Instructions

- **Main Files:** SSE Display Tweaks

##### SSE Display Tweaks - Custom INI

SSE Display Tweaks supports a custom INI file in which settings from the main configuration file can be selectively overwritten. This way, you will not have to redo your changes every time the mod updates.

- Open your `\Mod Organizer 2\mods\` directory and create a new folder called **SSE Display Tweaks - Custom INI** inside.
- Create a new folder called **SKSE** inside the **SSE Display Tweaks - Custom INI** folder.
- Create a new folder called **Plugins** inside the **SKSE** folder.

The resulting file path should be: `\Mod Organizer 2\mods\SSE Display Tweaks - Custom INI\SKSE\Plugins\`.

- Inside the **Plugins** folder, right-click and select **New** >> **Text Document**.
- Rename the new file to **SSEDisplayTweaks_Custom.ini** (make sure to change the file extension).
- Open the new INI file in your preferred editor and add the following lines to it:

```
[Render]
Fullscreen=false
Borderless=true
FramerateLimit=60

[HAVOK]
PhysicsDamageMult=0

[Miscellaneous]
LoadScreenFilter=true
LoadScreenAllow=
LoadScreenBlock=DynDOLOD.esm
```

*This will force Borderless Fullscreen regardless of your INI settings so that (on Windows 10 systems) the DXGI flip model feature works, improving performance. The framerate will be capped at 60FPS which is still ideal for Skyrim although increasing or removing the cap will no longer break the game. Additionally, the random physics damage from colliding with objects will be disabled. The meme loadscreens from DynDOLOD will also no longer appear.*

- Save your changes and close the editor.
- Back in Mod Organizer 2, press F5 to refresh the interface.
- The new mod will now show up below the main SSE Display Tweaks. Activate it.

##### [Unofficial High Definition Audio Project (UHDAP)](https://www.nexusmods.com/skyrimspecialedition/mods/18115?tab=files)

#### Download Instructions

Click "Manual Download" for all files:

- **Main Files:** Music - HQ 
- **Main Files:** Voices EN - Part 1
- **Main Files:** Voices EN - Part 2

> With large files, there's always a risk that MO2 won't download them properly and they may get corrupted.

#### Installation Instructions

- Wait for all three archives to be downloaded.
- Move the files to your downloads folder: `\Your Modding Folder\ARCHIVE\MO2 Downloads\`.
- Mod Organizer 2 may freeze briefly as it processes the files.
- Once it unfreezes, you will find them in the **Downloads** tab (right pane).
- Right-click each of the three archives (one at a time) and select **Query Info**.
- After all data has been retrieved from the Nexus, install the archives as usual by double-clicking them.
- Don't change their names and simply select **Merge** for the second and third file to place all in the same mod folder.

##### [Unofficial Skyrim Special Edition Patch (USSEP)](https://www.nexusmods.com/skyrimspecialedition/mods/266?tab=files&file_id=209150)

#### Download Instructions

- **Main Files:** Unofficial Skyrim Special Edition Patch

> The link leads to directly to USSEP 4.2.5b which is the last version for pre-AE SSE. Unfortunately, Arthmoor insists on removing all old files from his mod pages even when they are still needed by most users.

#### Additional Instructions

Delete the following file(s) and/or folder(s):

- `Unofficial Skyrim Special Edition Patch.modgroups`

##### [Disable USSEP Book](https://www.nexusmods.com/skyrimspecialedition/mods/26092?tab=files)

#### Download Instructions

- **Main Files:** Disable USSEP Book

##### [Skyrim Landscape and Water Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/26138?tab=files)

#### Download Instructions

- **Main Files:** Skyrim Landscape and Water Fixes - FOMOD

#### FOMOD Instructions

- **Patches:**
  - ~~ELFX~~
  - ~~Relighting Skyrim~~
  - ~~CACO~~
  - Landscape Fixes for Grass Mods
- **Walkway Wall FIX:**
  - Walkway Wall FIX SMIM
- **Optional:**
  - Missing Lights Fix
  - ~~ELFX - Exteriors Fixed Mesh~~

#### Crop Ownership Removal

Since release 5.1, SLaWF adds ownership flags to crops and modifies the harvesting favour. The result is that, in order to harvest crops on a farm, you need to first ask the farmer to permission after which interacting with them will no longer mean stealing them. In theory, this is a great addition to immersion - it makes sense that farmers would not just let you harvest everything in vanilla.

In practice, this feature is problematic though. It breaks the Faction Stealing option from powerofthree's Tweaks for one. And it also requires a good amount of consistency patching work for a fairly minor change. Finally it is also simply feature creep for a mod intended to fix holes and seams in the landscape.

We are going to use **zEdit** and a script by **VictorF** (thanks again!) to remove the ownership flags added by SLaWF:

- Run **zEdit** through Mod Organizer 2.
- Make sure **zEdit** mode is selected at the top and the **Skyrim SE (TPF)** profile at the bottom, then click **Start Session**.
- In the plugin selection window, press CTRL+A to select all, then Space to disable them.
- Check the **Landscape and Water Fixes.esm** (its masters will be enabled automatically) and click **OK**.
- When the plugins are loaded, right-click the **Landscape and Water Fixes.esm** and select **Automate**.
- Under **Script**, change the name to **Remove_New_Ownership.js** and paste the following below:

```js
let node = zedit.GetSelectedNodes()[0];
let file = node.element_type === xelib.elementTypes.etFile? node.handle: xelib.GetElementFile(node.handle);

function extractCells(blocks){
	let subBlocks = blocks.map(block => xelib.GetElements(block, '')).flat();
	let cells = subBlocks.map(subBlock => xelib.GetElements(subBlock, '')).flat();
	return cells;
}
function extractWorldspaceCells(world){
	let children = xelib.GetElements(xelib.GetChildGroup(world));
	let persistentCell = children.find(el => xelib.Signature(el) === 'CELL');
	let blocks = children.filter(el => xelib.Signature(el) === 'GRUP');
	let cells = extractCells(blocks);
	if(persistentCell) cells.push(persistentCell);
	return cells;
}
function getAllCells(file){
	let worldspaces = xelib.GetElements(file, 'WRLD');
	let cells = worldspaces.map(extractWorldspaceCells).flat();
	cells.unite(extractCells(xelib.GetElements(file, 'CELL')));
	return cells;
}
function getRefs(cell){
	return xelib.GetElements(xelib.GetChildGroup(cell))
		.map(group => xelib.GetElements(group, '')).flat();
}

let refs = getAllCells(file).map(getRefs).flat()
	.filter(ref => xelib.HasElement(ref, "Ownership") &&
		!xelib.HasElement(xelib.GetPreviousOverride(ref, file), "Ownership"));
refs.forEach(ref => xelib.RemoveElement(ref, "Ownership"));
```

- Click **OK** to run the script. It should finish near instantly.
- Click the X in the corner to close zEdit. When prompted to save your changes to **Landscape and Water Fixes.esm**, click **Save**.

![SLaWF zEdit Save Changes](/Pictures/tpf/mod-installation/slawf-zedit-save-changes.png)

We have now successfully removed the ownership flags. All that remains are the dialogue edits which we can quickly delete in SSEEdit:

- Run **SSEEdit** through Mod Organizer 2.
- In the plugin selection window, right-click and **Select None**.
- Check only **Landscape and Water Fixes.esm** (its masters will be enabled automatically again) and click **OK**.
- Once the plugins are loaded up, double-click **Landscape and Water Fixes.esm** in the left pane to open it up.
- Select the **Dialogue Topic** and **Dialogue Branch** sections, then right-click and **Remove** them both.
- Close SSEEdit and click **OK** to save your changes.

![SLaWF xEdit Delete Dialogue](/Pictures/tpf/mod-installation/slawf-xedit-delete-dialogue.png)

##### [Weapons & Armor Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/14223?tab=files)

#### Download Instructions

- **Main Files:** Weapons & Armor Overhaul

##### [Clothing & Jewelry Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/14223?tab=files)

#### Download Instructions

- **Main Files:** Clothing & Jewelry Overhaul

##### [Weapons Armor Clothing and Clutter Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/18994?tab=files)

#### Download Instructions

- **Main Files:** Weapons Armor Clothing and Clutter Fixes

#### Additional Instructions

Balancing in TPF is overhauled by WAO and CJO which were custom made for the guide. However, we still require a good amount of assets from WACCF that I do not have the skill to recreate and lack the permissions to reshare.

- Install and activate **Weapons Armor Clothing and Clutter Fixes** in MO2.
- Rename it to **WACCF Assets for TPF**.
- Extract the **Weapons Armor Clothing & Clutter Fixes.bsa** ([instructions](/tpf/guide-resources/basic-instructions/#extracting-bsas)).
- Extract the **Weapons Armor Clothing & Clutter Fixes - Textures.bsa** ([instructions](/tpf/guide-resources/basic-instructions/#extracting-bsas)).
- Press F5 to refresh the MO2 virtual data folder.
- Delete the following file(s) and / or folder(s):
  - `scripts\`
  - `WACCF_BashedPatchLvlListFix.esp`
  - `Weapons Armor Clothing & Clutter Fixes - Textures.bsa`
  - `Weapons Armor Clothing & Clutter Fixes.bsa`
  - `Weapons Armor Clothing & Clutter Fixes.esp`

Only the **textures** and **meshes** folders should now remain in your mod folder:

![WACCF Surgery 1](/Pictures/tpf/mod-installation/waccf-surgery-1.png)

Unfortunately, we are not done.

**Delete ALL files EXCEPT for those listed below:**

- Meshes for the Shrouded Armor:
  - `meshes\armor\dbarmor\1stpersondbamorsleeveless_0.nif`
  - `meshes\armor\dbarmor\1stpersondbamorsleeveless_1.nif`
  - `meshes\armor\dbarmor\1stpersondbamorsleeveless_f_0.nif`
  - `meshes\armor\dbarmor\1stpersondbamorsleeveless_f_1.nif`
  - `meshes\armor\dbarmor\dbarmorhood---.nif` >> *all files starting with this*
  - `meshes\armor\dbarmor\dbarmorsleeveless_0.nif`
  - `meshes\armor\dbarmor\dbarmorsleeveless_1.nif`
  - `meshes\armor\dbarmor\dbarmorsleeveless_f_0.nif`
  - `meshes\armor\dbarmor\dbarmorsleeveless_f_1.nif`
- Mesh for the female Argonian Draugr helmet:
  - `meshes\armor\draugr\draugrhelmargonianf.nif`
- Meshes for the Thieves Guild Armor:
  - `meshes\armor\thievesguild\f\1stpersontorsovariant_0.nif`
  - `meshes\armor\thievesguild\f\1stpersontorsovariant_1.nif`
- Meshes for the Executioner Armor:
  - `meshes\clothes\executioner\bodyf_0.nif`
  - `meshes\clothes\executioner\bodyf_1.nif`
  - `meshes\clothes\executioner\cowlargf_0.nif`
  - `meshes\clothes\executioner\cowlargf_1.nif`
  - `meshes\clothes\executioner\cowlargm_0.nif`
  - `meshes\clothes\executioner\cowlargm_1.nif`
  - `meshes\clothes\executioner\cowlelff_0.nif`
  - `meshes\clothes\executioner\cowlelff_1.nif`
  - `meshes\clothes\executioner\cowlelfm_0.nif`
  - `meshes\clothes\executioner\cowlelfm_1.nif`
  - `meshes\clothes\executioner\cowlf_0.nif`
  - `meshes\clothes\executioner\cowlf_1.nif`
  - `meshes\clothes\executioner\cowlm_0.nif`
  - `meshes\clothes\executioner\cowlm_1.nif`
  - `meshes\clothes\executioner\cowlmgnd.nif`
  - `meshes\clothes\executioner\glovesf_0.nif`
  - `meshes\clothes\executioner\glovesf_1.nif`
  - `meshes\clothes\executioner\glovesgo.nif`
- Meshes for Ulfric's Armor:
  - `meshes\clothes\yarlclothes02\1stpersonulfricf_0.nif`
  - `meshes\clothes\yarlclothes02\1stpersonulfricf_1.nif`
  - `meshes\clothes\yarlclothes02\ulfricbootsf_0.nif`
  - `meshes\clothes\yarlclothes02\ulfricbootsf_1.nif`
  - `meshes\clothes\yarlclothes02\ulfricf_0.nif`
  - `meshes\clothes\yarlclothes02\ulfricf_1.nif`
  - `meshes\clothes\yarlclothes02\ulfricglovesf_0.nif`
  - `meshes\clothes\yarlclothes02\ulfricglovesf_1.nif`
- Meshes for the Ancient Falmer Armor
  - `meshes\dlc01\armor\ivory\f\cuirassivoryalternate_0.nif`
  - `meshes\dlc01\armor\ivory\f\cuirassivoryalternate_1.nif`
- Textures for the Executioner's Armor:
  - `textures\clothes\executioner\executioners_cowlf.dds`
  - `textures\clothes\executioner\executioners_cowlf_n.dds`
  - `textures\clothes\executioner\executioners_cowlm.dds`
  - `textures\clothes\executioner\executioners_cowlm_n.dds`
  - `textures\clothes\executioner\executioners_glovesf.dds`
  - `textures\clothes\executioner\executioners_glovesf_n.dds`
  - `textures\clothes\executioner\executioners_torsof.dds`
  - `textures\clothes\executioner\executioners_torsof_n.dds`

If you now check the file size of the `\Mod Organizer 2\mods\WACCF Assets for WAO & CJO\` folder it should be **XXmb**.

##### [SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/12604?tab=files)

#### Download Instructions

- **Main Files:** SkyUI_5_2_SE

##### [Fix Note Icon for SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/32561/?tab=files)

#### Download Instructions

- **Main Files:** FixNotesForSkyUI SKSE64 2.0.17 and 2.0.19

##### [SkyUI Ghost Item Bug Fix](https://www.nexusmods.com/skyrimspecialedition/mods/49106?tab=files)

#### Download Instructions

- **Main Files:** SkyUI - Ghost Item Bug Fix

##### [SkyUI Weapons Pack](https://www.nexusmods.com/skyrimspecialedition/mods/37231?tab=files)

#### Download Instructions

- **Main Files:** SkyUI Weapons Pack SE 1.3

##### [Better Dialogue Controls](https://www.nexusmods.com/skyrimspecialedition/mods/1429?tab=files)

#### Download Instructions

- **Main Files:** Better Dialogue Controls v1_2

##### [Better MessageBox Controls](https://www.nexusmods.com/skyrimspecialedition/mods/1428?tab=files)

#### Download Instructions

- **Main Files:** Better MessageBox Controls v1_2

##### [More Informative Console](https://www.nexusmods.com/skyrimspecialedition/mods/19250?tab=files)

#### Download Instructions

* **Main Files:** More Informative Console 0.43

##### [Dear Diary - Better More Informative Console](https://www.nexusmods.com/skyrimspecialedition/mods/46437?tab=files)

#### Download Instructions

- **Main Files:** Dear Diary - Better More Informative Console

---

#### Continue with the [Assorted Plugins](/tpf/mod-installation-1/step-3/) page.