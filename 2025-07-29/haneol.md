
<details>
<summary> 
🔗 ResponseBody(or ResponseEntity)가 있을 때와 없을 때의 동작 방식의차이점을 말해주세요.
</summary>

링크 https://www.maeil-mail.kr/question/9

<pre>
✅ 답변 내용:
ResponseBody가 있다면 http 응답 본문에 반환값을 쓰게 됩니다. 이때 자바 객체를 자동으로 json, XML 등의 
타입으로 직렬화합니다.
ResponseBody가 없다면 반환값을 view 이름으로 해석을 합니다. 뷰 리졸버에서 뷰 이름에 해당하는 뷰를 반환하게 됩니다.
ResponseBody와 ResponseEntity 반환 중 어떤 방식이 더욱 좋나요?

💡 꼬리 질문:
- 꼬리 질문0
- 꼬리 질문1

👀 참고 링크:

</pre>
</details>

<details>
<summary> 
🔗 Filter와 Interceptor의 차이점을 말해주세요.
</summary>

(https://www.maeil-mail.kr/question/10)

<pre>
✅ 답변 내용: 
Filter는 요청 및 응답의 전처리와 후처리를 수행하고 서블릿 컨테이너에 의해 실행되는 java 클래스입니다.

특징:
서블릿 컨테이너 수준에서 동작한다.
- 필터는 모든 요청이 서블릿으로 전달되기 전에 Filter를 거친다.
- web.xml 이나 @WebFilter 어노테이션을 통해 설정할 수 있으며, 필터의 순서는 설정 파일에서 정의한다.

Interceptor는 특정 핸들러 메서드 실행 전후에 공통 기능을 구현합니다.

특징
Spring MVC의 핸들러 수준에서 동작한다. Dispatcher Servlet이 컨트롤러를 호출하기 전에 Interceptor를 거친다.


💡 꼬리 질문:
- 꼬리 질문0
- 꼬리 질문1
👀 참고 링크: 

</pre>
</details>
