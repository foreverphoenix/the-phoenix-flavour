---
title: "Automating MCMs"
weight:
type: docs
description: >
  How to automate MCMs (changing default settings).
---

{{< alert color="info" title="Summary" >}}
> This module covers how to change the default settings in a Mod Configuration Menu to avoid having to reconfigure them in every new save.<p>
> **Prerequisite(s):** [Mod Organizer 2](/bg/tool-setup/mo2/), [Creation Kit](/bg/tool-setup/creation-kit/), [SkyUI and Source 5.1 + 5.2](/bg/recommended-mods/skyui/){{< /alert >}}

## Automating MCMs

In the following, I will explain how to modify a mod directly to change its default MCM options using the example of [Realistic Water Two](https://www.nexusmods.com/skyrimspecialedition/mods/2182) (RW2).

The mod has several option features which can be toggled in the MCM, including *ripples* and *waves*. When I am using [GKB Waves Reborn](https://www.nexusmods.com/skyrimspecialedition/mods/71126), the RW2 waves features can be disable. When I am <u>not</u> using [Splashes of Storms](https://www.nexusmods.com/skyrimspecialedition/mods/72115), I might as well enable RW2's ripples on water.

## Modifying Globals

MCMs consist of a quest (defined in a plugin) and a script which can be linked to other records, such as *globals* or *references*. If a setting is controlled via a global, it is very easy to modify in the plugin:

![RW2 Change Global](/Pictures/bg/additional-modules/automating-mcms/change-global.png)

With the **Realistic Water Two - MCM Preset.esp** plugin loaded, the *ripples* feature will now be *enabled* by default in the RW2 MCM.

## Modifying Script Source

Scripts can only be modified in their source files which must be recompiled in the Creation Kit. Fortunately, **Realistic Water Two** and many other mods containing scripts ship with the source files included (or they are available for download as optional files).

### Editing Source Files

As usual, I recommend creating *copies* as opposed to modifying a mod directly.

- Create a new folder under `\Mod Organizer 2\mods\` and name it **Realistic Water Two - MCM Settings**.
- Inside, create the `\Scripts\Source\` folder structure.
- Copy the `\Source\Scripts\RealisticWaterTwoMCM.psc` from RW2 into the new **Source** folder.

Open the new copy of **RealisticWaterTwoMCM.psc** in a text editor such as Notepad++ (I recommend setting the app as the default for .PSC files).

- Scroll down to **Line 40** and change the following:

```
bool SkyrimWaves = false
```

- Save your change and close the file.

After recompiling the script, the *waves* feature will be disabled by default.

### SkyUI Source

When recompiling an MCM script, you need to have the SkyUI source files that were used when the MCM was originally made. This may be 5.2, 5.1, or an even older version. Generally, I would try 5.2 first. If the version is wrong, the Creation Kit log will complain about it:

![Wrong SkyUI Source](/Pictures/bg/additional-modules/automating-mcms/wrong-skyui-source.png)

### Recompiling Script

Before you recompile the script, check the following:

1. The **Creation Kit - Source** should be <u>enabled</u>.
2. The **SkyUI - Source** file set should be <u>enabled</u> (5.1 for RW2).
3. The mod you are recompiling the script for should be <u>disabled</u>.

{{< alert color="info" >}}The third step ensures that the Creation Kit creates a new copy of the script instead of overwriting the original.{{< /alert >}}

- Run the **Creation Kit** through Mod Organizer 2.
- Go to **Gameplay** >> **Compile Papyrus Script**.

![CK Compile Script](/Pictures/bg/additional-modules/automating-mcms/ck-compile-script.png)

You will be greeted by a window with a list of all present script source files.

- Press **R** to quickly jump to scripts starting with that letter.
- Check the **RealisticWaterTwoMCM.psc** and click **Compile**.

![Compile RW2 Script](/Pictures/bg/additional-modules/automating-mcms/compile-rw2-script.png)

The window will auto-close if the script was compiled successfully. Also check the [log window](/Pictures/bg/additional-modules/automating-mcms/script-no-errors.png) which should not contain any errors.

Close the Creation Kit.

## Finalisation

Any new plugins and/or recompiled scripts will be caught by Mod Organizer 2 in the ***Overwrite***. Create [a new mod](/Pictures/bg/additional-modules/automating-mcms/rw2-mcm-preset.png) to store the file(s). Place it below the original mod and activate it.

Remember to disable the CK and SkyUI source files unless you have other MCM scripts to recompile.