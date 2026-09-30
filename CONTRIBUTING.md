# Contributing

Thanks for helping keep this the most current directory of multimodal LLMs, their benchmarks, and the tooling around them!

## Adding an entry

1. **Check it fits:** a model that natively consumes a non-text modality (image, video, audio/speech), a published multimodal benchmark or eval, a framework/tool for building or evaluating multimodal systems, or a notable multimodal dataset. A PR must point at a primary source: the project's official page, vendor docs, repository, model/dataset card, conference page, or arXiv paper.
2. **Add to the right section** of `README.md`:
   - Vision-language models → image-understanding LLMs (open-weight or proprietary)
   - Video-understanding models → models that natively consume video
   - Audio & speech models → speech-to-speech, audio understanding, audio-language models
   - Benchmarks & evals → published multimodal benchmarks
   - Frameworks & tooling → serving engines, fine-tuning frameworks, eval toolkits, dataset tooling
   - Datasets → image-text, video-text, and audio-text training/eval datasets
3. **One entry = one bullet.** Format:
   `- [Name](https://official-source) — ✅ verified 2026-09-30. ` one-line description.
   Tag verification honestly: write `✅ verified <date>` only when you checked the entry's existence and category on an official source yourself; otherwise mark it `⚠️ unverified` and add the reason inline.
4. **Add the matching record** to `data/multimodal-llms.json` with these exact fields:

| field | type | values |
|---|---|---|
| `name` | string | model / benchmark / tool / dataset name |
| `vendor` | string | vendor / organization / team |
| `url` | string | official https:// URL |
| `description` | string | one sentence |
| `category` | string | `vision-language-model` / `video-model` / `audio-speech-model` / `benchmark` / `tooling` / `dataset` |
| `verified` | bool | `true` only if you checked an official source yourself |
| `verified_date` | string | required when `verified` is true, e.g. `"2026-09-30"` |
| `verified_source` | string | required when `verified` is true — the official source you read |
| `unverified_reason` | string | required when `verified` is false — why it couldn't be confirmed |

5. **Status changes:** if a model is retired, renamed, or a benchmark is superseded, update its README entry *and* add a row (newest-first) to `docs/status-changes.md`.

## Style rules

- Link the **official source** (project page, vendor docs, repo, model card), never a blog roundup or reseller.
- Facts that can change (model versions, benchmark scores, dataset sizes) get "as of" context in prose or are omitted — link the source instead of hard-coding numbers that rot.
- Vendor claims stay labeled as vendor claims ("vendor claims", "reported by community sources").
- Entries verified in the README are stamped with their verification date; never guess a spec, score, or claim.
- Keep README descriptions to one entry per bullet; put depth in `docs/`.

## CI

Every PR runs:
- **Link check** (lychee) over all markdown files — no dead links.
- **JSON validation** — `data/multimodal-llms.json` must parse, every record must have the required fields, `category` must be from the allowed set, verified entries need `verified_date` + `verified_source`, and unverified entries need `unverified_reason`.

Run locally before pushing:

```bash
python3 -c "import json; json.load(open('data/multimodal-llms.json')); print('ok')"
```
