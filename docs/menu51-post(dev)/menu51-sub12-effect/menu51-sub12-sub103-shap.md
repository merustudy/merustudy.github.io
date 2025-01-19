---
layout: default
title: shape
nav_order: 103
parent: P(Dev)
grand_parent: Post(Dev)
---

# 이펙트 제작 초보자용 가이드#3 Shape

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

* https://gall.dcinside.com/mgallery/board/view/?id=198234567890&no=4&page=2



------







![78eb8673b3876ef33bf1c6bb11f11a39a823dce9dd2322bc](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6aade22382e4ddd5fba0b47e193597f6e667863d700b5a9002f5e45e3)**2**



많은 타입이 존재하지만 실무에서는 **Sphere/Cone/Box** 세가지만 제대로 알아도 문제없음
나머지는 활용도가 매우 낮고 결국 기본의 파생형일뿐 딱히 다를게 없다

**Cone**
파티클 시스템을 추가하면 가장 기본으로 설정되어있는 모양임
2D프로젝트에서는 이거 원툴로 사용해도 될만큼 기초적이다



![7eef8174b48169f43dec84e4458375739fc0abdb2f880df004150e7453b483](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9caf13ee1da0b19b800996a37)**3**



실린더라고 생각하면 되는데 부채꼴로 퍼트릴수도 직선형 원통으로 만들수도 있음
**Angle**값을 통해 위 짤 처럼 부채꼴 각도를 조절할수있고
**Radius**값으로 통의 크기를 키울수있음
**RadiusThickness** 값이 중요한데



0으로 설정하면 원의 외곽에서만 생성되고 1로 설정하면 원안의 모든 범위에서 생성 됨



![7eec8275b4806bf73cee85e758d62d3b35e9437d1bebe5b08058aedc](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9cda239ef88594aeab2026e48)**4**



**Angle**값을 90도로 맞춰 놓고 사용하면 위 짤처럼 폭발이나 피격 이펙트들에 써먹을 수 있는 방사형 이펙트가 만들어지는데



![79ee8272b6806cf43deb85e74485777330b5cc64053ca6935829cb24b529d1](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d99bf73ee18c5c43ec3ea2605f)**5**



**StartSpeed**값을 마이너스로 입력하면 원 안으로 들어오는 이펙트를 만들 수 있다



![7eef8474b7816cf53ceb85e7429f2334757d4c82de5b51b75ff4901d02](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9ccfe3de3da591de94bf9d2e1)**6**

반대로 **Angle**값이 0에 가까운 원통형은 이런 쏘아내는 느낌의 버프이펙트를 만들 수 있고





![79ee8272b6806af53aed85e14282766f813783f4188878a3f67739d9f4d03b851a96](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9cffe6ce78b5d18e93ee36b49)**7**



이걸 **#2**에서 다룬것처럼 존나게 생성시킨 버전이 브래스가 되는거다

레이저를 만들게되면 그 레이저 주변을 이쁘게 장식할 파티클을 이 원통형으로 만든다

그리고 가장 많이 건드는 옵션중 하나가



![7eee8174b4806bf53fed85fb06df231dace6f335c7882742d06c](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6aade22382e4ddd5fba0b47e193597f6e31223159f8b4294b2fe30915)**8**



**Arc - Mode**인데 기본적으로는 **Random**으로 설정되어있음



![7cee8275b48069f53cee85e758d62d3bfbf6f1ca72e43d1e81f90e](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9cfa23fb28a094abd70679efe)**9**



**Loop**와 **Ping-Pong**은 앞서 **#2**에서 다뤘던 것처럼 **Duration**시간동안 **Shape**의 모양을 따라가며 생성하게 해주는 옵션으로
**Emission**에서 **Bursts**타입으로 한번에 많이 생성하는 방식과는 연동이 안되니 조심하고



![7eec8277b78169f53fec87e6449f23349e9812cc11eab3b546d63990](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9cbf268e0d95c43ed629f2330)**10**



반대로 **BurstSpread**는 한번에 많이 생성할때 객체가 겹치지않게 나눠서 뿌려주는 옵션이라 캐주얼 게임에 자주 쓰게된다



![7fec8375b7836bf43fec84e644806a3af11ab60e0ba03a631d57ef337a5f](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d99ba538e5d9594fef39764868)**11**



이런것 또한 **BurstSpread**옵션으로 생성하는거



![7cef8375b48069f53cec87e758d62d3b74c445ca4209d574beb3be](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d99ba039e78e5b1fefdc2fc5fa)**12**



물론 **Bursts**가 아닌 **Rate over Time**로 생성하게되면 한점에서만 생성되서 망하게되니까 주의



**Sphere**
3D프로젝트에서 많이 사용하는 모양으로 3차원값을 모두 쓰는 구체 형태를 띄고있음
2D적 표현으로는 한계가 있을때 사용하게되고 바닥에 배치해야 할 경우 반구체 모양인 **Hemisphere**를 쓰기도함
**cone**하고 구조가 비슷해서 설명할 포인트가 크게 다르진 않음
**Radius**값으로 구체의 크기를 키울수있고
**RadiusThickness** 값으로 구체 내부에서도 생성할지 외곽에서만 생성할지를 결정할수 있음



![7eec8275b7836bf73cec87e7458375731e41c31b943249c82ea9abeea13ae239](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d998ff6fef8c5c1dee25b0a34f)**13**



**Cone**의 경우와 마찬가지로 **StartSpeed**값을 마이너스로 입력해서 기모으는 연출을 입체적으로 표현 가능함
**RadiusThickness** 값을 0으로 해두지 않으면 반대 방향으로 뚫고 나가는 상황을 겪을 수 있으니 반드시 0에 가까운 수를 입력해두면됨
결국 **Cone**이랑 제작 방식은 비슷하니까 전방위를 표현해야하는 디테일이 필요할때만 쓰면됨



![7eec8275b7836bf43fed85e644806a3ac3e521561411703907671b31a8fc](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9c7a73fe18f5f1eef7668168d)**14**



나중에 다루게될 **Renderer**항목에서 **RenderMode**를 **Stretcged Billboard**타입으로 바꾸면
이렇게 에네르기파 기모으는 연출도 가능해진다



![7cee8274b68069f73ded87e6449f2334d1547bea0e429f08b1dee0c398](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d99cfe6eb4820a19edf6df4c69)**15**



물론 쏘아보내는것도 가능

**Box**
대부분 배경오브젝트에 배치해놓는 용도의 이펙트에 사용하게됨



![7eef8175b4806bf73cee85e7478276736f4d7104ac4a76ad10a183ebe6dc9d](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9cea06cb78d564de837c8038e)**16**





![7eec8277b68069f53cee85e7458076736acd51a29ef3d11ae85b4daa92d6](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d99da36fe4da0a4eb83eca32ea)**17**



반딧불이나 물방울 / 용암의 표면같은 설치형 이펙트들을 띄울때 사용한다
**EmitFrom**만 잘 체크해두면 되는데
**Volume** - 박스의 내부좌표에서 생성
**Shell** - 박스의 표면에서만 생성
**Edge** - 박스의 외곽 라인에서만 생성
이렇게 나눠지니까 어차피 안보이는 곳에 이펙트 뿌리지말고 잘 선택해서 최적화를 잘해보도록하자





------


다른 **Shape**옵션중에선 **Rotation**와 **Scale**정도만 사용하고
나머지는 알 필요 없음 이것들을 건들이면 반드시 바리에이션 칠때 사고가 발생한다
**Shape**항목은 여기서 끝
