# European Open-Weight Model Tracker

> Maintained by [Limes Labs](https://limeslabs.eu). Last updated: June 2026.

Tracks **European-headquartered or EU-sovereignty-positioned** models with meaningful open weights or open research releases. Not a leaderboard — a **public inventory** for contributors planning evals, fine-tunes, and deployment.

**Methodology:** company disclosures, Hugging Face model cards, EU policy reports, [European Open Source AI Index](https://osai-index.eu/), press. "Open-weight" ≠ fully open training data.

---

## Legend

| Tag | Meaning |
| --- | --- |
| 🟢 Apache/MIT | Permissive license for weights |
| 🟡 Custom / research | Restricted commercial or research-only terms |
| 🔴 API-only | No public weights |
| 🇪🇺 HQ | EU headquarters |
| 🏛️ Sovereign | Explicit public-sector / regulated-industry positioning |

---

## Frontier & large models

| Model | Org | 🇪🇺 | License | Params | Notes |
| --- | --- | --- | --- | --- | --- |
| Mistral Large 3 | Mistral AI (FR) | 🇪🇺 | 🟡 Custom / partial open | 675B MoE | European anchor lab; ASML strategic investment 2026 |
| Mixtral 8x22B | Mistral AI | 🇪🇺 | 🟢 Apache 2.0 | 141B total | Widely used sovereign fine-tune base |
| Mistral Small 3.2 | Mistral AI | 🇪🇺 | 🟢 Apache 2.0 | 24B | Strong EU enterprise self-host candidate |
| Mistral Nemo | Mistral + NVIDIA | 🇪🇺 | 🟢 Apache 2.0 | 12B | Multilingual |
| Pharia-1 / Pharia-1-LLM-7B | Aleph Alpha (DE) | 🇪🇺 🏛️ | 🟡 Enterprise | 7B–70B | Sovereign enterprise; Cohere merger announced Apr 2026 — verify status |
| Luminous series | Aleph Alpha | 🇪🇺 | 🟡 | Various | Older open research releases |
| Viking 33B / Poro | Silo AI / AMD (FI) | 🇪🇺 | 🟢 Apache 2.0 | 7–33B | OpenEuroLLM co-lead |
| EuroLLM (preview) | OpenEuroLLM consortium | 🇪🇺 | 🟢 Target | 1.7–9B+ | All EU languages; mid-2026 first releases |
| LightOn Alfred / Paradigm | LightOn (FR) | 🇪🇺 🏛️ | 🟡 | 7–40B | Document / enterprise |
| TildeOpen LLM | Tilde (LV) | 🇪🇺 | 🟢 Open | 30B | Trained on **LUMI** (2M GPU hours, 2025) |

---

## Mid-size & specialist

| Model | Org | License | Focus |
| --- | --- | --- | --- |
| Pleias 1.0 | Pleias (FR) | Public domain / fully open data claim | Strict open-data positioning |
| Moshi | kyutai (FR) | Open research | Real-time voice |
| Helium | kyutai | Open research | Text |
| SmolLM2 | Hugging Face (FR HQ) | 🟢 Apache 2.0 | Edge / efficient |
| vAIst-IT-7B | Var Group (IT) | 🟢 Open-weight | Italian |
| BgGPT | Bulgaria | Mistral-derived sovereign | Regional |
| PLLuM | Poland | Sovereign Polish LLM | From-scratch national build |
| Bielik | Poland | 🟢 Open | Polish sovereign |
| Apertus | Switzerland | Open-weight | Multilingual Swiss release |
| ALIA | Spain | Sovereign | Spanish public initiative |

---

## Code & multimodal (European labs)

| Model | Org | Notes |
| --- | --- | --- |
| Codestral | Mistral | Code generation |
| Pixtral | Mistral | Vision-language |
| Holo2 | H Company (FR) | Computer-use / GUI agents |
| OriOn | LightOn | Long-context document VLM |
| Stable LM / SD | Stability AI (UK/EU ops) | Mixed open weights |

---

## Infrastructure-dependent training (EuroHPC)

| Project | Compute | Outcome |
| --- | --- | --- |
| TildeOpen 30B | LUMI | Released open-weight LLM |
| OpenEuroLLM | BSC, SURF, LUMI (planned) | Consortium models 2026–2028 |
| Limes nanogpt experiments | Laptop → IT4LIA path | Char-level / small baseline — [limes-nanogpt](https://github.com/Limes-Labs/limes-nanogpt) |

---

## Watchlist (API-first but EU-relevant)

| Org | HQ | Notes |
| --- | --- | --- |
| DeepL | DE | Translation / writing; proprietary |
| Helsing | DE | Defence AI; proprietary |
| Poolside | FR | Code models; enterprise |
| Nyonic | DE | Sovereign preview |
| Cohere EU hub | UK/EU | Command R+; research/commercial mix |

---

## Evaluation hooks (eurobench)

Planned Limes eval dimensions for European models:

1. **Multilingual** — IT, FR, DE, ES, PL institutional prose
2. **Rights-aware QA** — GDPR / AI Act scenario questions
3. **Refusal quality** — dual-use prompts without over-refusal on benign PA tasks
4. **Constitutional alignment** — [limes-constitution](https://github.com/Limes-Labs/limes-constitution) rubric
5. **Citation honesty** — fabricated legal article detection

---

## Gaps & next updates

- [ ] Add release dates and Hugging Face repo links per row
- [ ] Track **OSAI Index** openness scores
- [ ] Separate **training data openness** column
- [ ] Monitor Aleph Alpha / Cohere merger impact on Pharia licensing
- [ ] Add Nordic (Silo/AMD, LUMI ecosystem) monthly diff

## Contribute

PRs welcome with: model name, org, license URL, weight link, date, one-line note + source.