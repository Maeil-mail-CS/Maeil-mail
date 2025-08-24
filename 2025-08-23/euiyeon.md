<details>
<summary> 
Record를 DTO로 사용하는 이유가 뭔가요?</summary>

🔗 질문 링크: [Record를 DTO로 사용하는 이유가 뭔가요?
](http://maeil-mail.kr/question/107)

✅ 답변 내용:
<pre>
  레코드는 생성자와 getter, setter를 자동으로 만들어주기 때문에
  코드를 훨씬 간결하게 작성 가능
  불변을 보장하기 때문에 변경을 막을 수 있다.

  dto는 요청을 받거나 응답으로 데이터를 담는 역할로 
  요청 응답에서 불변을 보장하는게 필요하면 필요하다.

  간결하기 위해 레코드를 생성한다.
</pre>

💡 꼬리 질문1: 그럼 Record로 생성한 모든 객체는 DTO인가요?
<pre>
  아닙니다. 레코드는 dto와 부합하기 때문에 사용하는거지 무조건 dto는 아닙니다.
</pre>
- 이 답변에 대해 레코드는 `"데이터를 캡슐화 하는 역할"`이라는 점을 보완하면 좋을 것 같다


💡 꼬리 질문2: Record와 VO를 비교해주세요 
<pre>
  VO를 잘 모르겠습니다.
</pre>
### VO(Value Object)란?
- 값 자체가 중요한 객체(고유 식별자(ID)❌)
- **내부 값이 같으면 같은 객체로 취급**
- DB 테이블 컬럼과 매칭되는 **단순 데이터 보관용 객체**

### Record와 VO 비교
```
Record와 VO는 모두 객체의 상태가 변경되지 않는 것을 보장합니다.
또 데이터를 캡슐화하여 표현하는 데 초점을 맞춥니다.
마지막으로 VO는 값 기반의 동등성을 가지며, Record도 동일한 필드 값을 가지면 동일한 객체로 간주된다는 점이 공통점입니다.

VO는 도메인 모델내에서 특정 개념을 표현하고, 도메인 로직과 밀접하게 관련이 있습니다.
즉, VO는 비즈니스 로직이나 규칙을 가질 수 있습니다.
반면에 Record는 단순히 데이터를 캡슐화하여 전달하는데 의미가 있습니다.

결론적으로 Record는 VO를 구현하는 데 적합하지만, VO의 모든 특성을 완벽히 대체하지는 않습니다.
VO는 더 넓은 도메인 맥락에서 사용되며, 비즈니스 로직을 포함할 수 있습니다.
```

💡 꼬리 질문3: Record의 한계는 뭐가 있을까요? 
<pre>
  변경이 필요한 경우 변경이 안되고 새로운 객체로 만들어야 되서 이런 문제가 한계이다.
</pre>
### Record의 한계
1. 다른 클래스 상속(`extends`) 불가
2. 모든 필드가 `final`로 선언되므로 확장에 제한
3. 데이터 전달 목적으로 설계되어 비지니스 로직에 부적절
4. 4. 자바 14/16 이전버전에서 호환 불가

📝 피드백 내용:
<pre>
  record 메서드에 setter는 없습니다.
</pre>

✨ 질문에 대한 보충 학습 내용:
<pre>
  "필드 선언만으로 자동으로 생성자, getter, equals(), hashCode(), toString() 등 메서드를 자동으로 생성해 보일러 플레이트 코드 감소"
  "멀티 스레드 환경에서 데이터가 의도치 않게 변경되지 않고 안전하게 전달 가능"
</pre>

**기존 클래스 기반 DTO**
```java
public class MemberDto {

    private final String name,
    private final String email,
    private final int age

    pulbic MemberDto(String name, String email, int age) {
        this.name = name;
        this.email = email;
        this.age = age;
    }

    public String getName(){
        return name;
    }

    public String getEmail(){
        return email;
    }

    public int getAge(){
        return age;
    }
}
```

**레코드 기반 DTO**  
쩌..쩐당!! 
```java
public record MemberDto(
    String name,
    String email,
    int age
){}
```

👀 참고 링크:
  
</details>
