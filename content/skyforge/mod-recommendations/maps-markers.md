---
title: "Maps & Markers"
weight: 14
type: docs
description: >
  Mod recommendations.
---

## Map Mods

When it comes to map mods, your choice boils down to the following:

- Improvements to the vanilla 3D world map.
- Complete replacement with a paper-style world map.

In vanilla, two worldspaces have maps: Skyrim and Solstheim. Some mods add proper maps for vanilla worldspaces like the Soul Cairn or the Forgotten Vale, and of course mods may add worldspaces with maps of their own.

{{< alert color="info" >}}While the vanilla map does not mark roads and paths, most map mods add them. *A Quality World Map* does so through manual modification of the LOD Level 32 textures while *A Clear Map of Skyrim and Other Worlds* generates them with LOD tools. Most paper world maps also add at least the major roads.{{< /alert >}}

- **Subtlety:** *Enhanced Worldspace Maps*
- **Convenience:** *A Quality World Map* and/or *Enhanced Worldspace Maps*
- **Consistency:** *A Clear Map of Skyrim and Other Worlds*
- **Novelty:** *Flat World Map Framework* + paper map retextures

### Paper vs 3D Map

If **consistency** is important to you, you may prefer the 3D world map over paper replacements. The reason for this is that there are many paper map textures, but few that are in a similar style. Unless you are not bothered by wildly different map styles for different worldspaces, I would recommend the 3D world map.

Paper map **patches** exist for many major worldspaces added by mods such as Wyrmstooth or Bruma. However, not all mods with new worldspaces have patches available.

In terms of **convenience**, paper world maps add extra steps and mod requirements to make them work with the vanilla map system that is made for a 3D map rather than a flat one. This is not too difficult, but means that a paper map overhaul is somewhat more involved by comparison.

### Maps & LOD

While paper map mods are simply flat textures, the 3D map uses [LOD](/skyforge/knowledge-base/distant-lods/) to populate the map with trees and objects. This means that regenerating LODs to match your mods (for tree overhauls, new settlements, etc) will update your map in turn. This is true for all map mods, but only *A Clear Map of Skyrim and Other Worlds* is based around and requires custom LOD integration to substantially increase the map quality.

The map uses **LOD Level 32** terrain LOD and **LOD Level 16** object LOD by default.

If your map mod comes with custom-made [LOD Level 32 textures](/Pictures/skyforge/mod-recommendations/maps-markers/lod-level-32-textures.png) you need to let them <u>overwrite</u> your **Terrain LOD** output generated with [SSELODGen](/skyforge/tool-setup/sselodgen/). This is the case for paper map mods as well as *A Quality World Map*.

Only *A Clear Map of Skyrim and Other Worlds* will actually take your Terrain LOD textures (which are based on your landscape textures) into account. If you use a green Whiterun plains overhaul or Seasons of Skyrim, this will be clearly visible on the map. 

{{< alert color="warning" >}}**Mod Order:** The *Maps & Markers* separator is fairly high up in my mod order because I use ACMOS which uses the Terrain LOD output. If you are using a map overhaul other than ACMOS, it will need to overwrite Terrain LOD and you may want to move the separator below the patcher output separator in your mod order.{{< /alert >}}

### Remove Depth Blur

You can remove the depth blur on the map by adding the following lines to the **Skyrim.ini**:

```
[MapMenu]
bWorldMapNoSkyDepthBlur=1
fWorldMapDepthBlurScale=0
fWorldMapMaximumDepthBlur=0
fWorldMapNearDepthBlurScale=0
```

Alternatively, you can add the lines to a plugin INI.

{{< alert color="info" >}}*A Clear Map of Skyrim and Other Worlds* and *A Quality World Map* already contain plugin INIs with these settings.{{< /alert >}}

### Map Weather

The lighting on the world map is determined by a **Weather** record: `000A6858 WorldMapWeather`. Some map mods, like *A Quality World Map*, modify this record. In case of conflicts between weather overhauls and map mods in this record, I recommend letting the map mod win. Alternatively, you can overwrite with *Weather of Worlds* if you prefer its weather edits.

A more sophisticated option is *Unique Map Weather* plus addons for unique lighting per map. Otherwise, a map added for worldspaces such as the Soul Cairn would always have the same lighting as the Skyrim map.

##### [A Quality World Map](https://www.nexusmods.com/skyrimspecialedition/mods/5804)

*A Quality World Map* is the classic map replacer, improving the vanilla 3D map with modified LOD Level 32 textures. This includes adding roads and plenty more detail, covering both Skyrim and Solstheim. The *Vivid* version also significantly reworks the colours.

If you want a simple, no-frills map replacer that requires no extra steps, this is your best option. However, remember that *A Quality World Map* will not take your custom landscape textures and Terrain LOD into account, and it will not add as much additional detail to the maps as *A Clear Map of Skyrim and Other Worlds*.

#### Download Recommendations

<mark>Classic or Vivid with roads plus the Clear Map Skies addon.</mark>

If using **Classic** I recommend *unpacking* the assets to ensure they can overwrite Terrain LOD resources. <u>Mind your mod order.</u> This mod's assets should win all conflicts.

#### Paper Map

There is also a paper map option for Skyrim (but not Solstheim) on the *A Quality World Map* mod page. If you want to go down the paper world map route, I would <u>not</u> recommend downloading this one, but going with the *Flat World Map Framework* and compatible map mods instead.

#### Additional Notes

The **Classic** version of the mod has a plugin to load the BSAs and a plugin INI to disable map blur, and to modify the weather record. Remember to check for conflicts with weather overhauls and let this mod win.

The **Vivid** version includes a quest in the plugin and two scripts to disable blur on the map instead of a plugin INI. Remember that it will overwrite your INI settings at runtime.

##### [Enhanced Worldspace Maps](https://www.nexusmods.com/skyrimspecialedition/mods/57176)

*Enhanced Worldspace Maps* can be paired with *A Quality World Map* or used standalone for some improvements to the two vanilla maps and to add proper maps for additional worldspaces (see list below) without changing anything stylistically.

- Blackreach
- Soul Cairn
- Beyond Skyrim: Bruma
- Wyrmstooth

*Enhanced Worldspace Maps* includes **custom weathers** for each worldspace, except for Skyrim and Solstheim for which it recommends *Unique Map Weather - Vanilla Additions*. This requires *Unique Map Weather*.

The mod is fully modular. You can pick and choose.

##### [A Clear Map of Skyrim and Other Worlds](https://www.nexusmods.com/skyrimspecialedition/mods/56367) (ACMOS)

*A Clear Map of Skyrim and Other Worlds* combines the features from the previous two mods while adding support for some additional mod-added worldspaces. Unlike *A Quality World Map*, it does not provide modified LOD Level 32 textures but provides resources to rebuild them in much higher detail with LOD generation tools while taking your mod choices into account. For example, with Seasons of Skyrim you will see snow all over the map during winter. ACMOS also adds paths and roads, and greatly improves map navigation (zoom, tilt, etc).

Worldspaces that are given proper maps with ACMOS include:

- Blackreach
- Skuldafn
- Sovngarde
- Forgotten Vale
- Soul Cairn
- Beyond Reach
- Beyond Skyrim: Bruma
- Falskaar
- Midwood Isle
- Vominheim
- Wyrmstooth

ACMOS includes **custom weathers** for each worldspace. This requires *Unique Map Weather*.

ACMOS <u>requires</u> fully [rebuilding all LODs](/skyforge/modding-resources/lod-occlusion/) with SSELODGen and DynDOLOD. Taking these extra few steps (described in the linked instructions) is more work than installing *A Quality World Map* but well worth the results.

{{< alert color="info" >}}Until you generate LODs, the map will look terrible and you will likely run into [large reference bugs](/skyforge/knowledge-base/large-reference-bug/). This is normal and will be fixed once LODs are present.{{< /alert >}}

#### FOMOD Recommendations

If you are going to follow [my instructions](/skyforge/modding-resources/lod-occlusion/) for regenerating LODs which include the extra steps for ACMOS, pick the following FOMOD options:

- **DynDOLOD Rules:** DynDOLOD 3
- **LOD Setup:** With DynDOLOD LOD32
- **Other Worlds:** *Check any that apply*

The **Remove Clouds** option will remove *all* map clouds, including those that obscure clouds on the very edge of the map. With it enabled, you will be able to look at jagged, unfinished terrain. On the other hand, the clouds often make it difficult to properly view the map. As a compromise, you could try the *Clear Map Skies* addon from *A Quality World Map* which does not remove the clouds from the edge of the map. This will still obscure some locations, like Castle Volkihar.

#### Load Order

The plugin from *A Clear Map of Skyrim and Other Worlds* qualifies as a [late loader](/skyforge/knowledge-base/late-loaders/), so keep it in the *late loader* section of your load order. Patches for lighting or water overhauls may be required, check in SSEEdit.

##### [Weather of World](https://www.nexusmods.com/skyrimspecialedition/mods/58782)

*Weather of World* is a simple map weather overhaul that can be used with the vanilla map or *A Quality World Map*.

##### [Unique Map Weather](https://www.nexusmods.com/skyrimspecialedition/mods/59919)

*Unique Map Weather* adds a framework for adding separate weather records per map. For example, it can be used to add dust storms to Solstheim or a purple hue to the Soul Cairn. Both *Enhanced Worldspace Maps* and *A Clear Map of Skyrim and Other Worlds* have inbuilt support for this mod and you should install it for best results.

**Requirement(s):** Skyrim Script Extender, Address Library for SKSE

##### [Unique Map Weather - Vanilla Additions](https://www.nexusmods.com/skyrimspecialedition/mods/78586)

*Unique Map Weather - Vanilla Additions* adds custom weathers for Solstheim and the Soul Cairn. Remember that the Soul Cairn will only have a map of its own with *Enhanced Worldspace Maps*. I recommend using this mod with *A Quality World Map* and / or *Enhanced Worldspace Maps*.

Do not use this mod with *A Clear Map for Skyrim and Other Worlds*.

**Requirement(s):** Unique Map Weather

##### [Flat World Map Framework](https://www.nexusmods.com/skyrimspecialedition/mods/29932)

*Flat World Map Framework* is absolutely essential if you want a paper world map. Because the vanilla map is three-dimensional it does not easily lend itself to a flat texture and map markers are placed to match the 3D perspective. Paper maps look especially good in combination with paper-themed UI overhauls such as [Dear Diary](https://www.nexusmods.com/skyrimspecialedition/mods/23010).

**In addition to the framework, you will need the actual retextures.** Most if not all compatible retextures for vanilla- and mod-added maps are listed on the mod page. The mod's FOMOD installer also contains some basic options.

**Requirement(s):** Skyrim Script Extender, Address Library for SKSE, SkyUI (if using MCM), MCM Helper (if using MCM)

#### FOMOD Recommendations

I recommend against selecting the patches for water/lighting overhauls in the FOMOD, mostly because they cannot address any three-way conflicts with other plugins. Create a custom patch for Worldspace (and CELL) record edits instead. Check the [late loader](/skyforge/knowledge-base/late-loaders/) article for more information (see *CELL Record Overwrite*).

The *Enhanced Volumetric Lighting and Shadows (EVLaS)* patch should <u>not</u> be necessary. Generate the underside mesh with DynDOLOD instead.

Do install the MCM for ingame customisation.

#### Load Order

Always let the weather edits from *Flat World Map Framework* overwrite other mods.

The plugin from *Flat World Map Framework* qualifies as a [late loader](/skyforge/knowledge-base/late-loaders/), so keep it in the *late loader* section of your load order. Patches for lighting or water overhauls may be required, check in SSEEdit.

##### [Common Marker Addon Project](https://www.nexusmods.com/skyrimspecialedition/mods/56123) (CoMAP)

*Common Marker Addon Project* adds new [map markers](https://docs.google.com/spreadsheets/d/174cztnd1qLoeCd6RzBFusf2QkIDZP622ZSGRNvC3Pfw/edit#gid=1187758697) for vanilla and new worldspaces added by mods. Check [this article](https://www.nexusmods.com/skyrimspecialedition/articles/3520) for a list of mods that already have CoMAP compatibility / integration.

**Requirement(s):** Skyrim Script Extender, Address Library for SKSE, SkyUI

#### Config File

In the **MapMarkerFramework.ini** you can configure multiple options. I recommend either creating a copy to overwrite the original with or at least documenting your changes in the MO2 **Notes** tab so you can re-apply them after an update to the mod.

Reducing the map markers to 75% size may help with markers overlaying each other and being difficult to click. It also looks a little neater (though this is subjective). You can also reduce map marker size in the *Atlas Map Markers* MCM if you use that mod.

```
fMarkerScale=0.75
```

The other two options control the obscured icons you see on the map and compass when you know the location but have not discovered it yet or (on the compass) if you are getting closer to it. If you prefer to not get "spoiled" about the location type, set either or both of these options to `1`. A generic icon for "undiscovered location" can be selected in the FOMOD.

#### Compatibility

While the CoMAP framework is very unintrusive, be aware that it will not be compatible with map marker replacers (recolours) out of the box. They can be used at the same time, but the design between old and new markers will not match without a manual patch.

When using a paper map mod, you may want to prefer beige map markers as they tend to look better than the vanilla white ones. *Dear Diary Dark Mode* is one of the few interface overhauls with CoMAP support so even if you do not want the rest of the mod, definitely grab the map markers.

{{< alert color="info" >}}The same map markers are used on the compass and on the actual map.{{< /alert >}}

#### Additional Notes

If you choose to install the map marker for Jorrvaskr, also install the [Proving Honor Companions Quest Progression Fix](https://www.nexusmods.com/skyrimspecialedition/mods/66128) to avoid breaking the *Proving Honor* quest by immediately travelling to Jorrvaskr. You can also enable a map marker for Jorrvaskr in *Atlas Map Markers*.

##### [Atlas Map Markers](https://www.nexusmods.com/skyrimspecialedition/mods/24104)

*Atlas Map Markers* adds various new map markers which is especially useful with mods that add maps to vanilla worldspaces as the Soul Cairn, the Forgotten Vale, etc, will have no markers by default. If you only want markers for these worldspaces because you have a mod adding proper maps to them, you can disable all other options in the mod's MCM.

[MCM settings loader available.](https://www.nexusmods.com/skyrimspecialedition/mods/68573)

**Requirement(s):** SkyUI

#### Additional Notes

If you choose to install the map marker for Jorrvaskr, also install the [Proving Honor Companions Quest Progression Fix](https://www.nexusmods.com/skyrimspecialedition/mods/66128) to avoid breaking the *Proving Honor* quest by immediately travelling to Jorrvaskr. You can also enable a map marker for Jorrvaskr in *Common Marker Addon Project*.

##### [HD Local Map](https://www.nexusmods.com/skyrimspecialedition/mods/74722)

{{< alert color="info" >}}**Recommended.** Very useful in any setup.{{< /alert >}}

*HD Local Map* is an SKSE plugin which greatly improves the quality of the local map (used in interior Cells and Worldspaces which do not have world maps of their own).

**Requirement(s):** Skyrim Script Extender, SkyUI