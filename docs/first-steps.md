---
title: First steps
nav_order: 3
---

# First steps: connect your world

You do these steps once, as the GM, in the browser you normally use for Foundry. Open **Game Settings → Configure Settings → D&D Beyond Gamelog → Open Gamelog Config** and go to the **Connection** page.

{: .warning }
This is a test build. If a step does not work as described, that may be a bug. Please report it, see [Feedback]({{ '/feedback.html' | relative_url }}).

{% include screenshot.html src="connection.png" alt="Connection page" %}

## 1. Log in to D&D Beyond with your cobalt cookie

The cobalt cookie is a small piece of text that D&D Beyond gives your browser when you log in. It is called `CobaltSession`. Gamelog uses it to read your game log on your behalf.

To copy it:

1. Log in on [dndbeyond.com](https://www.dndbeyond.com).
2. Open your browser's developer tools (F12).
3. In Chrome, go to **Application**. In Firefox, go to **Storage**.
4. Open **Cookies**, then `https://www.dndbeyond.com`.
5. Copy the value of `CobaltSession`.
6. In Gamelog Config → Connection, paste it into the cobalt cookie field and click **Connect**.

{% include screenshot.html src="cobalt-cookie.png" alt="Cobalt cookie in the browser developer tools" %}

{: .note }
The cookie is stored only in this GM browser. It is never sent to your players and never shared. Treat it like a password: do not post it in Discord or in a screenshot.

Only one GM browser relays D&D Beyond rolls at a time. The browser that relays is the one that holds your D&D Beyond credentials. If you have a second GM, only one of you should connect. The **Overview** page tells you whether this browser or another GM's browser relays.

## 2. Pick your campaign

After you log in, your D&D Beyond campaigns appear on the Connection page. Pick the campaign whose game log should feed this world. You must be the DM of that campaign.

If your campaign is not listed, use **Reload the list**, or paste the campaign link instead.

{% include screenshot.html src="campaign-picker.png" alt="Campaign picker" %}

A Foundry world belongs to the first D&D Beyond account that connects it. If you connect a world that another account connected first, see [Troubleshooting]({{ '/troubleshooting.html' | relative_url }}#this-world-is-registered-to-another-dd-beyond-account).

## 3. Link Patreon {#link-patreon}

Linking Patreon unlocks Basic, PRO or MAX features in this world. You can skip this step: the Free tier works without it, see [Tiers]({{ '/tiers.html' | relative_url }}).

On the Connection page, use the membership section to log in with Patreon. When it works, the page shows that the world is linked to your membership and its tier. Changes on Patreon apply within seconds.

{% include screenshot.html src="patreon-link.png" alt="Patreon link" %}

## 4. Join the test {#join-the-test}

While the test is closed, the server only sends D&D Beyond rolls to accounts that joined. On the Connection page, click **Join the test**. The page then shows your tier and how many days you have left.

If joining is refused, the page tells you why. You may have to log in with Patreon first so the server can check whether you can join.

Who can join and for how long depends on the phase:

| Phase | Dates (tentative) | Who can join | Access | You get |
| --- | --- | --- | --- | --- |
| Closed alpha | October 12–25, 2026 | Everyone who has Gamelog MAX now or had it at some point | 7 days | Gamelog MAX features |
| Closed beta | October 26–November 8, 2026 | Everyone who has Gamelog PRO or MAX now, plus everyone who tested the closed alpha | 7 days | Your own tier, at least PRO |
| Open beta | November 9–15, 2026 | Anyone, no Patreon membership needed | 3 days | Gamelog PRO features |

The open beta does not need a Patreon tier.
{% include screenshot.html src="test-phase.png" alt="Join the test" %}

When your access runs out, your world falls back to the tier of your own Patreon membership. While a closed phase runs, that means the server stops sending rolls until you have access again. You cannot join the same phase twice, but every new phase, and every new wave of testers inside a phase, lets you join again.

## 5. Link your characters

Your players' characters should be linked to their D&D Beyond characters, so rolls land on the right actor. See [Character linking]({{ '/features/character-linking.html' | relative_url }}).

## Check that it works

Roll something on D&D Beyond in the campaign you picked. A card should appear in Foundry chat. If not, see [Troubleshooting]({{ '/troubleshooting.html' | relative_url }}).
