---
layout: default
title: Basic
nav_order: 21
parent: Basic(Unity)
grand_parent: Unity
---

# Basic

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

## STEP 1. 기본 지식
### Step 1-1. 개요
* 빈 GameObject에 여러 Component를 조립하여 제작
* script파일을 파일명과 class 명이 같아야

* 어떤 기능을 Srpite로 만들 것인가 UI로 만들 것인가 
    * Sprite와 UI 차이
        * Sprite : 실제 영화 씬
        * UI : 영화 찍은 후 CG

### Step 1-2. 폴더 관리

* Assets
    * @Resources
        * Data, Font, Sounds
        * Prefabs
            * Creature
        * Creatures
            * Sprites 안에 관리할지? Animations 따로 관리할지? 아니면 Creature와 같이 관리할지 고민(케바케)
            * 여기서는 별도의 Creature 상위 폴더에 각기 하위 폴더를 만들어 이미지, animation 파일을 같이 모아서 관리
            * Goblin_01, Slime_01, Snake_01, ...
        * Sprites 
            * Item, Map, ...
            * UI
                * Joystick
    * @Scripts
    * @Scenes
        * Contents, Controllers, Managers, Ui, Utils

### Step 1-3. GameObject와 Component 연결

* `transform`, `gameObject`는 변수명으로 사용하지 않아야 함

```c#
//(참고) MonoBehaviour : Component를 상속 받음
public class Test : MonoBehaviour 
{
    void Start()
    {
        // gameObject 연결
        gameObject  

        // Transform 연결
        gameObject.GetComponent<Transform>();
        GetComponent<Transform>();  // gameObject 생략형
        transform;                  // 축약형
    }
}
```

### Step 1-4. 다른 GameObject와 연결

* 되도록 Component 타입으로 관리(가독성)

```c#
//(참고) MonoBehaviour : Component를 상속 받음
public class Test : MonoBehaviour 
{
    public _hp;
    [SerializedField]
    int _damage;

    [SerializedField]
    Player _player;
    // GameObject _player;
    // Transform _player;

    void Start()
    {
       _player.transform; 
       _player.gameObject;
    }
}
```


### Step 1-5. 유니티 상속

* `Createure.cs`

```c#
public class Creature : MonoBehaviour
{
    public int hp;

    List<Creature> creatures = new List<Creature>();
    ...
}
```

* `Player.cs`

```c#
// Monobehaviour을 상속받은 Creature을 상속받아 Component로 사용 가능
public class Player : Creature 
{
    ...
}
```
