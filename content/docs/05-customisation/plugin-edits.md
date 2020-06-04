---
title: "Plugin Edits"
weight: 9
type: docs
description: >
  Tweaking instructions for some of the guide's plugins.
---

## Dwemer Spectres - Remove Beards

By default, **Dwemer Spectres** includes the beards from [this mod](https://www.nexusmods.com/skyrim/mods/30062). Personally, I dislike these beards a lot and I recommend removing the 'Playable' flag from them so that they no longer appear in the character creation menu. This is easy to do in SSEEdit.

- Run SSEEdit through Mod Organizer 2.
- Click **OK** to load all your plugins and wait for SSEEdit to return `Background loader: finished`.
- Double-click **DwemerSpectresLegendary.esp** in the left pane.
- Expand the Head Part section. The records you need to edit are numbered.
- Click on `1. Dwemer Beard: Basic`. Under **DATA - Flags (sorted)**, right-click and select **Edit**.
- Click **Yes I'm absolutely sure** when the warning window pops up.
- Uncheck **Playable** in the list that pops up and click **OK** (see picture below).
- Repeat this process for the remaining records:
  - `3. Dwemer Beard: Lower `
  - `11. Dwemer Beard: Morrowind`
  - `5. Dwemer Beard: Lower Braids + Moustache`
  - `2. Dwemer Beard: Basic + Moustache`
  - `13: Dwemer Beard: Morrowind No Sideburns`
  - `14. Dwemer Beard: Morrowind No Sideburns or Moustache`
  - `12. Dwemer Beard: Morrowind No Moustache`
  - `9. Dwemer Beard - Full Braided Goatee`
  - `4. Dwemer Beard: Lower Braids + Sideburns`
  - `6. Dwemer Beard: Lower Braids + Moustache + Sideburns`
  - `7. Dwemer Beard: Lower Braids Goatee`
  - `10. DWemer Beard: Full Braided Goatee + Moustache`
  - `8. Dwemer Beard: Lower Braids Goatee + Moustache`
  - `15. Dwemer Beard: Nordic Style`
- When you're done, close SSEEdit and click **OK** to save your changes.

![Dwemer Spectres Remove Beards](/Pictures/customisation/dwemer_spectres_remove_beards.png)