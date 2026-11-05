---
title: Statistics (experimental)
parent: Features
nav_order: 8
---

# Statistics (experimental)

**Tier:** Free teaser, Basic for the party at a glance, the highlights and the character table, PRO for everything else. **Status:** experimental.

{: .warning }
This is a test build, and this feature is experimental on top of that. Figures may change or miss rolls. Please report problems, see [Feedback]({{ '/feedback.html' | relative_url }}).

| What | Tier |
| --- | --- |
| Session so far: rolls, natural 20s and 1s, most active roller | Free |
| Party at a glance, highlights, character table, range filter (latest session, 30 days, all time) | Basic |
| Players see their own statistics | PRO |
| Monster table, Checks & saves, Combat and Luck tabs | PRO |
| d20 distribution and session charts | PRO |
| Luck awards | PRO |
| Session history and CSV / JSON export | PRO |
| Import past rolls from D&D Beyond, and from a file | PRO |
| Session recap to chat and Discord | PRO |

Dice statistics for your campaign, built from the rolls Gamelog relays from D&D Beyond. Open them in **Gamelog Config → Statistics**.

## Where the numbers come from

- Every roll the GM's browser sees is stored there, so **flushing the chat log does not erase the statistics**.
- Records are filed per D&D Beyond campaign. The page shows the current campaign.
- They are kept in the **GM's browser only**, because they include private rolls. A second GM, or a cleared browser, starts with its own (or no) history.
- Rolls from before the module was installed, or made while no GM browser was open and deleted since, are missing. **Import and export** on the Sessions tab can fill that gap, see [Import and export](#import-and-export-pro).
- A new **session** starts after a 3-hour pause. The GM can also start one by hand, from the Sessions tab.

Rolls made in Foundry itself (from character or NPC sheets) are counted only if you switch them on, see [Settings](#settings).

## The tabs

The **Show** selector at the top picks the range: latest session, last 30 days, or all time.

- **Overview**: the party at a glance (total rolls, d20 average, natural 20s and 1s, damage dealt, healing done), highlights (highest and lowest d20 average, most natural 20s and 1s, biggest hit, most damage, most healing) and a table per character. With PRO, also a table for monsters and others.

{% include screenshot.html src="statistics-overview.png" alt="The Overview tab with highlights and the character table" %}

- **Checks & saves** (PRO): rolls by type, skills, ability checks and saving throws by ability, for the whole party or one character.

{% include screenshot.html src="statistics-checks.png" alt="The Checks & saves tab" %}

- **Combat** (PRO): attacks, damage, healing and death saves, per character and for the party.

{% include screenshot.html src="statistics-combat.png" alt="The Combat tab" %}

- **Luck** (PRO): how far each character's d20 average is above or below what the dice give on average, the d20 distribution chart and the luck awards.
- **Sessions** (PRO): session history, starting a new session, the recap, and import and export.
- **Settings**: what is counted and shown, the automatic recap, and **Reset statistics**.

{% include screenshot.html src="statistics-settings.png" alt="The Settings tab" %}

{: .note }
**There is no hit rate.** D&D Beyond rolls do not say what they were aimed at or whether they hit. The Combat tab shows the dice instead: attack d20 average, natural 20 and 1 shares, advantage and disadvantage use, damage and crits.

{: .note }
Rolls stored by earlier builds have no roll type. They count in the totals and tables of the Overview, but not in Checks & saves, Combat or Luck, and the tabs tell you how many were left out.

## Example data on locked tabs

With **Show upgrade hints** on (**Gamelog Config → General**), the tabs your membership does not include show **made-up example rolls** instead of a lock: Checks & saves, Combat and Luck (with the awards and the d20 chart) for Lite and Basic, and the session history and charts on the Sessions tab. A banner says the figures are examples, they are never stored, and your own rolls are not touched. Lite members get the tab bar too, with the real session-so-far teaser on the Overview tab. Switch the hints off and the tabs show the lock again.

## Luck

Luck is the d20 average minus the average the dice give for each roll's advantage mode. It evens out over many rolls, and it shows from 10 d20 rolls.

**Luck awards** (PRO) name the luckiest and toughest dice, and the longest hot streak (3 or more d20 rolls of 15 or higher in a row) and cold streak (3 or more of 5 or lower). They are **off by default**, only the GM sees them, and they are never posted to chat or Discord. Ties get no award.

{% include screenshot.html src="statistics-luck.png" alt="The Luck tab with luck per character and the d20 distribution" %}

{% include screenshot.html src="statistics-awards.png" alt="Luck awards on the Luck tab" %}

## Player view (PRO)

With **Let players see their own statistics** on (the default; locked without PRO), players get a **My dice statistics** button next to the chat input. It shows the rolls of the characters they own: personal bests, luck, a table and the range filter. Monsters and other players' private rolls never show.

{% include screenshot.html src="statistics-player-button.png" alt="The My dice statistics button next to the chat input" %}

{% include screenshot.html src="statistics-player.png" alt="The player's own statistics window" %}

It runs on the GM's PRO membership, players do not need one. Without PRO the button is not shown. A player's numbers start when the view first became available in their browser, and rolls of characters without a Foundry actor are not shown.

## Session recap (PRO)

The latest session as a summary: totals, highlights and the characters.

- **Post recap to chat** puts a themed card in the chat for the whole table, sent as "DDB Gamelog". Each character gets its own row with labelled values (rolls, d20 average, natural 20s and 1s, damage, healing) that wrap to fit a narrow chat, and empty values are left out.
- **Post recap to Discord** needs the Discord integration, see [Discord]({{ '/features/discord.html' | relative_url }}). The embed shows the totals as large numbers, the highlights with an emoji each, and the party as an aligned table. It is in English.
- The Settings tab can post the recap by itself when you use **Start** under **Current session**. A session that ends after a 3-hour pause is not posted.

Only **public rolls** are included, so private rolls never appear.

{% include screenshot.html src="statistics-recap-card.png" alt="The session recap card in Foundry chat" %}

{% include screenshot.html src="statistics-recap-discord.png" alt="The session recap as a Discord embed" %}

## Session history and current session (PRO)

The Sessions tab lists the latest sessions of the campaign with their rolls, natural 20s and 1s and the most active character, and charts the rolls and d20 average per session once there are two.

Under **Current session**, **Start** counts rolls from now on as a new session. With the automatic recap switched on, the session that ends is posted first.

{% include screenshot.html src="statistics-sessions.png" alt="The Sessions tab with the history, charts and the current session" %}

## Import and export (PRO)

One section on the Sessions tab, with three rows. Records are kept in this browser only, so this is also how you move statistics to another GM browser.

{% include screenshot.html src="statistics-import.png" alt="The Import and export section" %}

**Export** saves a file: **CSV** has one row per character or monster and session. **JSON** has the same figures and also keeps every roll of the campaign, private ones included, so it can be imported again. It is your own browser's data.

**From D&D Beyond** reads the campaign's earlier rolls from D&D Beyond's game log and adds the ones this browser has not stored yet, so the statistics reach back before tracking began.

- Only the browser that relays D&D Beyond rolls can do it, and it needs a connection to the server and a picked campaign. Otherwise the button is disabled and says why.
- It walks back from the newest roll, one page of 20 to 40 rolls at a time, and shows how many rolls it read, how many were new and how far back it got. **Stop** ends it; what was already added stays.
- Rolls the browser already has are not counted twice, and private rolls meant for other players are never included.
- If D&D Beyond limits requests, it waits 5, 15 and 45 seconds and tries again before it gives up. A run that stopped, failed or was limited carries on where it left off next time: the button then reads **Continue import from D&D Beyond**.
- After a complete import, a deeper import of the same campaign has a **3-hour cooldown**. A refresh of the latest rolls still works (the first pages), the older ones can be imported again after the time the page shows.
- After a complete import, running it again stops at the first page of rolls it already knows.

**From a file** imports a JSON export made with **Export JSON**, also one from another GM browser, and adds its rolls. Repeating it adds nothing. Exports made before the JSON kept the rolls cannot be imported, the page tells you so, and a file that is not a statistics export is refused without changing anything.

## Settings

- **Count Foundry rolls of player characters / of monsters**: also count rolls made from sheets in Foundry, added to the same actor's D&D Beyond rolls. Off by default, experimental.
- **Let players see their own statistics**: the player view above.
- **Show luck awards**: off by default.
- **Automatic recap** to chat and to Discord when you start a new session.
- **Reset statistics**: a red button that deletes the roll records this browser stored for the current campaign, after a confirmation. Rolls still in the chat log are not counted again.

## Known limits

- Statistics are only as complete as what the GM's browser saw, see [Where the numbers come from](#where-the-numbers-come-from).
- The history is not shared between GM browsers: use **Import and export** to move it.
- The cooldown of a deeper import is kept on the server and starts again if the server restarts.
- Only the latest manual session start is remembered, so older hand-made splits are not recovered.
- Without a membership that includes them, locked parts show a hint instead, see [Tiers]({{ '/tiers.html' | relative_url }}).
