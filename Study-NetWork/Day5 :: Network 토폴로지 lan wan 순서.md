## Network 토폴로지 lan wan 순서

##### ip address 설정(Step 1)

Router> enable

//관리자모드 접근



Router # configure terminal

//전역 설정 접근



Router(config)# interface fastEthernet 0/0  --- > (여기서 n/n은 해당 라우터 번호)

//인터페이스 접근



Router(config-if)# IP address(아이피 주소<내가 정해도 된다>)(서브넷 마스크 주소)

//ip 할당 및 서브넷 마스크 할당



Router(config-if)# no shutdown

// 포트 활성화 



exit 

//나가기

exit

//나가기





#####  serial number 작성 (step 2)

interface serial 0/3/0



ip address 172.168.10.1 255.255.255.0  





exit

//나가기



exit

//나가기





##### PC 설정하기(Step 3)



각 pc의 ip 를 설정해준다.



맨 마지막에 한 자리는 달라야 한다. 

< Router의 ip 주소와 맨 끝자리>

예시 : 192.168.10.1 -> 192.168.10.3

---> 이런식으로



##### ping 보내기

PC의 CLI에서 아무 설정 없는 상태에서 ping + 상대방 ip를 입력한다.(내가 했을 때는 이제 반대편 라우터의 serial number를 입력한다)

----





이후에 정상적으로 !!!!! 가 입력되면 ping 보내기 성공

서버통신 성공!



#### Ping 전송 성공



![](/Users/mac/Desktop/School SUB👩‍🏫/Study-SUB/Study-NetWork/ping 성공.png)



----------------



#### 내가 사용한 IP 주소

###### subnetmask의 값은 255.255.255.0으로 통일



왼쪽 



<fast Ethernet>

192.168.10.1



<serial number>

172.168.10.1







PC 0 



192.168.10.3





가운데



<fast Ethernet>

192.168.11.1







<serial number>

172.168.10.2



Next ->172.168.21.1





PC 2

192.168.11.3



맨 오른쪽 



<fast Ethernet>

192.168.12.1



<serial number>

172.168.21.2



0/3/1





PC 2





------

1. 선 연결

2. 라우터에서 호스트네임 설정 
3.  라우터에서 fastethernet의 ip 주소 설정 
4. 라우터에서 시리얼 포트의 ip 주소 설정 
5. 라우터에서 ip route 
6.  pc에서 ip주소, 게이트웨이 설정 
7. pc의 cmd에서 반대편 pc로 ping 보내기







