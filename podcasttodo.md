# Podcast Integration TODO

**Decision:** Add.  
**Status:** ✅ Independent 25-episode D&D/RPG podcast player added 16 September 2026.
**Topic bank:** Forgotten Realms, Sword Coast lore, D&D worldbuilding, tabletop RPG storytelling.

## Completed
- [x] Store the 25-episode D&D/RPG Spotify bank directly inside Sword Coast.
- [x] Add a collapsed bottom **🎧 Podcasts** launcher.
- [x] One tap selects/loads an episode and **🎲 Different podcast** avoids immediate repeats.
- [x] Persist the last selected episode locally in this browser.
- [x] Use a Spotify embed plus an **Open in Spotify** deep link without assuming autoplay.
- [x] Keep map/game/lore interactions primary by keeping the player collapsed until opened.
- [x] Keep the player mobile-friendly and keyboard-focusable.

## Independent implementation
`index.html` now loads only the local `podcast-player.js` file. The 25 episode IDs, titles, shows and tags live in that file, so Sword Coast no longer depends on JoshHub, jsDelivr, `podcast-launcher-v3.js`, `podcast-dock-universal.js`, or a remote podcast JSON file.
