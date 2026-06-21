# SPECTER — Public Documentation & Schemas

**© 2025 Tech Javelin, Ltd.**

This repository contains public-facing documentation and validation schemas for the [SPECTER](https://techjavelin.com) forensic acquisition toolkit.

## Contents

| Path | Description |
|------|-------------|
| `schemas/specter-manifest.schema.json` | JSON Schema for `specter-manifest.json` — the chain-of-custody manifest |

## Schema Versioning

Each tagged release of this repo corresponds to a SPECTER release. The schema at tag `v1.0.0` validates manifests produced by SPECTER `v1.0.0`.

The manifest's `specter_version` field identifies which schema version to validate against.

## Usage

Fetch the schema for a specific version:

```
https://raw.githubusercontent.com/techjavelin/specter-docs/v1.0.0/schemas/specter-manifest.schema.json
```

Or via the GitHub API:

```
GET https://api.github.com/repos/techjavelin/specter-docs/contents/schemas/specter-manifest.schema.json?ref=v1.0.0
```

## License

The schemas and documentation in this repository are provided for use with SPECTER. All rights reserved.
