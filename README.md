### 기술 스택
**주력 기술**
**주력 기술**
<div>
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=JavaScript&logoColor=black"/>
<img src="https://img.shields.io/badge/Vue.js-4FC08D?style=for-the-badge&logo=vue.js&logoColor=white"/>
<img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black"/>
<img src="https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=java&logoColor=white"/>
</div>

**임베디드 & 하드웨어**
<div>
<img src="https://img.shields.io/badge/STM32-03234B?style=for-the-badge&logo=STMicroelectronics&logoColor=white"/>
<img src="https://img.shields.io/badge/AVR-EE2E24?style=for-the-badge&logo=arduino&logoColor=white"/>
<img src="https://img.shields.io/badge/Verilog-0080FF?style=for-the-badge&logoColor=white"/>
<img src="https://img.shields.io/badge/FPGA-00979D?style=for-the-badge&logo=intel&logoColor=white"/>
</div>

### ⚡ 개발 경험
### 진행한 프로젝트

### 웹
```
💻 2024   EBS 온라인클래스 플랫폼 유지보수 | Vue.js, Nuxt.js
🔧 2024   Boardify (협업 프로젝트 관리 도구) | Vue.js, Supabase
🎮 2023   Escape From Tarkov Helper | React
📈 2023   Blueocean (주식정보 웹사이트) | Java, Spring
💊 2023   Pilldex (약물 검색 웹사이트) | Java, Spring
```

### 임베디드
```
🌀 2025   AVR 선풍기 | Atmega128a
🛗 2025   ARM 엘레베이터 | Stm32
🚗 2025   ARM RC카 / 자율주행 | Stm32
```

### 포트폴리오 및 이메일
<a href="https://webdesklinker.netlify.app/" target="_blank" rel="noopener noreferrer">
    <img src="https://img.shields.io/badge/Portfolio-00C7B7?style=for-the-badge&logo=Netlify&logoColor=white"/>
</a>
<a href="https://minsportfolio.netlify.app//" target="_blank" rel="noopener noreferrer">
    <img src="https://img.shields.io/badge/Portfolio-4285F4?style=for-the-badge&logo=GoogleChrome&logoColor=white"/>
</a>
<a href="mailto:alsvhtks@naver.com">
    <img src="https://img.shields.io/badge/이메일-EA4335?style=for-the-badge&logo=gmail&logoColor=white"/>
</a>

### 플로우차트
```mermaid
flowchart LR
    A((시스템 시작)) --> B[/센서 모니터링/]
    
    B --> C[/온도센서 DHT11/]
    B --> D[/거리센서 초음파/]
    B --> E[/키패드 입력/]
    B --> F[/도어버튼 입력/]
    B --> G[/조도센서 ADC/]
    B --> H[/사운드센서 ADC/]
    
    C --> I{고온감지?}
    D --> J{사람감지?}
    I --> K{환기팬 ON 조건?} 
    J --> K
    K -->|Yes| L[환기팬 켜기]
    K -->|No| M[환기팬 끄기]
    
    E --> N{패스워드 인증?}
    N -->|성공| O[도어 열림 10초]
    N -->|실패| P[다시 입력]
    
    F --> Q[수동 개방 10초]
    
    G --> R{조도 ≥ 2000?}
    R -->|Yes| S[커튼 닫기]
    R -->|No| T[커튼 열기]
    
    H --> U{박수 감지 ≥ 3000?}
    U -->|2회 연속| V[LED 토글]
    U -->|No| W[LED 유지]
    
    O --> X[서보모터 도어 제어]
    Q --> X
    S --> Y[서보모터 커튼 제어]
    T --> Y
    
    L --> Z[상태 표시 LED+7SEG]
    M --> Z
    V --> Z
    W --> Z
    X --> Z
    Y --> Z
    P --> B
    Z --> B
