---
title: "Interface"
weight: 1
type: docs
description: >
  Additional interface mods.
---

## Basic Mods

These are mods that I don't consider good fits for base TPF but that I still use personally.

### **[moreHUD Inventory Edition](https://www.nexusmods.com/skyrimspecialedition/mods/18619?tab=files)**

This mod adds more information to the SkyUI inventory. It also fixes item cards.

This mod is **optional**.

#### Download Instructions

- **Main Files:** moreHUD Inventory Edition Loose Version

### **[Main Menu Design Replacer](https://www.nexusmods.com/skyrimspecialedition/mods/30810?tab=files)**

This mod centers the main menu design, a change I'm personally rather fond of. It also looks very decent with TPF's standard main menu replacer.

This mod is **optional**.

#### Download Instructions

- **Main Files:** Main Menu Design Replacer (clean)

### **[Time Format Change](https://www.nexusmods.com/skyrimspecialedition/mods/28921?tab=files)**

As a European, I've always hated the 12h format of Skyrim's clock so here's a fix. Feel free to select whatever you want in the FOMOD, or skip this mod entirely.

This mod is **optional**.

#### Download Instructions

- **Main Files:** Time Format Changer - FOMOD Installer

## QuickLoot

QuickLoot implements a Fallout-4-style overlay that allows you to loot dead bodies or containers without having to go into the full menu. It is rather divisive which is why it is now **optional**. If you don't like QuickLoot, you can **skip it**.

### **[QuickLoot](https://www.nexusmods.com/skyrimspecialedition/mods/21085?tab=files)**

The main mod. If you decide to skip this, skip all mods in the QuickLoot section.

#### Download Instructions

- **Main Files:** QuickLootRE

### **[No Lockpick Activate (SKSE) - Updated](https://www.nexusmods.com/skyrimspecialedition/mods/26790?tab=files)**

While not originally intended as such, this mod is an addon of sorts to **QuickLoot**. Without it, you would be forced into the full menu upon unlocking a container even when QuickLoot is installed. With the mod, you will be able to see the QuickLoot overlay and loot through there. It does, however, also affect every other locked object so for example you have to interact with doors after unlocking them to go through.

Install this mod if you installed QuickLoot. Otherwise skip it.

#### Download Instructions

- **Main Files:** No Lockpick Activate (SKSE) - Updated

### **[QuickLootRE Texture Replacer](https://www.nexusmods.com/skyrimspecialedition/mods/39045?tab=files)**

The default QuickLoot design can be a little heavy 

#### Download Instructions

- **Main Files:** QuickLootRE Texture Replacer

#### FOMOD Instructions

- **Options:** Dialogue Style

## Font Replacer

Swapping out the font mod is one of the easiest changes possible. I am personally partial to Roboto which is my go to font for Skyrim but in memory of the good old days (way back in 2015), I also recommend Fertigo Pro as an alternative which was then my standard font replacer. However, you can essentially install any font replacer you like. If you decide to install a different font replacer, I would suggest editing the `fontconfig.txt` to continue using the Consolas font in the console.

This section is completely **optional**.

### **[Roboto Font Replacer](https://www.nexusmods.com/skyrimspecialedition/mods/1779?tab=files)**

Roboto is my favourite font replacer because it just fits the vanilla UI's modern aesthetic so well. It was the default for TPF for a long time until I ultimately relented and swapped it with the far more popular Sovngarde font replacer.

#### Download Instructions

- **Main Files:** Roboto Main Font Replacer

#### Additional Instructions

- Double-click **Roboto Font Replacer** in your mod order.
- Switch to the **Text Files** tab and select the **fontconfig.txt** file.
- Create a new line below `fontlib "Interface\fonts_en6.swf"`.
- Paste `fontlib "Interface\fonts_consolas.swf"` into the new **Line 4**.
- In **Line 5**, change `"Arial"` to `"Consolas"`.
- Close the window and click **Yes** when asked to save.

> This way we can use Roboto for dialogue, menus, etc and Dear Diary's Consolas font (packaged with Dear Diary - Better More Informative Console installed in the Essential Mods section) for the console.

![Roboto Console Font](/Pictures/tpf/mod-installation/roboto-console-font.png)

### **[Main Font Replacement - Fertigo Pro](https://www.nexusmods.com/skyrimspecialedition/mods/14356?tab=files)**

This was my first font mod of choice back in the day before Sovngarde was released. It was rather popular then and continues to hold up well as a compromise between simple and stylised.

#### Download Instructions

- **Main Files:** Fertigo Pro Font SSE

#### Additional Instructions

- Double-click **Main Font Replacement - Fertigo Pro** in your mod order.
- Switch to the **Text Files** tab and select the **fontconfig.txt** file.
- Create a new line below `fontlib "Interface\fonts_en2.swf"`.
- Paste `fontlib "Interface\fonts_consolas.swf"` into the new **Line 4**.
- In **Line 5**, change `"Arial"` to `"Consolas"`.
- Close the window and click **Yes** when asked to save.

> This way you can use Fertigo Pro for most of the game with Dear Diary's Consolas font for the console.

![Fertigo Consolas](/Pictures/tpf-x/installation/fertigo-consolas.png)