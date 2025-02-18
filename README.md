# 캠핑온 : 나만의 캠핑 라이프를 시작하세요!
![배너](https://github.com/user-attachments/assets/c6fcfce3-bdfa-41c4-8761-20fc76a4fa70)
## 아키텍쳐
## ERD
## 서비스 소개
> '캠핑온'은 캠핑 초보자부터 가족 캠핑 매니아까지, 다양한 캠핑 애호가들을 위한 **맞춤형 캠핑 예약 플랫폼**입니다.
> **개별 사이트에 일일이 들어가지 않고도** 캠핑온에서 **추천, 검색, 예약까지 한 번에** 해결가능합니다!

![스크린샷 2024-12-11 오후 3 10 45](https://github.com/user-attachments/assets/737362ff-60d0-442a-98d1-8f83ee6eacda)


처음 이용 시, 사용자 취향을 분석하기 위한 **키워드 선택 단계**를 통해 캠핑 스타일과 선호도를 파악하고, 그에 맞는 **캠핑장 추천**을 제공합니다. 또한, 원하시는 **검색어를 직접 입력**하여 캠핑장을 찾아볼 수도 있어, 사용자의 취향과 필요에 따라 **더욱 편리한 검색**이 가능합니다.

- **취향 분석으로 맞춤형 추천!** 사용자는 **`“별 보기 좋은”` `“아이들 놀기 좋은”` `“차대기 편한”` `“물놀이 하기 좋은”`** 등 여러 키워드 중 자신에게 맞는 항목을 선택할 수 있습니다. 선택한 키워드를 기반으로 자동 추천된 캠핑장에서 새로운 경험을 시작하세요.
- **초보 캠퍼도 안심!** 상세한 캠핑장 소개와 리뷰로 손쉽게 캠핑지를 선택하세요.
- **편리한 위치 탐색!** 직관적인 지도 기능을 통해 캠핑장 위치를 쉽게 확인하고, 주변 명소와의 거리도 한눈에 파악하여 더욱 즐거운 여행 계획을 세워보세요.

### *캠핑온과 함께 캠핑의 즐거움을 한층 더 높여보세요!*

# Links
[![Frontend Deploy Status](https://api.netlify.com/api/v1/badges/169cac93-39c4-473b-aecf-3113627195c9/deploy-status)](https://app.netlify.com/sites/celadon-arithmetic-f4288c/deploys) [![Backend Deploy Workflow Status](https://github.com/CampingOn/CampingOn-BE/actions/workflows/deploy.yml/badge.svg)](https://github.com/CampingOn/CampingOn-BE/actions/workflows/deploy.yml)
### [배포 사이트 바로가기↗︎](https://camping-on.site)
### [노션 팀페이지 바로가기↗︎](https://elice-track.notion.site/camping-on-notion?pvs=4)

# 기술 스택
- **Backend** : Spring Boot(v3.3.5), Java(v21)
- **Frontend**: React(v18.3.1), Material UI(v6.1.9), Tailwind CSS (v3.4.15), axios(v1.7.8)
- **Storage**: AWS RDS(MySQL Community v8.0.39), MongoDB(추천·검색 서비스, v8.0.3), Redis(JWT 토큰 Blacklist·Refresh Token 관리, v7.4.1), AWS S3(후기 이미지 저장)
- **Test**: JUnit(v5), Postman(API 테스트)
- **Security & Authentication**: Spring Security(v6), JWT, Google OAuth2, Let’s Encrypt(TLSv1.2, v1.3)
- **Deployment**: Netlify(Frontend), AWS EC2(Backend, Ubuntu 22.04.5), Github Actions(CI/CD), Nginx(Reverse Proxy, v1.18.0), Docker(v24.0.7)
- **DNS**: AWS Route 53
- **Build Tools**: Gradle
- **External API**: [고캠핑 공공데이터 API](https://www.data.go.kr/data/15101933/openapi.do), [Kakao 지도 API](https://apis.map.kakao.com/)
  
# 기능 소개
## 주요 기능
- 키워드 기반 추천 서비스
- 향상된 검색 서비스
- 예약 서비스

## 유저
### 회원 가입
![회원 가입](https://github.com/user-attachments/assets/f9602f1f-1df4-4a5e-96d3-df4c2f577538)
- 중복 확인을 하지 않으면 회원 가입 버튼이 활성화 되지 않음
- 이메일, 닉네임, 비밀번호 형식이 맞지 않을 경우 사용자에게 안내

### 로그인
- 일반 회원 로그인
![일반로그인](https://github.com/user-attachments/assets/58fffab4-ae9d-4cf1-8464-1d1e1ba5a5f2)
  - 처음 로그인을 한 경우 키워드 선택창으로 이동
- 구글 소셜 로그인
![구글로그인](https://github.com/user-attachments/assets/64d8d82b-fe08-4165-800c-d3d7fa474d96)


### 회원 정보 수정
- 닉네임 변경
![닉네임변경](https://github.com/user-attachments/assets/990a5c6f-938b-4386-8a6e-e75ae8c032b8)
  - 닉네임 중복확인을 하지 않으면 수정이 불가능함
- 비밀번호 변경
![비밀번호 변경](https://github.com/user-attachments/assets/b8624a4c-70eb-4f63-9eca-377ab7c567aa)
  - 비밀번호 변경 시 보안을 위해 자동 로그아웃 됨
  - 이전 비밀번호와 동일한 비밀번호는 사용할 수 없음

### 키워드 선택
![키워드변경](https://github.com/user-attachments/assets/4b8a8e5e-c2c6-492a-852c-41a5ceddebea)
  - 마이페이지에서도 키워드 변경이 가능

### 회원 탈퇴
![회원탈퇴](https://github.com/user-attachments/assets/e799d909-19fc-4b58-96a9-30517de4e553)
  - 탈퇴 사유 기록을 통한 서비스 피드백

## 검색
### 지역 선택과 자동완성
![자동완성](https://github.com/user-attachments/assets/90ea2918-a5f3-4175-aa9c-409c6305b770)
  - 지역 선택 시 지역명을 우선적으로 검색
  - 디바운스를 적용한 자동완성
    
### 연관 검색
![연관 검색](https://github.com/user-attachments/assets/3b46932b-5625-4d97-868e-fe08d040504a)
  - 키워드와 연관된 필드들을 가중값에 따라 우선순위를 매겨 검색

## 예약
### 예약 가능한 캠핑지 조회
![날짜선택2](https://github.com/user-attachments/assets/f71e9a25-0000-4859-871f-b6e4a6214393)
- 달력에서 날짜를 선택해 예약 가능한 캠핑지를 조회합니다.

![날짜선택](https://github.com/user-attachments/assets/e5b7f1d9-aa88-40bb-936b-0fad0a6bb592)
- 당일 예약과 6박 이상은 문의를 통해 예약 진행이 가능합니다.
- 예약 가능한 캠핑지 관리를 위해 날짜를 선택해야만 이후 예약 진행이 가능합니다.

### 예약 확정
![예약확정](https://github.com/user-attachments/assets/cc1feffd-2dee-4df4-ad63-a1ff8fb9efd0)
- 원하는 게스트 수를 선택합니다.
- 5명 이상부터는 초과요금 발생, 인원 수와 연박일 수에 따라 예상금액을 확인할 수 있습니다.
- 예약 확정되면 나의 예약 목록으로 이동합니다.
- 어뷰징 방지를 위해 이전 목록으로 돌아가면 예약확정 페이지가 아닌 캠핑장 상세페이지로 이동합니다.

### 나의 예약 목록
![예약목록](https://github.com/user-attachments/assets/69e35a57-a2ed-4904-9c4b-1e2ffa1a7e95)
- 이전에 예약했던 히스토리를 확인하실 수 있습니다.
- 다가오는 예약날짜가 가까운 순으로 조회됩니다.

### 예약 취소
![예약취소](https://github.com/user-attachments/assets/4ee4a5ab-8ea3-47aa-978b-6325c85e9a46)
- 예약목록에서 취소가능한 기간이라면 취소가 가능합니다.
- 예약취소와 체크인완료는 예약날짜에 따라 자동으로 업데이트됩니다.

## 캠핑장 정보(상세페이지) ##
- **전화 걸기**
  - 캠핑장 상세 페이지에서 제공되는 전화 걸기 버튼을 통해 사용자가 캠핑장에 직접 연락하여 예약 문의 및 기타 사항을 확인할 수 있습니다.
- **사진 더보기**
  - '더보기' 버튼을 클릭하면 캠핑장과 관련된 사진이 팝업 형태로 표시되어 캠핑장 환경과 시설에 대한 시각적인 정보를 얻을 수 있습니다.
- **지도**
  - 캠핑장의 위치를 지도에 표시하여 사용자가 경로를 쉽게 확인하고 방문 계획을 세울 수 있도록 지원합니다.

## 캠핑장 정보(상세페이지) ##
- **전화 걸기**
  - 캠핑장 상세 페이지에서 제공되는 전화 걸기 버튼을 통해 사용자가 캠핑장에 직접 연락하여 예약 문의 및 기타 사항을 확인할 수 있습니다.
- **사진 더보기**
  - '더보기' 버튼을 클릭하면 캠핑장과 관련된 사진이 팝업 형태로 표시되어 캠핑장 환경과 시설에 대한 시각적인 정보를 얻을 수 있습니다.
- **지도**
  - 캠핑장의 위치를 지도에 표시하여 사용자가 경로를 쉽게 확인하고 방문 계획을 세울 수 있도록 지원합니다.

## 리뷰 ##
- **예약 후기 작성**
  - 사용자는 '나의 예약페이지'에서 본인이 이용한 캠핑장에 대한 후기를 작성할 수 있습니다. 이를 통해 다른 사용자에게 유용한 정보를 제공할 수 있습니다.
- **예약 후기 확인**
  - 사용자는 '나의 예약페이지'에서 자신이 작성한 후기를 다시 확인하거나 수정할 수 있습니다.
- **캠핑장별 후기 확인**
  - 캠핑장 상세 페이지에서 해당 캠핑장을 이용한 사용자들의 후기를 확인할 수 있어 선택에 참고할 수 있습니다.

## 찜
![bookmark1](https://github.com/user-attachments/assets/32a64eb9-3c1a-4a56-87e4-c235080ed2c1)
- 원하는 캠핑장 찜클릭
- 찜한 캠핑장 목록에서 찜한 캠핑장 조회

# 아키텍처
![아키텍처 다이어그램](https://github.com/user-attachments/assets/02a5b73b-b856-4df7-992d-7d1024193400)


# ERD
![ERD v241213](https://github.com/user-attachments/assets/72959991-0f7f-417a-9d11-73ad5ae44039)


# 배포 환경
```
- 서버: AWS EC2 (Ubuntu 22.04.5 LTS, GNU/Linux 6.8.0-1019-aws x86_64)
	- 애플리케이션 서버:
		- Spring Boot (내장 서버 사용)
		- Docker 컨테이너 환경 (멀티 스테이지 빌드)
		- Java Runtime: openjdk version “21.0.4”
- 리버스 프록시:
	- Nginx (v1.18.0) - EC2 인스턴스에 직접 설치 (TSLv1.2, TSLv1.3 지원)
- 데이터베이스:
	- AWS RDS: MySQL Community (8.0.39)
	- MongoDB: 특정 데이터 저장 용도 (검색 및 추천)
	- Redis: Docker 컨테이너로 관리
- 파일 저장소: AWS S3 (이미지 파일 저장 용도)
- 도메인 및 DNS:
	- 가비아에서 구매한 도메인 camping-on.site, AWS Route 53으로 관리
	- EC2 인스턴스의 퍼블릭 IP에 도메인 연결
	- HTTPS 통신 (Let’s Encrypt SSL/TSL 인증서 사용, auto-renewal 활성화)
```


# Docs
### [📄 API 문서 ↗︎](https://elice-track.notion.site/camping-on-api-docs?pvs=4)
### [🎯 트러블 슈팅 ↗︎](https://elice-track.notion.site/camping-on-trouble-shooting?v=0ca8756809124d7cb88d4ca112bdabd4&pvs=4)

# 팀원 소개

<div align="center">
  
|[윤지현](https://github.com/jhYun505)|[고범석](https://github.com/kobumseouk)|[박유찬](https://github.com/ParkYuChan03)|[이은주](https://github.com/silverzoo)|[이찬진](https://github.com/chanjin23)
|:---:|:---:|:---:|:---:|:---:|
|<img src="https://avatars.githubusercontent.com/u/81208791?v=4" width="120">|<img src="https://avatars.githubusercontent.com/u/73152527?v=4" width="120">|<img src="https://avatars.githubusercontent.com/u/173863179?v=4" width="120">|<img src="https://avatars.githubusercontent.com/u/27897137?v=4" width="120">|<img src="https://avatars.githubusercontent.com/u/160113940?v=4" width="120">|
|팀장|팀원|팀원|팀원|팀원|
