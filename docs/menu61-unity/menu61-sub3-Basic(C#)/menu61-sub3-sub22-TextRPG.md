---
layout: default
title: TextRPG
nav_order: 22
parent: Basic(C#))
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

* c# : namespace만 똑같으면 class 파일의 class를 별도의 명령어 없이 사용 가능.

* 게임 모드로 관리(유용함) 
    * 설계 디자인 패턴 중 state 패턴과 비슷

* `Creature.cs`

```c#
public enum CreatureTpye
{
    None,
    Player = 1,
    Monster = 2
}

class Creature
{
    CreatureType type;
    // 주요 필드들 protected로 생성
    protected int hp = 0;
    protected int attack = 0;

    protected Creature(CreatureType type) // 생성자(외부 직접 접근 방지를 위해 protected)
    {
        this.type = type;
    }

    public void SetInfo(int hp, int attack)
    {
        this.hp = hp;
        this.attack = attack;
    }

    public int GetHp() { return hp; }	
    public int GetAttack() { return attack; }

    public bool IsDead() { return hp <= 0;}

    public void OnDamaged(int damage)
    {
        hp -= damage;
        if(hp <0)
            hp = 0;
    }
}
```

<br>

* `Player.cs`(새로 생성된 클래스 파일)

```c#
public enm Playertype	// 구분자: 클래스 구분해도 본인 타입은 내부에 갖고 있는게 좋음
{
    None = 0,
    Knight = 1,
    Archer = 2,
    Mage = 3
}

class Player : Creature
{
    protected PlayerType type = PlayerType.None;

    // new Player에 타입을 받음으로써 우리가 지정한 Knight, Archer, Mage 외 생성 가능한 경우를 방지하기 위함
    // 또한 protected로 지정하므로써 외부에서 사용 못하게 방지
    protected Player(PlayerType type) : base(CreatureType.Player)
    {
        this.type = type;
    }

    public PlayerTpye GetPlayerType() { return type; }
}   

class Knight : Player
{
    public Knight() : base(PlayerType.Knight)	// 생성자
    {
        SetInfo(100, 10);
    }
}

class Archer : Player
{
    public Archer() : base(PlayerType.Archer)	// 생성자
    {
        SetInfo(75, 12);
    }
}

class Mage : Player
{
    public Mage() : base(PlayerType.Mage)	// 생성자
    {
        SetInfo(50, 15);
    }
}
```

<br>

* `Monster.cs`

```c#
public enum Monster
{
    None = 0,
    Slime = 1,
    Orc = 2,
    Skeleton = 3
}

class Monster : Creature
{
    protected MonsterType type;

    protected Monster(MonsterType type) : base(CreatureType.Monster)
    {
        this.type = type;
    }

    public MonsterType GetMonsterType() { return type; }
}

class Slime : Monster
{
    public Slime() : base(MonsterType.Slime)
    {
        SetInfo(10, 10);
    }
}

class Orc : Monster
{
    public Orc() : base(MonsterType.Orc)
    {
        SetInfo(20, 20);
    }
}

class Skeleton : Monster
{
    public Skeleton() : base(MonsterType.Skeleton)
    {
        SetInfo(15, 25);
    }
}
```

<br>

* `Game.cs`

```c#
public enum GameMode
{
    None,
    Lobby,
    Town,
    Field
}

class Game
{
    private GameMode mode = GameMode.Looby;
    private Player player = null;
    private Monster monster = null;
    private Random rand = new Random();

    public void Process()
    {
        switch (mode)
        {
            case GameMode.Looby:
                ProcessLobby();
                break;
            case GameMode.Town:
                ProcessTown();
                break;
            case GameMode.Field:
                ProcessField();
                break;
        }
    }

    private void ProcessLobby()
    {
        Console.WriteLine("직업 선택");
        Console.WriteLine("[1] Knight");
        Console.WriteLine("[2] Archer");
        Console.WriteLine("[3] Mage]");

        string input = Console.ReadLine();

        switch (input)
        {
            case "1":
                player = new Knight();
                mode = GameMode.Town;
                break;
            case "2":
                player = new Archer();
                mode = GameMode.Town;
                break;
            case "3":
                player = new Mage();
                mode = GameMode.Town;
                break;
        }
    }

    private void ProcessTown()
    {
        Console.WriteLine("마을 입장");
        Console.WriteLine("[1] 필드 가기");
        Console.WriteLine("[2] 로비 돌아가기")

        string input = Console.ReadLine();

        switch (input)
        {
            case "1":
                mode = GameMode.Field;
                break;
            case "2":
                mode = GameMode.Lobby;
                break;
        }
    }

    private void ProcessField()
    {
        Console.WriteLine("필드 입장");
        Console.WriteLine("[1] 싸우기");
        Console.WriteLine("[2] 일정 확률로 마을 돌아가기")
   
        CreateRandomMonster();

        string input = Console.ReadLine();

        switch (input)
        {
            case "1":
                ProcessFight();
                break;
            case "2":
                TryEscape();
                break;
        }

    }

    private void CreateRandomMonster()
    {
        int randValue = rand.Next(0, 3);

        switch (randValue)
        {
            case 0:
                monster = new Slime();
                Console.WriteLine("Slime 생성");
                break;
            case 1:
                monster = new orc();
                Console.WriteLine("Orc 생성");
                break;
            case 2:
                monster = new Skeleton();
                Console.WriteLine("Skeleton 생성");
                break;
        }
    }

    private void ProcessFight()
    {
        while (true)
        {
            int damage = player.GetAttack();
            monster.OnDamaged(damage);
            if (monster.IsDead())
            {
                Console.WirteLine("승리");
                Console.WirteLine($"남은 hp {player.GetHp()}");
                break;
            }

            damage = monster.GetAttack();
            player.OnDamaged(damage);
            if (player.IsDaed())
            {
                Console.WirteLine("패배");
                mode = GameMode.Lobby;
                break;
            }
        }
    }

    private void TryEscape();
    {
        int randValue = rand.Next(0, 100);
        if (randValue < 33)
        {
            mode = GameMode.Town;
        }
        else
        {
            ProcessFight();
        }
    }
}
```

<br>

* `Program.cs`(Main)

```c#
class Program
{
    static void Main(string[] args)
    {
        Game game = new Game();

        while (true)
        {
            game.Process();
        }
    }
}
```