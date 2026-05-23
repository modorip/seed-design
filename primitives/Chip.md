# Chip

다중 선택 가능한 필터 토큰.

## 상태

| state | 시각 |
|---|---|
| `inactive` | 회색 배경, 다크 텍스트, 경계 1px |
| `active` | 프라이머리 톤 배경, 흰 텍스트 |

## 사이즈

| size | height | padding | font |
|---|---|---|---|
| `sm` | 28 | 0 10 | caption-1 / 600 |
| `md` | 32 | 0 12 | body-2 / 600 (기본) |

## 사용 예

```tsx
<Chip active>전체</Chip>
<Chip onClick={toggle}>산</Chip>
<Chip leadingIcon={<MountainIcon />}>해변·섬</Chip>
```

## 그룹 패턴

가로 스크롤 영역에 배치, gap 8, 좌우 인셋 16. 첫 칩은 "전체" 권장.

## 안티 패턴

- 단일 선택용으로 사용 — 그건 SegmentedControl
- 칭호·뱃지처럼 비클릭 정보 표시용 — 그건 Badge
