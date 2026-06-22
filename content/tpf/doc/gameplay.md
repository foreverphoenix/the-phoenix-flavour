---
title: "Gameplay Guide"
weight: 3
type: docs
description: >
  An overview of changes to gameplay in TPF.
---

## SimonRim

**The Phoenix Flavour** is a SimonRim setup, which means that it is based on gameplay overhauls by [SimonMagus](https://www.nexusmods.com/profile/SimonMagus). For details please consult the individual mod pages linked on below.

[Mysticism – A Magic Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/27839) improves all aspects of the magic system while also adding nearly 200 new spells. Magic now scales much better and remains viable into the late game. Scrolls and Staves are fully integrated and, thanks to [Scrambled Bugs](https://www.nexusmods.com/skyrimspecialedition/mods/43532), you will gain experience for the respective magic school while using them.  

### Perks and Abilities

[Adamant – A Perk Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/30191) is designed to complement Mysticism. Adamant streamlines and rebalances all perk trees, and makes various convenience tweaks. For example, you no longer need to wear a helmet (e.g., a fourth piece) to benefit from Light or Heavy Armor perks. Adamant also adds religion-themed perks for synergy with Pilgrim (see below).

The Adamant **Bard Perks Addon** adds bard-themed perks to the Speech tree. When you have an instrument in your inventory, you unlock a new power to play it and give temporary buffs to yourself and nearby allies.

[Hand to Hand – An Adamant Addon](https://www.nexusmods.com/skyrimspecialedition/mods/59790) merges Lockpicking and Pickpocketing into the new Trickery perk tree (originally ‘Security’ but renamed in TPF). The addon also adds a brand-new perk tree for unarmed combat. You will be able to find skill books and trainers in Skyrim to help you improve your Hand to Hand skill. The Locksmith Addon integrates [Remember Lockpick Angle Updated](https://www.nexusmods.com/skyrimspecialedition/mods/26838) with a perk requirement for improved balancing.

The Smithing perk tree is overhauled by **Ro – Smithing Perks** for synergy with TPF's custom balancing overhaul, Ro. The perk tree is based on Adamant's Smithing Addon and consists of two branches: One for improving gear and one for crafting. Thus, you will no longer be forced to take perks that are only useful for weapons, and you will have to invest fewer perks to unlock all crafting recipes.

[Lock Bashing](https://www.nexusmods.com/skyrimspecialedition/mods/165491) allows you to open locks by force. In TPF, this ability is integrated through perks in the One-Handed, Two-Handed, and Unarmed trees. With the respective perk, you can bash open all locks up to and including Master locks. This complements Mysticism's Open Lock spells and allows each major archetype to open chests and doors their own way.

### Standing Stones and Racial Bonuses

The Standing Stone effects are reworked by [Mundus – A Standing Stone Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/33411). While the negative effects of the Apprentice, Lover, and Ritual Stones are removed in TPF, I have left the Atronach Stone's downside intact because it is also present in vanilla.

[Aetherius – A Race Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/26686) changes racial bonuses to passive skills. Khajiit are the exception: they still gain the Night Eye ability which can now be toggled at will.

Please note that **Starting Spells** are removed entirely in TPF.

## Crafting

### Smithing

The Smithing perk tree from [[ro-smithing-perks]] is based on [[adamant-a-perk-overhaul-smithing-addon]] and contains the same changes to rebalance tempering. There are now 10 tempering tiers which is reflected in the items's names thanks to [[improvement-names-customized]].

## Combat

Combat is overhauled primarily by [[blade-and-blunt-a-combat-overhaul]]. With Blade and Blunt, stamina management becomes crucial and many actions – including sneaking or holding a bow string – now drain stamina. Attacking an enemy who is themselves preparing to attack deals extra damage. Staggered enemies likewise take more damage but there is a 5 second cooldown on applying stagger. The overall difficulty spike from Blade and Blunt was mitigated by reverting to the vanilla damage modifiers.

An injury system is added by Blade and Blunt but this is only enabled when playing with Survival Mode. Please refer to the section on Survival Mode for more information.

Melee combat is further spiced up by [[precision-accurate-melee-collisions]] which adds "physically accurate collisions" as well as hitstop and weapon trails. Weapon speed is now calculated more accurately when multiple bonuses apply ([[comprehensive-attack-rate-patch]]) and unarmed attacks also benefit from weapon speed buffs ([[unarmed-weapon-speed-scaling]]).

Blocking now prevents you from catching diseases or being poisoned ([[unpoisoned-blocking]]). [[simple-timed-block]] allows you to perform perfect blocks that are guaranteed to stagger your attacker. In YOL, this ability requires the Blocking 70 perk which has been renamed to **Perfect Timing** in the [[simple-timed-block-yolviing-patch]].

### Encounter Zones

[[arena-an-encounter-zone-overhaul]] rebalances all encounter zones according to a new progression system (see below). Certain enemies will also spawn at a higher level than the player, which increases the overall difficulty of the game. 

- **Level 05:** Bandits 
- **Level 10:** Draugr, Animals, Spriggans
- **Level 15:** Mages, Forsworn
- **Level 20:** Falmer, Dwarves, Giants, Dragon Lairs
- **Level 25:** Vampires
- **Level 30:** Dragon Priest Dungeons, Daedra 

Additionally, encounter zones now reset their level after clearing them thanks to [[encounter-zones-unlocked]]. With [[locational-encounter-zones]], encounter zones also affect enemies in exterior cells, such as bandits camping out in front of their hideout. Finally, [[enemies-respect-encounter-zones]] ensures that enemies with level scaling match their level to the encounter zone, rather than the player.

### Visual Effects

Weapon impacts, blood spatters, and related sound effects are overhauled by [[sanguine-symphony]] which is paired with [[dynamic-bloodpool-framework]] for a more gory combat experience. Sanguine Symphony also adds a visual and sound effect upon dealing a killing blow (can be turned off in the MCM). Crashes related to beheading are hopefully all fixed by [[next-gen-decapitations]].

## Followers

Yolviing does not feature a full-fledged follower overhaul. Instead, a variety of smaller mods have been included to improve specific aspects of follower management. 

No change has been made to the limit for vanilla followers: you can only recruit one to your party at a time. Custom followers, however, do not count toward that limit and Yolviing features seven custom followers (-> [[content-guide#new followers]]) that can be brought along. Additionally, you can have up to three pets in your party.

### Party Management

[[swiftly-order-squad]] adds the ability to quickly issue orders to your entire party. You can access its menu through the tween menu (**TAB**) on the right side: **Utilities** -> **Party**. Select with followers to apply the commands to on the left side and command them to wait or stop waiting. The teleportation ability is useful when followers get stuck.

You can precisely determine what followers should equip through the follower inventory thanks to [[follower-equip-control]]. This mod also allows you to command followers to consume potions or food, apply poisons, or learn spells from tomes. While trading with followers, you can see their carry weight ([[show-follower-carry-weight]]). To quickly access a follower's inventory, walk up to them and press the modifier key (**SHIFT** or **LB**) while interacting with them. This is a feature added by [[dynamic-activation-key-addons-collection]]. Unfortunately, it does not work on pets added by [[cc-pets-of-skyrim]].

With [[simply-order-summons]], all commands that can be given to normal followers -- such trading, waiting, and more -- also work with summoned or resurrected followers. To dismiss a summon, press the modifier key (**SHIFT** or **LB**) while interacting with them. Be careful what items you give to summons as you may lose them permanently when you dismiss the creature or the spell runs out.

### Followers in Combat

In YOL, followers behave more intelligently in combat. They will no longer draw weapons as soon as the player does ([[followers-dont-draw-weapons]]) and should better be able to detect when the party is actually being attacked ([[project-bro-hes-there-fix-followers-not-starting-combat]]). With [[smarter-conjuration-minions]], summons should also be better at finding enemies. Occasionally, followers will be very determined to hunt down and murder enemies even when the player would rather move on.

> [!WARNING] WIP
> In the case of Inigo, a custom follower, you should be able to whistle him back. Otherwise, you can teleport party members to you although they might run off in pursuit again. It might be useful to add a disengage from combat dialogue option.

If followers are injured in combat and enter the bleedout state (kneeling down), you can heal them by interacting with them ([[press-e-to-heal-followers]]). This will give them the lowest-tier healing potion in your inventory. To heal a vampire follower you will need a Blood Potion.

> [!TIP]
> To speak normally to a downed follower, interact with them while pressing the modifier key (**SHIFT** or **LB**).

### Pets

Pets are now controlled by the **Pet Framework** added by [[menagerie-an-anniversary-edition-pet-overhaul]] which encompasses pets added by vanilla and creations. All pets are stronger and will participate in combat (with the exception of a certain rabbit).

### Tweaks and Convenience

Thanks to [[im-walkin-here-ng-with-pets]], followers will never block your way: you can just walk through them. This feature does not work with Barbas and certain summons.

With [[follower-trap-safety]], followers -- including summons -- will no longer trigger traps.

[[considerate-followers-followers-are-silent-during-dialogue]] ensures that follower banter will not play when the player is in dialogue with someone else.