# Changelog

All notable changes to **housewire-catalog** are documented in this file.

Format inspired by [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
Versioning follows [Semantic Versioning](https://semver.org/) and is
**independent** of the HouseWire program version.

Catalog metadata lives in `catalog.yaml` (`version:`).

## [Unreleased]

## [0.5.0] — 2026-08-02

### Changed

- Terminal **ids** are face-cell tokens (``N1``, ``S2``, …); ``label`` holds
  casing marks (``L``, ``PE``, ``1``, …). Removed ``terminal_pairs``.
- TerminalStrip pins are ``N1``…``Nn`` (N-side convention) with ``NS`` grid.

## [0.4.0] — 2026-08-02

### Added

- ``Conductor`` type (``kind: conductor_type``) for leaf wires in house/v2
  ``cables:`` maps.

### Changed

- ``Cable`` is a sheath/bundle (``contains``); description updated for house/v2.
- ``Conduit`` description points at the unified ``cables:`` map.
- Catalog description targets house/v2 sites.

## [0.3.2] — 2026-08-02

### Changed

- Catalog title uses the **HouseWire** program name.

## [0.2.1] — 2026-08-01

### Added

- ``terminal_grid`` on Socket, Luminaire, Intercom, EarthElectrode,
  PowerSupply, and Relay (incl. ``mini_zbd`` subtype).

## [0.2.0] — 2026-08-01

### Added

- Element ``terminal_grid`` on MCB, MCB2P, RCD, TerminalStrip, Switch,
  Supply, and PETerminal (same face grammar as location ``opening_grid``).

## [0.1.0] — 2026-08-01

### Added

- Initial `catalog/v1` library: `catalog.yaml` + `types/*.yaml` (places,
  elements, cables, conduits) migrated out of the housewire package.
