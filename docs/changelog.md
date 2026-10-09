---
title: Changelog
nav_order: 9
---

# Changelog

{: .warning }
These are test builds. Each release may break things that worked before. Please report problems, see [Feedback]({{ '/feedback.html' | relative_url }}).

Newest first. This is a short summary for testers. Update the module in Foundry to get a release, see [Install]({{ '/install.html' | relative_url }}#update).

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
