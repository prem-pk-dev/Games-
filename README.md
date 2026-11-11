# Games — Global Browser Gaming Platform

A mobile-first static browser gaming website built with HTML, CSS and vanilla JavaScript.

## Current structure

- \`index.html\` — homepage and discovery sections
- \`games.html\` — searchable and filterable catalogue
- \`categories.html\` — category directory
- \`game.html\` — game detail and player shell
- \`favorites.html\` — locally saved favorites
- \`recently-played.html\` — local play history
- \`about.html\`, \`contact.html\`, \`game-submission.html\`
- \`privacy.html\`, \`terms.html\`
- \`assets/css/styles.css\` — responsive design system
- \`assets/js/data.js\` — game and category catalogue
- \`assets/js/app.js\` — navigation, search, filters and local state
- \`assets/js/game-player.js\` — original mini-game implementations

## Working mini-games in this starter build

- Reaction Tap
- Memory Match
- Tic Tac Toe (local two-player)
- 2048

Other catalogue entries are discovery placeholders and are clearly marked as not playable yet. They must not be represented as playable until the game build and distribution rights are verified.

## Run locally

Open \`index.html\` in a modern browser or serve the folder with any static web server.

## Deploy

The project is static and can be deployed to GitHub Pages or Cloudflare Pages. For Cloudflare Pages, use the repository root as the output directory; no build command is required.

## Important before public launch

- Verify game source, ownership, licenses and commercial distribution permissions individually.
- Replace placeholder game cards with genuine game builds and approved artwork.
- Connect the contact form to a form provider if submissions are needed.
- Review legal pages for the actual hosting, analytics, advertising and jurisdictions.
- Add privacy/consent handling before enabling analytics or advertising.
- Test mobile touch controls, keyboard controls, fullscreen and performance on real devices.

No backend or database is required for the current static features. Favorites, theme and recent history are stored locally in the visitor's browser and do not sync between devices.
