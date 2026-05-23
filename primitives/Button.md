# Button

기본 CTA. 시각 위계의 핵심.

## 변형 (variant)

| variant | 용도 |
|---|---|
| `primary` | 화면당 1~2개, 메인 액션 |
| `neutral` | 보조 액션, 회색 톤 |
| `outline` | 경계만, 캔슬 등 |
| `subtle` | 약한 강조 |
| `ghost` | 텍스트 링크 같은 |
| `soft` | 톤 다운된 컬러 채움 |

## 톤 (tone)

`primary` | `neutral` | `success` | `warning` | `danger` | `info`. variant와 직교.

## 사이즈

| size | height | padding | font |
|---|---|---|---|
| `sm` | 32 | 0 12 | body-2 / 600 |
| `md` | 40 | 0 16 | body-1 / 700 |
| `lg` | 48 | 0 20 | body-1 / 700 |
| `xl` | 56 | 0 24 | title-3 / 700 |

## 상태

- `loading`: 스피너 + 텍스트 가림 (너비 유지)
- `disabled`: opacity 0.4 + cursor not-allowed
- 호버: 톤 한 단계 진하게 (200ms ease-out-standard)

## 사용 예 (Phase 1 React)

```tsx
<Button variant="primary" size="lg">여기에서 발견하기</Button>
<Button variant="outline" tone="neutral">취소</Button>
<Button variant="soft" tone="danger" loading>처리 중</Button>
```

## 안티 패턴

- 같은 화면에 primary 버튼 3개 이상
- 텍스트만 있는 버튼은 height 미보장
- 위험한 액션을 primary로
