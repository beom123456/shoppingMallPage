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

-로그인 실패

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

![image](https://github.com/beom123456/shoppingMallProject/assets/169109573/4af89361-6716-4141-b629-31cd4f9d4e9c)

---

**상품 관리**
- 등록한 상품 관리
  
- 초기 화면에 컨트롤러에서 첫번째 인덱스 부터 3개 내용 나오게 설정
  
- 2페이지로 이동 하면 두 번째 페이지 내용 3개가 나오도록 설정
  
- 등록자, 등록시간은 Audit으로 만든 createdBy, regTime 으로 설정
  
![image](https://github.com/beom123456/shoppingMallProject/assets/169109573/f6b70fd0-866d-4cfa-96fe-20f3b74f91da)

---


**상품 관리(검색)**

- Q클래스를 활용하여 쿼리문 생성

- 날짜 설정

![image](https://github.com/beom123456/shoppingMallProject/assets/169109573/a96d7439-8623-425c-a71e-4828cf37b0db)

- 판매 상태 여부

![image](https://github.com/beom123456/shoppingMallProject/assets/169109573/9ee6ebd2-673d-4579-9c9c-0c44d4c47b01)

- 상품명으로 검색

![image](https://github.com/beom123456/shoppingMallProject/assets/169109573/d8aa2fa8-362a-409f-bdbe-4a6a9ae1bfe6)

- 등록자 이름으로 검색 

![image](https://github.com/beom123456/shoppingMallProject/assets/169109573/2decabd9-7ae8-488c-8b1c-30f776e2b56f)



**상품 수정 삭제**

- 상품 삭제시 상품에 대한 리뷰, 이미지 모두 삭제

![image](https://github.com/beom123456/Mall/assets/169109573/a63fcb28-d846-4427-b81e-7f08f99d8328)

---

### 5. 리뷰 

- 내용, 별점, 2개의 이미지 작성 가능.

![image](https://github.com/beom123456/Mall/assets/169109573/d9908ec6-36ff-4e4b-94cd-3963325f101d)

---

**리뷰 수정 삭제**

**수정 전**

![image](https://github.com/beom123456/Mall/assets/169109573/73843f67-63f1-4d7f-9b75-aaeb745b1469)

---

**수정 후**

![image](https://github.com/beom123456/Mall/assets/169109573/c2813776-9511-4891-aceb-dfd577d3fa80)

---

**삭제**

![image](https://github.com/beom123456/Mall/assets/169109573/b880f31f-cddc-4e09-9846-84f883581b26)

---

### 5. 장바구니

- 수량을 늘리면 늘린만큼 가격이 올라감

- 늘린 수량 만큼 장바구니 페이지로 이동 

![image](https://github.com/beom123456/Mall/assets/169109573/5ad86958-43f2-4172-9fe9-edcb7974ebd0)

---

**장바구니 페이지**

- 상품을 선택하면 선택된 상품의 개수 만큼 가격이 올라옴

![image](https://github.com/beom123456/Mall/assets/169109573/898ed5b8-2628-4129-bec8-64c1204c3ca6)

---

### 6. 주문하기

- 상품 설명, 장바구니 창에서 주문 가능.

 ![image](https://github.com/beom123456/Mall/assets/169109573/ce3fa8a6-0405-4a7c-a034-8cd0516b394a)

 ![image](https://github.com/beom123456/Mall/assets/169109573/fd33c247-8aa2-4c15-9178-436d5d247599)

 ---

 - 주문 취소

 ![image](https://github.com/beom123456/Mall/assets/169109573/78dd4330-066c-4c2a-a1b7-09b5527bea6a)


## 📄 라이선스

이 프로젝트는 MIT 라이선스 하에 라이선스됩니다. 자세한 내용은 [LICENSE](LICENSE) 파일을 참조하세요.

## 📧 연락처

- **작성자:** 박진범
- **이메일:** winter038@naver.com
- **연락처:** 010-2245-6759
