## IP addressing

+ ### IP address

##### -> IP는 논리적인 주소

​	TCP/IP를 사용하는 네트워크 상에 연결된 장비들에게는 고유의 IP주소가 부여된다.

​	(주소가 같은 다른 장비가 존재한다면 IP 주소가 서로 충돌)



##### -> IP address는 네트워크 부분과 호스트 부분으로 구성

(IP address = Network ID + Host ID)

ex ) 교실 이름과 학생 번호



+ IP 주소는 Network 부분과 Host부분으로 구성

+ 하나의 네트워크란 하나의 Broadcast Domain
+ 하나의 네트워크한 L3장비를 거치지 않고 통신이 가능한 영역
+ 다른 네트워크를 통신하기 위해서는 Router를 거쳐야 한다
  + 동일 네트워크에서는 Network 부분은 모두 같고 Host부분이 모두 달라야 한다
+ 이렇게 IP주소를 Network 부분과 Host부분으로 구분해주는 역할을 하는 것이 subnet mask이다.
+ 

-------------------------

+ ### Subnet mask

  ![IP adress](https://image2.slideserve.com/3649936/slide1-n.jpg)

  + Subnet mask의 값 : 255.255.255.0 / Network ID : 121.160.70.0

    + Host field를 모두 '0'으로 채우면 Network ID

    + Host field를 모두 '1'로 채우면 Broadcast 주소

    + Network ID와 Broadcast 주소는 IP주소로 사용할 수 없다.

      + 사용 가능한 IP주소 : 210.5.1.1 ~ 210.5.1.254
      + (총 호스트의 숫자 -2) = 2^n - 2 = 사용가능한 IP주소의 숫자

      

  + **IP주소를 Network 부분과 Host부분으로 규정**

    + IP = Network ID(고정된  bit) + Host IP (고정되지 않는 bit)

  + 총 네트웤 범위에서 NEtwork field에 '1' 을 할당하고 Host field에 '0'을 할당한 값이 Subnet mask.

  + IP주소와 Subnet mask를 AND 연산 하면 NetWork ID 값을 구할 수 있다.



#### IP주소에 따른 subnet mask 사용가능 여부

**2진수로 표현했을 떄 1이 연속적으로 나와야 한다.  **

ex )

| 255.255.255.0   | Subnet mask 사용 가능   |
| --------------- | ----------------------- |
| 255.255.255.10  | Subnet mask 사용 불가능 |
| 255.255.255.128 | Subnet mask 사용 가능   |

-> Prefix란 Subent mask의 '1'이 들어간 bit의 숫자

-----------------------

+ #### IP adress Class	

  IP 주소 범위에 따라 Subnet mask를 default값으로 정한 것

  

  ![image](https://i.pinimg.com/564x/fe/da/fe/fedafe4b628664f0d5084260d9c268f5.jpg)



##### 1) Class A(1~127)

 - 0과 127은 제외되고 1~126까지 사용
   	- 0.0.0.0 = All zero
   	- 12 7.0.0.0ㅇ은 Localhost

##### 2) Class B(128~191)

+ 128~191까지이다



##### 3) Class C(192~223)

+ 192~223까지이다.

  + Network 숫자 : 2,097,152개, 네트워크 당 HOST 숫자 : 254개

  

##### 4) Class D(224~239)

+ 224~239까지 이다.
+ multicast용으로 사용한다



##### 5) Class E(240~255)

+ 240~255까지이다
+ 실험용으로 예약된 주소이다
+ 실제로 사용하지 않음 (거의)



#### Quiz ?

##### ex ) 한 사무실에서 200대의 PC를 사용할 때 어느 Class의 IP를 배정하는 것이 좋은가?

-> Class C가 적당하다. Host의 숫자와 비례하게 생각하면 된다.



-------------

### Subneting

**기존의 호스트 bit로 할당된 bit 중 일부를 Subnet bit로 지정**

(즉, Host field의 bit를 빌려서 Network를 나눈다)

