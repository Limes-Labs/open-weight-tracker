# Tracker schema

The canonical tracker data lives in [../data/models.csv](../data/models.csv). Keep one row per model release or checkpoint family. When values differ between base, instruct, quantized, or fine-tuned variants, prefer a separate row.

Use `unknown` when a source does not support a field. Do not infer missing values from model names, rumors, third-party summaries, or benchmark leaderboards.

## Fields

| Field | Required | Description |
| --- | --- | --- |
| `model_name` | yes | Public model or checkpoint name. Include version when available. |
| `org` | yes | Releasing organization or collaboration. |
| `release_date` | yes | Public release date in `YYYY-MM-DD`, or `unknown` if not sourced. |
| `weights_available` | yes | `yes`, `partial`, `gated`, `no`, or `unknown`. Use `gated` when users must accept terms or request access before download. |
| `license` | yes | License identifier or short license name, such as `Apache-2.0`, `MIT`, `CC-BY-4.0`, `custom`, `research-only`, or `unknown`. |
| `license_notes` | yes | Short note about license scope, gating, redistribution, acceptable use policy, or uncertainty. |
| `parameters` | yes | Parameter count as sourced. For MoE models, include total and active parameters when both are available. |
| `context_length` | yes | Context window in tokens as an integer, or `unknown`. |
| `languages_claimed` | yes | Languages explicitly claimed by the publisher or model card. Separate values with semicolons. |
| `european_language_notes` | yes | Notes on European-language relevance, gaps, or caution. Keep performance claims tied to sources or EuroBench results. |
| `training_data_transparency` | yes | What the source discloses about pretraining, fine-tuning, data exclusions, licensing, or provenance. |
| `eval_links` | yes | Source URLs for external evaluations, model-card benchmark tables, papers, or `none`. These are not Limes endorsements. |
| `eurobench_status` | yes | `not_run`, `planned`, `in_progress`, `completed`, or `blocked`. Link results in notes or PR description when completed. |
| `safety_notes` | yes | Known safety limitations, moderation status, refusal policy, red-team notes, or `unknown`. |
| `deployment_notes` | yes | Practical constraints such as hardware, quantization, serving stack, gated access, on-prem suitability, or cloud/API-only limits. |
| `source_url` | yes | Primary source URL checked for the row. Prefer model cards, release posts, papers, or official repositories. |
| `date_checked` | yes | Date the contributor checked the source, in `YYYY-MM-DD`. |

## Interpreting status values

`weights_available` records access to model weights, not whether the model is "open source" in a broader sense. Training data, code, tokenizer, evaluation harnesses, and acceptable-use constraints should be described separately.

`eurobench_status` records Limes evaluation state only:

- `not_run`: no EuroBench run is known.
- `planned`: a run is intended but not started.
- `in_progress`: a run is underway.
- `completed`: a reproducible EuroBench result is linked.
- `blocked`: a run is blocked by missing weights, license constraints, hardware, tooling, or unclear provenance.

External benchmark links belong in `eval_links`; they do not change `eurobench_status`.

## CSV style

- Use UTF-8 CSV with a header row.
- Quote fields that contain commas.
- Prefer semicolons inside list-like cells.
- Keep each row to one physical line.
- Leave uncertainty visible with `unknown` instead of deleting columns.
