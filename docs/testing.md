---
title: Testing checklist
nav_order: 8
---

# Testing checklist

You do not have to work through all of this. Pick what matches your table, play a session, and report what felt wrong. The list is here so nothing important goes untested, and so a report can say "step 3 of the combat tracker" instead of "it broke".

{: .warning }
This is a test build. Use a copy of your world, or a world you can afford to lose, see [Use a test world]({{ '/install.html' | relative_url }}#use-a-test-world). Never test in the world you play your campaign in. Report problems in [Feedback]({{ '/feedback.html' | relative_url }}), with the console errors if there are any.

Each block says what to do and what should happen. Anything else is worth reporting, even if it looks small.

## Testing matrix

Nobody can cover everything. This matrix says which combinations matter most, so you can pick the row closest to your table and say which one you were on when you report something.

### Foundry and system

| Foundry | dnd5e | Priority | Note |
| --- | --- | --- | --- |
| v14 | 6.x | High | The main target. Item links and card look are tuned for it. |
| v13 | 5.x | High | The lowest supported pair. Cards use the dnd5e 5 markup. |
| v14 | 5.x | Medium | Worth a pass if you upgraded Foundry but not the system. |
| v13 | 6.x | Low | Unusual, but report it if you run it. |
| v12 or older, dnd5e 4 or older | — | Not supported | The module refuses to run, see [Install]({{ '/install.html' | relative_url }}#requirements). |

### Where Foundry runs

| Setup | Priority | What to watch |
| --- | --- | --- |
| Local Foundry, GM in Chrome or Edge | High | The baseline. |
| Local Foundry, GM in Firefox | High | Cookie paste, dialogs, the config window. |
| Hosted Foundry (The Forge, Molten, your own server) over HTTPS | High | The connection to the Gamelog server, and that it survives a sleep or a lost network. |
| Foundry desktop app as GM | Medium | Logging in with Patreon opens a browser window. |
| Safari, as GM or player | Medium | Layout of the config pages and the cards. |
| Tablet or phone as a player | Low | Cards should be readable, nothing more is promised. |

### Who you are in the world

| Role | Priority | What only you can see |
| --- | --- | --- |
| GM whose browser relays | High | Config, test block, unmatched marks, upgrade hints, encounter loading. |
| Second GM, not relaying | Medium | That the Overview says someone else relays, and taking over. |
| Player | High | That private rolls stay hidden and that cards land on the right actor. |

### Membership

| Tier | Priority | Point of the pass |
| --- | --- | --- |
| Test grant (what you get during a phase) | High | Everything in the checklist below. |
| Free, with the grant expired or before joining | Medium | Free features keep working and the rest is locked, not broken. |
| Your own Patreon tier after the grant ends | Medium | That the tier drops back cleanly, mid-session. |

### Roll sources

| Source | Tier | Priority |
| --- | --- | --- |
| D&D Beyond website, character sheet | Free | High |
| D&D Beyond mobile app | PRO | High |
| Encounter builder, monster rolls | PRO | Medium |
| Dice roller on the D&D Beyond site | Free | Medium |

### Other modules

| Module | Priority | Note |
| --- | --- | --- |
| None, Gamelog alone | High | Rules out conflicts in every other report. |
| ddb-importer | High | Automatic linking, and the [dynamic sync warning]({{ '/troubleshooting.html' | relative_url }}#sync-echo). |
| Dice So Nice | Medium | One roll of 3D dice, card after they land. |
| JB2A + Automated Animations | Medium | Animation on the right targets. |
| Midi-QoL | Low | Experimental, see [Integrations]({{ '/integrations.html' | relative_url }}#midi-qol-experimental). |
| Your usual module list | High | If something breaks only here, send the list. |

## 1. Install and update

- If the stable v2 module is installed, uninstall it first, see [Install]({{ '/install.html' | relative_url }}#uninstall-version-2-first).
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

{: .note }
**Please do not change your real Patreon tier for a test.** An upgrade charges you straight away, and a downgrade only takes effect when the paid period ends, so you would pay for something that proves nothing. To see how another tier behaves, use a second, **free** Patreon account instead, see below.

- Unlink Patreon on the Connection page, then link a different Patreon account that has no tier (a free account is enough).
- **Expect**: the Membership row follows within seconds, without reloading Foundry. The world drops to the lower tier, the paid features lock, and nothing breaks.
- Link your own account again.
- **Expect**: your tier comes back, equally fast. Your test grant is tied to your D&D Beyond user, not to Patreon, so it survives all of this.
- Reload Foundry in the middle of a session.
- **Expect**: it reconnects on its own and rolls keep arriving.
- With two GMs online, close the relaying GM's browser.
- **Expect**: the other GM can take over by entering their own cobalt cookie.

## What to send back

The build version, Foundry and dnd5e versions, the matrix row you were on (where Foundry runs, your role, your tier, roll source, other modules), what you did, what happened, what you expected — plus the support report and any red console errors. [Feedback]({{ '/feedback.html' | relative_url }}) has the details.
