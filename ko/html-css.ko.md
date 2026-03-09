# 기초: HTML & CSS

## 리소스

**[W3Schools HTML/CSS](https://www.w3schools.com/html/)**
*이유:* 문법과 속성을 가장 빠르게 참고할 수 있는 레퍼런스.
*활용법:*
- **학습 계획:** 3일, 하루 1시간. 시맨틱 HTML5(`<article>`, `<section>`, `<nav>`), 폼, 접근성 속성에 집중.
- **면접 포인트:** "저는 시맨틱 HTML을 사용합니다. SEO, 스크린 리더 호환성, 유지보수성이 향상되기 때문입니다. `<button>`은 `<div>`에는 없는 키보드 내비게이션이 내장되어 있습니다."
- **주의사항:** 모든 HTML 엔티티를 외울 필요 없음. 자주 쓰는 것만 알면 됨 (`&nbsp;`, `&lt;`, `&gt;`).
- **연습:** JavaScript 없이 이메일, 전화번호 유효성 검사가 있는 폼 만들기.

**[web.dev (Google)](https://web.dev/learn/html/)**
*이유:* 최신 모범 사례, Core Web Vitals 통합.
*활용법:*
- **학습 계획:** HTML + CSS 모듈 5일. `<picture>`, `srcset`, CSS containment 메모하기.
- **면접 스크립트:** "반응형 이미지에는 `<picture>`에 WebP와 JPEG 폴백을 사용합니다. 이전 프로젝트에서 LCP를 40% 줄였습니다."
- **연습:** CSS Grid로 반응형 카드 그리드 구현하기 (프레임워크 없이).

**[CSS-Tricks Flexbox/Grid 가이드](https://css-tricks.com/)**
*이유:* 멘탈 모델을 위한 시각적 다이어그램.
*활용법:*
- Flexbox와 Grid 치트시트를 인쇄. 5가지 일반적인 레이아웃 재현하기 (홀리 그레일, 사이드바, 매이슨리 스타일).
- **면접:** "Grid는 2D 레이아웃용, Flexbox는 1D용입니다. 대시보드에는 Grid, 내비게이션 바에는 Flexbox를 쓰겠습니다."

## 연습 체크리스트

```markdown
- [ ] 암기: Box model, 명시도(Specificity) 규칙, BEM 명명법
- [ ] 실험: CSS 커스텀 속성(변수), `@layer`, 컨테이너 쿼리(Container Queries)
- [ ] 빌드: 랜딩 페이지(모바일 퍼스트), CSS 전용 툴팁, 다크 모드 토글
- [ ] 접근성: `:focus-visible` 사용, 4.5:1 대비 비율 확보, 스크린 리더로 테스트
```

## 팁

- 매일 브라우저 DevTools를 사용하세요. 요소를 검사하고, CSS를 실시간 수정하고, 규칙을 외우기보다 Box model을 시각적으로 이해하세요.
- 개인 "Flexbox 놀이터" CodePen을 만들어 다양한 flex 속성을 테스트하세요. 레이아웃 면접에서는 이론보다 근육 기억이 낫습니다.
- CSS Grid는 문서를 읽기보다 실제 레이아웃(대시보드, 매거진 스타일, 포토 갤러리)을 만들면서 배우세요. 실전 경험이 더 오래 남습니다.
- CSS 디버깅 시, 브라우저의 계산된 스타일(Computed Styles) 패널부터 확인하세요. 실제 적용된 값을 보면 명시도 문제를 빠르게 잡을 수 있습니다.

**태그:** `#기초` `#html` `#css` `#접근성`
