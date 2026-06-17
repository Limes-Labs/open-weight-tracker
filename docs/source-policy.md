# Source policy

The tracker is only useful if contributors can tell which facts are verified, which statements are publisher claims, and which results come from Limes evaluation.

## Minimum source rule

Every row in [../data/models.csv](../data/models.csv) must include:

- `source_url`: a stable URL supporting the row
- `date_checked`: the date the contributor checked that source
- `unknown` for any field not supported by the source

Rows without source URLs should not be merged except as explicitly marked examples in documentation.

## Preferred sources

Use primary sources first:

- official model cards, such as Hugging Face or organization-hosted cards
- official release posts
- official papers or technical reports
- official GitHub repositories
- license files or acceptable-use policy pages

Use secondary sources only when the primary source is unavailable, and say so in the relevant notes field. Do not use social media, press articles, or leaderboard entries as the only source for licensing, weight availability, safety, or deployment claims.

## Claims and evaluation

Keep these categories separate:

- Facts: release date, license, downloadable weights, parameter count, context length when directly sourced.
- Publisher claims: languages, benchmark scores, safety statements, training-data descriptions, deployment suitability.
- Limes evaluation: EuroBench runs or Limes Constitution assessments performed by Limes or in a reproducible Limes-controlled workflow.

External evaluations may be useful evidence, but they are not EuroBench results. Leave `eurobench_status` as `not_run` unless a EuroBench result exists.

## Updating existing rows

When updating a row:

1. Re-check the primary source.
2. Update `date_checked`.
3. Keep old claims only if the source still supports them.
4. Move uncertainty into notes instead of strengthening the wording.
5. Mention any major change in the PR description, especially license, weight access, or EuroBench status changes.

## Institutional caution

The tracker does not provide legal advice, AI Act compliance determinations, GDPR compliance determinations, procurement approval, security certification, or deployment endorsement. It is a transparency aid for further review.
