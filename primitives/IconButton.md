# IconButton

아이콘 단독 인터랙티브 요소.

## 변형

| variant | 시각 |
|---|---|
| `outline` | 경계 1px, 투명 배경 |
| `soft` | 옅은 배경, 호버 시 진해짐 |
| `ghost` | 배경 없음, 호버 시 옅은 배경 |
| `inverse` | 다크 배경 위 사용 (흰 아이콘) |

## 사이즈

| size | container | icon |
|---|---|---|
| `sm` | 32 | 16 |
| `md` | 40 (기본) | 20 |
| `lg` | 48 | 24 |

## 필수 사항

- **`aria-label` 필수** (시각적 라벨이 없으므로)
- 컨테이너는 정사각형 (touch target 보장)

## 사용 예

```tsx
<IconButton aria-label="닫기" variant="ghost"><CloseIcon /></IconButton>
<IconButton aria-label="뒤로 가기" variant="soft"><ArrowLeftIcon /></IconButton>
```

## 안티 패턴

- aria-label 누락 → 스크린 리더가 "버튼"이라고만 읽음
- 텍스트 라벨이 명시적으로 필요한 액션 — 그건 Button
