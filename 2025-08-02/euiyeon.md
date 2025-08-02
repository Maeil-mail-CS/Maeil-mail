<details>
<summary> 
TCP 3-way handshake에 대해서 설명해주세요.
</summary>

🔗 질문 링크: [TCP 3-way handshake에 대해서 설명해주세요.](https://www.maeil-mail.kr/question/76)

✅ 답변 내용:
<pre>
  TCP 3-way handshake는 TCP/IP 프로토콜을 사용하는 네트워크에서 양쪽 호스트가 
  데이터 전송을 하기 전에 연결을 수립하는 과정입니다.
  연결을 요청하는 클라이언트가 SYN 신호를 보내면,
  서버는 연결을 수락한다는 ACK 신호와 함께 서버도 클라이언트 측에 연결을 요청하는 SYN 신호를 보내고(ACK + SYN)
  다시 클라이언트는 서버의 요청에 대한 응답으로 ACK 신호와 함께 데이터를 전송합니다.
</pre>

💡 꼬리 질문1: 4-way handshake에 대해 설명해주세요
<pre>
  3-way handshake가 데이터 전송을 위한 연결을 수립하는 과정이라면,
  4-way handshake는 연결을 해제하는 과정으로 알고 있습니다.
  좀 더 안정적인 연결 해제를 위해 사용하는 방식으로 알고 있지만
  자세한 과정은 모르곘습니다.
</pre>

✨ 질문에 대한 보충 학습 내용:
<pre>
  4-way handshake는 연결을 종료하는 과정인만큼,
  연결 종료를 요청/시도하는 FIN 플래그가 존재한다.
  그리고 데이터 유실을 방지하기 위해 FIN-ACK 플래그를 주고 받고 TIME_WAIT이라는 일정 시간 대기 상태를 거친 뒤
  연결을 종료한다.
</pre>

👀 참고 링크:  
네트워크 노션 페이지 복습하장
</details>
