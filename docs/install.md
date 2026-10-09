---
title: Install
nav_order: 2
---

# Install the test build

{: .warning }
This is a test build. It may break your game session. Do not try it right before a session you cannot afford to lose, and report problems, see [Feedback]({% link feedback.md %}).

## Requirements

- Foundry VTT v13 or newer (v13 is the minimum, v14 is verified).
- Game system dnd5e 5.0.0 or newer.
- A D&D Beyond account that is the DM of the campaign you want to connect.
- A Patreon membership if you want features above the Free tier, see [Tiers]({% link tiers.md %}).

## Install

1. In Foundry, open **Add-on Modules** and click **Install Module**.
2. Paste this manifest URL into the **Manifest URL** field at the bottom:

   ```text
   https://github.com/IamWarHead/ddb-gamelog-test-releases/releases/download/test-channel/module.json
   ```

3. Click **Install**.
4. Open your world, go to **Game Settings → Manage Modules**, enable **D&D Beyond Gamelog** and save.

{: .note }
This URL always points at the newest test build, so keep it: you need it once, and Foundry finds every later test release through it.

![Foundry install dialog with the manifest URL]({{ '/assets/img/install-manifest.png' | relative_url }})

Next: [First steps]({% link first-steps.md %}).

## Update

Test builds are updated often. To update, open **Add-on Modules** in Foundry and update **D&D Beyond Gamelog** like any other module. You do not need the manifest URL again, and you do not need to uninstall anything. Check the [Changelog]({% link changelog.md %}) to see what changed.

The module shows its build channel (TEST) and version on its Debug page: **Gamelog Config → Debug panel**.

If the module tells you that your version is no longer supported, update it.

## Go back to the stable v2 module

The test build and the stable v2 module use the same module id, so you can have only one of them installed at a time.

1. Close your world.
2. In **Add-on Modules**, uninstall the test build of **D&D Beyond Gamelog**.
3. Install the stable module from Foundry's module browser.

Your world keeps its settings. The test build reads your v2 settings once when it starts and stores its own copy, so your v2 settings and character links are not deleted. Two things to know:

- The cobalt cookie moves. v2 kept it in the world, the test build keeps it in the GM browser that relays and clears the world copy. After going back to v2, paste your cobalt into v2 again.
- Character links you made in the test build stay in its own settings. v2 does not read them, so check your links in v2.
