---
# 2024 ICT 공모전
---
# 프로젝트 주제

![header](https://capsule-render.vercel.app/api?type=venom&color=0:FC4100,100:b678c4&height=200&section=header&text=AI를%20활용한%20산불%20감지%20수막%20설비%20시스템&fontSize=40)

---
## 작품 기간 : 24.03.01 ~ 24.03.31
![개발](https://github.com/BChanGod/BChanGod_Device.github.io/blob/main/%EC%82%B0%EB%B6%88%EA%B0%90%EC%A7%80_%EC%9D%B4%EB%AF%B8%EC%A7%80/%EA%B0%9C%EB%B0%9C%EC%9D%BC%EC%A0%95.jpg)
---
## 주제 선정 배경
![산림청_자료](https://github.com/BChanGod/2024_ICT_Project/assets/159971128/afa049f9-28f3-4954-8455-0f7ea5eada07)

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
## 시스템 구성도
![시스템 구성도](https://github.com/BChanGod/2024_ICT_Project/assets/159971128/24445863-9642-4c8f-919d-c142f1277235)

## FlowChart
![전체시스템_flowchart](https://github.com/BChanGod/2024_ICT_Project/assets/159971128/3566f506-eee6-4758-8099-bc9f8d10f24b)

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
| 팀장 | 이병찬 |Data Set Yolov5 딥러닝 모델을 이용하여 AI 학습, Arduino Actuator, 통신부, H/W 제작|
| 팀원 | 김민환 |Arduino Sensor, Actuator, 통신부, 구성도 및 FlowChart 제작|
| 팀원 | 한민규 |MariaDB DB 생성, data 시각화, 학습된 AI를 Jetson nano Cam으로 검증|

## 향후 목표
AI를 활용한 산불 감지 수막 설비 시스템에서는 수막 설비를 대신하여 모터 펌프를 사용하고 일반 웹캠으로 산불을 감지하였으며, 외부 환경 변화가 적은 실내에서 시연을 진행하였다. 이점을 보완하여 상용화하기 위해서는 아래와 같은 향후 목표를 제안한다.

1) 센서 변경 및 추가
 탐지 거리가 짧은 불꽃 감지 센서를 긴 거리를 인식할 수 있는 센서로 교체하고, 산불에서 발생하는 일산화탄소와 같은 유독 가스를 감지할 수 있는 센서를 추가해 아두이노 센서 부에서 보내는 데이터의 신뢰도를 높일 수 있을 것이다.

2) 빅데이터 활용 기술 적용
 센서 부를 통해 얻은 온도 및 습도 및 환경데이터를 활용해서 산불의 발생 가능성이 얼마나 되는지를 분석하고, 이를 바탕으로 경고 및 예방 시스템을 구축하면 산불의 피해를 줄일 수 있을 것이다.

3) 에너지 효율성 개선
 전력 소비를 최소화하기 위해서, 하드웨어적으로 저전력 센서 사용, 태양광 및 신재생에너지를 활용해서 시스템에 필요한 전력을 공급하고, 젯슨 나노와 액추에이터와 같이 비활성 상태일 때의 전력 소비를 줄이기 위해서 Sleep Mode를 활용해 시스템을 장기간에 걸쳐 운영할 수 있을 것이다.

4) 설비 비용 개선
 기존 주택에 설치되어있는 물탱크와 스프링클러 시스템, 분기 배관 등을 활용해 설치비를 절감시키며 정기적인 유지 보수 또한 쉬워 시설 유지비가 줄어들어 경제적 효용성을 확보할 수 있을 것이다.

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
