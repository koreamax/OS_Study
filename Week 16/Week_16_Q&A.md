## Chapter 14. 가상 메모리

### 14-2 페이징
- 페이징
- 페이지 테이블
- 주소 변환
- 페이지 테이블 엔트리

### 14-3 페이지 교체
- 요구 페이징
- 페이지 교체 알고리즘
- 스래싱과 프레임 할당

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

1-1. 페이지 테이블 베이스 레지스터(PTBR)에 대해서 설명해주세요.
<details>
  <summary>정답</summary>
  PTBR은 현재 실행 중인 프로세스의 페이지 테이블 시작 주소를 가리키는 레지스터입니다. 프로세스가 바뀌는 문맥 교환이 발생하면 PTBR 값도 해당 프로세스의 페이지 테이블 주소로 변경됩니다.
</details>

1-2. 페이징 시스템에서 주소 변환 과정을 설명해주세요.
<details>
  <summary>정답</summary>
  논리 주소는 페이지 번호와 변위(Offset)로 구성됩니다. 페이지 번호로 페이지 테이블을 조회해 프레임 번호를 찾고, 그 프레임 번호에 기존 변위를 결합해 물리 주소를 만듭니다. <br>
  즉, 페이지 번호는 프레임 번호로 바뀌고 변위는 그대로 유지됩니다.
</details>

2-1. 스래싱(Thrashing)이 무엇인지 설명해주세요.
<details>
  <summary>정답</summary>
  스래싱은 페이지 폴트가 너무 자주 발생해 실제 작업보다 페이지 교체에 더 많은 시간을 사용하는 상태입니다. <br>
  이로 인해 디스크 접근이 증가하고 CPU 이용률과 시스템 성능이 떨어집니다.
</details>

2-2. 정적 할당과 동적 할당의 차이에 대해서 설명해주세요.
<details>
  <summary>정답</summary>
  정적 할당은 프로세스에 줄 프레임 수를 미리 정해두는 방식이고, 동적 할당은 실행 중 상황에 따라 프레임 수를 늘리거나 줄이는 방식입니다. <br>
  즉, 핵심 차이는 프레임 수가 고정인지, 실행 중 조절 가능한지입니다.
</details>
