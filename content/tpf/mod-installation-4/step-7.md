---
title: "Step 7: Animations & Camera"
weight: 7
type: docs
description: >
  Skeleton replacer, new animations, and camera improvements.
---

##### [Project New Reign - Nemesis Ultimate Behaviour Engine](https://www.nexusmods.com/skyrimspecialedition/mods/60033?tab=files)

#### Download Instructions:

- **Main Files:** Nemesis Unlimited Behavior Engine

> The mod is not properly installed until after running the included executable. This will be done in the Finalisation section of the guide.

##### [XP32 Maximum Skeleton Special Extended (XPMSSE)](https://www.nexusmods.com/skyrimspecialedition/mods/1988?tab=files)

#### Download Instructions

* **Main Files:** XP32 Maximum Skeleton Special Extended

#### FOMOD Instructions

- **Animation Rig Map:** No Physics
- **Character Creation:** None
- **First Person Animation - Ax:** ~~Axes on Back~~
- **First Person Animation - Sword** None
- **Mounted Combat Animation - Axe:** ~~Axes on Back~~
- **Mounted Combat Animation - Bow:** ~~Belt-Fastened Quiver~~
- **Mounted Combat Animation - Sword:** None
- **The Joy of Perspective:** None
- **Schlongs of Skyrim:** None >> `defaults to SOS, set to None`
- **Deadly Mutilation:** None

> The reason we are not installing the "full" XPMSSE is because it causes significant save bloat over time, continuously increasing the size of the SKSE co-saves and causing the game to freeze for several seconds when creating a new save.

##### [True Directional Movement - Modernized Third Person Gameplay](https://www.nexusmods.com/skyrimspecialedition/mods/51614?tab=files)

#### Download Instructions

- **Main Files:** True Directional Movement

##### [True Directional Movement - Tail Animation Fix](https://www.nexusmods.com/skyrimspecialedition/mods/53757?tab=files)

#### Download Instructions

- **Main Files:** TDM - Tail Behavior Fix

##### [Simple Dual Sheath](https://www.nexusmods.com/skyrimspecialedition/mods/50049?tab=files)

#### Download Instructions

- **Main Files:** Simple Dual Sheath
- **Optional Files:** XPMSSE Left Hand Sheathe Rotation Fix

#### Additional Instructions

- Double-click **Simple Dual Sheath** in your mod order.
- Switch to the **INI Files** tab and select the **SimpleDualSheath.ini**.
- In **Line 23** add the following flags: `Flags=Player|NPC|FirstPerson`.
- In **Line 29** set `ClenchedHandWorkaround=` to `true`.
- In **Line 38** add the following flags: `DisableHideOnSit=Player|NPC|MountOnly`.
- Press **CTRL+S** to save and close the window.

> The "FirstPerson" flag for ShieldsOnBack prevents the shield from appearing in first person view when it is "sheathed".

##### [Dynamic Animation Replacer](https://www.nexusmods.com/skyrimspecialedition/mods/33746?tab=files)

#### Download Instructions

- **Main Files:** DynamicAnimationReplacer v1.1.0 for SkyrimSE

##### [Draw 2 - Dual Weapon Equip-Unequip Options](https://www.nexusmods.com/skyrimspecialedition/mods/45579?tab=files)

#### Download Instructions

- **Main Files:** Draw 2

#### Plugin Edit

In the Draw 2 MCM, there is an option to enable "shield on back" animations. We are going to want this enabled as we turned on shield on back in Simple Dual Sheath. By editing the global in the Draw 2 MCM, we can set this option to be on by default, thus removing the need to configure the MCM manually.

- Open **Draw2.esp** in SSEEdit and double-click the plugin in the left pane to expand it.
- Expand the **Global** section and select the **Draw2ShieldOnBack** record.
- Change the **Value** to **1** (see screenshot).
- Close SSEEdit and click **OK** to save your changes.

![Draw 2 Automate MCM](/Pictures/tpf/mod-installation/draw2-automate-mcm.png)

##### [Movement Behavior Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/38950?tab=files)

#### Download Instructions

- **Main Files:** Movement Behavior Overhaul SE - AIO

#### FOMOD Instructions

- **Behaviour Trigger:** Combat and Non-Combat
- **Perk Options:** No Perk
- **Patch Options:**
  - ~~360 Walk and Run Plus~~
  - ~~Combat Gameplay Overhaul~~

#### Additional Instructions

With MBO installed, there is an issue with female characters wielding greatswords not properly gripping them with their left hand. This can be fixed by editing one of the DAR behavior files. Check this [before/after comparison](https://imgsli.com/ODc2MzQ) for the fix.

- Double-click **Movement Behavior Overhaul** in Mod Organizer 2.
- In the **Textfiles** tab, scroll down to the **#mvbo$28.txt** and select it.
- Change the value in **Line 12** from `10.000000` to `0.000000`.

```
			<hkparam name="twistAngle">0.000000</hkparam>
```

- Press CTRL + S to save your changes and close the window.

> Thanks to **Ambassadurp** for posting the solution to this problem in the MBO comments section!

![MBO Hand Position Fix](/Pictures/tpf/mod-installation/mbo-hand-position-fix.png)

##### [Movement Behavior Overhaul - True Directional Movement Patch](https://www.nexusmods.com/skyrimspecialedition/mods/53905?tab=files)

#### Download Instructions

- **Main Files:** TDM MBO Patch - With animations

##### [Jump Behavior Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/36889?tab=files)

#### Download Instructions

- **Main Files:** Jump Behavior Overhaul SE - AIO

#### FOMOD Instructions

- **Main Installation:** Behavior Module
- **Jump Animations:** Realistic Jump (Recommended)
- **Directional Jump Option:** Short Jump
- **Patch Options:** *select nothing*

##### [D13 Faster GET UP STAND UP Animation](https://www.nexusmods.com/skyrimspecialedition/mods/5890?tab=files)

#### Download Instructions

* **Main Files:** D13 Faster Get Up Stand Up SSE

##### [Super Fast Get Up Animation](https://www.nexusmods.com/skyrimspecialedition/mods/46714?tab=files)

#### Download Instructions

* **Main Files:** Super Fast Get Up Animation

#### FOMOD Instructions

- **Animation Condition:** Player + Combat only

##### [Faster Reanimation](https://www.nexusmods.com/skyrimspecialedition/mods/46357?tab=files)

#### Download Instructions

- **Main Files:** Faster Reanimation - 33 Percent Faster

##### [No Heavy Muscular Walk and Idle](https://www.nexusmods.com/skyrim/mods/213/?tab=files)

#### Download Instructions

* **Main Files:** No heavy muscular idle

#### Additional Instructions

- Optimise the mod with **Cathedral Assets Optimizer** ([instructions](/tpf/guide-resources/basic-instructions/#optimising-sle-assets)).

##### [3rd Person Dual Wielding Fix](https://www.nexusmods.com/skyrimspecialedition/mods/2425?tab=files)

#### Download Instructions

* **Main Files:** DWANIM

##### [Dragon Animations Replace](https://www.nexusmods.com/skyrimspecialedition/mods/2163?tab=files)

#### Download Instructions

* **Main Files:** DragonAnimationReplace_inSE_1_01

##### [Immersive Dragons](https://www.nexusmods.com/skyrimspecialedition/mods/18957?tab=files)

#### Download Instructions

* **Main Files:** Immersive Dragons

##### [Supreme Vampire Lord](https://www.nexusmods.com/skyrimspecialedition/mods/19706?tab=files)

#### Download Instructions

- **Main Files:** Supreme Vampire Lords XP32 SE

##### [Werewolf Claws Affect Spider Webs](https://www.nexusmods.com/skyrimspecialedition/mods/11431?tab=files)

#### Download Instructions

- **Optional Files:** Werewolf Claws Affect Spider Webs - XPMSSE

---

#### Continue with the [Sound FX](/tpf/mod-installation-4/step-8/) page.