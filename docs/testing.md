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
- **Expect**: your tier, matching what you pay for. If no login window opens (desktop app, popup blocker), the page offers a link and a copy button, and linking works through them.
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

## 11. Automatisms (PRO, experimental)

Turn the switches on in **Gamelog Config → Rolls & cards → Automatisms** first, and link a character with Fireball (or another area spell) prepared. See [Automatisms]({{ '/features/automatisms.html' | relative_url }}).

- Roll Fireball damage on D&D Beyond with tokens on the scene.
- **Expect**: template placement opens for the caster's player (or the GM); when placed, the tokens inside get target markers and the card's damage tray lists them.
- Cancel the placement, then roll Fireball again, or use the card's **Place template** button.
- **Expect**: you can place again — a cancelled attempt never blocks the next roll.
- With removal set to next turn or next round, run a combat past that point.
- **Expect**: the template disappears on the turn or round change.
- With targeting off, place again.
- **Expect**: the template lands but no targets change, on the card or in anyone's browser.
- Roll Vicious Mockery (or another spell with an effect) and open the effects tray on the card.
- **Expect**: the GM can apply the effect to the targeted tokens.
- On a card of an activity with a saving throw, click the save button.
- **Expect**: the targeted tokens roll the save with the right DC. With Midi-QoL on, there is no save button.
- Roll a private (to DM) area spell.
- **Expect**: no template placement is offered.
- With JB2A + Automated Animations on, place the template and watch the animation.
- **Expect**: it plays exactly once.

## 12. Statistics (Basic and PRO)

Open **Gamelog Config → Statistics** after some rolls, public and private. See [Statistics]({{ '/features/statistics.html' | relative_url }}).

- Roll a few attacks, checks, saves and damage on D&D Beyond, then switch the range between latest session, 30 days and all time.
- **Expect**: the counts, party at a glance, highlights and character table follow the range.
- Flush the chat log in Foundry and reopen the page.
- **Expect**: the numbers are still there.
- Switch on counting Foundry rolls (characters, monsters) and roll from a sheet in Foundry.
- **Expect**: the roll is added to the same actor's D&D Beyond rolls; switched off again, it leaves the view.
- Check the Checks & saves, Combat and Luck tabs (PRO).
- **Expect**: skills, abilities and saves are listed, each with a Luck column from 10 d20 rolls; Combat shows no hit rate, only dice figures and counts without percentages; Luck shows from 10 d20 rolls.
- Pick a character in the **Character** selector on Checks & saves, Luck and Sessions, and hover over a bar or a data point in a chart.
- **Expect**: the tables and charts narrow to that character, and the exact value shows on hover.
- Switch on **Show percentages** in Settings and open Combat.
- **Expect**: natural 20s and 1s show a share in brackets, and the advantage and disadvantage columns turn into percentages.
- Turn on luck awards in Settings.
- **Expect**: awards appear on the Luck tab for the GM only, and nowhere in chat.
- As a player, use the **My dice statistics** button next to the chat input (needs the GM on PRO).
- **Expect**: only your own characters, no monsters, no other player's private rolls. With the GM's switch off, the button explains it is unavailable.
- Post the recap to chat, and to Discord with a webhook connected.
- **Expect**: a chat card sent as "DDB Gamelog" with one wrapping row per character, readable in both Foundry 13 and 14; a Discord embed with big totals, emoji highlights and a party table. Public rolls only; private rolls never appear.
- Turn on the automatic recap, then use **Start** under **Current session** on the Sessions tab.
- **Expect**: the session that ended is posted, and new rolls count in a new session.
- Switch on **Name luck awards in the recap** and post the recap again.
- **Expect**: the card and the Discord embed list the session's awards (only when someone stands out), public rolls only.
- Roll at least 5 public rolls with the automatic recap on, then leave the table idle for 3 hours with the relaying GM browser open.
- **Expect**: the recap is posted once without anyone pressing a button, and not again after a reload.
- Use **Export CSV** and **Export JSON** in the **Import and export** section on the Settings tab.
- **Expect**: a file with one row per character or monster and session; the JSON also holds every roll.
- Use **Reset statistics** in Settings (the red button), confirm.
- **Expect**: the records of this campaign are gone and old chat rolls are not counted again.
- Pick **Import from file** and choose the JSON you exported before the reset.
- **Expect**: the rolls are back, with their types, skills and private/public state. Importing the same file again adds nothing. A file that is not an export, or an export made before this build, is refused with a message.
- Use **Import from D&D Beyond** in a browser that relays, with a campaign that has plenty of rolls.
- **Expect**: progress shows rolls read, new rolls and how far back it got; the dates move back. Rolls you already have are not doubled, and a private roll meant for another player never appears.
- Press **Stop** in the middle, then press the button again.
- **Expect**: it reads **Continue import from D&D Beyond** and carries on where it stopped.
- Tick **Also recreate the roll cards** and import from D&D Beyond again with some rolls that have no card yet.
- **Expect**: the page reports how many chat cards were made, at most the number picked next to the tick box (50, 100 or 200). The cards sit in the chat log in the order they were rolled, oldest at the top, themed like live cards, with no sound or notification, no templates or other automation, and no doubled numbers on the Statistics page. Attack and damage cards show the weapon or spell image and name; damage cards have no apply buttons. Running it again makes no further cards. A private roll is visible to the GM and its owner only.
- Let an import reach the oldest roll, then run it again.
- **Expect**: the second run stops after the first page, as it already knows everything. Within the hour after the first run the button is disabled, and hovering it shows when it works again.
- Import a campaign with more than 1,000 rolls.
- **Expect**: it stops at 1,000 rolls and says that is the most one import reads.
- Open the Sessions tab with a few sessions, including one with only a couple of rolls.
- **Expect**: dates along the bottom of the charts; a session without a d20 average or luck is a grey hollow mark with a dashed line, and hovering it says why.
- Switch on **Leave out short sessions** in Settings.
- **Expect**: sessions with fewer than 10 d20 rolls by player characters disappear from every tab, the history and the charts; switched off, they are back.
- With no attack rolls in the range, open Combat.
- **Expect**: "No attack or damage rolls in this range".
- Open the Sessions tab in a browser that does not relay, and as a member without PRO.
- **Expect**: the import from D&D Beyond is disabled and says why; without PRO the import and export buttons are locked with an upgrade hint.
- Without a tier (second free Patreon account, see section 10).
- **Expect**: the Overview shows only the session-so-far teaser with an upgrade hint, and the Checks & saves, Combat, Luck and Sessions tabs show example figures under an "Example data" banner. With **Show upgrade hints** switched off on the General page, they show a lock instead.

## 13. General page and sidebar button

Open **Gamelog Config → General** as a GM. See [First steps]({{ '/first-steps.html' | relative_url }}).

- Look at the sidebar tab column in Foundry.
- **Expect**: a dragon button above the Settings tab (in Foundry 14, below the Dice So Nice tab if you have it). Clicking it opens Gamelog Config; clicking it with the window already open brings it forward instead of opening a second one.
- Switch off **Gamelog button in the sidebar** and save.
- **Expect**: the button disappears at once, without reloading. Switch it on again and it returns.
- Log in as a player.
- **Expect**: no button.
- Switch **Show upgrade hints** off and look at a relayed card.
- **Expect**: no upgrade line, only for you.
- Change **Popup for a new module version** and reload Foundry when a newer build is out.
- **Expect**: the popup follows the choice; the green banner in Gamelog Config shows either way.

## What to send back

The build version, Foundry and dnd5e versions, the matrix row you were on (where Foundry runs, your role, your tier, roll source, other modules), what you did, what happened, what you expected — plus the support report and any red console errors. [Feedback]({{ '/feedback.html' | relative_url }}) has the details.
