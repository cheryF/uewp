# Changelog

All notable changes to **uewp.dev — UE5 World Partition Landscape Calculator** are documented here.

---

## [2.2] — 2026-04 · UE 5.7+

### Added
- **Mesh Terrain mode** (UE 5.8+ Experimental) — full support for non-destructive static mesh terrain with Nanite clusters and baked texture arrays
- **Terrain type toggle** — switch between Classic Landscape and Mesh Terrain in the Configurator with automatic UI adjustment per mode
- **Mesh Terrain input controls** — Max Triangles per Section, Channel Texel Size, Weight Channels
- **Mesh Terrain result cards** — Base Sections, Loaded Sections, Max Tri/Section, Nanite Geometry VRAM, Baked Texture Arrays, and Cook Time estimates
- **Artist Mode Mesh Terrain support** — terrain type persistence in URL hash, MT-specific parameters (mtTri, mtTexel) encoded in share links
- **Bidirectional terrain conversion** — switching modes automatically converts component/section values to matching ranges

### Changed
- UE target updated to 5.7+ (Mesh Terrain requires UE 5.8+)
- RVT VRAM calculation now uses pool-based estimation matching UE5's actual behavior
- Calculation refinements for CPU, VRAM and resource budget estimates across both terrain modes

### Fixed
- Component count values now correctly restore when switching between terrain modes

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


