---
title: "Essential Mods"
weight: 3
type: docs
description: >
  Mod recommendations.
---

##### [SSE Display Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/34705)

{{< alert color="success" >}}**Essential.** Everyone should install this mod.{{< /alert >}}

SSE Display Tweaks is huge package that contains a variety of display- and performance-related options, including its very own on-screen display (OSD) for tracking hardware usage ingame.

The mod also enables the game to run (mostly) without issues at a framerate exceeding 60FPS. <u>In vanilla, the physics engine is tied directly to the framerate.</u> When unlocking it and going above 60FPS, the game would increasingly bug out to the point where it would become completely unplayable. SSE Display Tweaks (mostly) fixes that*.

<font size=2>\**It should be noted that some minor bugs may still occur with increasing frequency at higher frame-rates. These include small physics bugs, such as objects moving for no reason or "spazzing out", or creatures falling out of the sky. However, there should be no more game-breaking issues.*</font>

I generally recommend using SSE Display Tweaks for all monitor-related settings (as opposed to the vanilla INI files).

**Requirements:** Skyrim Script Extender, Address Library for SKSE

#### Settings File

SSE Display Tweaks can be configured via its **SSEDisplayTweaks.ini** which can be overwritten with a custom file. This is usually preferable as changes will not be lost when updating the main mod.

- [Create a new empty mod](/Pictures/bg/create-empty-mod.png) in Mod Organizer 2 and name it **SSE Display Tweaks - Settings**.
- Right-click the new mod and select **Open in Explorer**.
- Create the following folder structure: `\Mod Organzier 2\mods\SSE Display Tweaks - Settings\SKSE\Plugins\`.
- Inside the **Plugins** folder, right-click, and select **New** >> **Text Document**.
- Name the file **SSEDisplayTweaks_Custom.ini**. <u>Remember to change the file extension.</u>

You can now copy any settings from the default **SSEDisplayTweaks.ini** into the **SSEDisplayTweaks_Custom.ini** and customise them there.

#### Monitor Configuration

For Windows 10 users, I recommend forcing Borderless Fullscreen so you are able to benefit from the DXGI flip model integration for better performance. Add the following to your **SSEDisplayTweaks_Custom.ini**:

```
[Render]
Fullscreen=false
Borderless=true
```

#### Screen Resolution

I also recommend using SSE Display Tweaks to set your resolution. A widescreen resolution is possible though you will need to install patches for UI mods.

Add the following line to your custom INI in the [Render] section and fill in your monitor resolution (1920x1080, 2560x1440, etc):

```
Resolution=
```

#### Downscaling

Skyrim does not scale well at higher resolutions and a quick performance boost can be gained by downscaling the game to a resolution lower than the monitor's native resolution. This does noticeably impact visual fidelty, however.

You can read more about monitor resolutions and performance [here](/bg/knowledge-base/resolution/).

To downscale set your desired resolution (see above) and add the following line:

```
BorderlessUpscale=true
```

#### Framerate Cap

As noted earlier, you can safely increase the framerate limit beyond 60FPS with SSE Display Tweaks installed. By default, the limit is 240FPS. You should, however, be aware that achieving a framerate above 100FPS with a decently modded game requires very good hardware, especially on resolutions above 1080p.

I personally cap at 60FPS regardless as that is enough for me. A good compromise could be 72FPS or 90FPS.

If you would like to change the framerate cap, you can do so in the **SSEDisplayTweaks_custom.ini** as well by adding the following to the [Render] section with \<framerate> being the value you want to cap at:

```
FramerateLimit=<framerate>
```

##### [SSE Engine Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/17230)

{{< alert color="success" >}}**Essential.** Everyone should install this mod.{{< /alert >}}

SSE Engine Fixes is a collection of engine-level fixes.

**Requirements:** Skyrim Script Extender, Address Library for SKSE

#### SKSE Preloader

SSE Engine Fixes requires the SKSE Preloader to be installed first. It is a root folder file available from the same mod page.

- Download the **(Part 2) Engine Fixes - skse64 Preloader and TBB Lib** main file.

If you are using [Root Builder](/bg/additional-modules/root-builder/), follow the instructions below. Otherwise, simply extract the files into your root folder.

- [Create a new empty mod](/Pictures/bg/create-empty-mod.png) in Mod Organizer 2 and name it **SKSE Preloader**.
- Right-click the new mod and select **Open in Explorer**.
- Create a new **Root** folder inside the mod folder.
- Extract the downloaded archive into the **Root** folder.
- Refresh Mod Organizer 2 with F5 and activate the new mod.
- Right-click it and select **Ignore missing data**.

I usually place the SKSE Preloader as the last mod below my **Skyrim Script Extender** separator.

{{< alert color="warning" >}}If you previously installed [SSE Creation Kit Fixes](/bg/tool-setup/creation-kit/#creation-kit-fixes), it will conflict with the SKSE Preloader because both contain tbb.dll and tbbmalloc.dll (my Google-Fu tells me these are Intel libraries). A [comparison](/Pictures/bg/recommended-mods/essential-mods/tbb-comparison.png) reveals that the SKSE Preloader appears to include a newer version of those libraries which is why I let it overwrite.{{< /alert >}}