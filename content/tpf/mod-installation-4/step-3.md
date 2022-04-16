---
title: "Step 3: Non-Player Characters"
weight: 3
type: docs
description: >
  Mods affecting NPCs, their behaviour and their voice lines.
---

##### [Run For Your Lives](https://www.nexusmods.com/skyrimspecialedition/mods/2272?tab=files)

#### Download Instructions

- **Main Files:** Run For Your Lives

##### [AI Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/21654?tab=files)

#### Download Instructions

- **Main Files:** AI Overhaul 1.7 AE

> If you do not have AE, grab **AI Overhaul for SE Only** from the Optional Files section instead.

##### [Tavern AI Fix](https://www.nexusmods.com/skyrimspecialedition/mods/23107?tab=files)

#### Download Instructions

- **Main Files:** TavernAIFix

#### Additional Instructions

The mod comes with two console commands to customise it. One will prevent innkeepers from showing you to your room, the other will make it so you'll be served whenever you sit down in an inn and not just the first time. Both can simply be added to **Autorun**.

* Double-click **Autorun** in your mod order (under the **UTILITIES** separator).
* In the **Textfiles** tab, select **Autorun.txt** and add the following lines:

```
Set TAIF_Settings_GreetPlayer to 2
Set TAIF_Settings_ShowRoom to 0
```

* Press CTRL+S to save and close the window.

> The commands will now be executed automatically when you start a new game or load your save.

##### [Rent Room Dialogue Tweak](https://www.nexusmods.com/skyrimspecialedition/mods/34470?tab=files)

#### Download Instructions

- **Main Files:** Rent Room Dialogue Tweak

##### [Welcome Back to the Bee and Barb](https://www.nexusmods.com/skyrimspecialedition/mods/33104?tab=files)

#### Download Instructions

- **Main Files:** Welcome Back to the Bee and Barb

##### [Guard Dialogue Overhaul (GDO)](https://www.nexusmods.com/skyrimspecialedition/mods/22075?tab=files)

#### Download Instructions

* **Main Files:** Guard Dialogue Overhaul SE

#### Additional Instructions

* Delete the following file(s) and/or folder(s):
  * `Guard Dialogue Overhaul.modgroups`

#### Customisation

You can disable comments that turned into memes ("no lollygagging", "someone stole your sweet roll", "curved swords", "arrow in the knee") by doing the following:

- Double-click **Autorun** in your mod order.
- Switch to the **Text Files** tab and select the **Autorun.txt**.
- Add the following line:
  - `set GDOMemes to 0`
- Close the window and click **Yes** when prompted to save your changes.

> By default, the "curved swords" line will play only until after the Alik'r quest, and the other three lines will no longer play in any hold that the player has become Thane of.

##### [Bandit Lines Expansion](https://www.nexusmods.com/skyrimspecialedition/mods/63733?tab=files)

#### Download Instructions

- **Main Files:** Bandit Lines Expansion

##### [Misc Dialogue Edits](https://www.nexusmods.com/skyrimspecialedition/mods/28904?tab=files)

#### Download Instructions

- **Main Files:** Misc Dialogue Edits - for Skyrim Unbound Reborn

##### [More Dialogue Options](https://www.nexusmods.com/skyrimspecialedition/mods/28905?tab=files)

#### Download Instructions

* **Main Files:** More Dialogue Options - for Misc Dialogue Edits

##### [Hunters Not Bandits](https://www.nexusmods.com/skyrimspecialedition/mods/1547?tab=files)

#### Download Instructions

* **Main Files:** Hunters Not Bandits

##### [Thugs Not Assassins](https://www.nexusmods.com/skyrimspecialedition/mods/34028?tab=files)

#### Download Instructions

- **Main Files:** Thugs Not Assassins
- **Optional Files:** Thugs Not Assassins - Book Covers Skyrim Patch
- **Optional Files:** Thugs Not Assassins - Timing Is Everything

> Even though Timing Is Everything will be installed later and lower in the mod order, the scripts from the TNA TIE patch will still override because the plugin will be loaded below TIE's (BSA-packed assets override according to load order, not mod order).

#### Plugin Edit

- Open **ThugsNotAssassins_BCS.esp** in SSEEdit.
- Double-click the plugin in the left pane and expand the **Book** section.
- Select the record inside. Forward the **Sound - Pickup** record from the USSEP into the TNA - BCS Patch.
- Close SSEEdit. Make sure the plugin is checked and click **OK** to save your changes.

![TNA BCS Patch Edit](/Pictures/tpf/mod-installation/tna-bcs-patch-edit.png)

##### [Narrative Gameplay Consistent Dialogue Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/64667?tab=files)

#### Download Instructions

- **Main Files:** Narrative Gameplay Consistent Dialogue Tweaks

##### [Thieves Guild Master Recognition](https://www.nexusmods.com/skyrimspecialedition/mods/65388?tab=files)

#### Download Instructions

- **Main Files:** Thieves Guild Master Recognition

##### [Windhelm Segregation - Stay at New Gnisis Cornerclub](https://www.nexusmods.com/skyrimspecialedition/mods/21181?tab=files)

#### Download Instructions

- **Main Files:** Windhelm Segregation - Stay at New Gnisis Cornerclub

#### Additional Instructions

- ESL-ify **WindhelmSegregation.esp** with SSEEdit ([instructions](/tpf/guide-resources/basic-instructions/#esl-ifying-plugins)).

#### Plugin Edit

- Open **WindhelmSegregation.esp** in SSEEdit.
- Double-click the plugin in the left pane to expand it.
- Go to **Dialog Topic** >> **RentRoomTopic**.
- Forward the **Goodbye** flag from **RentRoomDialogueFix.esp** in the records `00079B1A` and `0009CC95`.
- Close SSEEdit and click **OK** to save your changes.

![Windhelm Segregation CR](/Pictures/tpf/mod-installation/windhelm-segregation-cr.png)

##### [Alik’r Warriors Aren’t Welcome](https://www.nexusmods.com/skyrimspecialedition/mods/25384?tab=files)

#### Download Instructions

- **Main Files:** Alik’r Warriors Aren’t Welcome

#### Additional Instructions

- ESL-ify **CrimeFactionAlikr.esp** with SSEEdit ([instructions](/tpf/guide-resources/basic-instructions/#esl-ifying-plugins)).

##### [NPCs Wear Amulets of Mara](https://www.nexusmods.com/skyrimspecialedition/mods/66125?tab=files)

#### Download Instructions

- **Main Files:** NPCs Wear Amulets of Mara (SPID)

#### Additional Instructions

- Double-click **NPCs Wear Amulets of Mara** in your mod order and switch to the **INI files** tab.
- In the **NPCs_Wear_Amulets_Of_Mara_DISTR.ini**, change the `25` at the end of the line to `5`.
- Save your changes and close the window.

> A 5% chance for an NPC to be looking for a spouse seems more reasonable to me than 25%.

##### [Adopt Aventus Aretino](https://www.nexusmods.com/skyrimspecialedition/mods/3257?tab=files)

#### Download Instructions

- **Main Files:** Adopt Aventus Aretino

##### [Adopt Aventus Aretino - USSEP and Simple Children Patch](https://www.nexusmods.com/skyrimspecialedition/mods/26092?tab=files)

#### Download Instructions

- **Main Files:** Adopt Aventus Aretino - USSEP and Simple Children Patch

##### [Immersive Patrols](https://www.nexusmods.com/skyrimspecialedition/mods/718?tab=files)

#### Download Instructions

- **Main Files:** Immersive Patrols Lite

#### Additional Files

- Delete the following file(s) and / or folder(s):
  - `Immersive Patrols II.bsa`

> The BSA contains facegen files which we will later regenerate in higher quality.

#### Plugin Edit

- Open **Immersive Patrols II.esp** in SSEEdit.
- Double-click the plugin in the left pane to expand it.
- Right-click the **Leveled Item** category and select **Remove**, then confirm.
- Close SSEEdit and click **OK** to save your changes.

> This makes a patch for Open World Loot unnecessary.

![Immersive Patrols Plugin Edit](/Pictures/tpf/mod-installation/immersive-patrols-plugin-edit.png)

##### [Immersive Patrols Simplified](https://www.nexusmods.com/skyrimspecialedition/mods/32765?tab=files)

#### Download Instructions

* **Main Files:** Immersive Patrols II Simplified

#### FOMOD Instructions

- **Immersive Patrols Version:** Lite
- **Patches:** No Merchants

#### Plugin Edit

- Open **Immersive Patrols II Lite Simplified No Merchants.esp** in SSEEdit.
- Double-click the plugin in the left pane to expand it, then expand the **Leveled Item** category.
- Right-click the `LItemDawnguardWeaponAny` record, select **Remove**, and confirm.
- Close SSEEdit and click **OK** to save your changes.

> This makes a patch for Open World Loot unnecessary.

![IPS Plugin Edit](/Pictures/tpf/mod-installation/ips-plugin-edit.png)

##### [Immersive College NPCs](https://www.nexusmods.com/skyrimspecialedition/mods/9252?tab=files)

#### Download Instructions

* **Main Files:** Immersive College NPCs

#### FOMOD Instructions

* Change nothing and click **Install**.

#### Additional Instructions

- Delete the following file(s) and / or folder(s):
  - `ICNs_ImmersiveCollegeNPCs.bsa`

> The BSA contains facegen files which we will later regenerate in higher quality.

---

#### Continue with the [Improved Vanilla Quests](/tpf/mod-installation-4/step-4/) page.