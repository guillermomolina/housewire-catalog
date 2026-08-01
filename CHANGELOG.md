# Changelog

All notable changes to **housewire-catalog** are documented in this file.

Format inspired by [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
Versioning follows [Semantic Versioning](https://semver.org/) and is
**independent** of the housewire program version.

Catalog metadata lives in `catalog.yaml` (`version:`).

## [Unreleased]

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
