# Choosing a Multimodal Model

How to pick from the [vision-language](../README.md#vision-language-models), [video](../README.md#video-understanding-models), and [audio](../README.md#audio--speech-models) models in this list.

## 1. Start with the modality you actually need

- **Images / documents / charts** → a vision-language model (VLM). Almost every entry in the vision-language section handles single images; document-heavy work favors models with strong OCR (Pixtral 12B, Idefics3, Florence-2, proprietary flagships).
- **Multi-image or interleaved image+text** → LLaVA-OneVision, Idefics3, or the larger open families (InternVL3, Qwen2.5-VL).
- **Video** → use a video-native model (LLaVA-NeXT-Video, InternVideo2.5, LongVA) rather than sampling frames into an image VLM — temporal reasoning benchmarks (MVBench, EgoSchema) exist precisely because frame-stacking underperforms.
- **Speech in / speech out** → full-duplex dialogue (Moshi) or speech-instruction models (LLaMA-Omni); for transcription plus analysis, Qwen2-Audio.
- **Speech + vision + text in one checkpoint** → Phi-4-multimodal.

## 2. Open-weight vs. proprietary

- **Prototype on proprietary APIs** (GPT-5, Gemini 3, Claude) when you need the best zero-shot quality and don't want infra work.
- **Ship on open weights** (LLaVA-NeXT, InternVL3, Qwen2.5-VL, Molmo 2, Kimi-VL, MiniCPM-V 4.0) when you need cost control, on-prem deployment, or fine-tuning. Serve with vLLM, SGLang, LMDeploy, or Ollama.
- **Edge / on-device** → SmolVLM, Florence-2, MiniCPM-V 4.0, or the small Qwen variants.

## 3. Evaluate before you commit

Don't pick on vibes: run your shortlist through [lmms-eval](https://github.com/EvolvingLMMs-Lab/lmms-eval) or [VLMEvalKit](https://github.com/open-compass/VLMEvalKit) on the benchmarks closest to your task (see [benchmark notes](benchmark-notes.md)). A model that tops MMMU can still fumble your chart-reading workload.

## 4. Honesty rules for this list

- ✅ entries were checked on an official source on the stamped date (all 69 verified as of 2026-09-30); any ⚠️ entry was not — treat its description as a lead, not a fact.
- This list tracks **existence and category**, not leaderboard positions. Scores rot; the linked official sources are the authority.
