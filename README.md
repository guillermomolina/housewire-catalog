<p align="center">
  <img src="logo.svg" alt="HouseWire" width="96" height="96">
</p>

# HouseWire catalog

External type catalog for [HouseWire](https://github.com/guillermomolina/housewire) (`schema: catalog/v1`).

## Layout

```text
catalog.yaml     # id, version, title (catalog/v1)
CHANGELOG.md     # catalog SemVer (independent of HouseWire)
types/           # one YAML file per type (id, kind, terminals, …)
logo.svg         # HouseWire mark (same as the program UI)
```

Current catalog version: see `version:` in `catalog.yaml`.

## Use with HouseWire

From the HouseWire checkout:

```bash
mkdir -p catalogs
git clone https://github.com/guillermomolina/housewire-catalog.git catalogs/default
```

Or point at this tree:

```bash
export HOUSEWIRE_CATALOG=/path/to/housewire-catalog
# or
export HOUSEWIRE_CATALOGS_DIR=/path/to/parent   # loads <dir>/default
```

Site overlay: `$SITE/catalog/*.yaml` (shallow merge by `id`).
