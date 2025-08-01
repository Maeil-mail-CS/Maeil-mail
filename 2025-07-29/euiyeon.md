<details>
<summary> 
스레드, 프로세스, 코어의 수는 많을수록 좋을까요?
</summary>

🔗 질문 링크: [스레드, 프로세스, 코어의 수는 많을수록 좋을까요?](https://www.maeil-mail.kr/question/84)

✅ 답변 내용:
<pre>
1. 프로세스 수가 많으면?
프로세스는 CPU를 나눠서 쓰는 시분할 시스템내에서 실행되기 때문에,  
프로세스 수가 증가할 수록 문맥교환(Context Switching) 비용 증가가 우려됨

2. 스레드 수가 많으면?
스레드는 프로세스의 작업 단위이기 때문에, 스레드 수가 증가하면  
프로세스의 작업 효율이 일시적으로 좋아질 수 있으나  
스레싱(Thrashing) 현상 발생 가능성 

3. 코어 수가 많으면?
명확한 답변❌
단, 코어의 수가 많아질 수록 관리해야 할 자원의 수가 증가하기 때문에  
시스템의 복잡도나 관리 비용이 증가할 것으로 예상된다고 답변함
</pre>
  
✨ 질문에 대한 보충 학습 내용:
<pre>
1. 프로세스
- 문맥 교환 비용 증가
- 독립 메모리 공간으로 인한 자원 소모
- 운영체제 한계

2. 스레드
- 문맥 교환 비용 증가
- 자원 경쟁(락, 메모리, 캐시)로 인한 성능저하 및 데드락
- 동기화와 상태 관리 복잡으로 인한 버그 발생 가능성 증가

추가설명:
"일시적 효율 향상"이라는 표현은 모호함
"동시성 향상"이나 "병렬 처리 증가 가능"으로 좀 더 정확히 표

스레싱은 단순히 스레드 수 많아서가 아니라 
자원 초과 사용 시 컨텍스트 스위칭만 반복되는 상태이니, 정확한 조건 명시
  
3. 코어
- 멀티코어의 이점은 병렬 처리 가능한 소프트웨어일 때에만
- 단일 스레드 프로그램에서는 성능 향상❌
- 코어 수가 증가하면 전력, 발열, 비용 증가
</pre>
👀 참고 링크:
  
</details>


<details>
<summary> 
단위 테스트와 통합 테스트의 차이점은 무엇인가요?
</summary>
  
🔗 질문 링크: [단위 테스트와 통합 테스트의 차이점은 무엇인가요?](https://www.maeil-mail.kr/question/83)

✅ 답변 내용:
<pre>
1. 단위 테스트
애플리케이션에서 가장 작은 단위(함수)의 기능을 테스트

2. 통합 테스트
앞서 얘기한 작은 단위들이 모두 결합된 형태의 애플리케이션을 통합적으로 테스트
</pre>

💡 꼬리 질문1: 슬라이스 테스트란?
<pre>
잘 모르겠습니다.
</pre>

💡 꼬리 질문2: 테스트 코드를 작성해야되는 이유?
<pre>
- 개발자의 의도대로 기능이 동작하는지 확인하기 위해
- 문제를 조기에 발견하기 위해
</pre>

✨ 질문에 대한 보충 학습 내용:
1. 단위 테스트와 통합 테스트
- 단위 테스트의 독립성과 빠른 실행
- 통합 테스트의 실제 환경과 외부 시스템과의 통합 여부를 답변에 포함시킬 것
- 보완된 답변:
<pre>
단위 테스트(Unit Test)는 애플리케이션의 가장 작은 단위인 함수 또는 메서드의 동작을 독립적으로 검증하는 테스트입니다. 
외부 의존성 없이 테스트 대상 로직만 빠르게 실행하며, 문제를 조기에 발견하고 리팩터링 시 신뢰할 수 있는 기반이 됩니다.

통합 테스트(Integration Test)는 여러 단위(모듈, 클래스, 레이어 등)가 실제 환경처럼 연결된 상태에서, 
이들이 올바르게 상호작용하는지 확인하는 테스트입니다. 
DB, 메시징 시스템, 외부 API 등 실제 의존성과 함께 실행되므로 느리지만 현실과 유사한 시나리오를 검증할 수 있습니다.
</pre>

2. 슬라이스 테스트
<pre>
슬라이스 테스트는 애플리케이션의 특정 계층(ontroller, Repository 등)만 잘라서 테스트하는 방식입니다.  
Spring에서는 `@WebMvcTest`, `@DataJpaTest` 같은 어노테이션을 통해 해당 레이어만 로드하여 테스트할 수 있고, 
통합 테스트보다 가볍고 빠르게 실행됩니다.
</pre>

4. 테스트 코드를 작성해야 되는 이유
- 개발 생산성, 리팩터링 안정성, 문서 역할 등의 실무적인 가치들을 덧붙여 완성도를 높일 것
- 보완된 답변:
<pre>
버그를 조기에 발견하여 문제를 미리 방지할 수 있습니다.
리팩터링을 할 때 기존 동작이 유지되는지 확인할 수 있어, 안정성을 보장합니다.
반복적인 수동 테스트를 줄여 개발 속도를 높일 수 있습니다.
테스트 코드는 해당 기능의 사용법과 동작 조건을 보여주는 문서 역할도 합니다.
</pre>
