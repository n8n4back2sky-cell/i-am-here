# 003_DOMAIN_MODEL.md

# Domain Model

I am Here는 사람을 중심으로 설계됩니다.

우리는 "사용자(User)"보다 "사람(Person)"을 먼저 생각합니다.

---

## Core Entities

### Person

한 명의 사람입니다.

예)

* 어머니
* 아버지
* 할머니
* 고모님

모든 정보는 Person을 중심으로 연결됩니다.

---

### Helper

Person을 돌보는 사람입니다.

예)

* 딸
* 아들
* 손녀
* 배우자
* 친구
* 요양보호사

한 Person은 여러 명의 Helper를 가질 수 있습니다.

한 Helper는 여러 Person을 돌볼 수 있습니다.

---

### Memory

기억입니다.

예)

* 일정
* 약
* 메모
* 사진
* 음성
* 질문

---

### Care Wallet

자주 사용하는 중요한 정보입니다.

예)

* 생년월일
* Medicare
* 보험
* 응급 연락처
* 주치의
* 알레르기

이 정보는 RAG가 아니라 즉시 조회됩니다.

---

### Living Memory

매일 새롭게 생성되는 기억입니다.

예)

* 오늘 기분
* 오늘 일정
* 병원 방문
* 가족 메모

---

### Legacy

오랫동안 보존할 가치가 있는 기억입니다.

예)

* 가족 이야기
* 음성 편지
* 사진
* 인생 이야기

---

### Story

실제 돌봄 현장에서 있었던 경험입니다.

Story는 새로운 기능의 출발점입니다.

No Story, No Feature.

---

# Relationships

Person

├── Care Wallet

├── Living Memory

├── Legacy

├── Stories

└── Helpers

---

# Design Principle

우리는 데이터를 저장하지 않습니다.

우리는 사람을 중심으로 연결합니다.
