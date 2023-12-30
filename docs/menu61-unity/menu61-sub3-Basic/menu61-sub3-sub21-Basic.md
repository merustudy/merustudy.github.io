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

```C#
```

## STEP 1. 기본 지식
### Step 1-1. 개요

* 게임의 구분
    * 게임 데이터(게임 구현 리소스 등) : 램   
    * 게임 로직 : CPU 

### Step 1-1. 설계
* 절차(Procedure) 지향 : 함수 기반
    * 단점 : 함수 자체가 순서에 종속적 → 관리 어려움

* 객체 지향(Object Oriented) : 클래스 기반
    * 속성과 기능으로 나누어짐
    * ex) Knight
        * 속성: hp, attack
        * 기능: Move, Attack, Die


### Step 1-2. 디버깅
* 단축키 : F12?

* 브레이크 포인트(중단점) 
    * 숫자 앞 클릭 혹은 F9
    * 마우스 우클릭 옵션으로 해제시 흔적을 남길 수 있어서 유용함
    * 마우스 우클릭 옵션에서 조건을 선택하여 선택적으로 중단 가능
	* ex) 특정 몬스터 id를 옵션으로 하여 추적 가능
    * 개발 중에는 주로 사용 하나, 서비스 시에는 로그로 추적함

* 브레이크 포인트로부터 한단계씩 코드 실행
    * F11

* 프로시저(메소드) 단위 실행
    * F10

* 디버그 실행 중 노란색 화살표를 이동 시켜 실행 순서를 변경하여 실행 가능
    * 조사식을 통해 변수값도 수정하여 확인 가능

* 호출 스텍 : 
    * 몇 번째 레이어(Method) 안에 있는지 나타냄(영화 인셉션 생각)
    * 내가 오게 된 경로(코드 흐름)를 알 수 있음

* 조사식
    * 변수 값 확인 및 디버그 중 수정 가능

### Step 1-3. Stack/Heap 메모리
* Stack 메모리
    * 불안정 임시적
    * 함수를 실행하기 위한 메모장 같은 존재(실행 후 소멸)
    * 함수 안의 변수들은 본체가 Stack에 들어감
        * ex) struck 변수
    * 함수 안의 class(참조) 변수들은 본체 대신 주소(class의 경우 heap메모리 할당 주소)가 들어감
    * ref를 사용하여 참조시 본체가 스텍에 할당되어 있다면 스텍의 주소를 저장하게 됨
        * 참조한다고해서 모두 Heap 메모리에 본체가 있는 것은 아님 
    * 함수의 호출(영역 생성)가 종료(영역 소멸)를 통해 자동적으로 영역 관리가 됨
* Heap 메모리
    * 참조 타입 변수 본체 저장
    * class 인스턴스 생성 시 힙 메모리에서 할당됨
    * 깊은 복사 → Heap 메모리에서 할당되어 복사됨(knight.Clone())
    * C++에서는 할당된 메모리를 delete를 통해 소멸시켜줘야 되나 C#에서는 언어차원에서 가리키는 것이 없으면 자동으로 소멸됨

<br>

## STEP 2. Variable(데이터)

![image-20231226171136681](./../../../images/menu61-sub3-sub21-Basic/image-20231226171136681.png)

```c#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Test : MonoBehaviour  // class 이름은 script 파일 생성명, MonoBehaviour 상속
{

    // ==========enum(열거형) ========== //
    // 클래스 안이나 네임스페이스 내에서만 선언될 수 있음, 메서드 안이나 속성 안에서는 선언되지 않음
    // 변경 불가한 읽기 전용 깂 (예: 날짜, 색깔 등) 모아 관리 시 유용. 특히, int, bytes 등 정수형 상수 정의 시 유용
    enum Choice
    {
        Rock = 1,
        Paper = 2
        Scissors = 0
    }


    // ===========   구조체	=========== //
    // 클래스 안이나 네임스페이스 내에서만 선언될 수 있음, 메서드 안이나 속성 안에서는 선언되지 않음
    // 상속 여부 : Class는 상속이 가능하지만, 구조체는 상속이 불가능하다.
    // 형식 차이 : Struct는 값 타입(ValueType)이지만 Class는 참조(Reference Type)
    struct Player
    {
        public int hp;		// 밖에서도 사용 가능하다고 public 선언
        public int damage;
    } 

    void Start()
    {
        // ==========	int		==========
        int age = 30;
        Debug.Log(age);


        // ==========	float	========== 
        // 근사치를 저장함(int와 다른점)
        // ※ float형에 double형 대입시 float형에 들어가지 않는 범위 버려짐(오류 유발)
        // ※ 160.5f 사용(f 미사용시 double형 대입) 
        float height1 = 160.5f;
        float height2;
        height2 = height1;
        Debug.Log(height2);


        // ==========	string	==========
        // 문자와 숫자 더하기 하는 경우 int 변수를 문자열 취급
        // 큰 따음표 사용
        string name = "Harry Potter";

        // 1. 찾기
        bool found = name.Contains("Harry");	// true 
        int index = name.IndexOF('P');	// 6

        // 2. 번형
        name = name + " Junior";		// "Harry Potter Junior"
        string lowerCaseName = name.ToLower();	// 소문자 변형
        string upperCaseName = name.ToUpper();	// 대문자 변형
        string newName = name.Replace('r', 'l');	// 치환

        // 3. 분할
        string[] names = name.Split(new char[] {' '});	// 빈칸으로 분할
        string subStringName = name.Substring(5);	// 일정 인덱스 이후 문자부터 할당


        // ==========	char	==========
        // 작은 따음표 사용, 한글자만 저장
        char chr = 'R';
        Debug.Log(chr)


        // ==========   bool    ==========
        bool autoPlay = true;


        // ==========   var     =========== 
        // 자동 추론으로 빌드시 타입 대체
        // 가능하다면 타입을 명시하여 가독성을 높이는게 좋음
        var a = 1;
        var b = "STRING";
        var c = 1.0f;


        // ==========   Casting ==========
        // 큰 데이터 타입에서 작은 데이터 타입으로 변환 시 문법
        int a = 100;
        // (X) short b = a;		// Error occurred(큰 형식 → 작은 형식)
        shor b = (short)a; 	// Casting

        float c = a;
        int d = (int)c;		// Casting


        // ===========  String Format   ===========
        // string은 int와 float와 다른 class 해당되기 때문에 태생이 다름(Casting 외 다른 방법 필요)
        // string → int
        string input = Console.ReadLine();
        int number = int.Parse(input);
        Console.WriteLine(number);

        // int → string
        int hp = 100;
        int maxHp = 100;
        string message = string.Format("당신의 HP는 {0} / {1} 입니다", hp, maxHp);  // 예전 방식
        string message = $"당신의 HP는 {hp} / {maxHp} 입니다";		                // 요즘 방식
        console.WriteLine(message)

        
        // ==========    array   ==========
        int[] array = new int[5];

        array[0] = 1;
        array[1] = 2;
        array[2] = 3;
        array[3] = 4;
        array[4] = 5;
        for (int i = 0; i < array.Length; i++)
        {
            Debug.Log(array[i]);
        }

        int[] points = {53, 99, 53, 92, 51};
        int sum = 0;
        for (int i = 0; i < points.Length; i++)
        {
            sum += points[i];
        }
        float average = sum / points.Length;                // 정수로 계산되어 나옴
        float average_float = 1.0f * sum / points.Length;   // 1.0f 곱으로 소수 반환
        Debug.Log(average);
        Debug.Log(average_float);


        // ==========enum(열거형) ========== //
        // 클래스 안이나 네임스페이스 내에서만 선언될 수 있음
        // 메서드 안이나 속성 안에서는 선언되지 않음
        // casting을 통해 int로 사용 가능
        int choice = 3
        switch (choice)
        {
            case (int)Choice.Scissors:
                Console.WriteLine("가위");
                break;
            case (int)Choice.Paper:
                Console.WriteLine("보");
                break;
            case (int)Choice.Rock:
                Console.WriteLine("주먹");
                break;
        }


        // =========== struck(구조체) ========== //
        // 한번에 여러 데이터를 넘기고 관리하는데 유용함
        Player player;
        CreatePlayer("Knight", out player);
        Debug.Log($"hp:{player.hp}, damage:{player.damage}");

    }

    // struck(Player)을 통한 데이터 관리
    static void CreatePlayer(string classType, out Player player)
    {
        if (classType == "Knight")
        {
            player.hp = 10;
            player.damage = 5;
        }
    }

}

```

<!------------------------------------ STEP ------------------------------------>

<br>

## STEP 3. Operation(로직)

```c#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Test : MonoBehaviour  // class 이름은 script 파일 생성명, MonoBehaviour 상속
{
    void Start()
    {
        // ==========   Four basic Operations    ========== 
        int a = 10 / 3;     // 3
        int a = 10 % 3;     // 1

        int b = a++;
        // int b = a;
        // a += 1

        int b = ++a;
        // a += 1;
        // int b = a;


        // ===========  Comparison & Logical Operation  ========== 
        // AND  OR  NOT
        // &&   ||   !
    }
}
```

<!------------------------------------ STEP ------------------------------------>

<br>

## STEP 4. 제어문(로직)

```c#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Test : MonoBehaviour  // class 이름은 script 파일 생성명, MonoBehaviour 상속
{
    void Start()
    {
        // ==========	if	==========
        // 변수 범위: 중괄호 안에서 선언한 변수는 중괄호 안에서만 사용 가능
        bool isDead = ture
        if (isDead)
            Debug.Log("if문");

        int hp = 20;
        if (hp <= 50)
        {
            string inner_str = "전사";
            string log_message = inner_str + "도망!";
            Debug.Log(log_message);
        }
        else if (hp >= 200)
        {
            Debug.Log("공격");
        }
        else
        {
            Debug.Log("방어!");
        }
        // (X) Debug.Log(inner_str); // 변수 범위를 벗어나므로 오류 발생
        

        // ==========   switch  ==========
        // if 문의 축소판이지만 가독성이 좋아 if문에 우선시하여 사용
        // case 값으로 일반 변수 사용시 에러 발생, const 변수(상수), enum 사용 가능
        // case 값으로 하드코딩 대신 상수나, enum 값 사용 
        switch (choice)
        {
            case 0:
                Debug.Log("가위");
                break;
            case 1:
                Debug.Log("바위");
                break;
            case 2:
                Debug.Log("보");
                break;
            case 3:
                Debug.Log("치트키");
                break;
            default:	// else문과 같음
                Debug.Log("해당 없음");
                break;
        }


        // ===========  삼항연산자  ===========
        int number = 25;

        // bool 변수명 = (조건 ? 맞을때 : 틀릴때);
        bool isPiar = ((number % 2) == 0 ? true : false)

        // 아래와 같은 의미
        bool isPair;
        if ((number %2) == 0)
            isPair = true;
        else
            isPair = false;


        // =========== while =========== //
        int count = 5;
        while (count > 0)
        {
            Debug.Log("Hello, World");
            count--;
        }
        

        // 먼저 실행 후 while문 체크(사용빈도 적음)
        string answer
        do
        {
            Console.WriteLine("강사님은 잘생기셨나요? (y/n) : ");
            answer = Console.ReadLine();	// do문 안에서 string answer 시 while문 비교에 사용 안됨(변수범위)
        } while (answer != "y");


        //==========   for   ==========
        // for (초기화식; 조건식; 반복식) {내용문}
        // 초기화식 조건식 내용문 반복식 순서로 실행
        for (int i = 3; i >= 0; i--)
        {
            Debug.Log(i);
        }


        // =========== break =========== //
        // 특정 조건에서 바로 for 문을 뛰어 나옴
        int num = 97;
        bool isPrime = true;

        for (int i = 2; i < num; i++)
        {
            if ((num % i) ==0) 
            {
                isPrime = false;
                break;
            }
        }

        if (isPrime)
            Debug.Log("소수입니다");
        else
            Debug.Log("소수가 아닙니다");

        // =========== countinue =========== //
        // 특정 조건에서 바로 다음 루프 실행
        for (int i = 1; i <= 100; i++)
        {
            if ((i % 3) !=0)
                continue;
            
            // 3으로 나눠질 때 내용 기재 → if문 보다 가독성이 좋아짐
            Debug.Log($"3으로 나뉘는 숫자 발견 : {i}");
        }

    }
}
```

<!------------------------------------ STEP ------------------------------------>

<br>



## STEP 5. Method(Function)

* static 선언 시 class에 종속되는 유일한 Method 생성 가능
    * static 내부에서는 this 사용 불가(공용 함수라 개개 인스턴스 고유 정보 접근 불가)

* static method는 객체 생성 없이 직접 호출 가능
    * (static method) Console.WriteLine();
    * (일반 method) Random rand = new Random(); rand.Next(0, 2);

```c#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Test : MonoBehaviour  
{
    // Method
    // class 안에 있어야 함
    // 한정자 반환형식 이름(매개변수목록) {}
    // 한정자: static 

    // ==========    인수도 반환값도 없는 메서드    ========== //
    //void: 반환값이 없음을 의미
    void SayHello()
    {
        Debug.Log("Hello");
    }


    // ==========    인수를 출력하는 메서드 ========== //
    void CallName(string name)
    {
        Debug.Log("Hello" + name);
    }


    // ==========    인수와 반환값이 있는 메서드    ========== //
    // 선택적 매개변수: 초기 Method 선언시 인수값을 미리 지정해주면 입력 안해도 가능 
     int Add(int a, int b = 0, float c = 1.0f, double d = 3.0)
    {
        int result = a + b + c + d;
        return result;
    }

    void Start()
    {
        SayHello();
        CallName("Hello");
        int answer = Add(2, d:3.0f);    // 선택적 매개변수 값 지정
        Debug.Log(answer);
    }


    // ==========   ref    ========== //
    // 입력받은 변수를 직접적으로 변화시키고 싶을 때 메모리 참조하겠다는 뜻
    // return 대신 원본 변수로 반환 받는 경우
    // Swap 같은 함수 작성 시 유용
    static void AddOne(ref int number)  
    {
        number = number + 1;
    }

    static void AddOne2(int number) // 일반적으로 해당 방식 사용 권장
    {
        return number + 1;
    }

    void Start()
    {
        // 복사(짭퉁) 참조(진퉁)
        int a= 0;
        AddOne(ref a);  // ref 안쓰면 에러 발생(원본 변환 확인용)
        Debug.Log(a);

        a = AddOne2(a)
        Debug.Log(a);
    }

    static void Swap(ref int a, ref int b)
    {
        int temp = a;
        a = b;
        b = temp;
    }


    // ==========   out    ========== //
    // ref의 경우 실제로 사용하지 않거나 값을 넣어주지 않아도 정상 동작(에러 유발)
    // 다중 반환 가능, 반드시 값 넣어줌 필요   
    static void Divide(int a, int b, out int result1, out int result2)
    {
        result1 = a / b;
        result2 = a % b;
    }

    void Start()
    {
        int num1 = 10;
        int num2 = 3;

        int result1;
        int result2;
        Divide(num1, num2, out result1, out result2);
    }


    // ==========   Method Overloading   ========== //
    // 함수 이름의 재사용
    // 함수 이름이 같다면 매개변수 개수 또는 형식이 달라야함
    static int Add(int a, int b)
    {
        return a + b;
    }

    static int Add(int a, int b, int c)
    {
        return a + b + c;
    }

    static float Add(float a, float b)
    {
        return a + b;
    }

    void Start()
    {
        int result = Add(2, 3);
        float result2 = Add(2.0f, 3.0f);
        Debug.Log(result);
        Debug.Log(result2);

        
    // ===========  재귀함수    =========== //
    static int Factorial(int n)
    {
        if (n <= 1)
            return 1;

        return n * Factorial(n - 1);
    }

    }
}
```

<!------------------------------------ STEP ------------------------------------>

<br>

## STEP 6. Class

* [class와 struck 비교 블로그 url](https://velog.io/@livelyjuseok/C-Struct%EC%99%80-Class%EC%9D%98-%EC%B0%A8%EC%9D%B4.-%EA%B7%B8%EB%A6%AC%EA%B3%A0-%EC%99%9C-%EC%82%AC%EC%9A%A9%ED%95%A0%EA%B9%8C)
* [enum과 class 비교 블로그 url](https://homzzang.com/b/cs-36)
* enum, struct, class 비교
    * enum: 각 상수가 서로 다른 의미를 가지는 상황 적합(복사)
        * casting으로 int 표현 가능
        * ex) 요일
    * struct: 변수가 각기 다른 데이터를 가질 필요가 있을 때(복사)
        * ex) x, y 좌표 포인트
    * class: 인스턴스를 생성하여 각기 인스턴스의 변수값이 변할 필요가 있을 때(참조)
        * ex) 게임 몬스터 인스턴스 생성
* 클래스 안에 소속되어 있는 변수 : 필드
    * 필드 들은 class 인스턴스마다 다른 값을 가질 수 있음
    * static 선언 변수는 오로지 1개만 존재함

```c#
// 참조(ref)
class Knight
{
    static public int counter;  // 오로지 1개만 존재!

    // 속성
    public int id;              // public 모두 사용, 없을 경우 class 내에서만 사용
    public int hp;         
    public int attack;

    // 기능
    public void Move()
    {
        Console.WriteLine("Knight Move");
    }

    public void Attack()
    {
        Console.WriteLine("Knight Attack");
    }

    // 깊은 복사
    public Knight Clone()
    {
        Knight knight = new Knight();
        knight.hp = hp;
        knight.attack = attack;
        return knight;

    // =========== 생성자 =========== //
    // new로 생성 시 호출
    // class 이름과 같아야됨, 반환하는 타입 입력 안함
    public Knight()
    {
        hp = 100;
        attack = 10;
        Debug.Log("생성자 호출!");

        id = conuter;   // static 필드 사용예(아이디 카운터 발급)
        counter++;
    }

    /*
    public Knight(int hp, int attack)	// 생성자로 인수를 받는 경우 // Knight knight = new Knight(50, 10);
    {
        this.hp = hp;		// 생성자로 같은 이름 사용시 this를 사용하여 구분할 수 있음
        this.attack = attack;
        Debug.Log("int 생성자 호출!");
    } */

    public Knight(int hp) : this()	// 생성자 생성 후 빈 칸은 제일 처음 default 생성자의 값으로 채워 넣음(attack=10), 긴 인수를 가지는 경우 유용함
    {
        this.hp = hp;		
        Debug.Log("int 생성자 호출!");
    }

    // static method 
    // method 내부에 this는 사용 안되지만 인스턴스가 사용안된다는 것은 아님
    // Knight knight = Knight.CreateKnihgt();로 생성가능
    // Knight.Move();는 안되는 것가 차이 유의(인스턴스 생성 후 객체로 호출해야함)
    static public Knight CreateKnight()
    {
        Knight knight = new Knight();
        knight.hp = 100;
        knight.attack = 1;
        return knight
    }
    }

}


// 복사
struct Mage
{
    public int hp;
    public int attack;
}

class Program
{
    static void KillMage(Mage mage)
    {
        mage.hp = 0;
    }

    static void KillKnight(Knight knight)
    {
        knight.hp = 0;
    }

    static void Main(string[] args)
    {
        Knight knight = new Knight();   // new : 클래스를 가지고 새로운 객체를 만들 때 사용
        knight.hp = 100;
        knight.attack = 10;
        knight.Move();
        knight.Attack();
        KillKnight(knight); // 참조하여 넘기기 때문에 knight.hp는 0
        // 별도의 ref를 사용하지 않아도 참조됨

        Mage mage;
        mage.hp =100;
        mage.attack = 50;
        KillMage(mage);     // 복사하여 넘기기 때문에 mage.hp는 100

        Mage mage2 = mage;
        mage2.hp = 0;       // mage.hp는 100 유지(복사)

        Knight knight2 = knight;
        knight2.hp = 0;     // knight.hp는 0(참조)
        // 독립 인스턴스 생성방법
        // Knight knight2 = new Kinght();   // 1. 새 인스턴스 생성
        // knight.hp = 100; // Killknight 때문에 삽입
        // knight2 = knight.Clone();        // 2. 깊은 복사 사용
    }
}
```

<!------------------------------------ STEP ------------------------------------>

## STEP 7. 상속성
* OOP(객체지향 프로그래밍) 3대 특성 : 은닉성/상속성/다형성
* 상속성 언제 사용?
    * Knight 말고 Mage, Archer 등 직업군을 만들 때 모두 id, hp, attack 등 동일 필드 사용하나 매번 복붙할 수 없음
    * 묶을만한 하나의 개념

```c#
class Player		// 부모, 기반
{
    static public int counter = 1;
    public int id;
    public int hp;
    public int attac;    

    public Player()
    {
        Console.WriteLine("Player 생성자 호출");
    }

    public Player(int hp)
    {
        this.hp = hp;
        Console.WriteLine("Player hp 생성자 호출");
    }

    public void Move()
    {
        Debug.Log("Player Move"); 
    }
}

class Mage : Player		
{
}

class knight : Player	// 자식, 파생
{
    int a;

    // base를 통해 부모에 접근 가능
    public Knight() : base(100)	// base(100) 을 통해 Player(int hp) 생성자 호출 가능
    { 
        this.a = 10;
        base.hp = 200;
        Console.WriteLine("Knight 생성자 호출!");
    }
}

class Program
{
    static void Main(string[] args)
    {
        Knight knight = new Knight();
        knight.Move();
    }
}
```

<br>

<!------------------------------------ STEP ------------------------------------>

## STEP 8. 은닉성

* 은닉성
    * 보안레벨
    * 왜 사용?
        * ex) 자동차 핸들 페들 차문 정도만 조작 // 전자장치, 엔진 등은 외부에 노출되어 있지 않음 
* 접근한정자
    * public : 모두에게 공개
    * protected : 상속받은 class까지 사용 가능
    * private : class 내부에서만 사용(아무것도 입력하지 않을 시 default값)

```c#
class Knight
{
    private int hp;
    protected int attack;

    public void SetHp(int hp);		// 브레이크 포인트를 잡은 다음 누가 hp를 고쳤는지 확인하기 쉬움
    {
        this.hp = hp;
    }
}	

class SuperKnight : Knight
{
    void Teset()
    {
        attack = 10;		// protected 필드 접근
    }
}
```

<br>

<!------------------------------------ STEP ------------------------------------>

## STEP 9. class 형식 변환

```c#
class Player
{
    protected int hp;
    protected in attack;     
}


class Knight : Player
{
}

class Mage : Player
{
    public int mp;
}

class Program
{
    static void EnterGame(Player player)	// Knight나 Mage가 아니라 Player 가능
    {
        
        // (X) Mage mage = (Mage)player;    // knight를 인수로 받음에도 class 변환 가능	
        // (X) mage.mp = 10;                    // knight에 인수가 없으므로 실행시 에러발생
        // 위 코드는 컴파일 과정에서 정상문법으로 인지하므로 에러를 알기 어려움
        // class 변환시 크로스 체크를 하는 과정이 필요함
        // 1.
        bool isMage = (player is Mage);
        if (isMage)
        {
            Mage mage = (Mage)payer;
            mage.mp =10;
        }

        // 2. as 연산자: 변환가능 시 결과 리턴 실패하면 null 리턴
        // 캐스트 식과 달리 as 연산자는 예외를 throw하지 않음
        Mage mage = (player as Mage);	// Mage 클래스가 아닐 경우 null
        if (mage != null)
            mage.mp = 10;
    }

    static void Main(string[] args)
    {
        Knight knight = new Knight();
        Mage mage = new Mage();

        // Mage 타입 → Player 타입 가능
        Player magePlayer = mage;
        // Player 타입 → Mage 타입?
        //(X) Mage mage2 = magePlayer        // Error occurred
        Mage mage2 = (Mage)magePlayer;     // class 변환

        EnterGame(knight);
    }
}
```

<br>

<!------------------------------------ STEP ------------------------------------>

## STEP 10. 다형식(virtual, override)

* 오버라이딩 
    * 어떤 함수에다가 실제 타입에 따라서 다양한 형태로 동작하겠다는 의미
    * virtual method를 상속받으면 자손 뿐만 아니라 손자 이하도 override 가능

* virtual 버전은 일반 버전보다 성능에 부하를 미치기 때문에 모두 virtual은 비추천

```c#
// =========== 다형성 사용 이전  =========== //
class Player
{
    protected int hp;
    protected in attack;     

    public void Move()
    {
        Console.WriteLine("Player 이동!");
    }    
}


class Knight : Player
{
}

class Mage : Player
{
    public int mp;

    public new void Move()	// new를 붙임으로써 새로운 Method 가능 
    {
        Console.WriteLine("Mage 이동!");
    }    
}

class Program
{
    static void EnterGame(Player player)	
    {
        bool isMage = (player is Mage);
        if (isMage)
        {
            Mage mage = (Mage)payer;
            mage.mp =10;
        }

        player.Move();    
        // mage를 인수로 넘겨줘도 우리가 새로 지정한 mage.Move()가 동작하지 않음 
        // 앞으로 이런식으로 코드가 많이 작성될 텐데 어떻게 구별하지?
    }
    
    static void Main(string[] args)
    {
        Knight knight = new Knight();
        Mage mage = new Mage();

        EnterGame(mage);
    }
}

// =========== 다형성(virtual)  =========== //
class Player
{
    protected int hp;
    protected in attack;     

    public virtual void Move()	// virtual 추가
    {
        Console.WriteLine("Player 이동!");
    }    
}


class Knight : Player
{
    public override void Move()     // 오버라이딩하여
    {
        base.Move();		                // 부모껄 먼저 호출 후(자주 쓰이는 패턴) 
        Console.WriteLine("Knight 이동");    // 기능 추가
    }
    // (참고) public sealed override void Move() : sealed 사용시 이후 자손 부터는 오버라이딩 불가

}

class Mage : Player
{
    public int mp;
	
    // 오버라이딩 cf) 오버로딩(함수 이름의 재사용)
    public override void Move()	// new 대신 override 변경 
    {
        Console.WriteLine("Mage 이동!");
    }    
}

class Program
{
    static void EnterGame(Player player)	
    {
        bool isMage = (player is Mage);
        if (isMage)
        {
            Mage mage = (Mage)payer;
            mage.mp =10;
        }

        player.Move();	// 
    }
    
    static void Main(string[] args)
    {
        Knight knight = new Knight();
        Mage mage = new Mage();

        EnterGame(mage);    // mage.Move(); 잘 호출 됨
    }
}
```

<br>

<!------------------------------------ STEP ------------------------------------>

## STEP 11. ETC

```c#
// ==========   Const(상수)   ========== //
Const int GAME_SPPED = 50;
// (X) GAME_SPEED = 15; // Error occurred(Const varient)


// =========== Random   ========== //
Random rand = new Random();
int a = rand.Next(1, 4); // 1, 2, 3 중 랜덤 반환
```

