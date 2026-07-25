## Chapter 11. CPU 스케줄링
### 11-2 CPU 스케줄링 알고리즘
- 다양한 스케줄링 알고리즘

## Chapter 12. 프로세스 동기화
### 12-1 동기화란
- 동기화의 의미
- 생산자-소비자 문제
- 공유 자원과 임계 구역

---

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

1-1. 다단계 피드백 큐 스케줄링에서 프로세스는 어떻게 다른 큐로 이동하나요?
<details>
  <summary>정답</summary>
  프로세스 자체가 이동하는 것은 아닙니다.<br> 
  운영체제가 PCB의 우선순위 정보를 변경하고, 해당 PCB를 가리키는 항목을 다른 준비 큐로 옮깁니다.
</details>

1-2. 스케줄링의 전체적인 원리를 알려주세요.
<details>
  <summary>정답</summary>
  스케줄러(준비 큐 확인) → 준비 큐(PCB 참조) → PCB(프로세스의 상태와 실행 정보 저장) → 프로세스 실행<br>
  스케줄러가 준비 큐와 PCB 정보를 확인하여 다음에 CPU를 사용할 프로세스를 선택합니다.
</details>

2-1. Race Condition이란 무엇인가요?
<details>
  <summary>정답</summary>
  여러 실행 흐름이 같은 공유 자원에 접근할 때, 실행 순서에 따라 결과가 달라지는 문제입니다.<br>
예를 들어 두 프로세스가 같은 계좌 잔액을 동시에 읽고 수정하면, 한쪽 결과가 덮어써져 잘못된 잔액이 저장될 수 있습니다.
</details>

2-2. 싱글 프로세스나 싱글 스레드에서는 Race Condition이 발생하지 않나요?
<details>
  <summary>정답</summary>
  - 싱글 프로세스: 멀티 스레드가 있으면 발생할 수 있습니다.<br>
  - 싱글 스레드: 완전히 순차적으로 실행되면 일반적으로 발생하지 않습니다.<br> 단, 비동기 작업, 인터럽트 처리 코드, 외부 프로세스 등이 같은 자원에 접근하면 발생할 수 있습니다.
</details>
