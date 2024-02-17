---
title: "Porting SLE Mods"
weight:
type: docs
description: >
  About the porting process for various file types.
---

## Differences by File Type

Not all mods made for Skyrim LE will work out-of-the-box in Skyrim SE. A fair amount of them will need porting.

{{< alert color="warning" >}}A mod being available on the Skyrim SE Nexus does not automatically mean it was ported properly (or at all).{{< /alert >}}

- **Plugins:** Must always be ported using the CK. Occasionally require manual updates.
- **Archives:** Must always be unpacked or they will crash the game. Can be repacked afterwards.
- **SKSE Plugins:** Must always be ported for the newest version of SKSE.
- **Meshes:** Should be processed with SSE NIF Optimizer / Cathedral Assets Optimizer (though not always necessary).
- **Textures:** Some older formats must be changed to avoid crashes. Compression recommended.
- **Animations:** Should be processed with Cathedral Assets Optimizer.
- **Scripts:** No porting steps required.

### Plugins

Plugins created for Skyrim LE must always be ported. This requires the [Creation Kit](/skyforge/tool-setup/creation-kit/) and sometimes [SSEEdit](/skyforge/tool-setup/sseedit/) for additional steps.

Check the [Porting SLE Plugins](/skyforge/modding-resources/porting-sle-plugins/) page for instructions.

### Archives

Archives (BSAs) created for Skyrim LE must always be extracted. They will otherwise crash Skyrim SE on launch.

Please consult the article on [Extracting BSAs](/skyforge/modding-resources/extracting-bsas/) for instructions.

### Textures

Textures created for Skyrim LE sometimes need to be compressed or changed to a different format for Skyrim SE.

Since Skyrim SE, the engine supports the **BC7 compression format** which combines the small file size of a compressed texture while retaining nearly the same quality as an uncompressed texture of an older format. Textures for Skyrim LE were sometimes left uncompressed for better visual quality, but should be compressed to BC7 for use in Skyrim SE.

{{< alert color="warning" >}}Only <u>uncompressed</u> textures can be compressed to BC7. If a texture is already formatted as a DXT5/BC3, recompressing it to BC7 will not improve the quality or save any more space.{{< /alert >}}

Textures can be processed with CAO for optimisation. Instructions can be found [here](/skyforge/modding-resources/optimising-sle-assets/).

### Meshes

Meshes created for Skyrim LE often need to be optimised for Skyrim SE. They may crash the game or cause visual issues otherwise.

You can use either [Cathedral Assets Optimizer](/skyforge/tool-setup/cao/) or [SSE NIF Optimizer](/skyforge/tool-setup/sse-nif-optimizer/) for optimising meshes. CAO includes NIFOpt though the latter still has some useful additional options that cannot be accessed through CAO (e.g., more detailed logs and removal of parallax).

Instructions for processing with CAO can be found [here](/skyforge/modding-resources/optimising-sle-assets/).

### Animations

Animations created for Skyrim LE need to be optimised for Skyrim SE.

Animations can be processed with CAO for optimisation. Instructions can be found [here](/skyforge/modding-resources/optimising-sle-assets/).

{{< alert color="warning" >}}You cannot port FNIS animations this way, only vanilla replacers.{{< /alert >}}