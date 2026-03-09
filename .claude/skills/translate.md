# /translate — 섹션 번역

README.md의 특정 섹션을 한국어로 번역하여 보여주고, `ko/` 디렉토리에 저장하는 skill이다.

## 동작 절차

1. 사용자가 요청한 섹션명을 파악한다.
   - 예: `/translate React` → "React & Modern Frameworks" 섹션
   - 예: `/translate JavaScript` → "JavaScript Core" 섹션
   - 예: `/translate all` → README.md 전체

2. `ko/` 디렉토리에 해당 섹션의 번역 파일이 있는지 확인한다.
   - 섹션별 파일 명명 규칙: `ko/섹션명.ko.md`
     - 예: `ko/react.ko.md`, `ko/javascript-core.ko.md`, `ko/html-css.ko.md`
   - 전체 번역: `ko/README.ko.md`

3. 번역 파일이 이미 존재하면:
   - 해당 파일의 내용을 그대로 보여준다.
   - "이미 번역된 파일입니다"라고 안내한다.

4. 번역 파일이 없으면:
   - README.md에서 해당 섹션을 찾아 한국어로 번역한다.
   - 번역 시 다음을 유지한다:
     - 마크다운 형식 (표, 코드 블록, 링크)
     - 원문의 URL 링크
     - 기술 용어는 영어 병기 (예: "클로저(Closure)")
   - 번역 결과를 `ko/` 디렉토리에 파일로 저장한다.
   - 번역 내용을 사용자에게 보여준다.

## 섹션 매핑

| 키워드 | README 섹션 | 파일명 |
|--------|------------|--------|
| html, css, 기초 | Fundamentals: HTML & CSS | `ko/html-css.ko.md` |
| javascript, js | JavaScript Core | `ko/javascript-core.ko.md` |
| react | React & Modern Frameworks | `ko/react.ko.md` |
| design-patterns, 패턴 | Design Patterns | `ko/design-patterns.ko.md` |
| dsa, 알고리즘 | Data Structures & Algorithms | `ko/dsa.ko.md` |
| system-design, 시스템 | Frontend System Design | `ko/system-design.ko.md` |
| testing, 테스팅 | Testing & QA | `ko/testing.ko.md` |
| a11y, 접근성 | Accessibility | `ko/accessibility.ko.md` |
| performance, 성능 | Performance & Web Vitals | `ko/performance.ko.md` |
| tooling, 빌드 | Tooling, Build & Deploy | `ko/tooling.ko.md` |
| machine-coding | Machine Coding Rounds | `ko/machine-coding.ko.md` |
| ai | Bonus: Frontend with AI | `ko/frontend-ai.ko.md` |
| communication, 리더십 | Communication & Technical Leadership | `ko/communication.ko.md` |
| interview-kit, 면접킷 | Interview Kit | `ko/interview-kit.ko.md` |
| projects, 프로젝트 | Projects & Build List | `ko/projects.ko.md` |
| all, 전체 | 전체 README | `ko/README.ko.md` |

## 응답 언어

반드시 한국어로 응답한다.
