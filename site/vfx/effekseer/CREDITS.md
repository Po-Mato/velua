# Effekseer VFX used in Velua

The game uses **baked images rendered with Effekseer 1.80.7**, not its WASM/WebGL runtime.
All effect sources below are **CC0 1.0 Universal**.

- Official contribution and licensing page: https://effekseer.github.io/en/contribute.html
- CC0: https://creativecommons.org/publicdomain/zero/1.0/
- Packaged license evidence: `artifacts/effekseer-source/editor/Effekseer1.80.7Mac-arm64/Sample/readme.txt`

| Author / official pack | Source presets | Bundled images |
| --- | --- | --- |
| tktk / https://effekseer.github.io/en/contributes/tktk01/index.html | Light1, Sword20, Fire3, Sword16, Cure3, Sword22, Dark1, Sword17, Sword3, Cure5, hozyo3, Blow8, Sword18, Wind1 | judgement, holyBurst, fireNova, iceBurst, frostStorm, shadow, shadowRune, slash, cut, heal, shield, impact, crit, vortex |
| tktk / https://effekseer.github.io/en/contributes/tktk02/index.html | Sword4, Blow3 | lightning, blow |
| Pierre / https://effekseer.github.io/en/contributes/Pierre02/index.html | Benediction | sanctuary |

Adaptations: fixed random seed; front view for tktk and an angled view for Pierre; framing fitted per effect; rendered on black with the official WebGL runtime; 32 sampled frames packed in each sheet; black matte converted to straight alpha without altering the emitted light contribution; transparent padding; some sprites recoloured to holy/ice/shadow/steel/healing palettes while preserving highlights; lossy RGB WebP at quality 90 with full alpha. Native slash also has four job palette variants. Runtime blends the sheets using Canvas screen compositing to retain colour when effects overlap. The reused source folders preserve all original textures and editable .efkproj files.

Original archives and SHA-256 evidence are recorded in `artifacts/effekseer-source/toolchain-provenance.json`. Toolchain is the official MIT-licensed Effekseer / EffekseerForWebGL, downloaded from https://github.com/effekseer/Effekseer/releases/tag/1807 . It is used only to author assets. Sources and bake scripts remain in this workspace. No paid assets or AI-generated artwork were used.
