---
title: "Resolution"
weight:
type: docs
description: >
  About monitor resolutions (performance, interface, textures).
---

## Resolution

Monitors display images by rendering millions of tiny square pixels. Rendering more pixels increases image sharpness but requires more hardware power.

Pixels are arranged on most modern consumer monitors in a 16:9 ratio with other ratios, such as 16:10, 21:9, or 32:9, being quite rare. 5:4 and 4:3 ratios are essentially deprecated.

Common **16:9** resolutions include 1920x1080, 2560x1440, and 3440x2160. They may be abbreviated as 1080p, 1440p, and 2160p, respectively.

Common **21:9** or **widescreen** resolutions include 2560x1080 and 3440x1440.

{{< alert color="info" >}}The 3440x2160 pixels resolution is also commonly referred to as 4K which is currently the largest resolution used in gaming (with 8K still being very rare).{{< /alert >}}

### Performance

Skyrim is known to scale badly at higher resolutions, especially when heavily modded. Running the game with overhauled graphics and an ENB preset at 1440p or higher resolutions requires high end hardware to run at a stable 60FPS.

An easy boost to performance at the cost of sharpness is gained by running the game at a resolution that is *lower* than the monitor's native resolution. For example, if performance is very low on a 2160p monitor, you can try downscaling to 1440p. This can be done with [SSE Display Tweaks](/bg/recommended-mods/essential-mods/#sse-display-tweaks).

{{< alert color="info" >}}Downscaling will noticeably affect visual fidelity and other measures of performance optimisation should be taken first. When downscaling, you can counter the blurriness by using ENB or ReShade to add sharpening.{{< /alert >}}

### Interface

The vanilla interface and nearly all interface mods are made for the standard 16:9 ratio and will be cut off or misaligned on monitors with other ratios.

The [Complete Widescreen Fix](https://www.nexusmods.com/skyrimspecialedition/mods/1778) mod page offers patches for vanilla, SkyUI, and a variety of mods. Other interface mods may offer widescreen patches separately. These are largely for 21:9 monitors.

### Textures

There is a common misconception that 4K textures (with a resolution of 4096x4096 pixels) are unnecessary on non-4K monitors. **This is false.**

If you view a 4096x4096 pixels *flat image* on a 1440p screen you will indeed be unable to display all pixels at the same time. However, textures are not used as flat images in the game; they are wrapped around 3D objects called meshes.

Looking at a large mesh (like a part of a mountain) you only see a *portion* of the texture that is applied to it. Depending on the size of the object and how closely you approach it, even a 4K texture can start to appear blurry on a 1080p monitor because you are zooming in on a very small part of it.

{{< alert color="warning" >}}4K textures on a 1080p or 1440p monitor are very much noticeable on large objects and not at all redundant.{{< /alert >}}