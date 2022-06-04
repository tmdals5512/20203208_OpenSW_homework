#### 20203208_OpenSourceSW_homework

---
1) 리눅스 명령어

 top : CPU사용률이 높은 것 부터 보여주는 소프트웨어
 
 사용법 : top [옵션]
 
 | 옵션 | 설명 |
 |------|:-----|
 |-b|배치모드로 정보를 출력|
 |-d delay|지정한 시간 간격으로 정보를 업데이트 하여 출력|
 |-i idle|토글값이 off일때 idle프로세스나 좀비프로세스 출력x|
 |-n num|지정한 시간만큼 업데이트 정보를 출력|
 |-p pid|지정한 프로세스의 정보만 출력|
 |-q|시간 간격없이 계속 출력|
 |-s|몇개의 대화식 명령을 비활성화|
 |-S|누적된 정보를 출력|
 
 실행 후 단축키 명령어
 
 | 명령어 | 설명 |
 |:--:|:--:|
 |space|정보를 업데이트|
 |shift + p|cpu 사용률이 높은 순서대로 표시|
 |shift + m|메모리 사용률이 높은 순서대로 표시|
 |shift + t|프로세스가 돌아가고 있는 시간 순서대로 표시|
 |k|프로세스 종료|
 |a|메모리 사용량에 따라 정렬|
 |b|Batch 모드|
 |c|명령행, 프로그램 이름 토글|
 |h|도움말|
 |n or #|출력할 프로세스의 수를 지정|
 |s|출력할 정보의 업데이트 시간을 지정|
 |q|top을 종료|

 보는법
 
 |현재시간|부팅후 운영시간|사용자수|1,5,15분 평균부하율|||||
 |-|-|-|-|-|-|-|-|
 |전체실행 프로세스 수|현재실행 프로세스 수|휴식상탱 프로세스 수|종료된 프로세스 수|좀비프로세스 수||||
 |us사용자가 실행시킨 프로세스의 CPU사용률|sy시스템자체에서 사용하는 CPU사용률|ni noce정책에의해 사용되는 CPU사용률|id남은 CPU사용률|wa입출력대기 상태의 CPU사용률|hi IRQs에 사용된CPU|si softIRQ에 사용된 CPU|st steal값|
 |실제 메모리 사용량|프로세스에 의해 사용되는 메모리사용량|남은 메모리양|버퍼링된 메모리 양|||||
 |전체스왑 메모리양|프로세스에 의해 사용되는 스왑메모리양|남은 스왑메모리양|캐싱 매모리양|||||
 |PID 프로세스번호|USER 사용자|PR 우선순위|NI nice값|VIRT 가상메모리양|RES 물리메모리 사용량|SHR 공유메모리 총량||
 
 [출처](https://m.blog.naver.com/PostView.naver?isHttpsRedirect=true&blogId=tjrwjd3535&logNo=220873744452 "top")
  
 ps : 현재 실행중인 프로세스의 목록을 보여줌
 
 사용법 : ps [옵션]
 
 | 옵션 | 설명 |
 |------|:-----|
 |-e|모든 프로세스 출력|
 |-f|풀 포맷으로 출력|
 |-u [사용자 이름]|특정 사용자의 프로세스|
 |-p pid|특정 pid프로세스|
 |-l|긴 포맷|
 
 [출처](https://arer.tistory.com/150 "ps")
 
 jobs : 작업의 상태를 표시하는 명령어
 
 사용법 : jobs [옵션][job ID]
 
 | 옵션 | 설명 |
 |------|-----|
 |-l|프로세스 그룹 ID를 state 필드 앞에 출력|
 |-n|프로세스 그룹 중에 대표 프로세스 ID를 출력|
 |-p|각 프로세스 ID에 대해 한 행씩 출력|
 |command|지정한 명령어를 실행|
 
 jobs로 알 수 있는 세션의 상태 값
 | 상태 | 설명 |
 |------|-----|
 |Running|작업이 일시 중단되지 않았고 종료하지 않고 계속 진행 중임|
 |Done|작업이 완료되어 0을 반환하고 종료 했음을 의미|
 |Done(code)|작업이 정삭적으로 완료되었으며, 0이 아닌 코드를 반환 했음을 의미|
 |Stopped|작업이 일시 중단|
 |Stopped(SIGTSTP)|SIGTSTP 신호가 작업을 일시 중단|
 |Stopped(SIGSTOP)|SIGSTOP 신호가 작업을 일시 중단|
 |Stopped(SIGTTIN)|SIGTTIN 신호가 작업을 일시 중단|
 |Stopped(SIGTTOU)|SIGTTOU 신호가 작업을 일시 중단|
 
 [출처](https://shaeod.tistory.com/968 "jobs")
 
 kill : 프로세스에 특정한 신호를 보낼때 사용, 일반적으로 종료 되지 않는 프로세스를 종료시킬때 사용
 
 사용법 : kill [옵션] [PID]
 
 ![kill1](https://user-images.githubusercontent.com/80256817/172020867-2de6c201-1819-4b4a-9181-d42769c09b3c.png)
 ![kill2](https://user-images.githubusercontent.com/80256817/172020884-95fef38d-13c1-4619-afcd-f2e8a4372aef.png)
 
 [출처](https://m.blog.naver.com/koromoon/220804715310 "kill")

---
2) vim 에디터 매크로
