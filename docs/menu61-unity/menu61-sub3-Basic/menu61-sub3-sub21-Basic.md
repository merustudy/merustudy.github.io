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

## STEP 0. 기본 지식

* 게임의 구분
    * 게임 데이터(게임 구현 리소스 등) : 램   
    * 게임 로직 : CPU 

<br>

## STEP 1. Variable(데이터)

![image-20231226171136681](./../../../images/menu61-sub3-sub21-Basic/image-20231226171136681.png)


```C#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Test : MonoBehaviour  // class 이름은 script 파일 생성명, MonoBehaviour 상속
{

    // ==========enum(열거형) ========== //
    // 클래스 안이나 네임스페이스 내에서만 선언될 수 있음
    // 메서드 안이나 속성 안에서는 선언되지 않음
    enum Choice
    {
        Rock = 1,
        Paper = 2
        Scissors = 0
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
        string str = "happy";
        string message = str + age;
        Debug.Log(message);


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
    }
}

```

<!------------------------------------ STEP ------------------------------------>

<br>

## STEP 2. Operation(로직)

```C#
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

        int b =a ++;
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

## STEP 3. 제어문(로직)

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
        // Debug.Log(inner_str); // 변수 범위를 벗어나므로 오류 발생
        

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
            
            // 3이 아닐 때 내용 기재 → if문 보다 가독성이 좋아짐

            Debug.Log($"3으로 나뉘는 숫자 발견 : {i}");
        }

    }
}
```

<!------------------------------------ STEP ------------------------------------>

<br>



## STEP 3. Method(Function)

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
    }
}
```

<!------------------------------------ STEP ------------------------------------>

<br>

## STEP 4. Class

```c#
```

<!------------------------------------ STEP ------------------------------------>

<br>

## STEP 9. ETC

```c#
// ==========   Const(상수)   ========== //

Const int GAME_SPPED = 50;
// (X) GAME_SPEED = 15; // Error occurred(Const varient)
```

