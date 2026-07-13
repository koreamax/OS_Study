## Chapter 10. 프로세스와 스레드
### 10-1 프로세스 개요
- 프로세스 확인
- 프로세스 제어 블록 (PCB)
- 문맥 교환
- 프로세스 메모리 구조

### 10-2 프로세스 상태와 계층 구조
- 프로세스 상태
- 프로세스 계층 구조
- 프로세스 생성 기법

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

1-1. 운영체제는 프로세스를 관리하기 위해 PCB(Process Control Block)를 사용하는데, 이 PCB들은 어떤 자료구조로 관리될까요?
<details>
  <summary>정답</summary>
    주로 연결 리스트(Linked List) 로 관리됩니다. 상태별(Ready, Waiting 등)로 큐를 만들고, 각 큐를 PCB를 노드로 하는 연결 리스트로 연결해서 삽입·삭제를 유연하게 처리합니다.
</details>

1-2. 프로세스의 메모리 구조에서 전역변수와 지역변수는 각각 어느 영역에 저장될까요?
<details>
  <summary>정답</summary>
    전역변수 / static 변수 → 데이터 영역<br>
    지역변수 → 스택
</details>

2-1.  프로세스의 PID가 1이라는 것은 무엇을 의미할까요?
<details>
  <summary>정답</summary>
    최초로 실행되는 init 프로세스(현대 리눅스에서는 보통 systemd)를 의미합니다. 커널이 부팅 후 가장 먼저 띄우는 유저 프로세스로, 모든 프로세스의 조상이 되며 고아 프로세스(부모가 죽은 프로세스)를 입양하는 역할도 합니다.
</details>

2-2. 프로세스 생성과 관련된 fork와 exec 시스템 콜을 각각 설명해주세요.
<details>
  <summary>정답</summary>
    fork: 현재 프로세스를 그대로 복제해서 자식 프로세스를 만듭니다. 부모와 거의 동일한 복사본이 생기고, 반환값으로 부모(자식 PID)와 자식(0)을 구분합니다.<br>
    exec: 현재 프로세스의 껍데기(PID, PCB)는 유지되지만, 그 안의 내용물이 완전히 새로 생성됩니다. 즉 코드 영역, 데이터 영역, 힙, 스택 같은 메모리 공간이 기존 프로그램의 것을 버리고 새 프로그램의 것으로 싹 갈아엎어져 새롭게 세팅됩니다.
</details>
