---
title: Changelog
nav_order: 10
---

# Changelog

{: .warning }
These are test builds. Each release may break things that worked before. Please report problems, see [Feedback]({{ '/feedback.html' | relative_url }}).

Newest first. This is a short summary for testers. Update the module in Foundry to get a release, see [Install]({{ '/install.html' | relative_url }}#update).

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
