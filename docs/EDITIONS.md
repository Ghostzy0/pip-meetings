# Pip Meetings edition map

This custom repository publishes exactly the three editions listed in `distribution.json`. The default is `pip` (Pip Core).

| Variant | Product name | Default |
| --- | --- | --- |
| `baseline-enhanced` | Neutral Plus |  |
| `pip` | Pip Core | Default |
| `pip-enhanced` | Pip Plus |  |

## Build

```sh
scripts/test-native.sh
scripts/build-native.sh
scripts/build-native.sh baseline-enhanced
scripts/build-native.sh pip-enhanced
```

The three editions share the local meeting workflow and engine. Neutral Plus and Pip Plus include the same enhanced Open actions view; Pip Core is the non-enhanced Pip edition. Separate bundle identities mean grants and local data are not shared. See [public verification](../PUBLIC-VERIFICATION.md) for evidence and limitations.

`SOURCE-PROVENANCE.json` identifies this product and records the shared-engine digest, exact source-input manifest hashes and public-file manifest hash without a private repository origin or revision.
