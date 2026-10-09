---
title: Discord
parent: Features
nav_order: 5
---

# Discord

**Tier:** PRO.

{: .warning }
This is a test build. It may break. Please report problems, see [Feedback]({% link feedback.md %}).

Gamelog can post public rolls to a Discord channel.

| What | Tier |
| --- | --- |
| Discord relay of public rolls | PRO |

Only public rolls are posted. Rolls that stay private on D&D Beyond (to DM or to self) are never posted, and the server checks that again before it posts.

## Set it up

1. In Discord, create a webhook for the channel (channel settings, Integrations, Webhooks) and copy its URL.
2. In Foundry, open **Gamelog Config → Integrations → Discord**.
3. Paste the webhook URL and save.

{% include screenshot.html src="discord-config.png" alt="Discord settings" %}

{: .note }
A webhook URL lets anyone post to your channel. Do not share it and do not show it in screenshots.

## Who can change it

A Foundry world belongs to the first D&D Beyond account that connected it. Other accounts can still relay rolls, but cannot use or change the world's Discord webhook. See [Troubleshooting]({% link troubleshooting.md %}#this-world-is-registered-to-another-dd-beyond-account).

## If you delete the webhook

If you delete the webhook in Discord, rolls are no longer posted. Foundry tells you so. Set a new webhook in **Gamelog Config → Integrations → Discord**.
