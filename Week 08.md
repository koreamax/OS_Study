## Chapter 07. 보조기억장치
### 07-1 다양한 보조기억장치
- 하드 디스크
- 플래시 메모리

### 07-2 RAID의 정의와 종류
- RAID의 정의
- RAID의 종류

**최민경**

1-1. 
<details>
  <summary>정답</summary>
  
</details>

1-2. 
<details> 
  <summary>정답</summary>
  
</details>

1-3. 
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

1-1. 하드디스크(HDD)의 플래터, 헤드, 트랙, 섹터에 대해 설명하세요.
<details>
  <summary>정답</summary>
  플래터(Platter): 데이터가 실제로 저장되는 둥근 원판. 자성 물질로 코팅되어 있고 보통 여러 장이 축에 겹쳐 회전합니다.<br>
  헤드(Head): 플래터 표면 위를 움직이며 데이터를 읽고 쓰는 부품. 디스크 암(arm)에 붙어 함께 이동합니다.<br>
  트랙(Track): 플래터 위에 동심원 형태로 그려진 데이터 저장 경로. 같은 반지름의 원형 띠 하나가 하나의 트랙입니다.<br>
  섹터(Sector): 트랙을 부채꼴로 잘게 나눈 단위로, 디스크에서 데이터를 읽고 쓰는 최소 단위입니다.
</details>

1-2. 디스크 탐색 시간과 디스크에서 1MB를 순차적으로 읽는 시간은 각각 몇 나노초인가?
<details>
  <summary>정답</summary>
  디스크 탐색 시간: 약 10밀리초 = 10,000,000ns<br>
  1MB 순차 읽기: 약 30밀리초 = 30,000,000ns<br>
  CPU 연산(ns 단위)이나 RAM 접근(수십~수백 ns)에 비하면 수만~수백만 배 느리며, 이것이 디스크가 시스템 병목이 되는 근본 이유
</details>

2-1. 플래시 메모리는 NAND와 NOR 두 종류뿐인데, 만약 이 둘로 못 만드는 경우가 있다면 어떻게 되나요?
<details>
  <summary>정답</summary>
  NAND와 NOR로 못 만드는 경우는 없습니다. <br>
  플래시 메모리의 셀을 연결하는 방식은 결국 NAND 게이트 구조냐 NOR 게이트 구조냐로 귀결되며, 이 두 가지 구성이 "빠른 랜덤 접근(NOR)"과 "고집적·대용량(NAND)"이라는 양 극단의 요구를 각각 커버합니다. <br>
  즉 모든 플래시 메모리는 이 둘 중 하나의 구조로 구현 가능하기 때문에 두 종류만 존재하는 것입니다.
</details>

2-2.  플래시 메모리에서 읽기/쓰기는 페이지 단위인데 삭제는 블록 단위로 일어납니다. 그럼 페이지 하나만 삭제하고 싶으면 어떻게 하나요?
<details>
  <summary>정답</summary>
  페이지 하나만 골라 삭제하는 것은 불가능합니다. <br>
  삭제 대상 블록에서 valid 페이지들만 다른 빈 블록으로 복사하고, <br>
  원래 블록 전체를 삭제하여 invalid 페이지가 차지하던 공간까지 한꺼번에 회수합니다. <br>
  이 과정을 가비지 컬렉션(Garbage Collection) 이라고 합니다.
</details>
