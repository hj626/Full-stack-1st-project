# 🚀 Fundee (크라우드 펀딩 플랫폼)
**Position : 결제 시스템 개발, 수량별 자동 계산, 구매 내역 DB 관리, PPT 제작**
<br>
<br>

> **"소비를 즐겁게! 즐거운 후원문화를 만들고 싶습니다."** <br>
>
> Fundee는 Spring Framework와 MyBatis를 기반으로 구축된 사용자 중심의 크라우드 펀딩 웹 서비스입니다.


---

## ✨ 프로젝트 소개

**Fundee**는 판매자와 사용자 모두 클라우드 펀딩을 통하여 즐거운 후원문화를 만들어가고자
개발한 서비스입니다.

---

## 🎯 제작 배경

- 감정은 분명하지만 시간이 지나면 쉽게 희미해짐
- 기존 감정 기록 앱은 감정 선택 중심 → 흐름 파악이 어려움
- 글 기반 감정 분석을 통해 더 자연스러운 기록 경험 제공

---

## 🛠 기술 스택 (Tech Stack)

[![stackticon](https://firebasestorage.googleapis.com/v0/b/stackticon-81399.appspot.com/o/images%2F1772512284735?alt=media&token=6125330b-c6e5-4c7d-9768-897434946352)](https://github.com/msdio/stackticon)

- **Backend:** : Spring Framework (Legacy Project), Java, Oracle DB, MyBatis
- **Frontend** : JavaScript, Bootstrap, CSS


---

## 📁 프로젝트 구조


```
Fundee/
src/
└─ main
    ├─ java (Backend)
    │   └─ com.fundee
    │       ├─ pro         # 메인 비즈니스 로직 및 컨트롤러
    │       ├─ dao         # Data Access Object (DB 접근 계층)
    │       ├─ dto         # Data Transfer Object (데이터 객체)
    │       ├─ mapper      # MyBatis Mapper 인터페이스
    │       └─ util        # 공통 유틸리티 클래스
    │
    ├─ resources (Settings)
    │   └─ mapper          # MyBatis SQL XML 파일 (쿼리문 관리)
    │
    └─ webapp (Frontend)
        ├─ resources       # 정적 리소스 (CSS, JS, Fonts, Images)
        │   ├─ css
        │   ├─ js
        │   └─ images
        └─ WEB-INF
            ├─ spring      # 스프링 설정 (App/Root Context)
            └─ views       # JSP 페이지 (UI 레이아웃 및 뷰)

```

---


## 📌 주요 기능 (Key Features)

### 1. 계정 및 보안 (Account & Security)
- **세션 기반 로그인:** 일반 회원과 관리자(Role 0/1) 권한 분리.
- **HandlerInterceptor:** 보안 강화 및 권한 없는 사용자의 접근 제어. 
- **주소 API:** 카카오 주소 API를 통한 정확한 배송지 입력. 

### 2. 메인 및 상품 (Main & Product)
- **추천 상품:** 달성률 및 판매가 정보를 담은 펀딩 추천 상품 노출.
- **찜하기 기능:** Cookie를 활용하여 비로그인 상태에서도 관심 상품 저장.
- **시각화:** 펀딩 달성률을 그래프 바(Graph Bar) 형태로 자동 업데이트하여 노출.

### 3. 펀딩 및 결제 (Funding & Purchase)
- **자동 계산:** 사용자가 수량을 변경할 때마다 실시간으로 최종 결제 금액 반영.
- **데이터 관리:** 결제 완료 시 시퀀스를 활용한 구매 번호 자동 생성 및 DB 저장.
- **마이페이지:** 사용자의 과거 후원 내역 및 문의 내역 리스트 조회.

---

## 🗄 DB 설계 (Database ERD)
주요 테이블: `MEMBER`, `POSTS`, `BUY_LIST`, `NOTICE`, `QUESTION`, `ANSWER`


- **MEMBER:** 회원 정보 및 등급(Role) 관리.
- **POSTS:** 펀딩 상품 정보 및 목표 금액 관리.
- **BUY_LIST:** 구매 내역 및 결제 금액 저장 (MEMBER, POSTS 참조).


---

## 🔄 User Flow

### 👤 일반 사용자 (User)
1. 메인 페이지
2. 상품 리스트 페이지
3. 상품 상세 페이지
4. 결제 페이지
5. 마이페이지
6. 공지사항 및 Q&A


### 🔐 관리자 (Admin)
1. 관리자 로그인
2. 상품 관리 페이지
3. 게시판 관리


---

## 🌱 프로젝트 회고

- 구매 및 목표 펀딩금액 달성시 즐거움을 주는 시각적인 요소 추가 필요.
- 모바일 버전 디자인 보완 필요.
- 기능과 사용자 편의를 고려한 기능 및 기초 아키텍쳐에 보완에 대한 아쉬움.
  
---

## 🔮 향후 계획

- 시각적인 즐거움을 주는 그래픽 요소 추가 및 모바일 ver 레이아웃 수정.
- 플랫폼 접근성 확대를 위한 모바일 앱 출시.
- 사용자와 어드민 입장에서 필요한 기능과 필요없는 기능 분리 후 수정.
- 상품 카테고리 분류 기능 추가 및 Spring Security 도입을 통한 보안 체계 강화.
- 구매 취소 및 최근 활동 내역 업데이트 기능.


---

👥 NotNull Team 2조

<table>
<tr>
<td align="center" width="180">
<a href="https://github.com/yoonho41">
<img src="https://github.com/yoonho41.png?size=120" width="120" height="120" alt="김윤호" />
</a><br/>
<b>PL / 김윤호</b><br/>
<sub>PM / Full-stack</sub><br/>
<a href="https://github.com/yoonho41">@yoonho41</a>
</td>

<td align="center" width="180">
<a href="https://github.com/hj626">
<img src="https://github.com/hj626.png?size=120" width="120" height="120" alt="강혜정" />
</a><br/>
<b>강혜정</b><br/>
<sub>Full-stack</sub><br/>
<a href="https://github.com/hj626">@hj626</a>
</td>


<td align="center" width="180">
<a href="https://github.com/soyeongjang">
<img src="https://github.com/soyeongjang.png?size=120" width="120" height="120" alt="장소영" />
</a><br/>
<b>장소영</b><br/>
<sub>Full-stack</sub><br/>
<a href="https://github.com/soyeongjang">@soyeongjang</a>
</td>

<td align="center" width="180">
<a href="https://github.com/JIWoen-code">
<img src="https://github.com/JIWoen-code.png?size=120" width="120" height="120" alt="박지원" />
</a><br/>
<b>박지원</b><br/>
<sub>Full-stack</sub><br/>
<a href="https://github.com/JIWoen-code">@JIWoen-code</a>
</td>
</tr>
