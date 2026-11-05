---
title: Changelog
nav_order: 10
---

# Changelog

{: .warning }
These are test builds. Each release may break things that worked before. Please report problems, see [Feedback]({{ '/feedback.html' | relative_url }}).

Newest first. This is a short summary for testers. Update the module in Foundry to get a release, see [Install]({{ '/install.html' | relative_url }}#update).

## 3.0.0-beta.5 (2026-11-05)

New:

- **Choose how many roll cards to recreate (PRO).** Next to **Also recreate the roll cards** you pick 50, 100 or 200; cards are made for the newest rolls of an import and 200 is the most. The statistics still take every roll.
- The import button now explains in a tooltip why it is disabled, for example during the 3-hour cooldown of a deep import.

Fixed:

- Recreated damage and healing cards show the weapon or spell image and name again.
- Recreated cards are inserted in time order instead of in reverse at the bottom of the chat.
- A recreated attack or damage card whose item has no matching activity no longer fails to appear.
- A refused deep import no longer leaves a **Continue import** button that cannot continue after a complete import.

## 3.0.0-beta.4 (2026-11-05)

New:

- **Recreate roll cards on import (PRO).** The import of past rolls from D&D Beyond can also add each roll to the chat log as a card dated when it was rolled. Tick **Also recreate the roll cards** in the import section. The cards are silent, do not run automation and are not counted twice in the statistics. See [Statistics]({{ '/features/statistics.html' | relative_url }}#import-and-export-pro).

Fixed:

- The "rolling…" placeholder card now takes the card theme.

## 3.0.0-beta.3 (2026-11-05)

New:

- **Statistics (experimental).** Dice statistics for your campaign, built from the rolls Gamelog relays from D&D Beyond and kept per campaign in the GM's browser, so flushing the chat log does not erase them. Open them in **Gamelog Config → Statistics**. Basic gets the party at a glance, highlights, a character table and the range filter. PRO adds the monster table, Checks & saves, Combat and Luck tabs, the d20 distribution, session charts and history, luck awards and luck per skill. See [Statistics]({{ '/features/statistics.html' | relative_url }}) for what to try and the known limits.
- **Player view (PRO).** Players get a **My dice statistics** button next to the chat input and see their own characters only.
- **Session recap (PRO).** Post the latest session to chat as a themed card or to Discord as an embed, by hand or automatically when a session ends. Luck awards in the recap are opt-in.
- **Import and export (PRO).** Import past rolls from D&D Beyond's game log, export statistics as CSV or JSON, and import a JSON file again to move them to another GM browser.
- **Example data.** With upgrade hints on, tabs your membership does not include show made-up example rolls instead of a lock. They are never stored.
- **General page.** A new page in **Gamelog Config** for the upgrade hints, a sidebar shortcut button and the update popup.

Fixed:

- The rolling placeholder stays until Foundry's notification finishes.

## 3.0.0-beta.2 (2026-11-04)

New:

- **Automatisms (PRO, experimental).** Relayed rolls can place spell area templates (the caster's player places their own when online), apply activity effects from dnd5e's effects tray, and show the matched activity's buttons — saving throw with DC, place template, consume/refund. Everything is off by default; the switches are in **Gamelog Config → Rolls & cards → Automatisms**. See [Automatisms]({{ '/features/automatisms.html' | relative_url }}) for what to try and the known limits.
- **Warning when DDB Gamelog Tweaks is active.** That module supports Gamelog v2 only and does not work with v3; its features are built into v3 now. Remove it to avoid doubled buttons and templates.

## 3.0.0-beta.1 (2026-10-26)

New:

- **The beta runs on a new server.** Until now the test builds talked to a test server; from this build the module connects to the server version 3 will launch on. Link Patreon in your world once more after updating (Connection page, membership section), your test days carry over and you keep the same manifest URL. Builds before the beta stay on the old test server, update to move. See [Troubleshooting]({{ '/troubleshooting.html' | relative_url }}#beta-relink) if your tier looks wrong.

Nothing else changed in the module itself.

## 3.0.0-alpha.17 (2026-10-14)

New:

- **The combat tracker sync tells you when D&D Beyond limits requests.** The GM now sees a warning, and the sync pauses and picks up again by itself, see [When D&D Beyond limits requests]({{ '/features/combat-tracker.html' | relative_url }}#when-dd-beyond-limits-requests).

## 3.0.0-alpha.16 (2026-10-13)

New:

- **French, Spanish and Brazilian Portuguese translations**, next to English and Hungarian. The module follows Foundry's own language setting, see [Install]({{ '/install.html' | relative_url }}#language).

## 3.0.0-alpha.15 (2026-10-13)

New:

- **Update notice.** The GM gets a popup when a newer test build is out, and Gamelog Config shows a green banner until you update. Players never see either. You choose whether the popup shows once per release or every time Foundry loads, see [Install]({{ '/install.html' | relative_url }}#update).

## 3.0.0-alpha.14 (2026-10-13)

Fixed:

- **Gamelog Config in Foundry's light theme.** The dropdowns opened white with pale text and the buttons washed out; both stay readable now, whatever theme Foundry is set to.
- Themed chat cards no longer mix light text with a light surface in Foundry's light theme.

## 3.0.0-alpha.13 (2026-10-12)

Fixed:

- **Patreon login works without a popup.** If the browser blocks the login window, or you run the Foundry desktop app, the page now offers the login as a link you can open or copy. The world is linked as soon as you finish, in any browser, see [Troubleshooting]({{ '/troubleshooting.html' | relative_url }}#patreon-window).

## 3.0.0-alpha.12 (2026-10-10)

New:

- **Hungarian translation.** The module follows Foundry's own language setting, see [Install]({{ '/install.html' | relative_url }}#language). More languages follow, and the translation files will be opened to the community.
- The test block on the Connection page shows the phase as a progress bar, with the dates it opens and closes and a link to the [Testing guide]({{ '/testing.html' | relative_url }}).

Fixed:

- Translations other than English are shipped with the module, so they can be picked in Foundry.
- Long options in dropdowns no longer run under the arrow.

## 3.0.0-alpha.11 (2026-10-09)

Fixed:

- Clicking the item on a card opens its sheet on Foundry 13 with dnd5e 5 as well, not only on Foundry 14.
- Actions whose name carries a variant, like "Breath Weapon (Red)", find the matching item on the actor.
- A roll whose action has no matching item is marked for the GM, so you can see why the card has no item on it.

## 3.0.0-alpha.10 (2026-10-09)

Fixed:

- The item block inside a roll card follows the card theme instead of staying on dnd5e's own background.

## 3.0.0-alpha.9 (2026-10-09)

New:

- [Legendary Patrons]({{ '/features/legendary-patrons.html' | relative_url }}): a page in Gamelog Config listing MAX members who chose to be on it, and those who held MAX before. Opt-in, under a name you pick.

## 3.0.0-alpha.8 (2026-10-09)

New:

- The test block shows when joining opens, not only when it closes.
- The feedback button only appears once you are testing or can join.

## 3.0.0-alpha.7 (2026-10-09)

Fixed:

- **Patreon memberships are recognised again.** The server looked for the wrong campaign, so every linked account came back as Lite. Link Patreon again if your tier still looks wrong.
- The Patreon link stays visible and can be unlinked while a test grant gives you a higher tier.

## 3.0.0-alpha.6 (2026-10-09)

New:

- A link to this documentation on the **Debug panel** of test builds.

## 3.0.0-alpha.5 (2026-10-09)

New:

- The D&D Beyond combat tracker can be mirrored into Foundry's combat tracker. This is experimental. See [Combat tracker]({{ '/features/combat-tracker.html' | relative_url }}).
- The GM loads a D&D Beyond encounter into the combat tracker. It is no longer picked up automatically.
- The list of D&D Beyond encounters is remembered and refreshed on demand.
- A paused D&D Beyond combat is kept instead of being ended.
- A new GM setting for loading an encounter whose combat is still in the tracker.

Fixed:

- Only encounters attached to the campaign are mirrored, and the synced combat becomes the active combat.
- Ties in initiative are ordered like D&D Beyond, so the right combatant is on turn.
- Encounters without a name show as "Untitled Encounter".
- The combat tracker updates when the D&D Beyond bar becomes available.
- The "experimental" badge only shows on the Integrations page.

## 3.0.0-alpha.4 (2026-10-08)

Fixed:

- A Foundry world belongs to its first D&D Beyond account. Other accounts can still relay rolls, but cannot use or change its Patreon link or Discord webhook. See [Troubleshooting]({{ '/troubleshooting.html' | relative_url }}#this-world-is-registered-to-another-dd-beyond-account).

Builds before 3.0.0-alpha.4 are no longer available.
