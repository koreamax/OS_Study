## Chapter 10. 프로세스와 스레드
### 10-3 스레드
- 프로세스 vs 스레드
- 멀티프로세스 vs 멀티스레드


## Chapter 11. CPU 스케줄링
### 11-1 CPU 스케줄링 개요
- 프로세스 우선순위
- 스케줄링 큐
- 선점형 vs 비선점형 스케줄링

**최민경**

1-1. 
<details>
  <summary>정답</summary>
  
</details>

1-2. 
<details> 
  <summary>정답</summary>
  
</details>

2-1. 
<details>
  <summary>정답</summary>
  
</details>

2-2. 
<details>
  <summary>정답</summary>
  
</details>



**방혜윤**

1-1. 
<details>
  <summary>정답</summary>
  
</details>

1-2. 
<details>
  <summary>정답</summary>
  
</details>

2-1. 
<details>
  <summary>정답</summary>
  
</details>

2-2. 
<details>
  <summary>정답</summary>
  
</details>

**이민형**

1-1. IPC 방식 중 파이프에 대해 설명해주세요.
<details>
  <summary>정답</summary>
  파이프는 같은 컴퓨터 안의 프로세스들이 데이터를 주고받는 IPC 방식이다. 커널의 버퍼를 이용하며, 일반적으로 한 프로세스가 데이터를 쓰고 다른 프로세스가 읽는 단방향 통신에 사용된다.<br>

예: cat file | grep hello
</details>

1-2. IPC 방식 중 소켓에 대해 설명해주세요.
<details>
  <summary>정답</summary>
  소켓은 프로세스 간 데이터를 주고받는 양방향 통신 방식이다. 같은 컴퓨터뿐만 아니라 IP 주소와 포트 번호를 이용해 다른 컴퓨터의 프로세스와도 통신할 수 있다.<br>

  예: 웹 브라우저와 웹 서버의 통신
</details>

2-1. 선점형 스케줄링과 비선점형 스케줄링을 설명해주세요.
<details>
  <summary>정답</summary>
  선점형 스케줄링은 운영체제가 실행 중인 프로세스의 CPU 사용을 강제로 중단하고 다른 프로세스에 CPU를 할당하는 방식이다.<br>

비선점형 스케줄링은 실행 중인 프로세스가 종료되거나 스스로 CPU를 반납할 때까지 계속 실행하는 방식이다.
</details>

2-2. 선점형 스케줄링에서 발생하는 오버헤드를 설명해주세요.
<details>
  <summary>정답</summary>
  선점형 스케줄링에서는 다음과 같은 오버헤드가 발생한다.<br>

1. 인터럽트를 처리하는 비용<br>
2. 프로세스의 상태를 저장하고 복원하는 컨텍스트 스위칭 비용<br>
3. 다음 프로세스를 선택하는 스케줄러 연산 비용<br>
4. 시스템 콜 발생 시 사용자 모드와 커널 모드를 전환하는 비용
</details>

2-3. 오버헤드가 발생함에도 선점형 스케줄링을 사용하는 이유를 설명해주세요.
<details>
  <summary>정답</summary>
  특정 프로세스가 CPU를 독점하는 것을 방지하고, 여러 프로세스에 CPU를 공평하게 배분하기 위해 사용한다. 또한 긴급하거나 우선순위가 높은 작업을 빠르게 실행할 수 있어 시스템의 응답성이 향상된다.
</details>

3-1. CPU 관점에서 GPU 집중 프로세스는 CPU 버스트와 I/O 버스트 중 어느 특성이 강한지 설명해주세요.
<details>
  <summary>정답</summary>
  GPU 집중 프로세스는 CPU가 GPU에 작업을 전달한 후 결과를 기다리는 시간이 많기 때문에, CPU 관점에서는 I/O 버스트가 많은 프로세스와 유사하게 동작한다.<br>

즉, 짧게 CPU를 사용한 후 GPU 작업이 끝날 때까지 대기하는 형태이다. 단, GPU 연산은 일반적인 디스크나 네트워크 I/O와는 다른 가속기 연산이다.
</details>
