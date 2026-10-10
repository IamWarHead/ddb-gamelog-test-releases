---
title: Install
nav_order: 2
---

# Install the test build

{: .warning }
This is a test build. It may break your game session. Do not try it right before a session you cannot afford to lose, and report problems, see [Feedback]({{ '/feedback.html' | relative_url }}).

## Requirements

- Foundry VTT v13 or newer (v13 is the minimum, v14 is verified).
- Game system dnd5e 5.0.0 or newer.
- A D&D Beyond account that is the DM of the campaign you want to connect.
- A Patreon membership if you want features above the Free tier, see [Tiers]({{ '/tiers.html' | relative_url }}).

## Use a test world

{: .warning }
**Do not test in the world you play your campaign in.** This build writes to your actors: hit points, conditions, initiative, combats. A bug there is not something you can undo in the middle of a session.

Make a copy first. In Foundry's **Game Worlds** list, open the world's menu and use **Duplicate World**, then install and test in the copy. If you host elsewhere, take whatever backup your host offers before you start.

If you want to try it in a real session anyway, take a backup of the world beforehand and keep it until the session is over. Report what breaks either way, see [Feedback]({{ '/feedback.html' | relative_url }}).

## Uninstall version 2 first

The test build and the stable v2 module share the same module id, so Foundry can hold only one of them at a time. If **D&D Beyond Gamelog** is already installed from the module browser, remove it before you install the test build.

1. Close your world, so no world has the module active.
2. In **Add-on Modules**, find **D&D Beyond Gamelog** and uninstall it.
3. Restart Foundry if it still lists the old version.

Uninstalling does not touch your world. Your v2 settings and character links stay in it, and the test build reads them once when it first starts. Going back later is just as easy, see [Go back to the stable v2 module](#go-back-to-the-stable-v2-module).

{: .warning }
Do not try to install the test build over v2 without uninstalling. Foundry may keep the old files, and you end up with a module that half updates and fails in ways nobody can reproduce.

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

{% include screenshot.html src="install-manifest.png" alt="Foundry install dialog with the manifest URL" %}

## Language

The module follows Foundry's own language setting, under **Game Settings → Configure Settings → Core**. English and Hungarian are available; anything not translated falls back to English.

More languages are on the way, and the translation files will be opened up so the community can add its own. If you would like to translate Gamelog into your language, say so on [Discord](https://discord.com/invite/HSTtrphyFg) and you will be told how once it opens.

Next: [First steps]({{ '/first-steps.html' | relative_url }}).

## Update

Test builds are updated often. To update, open **Add-on Modules** in Foundry and update **D&D Beyond Gamelog** like any other module. You do not need the manifest URL again, and you do not need to uninstall anything. Check the [Changelog]({{ '/changelog.html' | relative_url }}) to see what changed.

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
