# Monster and boss VFX — organic revision

The current enemy renderer combines native Effekseer animation, purpose-made transparent elemental artwork, and deterministic ballistic fragments. It does not crop attacks into geometric circles or rectangles.

## Native motion layers

Rendered with **Effekseer 1.80.7**, using the official WebGL2 runtime as an offline authoring tool. Sources by tktk: official Effects vol.1 / vol.2, **CC0 1.0 Universal**.

- https://effekseer.github.io/en/contribute.html
- https://effekseer.github.io/en/contributes/tktk01/index.html
- https://effekseer.github.io/en/contributes/tktk02/index.html
- https://creativecommons.org/publicdomain/zero/1.0/

| Runtime asset | Original preset |
| --- | --- |
| cleave | tktk01 Sword17 |
| crush | tktk01 Sword3 |
| bolt | tktk01 Fire6 |
| rift | tktk02 Claw4 |
| nova | tktk01 Sword20 |
| pillar | tktk02 Fire2 |

Adaptations: fixed seed 831, automatic per-preset framing with unclipped-boundary checks, 36 native simulation samples across 72 Effekseer frames, trimmed impact start and resampled 36-frame timeline, crop fitted across the whole timeline, approximately 224px per frame, hostile palette corrections, emitted-light RGB to straight alpha, WebP quality 90/full alpha. Initial charge is displayed separately by the game. Source ranges, dimensions, pivots and SHA256 hashes: `manifest.json`. The original projects, textures and toolchain provenance remain in `artifacts/effekseer-source/`. Reproduction: `scripts/bake-enemy-vfx.js`, `scripts/pack-enemy-vfx.py`.

## Elemental silhouettes

`organic-earth.webp`, `organic-ice.webp`, `organic-void.webp`, `organic-fire.webp` were generated for this project with the built-in imagegen tool on 2026-10-18. These images are not claimed to be part of the CC0 Effekseer packs.

The RGBA source `artifacts/enemy-organic-source.png` contains four animation keyframes per element: eruption, expansion, peak and dissipation. Runtime rows preserve the artwork and transparency; keyframes crossfade while native emitters, shards and streaks provide continuous motion. Imagegen output provenance: `exec-03ca298b-493e-42d2-a06a-a6f78d2d16cd.png`. Source copy, packer and hashes remain in the workspace: `scripts/pack-enemy-organic.py`, `organic-manifest.json`.

The game plays Canvas images. It does not start a new WebGL/WASM context. Six native sheets (216 frames) and four authored rows (16 keyframes) total 3,380,948 bytes and approximately 40.62 MiB decoded.
