# JavaScript 핵심

## 리소스

**[JavaScript.info](https://javascript.info/)**
*이유:* 기초부터 고급(이벤트 루프, 마이크로태스크)까지 가장 잘 구조화된 튜토리얼.
*활용법:*
- **학습 계획:** 2주. 하루 2챕터 읽기. 인라인 연습 문제 풀기.
- **면접 핵심:** 4장(객체), 6장(함수), 11장(Promise), 14장(이벤트 루프).
- **주의사항:** 이벤트 루프를 대충 읽지 마세요. 직접 다이어그램을 그려보세요 (콜 스택, Web API, 태스크 큐, 마이크로태스크 큐).
- **연습:** `Promise.all`을 처음부터 구현하고, `Promise.allSettled`와의 차이를 설명하기.

**[Namaste JavaScript (YouTube 재생목록)](https://www.youtube.com/playlist?list=PLlasXeu85E9cQ32gLCvAvr9vNaUccPVNP)**
*이유:* 클로저(Closure), 호이스팅(Hoisting), `this`, 프로토타입(Prototype)의 시각적 설명.
*활용법:*
- **학습 계획:** 하루 2개 영상 시청 (각 20-40분). 일시정지하고 함께 코딩.
- **면접 스크립트:** "클로저란 내부 함수가 외부 함수의 스코프에 대한 접근을 외부 함수가 반환된 후에도 유지하는 것입니다. 이를 통해 데이터 프라이버시와 팩토리 패턴이 가능합니다."
- **연습:** `debounce` 함수를 작성하고 클로저가 왜 중요한지 설명하기.

**[You Don't Know JS (GitHub 책 시리즈)](https://github.com/getify/You-Dont-Know-JS)**
*이유:* 타입 변환(Coercion), 스코프(Scope), `this`, 프로토타입, 비동기(Async) 심층 분석.
*활용법:*
- **학습 계획:** 주 1권 읽기 (Scope & Closures부터 시작, 이후 this & Object Prototypes).
- **면접:** "JavaScript에서 `this`는 함수가 정의된 곳이 아니라 호출되는 방식에 따라 결정됩니다. 화살표 함수는 둘러싸는 스코프에서 `this`를 렉시컬하게 바인딩합니다."
- **주의사항:** 책이 밀도가 높습니다. 메모하고 예제를 만들어보세요.
- **연습:** `call`, `apply`, `bind`의 차이를 코드로 설명하기.

**[Learners Bucket](https://learnersbucket.com/)**
*이유:* 실전 JavaScript 문제, 폴리필, 프론트엔드 면접 질문.
*활용법:*
- **학습 계획:** 1주. JavaScript 섹션에 집중. `map`, `filter`, `reduce`, `bind`, `call`, `apply` 폴리필 구현.
- **면접 핵심:** "폴리필" 섹션. 면접관이 "Array.prototype.map을 처음부터 구현해보세요"라고 자주 물어봅니다.
- **실전 연습:** JS로 자료구조 구현 (연결 리스트, 큐, 스택, 트라이).
- **면접 스크립트:** "`Promise.all` 폴리필을 구현했는데, 거부(rejection)를 올바르게 처리하고 resolved 값의 순서를 유지합니다."
- **주의사항:** 솔루션을 그냥 복사하지 마세요. 기본 개념을 이해하세요 (bind의 클로저, 배열 메서드의 반복 패턴).
- **연습:** `Function.prototype.bind`를 구현하고 클로저를 사용해 컨텍스트를 보존하는 방법을 설명하기.

## 면접 핵심 개념

| 개념 | 암기할 내용 | 면접 설명 템플릿 |
|------|------------|-----------------|
| **클로저(Closure)** | 내부 함수 + 외부 스코프 | "데이터 캡슐화에 사용됩니다. 모듈 패턴과 고차 함수를 가능하게 합니다." |
| **이벤트 루프(Event Loop)** | 콜 스택 → Web API → 태스크 큐 → 마이크로태스크 큐 | "마이크로태스크(Promise)가 매크로태스크(setTimeout)보다 먼저 실행됩니다. 그래서 Promise.then이 setTimeout 0보다 먼저 로그됩니다." |
| **프로토타입(Prototype)** | 모든 객체에 `[[Prototype]]` 있음; class는 문법적 설탕 | "프로토타입 체인을 통한 상속. `class`가 더 깔끔하지만 내부적으로는 프로토타입을 사용합니다." |
| **메모리 누수(Memory Leak)** | 분리된 DOM, 전역 변수, 이벤트 리스너 | "정리(cleanup)에서 항상 리스너를 제거하세요. 캐시에는 WeakMap을 사용하세요." |
| **비동기 패턴(Async)** | 콜백 → Promise → async/await | "async/await는 Promise의 문법적 설탕입니다. try/catch로 에러 처리가 더 쉬워집니다." |

## 팁

- 이벤트 루프를 종이에 여러 번 그려서 마스터하세요. 면접에서 실행 순서를 설명할 때 시각적 기억이 도움됩니다.
- JavaScript 개념을 주니어 개발자에게 가르치듯 소리 내어 설명 연습하세요. 간단히 설명할 수 없다면 충분히 이해하지 못한 것입니다.
- Chrome DevTools 디버거를 적극 활용하세요. 브레이크포인트 설정, 클로저 검사, 콜 스택 관찰. 직접 디버깅하는 것이 읽는 것보다 낫습니다.
- 매일 작은 코드 스니펫으로 엣지 케이스를 테스트하세요: 화살표 함수에서 `this`는 어떻게 되나요? `Promise.race`는 거부된 Promise에 어떻게 동작하나요?

**태그:** `#javascript` `#기초` `#비동기` `#클로저`
