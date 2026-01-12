

## 안녕하세요 주니어 개발자 이두현입니다.



---

## Tech Stacks

**Languages**  
![C](https://img.shields.io/badge/C-00599C?style=flat&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=c%2B%2B&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)

**Embedded / MCU**  
![STM32](https://img.shields.io/badge/STM32-03234B?style=flat&logo=stmicroelectronics&logoColor=white)
![FreeRTOS](https://img.shields.io/badge/FreeRTOS-009688?style=flat)
![ESP8266](https://img.shields.io/badge/ESP8266-000000?style=flat)
![ESP32](https://img.shields.io/badge/ESP32-000000?style=flat)

**Linux & BSP**  
![Embedded Linux](https://img.shields.io/badge/Embedded_Linux-000000?style=flat&logo=linux&logoColor=white)
![CAN Bus](https://img.shields.io/badge/CAN_Bus-003366?style=flat)

**Multimedia / AI**  
![GStreamer](https://img.shields.io/badge/GStreamer-FF6F00?style=flat)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)
![MIL](https://img.shields.io/badge/MIL-000000?style=flat)
![Cognex](https://img.shields.io/badge/Cognex-FFD700?style=flat)
![Hailo-8](https://img.shields.io/badge/Hailo--8-FF1493?style=flat)
![CARLA](https://img.shields.io/badge/CARLA_Simulator-000000?style=flat)

**Tools**  
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)
![VS Code](https://img.shields.io/badge/VS_Code-007ACC?style=flat&logo=visualstudiocode&logoColor=white)
![STM32CubeIDE](https://img.shields.io/badge/STM32CubeIDE-03234B?style=flat)
![CMake](https://img.shields.io/badge/CMake-064F8C?style=flat&logo=cmake&logoColor=white)

---
## 📂 Projects

###  ESS 시설 이상 감지 및 관제 시스템 (E.S.S.E.N.T.I.A.L)
- **핵심 기술:** ROS2, Nav2, C++, MQTT, MariaDB, Qt, Raspberry Pi, STM32, OpenCV, RFID
- **주요 기여**
  - `control_node` 단일 노드로 **50ms Tick FSM** 기반 순찰/리프터/열화상 트리거/홈 복귀를 통합 제어
  - Nav2 Action(`navigate_to_pose`) 기반 **Zone 순찰 + Home 복귀**, TF(`map→base_link`)로 현재 위치 추적 및 Zone 상태 발행
  - `/ess/priority_zone` 수신 시 **Goal 강제 취소 + 정지 + Emergency Queue 우선 처리** 로직 구현
  - 홈 도착 후 **ArUco 정렬 요청/ACK + 10초 타임아웃 fail-safe** 적용
- **Repository:** [ess-guardian](https://github.com/dubung/ess-Guardian)

---

###  Raspberry Pi 5 + Hailo 기반 Smart Blackbox
- **핵심 기술:** Raspberry Pi 5, Hailo-8, Python, GStreamer, CARLA, PETRv2, ONNX
- **주요 기여**
  - CARLA → Raspberry Pi 영상 스트리밍 파이프라인 구성(GStreamer)
  - PETRv2 추론 파이프라인 적용 및 후처리(ONNX) 흐름 연결
- **Repository:** [smart-blackbox](https://github.com/StrongThrow/blackbox-project)

---

###  라즈베리파이 + MCU IoT 무드등 (smart-moodlight)
- **핵심 기술:** Raspberry Pi, STM32/MCU, MariaDB, (App/통신), Weather API, LCD
- **주요 기여**
  - 앱/통신 흐름 구현 및 DB(MariaDB) 연동
  - Weather API로 날씨 데이터 수집 → LCD 출력 기능 구현
- **Repository:** [smart-moodlight](https://github.com/dubung/smart-moodlight)

---

###  STM32 기반 자동차 와이퍼 제어 (Car-Wipers)
- **핵심 기술:** STM32F4(HAL), C, ADC, PWM, Timer ISR, FSM, I2C(LCD)
- **주요 기여**
  - 자동/수동 모드 포함 **전체 펌웨어 동작 흐름(FSM)** 설계
  - Servo 제어를 **구조체 + 함수포인터 기반 API로 캡슐화**(재사용/확장 목적)
  - ADC 입력(조이스틱/수위) + 타이머 기반 와이퍼 스윕 로직 구현
- **Repository:** [Car-Wipers](https://github.com/dubung/Car-Wipers)

---

###  Linux Kernel Device Driver 기반 시간 관리 임베디드 시스템 (SI-TA-PO)
- **핵심 기술:** C, Linux Kernel, GPIO Interrupt, Workqueue, I2C(SSD1306), DS1302, Raspberry Pi
- **주요 기여**
  - DS1302 통신을 **Bit-banging 방식으로 구현**(타이밍/신호 제어 기반) 및 시간 읽기/설정 기능 연동
  - (팀 프로젝트였다면) 내가 담당한 HW/통신 파트 중심으로 기능 검증 및 트러블슈팅 수행
- **Repository:** [SI-TA-PO](REPO_LINK_HERE)

---

##  Study & Algorithm

-  [Algorithm](https://github.com/dubung/Algorithm)  
  백준, 프로그래머스 문제 풀이를 정리한 레포지토리입니다. C/C++ 위주로 문제를 풀이하고 있습니다.

-  [sort-practice](https://github.com/dubung/MySort)  
  버블 정렬, 선택 정렬, 삽입 정렬, 퀵 정렬 등 기본 정렬 알고리즘을 직접 구현해 본 레포지토리입니다. 각 정렬의 동작 방식을 코드와 함께 정리하고 있습니다.

-  [sort-practice](https://github.com/dubung/MySort)  
  

---

##  Contact Me

[![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=flat&logo=Gmail&logoColor=white)](mailto:dlengussla1@gmail.com)
