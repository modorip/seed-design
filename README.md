# seed-design

> 여기여기 (Yeogi Yeogi) 의 디자인 시스템.
> 토스 TDS, 당근 seed-design 운영 사례를 참고해 코드 레포에서 분리된 public 저장소로 운영합니다.

## 무엇인가요

여기여기 앱은 한국관광공사 OpenAPI 기반의 게이미피케이션 여행 도감 앱입니다. 이 저장소는 그 앱이 사용하는 디자인 토큰·컴포넌트·패턴의 **단일 원천(Single Source of Truth)** 입니다.

- 토큰: 컬러·타입·라운드·모션
- 컴포넌트: Button · Badge · Chip · Avatar · IconButton · Card · ListRow · Progress
- 패턴: AppHeader · TabBar · SegmentedControl · BottomSheet · EmptyState · PresetCard · CourseMap
- 아이콘: Lucide stroke 스타일 자체 셋
- 자산: Pretendard / Wanted Sans 폰트 라이센스 안내, 한국 17광역 SVG path

## 철학

1. **차분하고 정확하게.** 과장 금지. 사용자를 가르치려 들지 않습니다.
2. **이모지 없이.** Lucide stroke 아이콘만 사용합니다.
3. **한글 우선.** Pretendard를 본문/UI 표준 폰트로 사용합니다.
4. **블러는 신중하게.** 그림자는 다중 박스 섀도우 컴포지트로 깊이를 표현합니다.
5. **위계를 통한 강조.** 색·굵기 남발 대신 크기·간격으로 위계를 설계합니다.

## 디렉터리

```
seed-design/
├── tokens/        디자인 토큰 명세 (컬러·타입·라운드·모션·스페이싱)
├── primitives/    원시 컴포넌트 (Button · Badge · Chip 등)
├── patterns/      복합 패턴 (AppHeader · TabBar 등)
├── icons/         아이콘 카탈로그
└── assets/        폰트·SVG 자원 안내
```

## Phase 로드맵

| Phase | 산출물 |
|---|---|
| **0 (현재)** | 마크다운 명세 + 참고 토큰 |
| 1 | `@yeogi/seed-design` npm 패키지 (React + TypeScript) |
| 2 | Figma 라이브러리 동기화 |
| 3 | 외부 컨트리뷰션 가이드 정착 |

## 라이센스

MIT. 자세한 내용은 [LICENSE](./LICENSE).

기여 가이드는 [CONTRIBUTING.md](./CONTRIBUTING.md).

## 기반

이 디자인 시스템은 **Wanted Design System** ([wanted-design.com](https://wanted-design.com)) 의 토큰·컴포넌트 구조를 기반으로 여기여기의 도메인(도감·발견·광역 등)에 맞춰 확장한 결과물입니다. 사용된 폰트와 라이브러리의 원 라이센스는 각 디렉터리의 안내를 따릅니다.
