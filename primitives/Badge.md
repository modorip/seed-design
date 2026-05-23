# Badge

상태 표시·라벨링.

## 톤

`neutral` | `primary` | `success` | `warning` | `danger` | `info` | `accent` | `heritage` | `festival`

마지막 3개(`accent`, `heritage`, `festival`)는 4계열 도메인 컬러용.

## 변형

| variant | 모양 |
|---|---|
| `solid` | 톤 색 채움 + 흰 텍스트 |
| `subtle` | 톤 색 옅은 배경 + 톤 색 텍스트 (기본) |
| `outline` | 경계만 |
| `dot` | 작은 도트 + 텍스트 |

## 사이즈

| size | height | font |
|---|---|---|
| `sm` | 18 | caption-2 / 600 |
| `md` | 22 | caption-1 / 600 (기본) |
| `lg` | 28 | body-2 / 700 |

## 사용 예

```tsx
<Badge tone="success" variant="solid">발견 완료</Badge>
<Badge tone="danger">매우 혼잡</Badge>
<Badge tone="nature" variant="subtle">자연 · 산</Badge>
```

## 안티 패턴

- 본문 텍스트 안에 뱃지 사용
- 인터랙티브 액션 (탭 가능)으로 사용 — 그건 Chip 또는 Button
