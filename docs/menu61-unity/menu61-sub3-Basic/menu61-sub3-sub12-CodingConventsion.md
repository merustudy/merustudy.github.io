---
layout: default
title: Coding Convention
nav_order: 12
parent: Basic(Unity)
grand_parent: Unity
---

# Coding Convention
{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>
<!------------------------------------ STEP ------------------------------------>

```C#
```

## STEP 1. Coding Convention

* 변수 하드코딩 데이터 관리방법
  * 대부분 데이터 파일로 따로 관리 or 맨 위에서 지정
  * 내용 중에 하드코딩 하지 않음

* 컨벤션
    * 클래스 내부에서만 사용 변수 : _
    * 멤버 변수(클래스 내부에서 선언되는 변수) : m_
        * 인스턴스 변수
        * 클래스변수(static)

* **시그널 이벤트는 모두 밑으로**


```c#
// 모두 대문자 변수: 변하지 않는 변수(상수)
const int GAME_SPEED = 3;

// 참조형 변수는 new를 통해 생성
int[] scores = new int[5] { 10, 20, 30, 40, 50 };   // 추천(new를 통해 참조 할당이라는 것을 인식 가능)
```
