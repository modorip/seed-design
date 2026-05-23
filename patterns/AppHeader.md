# AppHeader

화면 상단 헤더. 서브타이틀 + 큰 타이틀 + 우측 트레일링 액션 구조.

## 구조

```
[serial: 서브타이틀 caption-1 / 600 / fg-subtle]
[title: title-1 / 800 / -0.02em letter-spacing]                [trailing]
```

## 변형

- 기본: 좌측 정렬, 우측 trailing 액션
- 뒤로 가기 모드: leading에 IconButton(arrow-left), 타이틀은 한 줄
- 다크 모드 (히어로): 다크 배경 + 흰 텍스트 (프로필 화면)

## 사용 예

```tsx
<AppHeader
  subtitle="전국 도감"
  title="대한민국"
  trailing={<SegmentedControl ... />}
/>
```

## 인터랙션

- 스크롤 시 헤더 collapse: title 크기 축소, 그림자 노출 (Phase 1 옵션)
