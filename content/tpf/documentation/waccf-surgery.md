---
title: "WACCF Surgery"
weight: 10
type: docs
description: >
  My notes on the version of WACCF used in TPF.
---

The mod [Weapons Armor Clothing and Clutter Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/18994) is the absolutely essential and extremely inconvenient at the same time. It is bloated with features ranging from rebalancing weapon tiers to adding proper activators to dagger racks in Hearthfire player homes and improving the levelled lists for furniture containers.

For the longest time, I accepted the headache that WACCF causes with its sweeping changes, making use of various patches and mostly ignoring the rest. However, I finally decided for the 5.0 release of TPF to move forward with the balancing overhaul I had long wanted to create and this entailed the necessity to perform major surgery on WACCF.

## Removed Features

- **Armor and weapoon edits.** I have my own balancing tweaks in Weapons & Armor Overhaul.
- **Furniture containers respawn.** WACCF adds Respawn flags to some furniture containers. This would cause copies of these containers in player-owned areas to also respawn (and remove whatever the player put in them). WACCF does replace the vanilla ones with new NoRespawn ones, but overall the effort to do the same thing for mod-added containers is not worth it.
- **Armored Clothing:** WACCF adds armor values to some clothing items. I prefer having a clear distinction between armor and clothing so I went through and removed armor values from all clothes.
- **Perk and Spell edits.** The smithing perks are covered by SPO in TPF, all other perks are handled by Adamant. The spell edits mostly relate to the Bleeding affect applied by Hack and Slash/Limbsplitter perks; however, with Adamant, the damage caused is no longer weapon-tier specific so those spell records are actually unused.
- **Most Constructible Objects (crafting recipes).** These are already covered sufficiently by Simple Smithing Overhaul Simplified.
- **Proper activators for BYOH weapon displays.** Using the [original mod](https://www.nexusmods.com/skyrimspecialedition/mods/3622) that was merged into WACCF instead.

## Remaining Features

- **Clothing and jewelery edits.** These are the main reason I am holding onto WACCF. I kept a lot of the naming and mesh tweaks as well as adjustments to weight and value plus all related Armor Addon and Texture Set records.
- **Separate hoods and robes.** In vanilla, most robes are available in a hooded and a non-hooded variant. WACCF did the legwork of splitting off the hood meshes and implementing the hoods separately which I greatly appreciate and decided to keep.
- **Edits to the Diplomatic Immunity quest.** WACCF expands the conditions for remaining undiscovered in the Thalmor embassy a little. For one, it replaces the vanilla Hooded Thalmor Robes with Thalmor Robes and a separate Thalmor Hood (as per the previous feature). You can also wear other Thalmor Robes (found in the wild or crafted with MCE) for the same effect.
- **Furniture containers.** WACCF expands the variability of items found in various furniture contains such as wardrobes or end tables. 
- **Misc Item and Ingestible edits.** WACCF tweaks the weight and value for many items to be more consistent or sensible.
- **NPC and Leveled List tweaks.** These are staying for now and may be adjusted/removed in the future.
- **Enchanting tweaks.** Also staying for now, to be adjusted.
- **Projectile tweaks.** Because why not.

## Required Assets

Below listed are all the assets from WACCF that I am keeping for my modified copy of WACCF itself as well as my Weapon & Armor Overhaul.

### Meshes

Assets for that one skeleton to prevent crashes:

- `meshes\actors\`
- `meshes\armor\dbarmor\1stpersondbamorsleeveless_0.nif`
- `meshes\armor\dbarmor\1stpersondbamorsleeveless_1.nif`
- `meshes\armor\dbarmor\1stpersondbamorsleeveless_f_0.nif`
- `meshes\armor\dbarmor\1stpersondbamorsleeveless_f_1.nif`
- `meshes\armor\dbarmor\dbarmorhood---.nif` >> *all files starting with this*
- `meshes\armor\dbarmor\dbarmorsleeveless_0.nif`
- `meshes\armor\dbarmor\dbarmorsleeveless_1.nif`
- `meshes\armor\dbarmor\dbarmorsleeveless_f_0.nif`
- `meshes\armor\dbarmor\dbarmorsleeveless_f_1.nif`
- `meshes\armor\draugr\draugrhelmargonianf.nif`
- `meshes\armor\imperial\f\1stpersongauntletspenitus_0.nif`
- `meshes\armor\imperial\f\1stpersongauntletspenitus_1.nif`
- `meshes\armor\imperial\f\1stpersongauntletspenitusbeast_0`
- `meshes\armor\imperial\f\1stpersongauntletspenitusbeast_1`
- `meshes\armor\thievesguild\f\1stpersontorso_0.nif` >> needed?
- `meshes\armor\thievesguild\f\1stpersontorso_1.nif` >> needed?
- `meshes\armor\thievesguild\f\1stpersontorsoleader_0.nif` >> needed?
- `meshes\armor\thievesguild\f\1stpersontorsoleader_1.nif` >> needed?
- `meshes\armor\thievesguild\f\1stpersontorsovariant_0.nif`
- `meshes\armor\thievesguild\f\1stpersontorsovariant_1.nif`
- `meshes\ccor\`
- `meshes\clothes\`
- `meshes\dlc01\armor\falmerheavy\`
- `meshes\dlc01\armor\ivory\`
- `meshes\dlc01\clothes\`
- `meshes\dlc01\`

The `meshes\potions\` folder is a special case - it's in the wrong directory (it should be inside `meshes\clutter`). However, all meshes included are already replaced by Medieval Spirits and RUSTIC POTIONS, so keeping the ones from WACCF is unnecessary.

### Scripts

- The entire scripts folder.

### Textures

- `textures\actors\`
- `textures\armor\thievesguild\`
- `textures\ccor\`
- `textures\clothes\executioner\`
- `textures\clothes\wench\`