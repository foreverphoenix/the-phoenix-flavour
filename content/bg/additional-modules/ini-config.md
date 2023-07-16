---
title: "INI Configuration"
weight:
type: docs
description: >
  How to modify the vanilla INI files with BethINI.
---

{{< alert color="info" title="Summary" >}}
> This module covers recommended tweaks for the vanilla INI files made through BethINI.<p>
> **Prerequisite(s):** [BethINI](/bg/tool-setup/bethini){{< /alert >}}

## Modifying the INI Files

To learn more about the default INI files and their contents, please consult the [INI Files](/bg/knowledge-base/ini-files/) article. It also covers how to use <u>profile-specific INI files</u> in Mod Organizer 2 which I highly recommend.

You can modify the INI files manually (through MO2 or a text editor) though this requires a decent bit of knowledge on what the settings do, especially in terms of their performance impact.

Instead, I recommend using the [BethINI](/bg/tool-setup/bethini/) tool to modify the default set to at least apply one of its optimised presets instead of the vanilla preset.

## BethINI

Before running BethINI, make sure that Mod Organizer 2 is <u>closed</u>.

- Run **BethINI.exe**.
- Choose **Skyrim Special Edition** as the game.

### BethINI: Setup

> Switch to the **Setup** tab.

- **Game:** Should have *Skyrim Special Edition* selected.
- **Game Path:** Should point to the default installation folder:
  - `\Steam\steamapps\common\Skyrim Special Edition\`
- **Mod Organizer 2:** Should point to your Mod Organizer 2 instance.
- **INI Path:** Should point to your Documents folder <u>or</u> your MO2 profile if using profile-specific INI files.
  - *BethINI will restart if you change the INI Path.*

{{< alert color="warning" >}}If BethINI asks about modifying the **SkyrimCustom.ini**, I recommend clicking **No**. I personally do not find it more convenient to outsource, as it were, some settings to the Custom INI. Of course, your mileage may vary.{{< /alert >}}

![BethINI Setup](/Pictures/bg/additional-modules/ini-config/bethini-setup.png)

### BethINI: Basic

> Switch to the **Basic** tab.

- **Resolution:** Set to match your monitor's resolution.
  - *Read more about resolutions, performance, and widescreen support [here](/bg/knowledge-base/resolution/).*
- Check **Recommended Tweaks** and make sure **BethINI Tweaks** are toggled on.
- Select either the **Low**, **Medium**, or **High** preset.

Which preset you should select obviously depends on your hardware and monitor resolution.

Unless you are quite confident in your hardware, I would always recommend selecting the **Medium** preset as a baseline. Many of the most performance-intense settings can still be toggled and modified individually.

- **Windowed Mode** and **Borderless** as well as any settings relating to VSync and framerate can be left untouched as [SSE Display Tweaks](/bg/recommended-mods/essential-mods/#sse-display-tweaks) should override them.
- **Antialiasing:** FXAA is an older antialiasing technique that performs better than TAA but causes some blurriness. I recommend leaving FXAA off and enabling TAA as most PCs should be more than able to run it.
- **64-Bit Render Targets** is required to be enabled for certain ENB presets to look as intended but comes at a noticeable performance cost. You can disable it for now and re-enable it later if you end up installing an ENB preset that requires it.

![BethINI Basic](/Pictures/bg/additional-modules/ini-config/bethini-basic.png)

### BethINI: General

> Switch to the **General** tab.

There is nothing that I recommend modifying in this tab.

I want to especially emphasize that you should leave the Papyrus settings <u>untouched</u>. Since the Skyrim LE, a number of Papyrus tweaks have been floating around that were never more than placebo at best and actively harmful at worst.

### BethINI: Gameplay

> Switch to the **Gameplay** tab.

Once again, I do not recommend making changes here.

- **NPCs Use Ammo** sounds like a great option on paper, but does not work well in practice. In vanilla, archer NPCs spawn with a few arrows in their inventory which are not actually depleted as they fire them. Enabling this INI setting would cause them to rapidly burn through their arrows, then rendering them useless in combat.

### BethINI: Interface

> Switch to the **Interface** tab.

- **Subtitles** can be toggled here or ingame.
- **Bethesda Modding Platform** should be <u>enabled</u>.
  - *You can use [QUI](/bg/recommended-mods/utilities-frameworks/#qui) to disable the menu options as they should not be used.*
- **Mod Manager Menu** should be <u>disabled</u>.
- **Lock Sensitivity** is best configured ingame where you can immediately test your settings.

### BethINI: Detail

> Switch to the **Detail** tab.

- **Water:** I recommend also checking *Reflect Objects* when on the Medium preset.
- **Particles** should be set to <mark>2000</mark>, or <mark>7500</mark> if using an ENB.
- **Depth of Field** should remain toggled, even if you do not intend to use it because disabling it breaks underwater visuals. You can turn it down all the way ingame instead.
- **Lens Flare** and **Anamorphic Lens Flare** do not look particularly good and should be disabled.
  - *Always disable them when using ENB.*
- **Shadow Resolution** should be set to <mark>2048</mark>, unless severely CPU-bottlenecked.
- **Ambient Occlusion** has a noticeable performance impact but adds a great deal of depth and should be enabled <u>except</u> when using ENB which has its own, more advanced form of AO.

![BethINI Detail](/Pictures/bg/additional-modules/ini-config/bethini-detail.png)

### BethINI: View Distance

> Switch to the **View Distance** tab.

- **Grass Fade** distance can be increased to <mark>10000</mark> or higher with a relatively low performance cost.
- **Level 16:** Set to at least <mark>248705</mark> to prevent distant mountain peaks from looking completely white.

### BethINI: Visuals

> Switch to the **Visuals** tab.

- **Grass** settings (density, diversity) should be left untouched here as grass overhauls tend to come with plugin INIs which modify these settings to work well with the rest of the mod.
- **Projected UV Diffuse Normals** should always be left <u>enabled</u> for consistent snow coverage.
  - *This requires a matching projecteddiffuse.dds texture for your snow01.dds texture.*
- **Improved Shader** (for snow) should always be left <u>disabled</u>.

### BethINI: Finalisation

When you are happy with your changes, return to the **Basic** tab and click **Save and Exit**.

You can always re-run BethINI to modify the settings.