# 원시 컴포넌트 (Primitives)

토큰 위에 만든 가장 기본적인 빌딩 블록. 모든 화면은 이 컴포넌트들의 조합입니다.

## 목록

| 컴포넌트 | 문서 |
|---|---|
| Button | [Button.md](./Button.md) |
| Badge | [Badge.md](./Badge.md) |
| Chip | [Chip.md](./Chip.md) |
| Avatar | [Avatar.md](./Avatar.md) |
| IconButton | [IconButton.md](./IconButton.md) |
| Card | [Card.md](./Card.md) |
| ListRow | [ListRow.md](./ListRow.md) |
| Progress | [Progress.md](./Progress.md) |

## API 원칙

1. **모든 prop은 선택적이거나 합리적 기본값**
2. **variant + tone 분리**: 모양(`variant`)과 색(`tone`)은 직교
3. **as 또는 asChild**: 시맨틱 변경 가능
4. **forwardRef**: 모든 컴포넌트가 DOM ref 전달

## 접근성 기본

- 모든 인터랙티브 요소: 키보드 포커스 가능
- 포커스 가시화: `outline: 2px solid var(--color-primary); outline-offset: 2px`
- 비활성화: `disabled` 속성 + `aria-disabled`
- 컬러 외 의미 전달: 아이콘·텍스트 동반
