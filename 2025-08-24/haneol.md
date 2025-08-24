<details>
<summary> 
  자바에서 Checked Exception과 Unchecked Exception에 대해서 설명해주세요.
</summary>

🔗 질문 링크: [자바에서 Checked Exception과 Unchecked Exception에 대해서 설명해주세요.](https://www.maeil-mail.kr/question/50)

✅ 답변 내용:
<pre>
  Checked Exception는 반드시 잡아야하는 오류,.. 에러고요
  Unchecked Exception는 잡지 않아도 되는 에러입니다.

  Checked Exception 반드시 잡아야 하기 때문에 명시적으로 에러가 발생한다는 것을 개발자들에게 알릴 수 있는 에러입니다.
  그래서 try-catch나 throws를 통해 외부로 예외를 전파하는 용입니다.

  Unchecked Exception은 잡지 않아도 되기 때문에 상단에서 최종 메인이나 루트쪽에서 잡거나 유연하게 대처 가능한 에러입니다.
  
</pre>

💡 꼬리 질문1: 각각 언제 사용해야 할까요?🤔
<pre>
  Checked Exception같은 경우에느 개발자들에게나 누군가 이 메서드를 썻을 때 명시적으로 발생할 수 있는 
  Exception, Runtime Exception을 상속하지 않은 ... ,,  
  에러를 try-catch나 throws로 처리하도록 의도할 때 사용하고요

  Unchecked Exception는 반드시 잡지 않아도 되는 에러이기 때문에 
  사용자가 예상이 가거나 유연하게 대처할 수 있는 형식의 Runtime Exception을 상속하는 모든 Exception

  그래서 데이터베이스인 경우 I/O, Duplicate와 같은 치명적인 오류인 경우 Checked Exception을 Runtime Exception으로 감싸서 전달 
</pre>

💡 꼬리 질문2: Error와 Exception의 차이는 무엇인가요?🤓
<pre>
  Error는 치명적인 에러로 Out of memory와 같은.. 치명적인 오류
  Exception은 사용자가 예측 가능하거나 치명적이지 않은 오류(I/O, Runtimem)로 해결가능한 오류를 Exception이라고 합니다.
</pre>

📝 피드백 내용:
<pre>
  1. 답변을 듣는데 어지러워요 ... 주어와 어미 일치시키기
  2. Checked Exception과 Unchecked Exception을 설명할 때 "시점"에 대한 언급이 있었으면 좋겠음(컴파일 시점, 런타임 시점)
  3. 답변의 흐름 신경쓰기 !!!! 
  (꼬리질문2에서 Checked Exception 설명 -> 
                Unchecked Exception 설명 -> 
                예외적으로 Checked Exception을 Unchecked Exception으로 감싸서 전달하는 경우 설명)
</pre>

✨ 질문에 대한 보충 학습 내용:
<pre>
- 학습한 내용
- 또는 답변에 보완하면 좋았을 내용
</pre>

👀 참고 링크:
  
</details>
