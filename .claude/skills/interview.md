# /interview — 모의 면접 연습

완료한 학습 범위 내에서 프론트엔드 면접 질문을 출제하고 답변을 평가하는 skill이다.

## 동작 절차

1. `ko/progress.md`를 읽어 완료된 주차와 항목을 파악한다.

2. 면접 모드를 결정한다:
   - `/interview` — 완료한 전체 범위에서 랜덤 출제
   - `/interview react` — React 관련 질문만 출제
   - `/interview js` — JavaScript 관련 질문만 출제
   - `/interview system` — 시스템 설계 질문 출제

3. 질문을 출제한다:
   - README.md의 "Interview Talking Points", "Interview Script", "Interview Explanation Template" 등을 참고하여 면접 질문을 만든다.
   - 질문은 한국어로 하되, 기술 용어는 영어를 병기한다.
   - 난이도: 기본 → 심화 → 꼬리 질문 순서로 진행한다.

4. 질문 형식:
   ```
   🎤 모의 면접 — React 심화

   Q1. React에서 가상 DOM(Virtual DOM)의 재조정(Reconciliation) 과정을 설명해주세요.
       Key가 중요한 이유는 무엇인가요?

   답변을 입력해주세요. (모르겠으면 "패스"라고 입력)
   ```

5. 사용자 답변을 평가한다:
   - 핵심 키워드 포함 여부 확인
   - 부족한 부분을 보충 설명
   - README의 Interview Script를 한국어로 번역하여 모범 답변으로 제시
   - 평가 형식:
     ```
     📝 평가:
     ✅ 좋은 점: Virtual DOM 비교 과정을 정확히 설명했습니다.
     💡 보완할 점: Key의 역할에 대해 더 구체적으로 설명하면 좋겠습니다.

     📖 모범 답변:
     "React의 재조정은 가상 DOM 트리를 비교하는 과정입니다. Key는 React가
     어떤 항목이 변경되었는지 식별하는 데 도움을 줍니다. Key가 없으면
     불필요한 리렌더링이 발생할 수 있습니다."

     다음 질문으로 넘어갈까요? (계속 / 그만)
     ```

6. 세션 종료 시 요약을 제공한다:
   ```
   📊 면접 연습 결과
   - 총 질문: 5개
   - 잘 답변: 3개
   - 보완 필요: 2개
   - 약한 영역: 이벤트 루프, 프로토타입
   ```

## 출제 범위 매핑

| 키워드 | 출제 범위 |
|--------|----------|
| html, css | Fundamentals: HTML & CSS |
| js, javascript | JavaScript Core |
| react | React & Modern Frameworks |
| patterns, 패턴 | Design Patterns |
| dsa, 알고리즘 | Data Structures & Algorithms |
| system, 시스템 | Frontend System Design |
| testing, 테스팅 | Testing & QA |
| a11y, 접근성 | Accessibility |
| performance, 성능 | Performance & Web Vitals |

## 응답 언어

반드시 한국어로 응답한다.
