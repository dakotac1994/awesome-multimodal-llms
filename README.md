# Awesome Multimodal LLMs [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated directory of **multimodal large language models** — vision-language models, video-understanding models, and audio/speech-capable models — plus the **benchmarks, frameworks, and datasets** around them, as of **September 2026**.

**Verification confidence:** every entry is stamped ✅ **verified 2026-09-30** (existence and category checked on an official project page, vendor site, repository, model/dataset card, conference page, or arXiv). **Specs, scores, and claims are never guessed.** Machine-readable records live in [`data/multimodal-llms.json`](data/multimodal-llms.json) with a `verified` boolean plus `verified_date`/`verified_source` for every entry (`unverified_reason` is used whenever an entry can't be confirmed).

**69 entries** — all 69 verified on official sources as of 2026-09-30.

## 2026 Highlights

- **Open-weight VLMs caught up fast:** InternVL3, Qwen3-VL/Qwen2.5-VL, Molmo, Kimi-VL, MiniCPM-V 4.0, and Phi-4-multimodal made frontier-grade image understanding cheap to self-host.
- **Speech went full-duplex:** Kyutai's Moshi and LLaMA-Omni pushed real-time speech-to-speech dialogue; Qwen2-Audio paired voice chat with audio analysis.
- **Video evals matured:** Video-MME became the standard comprehensive video benchmark; LongVideoBench, MVBench, and EgoSchema stress long-context and temporal reasoning.
- **Audio evals arrived:** MMAU and OmniBench brought structured benchmarking to audio understanding and omni-modal reasoning.
- **One toolkit to run them:** lmms-eval and VLMEvalKit are the de-facto unified harnesses — if you run one benchmark, run it through one of these.

## Contents

- [Vision-language models](#vision-language-models)
- [Video-understanding models](#video-understanding-models)
- [Audio & speech models](#audio-speech-models)
- [Benchmarks & evals](#benchmarks-evals)
- [Frameworks & tooling](#frameworks-tooling)
- [Datasets](#datasets)
- [Guides](#guides)
- [Contributing](#contributing)
- [Related](#related)
- [License](#license)

---

## Vision-language models

Image-understanding LLMs — open-weight families and proprietary flagships.

- [GPT-5](https://platform.openai.com/docs/models) — ✅ verified 2026-09-30. OpenAI's flagship omni model with image and vision inputs alongside text and audio.
- [Gemini 3](https://deepmind.google/technologies/gemini/) — ✅ verified 2026-09-30. Google DeepMind's flagship multimodal family with native image, video, and audio understanding.
- [Claude Fable 5.1](https://www.anthropic.com/claude) — ✅ verified 2026-09-30. Anthropic's flagship model line with strong image and document understanding.
- [Grok 4.7](https://x.ai) — ✅ verified 2026-09-30. xAI's flagship model with image understanding alongside text reasoning.
- [LLaVA / LLaVA-NeXT](https://llava-vl.github.io/) — ✅ verified 2026-09-30. Pioneering open-source vision-language assistant connecting a vision encoder to an LLM; 1.5 and NeXT (1.6) generations.
- [LLaVA-OneVision](https://github.com/LLaVA-VL/LLaVA-NeXT) — ✅ verified 2026-09-30. Open single-sight model handling single images, multi-image, and video in one architecture.
- [InternVL3](https://huggingface.co/OpenGVLab/InternVL3-8B) — ✅ verified 2026-09-30. OpenGVLab's open multimodal family with strong image and video understanding.
- [Qwen3-VL](https://huggingface.co/Qwen/Qwen3-VL-8B-Instruct) — ✅ verified 2026-09-30. Alibaba's Qwen vision-language family for image and video understanding.
- [Molmo](https://huggingface.co/allenai/Molmo-7B-D-0924) — ✅ verified 2026-09-30. Ai2's open vision-language model family with strong grounding; Apache 2.0 weights.
- [Aria](https://github.com/rhymes-ai/Aria) — ✅ verified 2026-09-30. Open multimodal-native mixture-of-experts model from Rhymes AI.
- [NVLM 1.0](https://huggingface.co/nvidia/NVLM-D-72B) — ✅ verified 2026-09-30. NVIDIA's open frontier-class multimodal LLM family.
- [Pixtral 12B](https://mistral.ai/news/pixtral-12b/) — ✅ verified 2026-09-30. Mistral's open image/document vision-language model.
- [Janus-Pro](https://huggingface.co/deepseek-ai/Janus-Pro-7B) — ✅ verified 2026-09-30. DeepSeek's unified model for multimodal understanding and image generation.
- [Kimi-VL](https://github.com/MoonshotAI/Kimi-VL) — ✅ verified 2026-09-30. Moonshot AI's open MoE vision-language model for multimodal reasoning over images and video.
- [MiniCPM-V 4.0](https://github.com/openbmb/minicpm-v/blob/HEAD/docs/minicpm_v4_en.md) — ✅ verified 2026-09-30. OpenBMB's efficient open vision-language model for single/multi-image and video.
- [Phi-4-multimodal](https://huggingface.co/microsoft/Phi-4-multimodal-instruct) — ✅ verified 2026-09-30. Microsoft's small multimodal model combining speech, vision, and text in one checkpoint.
- [CogVLM2](https://github.com/THUDM/CogVLM2) — ✅ verified 2026-09-30. Tsinghua/Zhipu open visual-language model family for image and video understanding.
- [BLIP-2](https://github.com/salesforce/LAVIS) — ✅ verified 2026-09-30. Salesforce's bootstrapped vision-language pre-training approach; code lives in the LAVIS library.
- [PaliGemma 2](https://huggingface.co/google/paligemma2-3b-pt-224) — ✅ verified 2026-09-30. Google's open vision-language model family pairing SigLIP vision with Gemma.
- [SmolVLM](https://huggingface.co/blog/smolvlm) — ✅ verified 2026-09-30. Hugging Face's tiny open vision-language models designed for on-device and edge use.
- [Florence-2](https://huggingface.co/microsoft/Florence-2-large) — ✅ verified 2026-09-30. Microsoft's compact vision foundation model for captioning, detection, grounding, and OCR.
- [Idefics3](https://huggingface.co/HuggingFaceM4/Idefics3-8B-Llama3) — ✅ verified 2026-09-30. Hugging Face's open vision-language model with strong document and multi-image understanding.
- [Gemma 3](https://deepmind.google/technologies/gemma/) — ✅ verified 2026-09-30. Google's open-weight model family with vision understanding in its multimodal variants.
- [Llama 4](https://www.llama.com/) — ✅ verified 2026-09-30. Meta's open-weight multimodal model family with native image understanding.
- [Qwen2.5-VL](https://github.com/QwenLM/Qwen2.5-VL) — ✅ verified 2026-09-30. Alibaba's open vision-language model for image, document, and video understanding.

## Video-understanding models

Models that natively consume video frames/clips.

- [LLaVA-Video (Video-LLaVA)](https://huggingface.co/docs/transformers/v4.45.2/en/model_doc/video_llava) — ✅ verified 2026-09-30. Unified visual representation for joint image and video understanding.
- [LLaVA-NeXT-Video](https://llava-vl.github.io/blog/2024-04-30-llava-next-video/) — ✅ verified 2026-09-30. Zero-shot video understanding extension of LLaVA-NeXT via the AnyRes technique.
- [InternVideo2.5](https://github.com/OpenGVLab/InternVideo) — ✅ verified 2026-09-30. OpenGVLab's video foundation model family for understanding and generation research.
- [VideoChat2](https://github.com/OpenGVLab/Ask-Anything) — ✅ verified 2026-09-30. Chat-centric video understanding model from Shanghai AI Laboratory.
- [LongVA](https://github.com/EvolvingLMMs-Lab/LongVA) — ✅ verified 2026-09-30. Long-video understanding model extending context to thousands of frames.

## Audio & speech models

Speech-to-speech, audio understanding, and audio-language models.

- [Moshi](https://github.com/kyutai-labs/moshi) — ✅ verified 2026-09-30. Kyutai's real-time full-duplex speech-to-speech dialogue model.
- [LLaMA-Omni](https://huggingface.co/ICTNLP/Llama-3.1-8B-Omni) — ✅ verified 2026-09-30. Speech-language model generating text and speech responses from spoken instructions.
- [Qwen2-Audio](https://github.com/QwenLM/Qwen2-Audio) — ✅ verified 2026-09-30. Alibaba's large audio-language model for voice chat and audio analysis.
- [Whisper](https://github.com/openai/whisper) — ✅ verified 2026-09-30. OpenAI's open speech-recognition model; the audio encoder backbone for many speech LLMs.

## Benchmarks & evals

Published multimodal benchmarks across image, video, and audio.

- [MMMU](https://mmmu-benchmark.github.io/) — ✅ verified 2026-09-30. Massive multi-discipline multimodal understanding benchmark across college-level subjects.
- [MMBench](https://github.com/open-compass/MMBench) — ✅ verified 2026-09-30. Bilingual multi-dimension benchmark for vision-language model abilities.
- [MM-Vet](https://arxiv.org/abs/2308.02490) — ✅ verified 2026-09-30. Integrated evaluation of core vision-language capabilities on complex tasks.
- [MathVista](https://mathvista.github.io/) — ✅ verified 2026-09-30. Visual math reasoning benchmark combining diagrams, charts, and figures.
- [ChartQA](https://arxiv.org/abs/2203.10244) — ✅ verified 2026-09-30. Question answering over real-world charts requiring visual and logical reasoning.
- [DocVQA](https://www.docvqa.org/) — ✅ verified 2026-09-30. Document visual question answering over scanned and born-digital documents.
- [TextVQA](https://textvqa.org/) — ✅ verified 2026-09-30. VQA requiring reading and reasoning about text in images.
- [RealWorldQA](https://huggingface.co/datasets/xai-org/RealworldQA) — ✅ verified 2026-09-30. Real-world physical spatial understanding QA over everyday images.
- [MMStar](https://github.com/MMStar-Benchmark/MMStar) — ✅ verified 2026-09-30. Vision-indispensable multimodal benchmark minimizing text-only shortcuts.
- [Video-MME](https://github.com/MME-Benchmarks/Video-MME) — ✅ verified 2026-09-30. Comprehensive video analysis benchmark covering durations, subtitles, and audio.
- [LongVideoBench](https://github.com/longvideobench/LongVideoBench) — ✅ verified 2026-09-30. Long-context interleaved video-language understanding benchmark.
- [MVBench](https://github.com/OpenGVLab/Ask-Anything/blob/main/video_chat2/MVBENCH.md) — ✅ verified 2026-09-30. Multi-task video benchmark: 20 temporal understanding tasks spanning perception to cognition.
- [EgoSchema](https://github.com/EgoSchema/EgoSchema) — ✅ verified 2026-09-30. Long-form egocentric video understanding benchmark.
- [MMAU](https://iclr.cc/virtual/2025/poster/29528) — ✅ verified 2026-09-30. Massive multi-task audio understanding and reasoning across speech, sounds, and music.
- [OmniBench](https://github.com/ceilingfan456/omnibench) — ✅ verified 2026-09-30. Omnilingual omni-modal benchmark mixing image, audio, and text reasoning.

## Frameworks & tooling

Serving engines, fine-tuning frameworks, eval toolkits, and dataset tooling.

- [VLMEvalKit](https://github.com/open-compass/VLMEvalKit) — ✅ verified 2026-09-30. Open-source evaluation toolkit for large vision-language models.
- [lmms-eval](https://github.com/EvolvingLMMs-Lab/lmms-eval) — ✅ verified 2026-09-30. Unified evaluation framework for multimodal LLMs across image, video, and audio.
- [Hugging Face Transformers](https://github.com/huggingface/transformers) — ✅ verified 2026-09-30. Reference implementations and pipelines for vision, video, and audio-language models.
- [vLLM](https://github.com/vllm-project/vllm) — ✅ verified 2026-09-30. High-throughput serving engine with multimodal (image/audio) model support.
- [SGLang](https://github.com/sgl-project/sglang) — ✅ verified 2026-09-30. Fast serving framework with multimodal model support.
- [LMDeploy](https://github.com/InternLM/lmdeploy) — ✅ verified 2026-09-30. Model deployment toolkit with vision-language model support.
- [LLaMA-Factory](https://github.com/hiyouga/LLaMA-Factory) — ✅ verified 2026-09-30. Fine-tuning framework with multimodal (image/video/audio) training support.
- [FiftyOne](https://github.com/voxel51/fiftyone) — ✅ verified 2026-09-30. Dataset curation and visualization toolkit for vision and multimodal data.
- [LAVIS](https://github.com/salesforce/LAVIS) — ✅ verified 2026-09-30. Salesforce's library for language-vision intelligence research and applications.
- [Ollama](https://github.com/ollama/ollama) — ✅ verified 2026-09-30. Local model runner with support for open vision-language models.
- [OpenCompass](https://github.com/open-compass/opencompass) — ✅ verified 2026-09-30. General LLM evaluation platform covering multimodal benchmarks.

## Datasets

Notable image-text, video-text, and audio-text training/eval datasets.

- [COCO Captions](https://cocodataset.org/) — ✅ verified 2026-09-30. Large-scale image captioning dataset; a standard VLM pre-training and eval resource.
- [VQAv2](https://visualqa.org/) — ✅ verified 2026-09-30. Open-ended visual question answering dataset balancing language priors.
- [LAION-5B](https://laion.ai/) — ✅ verified 2026-09-30. Billion-scale open image-text dataset behind open CLIP and diffusion-era VLMs.
- [DataComp](https://www.datacomp.ai/) — ✅ verified 2026-09-30. Benchmark-driven dataset design competition for multimodal (CLIP-style) training data.
- [Visual Genome](https://arxiv.org/abs/1602.07332) — ✅ verified 2026-09-30. Dense image annotations: objects, attributes, relationships, and region descriptions.
- [ShareGPT4V](https://sharegpt4v.github.io) — ✅ verified 2026-09-30. 1.2M high-detail image captions bootstrapped from GPT-4V for VLM training.
- [InternVid](https://github.com/OpenGVLab/InternVideo/tree/main/Data/InternVid) — ✅ verified 2026-09-30. Millions of videos with LLM-generated multi-scale descriptions for video-text learning.
- [WavCaps](https://github.com/XinhaoMei/WavCaps) — ✅ verified 2026-09-30. Roughly 400K weakly-labelled audio clips with ChatGPT-cleaned captions.
- [AudioSet](https://research.google.com/audioset/) — ✅ verified 2026-09-30. Large ontology-labeled audio event dataset sourced from YouTube videos.

## Guides

- [Choosing a multimodal model](docs/choosing-a-multimodal-model.md) — match model to modality, latency, and budget.
- [Benchmark notes](docs/benchmark-notes.md) — what each benchmark actually measures, and how to read the scores.
- [Glossary](docs/glossary.md) — VLM, VQA, AnyRes, full-duplex, and other terms used in this list.
- [Status changes](docs/status-changes.md) — retirements, renames, and major releases (newest first).

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). One entry = one bullet + one JSON record; link the official source; tag verification honestly.

## Related

More curated LLM guides from [Awesome-llms-labs](https://github.com/awesome-llms-labs):

- [decision-making LLMs](https://github.com/awesome-llms-labs/awesome-decisions-llms)
- [inference-speed LLMs](https://github.com/awesome-llms-labs/awesome-fast-llms)
- [flagship LLMs](https://github.com/awesome-llms-labs/awesome-flagship-llms)
- [cost-efficient Flash-class LLMs](https://github.com/awesome-llms-labs/awesome-flash-llms)
- [free LLMs](https://github.com/awesome-llms-labs/awesome-free-llms)
- [AI agents](https://github.com/awesome-llms-labs/awesome-ai-agents)
- [AI sandboxes](https://github.com/awesome-llms-labs/awesome-ai-sandboxes)
- [Jev](https://github.com/awesome-llms-labs/awesome-jev)
- [microVMs](https://github.com/awesome-llms-labs/awesome-microVM)

## License

MIT — see [LICENSE](LICENSE).
