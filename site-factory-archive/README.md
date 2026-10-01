# Optional Theme Archive

Full themes are **not** stored automatically.

Before starting a new site's BUILD, the assistant asks whether to archive the previous completed working theme.

Only when the user answers **yes**, store:

```text
site-factory-archive/<domain>/<version>/
  theme.zip
  build-manifest.json
  qa.json
```

If the user answers **no**, no theme archive is created.

Structural anti-repeat history is separate and remains mandatory.
