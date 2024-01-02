---
layout: default
title: Convention
nav_order: 12
parent: Basic(C#)
grand_parent: Unity
---

# Convention
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

## STEP 0. 표기법
* 스네이크 케이스
  * `var snake_case;`
* 파스칼 케이스
  * `var PascalCase;`
* 카멜 케이스
  * `var camelCase;`


## STEP 1. Coding Convention

* 변수 하드코딩 데이터 관리방법
  * 대부분 데이터 파일로 따로 관리 or 맨 위에서 지정
  * 내용 중에 하드코딩 하지 않음

* 멤버 변수
  * 클래스 내부에서만 사용되는 변수 : 앞에 `_` 붙이고 카멜 케이스
  * 외부 연결 변수 : 파스칼 케이스

* **시그널 이벤트는 모두 밑으로**


```c#
// 모두 대문자 변수: 변하지 않는 변수(상수)
const int GAME_SPEED = 3;

// 참조형 변수는 new를 통해 생성
int[] scores = new int[5] { 10, 20, 30, 40, 50 };   // 추천(new를 통해 참조 할당이라는 것을 인식 가능)
```
