---
layout: default
title: Basic Information
nav_order: 11
parent: Basic(Godot4)
grand_parent: Godot
---

# Basic Information
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

## STEP 1. Node and Scene

### Step 1-1. Node and Scene

* **Node**
  * [노드](Node)란, 게임을 구성하는 부품
  * 고도엔진에는 그래픽을 표시하는 [노드], 소리를 재생하는 [노드], 물리 연산을 적용하는 [노드]등 여러가지 종류의 [노드]들이 존재하며 우리는 다양한 [노드]들을 적절하게 조립하면서 게임을 개발하게 된다. [노드]를 조립하는 것에 정답은 없으며 어떤 구조로 어떤 배치로 [노드]를 조립할지는 개발자 스스로가 정하는 것이다.

* **Scene**
  * [씬](Scene)이란, 하나 이상의 [노드]들의 정보를 배치 구조와 함께 저장한 것이다. 씬 독의 이름이 ‘씬 독’인 이유도 현재 열린 [씬]에 포함된 노드들을 보여주는 영역이기 때문에 ‘씬 독’인 것이다. 

### Step 1-2. Node 종류

* **Sprite2D** : 자신의 texture속성에 할당된 그래픽을 2D 스크린에 표시해주는 역할을 가진 [노드]

<br>

## STEP 2. Layer and Mask
* Reference Site
  * [dc](https://gall.dcinside.com/mgallery/board/view/?id=game_dev&no=147018&s_type=search_subject_memo&s_keyword=.EA.B3.A0.EB.8F.844&page=1)

### Step 2-1. Layer and Mask

* Layer : 이 물리 노드가 어떤 레이어에 해당하는지를 나타낸다.
* Mask : 이 물리 노드가 어떤 레이어를 감지해야 하는지를 나타낸다.

### Step 2-2. Layer Names Setting

* Project → Project Settings → Layer Names → 2D Physics
