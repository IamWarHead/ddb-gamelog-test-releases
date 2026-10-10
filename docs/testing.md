---
title: Testing checklist
nav_order: 8
---

# Testing checklist

You do not have to work through all of this. Pick what matches your table, play a session, and report what felt wrong. The list is here so nothing important goes untested, and so a report can say "step 3 of the combat tracker" instead of "it broke".

{: .warning }
This is a test build. Use a copy of your world, or a world you can afford to lose. Report problems in [Feedback]({{ '/feedback.html' | relative_url }}), with the console errors if there are any.

Each block says what to do and what should happen. Anything else is worth reporting, even if it looks small.

## 1. Install and update

- Install from the manifest URL, enable the module, open a world.
- **Expect**: no red errors in the browser console (F12), and **Gamelog Config** opens from Game Settings.
- Update to a newer test build when one arrives, then reopen the world.
- **Expect**: your settings, campaign and character links survive the update.

## 2. Connection

- Paste your cobalt cookie and connect.
- **Expect**: the Connection page shows you as logged in, and your campaigns appear.
- Pick your campaign.
- **Expect**: Overview shows the campaign and which browser relays.
- Link Patreon, then look at the Membership row.
- **Expect**: your tier, matching what you pay for.
- Press **Join the test**.
- **Expect**: the page says how long you have.

Coming from v2? See [the upgrade note]({{ '/troubleshooting.html' | relative_url }}#upgraded-from-v2) — being asked to link Patreon again is expected.

## 3. Rolls and chat cards

- Roll an ability check, a skill, a save, an attack and damage on the D&D Beyond website.
- **Expect**: each arrives in Foundry chat within a few seconds, with the right name, the formula and the result.
- Roll with the result set to **DM only**, then to **self**.
- **Expect**: players do not see it; you do.
- Roll something slow and watch before the result lands.
- **Expect**: a "rolling…" card that is replaced by the result, not a second card.
- Roll from the D&D Beyond **mobile app** (PRO).
- **Expect**: it arrives like a website roll.
- Roll for a **monster** from the encounter builder (PRO).
- **Expect**: it arrives, GM-only by default.

## 4. Card look (Basic and up)

- Switch the card theme, roll again.
- **Expect**: new rolls use the theme, including the item block inside the card.
- Turn player colour borders on, have two different players roll.
- **Expect**: each card carries that player's colour.
- Switch the avatar between D&D Beyond and Foundry art.
- **Expect**: the picture on new cards changes.

## 5. Character linking

- Link an actor by hand with its D&D Beyond character id, then roll on that character.
- **Expect**: the card lands on that actor; clicking it selects the token.
- With ddb-importer installed, import a character and roll.
- **Expect**: linked automatically, shown as "ddb-importer" on the Characters page.
- Roll initiative on D&D Beyond during a Foundry combat.
- **Expect**: the combatant gets that initiative, and you are asked before an existing value is replaced.

## 6. Character sync (PRO)

- Take damage, heal, and gain temporary hit points on D&D Beyond.
- **Expect**: the Foundry actor follows within seconds.
- Add and remove a condition on D&D Beyond.
- **Expect**: the condition appears and disappears on the token; your own non-D&D-Beyond effects are untouched.
- Change AC, exhaustion, inspiration, death saves, XP or a class level.
- **Expect**: only the values you left switched on are updated.
- On a damage card, select a token and use **Apply**, including half and double.
- **Expect**: hit points change by the right amount.

## 7. Combat tracker (PRO, experimental)

- Build an encounter on D&D Beyond, attached to your campaign, with tokens placed on the scene in Foundry.
- Open Foundry's combat tracker and use **Load D&D Beyond encounter**.
- **Expect**: combatants appear with initiative in the same order as on D&D Beyond.
- Press Next on D&D Beyond a few times.
- **Expect**: the turn and round follow, a few seconds behind — see [why]({{ '/features/combat-tracker.html' | relative_url }}#why-it-is-not-instant).
- Damage a monster on D&D Beyond.
- **Expect**: its hit points follow in Foundry.
- Pause the combat on D&D Beyond, then resume.
- **Expect**: Foundry keeps the combat and picks up again.
- Press **Stop**, then load the same encounter again.
- **Expect**: you are asked whether to continue or start over, and your answer is respected.

## 8. Discord (PRO)

- Connect a webhook, then roll publicly.
- **Expect**: the roll appears in the channel as the character, with the dice.
- Roll privately.
- **Expect**: nothing is posted.
- Delete the webhook in Discord, then roll.
- **Expect**: Foundry tells you it is gone instead of failing silently.

## 9. Other modules

- **Dice So Nice**: a D&D Beyond roll shows 3D dice, once, and the card appears when they land.
- **JB2A + Automated Animations**: an attack or spell plays its animation on the targets.
- **Midi-QoL** (experimental): damage is applied through Midi, and a D&D Beyond save answers Midi's save request.
- Turn an integration off in Gamelog Config and roll again.
- **Expect**: that integration stops, the rest keeps working.

## 10. Membership and sessions

- Change your Patreon tier (upgrade or downgrade).
- **Expect**: the Membership row follows within seconds, without reloading Foundry or re-linking.
- Reload Foundry in the middle of a session.
- **Expect**: it reconnects on its own and rolls keep arriving.
- With two GMs online, close the relaying GM's browser.
- **Expect**: the other GM can take over by entering their own cobalt cookie.

## What to send back

The build version, Foundry and dnd5e versions, what you did, what happened, what you expected — plus the support report and any red console errors. [Feedback]({{ '/feedback.html' | relative_url }}) has the details.
