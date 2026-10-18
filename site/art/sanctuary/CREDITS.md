# Sanctuary world art

Created for Velua with the built-in ImageGen authoring tool, 2026-10-17.
These are original generated illustrations, not downloaded commercial packs.

- Adventurer/creature atlas: 6 adventurers, 12 creature archetypes, 6 initial props.
- Region prop atlas: 3 distinct props per region, 4 regions.
- Ground paintings: forest, moonlit marsh, void citadel, ember sanctuary.
- Ability icon atlas: 18 painted spell icons.
- Ember dragon: a separate full-body boss illustration matching the existing boss name.

Source PNGs: `artifacts/world-art-source/` in the project.
Prompts and art direction: `docs/art-overhaul.md`.
Reproducible crop/resize/WebP packaging: `scripts/pack-world-art.py` (Pillow).
Runtime: `src/world-art.js`, `src/skill-icons.js`, Canvas 2D; no external asset server.

The existing Effekseer VFX have separate authors and CC0 source notices in
`public/vfx/effekseer/CREDITS.md`.
