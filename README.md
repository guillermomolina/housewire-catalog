<p align="center">
  <img src="src/housewire_catalog/logo.svg" alt="HouseWire" width="96" height="96">
</p>

# HouseWire catalog

External type catalog for [HouseWire](https://github.com/guillermomolina/housewire)
(`schema: catalog/v1`), installable as the Python package **`housewire-catalog`**.

## Install

```bash
pip install housewire-catalog
# from a checkout:
pip install -e .
```

```python
from housewire_catalog import catalog_root, types_dir, catalog_id

print(catalog_root())  # …/catalog.yaml + types/
print(types_dir())
print(catalog_id())    # "default"
```

HouseWire resolves this package automatically when no `HOUSEWIRE_CATALOG` /
`catalogs/default` override is set (`pip install 'housewire[catalog]'`).

## Layout

```text
src/housewire_catalog/
  catalog.yaml     # id, version, label (catalog/v1)
  types/           # one YAML file per type
  logo.svg
pyproject.toml
CHANGELOG.md
```

Root `catalog.yaml` / `types/` / `logo.svg` are symlinks into
`src/housewire_catalog/` so a plain git clone still works as a catalog root.

Current catalog version: see `version:` in `catalog.yaml`.

## Use with HouseWire (path override)

```bash
mkdir -p catalogs
git clone https://github.com/guillermomolina/housewire-catalog.git catalogs/default
# catalogs/default (via symlinks) is a valid catalog root
export HOUSEWIRE_CATALOG=/path/to/housewire-catalog   # or catalogs/default
```

Site overlay: `$SITE/catalog/*.yaml` (shallow merge by `id`).
