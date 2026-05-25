### 05-2 명령어 병렬 처리 기법
- 명령어 파이프라인
- 슈퍼스칼라
- 비순차적 명령어 처리

### 05-3 CISC와 RISC
- 명령어 집합
- CISC
- RISC


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

1-1. x86은 외부적으로 CISC지만 내부적으로 RISC처럼 동작한다. 그렇다면, Intel x86은 정말 CISC인가?
<details>
  <summary>정답</summary>
  ISA는 소프트웨어와 하드웨어 사이의 약속일 뿐이며, CPU 내부 구현은 규정하지 않는다. <br>
  x86은 겉으로 CISC 명령어를 제공하지만 내부에서는 마이크로 명령어로 쪼개 RISC처럼 실행한다.
</details>

1-2. 왜 모바일에서는 RISC가 유리한가?
<details>
  <summary>정답</summary>
  RISC의 고정 길이 명령어는 명령어 디코딩 복잡도를 낮추고, 이는 파이프라이닝 효율을 높여 낮은 클럭으로도 같은 성능을 낸다.<br>
  결과적으로 전력 소비가 줄어 배터리와 발열에 민감한 모바일 환경에 유리하다.
</details>

2-1. 다음 상황은 파이프라인 위험 3종(데이터/제어/구조) 중 무엇인가?<br> 
(1) JUMP 100 명령어 때문에 미리 가져온 다음 명령어들이 쓸모없어졌다.<br> 
(2) 명령어 A의 결과를 명령어 B가 사용해야 해서 동시에 실행할 수 없다.<br> 
(3) 두 명령어가 동시에 같은 ALU를 쓰려고 한다.
<details>
  <summary>정답</summary>
  (1) 제어 위험 → 분기로 인한 PC 변경<br> 
  (2) 데이터 위험 → 명령어 간 의존성<br> 
  (3) 구조 위험 → 같은 부품 경합
</details>

2-2. 왜 현대 CPU는 파이프라이닝을 꼭 사용할까?
<details>
  <summary>정답</summary>
  파이프라이닝이 없으면 한 명령어가 끝날 때까지 CPU 부품들이 놀게 된다. <br>
  단계가 겹치지 않는 명령어들을 동시에 처리하면 부품을 쉬지 않게 만들 수 있어, 클럭을 높이지 않고도 처리량이 크게 늘기 때문이다.
</details>
