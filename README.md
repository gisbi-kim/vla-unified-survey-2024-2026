# VLA Unified Survey 2024–2026

> **보고, 이해하고, 행동하는 로봇을 위한 Vision-Language-Action 모델의 모든 것**

🔗 **[Live Survey Page →](https://gisbi-kim.github.io/vla-unified-survey-2024-2026/)**

*DGIST APRL Lab · Prof. Giseop Kim · April 2026*

---

## 이 레포지토리는 무엇인가요?

14편의 VLA 서베이 논문을 하나의 통합된 시각으로 재구성한 **한국어 종합 서베이 페이지**입니다.
단순 논문 요약이 아니라, 개별 서베이들이 놓친 **교차 분석 인사이트**와 **5축 통합 분류 체계**를 제시합니다.

- 서베이 논문 14편 통합 분석
- 2024–2026 최신 VLA 동향 완전 커버
- 아키텍처 · 액션 토크나이제이션 · 학습 패러다임 · 효율화 · 응용 도메인 심층 다룸
- ICLR 2026 제출 트렌드 포함 (164편, 전년 대비 18× 성장)

---

## 목차 구성 (10개 섹션)

| # | 섹션 | 핵심 내용 |
|---|------|----------|
| 1 | Introduction | VLA 정의와 범위, 왜 지금 VLA인가 |
| 2 | Historical Timeline | 2017–2026 발전사 4단계 |
| 3 | Unified Classification | 14편 서베이를 하나의 프레임워크로 통합 |
| 4 | Architecture Deep Dive | Perception · Brain · Action 모듈 해부 |
| 5 | Action Tokenization | 8가지 토큰 타입 분류 및 설계 결정 |
| 6 | Learning Paradigms | Pre-training · BC · RL post-training |
| 7 | Efficiency | 경량화 · 엣지 배포 최적화 |
| 8 | Application Domains | 매니퓰레이션 · 자율주행 · UAV 등 |
| 9 | Datasets & Benchmarks | 평가 인프라 총정리 |
| 10 | Open Problems | 미해결 과제와 미래 방향 |

---

## 통합된 14편 서베이 논문

| # | 논문 | arXiv | 핵심 관점 |
|---|------|-------|----------|
| [1] | Ma et al. | [2405.14093](https://arxiv.org/abs/2405.14093) | Embodied AI 생태계 전반 (LLM/VLM/VLA 통합) |
| [2] | Kawaharazuka et al. | [2402.05741](https://arxiv.org/abs/2402.05741) | 실세계 배포 실용 인사이트 |
| [3] | Zhong et al. | [2509.19012](https://arxiv.org/abs/2509.19012) | Pure VLA 체계적 분류 (아키텍처/학습/데이터 3축) |
| [4] | Yu et al. | [2510.24795](https://arxiv.org/abs/2510.24795) | 효율화 및 모델 압축 (12개 모델 정량 비교) |
| [5] | Liu & Shao | [2508.13073](https://arxiv.org/abs/2508.13073) | 매니퓰레이션 벤치마크 (Monolithic vs Hierarchical) |
| [6] | Zhang et al. | [2505.04769](https://arxiv.org/abs/2505.04769) | 광범위 개념 개요 및 응용 도메인 |
| [7] | Chen et al. | [2507.01925](https://arxiv.org/abs/2507.01925) | 액션 토크나이제이션 심층 분석 (8가지 토큰 타입) |
| [8] | Xu et al. | [2512.11362](https://arxiv.org/abs/2512.11362) | Perception-Brain-Action 해부학적 접근 |
| [9] | Jin et al. | [2506.20966](https://arxiv.org/abs/2506.20966) | VLA+RL 포스트트레이닝 (GRPO/DPO 포함) |
| [10] | Jiang et al. | [2506.24044](https://arxiv.org/abs/2506.24044) | 자율주행 VLA 4세대 진화 |
| [41] | Hu et al. | [2512.16760](https://arxiv.org/abs/2512.16760) | AD-VLA: End-to-End vs Dual-System |
| [42] | Edge Survey | [2603.16952](https://arxiv.org/abs/2603.16952) | 엣지 배포 시스템 분석 (7가지 병목 규명) |
| [43] | Guan et al. | [2510.17111](https://arxiv.org/abs/2510.17111) | 매니퓰레이션 효율화 4차원 분류 |
| [44] | Large Model Embodied AI | [2508.10399](https://arxiv.org/abs/2508.10399) | 의사결정 프레임워크 (계층적 vs End-to-End) |

---

## 5축 통합 분류 체계

```
Architecture  ──  Monolithic (단일/이중 시스템)
               └─ Hierarchical (Planner-only / Planner+Policy)

Action Gen.   ──  Autoregressive / Diffusion / Discrete Diffusion
               └─ RL-based / Hybrid / Specialized

Anatomy       ──  Perception (비전 인코더)
               ├─ Brain (VLM 백본)
               └─ Action (디코더 모듈)

Functionality ──  Low/High-level Perception
               └─ Planning / Data Augmentation

Post-training ──  환경 인식 강화 / Embodiment 인식
               └─ 태스크 이해 / 멀티 컴포넌트 통합
```

---

## 주요 수치로 보는 현황 (2026년 기준)

- **ICLR 2026**: VLA 관련 164편 제출 (2025년 9편 → **18배 성장**)
- **경량화 성과**: 55B → 450M (SmolVLA) — 주요 성능 거의 유지
- **Discrete Diffusion VLA**: ICLR 2026 동시 4편 제출 (독립적 수렴 현상)
- **프론티어 모델 vs 공개 가중치**: 실세계 일반화 격차 미해결

---

## 로컬 실행

```bash
git clone https://github.com/gisbi-kim/vla-unified-survey-2024-2026.git
cd vla-unified-survey-2024-2026
# index.html을 브라우저에서 바로 열거나 로컬 서버 실행:
python -m http.server 8080
# → http://localhost:8080
```

---

## Citation

이 서베이 페이지를 참고하셨다면:

```bibtex
@misc{kim2026vla_unified_survey,
  author       = {Giseop Kim},
  title        = {VLA Unified Survey 2024--2026:
                  Vision-Language-Action 모델의 모든 것},
  howpublished = {\url{https://gisbi-kim.github.io/vla-unified-survey-2024-2026/}},
  year         = {2026},
  month        = {April},
  institution  = {DGIST APRL Lab}
}
```

---

## Related

- DGIST APRL Lab: [https://sites.google.com/view/aprl-dgist](https://sites.google.com/view/aprl-dgist)
