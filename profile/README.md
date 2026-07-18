<div align="center">

# 🎬 ScenePick
### 당신의 순간을 기록하고, 감상을 나누는 장면 기반 아카이빙 플랫폼

<br />

| 안송희 / AN SONGHEE      | 한현 / HAN HYEON       |
| :--------: | :--------: |
| <img width="150" height="150" alt="image" src="https://github.com/user-attachments/assets/2e313387-a16d-4646-82f1-80b74b619a3b" /> | <img width="150" height="150" alt="image" src="https://github.com/user-attachments/assets/65b5f50b-63a3-4bf5-a3bb-1fe03cb48c0c" /> |
| [@soooii](https://github.com/soooii)    | [@Hann244](https://github.com/Hann244)    |
<br />

### 🌐 [ScenePick 서비스 바로가기](https://scenepick.co.kr/)
[Frontend Repository](https://github.com/ScenePick-Project/ScenePick-FE) ·
[Backend Repository](https://github.com/ScenePick-Project/ScenePick-BE)

</div>

<br />

---

## 📌 프로젝트 소개

**ScenePick**은 영화, 드라마, 애니메이션 등 콘텐츠 속 인상 깊은 장면을
특정 재생 구간 단위로 기록하고 공유하는 **장면 중심 아카이빙 플랫폼**입니다.

사용자는 장면의 시작·종료 시간과 감상을 함께 저장하고,
타임스탬프와 OST가 포함된 리뷰를 통해 다른 사용자와 감상을 공유할 수 있습니다.

### 핵심 기능

* 시작·종료 시간을 지정한 장면 저장 및 개인 보관
* 타임스탬프와 OST를 첨부한 장면 기반 리뷰
* 작품·에피소드·배우·OST 검색 및 콘텐츠 탐색

<br />

| 구분           | 내용                           |
| :----------- | :--------------------------- |
| **개발 형태**    | 2인 팀 프로젝트                    |
| **개발 기간**    | 진행 중               |
| **진행 상태**    | 개발 진행 중                      |
| **서비스** | [ScenePick 바로가기](https://scenepick.co.kr/) |
| **Frontend** | React, TypeScript, Vite      |
| **Backend**  | Spring Boot, MyBatis, Oracle |

---

## 🏗️ Infrastructure Architecture
ScenePick의 프론트엔드 배포부터 백엔드 API 서버 및 데이터베이스까지의 전체 인프라 구성입니다.
<img width="1314" height="668" alt="image" src="https://github.com/user-attachments/assets/fefce43c-5082-4e98-8d39-e9169fd0169c" />
- 사용자 요청은 Cloudflare를 통해 처리됩니다.
- 프론트엔드 정적 리소스는 AWS S3에 배포했습니다.
- 백엔드 API는 OCI의 Public Load Balancer를 거쳐 Private Subnet의 Kubernetes Cluster로 전달됩니다.
- Kubernetes 내부의 ingress-nginx가 요청을 Spring Boot Pod로 라우팅합니다.
- 서비스 데이터는 Oracle Autonomous Database에 저장합니다.
- Bastion Server와 NAT Gateway를 통해 Private Subnet의 관리 및 외부 통신 경로를 구성했습니다.

---

## 📚 Project Documents

| 문서 | 설명 | 링크 |
| :--- | :--- | :---: |
| **IA** | 메뉴 구조, 기능 정의 및 개발 우선순위 | [바로가기](https://docs.google.com/spreadsheets/d/1-9HRAgQo5EfBozrs3qvHwOSrQhuJo22FT6aHHwsjsok/edit?gid=1762384318#gid=1762384318) |
| **API 명세서** | Frontend와 Backend 간 API 요청 및 응답 정의 | [바로가기](https://app.notion.com/p/ScenePick-API-2d1ef591f8938070b4daf4d5ae62da2b) |
| **Figma** | 스토리보드, 와이어프레임 및 화면 설계 | [바로가기](https://www.figma.com/design/PymaKqAqShg4UK9J5t0b3k/%EC%94%AC%ED%94%BD-ScenePick-?node-id=24-2&p=f&t=7Hz6SNGA4XI9AlIa-0) |

<br />

---

## 🚧 Development Status

ScenePick은 현재 개발 진행 중인 2인 팀 프로젝트입니다.

장면 저장, 타임스탬프 기반 리뷰, 작품 및 에피소드 조회 등  
핵심 기능을 우선순위에 따라 구현하고 있습니다.

상세 기능과 개발 우선순위는  
[IA 문서](https://docs.google.com/spreadsheets/d/1-9HRAgQo5EfBozrs3qvHwOSrQhuJo22FT6aHHwsjsok/edit?gid=1762384318#gid=1762384318)에서 확인할 수 있습니다.

<br />

---

<div align="center">

### 🎬 기억하고 싶은 장면을 ScenePick에 남겨보세요.

[🌐 ScenePick 서비스 바로가기](https://scenepick.co.kr/)

</div>
