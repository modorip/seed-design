# SegmentedControl

상호 배타적 옵션 중 하나를 선택하는 컨트롤. 탭의 작은 형태.

## 구조

```
┌──────────────────────────────┐
│ [옵션 1] [옵션 2] [옵션 3]    │
└──────────────────────────────┘
```

활성 옵션만 배경 + 그림자.

## Props

| prop | 설명 |
|---|---|
| `value` | 현재 선택된 옵션 id |
| `options` | `{ id, label, icon? }[]` |
| `onChange(id)` | 변경 핸들러 |
| `size` | `sm` \| `md` (기본) \| `lg` |
| `width` | `auto` (기본) \| `full` |

## 사이즈

| size | height | font |
|---|---|---|
| `sm` | 28 | caption-1 / 600 |
| `md` | 36 | body-2 / 700 |
| `lg` | 44 | body-1 / 700 |

## 시각

- 트랙: 옅은 회색 배경 (`--color-bg`)
- 활성: 흰 배경 + `--shadow-card-1` + 진한 텍스트
- 비활성: 투명 + `--color-fg-subtle` 텍스트

전환: 200ms `--ease-out-standard` (배경·텍스트 컬러).

## 사용 예

```tsx
<SegmentedControl
  value={view}
  options={[
    { id: 'list', label: '리스트' },
    { id: 'map',  label: '지도' },
  ]}
  onChange={setView}
/>
```

여기여기 앱에서의 사용:
- 도감 전국: 지도 / 카드
- 프리셋 상세 코스 순서: 리스트 / 지도
- 광장 메인: 피드 / 인기 프리셋 / 리더보드 / 동행

## 접근성

- `role="tablist"`, 각 옵션 `role="tab"` + `aria-selected`
- 키보드 좌/우 방향키 지원

## 안티 패턴

- 옵션이 5개 초과 — 그건 TabBar 또는 Dropdown
- 옵션 라벨이 길어 텍스트 줄바꿈 — 줄임표 처리 또는 사이즈 lg
- 다중 선택용 — 그건 Chip 그룹
