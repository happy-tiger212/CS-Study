## ARP
<img src="https://user-images.githubusercontent.com/91110192/197341599-58e9037a-b8ac-4909-a616-31e8ac719307.jpeg" width="70%">
ARP(Address Resolution Protocol): 논리 주소인 IP 주소로부터 MAC 주소를 구하는 프로토콜</br>
홉바이홉 통신을 하는 3계층에선 IP주소를 사용하지만, 2계층에선 MAC 주소를 사용한다. 그러므로 3계층 패킷이 캡슐화되기 전 ARP를 거치게 된다.

### ARP 동작
<img src="https://user-images.githubusercontent.com/91110192/197341602-6dbce96a-dc05-42dc-b90e-51fcc6e07b5d.jpeg" width="70%">
A가 ARP Request 브로드캐스트를 보내소 IP주소인 141.23.56.23에 해당하는 MAC 주소를 찾는다.</br>
그러고 나서 해당 주소에 맞는 장치 B가 ARP reply 유니 캐스트를 통해 MAC주소를 반환하는 과정을 거쳐 IP주소에 맞는 MAC 주소를 찾게 된다.</br>
</br>

_브로드캐스트: 송신 호스트가 전송한 데이터가 네트워크에 연결된 모든 호스트에 전송되는 방식</br>
유니캐스트: 고유 주소로 식별된 하나의 네트워크 목적지에 1:1로 데이터를 전송하는 방식_

## 홉바이홉 통신
IP 주소를 통해 통신하는 과정을 홉바이홉(hop by hop) 통신이라고 한다.  
여기서 홉(hop)이란 영어 뜻 자체로는 건너뛰는 모습을 의미한다. 이는 통신망에서 각 패킷이 여러 개의 라우터를 건너가는 모습을 비유적으로 표현한 것으로, 가각의 라우터에 있는 라우팅 테이블의 IP를 기반으로 패킷을 전달해나간다.


## IP 주소 체계
### IPv6
IPv6는 64비트를 16비트 단위로 점을 찍어 표기하는 방식(e.g.2001:db8::ff00:42:8329)
### DHCP
DHCP(Dynamic Host Configuration Protocol): IP 주소 및 기타 통신 매개변수를 자동으로 할당하기 위한 네트워크 관리 프로토콜.  
이 기술을 통해 네트워크 장치의 IP 주소를 수동으로 설정할 필요 없이 인터넷에 접속할 때마다 자동으로 IP 주소를 할당할 수 있다.
### NAT
NAT(Network Address Translation): 패킷이 라우팅 장치를 통해 전송되는 동안 패킷의 IP 주소 정보를 수정하여 IP 주소를 다른 주소로 매핑하는 방법
<img src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/40eee5b2-ba3b-4565-b9c7-8349dcd1701e/20221022_230032398.jpg?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20221022%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20221022T140133Z&X-Amz-Expires=86400&X-Amz-Signature=3ae62ca7f0f06d7cb2b30daaa34eff18cb9b16298c68294a542940e3eea4301e&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%2220221022_230032398.jpg%22&x-id=GetObject" width="70%">  
홍철 팀장, 가영 대리는 192.168.0.xxx를 기반으로 각각의 다른 IP를 가지고 있는데, 이는 **사설 IP**라고 한다.  
그리고 NAT 장치를 통해 하나의 **공인 IP**인 121.165.151.200으로 외부 인터넷에 요청할 수 있다.  
이를 통해 어비스 회사에 있는 홍철 팀장과 가영 대리는 하나의 IP인 121.165.151.200을 기반으로 각각의 다른 IP를 가지는 것 처럼 인터넷을 사용할 수 있다.  
이처럼 NAT 장치를 통해 사설 IP를 공인 IP로 변환하거나 공인 IP를 사설 IP러 변환하는 데 쓰인다.
