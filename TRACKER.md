# European Open-Weight Model Tracker

> Maintained by [Limes Labs](https://limeslabs.eu). Last updated: 2026-06-17.

This is a public inventory for contributors planning evaluations, fine-tunes, and European deployments. It is not a leaderboard and it is not an endorsement list.

The structured source of truth is [data/models.csv](data/models.csv). This Markdown view highlights the current seed entries and the review standard for future additions.

## Tracker fields

Each entry records model identity, release metadata, whether weights are available, licensing, context length, European language notes, training-data transparency, external evaluation links, EuroBench status, safety and deployment notes, and source provenance.

See [docs/schema.md](docs/schema.md) for field definitions and [docs/source-policy.md](docs/source-policy.md) for sourcing rules.

## Current inventory

| Model | Org | Weights | License | Parameters | Context | Languages claimed | EuroBench status | Source checked |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Mixtral 8x7B Instruct v0.1 | Mistral AI | yes | Apache-2.0 | 46.7B total / 12.9B active | 32k tokens | English, French, German, Spanish, Italian | not_run | 2026-06-17 |
| Mistral NeMo Instruct 2407 | Mistral AI and NVIDIA | yes | Apache-2.0 | 12B | 128k tokens | English, French, German, Spanish, Italian, Portuguese, Chinese, Japanese, Korean, Arabic, Hindi | not_run | 2026-06-17 |
| Poro 34B | LumiOpen / Silo AI / TurkuNLP / HPLT | yes | Apache-2.0 | 34.2B | 2048 tokens | Finnish, English, code | not_run | 2026-06-17 |
| SmolLM2 1.7B Instruct | Hugging Face TB | yes | Apache-2.0 | 1.7B | unknown | English | not_run | 2026-06-17 |

## Evaluation hooks

Planned Limes evaluation dimensions for European models:

1. Multilingual institutional prose in languages such as Italian, French, German, Spanish, Polish, Finnish, and other EU languages as coverage grows.
2. Rights-aware QA for GDPR, AI Act, procurement, public-service, and citizen-facing scenarios.
3. Refusal quality on dual-use prompts without over-refusal on benign administrative tasks.
4. Constitutional alignment using the [Limes Constitution](https://github.com/Limes-Labs/limes-constitution) rubric.
5. Citation honesty, including detection of fabricated legal articles, standards, and institutional references.

## Contribution checklist

- Add or update the row in [data/models.csv](data/models.csv).
- Include at least one stable `source_url` for the row.
- Set `date_checked` to the date you personally checked the source.
- Use `unknown` where the source does not support a field.
- Keep publisher claims in `languages_claimed`, `training_data_transparency`, `eval_links`, `safety_notes`, or `deployment_notes`; do not turn them into Limes quality claims.
- Set `eurobench_status` to `not_run` unless a EuroBench result is linked.

## Watchlist

Candidate rows still need source review before they should be added to the CSV: OpenEuroLLM releases, additional Mistral open-weight releases, Pleias releases, Kyutai releases, Polish and Baltic sovereign models, Italian domain models, and public-sector fine-tunes.
