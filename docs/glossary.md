# Glossary

Terms used across this list.

- **VLM (vision-language model)** — a language model that also accepts images as input, typically via a vision encoder (e.g. CLIP/SigLIP ViT) connected to the LLM through a projector or cross-attention.
- **MLLM** — multimodal LLM; the broader term covering vision, video, and audio inputs.
- **VQA (visual question answering)** — answering natural-language questions about an image; the classic VLM eval task (VQAv2, TextVQA, DocVQA).
- **Grounding / referring expression** — locating the image region a phrase refers to (bounding boxes or masks); Molmo and Florence-2 are strong here.
- **OCR** — optical character recognition; reading text in images/documents. Dominates DocVQA and chart/document workloads.
- **AnyRes** — LLaVA-NeXT's technique of splitting high-resolution images into grids of crops so the model sees fine detail; it generalizes naturally to video frames (LLaVA-NeXT-Video).
- **Full-duplex (speech)** — talking and listening simultaneously, like a phone call; Moshi's headline capability, versus half-duplex turn-taking.
- **Voice chat vs. audio analysis** — Qwen2-Audio's two modes: free-form spoken conversation without typed prompts, versus structured analysis of audio given text instructions.
- **Vision-indispensable** — a benchmark design goal (MMStar): questions must require the image, filtering out ones solvable from text alone.
- **Temporal reasoning** — understanding *change over time* in video (order, causality, motion), as opposed to describing individual frames; what MVBench isolates.
- **Long-context video** — handling minutes-to-hours of video (thousands of frames); tested by LongVideoBench and EgoSchema, enabled by models like LongVA.
- **Omni-modal / omni model** — a single model handling text, image, video, and audio (e.g. GPT-5, Gemini 3, Phi-4-multimodal).
- **Captioning** — generating text descriptions of images/audio/video; the pre-training task behind COCO Captions, ShareGPT4V, WavCaps, and InternVid.
- **Weakly-labelled** — training data with noisy, automatically-generated labels (WavCaps) rather than human annotation; cheaper at scale, noisier per sample.
- **lm-evaluation-harness analogue** — lmms-eval is to multimodal models what EleutherAI's lm-evaluation-harness is to text models: the standard unified eval runner.
