# Screenshots

Pages include the images below via `{{ '/assets/img/<name>.png' | relative_url }}`. Add the files here as PNG with exactly these names. Until a file exists, the page shows a broken image.

| File | What to capture | Used on |
| --- | --- | --- |
| `install-manifest.png` | Foundry "Install Module" dialog with the manifest URL filled in | install |
| `connection.png` | Gamelog Config, Connection page | first-steps |
| `cobalt-cookie.png` | Browser developer tools, cookie list, `CobaltSession` selected, value hidden | first-steps |
| `campaign-picker.png` | Campaign list on the Connection page | first-steps |
| `patreon-link.png` | Membership section after linking Patreon | first-steps |
| `test-phase.png` | Test phase block with the "Join the test" button | first-steps |
| `rolls-card.png` | A finished roll card in Foundry chat | features/rolls-and-chat-cards |
| `pending-card.png` | A pending ("rolling…") card | features/rolls-and-chat-cards |
| `card-themes.png` | Two or more card themes next to each other | features/card-look |
| `character-linking.png` | Characters page, character linking list | features/character-linking |
| `damage-card.png` | A damage or healing card with the apply buttons | features/character-sync |
| `discord-config.png` | Integrations page, Discord section, webhook hidden | features/discord |
| `combat-tracker.png` | Foundry combat tracker with a loaded D&D Beyond encounter | features/combat-tracker |
| `integrations.png` | Gamelog Config, Integrations page | integrations |
| `debug-panel.png` | Gamelog Config, Debug panel | troubleshooting |

## Naming

- Lowercase, words separated by hyphens, `.png`.
- The name describes the content, not the page.

## Never show these in a screenshot

Crop or blur before you commit:

- Installation ids.
- Cobalt cookies (`CobaltSession`).
- Discord webhook URLs.
- Email addresses.
- Other players' names. Use test accounts or blur the names.

Also check the browser tab bar, bookmarks and the support report for the same items.
