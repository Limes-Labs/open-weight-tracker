# Open Weight Tracker

Tracker of open-weight models and their relevance to European languages, institutions, and deployment constraints.

Before Europe can depend on open models, we need honest public tracking: what exists, what license it carries, what languages it supports, and how it performs on European tasks.

This repository is an inventory, not a leaderboard. It separates:

- factual release metadata, such as license, parameter count, and whether weights are available
- publisher claims, such as language coverage or benchmark scores
- Limes evaluation status, especially whether a model has run through [EuroBench](https://github.com/Limes-Labs/eurobench)

## What we will track

- Open weight model releases relevant to Europe
- Whether weights are actually downloadable
- License and deployment constraints
- European language coverage
- Evaluation links and EuroBench status
- Deployment notes and known limitations
- Source URLs and the date each entry was checked

## No endorsement or quality claim

Inclusion in this tracker does not mean Limes Labs endorses a model, recommends it for institutional use, or considers it safe, compliant, sovereign, high quality, or production ready.

External benchmark links are recorded as publisher or third-party claims unless they are reproduced by Limes Labs. Do not describe a model as passing, leading, recommended, rights-aware, or institution-ready unless the relevant EuroBench run is linked and the claim is supported by the recorded result.

## Repository map

- [TRACKER.md](TRACKER.md): human-readable inventory view
- [data/models.csv](data/models.csv): structured source-of-truth table
- [docs/schema.md](docs/schema.md): field definitions and allowed values
- [docs/source-policy.md](docs/source-policy.md): sourcing rules for contributions

## Status

Early. The schema and initial sourced entries are in place, with unknowns left explicit.

## How to contribute

1. Add or update a row in [data/models.csv](data/models.csv).
2. Include a stable `source_url` and current `date_checked`.
3. Keep claims narrow: quote the publisher's scope in notes, and use `unknown` when a field is not sourced.
4. Add EuroBench links only when a Limes-controlled or clearly reproducible run exists.
5. Keep [TRACKER.md](TRACKER.md) aligned with the CSV summary.

Join at [limeslabs.eu/join](https://limeslabs.eu/join)

## Links

- Website: [limeslabs.eu](https://limeslabs.eu)
- EuroBench: [github.com/Limes-Labs/eurobench](https://github.com/Limes-Labs/eurobench)
- Limes Constitution: [github.com/Limes-Labs/limes-constitution](https://github.com/Limes-Labs/limes-constitution)
