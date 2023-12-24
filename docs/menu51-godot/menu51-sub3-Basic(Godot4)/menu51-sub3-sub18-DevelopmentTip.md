---
layout: default
title:  Development Tip
nav_order: 18
parent: Basic(Godot4)
grand_parent: Godot
---

# Development Tip
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


## STEP 2. 개발

### Step 2-1. 파일 경로 이동 및 삭제

* [파일 삭제 혹은 경로은 파일독 내에서 수행](https://gall.dcinside.com/mgallery/board/view/?id=game_dev&no=145318&s_type=search_subject_memo&s_keyword=.EA.B3.A0.EB.8F.844&page=1)
  * **주의사항** : 프로젝트 폴더에 들어있는 파일을 삭제하거나 그 경로를 바꾸는 작업(새로운 폴더를 만들어서 그 곳에 집어 넣는 등)은 에디터 밖에서 하면 안되고 반드시 이 [파일 시스템 독]에서 수행해야만 한다. 게임의 다른 요소들이 어떤 파일을 이용할 때는 그 파일의 경로를 참조하는데, 경로가 바뀌면 파일을 불러오지 못해 프로젝트가 고장나 열리지 않게 될 수도 있다. 하지만 [파일 시스템 독]에서 경로를 바꿀 때는 그렇게 망가지지 않도록 고도엔진이 자동으로 프로젝트를 수정해준다. 따라서 파일의 삭제나 경로의 수정은 반드시 에디터를 켜서 [파일 시스템 독]에서만 해야 한다