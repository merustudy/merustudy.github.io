---
layout: default
title: TextRPG
nav_order: 22
parent: Basic(Unity)
grand_parent: Unity
---
# TextRPG

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

## STEP. Text RPG

* c# : namespace만 똑같으면 class 파일의 class를 별도의 명령어 없이 사용 가능

* `Player.cs`(새로 생성된 클래스 파일)

```c#
public enm Playertype	// 구분자: 클래스 구분해도 본인 타입은 내부에 갖고 있는게 좋음
{
    None = 0,
    Knight = 1,
    Archer = 2,
    Mage = 3
}

class Player
{
    // 주요 필드들 protected로 생성
    protected PlayerType _type;
    protected int hp;            
    protected int attack;

    // new Player에 타입을 받음으로써 우리가 지정한 Knight, Archer, Mage 외 생성 가능한 경우를 방지하기 위함
    // 또한 protected로 지정하므로써 외부에서 사용 못하게 방지
    protected Player(PlayerType type)
    {
        this.type = type;
    }

    public void SetInfo(int hp, int attack)
    {
        this.hp = hp;
        this.attack = attack;
    }

    // protected 필드의 정보를 외부에서 알기 위한 함수
    pubilc int GetHp() { return hp; }	
    public int GetAttack() { return attack; }
}   

class Knight : Player
{
    public Knight() : base(PlayerType.Knight)	// 생성자
    {
    }
}

class Archer : Player
{
    public Archer() : base(PlayerType.Archer)	// 생성자
    {
    }
}

class Mage : Player
{
    public Mage() : base(PlayerType.Mage)	// 생성자
    {
    }
}
```

