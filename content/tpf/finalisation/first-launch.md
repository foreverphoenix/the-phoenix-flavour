---
title: "First Launch"
weight: 11
type: docs
description: >
  Ingame testing.
---

## A Test Game

All mods are installed. The ENB preset is configured correctly. DynDOLOD is generated. Now comes the moment of truth.

Once arrived at this point it is important to test your setup in order to make sure your game looks as intended, performs well, and runs stable so that you can finally start a new playthrough without a high risk for nasty surprises.

* In Mod Organizer 2, select **SKSE** in the exectuables drop-down and hit **Run**.
* In the main menu, open the console by pressing the tilde key (above TAB, next to 1).
* Type in `coc riverwood` and hit Enter.
* After the loading screen, you'll find yourself in Riverwood with a test character.

**Before you continue, wait for all messages in the upper left corner to run through**.

### Immersive HUD

Changes to MCM settings do not carry over across save games so it would be a waste of time to configure all MCMs for a test run. There are merely two changes in the Immersive HUD MCM that I recommend for now.

- Press **ESCAPE** and select the **MCM** Option.
- Scroll down and click on **Immersive HUD** to open the mod's MCM.
- In the **Activation** tab, check the **Key press toggles** and **Link ALL SkyUI Widgets** options.
- You can also change the hotkey to a different one if its inconvenient for you (default is X).

> This will make it so that the clock widget from A Matter of Time is toggled along with the rest of the HUD, and that you only have to press the button once to toggle all elements.

### Depth of Field

While the default Depth of Field effect is fairly ugly, you will have noticed that we specifically left it turned on while configuring INI settings way back during the Setup section. This is because the DoF effect is tied to the underwater blur effect - turn off DoF and you will be able to see as clearly underwater as above the surface. The solution to this is leaving the effect on but turning it down all the way so that the DoF effect doesn't actually kick in.

* Press **ESCAPE** and go into **Settings** >> **Display**.
* Turn down **Depth of Field** all the way.

![Turn down DoF](/Pictures/tpf/finalisation/turn-down-dof.jpg)

## Testing Suggestions

I recommend you spend at least 10 to 20 minutes ingame. Enjoy the improved graphics and take some screenshots! Once you have quit the game, proceed with the next step.

* Activate the ENBSeries FPS counter (**F7**) to monitor your frame rate.
* It may be convenient to use the console in order to enable godmode (`tgm`) and disable enemy AI (`tcai`) for testing purposes.
* Travel around Skyrim and visit your favourite locations (open the console and type `tmm 1` to enable all map markers).

Especially intense areas where you frame rate might drop are:

* the southern forest, especially when looking down at Falkreath,
* the swamp surrounding Morthal,
* the bridge looking at Riverwood,
* the Rift, particularly when approaching Riften from the south.

**When you are satisfied, close Skyrim SE again.**

If you encounter any bugs, performance lower than expected, or even crashes, please join us on Discord and provide us with detailed information about the problem. Any outstanding issues should be solved before diving back into Skyrim for a proper playthrough.

Once you are ready to begin a proper playthrough:

#### Continue with the [Mod Configuration](/tpf/mod-configuration/) page.