# Velua typography

All fonts are self-hosted and distributed with their original SIL Open Font License 1.1 text. Runtime never requests Google Fonts or a remote CDN.

| Role | Family | Official source | License file |
| --- | --- | --- | --- |
| Korean engraved headings, menu titles, tabular stat numerals | Hahmlet variable, 100–900 | https://github.com/hyper-type/hahmlet ; https://github.com/google/fonts/tree/main/ofl/hahmlet | Hahmlet-OFL.txt |
| Ornamental Latin labels and floating combat numerals | Cinzel Decorative, 400 / 700 | https://github.com/google/fonts/tree/main/ofl/cinzeldecorative | CinzelDecorative-OFL.txt |
| Descriptions, controls, compact labels | SUIT variable, 100–900 | https://github.com/sun-typeface/SUIT | SUIT-OFL.txt |

Processing: FontTools 4.67.0 / Brotli WOFF2 conversion. Hahmlet is split into common and extended Unicode ranges while preserving the union of all 3,607 original mapped codepoints, including 2,788 Hangul syllables. Characters outside upstream coverage retain the system fallback. The variable weight axis and OpenType tables are preserved. SUIT is copied unchanged from the official WOFF2 distribution. Cinzel Decorative is converted from official TTF to WOFF2. Original copyright/name/license records are retained.

The common Hahmlet and SUIT files are preloaded. All faces use font-display: swap. Additional Hahmlet coverage loads when required. Stats use Hahmlet's tabular numerals; decorative combat numbers intentionally use Cinzel Decorative.

Original source files and download hashes: `artifacts/font-sources/sources.json`. Runtime hashes and coverage: `manifest.json`. Reproducible packaging: `scripts/pack-game-fonts.py`. The authoring dependencies are isolated under `artifacts/font-tools` and are not part of the game runtime.
