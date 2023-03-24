## 생활코딩 WEB2-Domain Name System 정리      
#
컴퓨터마다 고유한 ip를 가짐  
  
이것을 이용해 다른 컴퓨터가 웹사이트에 들어갈 수 있음  
  
ip에 고유한 domain 을 설정해 ip를 가리고 이름으로 웹사이트를 들어갈 수 있음  
  
DNS server에 자신에 ip를 domain 설정하고   
인터넷에 domain을 적으면 DNS server를 통해 다른 컴퓨터가 자신에 컴퓨터에 ip에 연결할 수 있음  
  
통신사(ips)들에 도메인서버가 대표적이나   
다른 도메인 서버도 사용할 수 있음(public DNS)  
  
xxx.xxxx.com.  
맨 마지막 점 => root  
com(kr) => Top-level domain  
xxxx => Second-level  
xxx => sub  

각 부분 마다 서버가 존재하며 모두 각 부분을 전담하고 있음  
상위는 직속하위에 정보를 알고 있음(. => com => xxxx => xxx)   
  
모든 컴퓨터는 root name server에 ip를 알고 있음  

등록자(Registrant) -> 등록대행자(Registrar) -> 등록소(Registry)   
위 순서로 도메인의 네임서버 정보를 전달함

인터넷에 연결시 내가 사용하는 기기가 내가 사용할 DNS Server에 ip를 자동으로 세팅함  

윈도우 기준 cmd창에 nslookup을 적으면 dns에 정보를 알 수 있음  

캐쉬기능 = 자신이 사용했던 서버에 주소를 기억했다가 한번 더 사용시 기억해놨던 주소를 사용해 네트워크에 부화를 줄이는 방법