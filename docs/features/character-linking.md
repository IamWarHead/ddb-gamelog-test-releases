---
title: Character linking
parent: Features
nav_order: 3
---

# Character linking

**Tier:** Free for manual linking and initiative tracking. Basic for automatic linking of ddb-importer characters.

{: .warning }
This is a test build. Links may be wrong or may break. Please report problems, see [Feedback]({% link feedback.md %}).

Character linking tells Gamelog which Foundry actor belongs to which D&D Beyond character. Without a link, Gamelog cannot put a roll on the right actor.

| What | Tier |
| --- | --- |
| Manual character linking, initiative tracking | Free |
| Automatic linking of ddb-importer characters | Basic |

## Link a character by hand (Free)

1. Open **Gamelog Config → Characters**.
2. In the **Character linking** section, find the actor.
3. Enter the **D&D Beyond character id**. It is the number at the end of the character's address on D&D Beyond: for `https://www.dndbeyond.com/characters/12345678` the id is `12345678`.

![Character linking page]({{ '/assets/img/character-linking.png' | relative_url }})

The list shows each actor, its character id and how it was linked: manual, ddb-importer or not linked.

## Automatic linking with ddb-importer (Basic)

Actors imported with [ddb-importer]({% link integrations.md %}#ddb-importer) are linked automatically. You do not have to enter ids.

## Initiative tracking (Free)

When someone rolls initiative on D&D Beyond, Gamelog writes that result onto the linked actor's combatant in the current Foundry combat. It fills a combatant that has no initiative yet, and asks before replacing one that already has a value. Both can be changed on the **Characters** page.

While a D&D Beyond encounter is loaded in the [combat tracker]({% link features/combat-tracker.md %}), initiative comes from that encounter instead, and these settings are switched off.

## Wrong character linked?

See [Troubleshooting]({% link troubleshooting.md %}#the-wrong-character-is-linked).
