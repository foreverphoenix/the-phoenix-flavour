---
title: "First Launch"
weight: 5
type: docs
description: >
  Ingame testing and ENB configuration.
---

## The Final Step

All mods are installed. The ENB preset is configured correctly. DynDOLOD is generated. Now comes the moment of truth.

Once arrived at this point it is important to test your setup in order to make sure your game looks as intended, performs well, and runs stable so that you can finally start a new playthrough without a high risk for nasty surprises.

## Start a test game

* In Mod Organizer 2, select **SKSE** in the exectuables drop-down and hit **Run**.
* In the main menu, select **New** to start your test save.
* After the initial loading screen you will find yourself in the AS LAL cell where you can customise your (testing) character.
* When you’re done, talk to the Statue of Mara and select the **I am camping in the woods** option.
* Go to the bed in the back in the cell and interact with it to "sleep".

## Configuration

### Immersive HUD

**Both of these changes are completely optional but recommended.**

Changes to MCM settings do not carry over across save games so it would be a waste of time to configure all MCMs for a test run. There are merely two changes in the Immersive HUD MCM that I recommend for now.

- Press **ESCAPE** and select the **MCM** Option.
- Scroll down and click on **Immersive HUD** to open the mod's MCM.
- In the **Activation** tab, select the following two options:
  - Key press toggles
  - Link ALL SkyUI Widgets
- You can also change the hotkey to a different one if its inconvenient for you (default is X).

> This will make it so that the clock widget from A Matter of Time is toggled along with iHUD (and therefore hidden most of the time). Pressing the hotkey once to toggle is more convenient than having to keep pressing it in my opinion.

### Depth of Field

While the default Depth of Field effect is fairly ugly, you will have noticed that we specifically left it turned on while configuring INI settings way back during the Setup section. This is because the DoF effect is tied to the underwater blur effect - turn off DoF and going underwater you will be able to see as clearly as above the surface. The solution to this is leaving the effect on but turning it down all the way so that the DoF doesn't actually show up.

* Press **ESCAPE** and go into **Settings** > **Display**.
* Turn down **Depth of Field** all the way.

![Turn down DoF](/Pictures/finalisation/turn_down_dof.jpg)

## To Riverwood

* You will spawn near Helgen in an area you likely know well. Take some time to look around.
* Activate the ENBSeries FPS counter if you installed ENB (default hotkey: Numpad *). Otherwise use the Steam overlay or something similar.
* Go for a walk to Riverwood (if you don't know where that is, open the console and type `tmm 1` to enable all map markers).

## ENB Configuration

Serio's ENB looks beautiful out of the box, but there are some tweaks that will optimise it for our setup. Open the console (this makes it much easier to customise the ENB) and press Shift+Enter to open the ENB GUI.

### Detailed Shadows

One of the moderately performance-intense features of ENB is **Detailed Shadows**, although that's not why I recommend disabling it. Cathedral Grass (and grass mods in general) looks, in my opinion, a great deal better with this setting disabled.

- Open the **EFFECT** section where you can toggle the main features of ENB.
- Uncheck `EnabledDetailedShadows` (see screenshot below).
- Click **Save Configuration**. Close the ENB GUI (Shift+Enter) and the console.

![Disable Detailed Shadows](/Pictures/finalisation/enb-disable-detailed-shadows.png)

### Interior Lighting

- Enter one of the two public interiors in town (the Sleeping Giant Inn or the Riverwood Trader).
- Once again, open the console and ENB GUI.
- Scroll down in the column on the left to **ENVIRONMENT** and open that section.
- Scroll down to the following two lines:
  - `AmbientLightingIntensityInteriorDay`
  - `AmbientLightingIntensityInteriorNight`
- These are currently tweaked for Enhanced Lighting and ENB, and are too high for Luminosity which is the TPF lighting overhaul.
- Tweak these values as you see fit. For `InteriorDay`, I prefer **1.10**, the `InteriorNight` value I set a little lower.
- You can close the GUI / console to Wait (default hotkey is T) for nighttime to tweak the `InteriorNight` value.
- Once done, click **Save Configuration**. Close the ENB GUI (Shift+Enter) and the console.

> Note that when you type the values in the ENB GUI and hit Enter, they will also be typed in the console which will return an error. Don't worry about this.

![ENB Environment](/Pictures/finalisation/enb-environment-section.png)

![ENB Ambient Lighting](/Pictures/finalisation/enb-tweak-interior-lighting.png)

### PostPassFX

- Go back outside and use the Wait function to set the time to midday. In case of bad weather, type `fw 81a` in the console and hit Enter.
- Position yourself so that you have a nice view of the village. Open the console and the ENB GUI.
- In the right column, open the **ENBEFFECTPOSTPASS.FX** section which includes a bunch of optional tweaks.

You can toggle these options at any time. Personally I only change the LUT to something a little colder. Feel free to experiment!

- Toggle and tweak the **Vignette** effect.
- Toggle and tweak the **Letterbox** effect.
- Toggle and tweak the **LUT** effect. Change the **Gradiant Tint Type** for different LUTs.

Don't forget to click **Save Configuration** if you changed anything.

![ENB Ambient Lighting](/Pictures/finalisation/enb-postpass-fx.png)

## Testing Suggestions

* You will spawn near Helgen in an area you likely know well. Take some time to look around.
* Activate the ENBSeries FPS counter if you installed ENB (default hotkey: Numpad *). Otherwise use the Steam overlay or something similar.
* It is often convenient to use the console in order to enable godmode (`tgm`) and disable enemy AI (`tcai`) for testing purposes.
* Travel around Skyrim and visit your favourite locations (open the console and type `tmm 1` to enable all map markers if you haven't done this already).
* Especially intense areas where you frame rate might drop are:
  * the southern forest, especially when looking down at Falkreath.
  * the swamp surrounding Morthal.
  * the bridge looking at Riverwood.
  * the Rift, particularly when approaching Riften from the south.

I recommend spending at least 10 to 20 minutes ingame. Enjoy the improved graphics and take some screenshots! Once you have quit the game, proceed with the next step.