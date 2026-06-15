## Chapter 06. 메모리와 캐시 메모리
### 06-1 RAM의 특징과 종류
- RAM의 특징
- RAM의 용량과 성능
- RAM의 종류

### 06-2 메모리의 주소 공간
- 물리 주소와 논리 주소
- 메모리 보호 기법

### 06-3 캐시 메모리
- 저장 장치 계층 구조
- 캐시 메모리
- 참조 지역성 원리

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

1-1. RAM 용량이 클 때의 장점을 CPU와 보조기억장치 관점에서 설명하세요.
<details>
  <summary>정답</summary>
  CPU 관점에서는 더 많은 데이터와 프로세스를 메모리에 상주시킬 수 있어, CPU가 보조기억장치까지 내려가지 않고 빠르게 데이터를 가져올 수 있습니다.<br>
  보조기억장치 관점에서는 디스크 I/O가 줄어들어 프로세스가 디스크 응답을 기다리며 블로킹되는 상황이 줄고, 보조기억장치가 전체 시스템의 병목이 되는 정도가 완화됩니다.
</details>

1-2. RAM 용량이 클 때 그에 따른 트레이드오프는?
<details>
  <summary>정답</summary>
  가격이 비싸지고, 전력 소모가 증가하며, 실제로 사용하지 않으면 그만큼 낭비가 크고, <br>
  관리해야 할 메모리 영역이 늘어나 메모리 관리 부담이 커집니다.
</details>

2-1. Redis는 일반적인 캐시처럼 SRAM이 아닌 DRAM 위에서 동작합니다. 그 이유는?
<details>
  <summary>정답</summary>
  SRAM은 빠르지만 용량이 작고 가격이 매우 비싸기 때문에, Redis가 다루는 데이터 규모를 올리기에는 부적합합니다.<br>
  또한 Redis가 비교 대상으로 삼는 것은 L1/L2/L3 같은 CPU 캐시가 아니라 DB나 SSD입니다. 즉 Redis는 CPU 캐시보다는 느리지만 DB/SSD보다는 훨씬 빠른 계층이라 캐시라고 부를 수 있습니다.
</details>

2-2. Redis에서 hit ratio(캐시 적중률)가 높을 때 생기는 트레이드오프는?
<details>
  <summary>정답</summary>
  hit ratio를 높이기 위해 TTL을 길게 잡으면 오래된 데이터가 캐시에 더 오래 머무릅니다.<br>
  이 경우 원본 데이터가 수정·변경되었음에도 캐시에서는 갱신 전의 오래된 데이터를 반환하는 상황이 발생할 수 있습니다. <br>
  즉 적중률(성능)과 데이터 최신성(정합성) 사이에 트레이드오프가 생깁니다.
</details>
