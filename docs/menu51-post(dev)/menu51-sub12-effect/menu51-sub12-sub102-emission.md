---
layout: default
title: emission
nav_order: 102
parent: P(Dev)
grand_parent: Post(Dev)
---

# 이펙트 제작 초보자용 가이드#2 Emission

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

###  

* https://gall.dcinside.com/mgallery/board/view/?id=198234567890&no=3&page=2




**Emission**
객체의 생성 방식과 개수를 결정하는 항목



**Rate over Time**



![7fee8175b7836bf43fec87e747827673795617bd297d3cc14dfa8961bac6fd](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9cdf43eb5da564ab94b135c77)**2**



초당 생성될 개수를 입력하는 곳 지속해서 뿌려질 이펙트를 제작할때 많이 사용됨
ex) 모닥불의 불똥 / 물방울 / 용암방울





![7fec8277b7836af720afd8b236ef203e4c7f7b0fa507d8](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6aade22382e4ddd5fba0b47e193597f6e627261b2438227ae02cee2e3)**3**



왼쪽끝 역삼각형 모양을 눌러서 **Curve**를 **Duration**시간동안 서서히 생성량을 줄어들게 잡게되면



![7eef8175b4806bf73cec87e747826a3aa3a06d433fb1f8d4326e38378f43](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9cca03de5d80b1eee1df3d3b2)**4**





![7fee8174b68169f43fec84fb11d8221d2c1dd6ca6b5174eb665280](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d99af538e0d95719bebedb41c8)**5**



브레스같은 연출을 할수있음

**Rate over Distance**

이 이펙트가 달리는 부모나 이펙트 최상단에 이동값이 생겼을경우 거리에 비례해서 생성함
멈춰있을때는 나오지않지만 움직임이 생겼을때 나와야하는 연출에 이 값을 사용하게됨



![7eef8377b78169f43fec84e747826a3ae3f3c47848fbd136f81a3a068e0a0c](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d99aa46eb38d0b1def1c2eb214)**6**



캐릭터의 꼬리나 발 혹은 자동차의 끝부분에 달아두면 아주 간단하고 실용적인 꼬리가 만들어짐
단순 달아두는것뿐만 아니라 부모이펙트의 서브로 써먹을수가 있는데



![7fec8375b7836bf43fec84e644806a3af11ab60e0ba03a631d57ef337a5f](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9c8a338e2835d19bd868a9357)**7**



나중에 본격적으로 다뤄볼 SubEmitters를 통해 부모 이펙트의 움직임을 따라서 생성되는 서브 이펙트로 만들수 있음
UI 버튼들 외곽을 따라 움직이는 꼬리이펙트들을 만들때도 아주 좋다

**Bursts**
위에 Rate over관련 옵션들이 시간/거리에 따라 한개씩 빠르거나 느리게 생성하는거라면
이 항목은 객체를 한번에 여러개를 생성하고 싶을때 사용됨



![7eef8377b78169f43fec84e445836a3a91cc944ab0760f65b6d34c45948a](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9cef16fe1dd5b1ae904e5954a)**8**





![7cee8277b6836bf43fec84fb06df231d96922c7f722172b36a20](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6aade22382e4ddd5fba0b47e193597f6e3a7434dcd4d0c5bcc1cca0fc)**9**



대부분의 피격이나 파괴 이펙트들은 해당 기능을 통해 만들어진다
**Count**
해당 **Time**에 한번에 생성할 개수를 적는곳인데
역삼각형 모양을 통해 **Curve**그래프로 바꿀수가 있지만 이전 글에서 다뤘던 **S****tartS****ize** 항목과 다르지 않음
0초에 25개를 생성하고 끝나는 상태이기 때문에 그래프적용이 안된다는 말



![7eef8175b7836bf43fee85e758c12a3a4bd3ff06deb8bb1e58c6](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6aade22382e4ddd5fba0b47e193597f6e3677656e1b07a997530a9b01)**10**



이 그래프를 적용시키려면 **Cycles**타입을 **Infinite**로 바꿔주거나 **Count**상태에서 **Interval**를 늘려주면되는데



![7eef8175b6836bf73fed85fb11d8221d04e02451c46b12578c5c11](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d99ba03eb38d581aec9710268b)**11**



이런식으로 그래프가 영향받을수 있게끔 바꿀수 있음
이때 **Interval**값을 늘려주지 않으면 딜레이없이 모든걸 쏟아내기 때문에 엄청난 렉이 생길수도 있다



![7eef8175b7836bf43fec84e4458375735388c07f04ce3ecc2731e46d8fa96e](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d99ff26bb78f5a42b87f30bb3e)**12**



이 옵션으로도 브레스 이펙트를 만들수 있는데 **Rate over Time**과 다른부분은 한번에 여러개를 생성할수 있기 때문에 위와같은 연출이 가능하다는점

하지만 보통 이렇게까지 파티클을 뿌려댈일이 별로 없고



![79e98472b19c3faf689fe8b115ef046505612b07](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d99ffe69e4885d18e926c19a52)**13**







![7cef8274b78076b660b8f68b12d21a1d146dab4032](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6aade22382e4ddd5fba0b47e193597f6e3b723548de788aefed969478)**14**



이렇게 **Bursts**를 늘려 **Time**을 분할 지정해서 뿌리는게 정석임

