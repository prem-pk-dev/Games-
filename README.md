# Games — Global Browser Gaming Platform

A mobile-first, **static frontend-only** browser gaming website built with HTML, CSS and vanilla JavaScript. It runs on GitHub Pages or Cloudflare Pages without a backend, database, paid API or build step.

## Website structure

- `index.html` — homepage and discovery sections
- `games.html` — searchable, sortable and filterable catalogue
- `categories.html` — category directory
- `game.html` — game detail and player shell
- `favorites.html`, `recently-played.html` — browser-local collections
- `about.html`, `contact.html`, `game-submission.html`
- `privacy.html`, `terms.html`, `404.html`
- `assets/css/styles.css` — responsive design system
- `assets/js/data.js` — game and category catalogue
- `assets/js/app.js` — navigation, search, filters and local state
- `assets/js/game-player.js` — compact self-contained games
- `games/*/index.html` — standalone full-size games

## Playable games

**Compact games (10):** Reaction Tap, Memory Match, Tic Tac Toe, 2048, Neon Racer, Space Pilot, Goal Rush, Snake, Minesweeper and Breakout. These are lightweight, self-contained mini-games implemented in `assets/js/game-player.js`.

**Standalone browser games (10):** Sports Heads Football, Ludo Classic, Line Trap, Sky Dash: Platform Quest, Bubble Shooter, Stack Tower 3D, Crossy Road, Flappy Flight, Space Invaders and Blockfall Tetris. Each has its own page under `games/<game-id>/index.html` and runs locally on this static site.

**Important distinction:** the seven games tagged `ORIGINAL GAME` are original lightweight canvas implementations, not licensed commercial/Poki game builds or photorealistic 3D productions. The three adapted games are third-party MIT-licensed projects with notices in `THIRD_PARTY_NOTICES.md`. Catalogue artwork is separate from in-game graphics; a card image is not evidence of a game build.

The catalogue also contains discovery concepts marked as coming soon. A game should only be marked playable when its actual game build is present and its source/usage rights have been checked.

## Run locally

Open `index.html` in a modern browser, or serve the repository root with any static web server. Standalone games can also be opened directly from their `games/<game-id>/index.html` paths.

## Deploy

Cloudflare Pages settings: repository root as the output directory, no build command. The site is static; no backend or database is required. Favorites, theme and recent history use browser localStorage and do not sync between devices.

## Release checklist

- Verify source ownership, license and commercial distribution rights for each imported game.
- Test keyboard, mouse, touch, restart, fullscreen and responsive layouts on real devices.
- Check every internal link and catalogue entry after deployment.
- Review privacy/legal copy for the actual hosting, analytics, advertising and jurisdictions.
- Connect a form service only if contact or game submissions need to be delivered online.
