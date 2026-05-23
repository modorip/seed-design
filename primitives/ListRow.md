# ListRow

리스트의 한 행. 좌측 leading, 가운데 title+subtitle, 우측 trailing 구조.

## 구조

```
[leading]  [title]              [trailing]
            [subtitle]
```

## Props

| prop | 설명 |
|---|---|
| `leading` | 좌측 (아이콘, 아바타, 이미지) |
| `title` | 메인 텍스트 (body-1 / 700) |
| `subtitle` | 보조 텍스트 (body-2 / 500 + fg-subtle) |
| `trailing` | 우측 (액션, 뱃지, 화살표) |
| `onClick` | 행 전체 탭 가능하게 |
| `divider` | 아래 1px 보더 |

## 사용 예

```tsx
<ListRow
  leading={<Avatar initial="박" tone="nature" />}
  title="박현우"
  subtitle="다양성 점수 72"
  trailing={<Badge tone="success">발견 완료</Badge>}
/>
```

## 안티 패턴

- title 없이 subtitle만 — 위계 무너짐
- trailing에 본문 텍스트 — 그건 별도 카드 패턴으로
