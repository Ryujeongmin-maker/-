# **1.1 인터넷이란 무엇인가**
위의 질문에 답하기 위해서는 2가지 방법이 있다
1. 인터넷의 구성요소(너트 , 볼트)를 기술하는 것으로 기본적인 하드웨어와 소프트웨어 구성요소를 기술하는 것,
2. 분산 애플리케이션에 서비스를 제공하는 네트워킹 인프라스트럭처 관점에서의 인터넷을 기술하는 것.

⁙네트워킹 인프라스트럭쳐(Networking Infrastructure) : 컴퓨터나 장치들이 서로 연결되어 통신할 수 있도록 해주는 물리적·논리적 장치들의 전체 구조 <br><br><br>  



  
### 1.1.1 구성요소로 본 인터넷
#### **인터넷(Internet)** 
•전 세계적으로 수십억 개의 컴퓨팅 장치를 연결하는 컴퓨터 네트워크<br><br><br>


#### **호스트(host)**  , **종단 시스템(end system)** 
• 네트워크에 연결되어 통신할 수 있는 모든 장치<br>
• 종단 시스템은 통신 링크와 패킷 스위치의 네트워크로 연결된다.<br><br><br>  



#### 패킷(packet)
• 한 종단 시스템이 다른 종단 시스템으로 보낼 데이터를 갖고 있을 때, 송신 종단 시스템은 그 데이터를 세그먼트(segment)로 나눈다<br>
• 그 후 각 세그먼트에 헤더(header)를 붙이고, 이렇게 해서 만들어진 정보패키지를 패킷이라고 함.<br>
• 패킷은 목적지에서 원래의 데이터로 다시 조립됨.<br><br><br>



#### 패킷 교환기(스위치)
• 도착하는 패킷을 받아서 출력 통신 링크의 하나로 그 패킷을 전달한다<br>
• 대표적인 두 종표<br>
(1) **라우터(router)** : 네트워크 코어에서 사용<br>
(2) **링크 계층 스위치(link-layer switch)** : 보통 접속 네트워크에서 사용<br><br><br>



#### 경로(route or path)
• 패킷이 송신 종단 시스템에서 수신 종단 시스템에 도달하는 동안 거쳐온 일련의 통신링크와 패킷 스위치

//예시.
수천 킬로미터 떨어진 창고(수신 종단 시스템)로 화물(데이터)을 옮겨야 하는 공장(송신 종단 시스템), 공장에서 화물은 세그먼트화되고 트럭 선단에 적재된다. 각 트럭은 고속도로, 도로 , 등등(네트워크)를 통해 목적지 창고로 운행한다.<br><br><br>



#### ISP(Internet Service Provider)
• 각 ISP는 패킷 스위치와 통신 링크로 이루어져 있다.<br>
• 웹사이트와 비디오 서버를 인터넷에 직접 연결하도록 CP(content provider)에게 인터넷 접속을 제공한다.<br>
• 다양한 네트워크 접속 제공( 가정용, 고속 LAN , 이동 무선 접속 ... )<br><br><br>



#### 프로토콜(protocol)
• 인터넷에서 정보의 송.수신을 제어함<br>
• 가장 대표적인 두 가지(TCP/IP)<br>
(1)**TCP(Transmission Control Protocol)**<br>
(2)**IP(Internet Protocol)** <br><br><br>



### 1.1.2 서비스 측면에서 본 인터넷
•1.1.1.에서 인터넷을 구성하는 여러 구성요소를 알아봤지만, 전혀 다른 관점에서 인터넷을 기술할 수 있음<br><br><br>



#### 애플리케이션에 서비스를 제공하는 인프라스트럭처
• 전자메일, 웹 서핑, 인터넷 메세징, 지도, 음악, 스트리밍 ...<br>
• 분산 애플리케이션(distributed application) 이라고도 부름.<br>
• **인터넷 애플리케이션은 종단 시스템에서 수행된다**(패킷 교환기에서 수행 X)<br>
⁙ 패킷교환기는 종단 시스템 간의 데이터 교환을 쉽게 해주지만 애플리케이션에는 관심을 갖지 않는다.<br><br><br>



#### 소켓 인터페이스(socket interface)
• Q. 한 종단 시스템에서 수행되는 애플리케이션이 다른 종단 시스템에서 수행되고 있는 프로그램으로 데이터를 보내도록 인터넷에 어떻게 지시할 것인가.<br>
  A. 종단 시스템들은 소켓 인터페이스를 제공하며, 이는 한 종단 시스템에서 수행되는 프로그램이 다른 종단 시스템에서 수행되는 특정 목적지 프로그램으로 데이터를 제공하는지를 명시함.<br>
• 인터넷 소켓 인터페이스는 송신 프로그램이 따라야 하는 규칙의 집합이며, 인터넷은 이 규칙에 따라 데이터를 목적지 프로그램으로 전달함.<br><br><br>



### 1.1.3 프로토콜이란 무엇인가?
• ex) 사람이 다른 프로토콜을 수행한다면 그 프로토콜은 상호작용할 수 없으며 원하는 작업을 수행할 수 없다,(그림 1.2 참고)<br>
 --> 어떤 일을 수행하려면 둘 이상의 통신 개체가 함께 인식하는 프로토콜이 필요함.<br><br><br>


 #### 네트워트 프로토콜
 • 통신하는 둘 이상의 원격 개체가 포함된 인터넷에서의 모든 활동을 프로토콜이 제어한다.<br>
 • 종단 시스템의 혼잡 제어(congestion-control) 프로토콜 : 송수신자 간에 전송되는 패킷 전송률을 조절한다.<br>
 • 라우터에서의 프로토콜 : 출발지에서 목적지까지 패킷 경로로 설정한다.<br>

 ⁙프로토콜은 둥 이상의 통신 개체 간에 교환되는 메시지 포맷과 순서뿐만 아니라, 메세지의 송수신과 다른 이벤트에 따른 행동들을 정의한다.
