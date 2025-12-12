# ✋임베디드 소프트웨어 개발자 김동현입니다.

## SKILLS
![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=cplusplus&logoColor=white)
![javascript](https://img.shields.io/badge/JAVASCRIPT-F7D1E?style=flat-square&logo=JavaScript&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=white)
![UBUNTU](https://img.shields.io/badge/UBUNTU-E95420?style=flat-square&logo=ubuntu&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Arduino](https://img.shields.io/badge/Arduino-00878F?style=flat-square&logo=arduino&logoColor=white)
![RaspberryPi](https://img.shields.io/badge/RaspberryPi-A22846?style=flat-square&logo=raspberrypi&logoColor=white)
![Qt](https://img.shields.io/badge/Qt-41CD52?style=flat-square&logo=qt&logoColor=white)
![OpenCv](https://img.shields.io/badge/OpenCv-5C3EE8?style=flat-square&logo=opencv&logoColor=white)



## Featured Projects
### 1. 👾 STM32 Mini Pac-Man Game 
- **[프로젝트 설명]**

  STM32 마이크로컨트롤러(F429ZI)를 활용해 LCD에 출력되는 미니 팩맨 게임을 구현한 임베디드 프로젝트입니다.
게임 로직, 조이스틱 입력, 타이머 이벤트, 부저 사운드 등을 포함한 작은 규모의 게임 시스템을 STM32로 구성했습니다. 
- **[주요 역할]**

  1️⃣ 게임 로직 구현
     팩맨/적 캐릭터 동작 로직
     게임 상태 처리 및 충돌 검사
     LCD에 상태 출력

  2️⃣ ADC 기반 조이스틱 입력 처리
     ADC DMA Setup
     방향 판별 함수 구현
  
- **[사용한 기술]**

  'STM32CubeIDE' ,'ADC 모드' , '타이머 인터럽트' 
- **[시스템 회로도]**
<img width="640" height="460" alt="{8633471F-6860-4878-95A1-ABBB25E3D4B5}" src="https://github.com/user-attachments/assets/9521ccba-b00e-4dee-8502-3fb79e61444b" />

- **[게임 로직 구조]**

▶️ 조이스틱 방향 -> 팩맨 이동 -> LCD 갱신 -> 적 이동 -> 충돌 or 승리 검사

1️⃣ 게임 상태: ING(게임 진행 중), WIN(승리), OVER(실패)
조이스틱 방향 -> 팩맨 이동 -> LCD 갱신 -> 적 이동 -> 충돌 or 승리 검사

2️⃣ LCD 출력 처리: I2C 기반의 16*2 문자 LCD 사용, 팩만 & 적 캐릭터 커스텀 문자를 등록하여 그래픽처럼 표시
(LCD Custom Character Generator 사이트 활용)

3️⃣ 타이머 & PWM: TIM2 적 움직임 제어용, TIM3 부저 PWM 사운드 제어
   
- **[시연 영상]**  
  <a href="https://youtube.com/shorts/oa5NfzWY2-4?si=lXIWHLyZj8PD6Caf">
  <img src="https://img.shields.io/badge/YouTube-Video-FF0000?style=flat-square&logo=youtube&logoColor=white">
  </a>
### 2. OpenVINO 기반 공장 컨베이어 자동화 시스템
- **[프로젝트 설명]** OpenVINO로 최적화된 AI 모델을 활용하여, 단일 컨베이어 벨트 위에서 3가지(정상, 부분불량, 완전불량) 유형의 제품을 실시간으로 선별하는 자동화 시스템을 개발했습니다.
- **[주요 역할]** **PM**을 맡아 전체 **코드 통합** 및 **하드웨어 연동** 테스트를 총괄했습니다. (Arduino, 컨베이어 제어 등)
- **[사용한 기술]** `Python`, `OpenVINO`, `Tkinter`, `Arduino`, `MySQL`, `PySerial`
- **[관련 링크]**  
  <a href="https://github.com/kccistc/intel-08/tree/main/Team2">
  <img src="https://img.shields.io/badge/GitHub-Repository-181717?style=flat-square&logo=github&logoColor=white">
  </a>
- **[영상]**  
  <a href="https://youtu.be/eomAWej_1nU">
  <img src="https://img.shields.io/badge/YouTube-Video-FF0000?style=flat-square&logo=youtube&logoColor=white">
  </a>

### 2. AI 기반 장문 텍스트 요약 서비스 (캡스톤 디자인)
- **[프로젝트 설명]** SKT의 KoBART 요약 모델을 활용하여 사용자가 입력한 장문의 텍스트를 핵심 내용으로 요약해주는 프로그램을 개발했습니다. Jetson Nano Orin 환경에서 AI 모델을 서빙하는 백엔드를 구축했습니다.
- **[주요 역할]** 
- **[사용한 기술]** `Python`, `FastAPI`, `Hugging Face`, `PyTorch`, `Jetson Nano`, `HTML/JS/PHP`
- **[관련 링크]**  
  <a href="https://github.com/seo-amugae/Long-article-summary">
  <img src="https://img.shields.io/badge/GitHub-Repository-181717?style=flat-square&logo=github&logoColor=white">
  </a>

### 3. CDS 센서 기반 태양광 패널 추적 시스템
- **[프로젝트 설명]** 8방위로 배치된 CDS 조도 센서 모듈을 통해 가장 밝은 빛을 감지하고, STM32 보드를 이용해 태양광 패널이 항상 태양을 향하도록 자동 회전하는 시스템을 구현했습니다.
- **[주요 역할]** **STM32 파트의 하드웨어 설계** 및 **펌웨어 프로그래밍**을 담당했습니다. (ESP8266 WiFi 통신, MySQL DB 데이터 저장, 패널 회전 로직 구현)
- **[사용한 기술]** `C`, `STM32`, `Arduino`, `MySQL`, `HTML`
- **[관련 링크]**  
  <a href="https://github.com/intel-edge-ai-sw-8/250826_2nd_miniproj_08"><img src="https://img.shields.io/badge/GitHub-Repository-181717?style=flat-square&logo=github&logoColor=white"></a>
- **[영상]**  
  <a href="https://youtu.be/LcX8HYHIwDM">
  <img src="https://img.shields.io/badge/YouTube-Video-FF0000?style=flat-square&logo=youtube&logoColor=white">
  </a>

### 4. 차량 승하차 편의를 위한 자동 시트 조절기 (개인 프로젝트)
- **[프로젝트 설명]** 차량 승하차 편의를 위해, 차량 시동 상태와 기어 상태(P단)를 감지하여 시트 포지션을 자동으로 조절하는 하드웨어 시스템을 개발했습니다.
- **[주요 역할]** 개인 프로젝트 (회로 설계, Arduino 프로그래밍 및 차량 설치)
- **[사용한 기술]** `Arduino`, `Relay 2CH`
- **[관련 링크]**  
  <a href="https://github.com/seo-amugae/auto-seat-height-controller"><img src="https://img.shields.io/badge/GitHub-Repository-181717?style=flat-square&logo=github&logoColor=white"></a>
- **[영상]**  
  <a href="https://youtu.be/nxEUnxjBgeY">
  <img src="https://img.shields.io/badge/YouTube-Video-FF0000?style=flat-square&logo=youtube&logoColor=white">
  </a>

---

## Education

* **백석대학교** 컴퓨터공학부 인공지능학 졸업 예정 (2026.07.)
* **대한상공회의소 서울기술교육센터** 인텔 AI 엣지 아카데미 교육 수료중 (2025.07. ~ 2026.01.)

---

## Connect with Me

E-MAIL: thisme1227@gmail.com
