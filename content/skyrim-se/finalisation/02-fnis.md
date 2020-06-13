---
title: "02 Fores New Idles"
weight: 2
type: docs
description: >
  Generating meshes and scripts for FNIS.
---

## 2.1 Add FNIS to MO2

In Step 38 we installed **Fores New Idles in Skyrim** (FNIS) which is a tool used to add custom animations to Skyrim. It is required by XPMSSE and needs to be run on our mod order before it is properly installed.

* Open the **Executables** window in Mod Organizer 2 (Tools > Executables or CTRL + E).
* Click the blue plus icon and select **Add from file**.
* Navigate to `Mod Organizer 2\mods\Fores New Idles in Skyrim\tools`.
* Double-click **GenerateFNISforUsers.exe**.
* Change the Title to **Generate FNIS**.
* Click **OK**.

![Add FNIS to Tools](/Pictures/finalisation/add_fnis_to_tools.png)

## 2.2 Generate FNIS

- Run FNIS (the executable we just added) through Mod Organizer 2.
- In the window that comes up, check the following two patches in the bottom list:
  - `"GENDER Specific Animations"`
  - `"SKELETON Arm Fix"`
- Click **Update FNIS Behaviour** to generate the new files.
- Wait until FNIS confirms that animations were succesfully included, then close the window.
- If asked to create a Desktop shortcut, click **Cancel**.

## 2.3 FNIS Output

After running FNIS, all generated files will be located inside the MO2 ***Overwrite***.

* Right-click the ***Overwrite*** located at the bottom of your mod order.
* Select **Create Mod,** enter **FNIS Output** as the name and click **OK**.
* Check the mod in your mod order.
