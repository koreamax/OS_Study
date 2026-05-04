## Chapter 04. CPU와 작동 원리
### 04-1 ALU와 제어장치
- ALU
- 제어장치

### 04-2 레지스터
- 반드시 알아야 할 레지스터
- 스택 주소 지정 방식
- 변위 주소 지정 방식
- CPU 내 레지스터 및 주소 지정 방식

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

1-1. 변위 주소 지정 방식에서 명령어 필드는 무엇으로 구성되나요?
<details>
  <summary>정답</summary>
  연산코드(opcode) + 레지스터 필드 + 오퍼랜드
</details>

1-2. 시스템 버스에서 사용되는 버스의 종류 3가지와 각각의 역할을 설명하시오.
<details>
  <summary>정답</summary>
  데이터 버스: 실제 데이터를 전달하는 통로<br>
  주소 버스: CPU가 접근할 메모리/장치의 주소 전달<br>
  제어 버스: 읽기/쓰기, 인터럽트 등 제어 신호 전달
</details>

2-1. 주요 플래그 레지스터 4가지와, 각 플래그 값이 1일 때의 의미를 설명하시오.
<details>
  <summary>정답</summary>
  부호 플래그: 1이면 결과가 음수<br>
  캐리 플래그: 1이면 자리올림/빌림 발생<br>
  제로 플래그: 1이면 결과가 0<br>
  오버플로우 플래그: 1이면 오버플로우 발생
</details>

2-2. 프로그램 카운터(PC)가 단순히 +1 증가하지 않는 경우를 설명하시오.
<details>
  <summary>정답</summary>
  분기 명령어(jump, branch, call, return) 실행 시 → 특정 주소로 이동<br>
  인터럽트 발생 시 → 인터럽트 처리 루틴 주소로 이동
</details>

