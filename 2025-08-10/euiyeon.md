<details>
<summary> 
@Component, @Controller, @Service, @Repository의 차이점에 대해서 설명해주세요.
</summary>

🔗 질문 링크: [질문내용](https://www.maeil-mail.kr/question/72)

✅ 답변 내용:
<pre>

컴포넌트는 스프링 컨테이너가 자동으로 관리해주는 bean을 명시해주는 어노테이션이다.

스프링에 의해 관리되기 때문에 의존성 주입이 자동으로 된다.

controller는 외부 요청을 처리, 응답 반환

service는 애플리케이션의 비즈니스를 처리하는 계층

repository는 데이터베이스에 접근하는 계층으로 분리한다.

</pre>

💡 꼬리 질문1: @Controller, @Repository 대신 @Component 사용하면 안되나요?
<pre>
사용해도 되지만 명시되지 않아서 역할이나 가독성에 대해서 문제가 있을 수 있다.
</pre>

📝 피드백 내용:
<pre>

각 계층의 역할을 알고 있고 componentScan에 의해 빈 주입과 스프링 컨테이너의 동작 과정을 어느정도 알고 있다고 느껴졌다.

하지만, 각 계층의 어노테이션의 기능을 명확하게는 알지 못하는 느낌으로 그냥 사용하는 정도로만 느껴졌다.

추후 학습이 필요할 것 같습니다.

</pre>

✨ 질문에 대한 보충 학습 내용:
<pre>
- 학습한 내용
- 또는 답변에 보완하면 좋았을 내용
</pre>

👀 참고 링크:
  
</details>
