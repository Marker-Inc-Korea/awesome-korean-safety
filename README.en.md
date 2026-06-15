# 🛡️ Awesome Korean Safety [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

**🌐 Language:** [한국어](README.md) · **English**

An awesome list of **Korean LLM safety benchmarks & datasets**.

It curates benchmarks for evaluating LLMs on toxicity, social bias, hate speech, sensitive-question handling, red-teaming, and multimodal safety **within Korean language and cultural contexts**.
The format is inspired by [Awesome-LLM-Safety](https://github.com/ydyjya/Awesome-LLM-Safety) and [awesome-korean-llm](https://github.com/NomaDamas/awesome-korean-llm).

> ⚠️ The **Commercial use** column is based on the dataset license. Always verify the original LICENSE in each repository before use.
> ✅ Allowed (MIT · Apache · CC-BY · CC-BY-SA, etc.) / ❌ Not allowed (CC-BY-NC · NC-ND, closed or restricted release) / ❓ Unclear · contact required

---

## 🚀 Table of Contents

- [Values & Alignment](#-values--alignment)
- [Social Bias](#-social-bias)
- [Hate / Offensive / Toxicity](#-hate--offensive--toxicity)
- [Harmful Instruction, Red-teaming, Jailbreak & Guardrails](#-harmful-instruction-red-teaming-jailbreak--guardrails)
- [Multimodal Safety](#-multimodal-safety)
- [Multilingual (incl. Korean)](#-multilingual-incl-korean)
- [Domain-specific](#-domain-specific)
- [Leaderboards](#-leaderboards)
- [Contributing](#-contributing)

---

## 🧭 Values & Alignment

Evaluate how well a model aligns with Korean social values, common knowledge, and appropriate handling of sensitive questions.

| Name | Focus | Size | Creator | Venue (Year) | Commercial | Data |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| [KorNAT](https://aclanthology.org/2024.findings-acl.666/) | Social value & knowledge alignment | Social value 4K + knowledge 6K (≈10K MCQ) | KAIST · Selectstar · NIA | ACL 2024 (Findings) | ❓ | [🤗 HF](https://huggingface.co/datasets/jiyounglee0523/KorNAT) |
| [SQuARe](https://github.com/naver-ai/korean-safety-benchmarks) | Sensitive questions & responses | ≈49K questions + ≈42K responses | NAVER AI Lab | ACL 2023 | ✅ | [GitHub](https://github.com/naver-ai/korean-safety-benchmarks) |
| [Korean LLM Trustworthiness Benchmark](https://aihub.or.kr/aihubdata/data/view.do?dataSetSn=71760) | Trustworthiness (bias · ethics · factuality) | Large-scale (built 2023 / updated 2024.12) | NIA · MSIT | AI Hub (2023~) | ❓ | [AI Hub](https://aihub.or.kr/aihubdata/data/view.do?dataSetSn=71760) |

## ⚖️ Social Bias

Measure model bias toward social groups (gender, age, region, religion, etc.).

| Name | Focus | Size | Creator | Venue (Year) | Commercial | Data |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| [KoBBQ](https://github.com/naver-ai/KoBBQ) | Social-bias QA (Korean BBQ) | 268 templates / 76,048 samples (12 categories) | KAIST · NAVER AI Lab | TACL 2024 | ✅ | [GitHub](https://github.com/naver-ai/KoBBQ) |
| [KoSBi](https://github.com/naver-ai/korean-safety-benchmarks) | Social-bias sentence classification | ≈68K (context-sentence pairs) | NAVER AI Lab | ACL 2023 (Industry) | ✅ | [GitHub](https://github.com/naver-ai/korean-safety-benchmarks) |

## 💬 Hate / Offensive / Toxicity

Datasets for detecting and classifying hate, offensive, and toxic language — widely used for training/evaluating safety filters and guardrail models.

| Name | Focus | Size | Creator | Venue (Year) | Commercial | Data |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| [K-HATERS](https://github.com/ssu-humane/K-HATERS) | Hate speech (target · intensity) | 192,158 (news comments) | Soongsil Univ. (ssu-humane) | EMNLP 2023 (Findings) | ✅ | [GitHub](https://github.com/ssu-humane/K-HATERS) |
| [K-MHaS](https://github.com/adlnlp/K-MHaS) | Multi-label hate speech (8 classes) | 109,692 utterances | Univ. of Sydney · UWA | COLING 2022 | ✅ | [🤗 HF](https://huggingface.co/datasets/jeanlee/kmhas_korean_hate_speech) |
| [KOLD](https://github.com/boychaboy/KOLD) | Hierarchical offensive language | 40,429 (comments) | KAIST · Softly AI | EMNLP 2022 | ❓ | [GitHub](https://github.com/boychaboy/KOLD) |
| [AIHub Harmful Expression Detection](https://www.aihub.or.kr/aihubdata/data/view.do?dataSetSn=71833) | Harmful-expression detection (11 categories) | Large-scale (80% train / 20% test) | NIA · TTA | AI Hub | ❓ | [AI Hub](https://www.aihub.or.kr/aihubdata/data/view.do?dataSetSn=71833) |
| [AIHub Text Ethics Verification](https://aihub.or.kr/aihubdata/data/view.do?dataSetSn=558) | Unethical-sentence verification (7 categories) | 453,340 sentences / 132,807 conversation sets | Simsimi Inc. et al. · NIA | AI Hub 2021 | ❓ | [AI Hub](https://aihub.or.kr/aihubdata/data/view.do?dataSetSn=558) |
| [UnSmile](https://github.com/smilegate-ai/korean_unsmile_dataset) | Multi-label hate speech (10 labels) | 18,742 sentences | Smilegate AI | 2022 | ❌ | [GitHub](https://github.com/smilegate-ai/korean_unsmile_dataset) |
| [HateScore](https://github.com/sgunderscore/hatescore-korean-hate-speech) | Hate-speech robustness (neutral FP reduction) | ≈11K | Underscore | 2022 | ❓ | [GitHub](https://github.com/sgunderscore/hatescore-korean-hate-speech) |
| [APEACH](https://github.com/jason9693/APEACH) | Hate-speech eval set (crowd-generated) | ≈3.7K (eval set) | Kakao · Soongsil · SNU | EMNLP 2022 (Findings) | ✅ | [🤗 HF](https://huggingface.co/datasets/jason9693/APEACH) |
| [KODOLI](https://github.com/cardy20/KODOLI) | Fine-grained offensiveness (3 levels) | 3 offensiveness levels | Catholic Univ. of Korea | EACL 2023 (Findings) | ❓ | [GitHub](https://github.com/cardy20/KODOLI) |
| [KOTOX](https://github.com/leeyejin1231/KOTOX) | Obfuscated toxicity (deobfuscation·detox) | 3 difficulty levels (easy/normal/hard) | Yejin Lee et al. | arXiv 2025.10 | ❓ | [GitHub](https://github.com/leeyejin1231/KOTOX) |
| [BEEP!](https://github.com/kocohub/korean-hate-speech) | Hate/bias speech | 9,381 labeled (+ ≈2M unlabeled) | kocohub (Moon et al.) | ACL 2020 (SocialNLP WS) | ✅ | [GitHub](https://github.com/kocohub/korean-hate-speech) |
| [DKTC](https://github.com/tunib-ai/DKTC) | Threatening-conversation classification | ≈4K dialogues | TUNiB | 2022 | ❌ | [GitHub](https://github.com/tunib-ai/DKTC) |

> ℹ️ **KOTOX** (obfuscation, Lee et al.) and **KoTox** (harmful instruction, Byun et al.) are similarly named but distinct datasets.

## 🎯 Harmful Instruction, Red-teaming, Jailbreak & Guardrails

Datasets that elicit harmful/abusive model outputs (red-teaming / jailbreak) or are used for ethical tuning and guardrail training.
> 💡 Jailbreak-related data also appears outside this section: [CSRT](#-multilingual-incl-korean) (code-switching jailbreak), [XL-SafetyBench](#-multilingual-incl-korean) (country-grounded jailbreak), and [KSAFE-MM](#-multimodal-safety) (multimodal jailbreak).

| Name | Focus | Size | Creator | Venue (Year) | Commercial | Data |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| [CAGE / KoRSET](https://arxiv.org/abs/2602.20170) | Culturally adaptive red-teaming | KoRSET ≈7,161 prompts | SelectStar AI (Kim et al.) | arXiv 2026.02 | ❓ | [arXiv](https://arxiv.org/abs/2602.20170) |
| [EN-KO Jailbreak Prompts](https://koreascience.or.kr/article/JAKO202518939602628.page) | Jailbreak prompt classification | jailbreak 86,512 (+ benign 64,979 · harmful 26,480) | Soongsil Univ. · Iroun&Company (Park et al.) | KIISC Journal 2025 | ❓ | [Paper](https://koreascience.or.kr/article/JAKO202518939602628.page) |
| [KoTox](https://github.com/byunsj/KoTox-Korean-Toxic-Instruction-Dataset) | Harmful-instruction handling | 39K (instruction-output pairs) | Seoul National Univ. (Byun et al.) | NeurIPS 2023 (WS) | ✅ | [GitHub](https://github.com/byunsj/KoTox-Korean-Toxic-Instruction-Dataset) |
| [K-Guardrail](https://github.com/skan0779/korean-guardrail-dataset) | Agent guardrail eval (jailbreak·PII) | 320+ prompts | skan0779 (open-source) | GitHub 2025 | ❓ | [GitHub](https://github.com/skan0779/korean-guardrail-dataset) |
| [EVE (v1/v2)](https://arxiv.org/abs/2403.06537) | Misuse red-teaming (criminal advice) | v1 200 QA + v2 600 (precedent-based) | AAAI 2024 authors | AAAI 2024 | ❌ | [arXiv](https://arxiv.org/abs/2403.06537) |

## 🖼️ Multimodal Safety

Evaluate safety across multimodal inputs — image, video, audio — in addition to text.

| Name | Focus | Size | Creator | Venue (Year) | Commercial | Data |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| [AssurAI](https://huggingface.co/datasets/TTA01/AssurAI) | Multimodal risk eval (35 factors) | 11,480 instances | TTA · KAIST · Kakao, etc. | arXiv 2025.11 | ❌ | [🤗 HF](https://huggingface.co/datasets/TTA01/AssurAI) |
| [KSAFE-MM](https://arxiv.org/abs/2605.28013) | MLLM safety (jailbreak·cross-modal) | 14,135 samples (G: translated / C: Korea-specific) | Yongwoo Kim et al. | arXiv 2026.05 | ❓ | [arXiv](https://arxiv.org/abs/2605.28013) |

## 🌐 Multilingual (incl. Korean)

Multilingual safety benchmarks that **include Korean**. The Korean subset/translation can be used on its own.

| Name | Focus | Size | Creator | Venue (Year) | Commercial | Data |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| [XL-SafetyBench](https://arxiv.org/abs/2605.05662) | Country-grounded jailbreak·cultural sensitivity | 5,500 | AIM Intelligence · KT · Microsoft · BMW | arXiv 2026.05 | ❓ | [arXiv](https://arxiv.org/abs/2605.05662) |
| [PolyGuardPrompts](https://huggingface.co/datasets/ToxicityPrompts/PolyGuardPrompts) | Multilingual guardrail eval (17 languages) | 29,325 | PolyGuard authors | arXiv 2025.04 | ❓ | [🤗 HF](https://huggingface.co/datasets/ToxicityPrompts/PolyGuardPrompts) |
| [WildGuardMix-KO](https://huggingface.co/datasets/iknow-lab/wildguardmix-test-ko) | Korean translation of WildGuardMix | Test-KO ≈1.7K (+ translated train) | iknow-lab | 2024 | ✅ | [🤗 HF](https://huggingface.co/datasets/iknow-lab/wildguardmix-test-ko) |
| [CSRT](https://arxiv.org/abs/2406.15481) | Code-switching jailbreak (10 languages) | 315 queries | Yoo, Yang, Lee | arXiv 2024.06 | ❓ | [🤗 HF](https://huggingface.co/datasets/walledai/CSRT) |

## 🔬 Domain-specific

Safety datasets specialized for particular risk domains (factuality/hallucination, location privacy, suicide/self-harm, etc.).

| Name | Focus | Size | Creator | Venue (Year) | Commercial | Data |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| [K-HALU](https://github.com/J-Seo/K-HALU) | Hallucination · factuality detection | 2K+ samples | Korea Univ. (Seo & Lim) | ICLR 2025 | ❓ | [GitHub](https://github.com/J-Seo/K-HALU) |
| [KoreaGEO Bench](https://arxiv.org/abs/2506.03371) | Location-privacy VLM eval | 1,080 images | KoreaGEO authors | EMNLP 2025 | ❓ | [arXiv](https://arxiv.org/abs/2506.03371) |
| [Harmful Suicide Content Detection](https://arxiv.org/abs/2407.13942) | Harmful suicide content detection | Multimodal | (2024 study) | arXiv 2024.07 | ❌ | [arXiv](https://arxiv.org/abs/2407.13942) |

---

## 🏆 Leaderboards

| Name | Safety-related tasks | Operator | Notes |
| :---: | :---: | :---: | :---: |
| [Open Ko-LLM Leaderboard2](https://huggingface.co/spaces/upstage/open-ko-llm-leaderboard) | Ko-Harmlessness (bias · hate · sensitiveness · illegal), KorNAT-Social-Value, KorNAT-Knowledge | Upstage & NIA | Private eval set, comprehensive Korean LLM evaluation ([paper](https://arxiv.org/abs/2410.12445)) |

---

## 🤝 Contributing

Found incorrect info or a new Korean safety benchmark? PRs are always welcome!

- Add a row: `Name / Focus / Size / Creator / Venue / Commercial / Data`
- Please include both a **paper link** and a **data/code link** when possible.
- In-table ordering: **most recent → citation/usage frequency → venue prestige**.
- Base the commercial-use flag on the repository LICENSE (`✅ / ❌ / ❓`).
- Propose a new section if no category fits.

> ⚠️ Some sizes/licenses are estimates or unverified (`❓` / `≈`). Always confirm with the original source before research or production use.

## License

This list (text) is released under [CC0](https://creativecommons.org/publicdomain/zero/1.0/). Each dataset, however, is governed by its **own license**.
