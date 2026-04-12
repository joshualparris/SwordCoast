# Chronicles of the Sword Coast

A modular browser RPG rebuilt from a truncated legacy snapshot.  
**Repository:** [github.com/joshuaparris/SwordChronicles](https://github.com/joshuaparris/SwordChronicles)

## Run locally
1. Open a terminal in this folder.
2. Start a local server:
   - `python -m http.server 8765`
3. Open `http://127.0.0.1:8765/index.html` in a browser.

## Deploy on Vercel (static site)

This app is **plain HTML/CSS/JS** at the **repository root** (`index.html`, `src/`, `styles/`, `assets/`). Vercel must deploy **that** tree—not an empty repo with only a README.

1. **Use the right GitHub repo**  
   Your build log showed only **`/README.md` (12 B)** and *No framework detected* — that means the connected repo had almost no files. Connect the project that contains the full game (for example [SwordChronicles](https://github.com/joshuaparris/SwordChronicles)), or push this entire folder to the repo Vercel is using, then redeploy.

2. **Vercel project settings**  
   - **Root Directory:** leave empty (or `.`) so `index.html` is at the site root.  
   - **Framework Preset:** **Other** (or “No Framework”).  
   - **Build Command:** leave **empty** (no `npm run build` unless you add a real build).  
   - **Output Directory:** leave **empty** — the site is the repo root, not `dist/`.

3. **Redeploy**  
   After Git is fixed, trigger a new deployment. Opening `https://your-project.vercel.app/` should load `index.html` (same as local `python -m http.server`).

If you still see **404 NOT_FOUND**, the deployment output still does not include `index.html` — check the **Deployment → Sources** file list on Vercel.

## Project structure
- `index.html`: app shell and UI containers.
- `styles/main.css`: core styling (recovered + patch updates).
- `src/main.js`: gameplay loop, UI actions, dialogue, encounters, crafting, boss flow.
- `src/core/*`: dice, save/load, state helpers.
- `src/data/*`: races, classes, spells, items, recipes, NPCs, locations, quests.
- `src/ui/render.js`: screen rendering and sidebar/action panel rendering.
- `legacy/DNDGAME_snapshot_truncated.html`: preserved legacy extraction.
- `PLAN.md`: phased roadmap.
- `BUGS.md`: source integrity issues from the legacy snapshot.

## Save data
- Save key: `chronicles_sword_coast_save`
- Schema version: `1`
- Save payload includes `version`, `savedAt`, and serialized `state`.

## Content authoring
Add or edit content in `src/data/*`:
- New NPCs: `src/data/npcs.js`
- New locations/encounters/boss tuning: `src/data/locations.js`
- New quests: `src/data/quests.js`
- New items/shop entries: `src/data/items.js`
- New crafting recipes: `src/data/recipes.js`
- New spells/classes/races: corresponding data files

## Current gameplay coverage
- Title screen, new game, load game, help prompt
- Character creation
- Exploration and travel
- NPC interactions
- Turn-based combat with attacks, spells, potion, flee
- Side quest and main quest progression
- Crafting Warded Key
- Final boss fight and victory ending state
- Death/recovery path

## Known limitations
- No automated browser test harness yet.
- Encounter and dialogue depth is intentionally compact for this checkpoint.
- Balance tuning is baseline only and may need iteration.
# SwordCoast
