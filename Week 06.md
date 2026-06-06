### 05-2 명령어 병렬 처리 기법
- 명령어 파이프라인
- 슈퍼스칼라
- 비순차적 명령어 처리

### 05-3 CISC와 RISC
- 명령어 집합
- CISC
- RISC


**최민경**

1-1. RAM과 ROM의 차이를 설명해주세요.
<details>
  <summary>정답</summary>
  RAM은 휘발성 저장장치로, 자유롭게 읽기 쓰기가 가능하며 속도가 빠르다는 특징이 있습니다. ROM은 반대로 비휘발성 저장장치이며, 일반적으로 읽기 전용입니다. 속도는 RAM보다 느린 편입니다.
</details>

1-2. 
<details> RAM 중에서 대용량일 필요는 없고, 속도는 빨라야 할 때 사용할 수 있는 RAM은 무엇일까요?
  <summary>정답</summary>
  SRAM입니다. SRAM은 DRAM보다 속도는 빠르지만, 집적도가 낮아서 용량이 작은 특징이 있습니다.
</details>

1-3. 
<details> 속도도 빠르면서 용량도 커서 현대 컴퓨터에서 메인 메모리로 사용하는 RAM은 무엇일까요?
  <summary>정답</summary>
  DDR입니다. DDR은 대역폭을 넓혀 SDRAM 대비 속도를 두 배 빠르게 만들고, 용량도 큰 편이어서 현대 컴퓨터의 메인 메모리로 작동하고 있습니다.
</details>

2-1. CPU에서 물리주소 대신 논리주소를 사용하는 이유가 무엇일까요?
<details>
  <summary>정답</summary>
  메모리는 시시각각 저장된 정보 위치가 변하기 때문에 CPU는 메모리 어디에 데이터가 저장되어있는지 알 수 없기 때문입니다.
</details>

2-2. CPU에서 주소가 물리주소로 변환될 때 구조를 설명해주세요.
<details>
  <summary>정답</summary>
  CPU가 논리주소 0x10번지 데이터를 요청한 경우,
  CPU의 논리 주소가 논리 주소 버스를 타고 MMU 칩으로 들어갑니다. MMU 칩이 논리 주소를 물리 주소로 변환하고, 변환된 주소가 물리 주소 버스를 타고 RAM에 도달합니다.
  하지만, 현대 컴퓨터의 경우 대부분 프로세서에서 MMU는 CPU 내부 구성 요소입니다. 따라서, CPU의 MMU에서 물리 주소로 변환 후에 주소 버스를 통해 RAM에 신호를 보내는 형태입니다.
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
