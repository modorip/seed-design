# CourseMap

코스(프리셋)의 자원 순서를 지도 위에 시각화하는 패턴.

## 구조

```
┌───────────────────────────────────────┐
│  ╭─ 광역 SVG polygon 배경 ─╮          │
│  │                          │          │
│  │   ①                       │          │
│  │     ╲                     │          │
│  │      ╲                    │          │
│  │       ②                   │          │
│  │        ╲                  │          │
│  │         ③                 │          │
│  │                           │          │
│  ╰──────────────────────────╯          │
└───────────────────────────────────────┘
```

## 구성

- **배경**: 해당 지역의 광역 SVG polygon. fill은 `--color-bg`, stroke는 `--color-border`
- **경로 (polyline)**: 핀과 핀 사이를 잇는 파란 점선 (`stroke: var(--color-primary); stroke-dasharray: 4 4`)
- **핀**: 카테고리 색상 원 + 흰 보더 (3px) + 중앙에 순서 번호 (1, 2, 3...)
- **핀 그림자**: `--shadow-card-2`로 부유감 표현
- **탭**: 핀 탭 시 해당 자원 상세 페이지로 이동

## 좌표

Phase 0: placeId 해시로 deterministic 생성 (실 좌표 미보유).
Phase 1: KTO API `mapx` / `mapy` 필드를 viewBox 정규화 후 사용.

## Props

| prop | 설명 |
|---|---|
| `preset` | `Preset` 객체 |
| `region` | 광역 정보 (실루엣 path 포함) |
| `onPinClick(placeId)` | 핀 탭 핸들러 |

## 사용 예

```tsx
<CourseMap
  preset={preset}
  region={region}
  onPinClick={(placeId) => openPlace(placeId)}
/>
```

## 동작

- 진입 시 viewBox는 광역 polygon 경계 + 8% 패딩
- 핀이 1개면 경로 미렌더
- 핀이 2개 이상이면 자동 폴리라인 연결

## 접근성

- 각 핀에 `aria-label="{순서}. {자원명}"`
- `role="img"` 컨테이너 + `aria-label="코스 지도, 자원 N곳"`
- 키보드 사용자 대비: 리스트 뷰가 동등한 정보를 제공해야 함

## 안티 패턴

- 다지역 코스 (CourseMap은 단일 광역 전제)
- 좌표 없이 임의 격자 배치 (시각적으로 코스 의미 약화)
- 경로를 실선으로 (실제 도로 라우팅 오해 유발)
