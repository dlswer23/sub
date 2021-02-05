## Network 토폴로지 lan wan 순서



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





#####  라우터끼리 접속

interface serial 0/3/0



exit

//나가기



exit

//나가기



##### ping 보내기

아무 설정 없는 상태에서 ping + 상대방 ip를 입력한다.(내가 했을 때는 이제 반대편 라우터의 serial number를 입력한다)

----





이후에 정상적으로 !!!!! 가 입력되면 ping 보내기 성공

서버통신 성공!





