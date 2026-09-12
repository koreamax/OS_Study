## Chapter 15. 파일 시스템
### 15-1 파일과 디렉터리
- 파일
- 디렉터리
- 경로

### 15-2 파일 시스템
- 파티셔닝과 포매팅
- 파일 할당 방식
- 파일 시스템 구조
- 저널링
- 마운트

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

1-1. FAT는 연결 할당의 어떤 단점을 어떻게 해결했나요?
<details>
  <summary>정답</summary>
  연결 할당은 다음 블록 포인터가 데이터 블록 안에 있어서 n번째 블록을 읽으려면 디스크를 n번 따라가야 하고, 포인터 하나가 깨지면 뒤가 다 끊깁니다. <br> FAT는 이 포인터들을 디스크 앞의 테이블 하나에 모아 두고 메모리에 올려서, 디스크 접근 없이 블록 위치를 찾게 했습니다.
</details>

1-2. 연결 할당은 왜 FAT처럼 할당 정보를 메모리에 두고 쓰지 않나요?
<details>
  <summary>정답</summary>
  포인터가 데이터 블록 안에 흩어져 있어서 모으려면 디스크 전체를 읽어야 하고, 그렇게 모은 테이블이 곧 FAT입니다. <br> 그래서 별도로 캐시하는 대신 처음부터 포인터를 테이블로 분리한 FAT 방식을 씁니다.
</details>

2-1. 시스템 크래시가 파일시스템에 어떤 문제를 일으키나요? 
<details>
  <summary>정답</summary>
  시스템 크래시는 정전, 커널 패닉, 강제 종료처럼 OS가 정상 종료 절차 없이 멈추는 상황입니다.<br>
  중간에 전원이 나가면 일부만 반영되어 메타데이터가 불일치합니다. 전통적으로는 부팅 때 fsck로 디스크 전체를 검사해야 해서 오래 걸립니다.
</details>

2-2. 저널링 파일시스템은 이걸 어떻게 해결하나요?
<details>
  <summary>정답</summary>
  실제 위치에 쓰기 전에 변경 내용을 저널이라는 로그에 먼저 기록하고 커밋합니다. <br>
  크래시 후에는 저널(로그)만 보고 커밋된 건 다시 반영, 안 된 건 버리면 되므로 전체 검사가 필요 없습니다. <br>
  디스크 전체를 검사할 필요 없이 로그만 되감으면 되므로 복구가 빠릅니다. ext4, XFS, NTFS가 대표적입니다.
</details>
