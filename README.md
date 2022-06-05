# 오픈소스 SW개론

### [과제 2] 조사내용 README파일로 정리하기
  by. 조선대학교 IT융합대학 컴퓨터공학과 __20205078 김연희__
<br/> 

--------------------------------------------------------------------------------------------------------
## 1. 리눅스 명령어에서 _top, ps, jobs, kill_ 명령어를 조사하기
+ 먼저 **top, ps, jobs, kill** 명령어의 역할은 아래와 같다.

|**명령어**|**설명**|
|:---:|---|
|__top__|현재 OS의 상태를 나타내주는 CLI 어플리케이션|
|__ps__|현재 실행중인 프로세스의 목록을 보는 명령어|
|__jobs__|작업의 상태를 표시하는 명령어|
|__kill__|프로세스에 특정한 시그널을 보내는 명령어|

--------------------------------------------------------------------------------------------------------
### 1) top 명령어
+ top 명령어는 'top 명령어는 현재 OS의 상태를 나타내주는 CLI 어플리케이션'으로 *메모리 사용량, CPU 사용량 등* 을 나타내준다.
+ top를 실행하는 동안에는 주기적인 업데이트로 실시간에 근접한 내용을 보여준다.
+ 위에는 전체의 요약이, 아래에는 각 프로세스마다의 구체적인 내용이 있다. <br/> - 상단에 위치한 **요약영역**은 전체 프로세스가 OS에 대해서 리소스를 어느정도 차지하고 있는지를 알려준다. <br/> - 요약 영역에 나타나는 대표적인 값은 **시간, 유저, 로드 에버리지(Load Average), 테스크(Tasks), CPU, 메모리(memory)**이다.

### 2) ps 명령어
+ ps 명령어는 '현재 실행중인 프로세스의 목록을 보는 명령어'로 옵션없이 사용하면 현재 셸이나 터미널에서 실행한 사용자 프로세스에 대한 정보를 출력한다.
+ 아래 표는 ps 명령어의 옵션 중 세 가지이다.

|**옵션**|**설명**|
|:---:|---|
|**-e**|실행하고 있는 모든 프로세스 출력|
|**-f**|각 프로세스에 대한 좀 더 상세한 정보를 출력|
|**-u**|해당 사용자가 실행 중인 프로세스를 출력|

### 3) jobs 명령어

### 4) kill 명령어
--------------------------------------------------------------------------------------------------------
## 2. vim 에디터에서 매크로 사용방법에 대하여 조사하기 (q , @) (' : '은 생략한다.)
+ vim 에디터에서는 '**q**'와 '**@**'를 이용하여 '*같은 명령을 반복* '하는 매크로 기능을 사용할 수 있다.
+ 순서는 다음과 같다.

  >- **명령 모드**에서 '**q**'를 누른 다음 '매크로의 이름'으로 사용할 __알파벳__`(a-z)` 또는 __숫자__`(0-9)`를 넣어준다. (ex. qa)
  >- '반복할 동작'을 입력한다.
  >- '**q**'를 눌러 매크로 모드를 종료한다.
  >- '**@**' 뒤에 '매크로의 이름'을 붙이면 매크로가 실행된다. (ex. @a)

+ 예시
  ```c
  q[MacroName]   //매크로 모드 시작
  [Movement]     //반복할 동작 입력
  q              //매크로 모드 종료
  @[MacroName]   //매크로 실행
  ```
<div align="right"> 
  ( 주의! 명령모드에서 진행해야한다.)
</div>
<br/> 

+ **만약 마지막으로 한 작업을 되돌리고 싶다면 (명령모드에서)  *u* 를 누르면 된다.** ~`매크로 입력 도중 u를 누른다면...`~
   
