# 🛒 MyShop - 온라인 쇼핑몰

![image](https://github.com/beom123456/shoppingMallPage/assets/169109573/5a5bed7a-66fb-4a90-9144-d86af21f1a3a)

## 🚀 프로젝트 개요

MyShop은 사용자가 제품을 검색하고, 장바구니에 추가하며, 구매할 수 있는 전자상거래 플랫폼입니다. 또한 사용자 등록, 로그인 및 주문 추적 기능을 포함하고 있습니다.

## ✨ 주요 기능

- 사용자 인증 및 권한 부여
- 상품 등록, 수정
- 카테고리 및 필터가 있는 제품 목록
- 장바구니 기능
- 주문 관리
- 다양한 필터가 있는 검색 기능
- 제품 및 주문 관리를 위한 관리자 패널

## 🛠️ 기술 스택

- **프론트엔드:** HTML, CSS, JavaScript, Thymeleaf
- **백엔드:** Spring Boot, JAVA 
- **데이터베이스:** mariaDB
- **버전 관리:** Git & GitHub
- **빌드 도구:** gradle

### 사전 요구 사항

- Java 17 이상
- gradle
- mariaDB 10.5

### 앤티티 관계도 

![image](https://github.com/beom123456/shoppingMallPage/assets/169109573/38a41ec8-1da0-4642-8975-f938c4ac4741)

## 📖 사용법

### 1. 사용자 등록

**회원가입 페이지**

 - 회원가입 정보를 입력
  
 - DB에 가입정보 저장 후 로그인 페이지로 이동.
   
![image](https://github.com/beom123456/shoppingMallPage/assets/169109573/023e42c3-8fd8-4ce9-b055-a09010da7e7d)


---

### 2. 로그인

**로그인 페이지**

**Security config**

- 로그인 성공, 실패 시 페이지 이동 

- 권한별 페이지 접근 설정
   
![image](https://github.com/beom123456/shoppingMallPage/assets/169109573/459bc77c-573a-4eb8-9af0-12532b64be62)

---

- 로그인 실패

![image](https://github.com/beom123456/shoppingMallPage/assets/169109573/72923fd4-d804-4ee5-ab4b-6b105a1c50fd)


**관리자로 로그인 요청**

- 관리자로 접근하지 않았을 때 "/member/login/accessDenied" 로 redirect
   
---

### 4. 상품 등록

**상품 등록 페이지**

- 상품 등록 정보 입력

- 등록 내용과 이미지를 서버로 보냄.
  
![image](https://github.com/beom123456/shoppingMallPage/assets/169109573/5ee674db-3f79-42bf-afa4-9be886f21f6e)



**이미지 요청 처리**

- 이미지에 대한 요청이 오면 uploadPath로 처리.

- uploadPath는 `file:///C:/mall/` 

---

**상품 설명**

- 상품 등록 시 입력 했던 정보로 표시
 
- 첫번 째로 올린 이미지를 대표이미지로 설정
  
- 대표 이미지만 상품 설명 상단에 나오게 함
  
 ![image](https://github.com/beom123456/shoppingMallPage/assets/169109573/b465a20a-6da6-4b21-b707-aa6500616243)

---

- 대표 이미지로 설정한 이미지와 상품에 간략한 설명이 매인화면에 나오도록 설정

![image](https://github.com/beom123456/shoppingMallPage/assets/169109573/ae6af144-2654-4d45-8c8f-2b047bf76813)

---

**상품 관리**
- 등록한 상품 관리
  
- 초기 화면에 컨트롤러에서 첫번째 인덱스 부터 3개 내용 나오게 설정
  
- 2페이지로 이동 하면 두 번째 페이지 내용 3개가 나오도록 설정
  
- 등록자, 등록시간은 Audit으로 만든 createdBy, regTime 으로 설정
  
![image](https://github.com/beom123456/shoppingMallPage/assets/169109573/b355d369-d78c-4ed0-9eda-e57b01e1a876)

---


**상품 관리(검색)**

- Q클래스를 활용하여 쿼리문 생성

- 날짜 설정

![image](https://github.com/beom123456/shoppingMallPage/assets/169109573/88fa3b54-c2cb-42b3-91c1-b207fb5588ba)

- 판매 상태 여부

![image](https://github.com/beom123456/shoppingMallPage/assets/169109573/8aa5af5a-3283-4599-91be-49169293d440)

- 상품명으로 검색

![image](https://github.com/beom123456/shoppingMallPage/assets/169109573/c12448a8-76fe-47b2-8f2a-f00400ba2e13)


- 등록자 이름으로 검색 

![image](https://github.com/beom123456/shoppingMallPage/assets/169109573/f7da751f-db5e-4d29-934b-3ee2b973b51a)



**상품 수정 삭제**

- 상품 삭제시 상품에 대한 리뷰, 이미지 모두 삭제

![image](https://github.com/beom123456/shoppingMallPage/assets/169109573/6e219daf-2c1c-4c0f-b28e-eb2b7ab3757d)

---

### 5. 리뷰 

- 내용, 별점, 2개의 이미지 작성 가능.

![image](https://github.com/beom123456/shoppingMallPage/assets/169109573/8cea360f-971b-473b-9011-b9dda42eb4ba)

---

**리뷰 수정 삭제**

**수정 전**

![image](https://github.com/beom123456/shoppingMallPage/assets/169109573/7649c67e-45b4-443f-8c6d-5412b06da342)

---

**수정 후**

![image](https://github.com/beom123456/shoppingMallPage/assets/169109573/77d2a414-e9cd-498f-b332-7540380ed1cc)


---

**삭제**

![image](https://github.com/beom123456/shoppingMallPage/assets/169109573/a21ee23f-50e0-4d89-9713-ae9a83cfb72b)

---

### 5. 장바구니

- 수량을 늘리면 늘린만큼 가격이 올라감

- 늘린 수량 만큼 장바구니 페이지로 이동 

![image](https://github.com/beom123456/shoppingMallPage/assets/169109573/b571491f-e9ea-400c-9a12-013859263083)

---

**장바구니 페이지**

- 상품을 선택하면 선택된 상품의 개수 만큼 가격이 올라옴

![image](https://github.com/beom123456/shoppingMallPage/assets/169109573/7380ef5b-bc70-406f-ae13-ae2a15f44061)

![image](https://github.com/beom123456/shoppingMallPage/assets/169109573/46dec766-c511-4ec0-8fd3-c8dd692af2fc)

---

### 6. 주문하기

- 상품 설명, 장바구니 창에서 주문 가능.

- 주문 취소기능

![image](https://github.com/beom123456/shoppingMallPage/assets/169109573/64f5b56b-dc1a-4064-8d3a-28f6a58c4e05)

 ---

  ### 어려웠던 점


1. 동적인 페이지 구동

   장바구니 수량을 추가하거나 전체선택을 할 때마다 페이지가 동적으로 변해야 했습니다.
   이를 위해 JavaScript와 Ajax를 사용하여 사용자 경험을 향상시키는 데 많은 노력이 필요했습니다.

   
2. 데이터베이스 참조키 관리

  데이터베이스에서 참조키를 관리하는 것은 복잡했습니다. 특히, 삭제 또는 수정 시 참조 무결성을 유지하는 것이 중요했습니다.
  이를 위해 JPA를 활용하여 엔티티 간의 관계를 적절히 설정하고 관리해야 했습니다.
  장바구니 및 주문 처리 로직



이러한 문제들을 해결하기 위해 많은 단계를 거쳤습니다. MyShop 프로젝트에 대한 관심과 참여에 감사드립니다!


## 📄 라이선스

이 프로젝트는 MIT 라이선스 하에 라이선스됩니다. 자세한 내용은 [LICENSE](LICENSE) 파일을 참조하세요.

## 📧 연락처

- **작성자:** 박진범
- **이메일:** winter038@naver.com
- **연락처:** 010-2245-6759
