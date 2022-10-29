## 운영 체제 (Operating system)
    사용자가 쉽게 컴퓨터를 사용할 수 있도록 해주는 인터페이스(interface)

    한정된 메모리와 시스템 자원을 효율적으로 분배하게 해주는 일꾼



### OS 구조

<img src="https://velog.velcdn.com/images/hagyoung99/post/1ec717d0-7ff2-4d0f-8792-1564f326edf2/image.png" width="40%"> 이미지 출처 - 면접을 위한 cs 지식노트 

위 구조로 되어있으며 GUI 부터 드라이버까지 운영체제(OS)를 지칭한다. 참고로 GUI가 없고 CUI만 있는 리눅스 서버도 있다.(CUI Charctor user interface)


#### 시스템 콜 (≒ 시스템 호출)
    운영 체제가 커널에 접근하기 위한 인터페이스이며 유저 프로그램이 운영체제의 서비스를 받기 위해 커널 함수를 호출할 때 사용. (추상화 계층)

    유저 프로그램이 I/O 요청을 하면 올바른 요청인지 확인한 후 유저 모드가 시스템 콜을 통해 커널 모드로 변환되어 실행된다.

    시스템 콜이 작동될 때 **modebit**을 참고하여 **유저 모드**와 **커널 모드**를 구분한다.

* 유저 모드 : 유저가 접근할 수 있는 영역을 제한적으로 두며 컴퓨터 자원에 함부로 침범하지 못하는 모드
* 커널 모드 : 모든 컴퓨터 자원에 접근 가능한 모드
* modebit : 1 또는 0의 값을 가지는 플래그 변수. 유저 모드와 커널 모드가 각 영역에서 올바르게 작동하기 위한 역활을 한다.

<img src="https://post-phinf.pstatic.net/MjAyMjEwMDRfMjQz/MDAxNjY0ODQzNjQzMDc5.SHa8XjadxD9o3CUPo160W_PNbD8BmMx_ThUMvZYSyI0g.5YGbDOEv_D64q0JLm6ac_mZSOrevvZOvIGehjJeY25og.PNG/%EC%9A%B4%EC%98%81%EC%B2%B4%EC%A0%9C_%EC%BB%A4%EB%84%90%EB%AA%A8%EB%93%9C_%EC%82%AC%EC%9A%A9%EC%9E%90%EB%AA%A8%EB%93%9C_2.png?type=w1200"> 

이미지 출처 - 한빛 미디어 https://post.naver.com/viewer/postView.naver?volumeNo=34569580&memberNo=25379965



----

### 컴퓨터의 요소
컴퓨터는 CPU, DMA, 컨트롤러, 메모리, 타이머, 디바이스 컨트롤러 등으로 이루어져 있다.

#### CPU (Central Processing Unit)
    산술 논리연산장치, *제어장치, *레지스터로 구성되어있는 컴퓨터 장치 (≒ 일꾼)
    인터럽트에 의해 단순히 메모리에 존재하는 명령어를 해석하여 실행한다.

* 제어장치 : 프로세스 조작을 지시하는 CPU의 한 부품. 입출력 장치 간 통신을 제어하고 명령어들을 읽고 해석하며 데이터 처리를 위한 순서를 결정한다.
* 레지스터 : CPU 안에 있는 임시기억장치를 가리키며 CPU와 직접 연결되어있어 연산속도가 매우 빠르다. CPU는 데이터 저장할 방법이 없어 레지스터를 거쳐 데이터를 전달한다.