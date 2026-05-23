# BottomSheet

화면 하단에서 올라오는 모달. 선택 자원 미리보기, 액션 시트 등에 사용.

## 구조

```
─ drag handle (4×40, fg-muted)
─ optional title
─ content
─ optional sticky CTA
```

## 동작

- 진입: translate Y(100%) → Y(0), 320ms `--ease-out-standard`
- 닫기: 백드롭 탭, drag-down (40px 이상), ESC 키
- 백드롭: `rgba(0,0,0,0.32)`, 탭 시 닫힘

## 사이즈

- `auto`: 콘텐츠 크기만큼
- `half`: 뷰포트 50%
- `full`: 상단 인셋 16 남기고 풀스크린

## 접근성

- `role="dialog"`, `aria-modal="true"`
- 포커스 트랩: 오픈 시 첫 인터랙티브 요소로 포커스
- 닫기 시 트리거 요소로 포커스 복귀

## 사용 예

```tsx
<BottomSheet open={open} onClose={close} size="auto">
  <SelectedPlaceCard place={place} />
  <Button variant="primary" size="lg">여기에서 발견하기</Button>
</BottomSheet>
```
