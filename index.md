---
layout: default
title: Home
nav_order: 99
description: "description"
permalink: /
---

# Welcom to github.io

* [Just-the-docs 테마 적용법](https://100sang.net/292)

# TEMP

## Stable Diffusion 관련 사이트

### 셋팅
* [Stable-Diffusion WebUI Colab 무료 티어 이용방법! (colab, 무료)](https://www.youtube.com/watch?v=C8uEhp822BI)


### 학습(드립 부스)
* [초보 분들을 위한 드림 부스 셋팅 정보입니다.](https://www.clien.net/service/board/cm_aigurim/17996081)
* [Dreambooth로 특정 화가의 스타일을 학습시키기](https://www.clien.net/service/board/cm_aigurim/18000175)
* [신윤복 화백님 LoRA](https://www.clien.net/service/board/cm_aigurim/18004978)

### 기타
* [스타일 일관성 유지시켜주는 새로운 기술](https://www.clien.net/service/board/cm_aigurim/18467242?od=T31&po=2&category=0&groupCd=)
* [ChatGPT+Stable Diffusion: 프롬프트 작성 너무 쉽습니다. 미친 조합이에요!](https://www.youtube.com/watch?v=rQpaoCGpnGY)

* [Stable Diffusion 에서 지원하는 Artists 목록](https://prompts.co.kr/articles/3648?board_category=4)
* [Stable Diffusion XL artists list](https://stablediffusion.fr/artists)
* [Stable Diffusion XL artists list2](https://www.urania.ai/top-sd-artists)
<br>

## Unity

<br> 

## TODO
* (이미지 수준을 높일수 있는 팁 #2 - VAE 그리고 CLIP skip)[https://www.youtube.com/watch?v=sXpC15-K6qM]

<br>

## TEMP
* [필독) AI그림 채널 정보글 모음](https://arca.live/b/aiart/70255821?target=all&keyword=모바일+캐릭터&p=2)



### 게임성

* [매직서바이벌](https://nomoneygame.tistory.com/106)
* [오라룩스]
* [던전 스쿼드]
* [레드 브로즈]

### 디자인
* [단조의 장인]


## 유니티 ANIM
* [How to animate your Photoshop characters in Unity](https://www.youtube.com/watch?v=vLDK0eHwsho)
* [Unity 스프라이트 교환 기능](https://www.youtube.com/watch?v=wBGykdKd80w)

* [Unity 2D Rigging E1 - Build the Rig](https://www.youtube.com/watch?v=oxKstruadGc&list=PL2cNFQAw_ndxLtVGMDtbbNdWch4yIioBP&index=1)

* [Building 2D Games with Unity. Part 3: 2D Skeletal Animation](https://www.youtube.com/watch?v=eagChFn_BAE)

* [Unity 2D Animation 2020 – Skin Swapping Tutorial Part 2](https://www.youtube.com/watch?v=hoKKFQ2PWMw)

* [2D Character Customization - Full Skin Changing - Unity Tutorial](https://www.youtube.com/watch?v=ZgCB4tifQ_c&list=RDCMUCLWdeb3R2U_htIdI3RqT5YA&index=2)
  
* [Spine 2D Animation - Knight Game Character](https://www.youtube.com/watch?v=q3URlLrI1KE)
  
* [How To Make Cartoon Chest Opening Animation In Spine 2D](https://www.youtube.com/watch?v=BOqaKeKOV-8)

### Asset
* [[유니티 에셋 추천] All In 1 Sprite Shader](https://dev-junwoo.tistory.com/133)
* VFX Asset
  * [Cartoon FX Remaster Free](https://assetstore.unity.com/packages/vfx/particles/cartoon-fx-remaster-free-109565)

### VFX
* [How to make Weapon Slash Effect - Spine 2D Animation Tutorial](https://www.youtube.com/watch?v=8pKR9drPfQ0)


## 포토샵
* [#01. 포토샵에서 마법봉 100%활용하는 완전 꿀팁!! [포토샵팁]](https://www.youtube.com/watch?v=NYSofJsIYAw)
* [#03. 1초만에 이미지 부분 삭제하는 방법[포토샵팁]](https://www.youtube.com/watch?v=qN6-UAGoQgs)
    * Shift + F5
* [#04. 초간단 배경과 자연스럽게 삭제하는 방법[포토샵 팁]](https://www.youtube.com/watch?v=KCsw27MFEiA)
* [#05.간단하게 컬러보정하는 8가지 방법! [포토샵 팁]](https://www.youtube.com/watch?v=F3qVswEDG8w)
* [이미지 따는 이 방법을 알까? 초간단 3가지 방법 [예제 파일 제공]](https://www.youtube.com/watch?v=jHz1XaGPL1k)


### Step. IK Manager
* Reference: [How to animate your Photoshop characters in Unity](https://www.youtube.com/watch?v=vLDK0eHwsho)
1. Prefab Object에 IK Manager 추가
2. LIMB 추가
3. 영향 주고하는 최상위(ex.어께) 본 하위에 빈 오브젝트 생성
4. 빈 오브젝트를 영향력 하단(ex. 손 끝) 까지 이동
5. Solver에서 빈 오브젝트 선택 입력
6. Solver 타겟 생성
7. 움직임 확인 후 필요시 flip 체크

### Step. 
* Reference: [2D Character Customization - Full Skin Changing - Unity Tutorial](https://www.youtube.com/watch?v=ZgCB4tifQ_c&list=RDCMUCLWdeb3R2U_htIdI3RqT5YA&index=2)
1. (전제)기본 PSB 파일(Player1) 임포트 및 Rigging 완료
2. Prefab Object에 Sprite Library 추가
3. 프로젝트에 Create > 2D > Sprite > Sprite Library Asset 생성
4. Sprite Library Asset 기본(부모, Player) 빈 Category 만들기
5. 추가 Sprite Library Asset(Player1) 생성 후 이전 부모 Library(Player) 상속
6. 각 Category 별로 기본 PSB 파일의 Spirte 추가
7. Prefab 파일의 하위 교체할 Sprite Render를 가지고 있는 Object에 Sprite Resolver 생성(그룹 선택 후 한번에 생성가능)
8. 각 Sprite Resolver에 카테고리가 잘 선택되어 있는지 확인
9. 교체할 새로운 PSB 파일(Player2) 임포트
10. 임포트한 PSB의 Inspector 창에서 Character Rig의 Main Skeleton에서 이전에 Rigging한 Player1 Skeleton 선택
11. 임포트한 PSB의 Sprite Editor에 가서 Auto Geometry 생성 및 Apply
12. Sprite Library Asset(Player2) 생성 후 이전 부모 Library(Player) 상속
13. 각 Category 별로 새로운 PSB 파일의 Sprite 추가
14. Prefab Object의 Sprite Library에서 Player1과 Player2를 변경해가며 잘 적용되는지 확인


