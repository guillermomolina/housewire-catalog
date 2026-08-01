# housewire-catalog

External type catalog for [housewire](https://github.com/guillermomolina/housewire) (`schema: catalog/v1`).

## Layout

```text
catalog.yaml     # catalog metadata (id, title)
types/           # one YAML file per type (id, kind, terminals, …)
```

## Use with housewire

From the housewire checkout:

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
