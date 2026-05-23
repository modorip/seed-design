# Progress

진행률 막대.

## Props

| prop | 기본 | 설명 |
|---|---|---|
| `value` | 0 | 0~1 (또는 `valueMax`와 함께 0~N) |
| `valueMax` | 1 | 최대값 |
| `tone` | `primary` | 톤 |
| `height` | 6 | px |
| `radius` | `full` | 라운드 |
| `track` | `subtle` | 트랙 톤 |

## 사용 예

```tsx
<Progress value={0.65} tone="primary" />
<Progress value={73} valueMax={100} tone="nature" height={8} />
```

## 애니메이션

값 변경 시 320ms `--ease-out-standard` 로 width 전환.

## 접근성

`role="progressbar"`, `aria-valuenow`, `aria-valuemin`, `aria-valuemax` 자동 부여.
