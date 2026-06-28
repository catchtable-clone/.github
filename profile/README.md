<h1 align="center"> CatchEAT </h1>
<div align="center"> 
<h3><b> 맛집 예약 / 빈자리 알림 / AI 챗봇 </b></h3><br>

<img width="600" src="images/main_image.gif" alt="대표 이미지">

<h3><b> Catchtable Clone Coding Project </b></h3>
<br>
</div>
<br><br>


# 📖 Table of Contents
* [Introduction](#-introduction)
* [Demo](#-demo)
* [API](#-api)
* [System Architecture](#-system-architecture)
* [ERD](#-erd)
* [Tech Stack](#-tech-stack)
* [Monitoring](#-monitoring)
* [Directory Structure](#-directory-structure)
* [How to Start](#-how-to-start)
* [Team Members](#-team-members)

<br>

# 📣 Introduction

### 소개
본 프로젝트는 레스토랑 예약 플랫폼 캐치테이블을 클론 코딩하며 매장 검색, 예약, 선착순 쿠폰,
실시간 빈자리 알림, AI 챗봇 서비스를 구현하고 가상 트래픽이 몰리는 상황에서 아키텍처적 결함을 확인하고 개선한 백엔드 엔지니어링 프로젝트입니다.

### 문서
> 📦 Backend Repo: [catchtable-clone/backend](images/catchtable-clone/backend)
>
> 📦 Frontend Repo: [catchtable-clone/frontend](images/catchtable-clone/frontend)

<br>

- **맛집을 검색하고 실시간 잔여 좌석을 예약하는 레스토랑 예약 플랫폼**
- **원하는 매장의 빈자리가 생기면 실시간으로 알림 (Vacancy 구독 + Kafka)**
- **선착순 쿠폰 발급 — Redis Lua + 분산 락으로 대량 트래픽에도 정확한 재고 관리**
- **PortOne(카카오페이) 연동 예약금 결제**
- **위치 기반 매장 검색 (PostGIS) — 내 주변 맛집 탐색**
- **AI 챗봇(Google Gemini)으로 간편하게, 매장 추천/예약 도우미**
- **북마크로 나만의 맛집 리스트 관리**

<br>

# 🕺🏻 Demo

### 메인 / 매장 탐색
> 카테고리 / 지역 / 위치 기반으로 맛집들을 둘러보는 화면입니다.
<br>
<img align="center" width="800" src="images/main_image.gif" alt="메인 화면">
<br><br>

### 로그인 / 마이페이지
> Google 간편 로그인과 사용자의 예약 내역 /리뷰 /쿠폰 관리, 관리자(매장/메뉴/쿠폰) 화면입니다.
<br>
<img align="center" width="800" src="images/login.gif" alt="로그인 화면">
<br><br>

### 매장 상세 / 예약 / 결제
> 매장 정보 / 메뉴를 확인하고 원하는 시간의 잔여 좌석을 예약합니다. 결제 화면은 PortOne 연동 카카오페이 서비스입니다.
<br>
<img align="center" width="800" src="images/store_reservation.gif" alt="예약 화면">
<br><br>

### 빈자리 알림
> 마감된 시간대의 빈자리를 구독하고, 자리가 나면 알림을 받습니다.
<br>
<img align="center" width="800" src="images/vacancy.gif" alt="빈자리 알림 화면">
<br><br>

### 쿠폰
> 선착순 쿠폰을 발급받는 화면입니다.
<br>
<img align="center" width="800" src="images/limited_coupon.gif" alt="쿠폰 화면">
<br><br>

### AI 챗봇
> Google Gemini 기반 챗봇과 대화하며 예약을 진행합니다.
<br>
<img align="center" width="800" src="images/chatbot.gif" alt="AI 챗봇 화면">
<br><br>

<br>

# 📗 API
<div align="center">
<img width="800" src="images/swagger-ui_index.png" alt="API Swagger 이미지">
</div>
<br><br>

# 🛠️ System Architecture <a name="-system-architecture"></a>
<div align="center">
  <img align="center" width="800" src="images/system_architecture.png" alt="System Architecture">
</div>
<br><br>

# 🔑 ERD
<div align="center">
  <img width="800" src="images/erd_image.png" alt="ERD">
</div>
<br><br>


# 💻 Tech Stack

<div align="center">
  <table>
    <tr>
      <th>Field</th>
      <th>Technology of Use</th>
    </tr>
    <tr>
      <td><b>Frontend</b></td>
      <td>
        <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white">
        <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black">
        <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white">
        <img src="https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white">
        <img src="https://img.shields.io/badge/React%20Query-FF4154?style=for-the-badge&logo=reactquery&logoColor=white">
        <img src="https://img.shields.io/badge/Zustand-433E38?style=for-the-badge&logo=react&logoColor=white">
        <img src="https://img.shields.io/badge/Axios-5A29E4?style=for-the-badge&logo=axios&logoColor=white">
        <img src="https://img.shields.io/badge/ESLint-4B32C3?style=for-the-badge&logo=eslint&logoColor=white">
        <img src="https://img.shields.io/badge/Prettier-F7B93E?style=for-the-badge&logo=prettier&logoColor=black">
        <img src="https://img.shields.io/badge/npm-CB3837?style=for-the-badge&logo=npm&logoColor=white">
      </td>
    </tr>
    <tr>
      <td><b>Backend</b></td>
      <td>
        <img src="https://img.shields.io/badge/Java%2021-007396?style=for-the-badge&logo=openjdk&logoColor=white">
        <img src="https://img.shields.io/badge/Spring%20Boot%204-6DB33F?style=for-the-badge&logo=springboot&logoColor=white">
        <img src="https://img.shields.io/badge/Spring%20Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white">
        <img src="https://img.shields.io/badge/Spring%20Data%20JPA-6DB33F?style=for-the-badge&logo=spring&logoColor=white">
        <img src="https://img.shields.io/badge/Hibernate%20Spatial-59666C?style=for-the-badge&logo=hibernate&logoColor=white">
        <img src="https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white">
        <img src="https://img.shields.io/badge/Resilience4j-0B5394?style=for-the-badge&logo=java&logoColor=white">
        <img src="https://img.shields.io/badge/Gradle-02303A?style=for-the-badge&logo=gradle&logoColor=white">
        <img src="https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=swagger&logoColor=black">
        <img src="https://img.shields.io/badge/JUnit5-25A162?style=for-the-badge&logo=junit5&logoColor=white">
        <img src="https://img.shields.io/badge/Testcontainers-291A3F?style=for-the-badge&logo=testcontainers&logoColor=white">
      </td>
    </tr>
    <tr>
      <td><b>Messaging / Cache</b></td>
      <td>
        <img src="https://img.shields.io/badge/Apache%20Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white">
        <img src="https://img.shields.io/badge/Redis-FF4438?style=for-the-badge&logo=redis&logoColor=white">
        <img src="https://img.shields.io/badge/Redisson-CC0000?style=for-the-badge&logo=redis&logoColor=white">
      </td>
    </tr>
    <tr>
      <td><b>Database</b></td>
      <td>
        <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white">
        <img src="https://img.shields.io/badge/PostGIS-008BB9?style=for-the-badge&logo=postgresql&logoColor=white">
      </td>
    </tr>
    <tr>
      <td><b>AI</b></td>
      <td>
        <img src="https://img.shields.io/badge/Spring%20AI-6DB33F?style=for-the-badge&logo=spring&logoColor=white">
        <img src="https://img.shields.io/badge/Google%20Gemini-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white">
      </td>
    </tr>
    <tr>
      <td><b>External API</b></td>
      <td>
        <img src="https://img.shields.io/badge/Google%20OAuth2-4285F4?style=for-the-badge&logo=google&logoColor=white">
        <img src="https://img.shields.io/badge/PortOne-1B64DA?style=for-the-badge&logo=naver&logoColor=white">
        <img src="https://img.shields.io/badge/Kakao%20Map-FFCD00?style=for-the-badge&logo=kakao&logoColor=black">
      </td>
    </tr>
    <tr>
      <td><b>DevOps</b></td>
      <td>
        <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white">
        <img src="https://img.shields.io/badge/NGINX-009639?style=for-the-badge&logo=nginx&logoColor=white">
        <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white">
        <img src="https://img.shields.io/badge/GHCR-181717?style=for-the-badge&logo=github&logoColor=white">
        <img src="https://img.shields.io/badge/Let's%20Encrypt-003A70?style=for-the-badge&logo=letsencrypt&logoColor=white">
      </td>
    </tr>
    <tr>
      <td><b>Monitoring</b></td>
      <td>
        <img src="https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white">
        <img src="https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white">
        <img src="https://img.shields.io/badge/Loki-F46800?style=for-the-badge&logo=grafana&logoColor=white">
        <img src="https://img.shields.io/badge/Promtail-F46800?style=for-the-badge&logo=grafana&logoColor=white">
        <img src="https://img.shields.io/badge/Micrometer-117A65?style=for-the-badge&logo=micrometer&logoColor=white">
      </td>
    </tr>
    <tr>
      <td><b>Load Test</b></td>
      <td>
        <img src="https://img.shields.io/badge/k6-7D64FF?style=for-the-badge&logo=k6&logoColor=white">
      </td>
    </tr>
    <tr>
      <td><b>ETC</b></td>
      <td>
        <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white">
        <img src="https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white">
      </td>
    </tr>
  </table>
</div>
<br><br>

# 📊 Monitoring
<div align="center">
    <img align="center" width="800" src="images/monitoring_1.png" alt="Monitoring image 1">
    <img align="center" width="800" src="images/monitoring_2.png" alt="Monitoring image 2">
</div>

# 📂 Directory Structure

<details>
<summary>CatchEAT</summary>
<pre>
<code>
🗂️ catchtable-clone
┣ 📂 backend                         # Spring Boot 4 (Java 21) REST API
┃ ┣ 📂 src/main/java/com/catchtable
┃ ┃ ┣ 📂 bookmark                    # 북마크 / 즐겨찾기 폴더
┃ ┃ ┣ 📂 chatbot                     # AI 챗봇 (Spring AI + Gemini)
┃ ┃ ┣ 📂 coupon                      # 선착순 쿠폰 (Redis Lua + 분산 락)
┃ ┃ ┣ 📂 file                        # 파일 업로드
┃ ┃ ┣ 📂 menu                        # 메뉴
┃ ┃ ┣ 📂 notification                # 알림 (Kafka)
┃ ┃ ┣ 📂 payment                     # 결제 (PortOne)
┃ ┃ ┣ 📂 remain                      # 잔여 좌석 슬롯
┃ ┃ ┣ 📂 reservation                 # 예약
┃ ┃ ┣ 📂 review                      # 리뷰 / 평점
┃ ┃ ┣ 📂 store                       # 매장 (PostGIS 위치 검색)
┃ ┃ ┣ 📂 user                        # 회원 / 인증
┃ ┃ ┣ 📂 vacancy                     # 빈자리 알림 구독
┃ ┃ ┗ 📂 global                      # config, security, lock, common, exception
┃ ┣ 📂 data                          # 시드 SQL & CSV
┃ ┣ 📂 k6                            # 부하 테스트 시나리오
┃ ┣ 📂 grafana / monitoring / nginx  # 인프라 설정
┃ ┣ 📃 docker-compose.dev.yml
┃ ┣ 📃 docker-compose.prod.yml
┃ ┣ 📃 Dockerfile
┃ ┗ 📃 build.gradle
┗ 📂 frontend                        # Next.js 16 (React 19, TypeScript)
  ┗ 📂 src
    ┣ 📂 app                         # App Router 페이지
    ┣ 📂 components                  # 공통 / 매장 컴포넌트
    ┣ 📂 hooks
    ┣ 📂 lib/api                     # API 클라이언트
    ┣ 📂 stores                      # Zustand 스토어
    ┗ 📂 types
</code>
</pre>
</details>
<br>

# 🧐 How to Start

### Prerequisites
- Java 21
- Docker / Docker Compose
- Node.js 20+

### 1. Clone
```bash
git clone images/catchtable-clone/backend.git
git clone images/catchtable-clone/frontend.git
```

### 2. env setting

* `backend/.env`
```
DB_NAME=
DB_USER=
DB_PASSWORD=
DB_PORT=

GOOGLE_CLIENT_ID=
GOOGLE_CLIENT_SECRET=
GOOGLE_PLACES_API_KEY=

JWT_SECRET=
FRONTEND_URL=

GEMINI_API_KEY=
PORTONE_SECRET_KEY=

GRAFANA_USER=
GRAFANA_PASSWORD=
```

* `frontend/.env`
```
NEXT_PUBLIC_API_URL=
NEXT_PUBLIC_GOOGLE_CLIENT_ID=
NEXT_PUBLIC_KAKAO_MAP_KEY=
NEXT_PUBLIC_PORTONE_STORE_ID=
NEXT_PUBLIC_PORTONE_CHANNEL_KEY=
NEXT_PUBLIC_USE_MOCK=
```

### 3. Run Infra & Backend
```bash
cd backend
docker compose -f docker-compose.dev.yml up -d   # PostgreSQL · Redis · Kafka
./gradlew bootRun                                # http://localhost:8080
```

### 4. Frontend Start
```bash
cd frontend
npm install
npm run dev                                       # http://localhost:3000
```

### 5. 로컬 환경에서 접속
- Web: `http://localhost:3000`
- Swagger: `http://localhost:8080/swagger-ui.html`

<br>

# 👨‍👩‍👧‍👦 Team Members

<table width="800">
<tbody>
<tr>
<th>Name</th>
<td width="150" align="center">김재범</td>
<td width="150" align="center">김동안</td>
<td width="150" align="center">이상진</td>
<td width="150" align="center">이주희</td>
</tr>
<tr>
<th>Profile</th>
<td width="150" align="center">
<a href="https://github.com/jaebeom79">
<img src="images/jaebeom79.jpg" width="50" height="60">
</a>
</td>
<td width="150" align="center">
<a href="https://github.com/docodocod">
<img src="images/docodocod.jpg" width="50" height="60">
</a>
</td>
<td width="150" align="center">
<a href="https://github.com/silkair">
<img src="images/silkair.jpg" width="50" height="60">
</a>
</td>
<td width="150" align="center">
<a href="https://github.com/johe00123">
<img src="images/johe00123.jpg" width="50" height="60">
</a>
</td>
</tr>
<tr>
<th>Role</th>
<td width="150" align="center">Backend</td>
<td width="150" align="center">Backend</td>
<td width="150" align="center">Backend</td>
<td width="150" align="center">Backend</td>
</tr>
<tr>
<th>GitHub</th>
<td width="150" align="center">
<a href="https://github.com/jaebeom79"><img src="http://img.shields.io/badge/jaebeom79-green?style=social&logo=github"/></a>
</td>
<td width="150" align="center">
<a href="https://github.com/docodocod"><img src="http://img.shields.io/badge/docodocod-green?style=social&logo=github"/></a>
</td>
<td width="150" align="center">
<a href="https://github.com/silkair"><img src="http://img.shields.io/badge/silkair-green?style=social&logo=github"/></a>
</td>
<td width="150" align="center">
<a href="https://github.com/johe00123"><img src="http://img.shields.io/badge/johe00123-green?style=social&logo=github"/></a>
</td>
</tr>
</tbody>
</table>
<br><br>