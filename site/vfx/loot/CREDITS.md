# Loot beacon VFX

Created with **Effekseer 1.80.7** (official macOS arm64 editor CUI export and official WebGL2 offline renderer).

External source: **tktk Effects vol.1**, distributed under **CC0 1.0 Universal** by the official Effekseer site:
- https://effekseer.github.io/en/contributes/tktk01/index.html
- https://effekseer.github.io/en/contribute.html
- https://creativecommons.org/publicdomain/zero/1.0/

Reused original textures: `Line01.png`, `Aurora.png`, `star.png`, `Particle01.png`, `circle4.png`, `AuroraRing.png`. The new editable projects combine those textures into six rarity-specific continuous loot columns with animated energy ribbons, rising particles, rotating ground seals and high-rarity suspended crowns. A short discovery burst also reuses Pierre's CC0 Benediction preset from the game's existing Effekseer atlas set (see ../effekseer/CREDITS.md).

Tool sources, copied textures with SHA256 hashes, `.efkproj`, exported `.efk`, and captured frames are retained in `artifacts/loot-vfx-source/`. Reproduction scripts: `scripts/author-loot-vfx.py`, `scripts/bake-loot-vfx.js`, `scripts/pack-loot-vfx.py`.

Each file contains 24 native-rendered animation frames sampled after the emitters reach equilibrium, resized to 128x384, packed in 6 columns, with the black light contribution converted to straight alpha. Runtime: 12 fps, six cached images, Canvas screen blending, no Effekseer/WASM execution in the game. A static authored frame is used in reduced-effects mode; a procedural beacon remains available if an asset fails to load.
