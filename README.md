# 딥러닝자연어처리 2026-2

제주한라대학교 인공지능학과 3학년 - 대규모 언어모델의 적응, 정렬, 검색 결합

**사이트**: [deepnlp-2026.halla.ai](https://deepnlp-2026.halla.ai)
**저장소**: [github.com/halla-ai/deepnlp-2026](https://github.com/halla-ai/deepnlp-2026)

| 항목 | 내용 |
|---|---|
| 학수번호 | 131307379A |
| 대상 | 3학년 |
| 학점·시수 | 3학점 / 3시수 |
| 운영 | BL - 온라인 2시수(AI Professor) + 대면 1시수 |

---

## 학생이라면

- **강의계획서**: [deepnlp-2026.halla.ai/syllabus](https://deepnlp-2026.halla.ai/syllabus)
- **실습 노트북**: [deepnlp-2026.halla.ai/notebooks](https://deepnlp-2026.halla.ai/notebooks) - Colab에서 바로 열린다
- **과제 제출**: [deepnlp-2026.halla.ai/assignments](https://deepnlp-2026.halla.ai/assignments) - GitHub 웹에서만 해도 된다

설치할 것이 없다. 브라우저만 있으면 된다.

---

## 주차 구성

| 주 | 주제 |
|---|---|
| 1 | 차세대 NLP 아키텍처의 이해와 과목 뼈대 공유 |
| 2 | 구현 기반 - 학습 루프와 텐서 연산 |
| 3 | 효율적 미세조정의 원리와 변형 |
| 4 | 프롬프트와 문맥학습의 원리 |
| 5 | 평가 시스템과 지표가 측정하지 못하는 것 |
| 6 | 멀티모달 표현의 결합 |
| 7 | 장문맥 처리와 효율적 추론 |
| 8 | 중간고사 및 PEFT 심화 |
| 9 | 검색 결합 생성(RAG)의 구조 |
| 10 | 정렬 기법의 계보 - RLHF에서 GRPO까지 |
| 11 | 과정 감독과 신용 할당 - PRM과 토큰 수준 credit |
| 12 | AI 규제와 책임 있는 AI |
| 13 | 최신 연구 동향과 미래 전망 |
| 14 | 최종 프로젝트 개발 및 운영 전환 |
| 15 | 산업 응용 사례 분석 및 최종 발표 |

---

## 저장소 구조

```
src/content/docs/     강의 사이트 콘텐츠 (Astro + Starlight)
  weeks/              주차별 강의노트 15개
  syllabus.md         학생용 강의계획서 (학사시스템 등록본에서 파생)
notebooks/            실습 노트북. Colab 배지로 열린다
assignments/          과제 제출. week-NN/<학번>/
```

## 개발

```bash
make install    # 의존성 설치
make dev        # localhost:4321
make build      # dist/ 정적 빌드
make status     # 콘텐츠 현황
```

새 콘텐츠:

```bash
make new-week N=07       # 주차 페이지
make new-notebook N=07   # 실습 노트북 (표준 형태로 생성)
```

## 배포

`main` push 시 GitHub Actions가 빌드해 GitHub Pages로 배포한다.

## 실습 설계 원칙

노트북은 **동작하는 상태로 제공한다.** 학생은 먼저 그대로 실행해 결과를 확인하고,
표시된 **한 지점만** 바꿔 무엇이 달라지는지 본다. 밑바닥부터 작성하게 하지 않는다.

매 주차 돌아가는 결과물을 손에 쥐고 나가는 것이 목표다.
