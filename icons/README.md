# 아이콘

## 원칙

- **Lucide stroke 스타일만 사용** (https://lucide.dev/ 기반)
- 이모지 절대 금지
- 1.5~2px stroke, round join, 24×24 viewBox
- 색은 `currentColor` (상속)

## 셋

| 카테고리 | 예시 |
|---|---|
| 네비 | `home`, `compass`, `book-open`, `users`, `user` |
| 액션 | `arrow-left`, `close`, `heart`, `share-2`, `more-horizontal` |
| 상태 | `check`, `alert-triangle`, `info`, `clock` |
| 카테고리 | `mountain`, `landmark`, `palette`, `sparkles` (4계열) |
| 도메인 | `target` (발견), `map-pin` (위치), `book-marked` (도감) |

## 추가 가이드

- 새 아이콘 추가 시 Lucide에 같은 의미의 아이콘이 있는지 먼저 확인
- 없으면 동일 톤(stroke 2, round)으로 자체 SVG 작성
- 모든 아이콘은 같은 viewBox(24×24)와 stroke 두께 유지

## 광역 실루엣

17광역의 추상화된 SVG path는 별도 카테고리. Phase 1에서 본 저장소 `assets/regions.json` 으로 이관.
