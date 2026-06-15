# Changelog

All notable changes to this project are documented here. The format is based on
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to
[Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.2.0] - 2026-06-15

### Added
- **LBB Builder Aurora** theme — a vivid, higher-saturation variant on a deeper background, kept eye-strain-optimized (capped chroma, tinted background, red reserved for errors).
- **Semantic highlighting** (`semanticHighlighting: true` + `semanticTokenColors`) across all three themes.
- **dircolors preset** (`extras/dircolors/lbb.dircolors`) for colorful `ls` output that matches the terminal palette.

### Changed
- **Rebuilt all three palettes from color science.** Every color is now derived in the perceptual **OKLCH** space and tuned to **APCA** contrast targets per role (body text, accents, comments, punctuation), with the measured contrast recorded. Backgrounds are tinted and moderate (never pure black/white); body text sits near APCA Lc 85–90 for legibility without harshness.
- **Light is now designed independently** (lower-lightness, higher-chroma accents), not an inverted dark theme — better for sustained reading in bright rooms.
- **Restricted, semantic color allocation** to avoid the "Christmas-tree" effect: variables and punctuation are de-emphasized; saturation is reserved for meaning-bearing tokens (keywords, functions, types, strings, numbers, errors).
- Fixed **Markdown** highlighting: full H1–H6 heading hierarchy, prose kept at body color for comfortable reading, code-in-Markdown in teal, no hot reds.
- **Red reserved for error meaning only** (invalid/deprecated, diff-deleted, ANSI red); numbers/constants on peach. Red and green separated by lightness for color-vision-deficiency safety.
- Simplified the **README** and added a section on `LS_COLORS`; demoted Starship to an optional note.

## [1.1.4] - 2025

- Added official website link to README; company website URL in metadata.

## [1.1.3] - 2025

- Maintenance release.

## [1.1.2] - 2025

- Maintenance release.
