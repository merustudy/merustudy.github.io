---
layout: default
title: 이펙트 제작 초보자용 가이드#1 Particle System
nav_order: 101
parent: P(Dev)
grand_parent: Post(Dev)
---

# 이펙트 제작 초보자용 가이드#1 Particle System

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

* https://gall.dcinside.com/mgallery/board/view/?id=198234567890&no=2&page=2



------





유니티에서 이펙트를 만드는 방식은 크게 두가지가 있음


완성된 이펙트를 시퀀스화 시켜서 한장한장 애니메이션 시키는방식과
리소스 한장을 파티클 시스템으로 굴리는 방식

자세하게 적으면 끝도 없는데
결국 둘 다 쓰게되긴 하니까 뭘 선택할 필요는 없음

다만 유니티로 이펙트를 만드려면
드로잉실력이 되던가 에프터이펙트나 파티클일루전같은 시뮬레이션 툴들을 배워야 한다는건데
게임제작 관련 갤러리중 유일하게 살아남은 갤러리는 플머들밖에 없는 인디게임개발 갤러리뿐이니까
이펙트 에셋을 구매했다는걸 가정하에 설명해 줄것임

\- 유니티외에 드로잉이나 기타 툴 설명은 생략하겠다는 말








결국 파티클 시스템을 알아야 제작하거나 구매한 에셋을 수정하는게 가능하겠지?
지금부터 쓸일 없는건 걍 생략하고 필요한 부분들만 활용방법을 위주로 설명해주겠음





![7cee8274b78169f43dee98a518d60403727719fffa75ad8823](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27791cfc686f767dfdfd08770cdcf963bc861944964168a444d8f63f6f2c90d503db854b2ad0b1dd39cb9f68da)**1**



파티클시스템을 추가해보면 이런 상태를 볼수있을거임 이 위쪽 메인시스템에 대한 설명부터 시작하겠음
유니티 버전에 따라서 기능들이 없거나 못보던게 있긴 하겠지만 이 시스템의 구조가 바뀌는건 아니니까 당황할 필요없음



**Duration**
이 파티클 시스템의 총 지속시간
밑에 **Looping**를 체크했다면 N초마다 이 이펙트를 반복하게 할수있음
피격이펙트처럼 1회성 반짝연출이라면 **Looping**를 해제하고
계속 유지해야하는 오오라같은 버프효과나 배경오브젝트에 올릴 광원이나 비/눈같은것들은 **Looping**를 켜주면되겠지





![7cef8374b6836af53fed98a518d60403d1079006884bcd4b](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27791cfc686f767dfdfd08770cdcf963bc861944964168a444d8f63f6f2c90d503da884ca08ec635b9280ef735)**2**



*공통적으로 알아야 할 점은 파티클 시스템에서 오른쪽 끝 역삼각형 모양을 눌러서 나오는 옵션중 **Curve**임

**Duration**의 '남은 시간'동안 생성될 새 객체들에만 영향을 미친다는 부분이다



**Duration**이 1초라고 가정했을때 **StartSize**의 **Curve**모양을 1에서부터 0까지 도달하게 잡았을경우



<video autoplay="" loop="" muted="" playsinline="" onmousedown="mp4_overlay(this, 'https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d99ff339e2dd094ce82e1f2012');" data-src="https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d99ff339e2dd094ce82e1f2012" style="margin: 0px; padding: 0px; border: 0px; vertical-align: baseline; background: transparent; font-style: normal; max-width: 100%;"></video>

**3**



윗 짤처럼 서서히 작은 객체가 생성되게됨

달리 말하면 이펙트를 켜자마자 한번에 뿜어져 나오고 끝나는 단발성 이펙트라면 Curve값을 받지 않으니 표현하고자하는 상황을 잘 생각해야 한다는거


**StartDelay**
이펙트 시작시간에 딜레이를 줄수있음
단독 이펙트에 쓸일은 없음 서브로 사용할때 쓰게되는데 메인으로 보여질 이펙트보다 나중에 보여야할 필요성이 있을때 쓰게된다



<video autoplay="" loop="" muted="" playsinline="" onmousedown="mp4_overlay(this, 'https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9cbf53ab7895a1eeb44f0b75e');" data-src="https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9cbf53ab7895a1eeb44f0b75e" style="margin: 0px; padding: 0px; border: 0px; vertical-align: baseline; background: transparent; font-style: normal; max-width: 100%;"></video>

**4**



ex) N초간 기를 모은다음 터트리는 연출에서 터지는쪽 이펙트 / 검격의 마지막쯤에 뿌려질 작은 파티클들

**StartLifetime**
생성할 객체 하나하나의 지속시간
**Duration**와 동일한 값을 줘서 파티클 단 한장이 무한히 유지되게 만들수도있음



<video autoplay="" loop="" muted="" playsinline="" onmousedown="mp4_overlay(this, 'https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9cbfe3de18f581fe92ff8f19d');" data-src="https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9cbfe3de18f581fe92ff8f19d" style="margin: 0px; padding: 0px; border: 0px; vertical-align: baseline; background: transparent; font-style: normal; max-width: 100%;"></video>

**5**



다만 **Duration**과 **StartLifetime**이 동일할때 본인 프로젝트 설정에따라 교체될때 튀는현상이 발생할수 있으니 주의
멈추지않고 계속 유지해야하는 경우가 생기면 왠만하면 **StartLifetime**수치를 **Duration**의 두배값으로설정해주고



<video autoplay="" loop="" muted="" playsinline="" onmousedown="mp4_overlay(this, 'https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d99fff68e3d80c48e8507e8dca');" data-src="https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d99fff68e3d80c48e8507e8dca" style="margin: 0px; padding: 0px; border: 0px; vertical-align: baseline; background: transparent; font-style: normal; max-width: 100%;"></video>

**6**



나중에 설명할 **ColororOverLifetime**으로 실제로는 두장인데 한장처럼 보이게 설정하는게 좋음

**StartSpeed**
객체가 생성될때의 속도값을 설정할수있음 여기서 설정하는 수치는 XYZ 특정 방향의 값을 가진게 아님
나중에 설명할 **Shape**항목의 종류와 옵션 따라서 방사형이 될수도 직선이 될수도 있는 일종의 힘과 같다

**StartSize**
생성될때의 크기 값을 설정할수있고 상단의 **3DStartSize**를 체크하면 리소스를 ZYX축으로 늘리고 줄일수있게됨
나중에 언급하게 될지도 모르겠지만 파티클 시스템은 원본리소스의 비율따윈 신경쓰지 않는다



![viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6aade22382e4ddd5fba0b47e193597f6e367235c16e5ea2532475c7e4](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6aade22382e4ddd5fba0b47e193597f6e367235c16e5ea2532475c7e4)**7**



300x150해상도 텍스쳐를 파티클시스템에 넣으면 그냥 정사각형으로 찌부되서 올라온다는 소리임
때문에 텍스쳐 크기를 빈공간을 추가해서 300x300으로 수정해서 쓰던가 3D옵션으로 비율을 맞춰주는게 좋은데
리소스에 빈공간이 많을수록 내부적으론 그걸 다 계산하기 때문에 최적화에는 좋지않음

파티클 시스템으로 시퀀스애니메이션을 넣는게 아니라면 빈공간 최대한 없는 리소스를 쓰고 **3DStartSize**로 비율 맞춰라


**StartRotation**
오른쪽에 🔽을 눌러서 **Random Two Constants** 옵션 랜덤 범위값을 가장 많이 쓰게됨



<video autoplay="" loop="" muted="" playsinline="" onmousedown="mp4_overlay(this, 'https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9caa23fe4df5c4fb9ad881507');" data-src="https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9caa23fe4df5c4fb9ad881507" style="margin: 0px; padding: 0px; border: 0px; vertical-align: baseline; background: transparent; font-style: normal; max-width: 100%;"></video>

**8**



피격이펙트중 검흔모양을 360도 돌려가면서 랜덤으로 나오게하면 다단히트같이 반복해서 튀어나올때 타격감 살리기가 좋음

개인 팁이라면 360/-360말고 180/-180으로 잡아놔야 겹치는 경우를 더 줄일수있다
**StartSize**랑 동일하게 3D옵션을 체크해서 xzy축으로 돌릴수있음 색종이 같은걸 뿌릴때 켜주면 좋다
만약 파티클시스템에 이미지를 넣었는데 안보인다?
그러면 90도 돌아가있어서 짜되서 안보이던가 매쉬나 쉐이더에 twoface설정이 안되어있어서 뒷면이 보이고있는 상황일꺼다
이미지가 안보이는 상황에는 다른 경우도 있긴한데 그건 나중에 다룸

**StartColor**



![viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6aade22382e4ddd5fba0b47e193597f6e327765640fdd70dd9426e0d7](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6aade22382e4ddd5fba0b47e193597f6e327765640fdd70dd9426e0d7)**9**



이것또한 대부분 🔽으로 확장해서 **Random Two Color**를 쓰게될건데



![7cee8275b7836bf43fec84e458c12a3ae94c85ebc808d765368b5a](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27791cfc686f767dfdfd08770cdcf963bc861944964168a444d8f63f6f2c90d5038e8616b558455fa5ec946496)**10**



**Two Color**을 쓸경우 두 색의 중간지점 컬러값 또한 표현하기때문에 단순히 채도만 다르게 하는건 문제없는데
빨강+초록을 할경우 위처럼 중간의 똥색부분들도 나오게되어버림



![7cee8275b7836af53ff1c6bb11f11a39d35deb1109dfd5](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27791cfc686f767dfdfd08770cdcf963bc861944964168a444d8f63f6f2c90d503d4841ac1fd54c1d008ce765a)**11**



이때 **Random Color**를 선택하고 해당 **Fixed**모드를 사용해주면 위 짤처럼 깔끔하게 원하는 컬러들만 나오게끔 설정할수있음
**Gradient**의 경우 위에 설명한 **Curve**와 마찬가지로 한순간에 뿜어져 나오고 끝인 연출에는 쓸일 없다





**GravityModifier**
중력값
위나 아래로 점차 가중되는 속도 값을 줄수있음
파괴된 오브젝트가 떨어지거나 물방울이나 불똥이 날아올라가는 연출을 표현할때 쓰게됨



<video autoplay="" loop="" muted="" playsinline="" onmousedown="mp4_overlay(this, 'https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9cdf032ee8d5842e2e42f0195');" data-src="https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9cdf032ee8d5842e2e42f0195" style="margin: 0px; padding: 0px; border: 0px; vertical-align: baseline; background: transparent; font-style: normal; max-width: 100%;"></video>

**12**



나중에 설명할 **Collision**항목을 통해 바닥이나 특정 오브젝트에 튕기다가 멈추는 연출을 할때
이 값이 너무 크게 입력되어있다면 바닥에서 달달달 떨릴수도 있음
이 경우 **Collision**충돌시 생성하는 이펙트가 미친듯이 나오는 상황이 발생할수 있으니 주의



![viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6aade22382e4ddd5fba0b47e193597f6e32213804278a0cc28d0042b3](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6aade22382e4ddd5fba0b47e193597f6e32213804278a0cc28d0042b3)**13**





*추가로 주의할점은 **ProjectSettings**의 **Phtsics**에서 프로젝트 기본 중력값 세팅을 할수있는데
이 값에 따라서 파티클 시스템 중력값이 다르게 적용될수있음
에셋을 구매했는데 왜 나는 이상하게 보이지?의 범인이 이새끼 일수도 있다는거

**SimulationSpace**



![7cee8275b48069f53cec87e758c12a3a7fa183bf3158ec0b1b70](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27791cfc686f767dfdfd08770cdcf963bc861944964168a444d8f63f6f2c90d503d5891fb4eaface6017551886)**14**



**Local**은 이 파티클 시스템으로 생성한 객체가 상위노드의 이동값에 영향을 받는 상태를 말함
예를들면 눈의 안광이나 마법구의 글로우 이펙트들이 이에 해당됨 움직임을 따라가야하니까 반드시 로컬이어여함
**World**는 반대로 상위노드의 영향을 받지않는 객체를 말함



<video autoplay="" loop="" muted="" playsinline="" onmousedown="mp4_overlay(this, 'https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d998f26ee18d581eb8ff5a0203');" data-src="https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d998f26ee18d581eb8ff5a0203" style="margin: 0px; padding: 0px; border: 0px; vertical-align: baseline; background: transparent; font-style: normal; max-width: 100%;"></video>

**15**



예를들면 달릴때 발밑에 발생할 먼지나 들고있는 횟불의 불똥 이런것들
그런데 웃긴건 유니티가 좆꾸져서 원래는 영향 받으면 안되는 상위노드의 회전값이 충돌나는 경우가 생김
때문에 복잡한 움직임이 있는 곳에 파티클 시스템을 달게될거라면 이동값이 없게 잡아놔야 충돌을 방지할수 있다

**SimulationSpeed**
이 파티클 시스템의 전체 속도를 말함
2초동안 그려질 이펙트를 1초만에 보여주거나 4초동안 느리게 보여줄수있게하는 수치값임
유니티에서 가장 좆같은게 꼬리연출인데 아주 빠른 동작을 이 trail보고 따라가라고 하면 뚝뚝 끊어지고 각진 움직임을 가지게되는데
스무스한 움직임을 먼저 만들고 이 수치로 속도를 높여버리면 아주 깔끔한 속도감있는 꼬리 이펙트를 만들어낼수있음
ex) 용대가리 날리는 이펙트의 꼬리 or 기모을때 유저 주위를 회전하는 선들 or 레벨업 이펙트

**ScalingMode**



![7cee8277b68069f53cec87e747827673317d8ecf8c1f61236787e69d73](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27791cfc686f767dfdfd08770cdcf963bc861944964168a444d8f63f6f2c90d5038f864d108bdb34d99e673ec1)**16**



이 이펙트가 배치될 부모의 크기값에 영향을 받을꺼냐 말꺼냐를 정해주는 옵션
**Local** - 부모 크기가 0.0001배여도 좆까하고 원래 크기로나옴 주로 UI에 올릴 파티클을 만들때 쓰게됨
변수가 없다는건...비슷한 연출을 다른곳에도 넣어야 할때 비슷한걸 또 바리에이션을 치게된다는 말과 같음
**Hierarchy** - 부모 크기에 영향을 받아 확대 축소가 자동으로 됨
UI는 해상도별로 자동으로 스케일링 되기때문에 UI연출에 파티클을 쓰게된다면 해당 옵션을 쓰면 못생겨질수있음



<video autoplay="" loop="" muted="" playsinline="" onmousedown="mp4_overlay(this, 'https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9c7a73ee5885649ef97d8e58c');" data-src="https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9c7a73ee5885649ef97d8e58c" style="margin: 0px; padding: 0px; border: 0px; vertical-align: baseline; background: transparent; font-style: normal; max-width: 100%;"></video>

**17**



*위 짤처럼 부모의 크기에따라 객체의 크기도 함께 늘어나기 때문에 위처럼 표현할바에는 그냥 저렇게 생겨먹은 텍스쳐 한장을 만드는게 최적화 면에서 좋음

**Shape** - 나중에 다루게될 **Shape**만 부모의 크기값에 영향을 받고 객체의 크기는 유지함



<video autoplay="" loop="" muted="" playsinline="" onmousedown="mp4_overlay(this, 'https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d99dfe32b2dd5d4ee2e4a2db5f');" data-src="https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d99dfe32b2dd5d4ee2e4a2db5f" style="margin: 0px; padding: 0px; border: 0px; vertical-align: baseline; background: transparent; font-style: normal; max-width: 100%;"></video>

**18**



뱀서류에 많이 쓰이는 스킬 레벨이 높아질수록 범위가 증가하는이펙트들을 이 옵션을 사용하면 범위만 늘어나고 객체 크기는 유지되서 이쁘게 표현할 수 있게 됨
이펙트 하나로 부모 크기값만 레벨별로 키워 주면 그만이니까
다만 **Hierarchy**랑 다르게 생성된 순간에만 영향을 받기때문에 그점은 유의

에셋을 샀는데 이펙트가 이상하게 보인다? 십중팔구 **ScalingMode** 옵션때문임 에셋 상태가 안좋을경우 Position을 싹다 다시 잡아야 할수도있음


**MaxParticles**
이 파티클 시스템으로 생성할수있는 최대 객체수를 지정할수있음 최적화 한답시고 무조건 최소한으로 줄여놓는 사람들이 있는데 존나 상관없다 ㅋㅋ
이거를 최소한으로 설정하게될 상황은 나중에 다루게될 **SubEmiters**항목의 **Collision**옵션 때문일 확률이 높음
간단하게 설명하자면 **SubEmiters**는 부모 파티클의 각 상황별(생성/소멸/충돌등)로 서브 이펙트를 불러오는 기능인데
여기서 '충돌시'가 한번에 여러번 체크되서 존나게 뿜어져나오는 경우가 있기때문에 **Ma****xParticles**로 개수를 제한해 두어야 이쁘게 나옴

**AutoRandomSeed**
파티클 시스템은 🔽를 통해 수치값을 두개이상 입력한 모든 설정의 사이값을 랜덤으로 결정함
해당 옵션을 끄게되는 경우 **RandomSeed**를 입력할수있는 항목이 추가되는데
이 **Seed**를 통일한 파티클 시스템은 입력한 수치가 같은이상 항상 동일한 변수값을 가지게된다



<video autoplay="" loop="" muted="" playsinline="" onmousedown="mp4_overlay(this, 'https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9c7f53eb3de0b1ae804d39c23');" data-src="https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9c7f53eb3de0b1ae804d39c23" style="margin: 0px; padding: 0px; border: 0px; vertical-align: baseline; background: transparent; font-style: normal; max-width: 100%;"></video>

**19**

요렇게 지멋대로 나오던 애들을 시드만 통일해주면 같은 방향으로 보낼수 있게됨





<video autoplay="" loop="" muted="" playsinline="" onmousedown="mp4_overlay(this, 'https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9c8f068e0dd594fe2b0f24ace');" data-src="https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277913fc7dff14dca9920449a1c55bb6c6ee8d799d4bb50a26c358d9c8f068e0dd594fe2b0f24ace" style="margin: 0px; padding: 0px; border: 0px; vertical-align: baseline; background: transparent; font-style: normal; max-width: 100%;"></video>

**20**



요런 느낌으로 한쪽에만 **Size over Lifetime** 그래프를 추가해서 다채로운 표현을 만들어 낼수있다

파티클시스템의 기본시스템 설명은 이걸로 끝

다음 단계에서는 탭단위로 분류되어있는 각각의 항목으로 어떤 표현을 할수있나를 설명해주겠음
