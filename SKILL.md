---
name: dsr-ai-newsletter
description: DSR 'AI Multiplier(리더의 AI 곱셈법)' 뉴스레터 HTML을 생성한다. 볼륨 번호와 주제만 입력하면 고정 형식대로 완성본을 만든다.
---

# DSR AI Multiplier 뉴스레터 생성 스킬

## 고정 정보 (매호 동일)

- **브랜드명**: AI Multiplier / 리더의 AI 곱셈법
- **대상 독자**: 한국 중견 제조업 임원·리더
- **폰트**: Pretendard (Google Fonts)
- **색상**: 메인 #0284c7(파랑), 배경 #f8fafc, 텍스트 #0f172a
- **CSS 프레임워크**: Tailwind CDN
- **Phase 구조**: Phase 1(Vol.01~04) / Phase 2(Vol.05~08) / Phase 3(Vol.09~12)

## 매호 바뀌는 정보 (입력받을 것)

| 항목 | 예시 |
|------|------|
| Vol 번호 | 03 |
| Phase 번호 | 1 |
| 주제 한 줄 | 검색의 종말, 딥 리서치 활용법 |
| Hero 헤드라인 | 검색은 끝났습니다, '딥 리서치'로 보고서를 받으십시오. |
| Hero 부제 | 키워드를 검색하던 시대는 끝났습니다... |
| Radar 유튜브 URL | https://youtube.com/embed/... |
| 해독기 핵심 개념 3~5개 | 딥 리서치란, 활용법, 주의점 등 |
| Action Lab 미션 내용 | 부서별 프롬프트 시나리오 |
| 현재 Vol 로드맵상 상태 | 완료/현재/예정 |

## 고정 섹션 구조 (순서 지킬 것)

1. **Nav** — DSR 로고 + AI Multiplier + Phase/Vol 뱃지
2. **Hero** — Executive Focus 뱃지 + 대형 헤드라인 + 부제
3. **로드맵** — Phase 1~3 카드, 현재 Vol 하이라이트(파란 점 애니메이션)
4. **Radar** — 유튜브 임베드 + 영상 핵심 요약 3줄
5. **해독기** — 핵심 개념 카드 형식으로 설명
6. **Action Lab** — 부서 탭(제조/구매/HR/영업/경영기획) + 프롬프트 생성기
7. **Footer** — DSR 저작권

## 디자인 규칙

- 카드 border-radius: 2rem 이상
- 강조색은 파랑 계열만 사용 (emerald는 복사 완료 버튼에만)
- 섹션 간 여백: mb-20 ~ mb-32
- 모바일 대응 필수 (Tailwind md: 브레이크포인트 사용)
- Hero 배경: `linear-gradient(135deg, #f0f9ff 0%, #e0f2fe 100%)`

## Action Lab 기획 규칙

HTML 생성 전 반드시 아래 순서로 진행:

1. Claude가 해당 Vol 주제를 보고 **Action Lab 미션 후보 3개를 먼저 제안**
2. 사용자가 후보 중 선택하거나 수정
3. 확정된 미션으로 HTML 생성

> Claude는 "Action Lab 내용을 알려주세요"라고 묻지 말고, 항상 먼저 제안할 것

## 실행 방법

사용자가 아래 형식으로 입력하면 즉시 HTML 생성:

```
Vol.번호, 주제: [주제명]
헤드라인: [Hero 헤드라인]
유튜브: [URL 또는 "없음"]
해독기 주제: [개념 목록]
Action Lab: [미션 설명]
```

## 품질 체크 (생성 후 자기검증)

- [ ] Vol 번호가 로드맵에 정확히 반영됐는가
- [ ] 이전 Vol은 취소선(line-through), 현재 Vol은 파란 점 표시인가
- [ ] Action Lab 부서 탭 5개 모두 동작하는가
- [ ] 프롬프트 복사 버튼이 작동하는가
- [ ] 모바일 레이아웃 깨지지 않는가
