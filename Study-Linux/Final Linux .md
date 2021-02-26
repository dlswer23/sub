# Final Linux day



#### 사용자와 그룹

+ 리눅스는 다중 사용자 시스템임
+ 기본적으로 root라는 이름을 가진 수퍼유저(superuser)가 있으며, 모든 작업을 할 수 있는 권한이 있음
+ 모든 사용자를 하나 이상의 그룹에 소속되어 있음
+ 사용자는 /etc/passwd 파일에 정의 되어 있음 
+ 사용자의 비밀번호는 /etc/shadow 파일에 정의되어 있음 
+ 그룹은 /etc/group 에 저장되어 있다





#### 명령어 알아보기!

```
사용자 생성시 옵션
--uid : ID 지정
--gid : 그룹 지정
-- home : 홈 디렉터리 지정
--shell : 셸 지정
```



+ ##### adduser

  + 새로운 사용자를 추가
  + 예 ) # adduser newuser1

+ ##### passwd

  + 사용자의 속성을 변경
  + 예 ) passed newuser1

+ ##### usermood

  + 사용자의 속성을 변경
  + #usermood --group ubuntu newuser1

+ ##### userdel

  + 사용자를 삭제
  + #userdel newuser2

+ ##### change

  + 사용자의 암호를 주기적으로 변경하도록 설정 
  + 예 ) #change -m 2 newuser1

+ ##### groups

  + 현재 사용자가 속한 그룹을 보여줌 
  + 예 ) # groups

+ ##### groupadd

  + 새로운 그룹을 생성 
  + 예 ) groupadd newgroup1

+ ##### groupmod

  + 그룹의 속성을 변경 
  + 예 ) # gropmod --new-name mygroup1 new group1

+ ##### groupdel 

  + 그룹을 삭제 
  + 예 ) #group newgroup2

+ ##### gpasswd

  + 그룹의 비밀번호를 삭제





#### 각 행의 의미는 다음과 같다

​	사용자 이름 : 암호:사용자 ID:사용자가 소속도니 그룹 ID: 추가 정보: 홈 디렉터리 

