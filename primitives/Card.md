# Card

표면. 화면의 정보 그룹 단위.

## Props

| prop | 기본 | 설명 |
|---|---|---|
| `padding` | `var(--gap-card)` (16) | 내부 패딩 |
| `radius` | `var(--radius-lg)` (16) | 라운드 |
| `elevated` | `false` | 그림자 사용 여부 |
| `tone` | `surface` | 배경 톤 (`surface` \| `subtle` \| `inverse`) |
| `as` | `div` | 시맨틱 변경 가능 |

## 사용 예

```tsx
<Card padding={20} elevated>
  <h3>오늘의 추천</h3>
</Card>

<Card tone="inverse" radius={24}>
  <ProfileHero />
</Card>
```

## 안티 패턴

- 카드 안의 카드: 시각 위계 무너짐
- 카드 외부에 그림자 + 카드 내부에도 그림자
- 너무 작은 카드 (radius보다 가로폭이 작음)
