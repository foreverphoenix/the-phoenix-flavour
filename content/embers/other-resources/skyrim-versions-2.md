---
title: "Skyrim Versions"
weight: 1
type: docs
no-list: false
description: >
 About the different versions of Skyrim.
---

## Timeline

- 2011: Skyrim
- 2013: Skyrim Legendary Edition (SLE)
- 2016: Skyrim Special Edition (SSE)
- 2018: Skyrim VR (SVR)
- 2021: Skyrim Anniversary Edition (SAE)

### Skyrim (2011)

Skyrim was originally released on November 11, 2011 for PC, Xbox 360, and PlayStation 3. Three paid DLC were released: Dawnguard, Hearthfire, and Dragonborn, that were available on all platforms. Since not everyone owned every DLC, it became standard for mods to state which DLC were supported or outright required. There were separate Unofficial Patches for the base game (Unofficial Skyrim Patch, USKP) and each DLC.

Only the PC version of the original Skyrim could be modded. Most Skyrim mods can be found on the [Skyrim](https://www.nexusmods.com/skyrim) portal on Nexus mods, but there is also a Steam workshop page. The classic version of the Skyrim Script Extender for the 2011 release is still available on the SKSE website.

### SLE: Skyrim Legendary Edition (2013)

An all-in-one package of Skyrim, the base game with all three DLC and some new extra features (legendary difficulty and legendary skills) was released in 2013 for the same platforms as the original. This version of Skyrim is typically abbreviated as **SLE**. The modding community gradually shifted to largely offer merged files that required all DLC / SLE, for example the Unofficial Patches were merged together into the Unofficial Skyrim Legendary Edition Patch (USLEEP). Skyrim + all DLC became the standard requirement as supporting different versions or patches for various DLC combinations was too cumbersome.

Both the original Skyrim and the Legendary Edition re-release are also known as **Classic Skyrim** or **Oldrim**.

### SSE: Skyrim Special Edition (2016)

A remastered version of Skyrim with all DLC packs was released in 2016 for PC, Xbox One, and Playstation 4. The **SSE** came with a number of significant changes: It was built on the upgraded 64bit version of the Creation Engine originally developed for Fallout 4 which was released a year prior. This meant that the game could now use a larger amount of system memory, fixing various crashes. Compared to the original, SSE was rock solid.

However, the SSE engine upgrade required many of the most important mods and frameworks to be essentially rebuilt from scratch which took a while. The SSE modding community did not pick up steam until late 2017.

As foundation for a modded setup, SSE was the superior option because of its increased stability and once certain mods were ported over, most of the modding community followed suit. Many mods were eventually discontinued for SLE and only developed for SSE. Others never released for SLE to begin with. The Skyrim modding community entered an unexpected rennaissance with many revolutionary new mods being released in that time.

SSE also brought with it a new modding platform, the **Bethesda.net** website. It was largely used for **console modding** which now became possible, although because of technical limitations could never reach the complexity of modding on PC. Notably, Steam never added a workshop for SSE (it would have been fairly redundant).

### SVR: Skyrim VR (2018)

Skyrim SE was ported to VR in 2018 for PC and PlayStation 4. Its modding community largely overlaps with the SSE one and most SSE mods can be used in VR. However, there is a specific version of the Script Extender for SVR so any SKSE plugins need to be made specifically for the VR version of SKSE. All other SSE mods can be used as usual with SVR, porting steps are not required.

### SAE: Skyrim Anniversary Edition (2021)

On its tenth birthday, Skyrim was re-released once more for PC, Xbox Series X/S, and Playstation 5. This time around, the upgrade added all existing and some new "creations" packaged together. Unlike the SSE upgrade for SLE users, the SAE upgrade was not free for SAE users (only discounted).

Unlike SLE and SSE, the SAE is not a separate game in the Steam library, but rather a DLC for SSE. The base game edits it made (adding some assets) were part of a free update for SSE, 1.6.318.0, and buying the DLC would simply prompt the game to download all Creation Club content upon launching it. Thus, the modding community will likely move on to the new version of SSE that was released alongside SSE. However, this does not mean that AE will became a requirement or develop its separate modding community like SSE did. Buying the AE upgrade will remain optional, although Creation Club support or integration will likely become more common for mods.

## Technical Differences

Essentially, all versions of Skyrim can be split into two categories: **Classic Skyrim** with the old **32bit engine** and **Skyrim SE** with the upgraded **64bit engine**. All Skyrim releases after 2016 are based on SSE (Skyrim VR and Skyrim AE). Most mods made for the old engine version (Skyrim, SLE) need to be ported before they can be safely used in the new engine version (SSE, SVR, SAE).

### Script Extender

How well a version of Skyrim can be modded depends on whether there is a version of SKSE available for it. There are now four different versions of SKSE available:

- **SKSE** is compatible with the Steam version of Classic Skyrim / Skyrim LE.
- **SKSE 64** is compatible with the Steam version of Skyrim SE up until release `1.5.97.0`.
- **SKSE VR** is compatible with the Steam version of Skyrim VR.
- **SKSE AE** is compatible with the Steam version of Skyrim SE from release `1.6.318.0` onwards.

SKSE is not available for any console port or the Xbox Game Pass version of Skyrim SE for PC.

## Creation Club

One of SSE's major features was the Creation Club offering additional mini-DLC, "creations", made by Bethesda and various modders hired by them. The Creation Club is available for Skyrim SE, Skyrim VR, and Skyrim AE on all respective platforms.