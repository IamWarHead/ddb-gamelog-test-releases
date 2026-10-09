---
title: Feedback
nav_order: 8
---

# Feedback

{: .warning }
This is a test build. It will have bugs. Your reports are the reason it exists.

For now, all feedback and help go through Discord. If you are not on the server yet, join it first: [https://discord.com/invite/HSTtrphyFg](https://discord.com/invite/HSTtrphyFg)

Each test phase has its own channel. Post your reports in the channel of the phase you are testing:

| Phase | Channel |
| --- | --- |
| Closed alpha | [Closed alpha feedback](https://discord.com/channels/809036031835111475/1558030216763547648) |
| Closed beta | [Closed beta feedback](https://discord.com/channels/809036031835111475/1558031330430816287) |
| Open beta | [Open beta feedback](https://discord.com/channels/809036031835111475/1558031803317756034) |

The channel links only open once you are on the server.

## What to include

- Module version, for example 3.0.0-alpha.5. You find it on **Gamelog Config → Debug panel**.
- Foundry VTT version.
- dnd5e version.
- What you did, step by step.
- What happened.
- What you expected to happen.
- Any red error from the browser console, see below.

Foundry shows the Foundry and system versions at the bottom of the **Game Settings** sidebar tab.

## Errors in the browser console

Foundry runs in your browser, so most problems leave a message there. It is the single most useful thing you can send.

1. Press **F12** in the browser window that runs Foundry. On a Mac use **⌥⌘I** (Chrome, Edge) or **⌥⌘C** (Safari, after enabling the Develop menu).
2. Open the **Console** tab.
3. Reproduce the problem.
4. Copy the red lines, especially any that mention `ddb-game-log`.

A screenshot of the console works too. Keep the whole message, not only its first line: the part below it says where the error came from.

{: .note }
The console may also show errors from Foundry itself and from other modules. Send what you see, we sort it out.

## Easy way

On the **Connection** page there is a **Send feedback** button. It copies a diagnostics report to your clipboard (no secrets in it). Paste it into your message on Discord.

You can also use **Copy support report** on the **Debug panel**.

## Do not share

Do not post any of these in Discord, in screenshots or anywhere else:

- Your cobalt cookie (`CobaltSession`).
- A Discord webhook URL.
- Your email address.

The console prints network requests as well, so check a console screenshot for these before you post it.

Screenshots help a lot. Check them before you post.
