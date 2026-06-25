---
title: "Prerequisites"
weight: 1
type: docs
description: >
  In this (short) step we will go over the basic requirements, the version of Skyrim you need for TPF, enabling file extensions in Window Explorer, and, optionally, how to properly calibrate your monitor.
---

## Requirements

First up, we have some general requirements. You need:

- A legit Windows 10 or 11 installation (64bit).*
- Editing software such as [Notepad++](https://notepad-plus-plus.org/).
- An archiving tool like [7zip](https://www.7-zip.org/download.html).
- Latest drivers for your GPU ([NVIDIA](https://www.nvidia.de/Download/index.aspx), [AMD](https://www.amd.com/en/support), or [Intel](https://www.intel.com/content/www/us/en/search.html#sortCriteria=@lastmodifieddt%20descending&cf-tabfilter=Downloads&cf-downloadsppth=Graphics)).

<font size=2>\* While modding on Linux (PC or SteamDeck) is technically possible, I have never done it and so I cannot provide support for it.</font size>

In terms of soft skills, some tech literacy is inevitably required. You need to know how to create new files and folders, handle archived files, and install programmes.

Finally, the most important prerequisite -- and the one most often ignored -- is <mark>the willingness to read</mark>. Thirty seconds saved by skimming can easily turn into thirty minutes of tedious troubleshooting. Remember to take regular breaks!

### Nexus Accounts

We will source the vast majority of our mods and tools from [Nexus Mods](https://www.nexusmods.com/). In order to download mods from the Nexus, you need an account.

- If you do not have a Nexus account yet, go ahead and [create one now](https://users.nexusmods.com/register).

{{< alert color="info" >}}The Nexus also offers [Premium subscription](https://www.nexusmods.com/premium) which, among other things, removes ads and uncaps download speeds. While Premium is not required for TPF, it will save you some time in the *Mod Installation* section.{{< /alert >}}

### Skyrim Version

TPF was written for the [Steam version](https://store.steampowered.com/app/489830/The_Elder_Scrolls_V_Skyrim_Special_Edition/) of **Skyrim Special Edition**. This version is <u>required</u> for following the guide.*

<font size=2>\* Support for the GOG version may be added at a later date.</font size>

{{< alert color="info" >}}To learn more about the different versions of Skyrim and their suitability for modding, [read this article](/manual/resources/skyrim-versions/).{{< /alert >}}

The [Anniversary Edition DLC](https://store.steampowered.com/app/1746860/The_Elder_Scrolls_V_Skyrim_Anniversary_Upgrade/) (or all creations bought separately) is also <u>required</u>. Content from the CCs is too deeply integrated in TPF to make this optional.

## Show File Extensions

Make sure that file name extensions are set to visible in Windows Explorer. This will enable you to tell apart files by their extensions.

- <mark>**Windows 10:**</mark> In the **View** tab/ribbon, make sure **File name extensions** is checked  ([screenshot](/Pictures/manual/setup/prerequisites/show-file-extensions-win10.png)).
- <mark>**Windows 11:**</mark> Go to **View** > **Show** and make sure **File name extensions** is checked ([screenshot](/Pictures/manual/setup/prerequisites/show-file-extensions-win11.png)).

## Monitor Calibration (*)

Correct monitor calibration can improve colour balance and brightness, ensuring that Skyrim (and any other game) looks as intended. 

{{< alert color="warning" >}}Your monitor should have been running for at least 30 minutes before you adjust it.{{< /alert >}}

Many monitors can be adjusted directly via a button and an in-built menu. You should be able to find instructions by looking up the model on Google.

You can also adjust monitor settings through software:

- **Windows:** Control Panel > Colour Management > Advanced > Calibrate display
- **NVIDIA:** Control Panel > NVIDIA Control Panel > Adjust Desktop Color Settings
- **AMD:** *Unfortunately, I never owned an AMD GPU so I cannot give advice here.*

To help you find the sweet spot for your monitor, check out these resources:

- [CLF ENB - monitor calibration help](https://i.imgur.com/k1v8p1M.png)
- [Photo Friday Monitor Calibration Tool](https://www.photofriday.com/info/calibrate)
- [Lagom: LCD monitor test images](http://www.lagom.nl/lcd-test/)

### Dynamic Range

It is recommended that you set monitor's **Dynamic Range** to "Full" if it is connected to your PC via DisplayPort or HDMI. Instructions for NVIDIA- and AMD-based systems can be found [here](https://pcmonitors.info/articles/correcting-hdmi-colour-on-nvidia-and-amd-gpus/).

---

<font size=4>Continue with [Clean Install](/manual/setup/clean-install/).</font size>