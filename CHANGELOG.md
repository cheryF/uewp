# Changelog

All notable changes to **uewp.dev — UE5 World Partition Landscape Calculator** are documented here.

Format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

---

## [2.1] — 2026-03 · UE 5.7

### Added
- **Platform Presets** — one-click hardware profiles (PC high-end, console, mobile) that auto-fill CPU, GPU and RAM fields
- **Collapsible result sections** — all result groups can be expanded/collapsed individually
- **Streaming Memory Profile** section with active/inactive cell breakdown
- **Cook / Import Time Estimator** — approximate editor import and cook time based on landscape size and system specs
- **Collision Memory** calculator — RAM cost for Simple, Complex and Per-Poly collision modes
- **Nanite Landscape + VSM warnings** — diagnostic alerts for known GPU budget conflicts
- **Medium and High-end Mobile presets** with approximate values and caveat notice
- **Artist Mode** (`artist.html`) — simplified artist-facing view with Share Artist Link
- **Bidirectional URL linking** — Configurator ↔ Artist Mode share links via Base64-encoded URL hash
- **Bit depth dynamic recommendation** — suggested heightmap/weightmap bit depth auto-calculated from map size, altitude range and layer count
- RVT vs Weightmap VRAM comparison table

### Changed
- Upgraded to **v2.1** versioning (was v2.0 internal)
- Resource Budget section now shows hardware load bars (CPU, RAM, GPU TFLOPs, VRAM) with color-coded thresholds
- Streaming Grid Preview canvas updated to show HLOD region boundaries
- Improved tooltip system with impact descriptions
- All result cards unified into collapsible `rsec` sections

### Fixed
- Share button `btoa` encoding edge cases causing broken URLs
- Temporal Dead Zone error in `script.js` affecting first-load calculations
- Artist Mode redirect not preserving state hash on return to Configurator
- RVT inputs remaining interactive when RVT was disabled
- Incorrect component count display for non-square configurations

---

## [2.0] — 2026-02

### Added
- Initial public release of the v2.0 calculator
- World Partition grid and streaming distance inputs
- Heightmap and Weightmap memory calculations (multi-bit-depth comparison tables)
- Runtime Virtual Texture (RVT) configuration and VRAM estimation
- Nanite Landscape toggle (UE 5.4+)
- Virtual Shadow Maps (VSM) toggle
- Per-WP-cell and per-HLOD-region memory breakdown
- View Distance / LOD / HLOD transition table
- Streaming Grid canvas visualizer
- Diagnostics panel with live warnings
- Legal Disclaimer page (`legal.html`)
- Google Analytics integration

---

## [1.x] — 2025

> Internal / pre-release versions. Not publicly documented.
