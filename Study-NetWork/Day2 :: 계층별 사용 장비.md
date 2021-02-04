### 계층 별 사용 장비

---------------------------------------------



1 ) 물리계층 : 물리적으로 데이터를 전송하는 역할을 수행

+ Repeater(리피터), Hub

  + Repeater : cable 전송으로 약화된 신호를 초기화, 증폭, 재전송의 기능을 수행한다
  + Hub : Repeate와 마찬가지로 전기적 신호를 증폭

  

2 ) 데이터 링크 계층 : 물리적 전송 오류를 해결 ( 오류 감지 / 재전송 기능)

+ Switch, Bridge

  + MAC address를 사용하는 계층

  + LLC : Data Link의 부 계층 중 하나로 물리적 매체 상에서 흐름 제어와 에러 제어 등을 관리

  + 1. Bridge(브리지)  : 브리지, 스위치도 허브와 마찬가지로 장비를 물리적으로 연결하고 Frame의 전송거리를 연장 

       단순히 전기적 신호만을 증촉시키는 것이 아니라 Frame을 다시 만든다

       

       1. Switch(스위치)  : 브리지와 스위치는 MAC address 와 해당 장비의 포트 번호가 기록된 MAC address table을 보고 목적지에게만 Frame을 전송

    

    #### !허브는 1차선 도로, 스위치는 다 차선 도로 !

    

3 ) 네트워크 계층 : 올바른 전송 경오를 선택(혼잡 제어 포함)

+ Router, L3 Switch	

  + Routher

    + 라우터는 특정 인터페이스를 통하여 수신한 packet의 목적지 IP주소를 보고 목적지와 연결된 인터페이스를 통하여 전송할 것을 결정한다. --> 이를 Routing이라고 한다
    + 라우터의 기본 기능은 경로설정 -> 경로에 따른 Packet 전송이다.(이외에도 네트워크 보안 등이 있다)

    

    #### Router의 역할

    + ##### 경로결정

      + packet이 목적지로 갈 수 있는 경로를 확인하고 어느 경로가 가장 최적경로인지 결정

    + ##### 스위칭

      + 결정된 경로대로 packet을 전송해주는 것

    + Router는 Routing table 을 보고 packet을 전송

    + Routing protocol에 따라  Routing table을 작성한다.

    

    ####   Router의 종류

    + 단독형 : 일체형으로 이미 모든 Interface가 구성(확장성 X)
    + 모듈형 : 사용자의 필요에 따라 Interface모듈의 직접 꽃아서 사용가능(확장성 O)

    ![Router종류](https://slidesplayer.org/slide/14059271/86/images/4/Router+-+Router%EC%9D%98+%EC%A2%85%EB%A5%98+1%29+%EB%8B%A8%EB%8F%85%ED%98%95+%3A+%EC%9D%BC%EC%B2%B4%ED%98%95%EC%9C%BC%EB%A1%9C+%EC%9D%B4%EB%AF%B8+%EB%AA%A8%EB%93%A0+Interface%EA%B0%80+%EA%B5%AC%EC%84%B1.+%28%ED%99%95%EC%9E%A5%EC%84%B1+X%29.jpg)

    

    

    

    #### Router Interface 종류

    1) LAN구간 Interface -> Ethernet

    2) WAN 구간 Interface -> Serial Interface

    3 ) 관리용 Interface -> Console Port, Auxiliary Port

    

    #### Router에 사용되는 Cable

    ![Cable](https://slidesplayer.org/slide/14059271/86/images/6/Router+WAN+LAN+LAN+-+Router%EC%97%90+%EC%82%AC%EC%9A%A9%EB%90%98%EB%8A%94+Cable.jpg)

    1) V.35 -> WAN 구간에 사용되는 케이블 중 하나

    2) UTP -> LAN 구간에 사용되는 케이블

    3) Console cable : 장비 관리용 케이블

    

    #### Router 특징

    + Router는 성능, Interface의 숫자, 지원하는 기능, 메이커에 따라 가격이 다르다

    + 모듈형에서 Interface는 따로 구입해야 한다

    + Router에서 사용되는 Software는 IOS라고 한다

      + 즉, Router의 운영체제이다(ex. PC의 Window)

      

    #### Router 접속 방법

    ##### 1) Console cable

    + Router의 Console 포트에 Console cable을 연결하고 나머지 한쪽을 컴퓨터의 Serial 포트에 연결
    + 열결 후 터미널 프로그램을 사용해서 접속
    + console cable이 가장 일반적이고 편리한 방법
      + Router 에 PC를 직접 연결해야 하고 consolecable이 필요하다는 불편함이 있다 -> telnet을 주로 사용
    + 가장 안정적인 접근이 장점

    ##### 2) Telnet

    + 대부분 Router를 관리할 때 가장 많이 사용하는 방법
    + Router의 IP주소를 알고 네트워크에 접속만 되어 있다면 장소와 상관없이 접속이 가능하다
    + Router를 처음 구성할 경우 IP주소 설정이 안되어있기 때문에 Telnet사용이 불가능하고 네트워크 연결이 끊어질 경우 접속이 불가능 하다는 단점이 있다.
    + Telnet을 Virtual Terminal이라고 한다
    + 터미널 프로그램을 사용해서 접속 MS-DOS에서도 'telnet x.x.x.x'로 접속이 가능

    

    ##### 3) 기타 접속 방식

    + AUX포트, NMS로 Router에 접속해서 설정할 수도 있다
+ TFTP 서버를 통해 다른 Router에서 만들어놓은 Router 설정파일을 Router로 다운로드 하는 방식이 있다.
    

  
#### Router 내부 구성
  
![Router](https://t1.daumcdn.net/cfile/tistory/2626F14C52977AB601)



#### 두가지의 특징!

+ RAM에 올라가 있는 설정 내용들은 'Running-config'(전원 차단 시 삭제)
+ NVRAM에 저장된 설정 내용들은 'Startup-config'(전원을 차단해도 저장)

-----------

+ ##### RAM : IOS가 올라와서 실행되고, Routing table과 구성파일이 올라와서 동작하는 장소

  + 그 외에도 ARP cache 나 fast swiching에 대한 cache를 가지고 있다
  + 휘발성 메모리이기 때문에 전원을 차단하면 모든 정보가 지워진다.

  

+ ##### NVRAM : 전원을 차단해도 저장된 내용이 지워지지 않는 비 휘발성 메모리

  + 설정파일을 저장한다. Routing table은 저장하지 않는다.



+ #####  Flask 메모리

  + 전원을 차단해도 저장된 내용이 지워지지 않는다
  + 주로 IOS 이미지 파일 저장용으로 사용된다
  + Router에 새로운 기능이 추가 되면 Router 자체를 교환하는 것이 아니라 IOS를 업그레이드 하면 된다.

  

+ ##### ROM

  + Router의 가장 기본적인 내용 저장
  + 전원이 들어올 경우 어떤 순서로 Router 자신의 상태를 점검하고 IOS를 어디서 RAM으로 올리는지 등의 내용이 저장돼있다.
  + 복구용 Mini IOS가 저장돼 있다.

  

---------



#### Router 부팅 과정

1) Power on self test(POST)

2) Load and run bootstrap code

3) Find the IOS sofrware

4) Load thr IOS sofrware

5) Find the configuration

6) Load the configuration

7) Run





-----------------

#### **Router 의 Mode**

1.ROMMON Mode

2.Setup Mode

3.User Mode

![](https://t1.daumcdn.net/cfile/tistory/2147C3405297806302)

+ 사용중인 Router에 Console 혹은 Teinet으로 접속하면 처음 보이는 화면 
+ 프롬프트가 기본적으로 'Router>' 로 표시

4.Privileged Mode

![](https://t1.daumcdn.net/cfile/tistory/21074D385297811211)

+ Router의 **운영자모드**

  -User Mode에서 enable(en만 입력해도됨)명령어를 사용하면 Privileged mode로 들어가게 된다

   (암호가 걸려있는 경우 암호까지 입력해야함)

5.Global configuration Mode (설정모드)









































