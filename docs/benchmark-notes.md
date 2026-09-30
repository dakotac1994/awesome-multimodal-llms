# Benchmark Notes

What the [benchmarks](../README.md#benchmarks--evals) in this list actually measure — and how to read their scores without fooling yourself.

## Image / document understanding

- **MMMU** — college-level, multi-discipline questions requiring domain knowledge plus vision. The closest thing to a "general intelligence" VLM test; hard to game with text-only shortcuts.
- **MMBench** — bilingual (EN/CN), multi-ability breakdown (perception vs. reasoning). Good for diagnosing *which* capability fails.
- **MM-Vet** — complex integrated tasks combining recognition, OCR, spatial reasoning, and math. Favors models with tool-like compositional skills.
- **MMStar** — deliberately "vision-indispensable": questions solvable from text alone were filtered out. Use it to check whether a model actually looks at the image.
- **MathVista** — math with visual context (diagrams, plots, figures). Tests whether the vision encoder preserves the detail math needs.
- **ChartQA** — real-world charts; requires reading values off axes and doing arithmetic. A practical proxy for BI/dashboard workloads.
- **DocVQA** — document images (scans, PDFs). OCR quality dominates here.
- **TextVQA** — reading text *in* natural images (signs, labels). Different failure mode from DocVQA: scene text, not documents.
- **RealWorldQA** — everyday physical/spatial questions. Small but grounded; good sanity check for embodied/robotics use.

## Video

- **Video-MME** — the broadest video benchmark: short/medium/long durations, with and without subtitles/audio. Start here for general video capability.
- **LongVideoBench** — long-context interleaved video+text. Tests whether the model can find a needle in a long video, not just summarize clips.
- **MVBench** — image tasks converted to video to isolate *temporal* understanding. If a model aces image VQA but flops MVBench, its video handling is frame-stacking, not temporal reasoning.
- **EgoSchema** — long egocentric videos with narrative-level questions. Hard; near-human performance is still rare.

## Audio

- **MMAU** — speech, environmental sounds, and music across understanding and reasoning tasks. The audio analogue of an MMLU-style suite.
- **OmniBench** — mixes image, audio, and text in single questions. The only benchmark here that tests cross-modal fusion directly.

## Reading scores honestly

1. **Scores rot.** Benchmark versions change; always check which split/version a reported number used.
2. **Vendor-reported ≠ independent.** Prefer numbers reproduced through lmms-eval or VLMEvalKit with published configs.
3. **Saturation is real.** On older benchmarks (VQAv2, COCO Captions) top models cluster within noise — use harder suites (MMMU, MMStar, Video-MME) to separate them.
4. **Match the benchmark to the task.** A chart-reading product should be chosen on ChartQA/DocVQA numbers, not MMMU rank.
