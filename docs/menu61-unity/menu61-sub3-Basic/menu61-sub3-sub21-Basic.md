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



## STEP 1. Variable

![image-20231226171136681](./../../../images/menu61-sub3-sub21-Basic/image-20231226171136681.png)

```C#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Test : MonoBehaviour  // class 이름은 script 파일 생성명, MonoBehaviour 상속
{
    void Start()
    {
        // ==========	int		==========
        int age = 30;
        Debug.Log(age);


        // ==========	float	========== 
        // ※ float형에 double형 대입시 float형에 들어가지 않는 범위 버려짐(오류 유발)
        // ※ 160.5f 사용(f 미사용시 double형 대입) 
        float height1 = 160.5f;
        float height2;
        height2 = height1;
        Debug.Log(height2);


        // ==========	string	==========
        // 문자와 숫자 더하기 하는 경우 int 변수를 문자열 취급
        string str = "happy";
        string message = str + age;
        Debug.Log(message);
        
        
        //==========    array   ==========
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
    }
}
```



<!------------------------------------ STEP ------------------------------------>

<br>



## STEP 2. 제어문

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
        int hp = 20;
        if (hp <=50 )
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
        

        //==========   for   ==========
        for (int i = 3; i >= 0; i--)
        {
            Debug.Log(i);
        }
    }
}
```

<!------------------------------------ STEP ------------------------------------>

<br>



## STEP 3. Method

```c#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Test : MonoBehaviour  
{
    //==========    인수도 반환값도 없는 메서드
    //void: 반환값이 없음을 의미
    void SayHello()
    {
        Debug.Log("Hello");
    }


    //==========    인수를 출력하는 메서드
    void CallName(string name)
    {
        Debug.Log("Hello" + name);
    }



    //==========    인수와 반환값이 있는 메서드
     int Add(int a, int b)
    {
        int c = a + b;
        return c;
    }


    void Start()
    {
        SayHello();
        CallName("Hello");
        int answer = Add(2, 3);
        Debug.Log(answer);
    }
}
```

<!------------------------------------ STEP ------------------------------------>

<br>



## STEP 4. Class

```c#
```

