---
title: Troubleshooting
nav_order: 7
---

# Troubleshooting

{: .warning }
This is a test build. Some problems are bugs. If nothing here helps, report it, see [Feedback]({% link feedback.md %}).

Before you report a problem, open **Gamelog Config → Debug panel** and use **Copy support report**. It contains no cookies, keys or tokens. Paste it into your report.

![Debug panel]({{ '/assets/img/debug-panel.png' | relative_url }})

## It does not connect

Open **Gamelog Config → Connection** and read the message. Common ones:

| Message says | What to do |
| --- | --- |
| The server is in a closed test | Click **Join the test**, see [First steps]({% link first-steps.md %}#join-the-test). |
| D&D Beyond rejected the cobalt cookie | Log in on dndbeyond.com again and copy a fresh `CobaltSession` value. |
| D&D Beyond refused the campaign | Check that you picked the right campaign and that your account is its DM. |
| The Gamelog server is not reachable | Try again in a few minutes. If it stays like this, ask on [Discord](https://discord.com/invite/HSTtrphyFg). |
| This module version is no longer supported | Update the module, see [Install]({% link install.md %}#update). |
| Your membership is already used by another D&D Beyond account | Ask on Discord. |
| This installation is blocked | Contact support on Discord. |

If none of these fits, check that you meet the [requirements]({% link install.md %}#requirements).

## Rolls do not arrive

Check these in order:

1. You joined the test and you are logged in to D&D Beyond (Connection page).
2. You picked the right campaign.
3. A GM browser is relaying. Only one GM browser relays at a time. The **Overview** page tells you whether this browser or another GM's browser relays. If another GM relays, rolls arrive through that browser.
4. The roll is not private. Rolls sent to the DM or to self on D&D Beyond stay private in Foundry.
5. The roll type is in your tier. Monster rolls and rolls from the D&D Beyond player app need PRO, see [Tiers]({% link tiers.md %}).
6. The character is linked, see [Character linking]({% link features/character-linking.md %}).

If you changed your Patreon membership, the change arrives within seconds and the Connection page updates itself. If your tier still looks wrong a minute later, reload Foundry.

## The wrong character is linked {#the-wrong-character-is-linked}

1. Open **Gamelog Config → Characters**.
2. Find the actor and look at its **D&D Beyond character id** and how it was linked (manual, ddb-importer or not linked).
3. Correct the id, or enter the right one.

A link you made by hand always wins: ddb-importer never overwrites it. If you want to ignore ddb-importer's ids altogether, turn off **Match ddb-importer actors** on the **Characters** page.

See [Character linking]({% link features/character-linking.md %}).

## This world is registered to another D&D Beyond account {#this-world-is-registered-to-another-dd-beyond-account}

The full message is: "This world is registered to another D&D Beyond account, so its Patreon link and Discord webhook cannot be used or changed with your login. Rolls still work."

A Foundry world belongs to the first D&D Beyond account that connects it. Other accounts can still relay rolls, but they cannot use or change the Patreon link or the Discord webhook of that world.

What to do:

- If you only want to relay rolls, you do not have to do anything.
- If you took over this world and the first account is not yours, ask on [Discord](https://discord.com/invite/HSTtrphyFg) to have it moved to your account.
