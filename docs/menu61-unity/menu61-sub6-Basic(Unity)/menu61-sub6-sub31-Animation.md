---
layout: default
title: Animation
nav_order: 31
parent: Basic(Unity)
grand_parent: Unity
---

# Animation

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

## STEP 1. 본에니메이션



### Step 1-1. IK Manager
* Reference: [How to animate your Photoshop characters in Unity](https://www.youtube.com/watch?v=vLDK0eHwsho)
1. Prefab Object에 IK Manager 추가
2. LIMB 추가
3. 영향 주고하는 최상위(ex.어께) 본 하위에 빈 오브젝트 생성
4. 빈 오브젝트를 영향력 하단(ex. 손 끝) 까지 이동
5. Solver에서 빈 오브젝트 선택 입력
6. Solver 타겟 생성
7. 움직임 확인 후 필요시 flip 체크

### Step 1-2. Spirte Library 
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

### Step 1-3. 위 케릭터 정렬 방법 
* [정렬 그룹](https://docs.unity3d.com/kr/2017.4/Manual/SortingGroup.html)
    * [Transparency Sort Mode에서 소팅 이상해지는 어케해야할까](https://gall.dcinside.com/mgallery/board/view/?id=game_dev&no=32436&page=1)


<br>

## STEP. ETC

### Unity Animation

* [2DAnimation! 본 애니메이션!](https://www.youtube.com/watch?v=BSYwMXcQ2ak)

* [쉽고 빠른 애니메이션 제작을 위한 2D Animation 패키지 기능 완전 정복!](https://www.youtube.com/watch?v=b3J2SInvuwM&list=PL412Ym60h6uvqYiCVKk5NiEFpDEwOMQFX&index=55)

* [유니티 2D 애니메이션 1 - PSB파일](https://boxwitch.tistory.com/entry/%EC%9C%A0%EB%8B%88%ED%8B%B0-2D%EC%95%A0%EB%8B%88%EB%A9%94%EC%9D%B4%EC%85%98-PSB%ED%8C%8C%EC%9D%BC)
* [How to reuse Animation Clip for other characters in Unity](https://www.youtube.com/watch?v=6mNak-mQZpc)

* [How to animate your Photoshop characters in Unity](https://www.youtube.com/watch?v=vLDK0eHwsho)

* [Unity 스프라이트 교환 기능](https://www.youtube.com/watch?v=wBGykdKd80w)

* [Unity 2D Rigging E1 - Build the Rig](https://www.youtube.com/watch?v=oxKstruadGc&list=PL2cNFQAw_ndxLtVGMDtbbNdWch4yIioBP&index=1)

* [Building 2D Games with Unity. Part 3: 2D Skeletal Animation](https://www.youtube.com/watch?v=eagChFn_BAE)

* [Unity 2D Animation 2020 – Skin Swapping Tutorial Part 2](https://www.youtube.com/watch?v=hoKKFQ2PWMw)

* [2D Character Customization - Full Skin Changing - Unity Tutorial](https://www.youtube.com/watch?v=ZgCB4tifQ_c&list=RDCMUCLWdeb3R2U_htIdI3RqT5YA&index=2)
  
* [Spine 2D Animation - Knight Game Character](https://www.youtube.com/watch?v=q3URlLrI1KE)
  
* [How To Make Cartoon Chest Opening Animation In Spine 2D](https://www.youtube.com/watch?v=BOqaKeKOV-8)


<br>

### ETC

* [게임 유닛(Game Unit)과 Pixels Per Unit](https://wonsorang.tistory.com/391)