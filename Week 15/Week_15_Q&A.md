## Chapter 13. 교착 상태
### 13-2 교착 상태 해결 방법
- 예방
- 회피
- 검출 및 회복

## Chapter 14. 가상 메모리
### 14-1 연속 메모리 할당
- 스와핑
- 메모리 할당
- 외부 단편화

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

1-1. 오프로딩과 스와핑의 차이점은 무엇인가요?
<details>
  <summary>정답</summary>
  - 오프로딩: CPU가 처리하던 연산 작업을 GPU나 NPU, DSP 같은 별도의 처리 장치로 넘기는 것<br>
  - 스와핑: 메모리가 부족할 때 프로세스 이미지 전체를 메모리에서 디스크의 스왑 영역으로 내보냈다가 필요할 때 다시 불러오는 것<br>
  즉 오프로딩은 작업을 어디서 처리할지에 대한 분배 전략이고, 스와핑은 메모리를 어떻게 아껴 쓸지에 대한 메모리 관리 기법
</details>

1-2. 오프로딩이 발생할 때 프로세스가 이동하는 것도 스와핑인가?
<details>
  <summary>정답</summary>
  아닙니다. 오프로딩에서 실제로 옮겨지는 것은 프로세스 자체가 아니라 실행할 코드와 데이터일 뿐입니다.<br>
  프로세스 제어 블록은 여전히 원래 CPU 쪽에 남아 관리되고, 프로세스는 계속 실행 상태를 유지합니다.<br>
  반면 스와핑은 프로세스 전체가 메모리에서 통째로 내려가 대기 상태로 전환되며, 이후 다시 적재될 때까지 실행될 수 없습다.
</details>

2-1. 데드락 회피 과정 중에서 안전 상태에서 불안전 상태로 바뀌는 경우는 언제인가요?
<details>
  <summary>정답</summary>
  자원 요청이 들어오면 그것을 가상으로 할당해본 뒤 안전 순서가 존재하는지 검사하고, <br>존재할 때만 실제로 승인하기 때문에 이 전이는 원칙적으로 발생하지 않습니다.<br>
</details>

2-2. 데드락 회피 과정 중 불안전 상태에서 교착상태로 바뀌는 경우는 언제인가요?
<details>
  <summary>정답</summary>
  남은 가용 자원으로는 어떤 프로세스도 자신의 잔여 요구량을 채울 수 없고, 모든 프로세스가 <br>이미 확보한 자원을 점유한 채 요청을 걸어둔 상태로 대기하며, 그 대기 관계가 서로 맞물려 순환을 이루는 순간
</details>
