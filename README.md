<div align="center">

# 박지원 | Backend Developer

서비스의 기능 구현부터 배포와 운영 안정화까지 연결해서 고민하는 백엔드 개발자입니다.

[![GitHub](https://img.shields.io/badge/GitHub-jiwon824-181717?style=flat-square&logo=github)](https://github.com/jiwon824)
[![Solved.ac](https://img.shields.io/badge/Solved.ac-jiwon0824-17CE3A?style=flat-square&logo=solveddotac&logoColor=white)](https://solved.ac/jiwon0824)

</div>

## About Me

- Spring Boot 기반 REST API와 서비스 정책이 포함된 도메인 로직을 구현했습니다.
- 사용자 진행 상태, 채점, 추천 후보군, 복습 시점과 같은 상태 기반 로직을 설계했습니다.
- Docker Compose, Nginx, AWS EC2를 활용해 서비스 운영 환경을 구성했습니다.
- GitLab CI/CD를 구축하고 빌드·테스트·배포 및 운영 알림을 자동화했습니다.
- 로그와 실행 환경을 기반으로 문제를 분석하고, 해결 과정을 재사용 가능한 운영 기준으로 기록합니다.

## Tech Stack

### Backend

<p>
  <img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white"/>
  <img src="https://img.shields.io/badge/Spring Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white"/>
  <img src="https://img.shields.io/badge/Spring Data JPA-6DB33F?style=flat-square&logo=spring&logoColor=white"/>
  <img src="https://img.shields.io/badge/QueryDSL-0769AD?style=flat-square"/>
  <img src="https://img.shields.io/badge/JUnit5-25A162?style=flat-square&logo=junit5&logoColor=white"/>
</p>

### Frontend

<p>
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=000000"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/>
  <img src="https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white"/>
</p>

### Database & Cache

<p> <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/> <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white"/> <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white"/> <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white"/> <img src="https://img.shields.io/badge/pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white"/> </p>

### Infrastructure & CI/CD

<p>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker Compose-2496ED?style=flat-square&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white"/>
  <img src="https://img.shields.io/badge/AWS EC2-FF9900?style=flat-square&logo=amazonec2&logoColor=white"/>
  <img src="https://img.shields.io/badge/GitLab CI/CD-FC6D26?style=flat-square&logo=gitlab&logoColor=white"/>
</p>

### Monitoring & Tools

<p>
  <img src="https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white"/>
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white"/>
  <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white"/>
  <img src="https://img.shields.io/badge/GitLab-FC6D26?style=flat-square&logo=gitlab&logoColor=white"/>
</p>

## Projects

### 아이다

> 초등학생이 AI의 학습 과정과 한계를 직접 체험하는 AI 리터러시 교육 플랫폼

**2026.04 ~ 2026.05 | 6인 팀 | Infra·Frontend**

- Nginx, Spring Boot, PostgreSQL, Redis를 Docker Compose로 구성하고 운영 서비스별 역할과 네트워크 구조 정리
- 프론트엔드 빌드·테스트와 백엔드 테스트·빌드를 선행하는 GitLab CI/CD 검증 및 배포 파이프라인 구축
- GitLab Webhook을 Discord·Mattermost와 연동해 MR 및 파이프라인 실패 알림 자동화
- Backend healthcheck와 `depends_on: condition: service_healthy`를 적용해 애플리케이션 준비 전 Nginx가 실행되며 발생하던 초기 502 문제 개선
- Certbot webroot 방식으로 HTTPS 인증서를 재발급하고 인증서 볼륨 및 재배포 운영 절차 정리
- PostgreSQL을 외부에 직접 공개하지 않고 SSH 터널을 통해 접근하도록 구성
- Prometheus를 적용하고 `/prometheus` 경로를 Docker Volume으로 분리해 재배포 시 모니터링 데이터가 사라지는 문제 개선
- PNG 이미지 280개를 WebP로 변환해 정적 자산 용량을 64.40MiB에서 41.20MiB로 36.02% 절감
- Git pre-commit 기반 PNG → WebP 자동 변환 흐름을 구성해 자산 관리 작업 자동화
- QA 항목에 긴급도와 난이도 기준을 추가해 사용자 핵심 흐름을 우선적으로 점검할 수 있도록 개선

`Docker Compose` `Nginx` `AWS EC2` `GitLab CI/CD` `Prometheus` `React` `TypeScript` `Vite`

---

### 뉴스바라

> 기술 블로그와 뉴스 콘텐츠를 수집·가공해 요약, 퀴즈, 인사이트를 제공하는 AI 기반 기술 콘텐츠 추천 서비스

**2026.02 ~ 2026.03 | 6인 팀 | Backend·Infra**

- 내 정보 조회, 닉네임·비밀번호 변경, 관심 키워드 조회·수정 및 중복 확인 API 구현
- 회원가입 시 관심 키워드의 임베딩 평균을 계산해 사용자 벡터를 생성하는 로직 구현
- 회원가입 이후 Redis 추천 후보군을 비동기로 초기화하고, 후보군이 부족할 때 DB 조회로 보완하는 pool + fallback 구조 설계
- 기사 목록·상세·스크랩 목록 API와 MongoDB 원문 fallback 정책 보강
- 퀴즈 정답 날짜를 기준으로 연속 학습 일수를 계산하는 스트릭 및 히스토리 API 구현
- FSRS 기반 복습 퀴즈 조회와 복습 간격 갱신 로직 구현
- PostgreSQL, pgvector, Redis, MongoDB를 포함한 Docker Compose 운영 환경 구성
- EC2 Nginx와 Certbot을 활용해 HTTPS Reverse Proxy 구조 구성
- GitLab Runner 기반 빌드·테스트·배포 파이프라인 구축 및 배포 경로와 환경변수 관리 기준 통일
- Vite 환경변수가 빌드 시점에 반영되도록 프론트엔드와 백엔드 환경변수 관리 방식 분리
- Redis 재연결 스레드, HikariPool 종료 및 Testcontainers 종료 순서를 분석해 전체 테스트 시간을 6분 38초에서 1분 33초로 단축
- 사용자·추천·기사·퀴즈 도메인의 Controller, Service, Integration Test 보강
- 외부 라이브러리 보안 이슈 발생 시 선언 버전과 lockfile의 실제 설치 버전을 함께 점검하는 의존성 검증 절차 수행

`Java` `Spring Boot` `JPA` `PostgreSQL` `pgvector` `Redis` `MongoDB` `Docker Compose` `Nginx` `GitLab CI/CD`

---

### SQUIZ

> 스터디 생성부터 학습, 퀴즈, 복습, 통계까지 하나의 흐름으로 제공하는 AI 학습 플랫폼

**2026.01 ~ 2026.02 | 6인 팀 | Full Stack**

#### Backend

- 퀴즈 코스 목록·상세 조회, 문제 풀이, 답안 제출 및 채점 API 구현
- 사용자의 진행 상태에 따라 다음 문제와 접근 가능한 섹션을 결정하는 연속 퀴즈 로직 구현
- 클라이언트가 전달한 정답 여부를 신뢰하지 않고, 서버가 정답과 사용자 답안을 비교하는 서버 중심 채점 구조로 개선
- `attemptId`를 기준으로 진행 중인 퀴즈 세션을 임시저장하고 재개하는 흐름 구현
- 중복 `IN_PROGRESS` 시도 발생 시 답변이 가장 많이 저장된 시도를 보존하는 Self-healing 로직 적용
- FSRS 기반 복습 대상 조회 및 다음 복습 시점 갱신 로직 구현
- 현재 복습 상태와 풀이 이력을 `user_review_items`, `user_review_log`로 분리
- QueryDSL을 활용한 코스별 정답 통계, 오답 목록, 취약 개념 조회 및 정렬·페이징 구현
- QuizCourse, ContinuousQuiz, Review, FSRS Service 및 Repository 테스트 작성·보강

#### Frontend

- 퀴즈 코스 목록·상세·문제 풀이 및 연속 퀴즈 화면 구현
- 오늘의 복습, 틀린 문제, 취약 개념, 학습 통계 화면 구현
- 객관식·복수 선택형·주관식 문제의 답안 입력과 정답·오답 표시 흐름 구현
- 저장된 답안을 퀴즈 재진입 시 복구하도록 프론트엔드 상태와 백엔드 응답 데이터 매핑 개선
- Page Visibility API를 활용한 문제별 응답 시간 측정
- 퀴즈 관련 변환·채점 유틸리티를 공통 모듈로 정리

`Java` `Spring Boot` `JPA` `QueryDSL` `MySQL` `React` `TypeScript` `Vite`

## Education

- (2025.07~2026.06) 삼성청년SWAI아카데미 모바일트랙 14기
- (2023.06~2023.12) 에티버스러닝 유니티 부트캠프 1기
- (2018.02~2022.08) 한국외국어대학교 철학과 컴퓨터전자시스템공학(복수전공)
  
## Certifications & Activities

- (2026.05) 우수 프로젝트(1st): 아이다, AI 리터러시 교육 서비스
- (2026.04) 우수 프로젝트(3rd): 뉴스바라, 관심사 기반 IT 컨텐츠 추천 서비스
- (2025.12) SQLD
- (2025.09) SSAFY 알고리즘 스터디 운영(9월 우수 스터디 선정)
- (2024.12) 정보처리기사

## GitHub Activity

<div align="center">

<a href="https://www.gitanimals.org/en_US?utm_medium=image&utm_source=jiwon824&utm_content=farm">
  <img
    src="https://render.gitanimals.org/farms/jiwon824"
    width="600"
    height="300"
    alt="GitAnimals Farm"
  />
</a>

<br/>

[![Solved.ac Profile](http://mazassumnida.wtf/api/generate_badge?boj=jiwon0824)](https://solved.ac/jiwon0824)

<br/>

<img
  src="https://github-readme-stats.vercel.app/api?username=jiwon824&show_icons=true&theme=onedark"
  alt="GitHub Stats"
/>

</div>
