# Game Source & License Audit

Last reviewed: 2026-11-11

This file records source/license screening for adding complete HTML5 games. A repository being public does not, by itself, grant reuse rights. A candidate is not imported until its license, code, assets, runtime dependencies and static-hosting compatibility are checked.

## Current website game groups

- **Compact mini-games (10):** Reaction Tap, Memory Match, Tic Tac Toe, 2048, Neon Racer, Space Pilot, Goal Rush, Snake, Minesweeper and Breakout. These are small custom game experiences in the shared player script.
- **Standalone HTML5 builds (10):** Sports Heads Football, Ludo Classic, Line Trap, Sky Dash, Bubble Shooter, Stack Tower 3D, Crossy Road, Flappy Flight, Space Invaders and Blockfall Tetris.
- The seven standalone games tagged as original are lightweight original implementations. They are not claimed to be commercial-grade or equivalent to Poki's licensed game catalogue.
- Sports Heads Football, Ludo and Line Trap are adapted from `sausi-7/games` under its MIT license. Their local copies and notices must remain together.

## External source candidates screened

### Hextris — conditionally suitable, not imported yet

- Source: https://github.com/Hextris/hextris
- Playable reference: https://hextris.github.io/hextris/
- License found in upstream README and `LICENSE.md`: GNU GPL version 3 or later.
- It is a complete HTML5 canvas puzzle game with separate JavaScript modules and local vendor scripts.
- **Blockers before import:** preserve the full GPL notice and corresponding source; package its required JS, CSS, SVG and image assets locally; remove upstream advertising and analytics; verify no required assets are omitted; test touch, keyboard, resize and fullscreen in our iframe.
- Decision: do not embed a remote URL or copy only the main HTML. Import only after the complete local dependency tree and license obligations are satisfied.

### Mozilla BrowserQuest — rejected for current static-only scope

- Source: https://github.com/mozilla/BrowserQuest
- Upstream license file states code is MPL-2.0 and content is CC-BY-SA 3.0.
- Upstream repository describes the project as deprecated and as a multiplayer HTML5 experiment.
- **Blocker:** the multiplayer game requires server-side components; a static-only Cloudflare Pages build cannot provide its original multiplayer service.
- Decision: do not list it as a working multiplayer game. A separate offline/local adaptation would need its own scope and QA.

### Blockrain.js — not selected

- Source: https://github.com/Aerolab/blockrain.js
- Description: HTML5 Tetris game for jQuery.
- **Blocker:** it duplicates the falling-block/Tetris category already represented by Blockfall Tetris. The exact upstream license and asset provenance still need review before any reuse.
- Decision: do not add a duplicate Tetris entry.

## Import acceptance checklist

A game may be marked playable only after all of these checks pass:

1. A complete local build exists in this repository; no dependency on an unrelated third-party game host.
2. A clear license covers the game code and every included image, sprite, font, audio file and other asset.
3. Required attribution, license text and source-availability obligations are preserved.
4. No paid API, secret key, account login or backend service is required for the advertised core gameplay.
5. The game runs inside the site player and its own direct URL.
6. Keyboard, mouse and touch controls are checked where applicable.
7. Start, pause, restart, game-over/win, score persistence and fullscreen are checked where applicable.
8. Desktop and mobile layouts are tested; only then may the catalogue label it playable.

## Important honesty rule

A catalogue thumbnail, SVG illustration, title or loading screen is not a game build. Do not count a game as verified merely because its page opens. Keep "source reviewed", "syntax checked", "deployed" and "manually gameplay tested" as separate statuses.
