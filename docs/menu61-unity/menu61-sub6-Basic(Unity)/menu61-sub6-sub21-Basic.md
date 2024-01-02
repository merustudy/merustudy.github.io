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
        * Sprite : 실제 영화 씬(살아 움직이는 것)
            * 맵 
            * 움직임이 있는 경우 UI 보다 성능 좋음
        * UI : 영화 찍은 후 CG(버튼 등), 화면에 따른 비율 처리가 Sprite에 비해 쉬움
    * 정답은 없음

### Step 1-2. 폴더 관리

* Assets
    * @Resources
        * Data, Font, Sounds
        * Prefabs
            * Creature, Map
        * Creatures
            * Sprites 안에 관리할지? Animations 따로 관리할지? 아니면 Creature와 같이 관리할지 고민(케바케)
            * 여기서는 별도의 Creature 상위 폴더에 각기 하위 폴더를 만들어 이미지, animation 파일을 같이 모아서 관리
            * Goblin_01, Slime_01, Snake_01, ...
        * Sprites 
            * Item, Map, ...
            * UI
                * Joystick
    * @Scripts
        * Contents, Managers, Ui, Utils
        * Scenes
            * Game
        * Controllers
            * PlayerController
    * @Scenes
        * GameScene

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


### Step 1-6. Prefab 코드로 인게임 배치

* 인게임 object 뿐만 아니라 prefab 파일도 직접 연결 가능

* `GameScene.cs`

```c#
public class GameScene : MonoBehaviour 
{
   public GameObject _goblinPrefab; // Prefab을 메모리에 들고 있는 것을 의미(배치 X), 일단 드레그엔드롭으로 연결
   public GameObject _SlimePrefab; 

   GameObject  _goblin;
   void Start()
   {
        _goblin = GameObject.Instantiate(_goblinPrefab); // 인게임 배치 
        _slime = GameObject.Instantiate(_slimePrefab);

        // 상위 오브젝트 만들어서 그 아래로 배치
        GameObject go = new GameObject() { name = "@Monsters" };
        _goblin.transform.parent = go.transform;

        // 오브젝트 이름 변경
        _goblin.name = _goblinPrefab.name;
        _slime.name = _slimePrefab.name;

        // 컴포넌트 붙이기
        _slime.AddComponent<PlayerContorller>();

        // 카메라 타겟 설정
        Camera.main.GetComponent<CameraController>().Target = _slime;
   }
}
```


* preFab 코드로 인게임 배치된 오브젝트 연결하기
    * 코드로 생성되기 때문에 드래그드롭 안됨

* `CameraController.cs`

```c#
public class CameraController : MonoBehaviour 
{
    public GameObject Target;

    void Start()
    {
        // (X) Target = GameObject.Fine("Slime_01");    // Life Cycle 때문에 동작 안됨(CameraContorller Start() 된 후 Slime_01 오브젝트 생성되기 때문)
        // Life Cycle을 모두 파악하는 것은 어렵기 때문에 위 방식은 안씀
        
        // GameSecen에서 prefab 오브젝트 생성하기 때문에 GameSecne에서 Target 추가
    }

    void LateUpdate()   // 카메라는 떨림현상(Update 순위 구분 때문에 발생) 방지를 위해 LateUpdate 사용
    {
        if (Target == null)
            return;

        transform.position = new Vector3(Target.transform.position.x, Target.transform.position.y, -10);
    }
}
```

<br>