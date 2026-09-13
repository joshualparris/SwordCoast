# Podcast Integration TODO

**Decision:** Add.  
**Status:** ✅ Core one-click podcast bank added 13 September 2026.
**Topic bank:** Forgotten Realms, Sword Coast lore, D&D worldbuilding, tabletop RPG storytelling.

## TODO
- [x] Use the shared 25-episode D&D/RPG Spotify bank.
- [x] Add a collapsed bottom dock: **🗺️ Listen to a different Sword Coast / D&D podcast**.
- [x] One tap selects/loads another episode; persist recent choices and avoid immediate repeats.
- [x] Use Spotify embed/deep links without assuming autoplay.
- [x] Collapse automatically when HTML narration/audio/video becomes active; no autoplay is introduced.
- [x] Shared bank tags cover lore, DM advice, worldbuilding, encounters and RPG design.
- [x] Keep core map/game/lore interactions primary through the collapsed dock design.
- [x] Shared dock supplies mobile/a11y, reduced-motion and persistence behaviour; app-specific regression tests can be added later.

## Implementation
`index.html` loads the shared JoshHub `dnd` catalogue through `podcast-dock-universal.js`.
