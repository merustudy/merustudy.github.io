---
layout: default
title: Coroutine
nav_order: 41
parent: Basic(Unity)
grand_parent: Unity
---

# Coroutine

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

## STEP. 

### Step 1-1. StopCoroutine

```C#
//시작할 때
Startcoroutine("코루틴명칭");//string 호은 IEnumerator 개체명

// 중단할 떄
StopCoroutine("코루틴명칭");//이렇게 쓰면 안됨
```

* StartCoroutine는 잘되는데 StopCoroutine은 안됨
    * StopCoroutine을 할때는 IEnumerator 혹은 Coroutine 변수를 선언 후 할당해주어야
    * [URL](https://m.blog.naver.com/yoohee2018/220827807653)