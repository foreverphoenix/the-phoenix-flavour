---
title: "Mod Configuration Menus"
weight:
type: docs
description: >
  About Mod Configuration Menus (MCMs).
---

## About Mod Configuration Menus

This article summarises some basic knowledge about **Mod Configuration Menus** (MCM).

The Mod Configuration Menu is a new settings menu accessible from the ESCAPE menu for customising mods, replacing older customisation methods like powers, spells, or books. The framework for MCMs is added by [SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/12604) which in turn requires the [Skyrim Script Extender](/bg/additional-modules/skyrim-script-extender/).

## Saving MCM Settings

For every new save, Mod Configuration Menus will be rolled back to the default settings which can be inconvenient, especially during testing. Reconfiguring two dozen MCMs for every `coc riverwood` can be a lot of work.

Fortunately, MCM settings can be maintained across saves in multiple ways:

1. By saving presets using FISS, JContainers, PapyrusUtil, or MCM Helper.
2. By using a Settings Loader mod.
3. By modifying the MCM directly in the script or plugin.

### Saving Presets

Some older mods explicitly come with a preset feature powered by either [FileAccess Interface for Skyrim SE Scripts (FISSES)](https://www.nexusmods.com/skyrimspecialedition/mods/13956), [PapyrusUtil](https://www.nexusmods.com/skyrimspecialedition/mods/13048), or [JContainers](https://www.nexusmods.com/skyrimspecialedition/mods/16495).

{{< alert color="danger" >}}**Note that FISSES has been known to cause crashes and should no longer be used.** It has been fully replaced by PapyrusUtil and MCM Helper.{{< /alert >}}

The best option today for MCM presets is [MCM Helper](https://www.nexusmods.com/skyrimspecialedition/mods/53000) which (among other features) saves MCM changes in readable INI files which can easily be saved as presets.

[MaskedRPGFan](https://www.nexusmods.com/skyrimspecialedition/users/22822094?tab=user+files) has created **Settings Loader** mods for various mods with MCMs which add support for either PapyrusUtil or MCM Helper for easy automation.

Alternatively, you can also modify MCMs directly through either plugin or script (see below).

### Managing Presets

After installing a Settings Loader mod or any mod with MCM Helper support, you need to go ingame, configure the MCM as desired, and quit. The preset file will be in the ***Overwrite***.

From here, I strongly recommend keeping the file in its own folder as opposed to dropping it into the original mod's folder. This way you can avoid having to reconfigure the MCM every time the mod is updated.

### Automating MCMs

An alternative to using MCM Helper presets is automating MCMs by modifying them directly. This is not done as much since MCM Helper is more widely supported, but it can be still be a convenient way of permanently changing default settings in MCMs.

{{< alert color="info" >}}See the [Automating MCMs](/bg/additional-modules/automatic-mcms/) page for instructions on how modify MCMs directly.{{< /alert >}}