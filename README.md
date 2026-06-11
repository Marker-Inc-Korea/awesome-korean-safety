# 🛡️ Awesome Korean Safety [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

한국어 LLM **안전성(Safety) 벤치마크 및 데이터셋** 정보를 모아놓은 awesome list입니다.

LLM의 유해성, 사회적 편향, 혐오표현, 민감 질문 대응, 레드티밍, 멀티모달 안전성 등을 **한국어·한국 문화 맥락**에서 평가할 수 있는 벤치마크들을 정리합니다.
포맷은 [Awesome-LLM-Safety](https://github.com/ydyjya/Awesome-LLM-Safety), [awesome-korean-llm](https://github.com/NomaDamas/awesome-korean-llm)을 참고했습니다.

> ⚠️ **상업적 사용** 컬럼은 데이터셋 라이선스 기준이며, 실제 사용 전 각 저장소의 LICENSE 원문을 반드시 직접 확인하세요.
> ✅ 가능 (MIT·Apache·CC-BY·CC-BY-SA 등) / ❌ 불가 (CC-BY-NC·NC-ND, 비공개·제한적 공개) / ❓ 불명확·문의 필요

---

## 🚀 Table of Contents

- [가치 · 정렬 (Values & Alignment)](#-가치--정렬-values--alignment)
- [사회적 편향 (Social Bias)](#-사회적-편향-social-bias)
- [혐오 · 유해 표현 탐지 (Hate / Offensive / Toxicity)](#-혐오--유해-표현-탐지-hate--offensive--toxicity)
- [유해 지시 · 레드티밍 · 가드레일 (Harmful Instruction, Red-teaming & Guardrails)](#-유해-지시--레드티밍--가드레일-harmful-instruction-red-teaming--guardrails)
- [멀티모달 안전성 (Multimodal Safety)](#-멀티모달-안전성-multimodal-safety)
- [다국어 벤치마크 (한국어 포함) (Multilingual, incl. Korean)](#-다국어-벤치마크-한국어-포함-multilingual-incl-korean)
- [도메인 특화 (Domain-specific)](#-도메인-특화-domain-specific)
- [리더보드 (Leaderboards)](#-리더보드-leaderboards)
- [관련 자료 (Related Resources)](#-관련-자료-related-resources)
- [검증에서 제외 / 보류한 항목](#-검증에서-제외--보류한-항목)
- [Contributing](#-contributing)

---

## 🧭 가치 · 정렬 (Values & Alignment)

한국 사회의 가치관·상식·민감한 질문에 대해 모델의 정렬(alignment) 정도를 평가합니다.

| 이름 | 평가 영역 | 사이즈 | 제작자 | 발표 (학회/연도) | 상업적 사용 | 데이터 |
| --- | --- | --- | --- | --- | --- | --- |
| [KorNAT](https://aclanthology.org/2024.findings-acl.666/) | 한국 사회 가치·상식 정렬 (National Alignment) | 사회가치 4K + 상식 6K (≈10K MCQ) | KAIST · Selectstar · NIA | ACL 2024 (Findings) | ❓ (연구용·확인 필요) | [🤗 HF](https://huggingface.co/datasets/jiyounglee0523/KorNAT) |
| [SQuARe](https://github.com/naver-ai/korean-safety-benchmarks) | 민감 질문 · 수용 가능 응답 | 질문 ≈49K + 응답 ≈42K | NAVER AI Lab | ACL 2023 | ✅ (MIT) | [GitHub](https://github.com/naver-ai/korean-safety-benchmarks) |
| [초거대 언어모델 신뢰성 벤치마크](https://aihub.or.kr/aihubdata/data/view.do?dataSetSn=71760) | 신뢰성 종합 (편향·윤리·사실성) | 대규모 (2023 구축 / 2024.12 갱신) | NIA · 과기정통부 | AI Hub (2023~) | ❓ (AI Hub 약관) | [AI Hub](https://aihub.or.kr/aihubdata/data/view.do?dataSetSn=71760) |

## ⚖️ 사회적 편향 (Social Bias)

성별·연령·지역·종교 등 사회집단에 대한 모델의 편향을 측정합니다.

| 이름 | 평가 영역 | 사이즈 | 제작자 | 발표 (학회/연도) | 상업적 사용 | 데이터 |
| --- | --- | --- | --- | --- | --- | --- |
| [KoBBQ](https://github.com/naver-ai/KoBBQ) | 사회적 편향 QA (한국 문화 적응 BBQ) | 268 템플릿 / 76,048 샘플 (12 범주) | KAIST · NAVER AI Lab | TACL 2024 | ✅ (MIT) | [GitHub](https://github.com/naver-ai/KoBBQ) |
| [KoSBi](https://github.com/naver-ai/korean-safety-benchmarks) | 사회적 편향 안전/유해 문장 (72 집단 / 15 속성) | ≈68K (맥락-문장 쌍) | NAVER AI Lab | ACL 2023 (Industry) | ✅ (MIT) | [GitHub](https://github.com/naver-ai/korean-safety-benchmarks) |

## 💬 혐오 · 유해 표현 탐지 (Hate / Offensive / Toxicity)

혐오·공격·유해 표현을 탐지·분류하는 데이터셋으로, 안전성 필터/가드레일 모델 학습·평가에 널리 쓰입니다.

| 이름 | 평가 영역 | 사이즈 | 제작자 | 발표 (학회/연도) | 상업적 사용 | 데이터 |
| --- | --- | --- | --- | --- | --- | --- |
| [K-HATERS](https://github.com/ssu-humane/K-HATERS) | 혐오표현 (타깃별 세분화 레이블 · 강도 등급) | 192,158 (뉴스 댓글) | 숭실대 (ssu-humane) | EMNLP 2023 (Findings) | ✅ (CC BY 4.0) | [GitHub](https://github.com/ssu-humane/K-HATERS) |
| [K-MHaS](https://github.com/adlnlp/K-MHaS) | 멀티라벨 혐오표현 (8개 클래스 + 1) | 109,692 발화 | Univ. of Sydney · UWA | COLING 2022 | ✅ (CC BY-SA 4.0) | [🤗 HF](https://huggingface.co/datasets/jeanlee/kmhas_korean_hate_speech) |
| [KOLD](https://github.com/boychaboy/KOLD) | 계층적 공격 표현 (유형 · 대상 · span) | 40,429 (댓글) | KAIST · Softly AI | EMNLP 2022 | ❓ (미명시) | [GitHub](https://github.com/boychaboy/KOLD) |
| [AIHub 유해표현 검출 데이터](https://www.aihub.or.kr/aihubdata/data/view.do?dataSetSn=71833) | LLM 말뭉치 유해표현 검출 · 11개 범주 분류 | 대규모 (학습 80% / 테스트 20%) | NIA · TTA | AI Hub | ❓ (AI Hub 약관) | [AI Hub](https://www.aihub.or.kr/aihubdata/data/view.do?dataSetSn=71833) |
| [UnSmile](https://github.com/smilegate-ai/korean_unsmile_dataset) | 멀티라벨 혐오표현 (여성/지역/종교 등 10개) | 18,742 문장 | Smilegate AI | 2022 | ❌ (CC BY-NC-ND 4.0 · 별도 문의) | [GitHub](https://github.com/smilegate-ai/korean_unsmile_dataset) |
| [HateScore](https://github.com/sgunderscore/hatescore-korean-hate-speech) | 혐오표현 강건성 (HITL + 중립 문장 오탐 완화) | ≈11K | Underscore | 2022 | ❓ (미명시) | [GitHub](https://github.com/sgunderscore/hatescore-korean-hate-speech) |
| [APEACH](https://github.com/jason9693/APEACH) | 혐오표현 평가셋 (크라우드 생성) | ≈3.7K (평가셋) | Kakao · 숭실대 · SNU | EMNLP 2022 (Findings) | ✅ (CC BY-SA 4.0) | [🤗 HF](https://huggingface.co/datasets/jason9693/APEACH) |
| [KODOLI](https://github.com/cardy20/KODOLI) | 세분화된 공격성 (offensive / likely / not) | 공격성 3단계 | 가톨릭대 | EACL 2023 (Findings) | ❓ (미명시) | [GitHub](https://github.com/cardy20/KODOLI) |
| [KOTOX](https://github.com/leeyejin1231/KOTOX) | 한글 난독화 유해 표현 탐지 · 복원 · 순화 | 난이도 3단계 (easy/normal/hard) | Yejin Lee et al. | arXiv 2025.10 | ❓ (미명시) | [GitHub](https://github.com/leeyejin1231/KOTOX) |
| [BEEP!](https://github.com/kocohub/korean-hate-speech) | 혐오·편향 표현 (최초의 한국어 혐오 벤치마크) | 9,381 라벨 (+ ≈2M 비라벨) | kocohub (Moon et al.) | ACL 2020 (SocialNLP WS) | ✅ (CC BY-SA 4.0) | [GitHub](https://github.com/kocohub/korean-hate-speech) |
| [DKTC](https://github.com/tunib-ai/DKTC) | 위협 대화 분류 (협박 · 갈취 · 괴롭힘 등) | ≈4K 대화 | TUNiB | 2022 | ❌ (비상업·연구용) | [GitHub](https://github.com/tunib-ai/DKTC) |

> ℹ️ **KOTOX**(난독화, Lee et al.)와 아래의 **KoTox**(유해 지시, Byun et al.)는 이름이 비슷하지만 서로 다른 데이터셋입니다.

## 🎯 유해 지시 · 레드티밍 · 가드레일 (Harmful Instruction, Red-teaming & Guardrails)

모델의 유해 출력·악용 가능성을 유도하거나(레드티밍), 윤리 튜닝·가드레일 학습에 쓰이는 데이터셋입니다.

| 이름 | 평가 영역 | 사이즈 | 제작자 | 발표 (학회/연도) | 상업적 사용 | 데이터 |
| --- | --- | --- | --- | --- | --- | --- |
| [CAGE / KoRSET](https://arxiv.org/abs/2602.20170) | 문화 적응형 레드티밍 (한국 법·문화 기반) | KoRSET ≈7,161 프롬프트 | SelectStar AI (Kim et al.) | arXiv 2026.02 | ❓ (제한적 공개) | [arXiv](https://arxiv.org/abs/2602.20170) |
| [KoTox](https://github.com/byunsj/KoTox-Korean-Toxic-Instruction-Dataset) | 유해 instruction 대응 (정치편향 · 범죄 · 혐오) | 39K (instruction-output 쌍) | 서울대 (Byun et al.) | NeurIPS 2023 (WS) | ✅ (MIT) | [GitHub](https://github.com/byunsj/KoTox-Korean-Toxic-Instruction-Dataset) |
| [K-Guardrail](https://github.com/skan0779/korean-guardrail-dataset) | AI 에이전트 가드레일 평가 (탈옥 · PII 등) | 320+ 프롬프트 | skan0779 (오픈소스) | GitHub 2025 | ❓ (미명시) | [GitHub](https://github.com/skan0779/korean-guardrail-dataset) |
| [EVE (v1/v2)](https://arxiv.org/abs/2403.06537) | 오픈소스 모델 악용 레드티밍 (범죄 조언) | v1 200 QA + v2 600 (판례 기반) | AAAI 2024 저자 | AAAI 2024 | ❌ (비공개) | [arXiv](https://arxiv.org/abs/2403.06537) |

## 🖼️ 멀티모달 안전성 (Multimodal Safety)

텍스트뿐 아니라 이미지·영상·음성 등 멀티모달 입력에 대한 안전성을 평가합니다.

| 이름 | 평가 영역 | 사이즈 | 제작자 | 발표 (학회/연도) | 상업적 사용 | 데이터 |
| --- | --- | --- | --- | --- | --- | --- |
| [AssurAI](https://huggingface.co/datasets/TTA01/AssurAI) | 한국 사회문화 위험 35종 멀티모달 평가 (텍스트·이미지·영상·음성) | 11,480 instances | TTA · KAIST · Kakao 등 | arXiv 2025.11 | ❌ (CC BY-NC 4.0) | [🤗 HF](https://huggingface.co/datasets/TTA01/AssurAI) |
| [KSAFE-MM](https://arxiv.org/abs/2605.28013) | 한국 문화 특화 MLLM 안전성 (cross-modal 공격 포함) | 14,135 samples (G: 번역 / C: 한국 특화) | Yongwoo Kim et al. | arXiv 2026.05 | ❓ (확인 필요) | [arXiv](https://arxiv.org/abs/2605.28013) |

## 🌐 다국어 벤치마크 (한국어 포함) (Multilingual, incl. Korean)

여러 언어를 다루며 **한국어를 포함**하는 안전성 벤치마크입니다. 한국어 부분집합/번역만 떼어 활용할 수 있습니다.

| 이름 | 평가 영역 | 사이즈 | 제작자 | 발표 (학회/연도) | 상업적 사용 | 데이터 |
| --- | --- | --- | --- | --- | --- | --- |
| [XL-SafetyBench](https://arxiv.org/abs/2605.05662) | 국가별 jailbreak + 문화 민감성 (10개국, 한국 포함) | 5,500 | AIM Intelligence · KT · Microsoft · BMW | arXiv 2026.05 | ❓ (확인 필요) | [arXiv](https://arxiv.org/abs/2605.05662) |
| [PolyGuardPrompts](https://huggingface.co/datasets/ToxicityPrompts/PolyGuardPrompts) | 다국어 가드레일 평가 (유해성 · 거부 라벨, 17개 언어) | 29,325 | PolyGuard 저자 | arXiv 2025.04 | ❓ (확인 필요) | [🤗 HF](https://huggingface.co/datasets/ToxicityPrompts/PolyGuardPrompts) |
| [WildGuardMix-KO](https://huggingface.co/datasets/iknow-lab/wildguardmix-test-ko) | WildGuardMix 한국어 번역 (프롬프트·응답 유해성·거부) | Test-KO ≈1.7K (+ Train 번역본) | iknow-lab | 2024 | ✅ (ODC-BY, test) | [🤗 HF](https://huggingface.co/datasets/iknow-lab/wildguardmix-test-ko) |
| [CSRT](https://arxiv.org/abs/2406.15481) | 코드 스위칭 레드티밍 / jailbreak (10개 언어, 한국어 포함) | 315 쿼리 | Yoo, Yang, Lee | arXiv 2024.06 | ❓ (확인 필요) | [🤗 HF](https://huggingface.co/datasets/walledai/CSRT) |

## 🔬 도메인 특화 (Domain-specific)

특정 위험 도메인(사실성/환각, 위치 프라이버시, 자살·자해 등)에 특화된 안전 데이터셋입니다.

| 이름 | 평가 영역 | 사이즈 | 제작자 | 발표 (학회/연도) | 상업적 사용 | 데이터 |
| --- | --- | --- | --- | --- | --- | --- |
| [K-HALU](https://github.com/J-Seo/K-HALU) | 한국어 환각 · 사실성 탐지 | 2K+ samples | 고려대 (Seo & Lim) | ICLR 2025 | ❓ (AI Hub 약관) | [GitHub](https://github.com/J-Seo/K-HALU) |
| [KoreaGEO Bench](https://arxiv.org/abs/2506.03371) | 위치정보 프라이버시 VLM 평가 (스트리트뷰) | 1,080 images | KoreaGEO 저자 | EMNLP 2025 | ❓ (확인 필요) | [arXiv](https://arxiv.org/abs/2506.03371) |
| [Harmful Suicide Content Detection](https://arxiv.org/abs/2407.13942) | 유해 자살 콘텐츠 탐지 (위험 등급) | 멀티모달 | (2024 연구) | arXiv 2024.07 | ❌ (제한적 접근) | [arXiv](https://arxiv.org/abs/2407.13942) |

---

## 🏆 리더보드 (Leaderboards)

| 이름 | 안전성 관련 평가 항목 | 운영 | 비고 |
| --- | --- | --- | --- |
| [Open Ko-LLM Leaderboard2](https://huggingface.co/spaces/upstage/open-ko-llm-leaderboard) | Ko-Harmlessness (편향·혐오·민감성·불법), KorNAT-Social-Value, KorNAT-Knowledge | Upstage & NIA | 비공개 평가셋 기반 종합 평가 ([논문](https://arxiv.org/abs/2410.12445)) |

---

## 📚 관련 자료 (Related Resources)

- [NAVER CLOVA Tech Blog — 한국어 안전성 벤치마크 소개 (SQuARe, KoSBi, KoBBQ, KorNAT)](https://clova.ai/en/tech-blog/en-using-korean-benchmark-datasets-to-develop-and-evaluate-hyperclova-x-and-other-safe-and-trustworthy-language-models)
- [naver-ai/korean-safety-benchmarks](https://github.com/naver-ai/korean-safety-benchmarks) — SQuARe & KoSBi 공식 레포
- [LLM 안전성 데이터셋 모음 (HF Collection)](https://huggingface.co/collections/nayohan/llm-safety-datasets-668a8ba41725ae18ed3353a8) — 한국어 포함 안전성·윤리 데이터셋 컬렉션
- [AwesomeKorean_Data](https://github.com/songys/AwesomeKorean_Data) — 한국어 데이터셋 종합 목록 (혐오표현 섹션 포함)
- [Awesome-LLM-Safety](https://github.com/ydyjya/Awesome-LLM-Safety) — LLM 안전성 전반 (영문)
- [AI Hub](https://aihub.or.kr) — NIA 주관 텍스트 윤리검증·신뢰성 데이터 등 공공 데이터셋

---

## 🔎 검증에서 제외 / 보류한 항목

큐레이션 신뢰성을 위해, 실재 여부를 확인할 수 없거나 한국어 LLM safety 범위에 맞지 않는 항목은 제외했습니다.

- **K-FalseRefusal** — 한국어 over-refusal 데이터셋으로 검색·확인되지 않음(영어 *FalseReject*, *OR-Bench*, *PHTest*만 존재). **검증 불가로 제외** (실재가 확인되면 추가 환영).
- **KorMedMCQA / KorMedMCQA-V** — 의료 면허시험 기반 지식 QA로, 안전성보다 **도메인 역량(capability) 벤치마크**에 가까워 제외.
- **KoDF** — 한국어 **딥페이크 영상 탐지**(미디어 포렌식) 데이터셋으로, LLM/생성형 텍스트 safety 범위 밖이라 제외.
- **Korean Hate Speech Analysis Dataset (Datumo)** — 제시된 형태(11범주·Likert·Datumo)를 단일 출처로 확정하지 못해 **보류**.

> 위 판단에 이견이 있거나 출처를 알고 계시면 이슈/PR로 알려주세요.

---

## 🤝 Contributing

틀린 정보가 있거나 새로운 한국어 안전성 벤치마크가 있다면 언제든 PR을 보내주세요!

- 표에 한 행을 추가합니다: `이름 / 평가 영역 / 사이즈 / 제작자 / 발표 / 상업적 사용 / 데이터`
- 가능하면 **논문 링크**와 **데이터/코드 링크**를 모두 포함해 주세요.
- 표 내 정렬 기준: **최신 발표일 → 인용/사용 빈도 → 발표 venue 공신력** 순
- 라이선스/상업적 사용은 원 저장소의 LICENSE를 근거로 `✅ / ❌ / ❓`와 라이선스명을 함께 기재해 주세요.
- 적절한 카테고리가 없다면 새 섹션을 제안해 주세요.

> ⚠️ 일부 항목의 정확한 샘플 수·라이선스는 추정치이거나 미확인 상태입니다(`❓` / `≈` 표기). 실제 연구·서비스에 사용하기 전 반드시 원 출처를 확인하세요.

## License

이 목록(텍스트)은 [CC0](https://creativecommons.org/publicdomain/zero/1.0/)로 배포됩니다. 단, 각 데이터셋은 위 표에 명시된 **고유 라이선스**를 따릅니다.
