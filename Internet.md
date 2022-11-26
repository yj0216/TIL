# 인터넷 동작 원리
## 인터넷이란?

- TCP/IP 프로토콜을 기반으로 한 컴퓨터와 네트워크들이 연결된 광범위한 컴퓨터 통신망

## TCP/IP란?

- TCP/IP는 컴퓨터와 컴퓨터 간의 지역네트워크(LAN) 광역네트워크(WAN)에서 원할 한 통신을 가능하도록 하기위한 통신규약으로 정의

쉽게 말해 서로 다른 컴퓨터 2대가 연결된 것

예를 들어 우리가 가진 컴퓨터가 네이버에 화면을 띄워 달란 요청을 보내게 되면 네이버에서는 화면과 각종 자료들을 보내 우리 컴퓨터에 전달함 이 네이버를 서버라고 함

이렇게 서로 연결된 컴퓨터가 많은 것을 인터넷이라고 함

## 연결방식

### 라우터

간단하게 두개의 컴퓨터가 통신이 필요할 때 나의 컴퓨터와 다른 사람의 컴퓨터 물리적(케이블 선) 또는 무선(WiFi, Bluetooth)으로 연결이 되어야한다. 이러한 방식으로 여러 대의 컴퓨터를 연결을 할 수는 있다.

그러나 이런 식으로 연결될 시 가독성이 떨어지게 되고 관리도 어려워 비효율적이다

이 방식을 해결 하기 위해 라우터가 나왔는데 각 컴퓨터는 라우터라는 소형 컴퓨터에 연결되게 된다

컴퓨터와 컴퓨터 간의 연결이 아닌 컴퓨터가 하나의 10개의 플러그가 있는 라우터에 10대의 컴퓨터 각 하나씩 가지고 있는 케이블로만 연결이 된다.

그럼 라우터는 각 컴퓨터에 필요한 데이터만을 보낸다

많은 컴퓨터를 연결할 시에는 단일 라우터만으로는 문제가 생기지만 라우터도 결국은 소형 **컴퓨터**이기때문에 서로 연결하여 해결이 가능하다

### 모뎀

모든 네트워크를 하나의 통신망으로 연결하는 것이 인터넷이다. 그러나 아주 먼 곳에 있는 곳과는 케이블 연결이 불가능에 가깝다.

 이걸 해결하게 된 것이 바로 전화와 전력이다. 심지어 전화 기반 시설 같은 경우는 세계적으로 연결돼 있기 때문에 이미 네트워크는 구성이 되었다. 

그럼 네트워크를 구성하기 위해서는 네트워크를 전화 기반 시설에 연결하면 되는데 이 것을 해주는 것이 바로 모뎀이다.

모뎀은 우리 네트워크의 정보를 전화 시설에서 처리 할 수 있는 정보로 바꾼다

### ISP

이제 네트워크는 전화망에 연결이 되어 데이터를 주고 받을 수 있다. 

하지만 그 데이터를 주고 받기 위해서는 네트워크를 인터넷 서비스 제공업체 ISP에 연결한다.

ISP는 모두 함께 연결되는 몇몇 특수한 라우터를 관리하고 다른 ISP의 라우터에도 액세스를 할 수 있는 회사다.

예) LG U+, KT, SKT 등

따라서 우리의 네트워크의 메시지는 ISP 네트워크의 네트워크를 통해 대상 네트워크로 전달된다.

간단히 말해 그냥 중간에서 데이터를 전달하는 역할이다.