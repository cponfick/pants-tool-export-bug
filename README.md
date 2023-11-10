# Pants Tool Export Bug

With pants `>=2.18.0rc1` it is not possible to export python tools with:

```bash
pants export --resolve=black
```

It fails with:

```bash
[ERROR] 1 Exception encountered:

Engine traceback:
  in `export` goal

ExportError: No resolve named black found in [python].resolves.
```

With following versions the `black` export works as expected:
- `2.17.0`
- `2.17.1rc1`
- `2.17.1rc2`
- `2.17.1rc3`