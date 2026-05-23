# PresetCard

여행 코스(프리셋)를 광장·프로필 등에서 카드 형태로 표현하는 패턴.

## 구조

```
┌─────────────────────────────────────────────┐
│ [지역 SVG]  제목 (title-3 / 700)             │
│ 실루엣      "자원 N곳 · 담음 N회" (body-2)    │
│             [태그 칩 ×3]                     │
│                                              │
│             [자원 미리보기 5장 가로 슬라이드]   │
│                                              │
│             [작성자 아바타] 이름  · 인기도     │
└─────────────────────────────────────────────┘
```

## Props

| prop | 설명 |
|---|---|
| `preset` | `Preset` 객체 |
| `region` | 광역 정보 (실루엣·톤) |
| `compact` | 프로필 등 좁은 영역에서 축약 표시 |
| `savedBadge` | 사용자가 담았는지 표시 (true이면 "담음" 뱃지) |
| `medalRank` | 1\|2\|3 (Top 3 메달 뱃지) |
| `onClick` | 카드 탭 핸들러 |
| `onAuthorClick` | 작성자 탭 핸들러 |

## 변형

- `default`: 광장에서 사용. 자원 미리보기 5장 풀 노출
- `compact`: 프로필·다른 사용자 페이지에서 사용. 미리보기 3장만, 작성자 hide

## 메달 뱃지 (Top 3)

`medalRank` 지정 시 카드 우상단에 표시:
- 1: 골드 (`#FFD700` 배경, `#7A5C00` 텍스트)
- 2: 실버 (`#C0C0C0` 배경, `#4A4A4A` 텍스트)
- 3: 브론즈 (`#CD7F32` 배경, `#5A3A1A` 텍스트)

크기: 28×28 원형, 숫자만 표시 (1, 2, 3).

## 사용 예

```tsx
<PresetCard
  preset={preset}
  region={REGIONS.find(r => r.id === preset.regionId)}
  medalRank={index < 3 ? index + 1 : undefined}
  onClick={() => openPreset(preset.id)}
  onAuthorClick={() => openUser(preset.authorId)}
/>
```

## 안티 패턴

- 카드 안에 카드 (중첩 surface) — 위계 무너짐
- 자원 미리보기 6장 이상 — 행 줄바꿈으로 정보 산만함
- 메달 뱃지를 Top 3 이외에 사용 — 뱃지 가치 희석
