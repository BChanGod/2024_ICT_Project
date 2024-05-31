---
# 2024 ICT 공모전
---
# 프로젝트 주제

![header](https://capsule-render.vercel.app/api?type=venom&color=0:FC4100,100:b678c4&height=200&section=header&text=AI를_활용한_산불_감지_수막_설비_시스템&fontSize=40)

---
## 작품 기간 : 24.03.01 ~ 24.03.31
---
## 주제 선정 배경
전 세계적인 기후 변화로 산불 발생 빈도와 규모가 커지는 추세이고, 봄철의 경우 건조하여 산불 발생 빈도가 높다.
<br>

우리나라의 경우 2023년 크고 작은 산불이 569건 발생하여 4,992ha의 산림이 소실되었고, 산불이 번져 주택과 시설, 인명 피해까지 일어난다.
<br>

이 설비는 산림 인접 주택이나 시설을 시작으로 점차 확대될 것이지만, 수동으로 동작하다 보니 주 부재 시 대응하기 힘들다는 문제점이 있어 센서들과 AI, 다양한 첨단 기술을 이용해 화재를 막기 위해 주택과 시설 주변에 수막 설비 시스템을 설치하고 불이 붙지 못하도록 한다.

## 기술 구현 목표
1. 가스 센서, 적외선 불꽃 감지 센서, 온/습도 센서로 산불 초기 감지 > wifi와 통신하는 센서 값과 GPS 위치를 DB에 데이터 전송
2. 산불과 연기를 학습한 카메라가 산불 인식 > DB에 센서 데이터 전송
3. 화재 인식과 동시에 Buzzer가 울리면서 LED 점멸(경고, 대피용), 소방당국이 DB를 통해 실시간 정보와 GPS로 위치를 확인할 수 있다.
4. 수막 설비 시스템 동작 > DB로 Actuator 데이터 전송
5. DB를 소방서와 공유 > 화재가 감지된 장소로 이동
6. 불이 진압 되면 수막 설비 시스템 종료

## 기대 효과
- 산불 발생 시 초기에 감지 및 진화하여 산불 확산을 사전에 방지한다.
- 사람 눈으로 산불 발견이 어려운 만큼 IoT 센서와 딥러닝으로 학습된 카메라를 통해 이중으로 감지한다.
- 자동화된 시스템을 통해 산불이 마을로 접근하는 경우 주민들의 대피 시간을 확보하며 물적 피해 또한 줄인다.

<br>

**위의 효과로 대피 시간 확보와 산불 번짐을 저지 및 둔화 시킬 수 있으며, 적은 인원으로 효율적인 시스템 관리와 소방산업 활성화의 기여할 것**

---
## 개발 환경
| Board | Arduino | Jetson Nono | Raspberry Pi|
| --- | --- | --- | --- |
| Language | C++ |Python|C, PhP|
| OS |Windows|NVIDIA JetPack|RaspberryPi, linux|
| Library |DHT, SerialSoftWare, WiFiEsp, TinyGps, I2C|OpenCV, Yolov5|sys/socket, type, stdio, pthread, netinet/in.sys/stat, arpa/inet|
| System | Arduino |VSCode|GCC, APACHE, MariaDB|

## 프로젝트 팀원
|  | 이  름 | 역할 분담 |
| --- | --- | --- |
| 팀장 | 이병찬 |Data Set Yolov5 학습, Arduino Actuator, 통신부, H/W 제작|
| 팀원 | 김민환 |Arduino Sensor, Actuator, 통신부, 구성도 및 FlowChart 제작|
| 팀원 | 한민규 |MariaDB DB생성, data 시각화, AI 학습 data Jetson nano Cam 인식|

## 개발 일정
![개발](https://github.com/BChanGod/BChanGod_Device.github.io/blob/main/%EC%82%B0%EB%B6%88%EA%B0%90%EC%A7%80_%EC%9D%B4%EB%AF%B8%EC%A7%80/%EA%B0%9C%EB%B0%9C%EC%9D%BC%EC%A0%95.jpg)

## 향후 목표
-준비-

## 참고 자료, 문헌
- 산림청, 산불 발생 현황, https://www.forest.go.kr/kfsweb/kfi/kfs/frfr/selectFrfrStats.do?mn=NKFS_02_02_01_05
- KBS “산불 취약한 산지 주택…‘수막으로 보호’”, https://news.kbs.co.kr/news/pc/view/view.do?ncd=7909242
- 인텔리즈 [딥러닝 기술 동향] Yolo V5 - Deep learning, https://blog.naver.com/PostView.naver?blogId=intelliz&logNo=222824372526
- YOLO v5 논문 리뷰, https://cake.tistory.com/34
- 한국건설기술연구원, (2020.12), “경제성 및 화재 안전성 향상을 위한 스마트 스프링클러 시스템”, p.16
- 한국농촌경제신문, “산불 진화효율 높이자... 'K-산불시스템' 기대”, http://kenews.co.kr/mobile/article.html?no=79718
- 이준원, (2020), 메이커를 위한 아두이노의 모든 것, 프리렉
- 윤성우, (2009), 윤성우의 열혈 TCP/IP 소켓 프로그래밍, 오렌지미디어
- 서영진, (2020), 사물인터넷을 위한 리눅스 프로그래밍 with 라즈베리파이, 제이펍
