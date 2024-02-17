---
title: "Skyrim Versions"
weight:
type: docs
description: >
  About the various versions of Skyrim and the differences between them.
---

Skyrim has been updated and re-released many times on many platforms since its initial launch in 2011. Significant differences exists between the available versions which affect modding.

## Skyrim LE / Skyrim SE

There are two 'main' versions of Skyrim:

- **Skyrim Legendary Edition (SLE)** is the version originally released in 2011 and packaged with its three DLC (Dawnguard, Hearthfire, Dragonborn).
- **Skyrim Special Edition (SSE)** is a remaster released in 2016, also packaged with all DLC. One of its core features was a major engine upgrade.

The original Skyrim ran on a 32bit version of the *Creation Engine* which limited the game to 4GB of RAM and generally made it more difficult to build a stable, modded setup.

Skyrim SE was given the 64bit engine upgrade originally built for *Fallout 4* which improved various rendering techniques for visual improvements but also increased stability. It is generally easier to mod Skyrim SE. However, certain kinds of SLE mod require to be **ported** before they work properly in SSE and it took several years for the modding community to fully move on to the new version.

Nowadays, most mods are being developed and released for SSE exclusively. The only reason to choose SLE over SSE is performance as it will run better on extremely low-end systems.

### Creation Club

The Creation Club was one of the main selling points for the Skyrim SE release. It is effectively a microtransaction store selling mini-DLC, some created by Bethesda developers, others by popular modders hired by Bethesda.

For more details, see [Creation Club](/skyforge/knowledge-base/creation-club/).

### Skyrim AE

Skyrim Anniversary Edition (SAE) was released in 2021 and is often described as a third version of the game, after SLE and SSE. This is fundamentally incorrect. **Skyrim AE has no meaningful technical differences from SSE** and is simply packaged with all Creation Club content. It is, in effect, a regular SSE update with some additional content.

{{< alert color="warning" >}} With the exception of mods that always need to be updated when the game updates (i.e., SKSE and SKSE plugins), mods do not need to be ported from SSE to SAE.{{< /alert >}}

### Storefronts

Skyrim SE is available from multiple sources:

- Steam
- GOG
- XBOX Game Pass

SKSE is available for the **Steam** and **GOG** versions, but <u>not</u> for the **Game Pass** version. However, because there is a separate version of SKSE, not all mods with SKSE plugins offer compatibility for the GOG version of Skyrim SE.

**The Steam version of Skyrim SE is the best option for modding.**

## Consoles

The original Skyrim LE was also ported to **PlayStation 3** and **XBOX 360**. These console versions were not moddable.

Skyrim SE was released for the next generation of consoles, **PlayStation 4** and **XBOX One** in 2016 with a major difference being that on these platforms modding was made possible through the Bethesda.net infrastructure.

Skyrim SE (as part of the Anniversary Edition) was ported to **PlayStation 5** and **XBOX Series X/S** in 2021 and is moddable in the same way as in the previous generation.

Skyrim SE was also ported to the **Nintendo Switch** in 2017. Modding is possible in a limited fashion if custom firmware has been installed on the device which carries its own risks.

Skyrim SE can be modded on a **Steam Deck**; however, there are some limitation due to the Deck running on Linux.

{{< alert >}} While technically possible, <u>modding on PlayStation and XBOX is not comparable to modding on PC</u> due to the hard limit on space and the lack of access to the root folder which makes it impossible to use advanced mods/tools like SKSE and ENB.{{< /alert >}}

## VR

A VR version of Skyrim was released for Windows and PlayStation VR. Though based on Skyrim SE, it has various technical differences, requires its own version of SKSE, and is not always compatible with Skyrim SE mods.