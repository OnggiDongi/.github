<img width="460" height="460" alt="image" src="https://github.com/user-attachments/assets/c98e226b-68da-4f45-815a-b037a25454f1" /># ✨ 디지털하나로 금융서비스개발 7기 2차 프로젝트 — **따봉(DDABONG)**

> **시니어 재능봉사 매칭 & 포인트 리워드 플랫폼**  
> 심심한 시간을 **따뜻한 온기**로. 시니어의 재능이 필요한 현장과 연결하고, 활동 시간은 **포인트(하나머니 연계 가정)**로 보상됩니다.  
> **교감 → 신뢰 → 손님**으로 이어지는 지역 선순환을 만듭니다.

---

## 🧭 핵심 한 줄
**“시니어의 시간과 재능을 가치로 바꿉니다.”**  
가까운 곳의 **가벼운 봉사**부터, 경력·자격을 살린 **전문 봉사**까지.

---

## 👩🏻‍💻 옹기동기 팀 소개
| [<img src="https://github.com/sooocong.png" width="100"/>](https://github.com/sooocong) | [<img src="https://github.com/kiyeonkimm.png" width="100"/>](https://github.com/kiyeonkimm) | [<img src="https://github.com/bokyeommmmm.png" width="100"/>](https://github.com/bokyeommmmm) | [<img src="https://github.com/Ausdauer1.png" width="100"/>](https://github.com/Ausdauer1) | [<img src="https://github.com/dlwlals1289.png" width="100"/>](https://github.com/dlwlals1289) |
|:--:|:--:|:--:|:--:|:--:|:--:|
| 최수빈(팀장) | 김기연 | 김보겸 | 우재현 | 이지민 |

---

## 🔨 기술 스택

| 분류 | 기술 |
|:-:|:-|
| Language | TypeScript, Java |
| Frontend | Next.js(React), Tailwind CSS, React Query, Axios |
| Backend | Spring Boot, Spring Security(JWT), Spring Data JPA, QueryDSL |
| Infra | MySQL, Docker, GitHub Actions(CI), AWS S3(파일 업로드) |
| Docs & Monitoring | Swagger(OpenAPI), Spring Actuator, Logback(콘솔/파일 분리·롤링) |
| Test | Vitest(FE), JPA Repository Tests(BE) |
| Collaboration | Figma, Notion, Slack, GitHub |

---

## 🎯 문제 정의 & 인사이트
- **은퇴 후 시간의 공백**과 **사회적 고립** 증가  
- 기존 플랫폼의 **시니어 친화성 부족**(큰 글씨/간단 동선/오프라인 연계 부족)  
- “봉사=무상” 인식 → **시간의 가치화** 필요

**해결:** 시니어의 시간·재능을 **포인트화**하고, 기관·소상공인과의 **호혜 구조**를 설계

---

## 🍥 서비스 핵심 기능

### 1) 시니어 맞춤 추천
- 연령/거주지/관심/체력소모도 기반 추천  
- **글을 못 써도 OK**: 키워드·장소·시간만 입력하면 **모집글 자동 생성**(템플릿 + LLM 프롬프트)

### 2) 봉사 시간 → 리워드
- 활동 시간 누적 **포인트 적립**  
- **50시간마다 봉사 인증서(PDF)** 자동 발급

### 3) 기관 관리(백오피스)
- 모집글 등록/지원자 관리/활동 평가  
- **AI 요약 리뷰**로 후기 자동 요약·태깅

### 4) 로컬 연계(브랜드 플러스)
- 행사 시 **하나 버스·커피차** 지원 시나리오  
- **노란우산공제 가맹 소상공인**과 포인트 사용 연계(상권 활성화)

### 5) 접근성·신뢰
- 큰 글씨, 단순 동선, 명확한 버튼  
- **자녀-시니어 화면 분리**(권한·알림 연동)  
- **JWT 기반 Role 접근 제어**(ROLE_ADMIN/ROLE_USER)

---

## 🗃️ ERD 다이어그램
<img src="https://github.com/user-attachments/assets/86932126-b888-4e80-a1bd-9eec844abdfa" width="720" />

**핵심 엔터티(요약)**  
- `Member`(시니어/기관관리자), `VolunteerActivity`(모집/카테고리/체력도/위치)  
- `Application`(지원/상태/평가), `VolunteerRecord`(시간 누적, 인증서 트리거)  
- `PointLedger`(적립/사용), `Order`(정산), `Item`–`ItemImages`(1:N, TMP→ORIGIN)

---<img width="5760" height="3240" alt="서비스 소개" src="" />



## 📸 서비스 스냅샷
<p>
  <img src="https://github.com/user-attachments/assets/e5006767-65de-4ae3-bc1b-92f4eefe98d0" width="320" />
</p>
<p>
  <img src="https://github.com/user-attachments/assets/3eedde87-5904-448e-89ca-7b5f0b9bdf0b" width="320" />
  <img src="https://github.com/user-attachments/assets/5c47d22c-80e6-437c-a4fe-5261185fefac" width="320" />
  <img src="https://github.com/user-attachments/assets/505a9891-befe-4388-8168-92f7c3cade1b" width="320" />
  <img src="https://github.com/user-attachments/assets/f81a076e-69d7-42a9-bfce-9d0f2ee6e3ef" width="320" />
</p>

---

## 🏗️ 모놀리포 구조(예시)
