# Avatar

사용자·탐험가 표현. 이미지 + fallback 이니셜.

## 사이즈

| size | px |
|---|---|
| `xs` | 24 |
| `sm` | 32 |
| `md` | 40 (기본) |
| `lg` | 56 |
| `xl` | 80 |
| `2xl` | 120 (프로필 히어로) |

## 변형

- `image`: src 제공 시
- `initial`: src 없거나 로드 실패 시, 이니셜 + tone 색 배경
- `placeholder`: 둘 다 없을 때, 사람 실루엣 아이콘

## 사용 예

```tsx
<Avatar src={user.photo} fallback={user.name[0]} tone="primary" />
<Avatar initial="박" tone="nature" size="lg" />
```

## 그룹

`AvatarGroup` 으로 -8px 음수 마진 겹침 표현. 5명 초과 시 `+N`.

## 안티 패턴

- 사이즈를 px로 직접 — 항상 토큰 size 사용
- 이미지 로드 실패 시 깨진 아이콘 노출 — initial fallback 필수
