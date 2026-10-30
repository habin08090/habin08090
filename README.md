# 안녕하세요, 백엔드 개발자 김하빈입니다.

> **원인을 분석하고, 근거를 갖고 개선하는 백엔드 개발자**
> 화학과에서 컴퓨터소프트웨어공학부로 전과하며, 문제를 분해하고 원인과 결과를 따져 보는 사고방식으로 개발합니다.

### 🛠 Tech Stack
- **Backend**: Java 17, Spring Boot, Spring Data JPA, QueryDSL
- **Database & Cache**: PostgreSQL, Redis (캐시, Lua 스크립트), Flyway
- **External**: OpenFeign, WebSocket(STOMP), Jsoup
- **Testing & Quality**: JUnit 5, Mockito, FixtureMonkey, JaCoCo
- **Tools**: Git/GitHub (Fork 기반 협업, PR 리뷰), Docker (로컬 개발 환경), AWS S3 (팀 구성 환경 연동), Swagger

### 📌 Featured Projects
**[Otboo (옷장을 부탁해)](https://github.com/sb11-code-rangers/sb11-otboo-team4)** — 날씨·프로필 기반 의상 추천 & AI 챗봇 서비스 (백엔드 4인 팀, API 11개 담당)
- LLM 추천 결과를 Redis에 캐싱해 첫 호출 3.9초 → 캐시 적중 시 0.02초 (로컬 실측). 입력 해시 기반 캐시 키로 별도 무효화 없이 최신성 유지, 장애 시 규칙 기반 추천으로 폴백
- 쇼핑몰 OG 태그를 먼저 파싱하고 비어 있을 때만 LLM을 호출해 불필요한 호출을 줄임
- 기존 DM·STOMP 구조를 재사용해 팀 코드 수정 없이 챗봇 구현, Redis Lua 스크립트로 요청 횟수 제한
- 테스트 252개 작성, 담당 패키지 라인 커버리지 97.4% (로컬 JaCoCo 기준)
