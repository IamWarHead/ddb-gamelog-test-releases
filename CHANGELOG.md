# Changelog

## [3.0.0-alpha.5](https://github.com/IamWarHead/ddb-game-log-dev/compare/foundry-module-v3.0.0-alpha.4...foundry-module-v3.0.0-alpha.5) (2026-10-09)


### Features

* cache the D&D Beyond encounter list in the module, refresh on demand ([2aa7970](https://github.com/IamWarHead/ddb-game-log-dev/commit/2aa7970889a08016139985566be6ad275b56e650))
* keep a paused D&D Beyond combat instead of ending it ([26ae5c0](https://github.com/IamWarHead/ddb-game-log-dev/commit/26ae5c0fddda5133a9ab1a73e4415a735a709cf3))
* **module:** GM setting for loading an encounter whose combat is still in the tracker ([4986f7f](https://github.com/IamWarHead/ddb-game-log-dev/commit/4986f7febb5a3038929d3a46dfb6fa4bf2fb17b3))
* **module:** mark the D&D Beyond combat tracker as experimental ([665845a](https://github.com/IamWarHead/ddb-game-log-dev/commit/665845a575933876f1b51c644c9b6202a5195e13))
* **module:** mirror the D&D Beyond combat tracker into Foundry's combat tracker ([19431a2](https://github.com/IamWarHead/ddb-game-log-dev/commit/19431a2ca8a5bd11346da77df01b5b71f1feb198))
* the GM loads a D&D Beyond encounter into the combat tracker instead of automatic pickup ([c6a96a3](https://github.com/IamWarHead/ddb-game-log-dev/commit/c6a96a3b6b9691e81261effd803acf1b203b512f))


### Bug Fixes

* mirror only encounters attached to the campaign; activate the synced combat ([38f6f4c](https://github.com/IamWarHead/ddb-game-log-dev/commit/38f6f4c5d99143c49dbf9c5258d74176e04c0474))
* **module:** break initiative ties by name like D&D Beyond ([8503fae](https://github.com/IamWarHead/ddb-game-log-dev/commit/8503fae1968cb53be33afde05869896c174ef26a))
* **module:** experimental badge only on the Integrations page ([60b28a8](https://github.com/IamWarHead/ddb-game-log-dev/commit/60b28a8046438c1636e855af54b8b0c80141c642))
* **module:** new options object for every Foundry document call (Foundry mutates them) ([f85b68b](https://github.com/IamWarHead/ddb-game-log-dev/commit/f85b68b34ac756b55e8fec1c7cdf181d56ea28c4))
* **module:** order ties like D&D Beyond (list order), so the right combatant is on turn ([dbcbdae](https://github.com/IamWarHead/ddb-game-log-dev/commit/dbcbdaea9d845722561871455c8b0c15b50009b1))
* **module:** re-render the combat tracker when the D&D Beyond bar becomes available ([ce9ca4e](https://github.com/IamWarHead/ddb-game-log-dev/commit/ce9ca4ec61f1abc336f91f59edc7cad56a03085e))
* **module:** show unnamed encounters as Untitled Encounter, singular counts ([129d337](https://github.com/IamWarHead/ddb-game-log-dev/commit/129d337ea132c9666e548b541bfd0a03486df431))

## [3.0.0-alpha.4](https://github.com/IamWarHead/ddb-game-log-dev/compare/foundry-module-v3.0.0-alpha.3...foundry-module-v3.0.0-alpha.4) (2026-10-08)


### Bug Fixes

* **server:** an installation belongs to its first D&D Beyond user; others cannot use or change its Patreon link or Discord webhook ([76c1a89](https://github.com/IamWarHead/ddb-game-log-dev/commit/76c1a89eb479f40f8175e4bb7d0cd840fe4ce9ca))

## [3.0.0-alpha.3](https://github.com/IamWarHead/ddb-game-log-dev/compare/foundry-module-v3.0.0-alpha.2...foundry-module-v3.0.0-alpha.3) (2026-10-08)
