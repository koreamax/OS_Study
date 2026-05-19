## Chapter 04. CPU와 작동 원리
### 04-3 명령어 사이클과 인터럽트
- 명령어 사이클
- 인터럽트
- 예외의 종류

## Chapter 05. CPU 성능 향상 기법
### 05-1 빠른 CPU를 위한 설계 기법
- 클럭
- 코어와 멀티코어
- 스레드와 멀티스레드

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

1-1. 4.9GHz는 클럭이 몇 번 반복되는 속도일까요?
<details>
  <summary>정답</summary>
  1초에 약 4.9 × 10⁹ 번, 즉 49억 번의 클럭이 발생합니다. <br>
  GHz는 초당 사이클 수(Hz)의 10억 배 단위이며, CPU의 동작 주파수를 의미합니다.
</details>

1-2. 오버클럭킹(Overclocking)이란 무엇인가?
<details>
  <summary>정답</summary>
  클럭 속도는 항상 일정하게 유지되는 것이 아니라, 부하 상황에 따라 가변적으로 조정됩니다. <br>
  더 높은 성능이 필요할 때 정격 클럭보다 빠르게 동작하도록 의도적으로 끌어올리는 동작을 오버클럭킹이라고 합니다.
</details>

2-1. 8코어 16스레드는 어떤 의미인가?
<details>
  <summary>정답</summary>
  8개의 물리 코어(CPU)가 있고, 각 코어가 2개의 명령 흐름을 동시에 처리합니다. <br>
  결과적으로 총 16개의 소프트웨어 스레드가 병렬로 동작합니다.
</details>

2-2. 1코어 1스레드 환경에서도 동시 처리가 가능해 보이는 이유는?
<details>
  <summary>정답</summary>
  실제로는 한 번에 하나의 명령어만 처리되지만, 처리 속도가 매우 짧기 때문에 <br>
  사용자 입장에서는 여러 작업이 동시에 실행되는 것처럼 보이기 때문이다.
</details>
