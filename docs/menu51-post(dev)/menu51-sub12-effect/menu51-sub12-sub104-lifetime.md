---
layout: default
title: lifetime
nav_order: 104
parent: P(Dev)
grand_parent: Post(Dev)
---

# 이펙트 제작 초보자용 가이드#4 ~over Lifetime

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

* https://gall.dcinside.com/mgallery/board/view/?id=198234567890&no=5&page=2




파티클 시스템의 모든 옵션을 설명하진 않을거임
이펙트는 결국 어떤 기능을 어떻게 써먹든 남들이 보기에 결과물만 비슷하면 아무 상관이 없거든
그런 의미에서 파티클 시스템에는 잉여 기능들이 많다고 볼수있음



![7eef8175b4816af53fed85e7479f34339a6d1973851c1a19ba861ff2](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68af53988c3ef0b109e7f832d9758fe5aaf54f59b6393dd6a58944a4e)**1**



이렇게 **over Lifetime**로 분류되어있는 기능들중 밑줄 친것만 다룰줄 알아도 이펙트 제작에 아무 지장이 없다는 말임
딱봐도 알겠지만 각각 생성될 객체들의 이동/색상/크기/회전 값을 담당하는곳이고
이동관련된 **Velocity over Lifetime**을 제외한 나머지는 특별한 조작 노하우랄게 없을정도로 1차원적인 기능들을 가지고있음





![7eef8175b7836bf73cee85e747827673b75775013ff96339af6d61dba567a7](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68ab06fd2a7cc2cf8a2aba8aca474f023a3ea9b390bcf1a)**2**



**Cone**를 이용한 기본 방사형 상태에



![7eec8275b48069f43dee85e745806a3a20764508049a9c6cb9ab50c3d40d](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68ab06fd2a7cc2cf8a2aba8a9a673f071a4ba9a39533bb1)**3**





![7eec8275b7836af53fec87e74482756f8d5b0980c972a354f11037d93f0f7920](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68af53988c3ef0b109e7f832d9758fe5aa101f5c4a70f047f1700fb44)**4**



**Color over Lifetime**을 이렇게 만져서 파티클의 생성과 소멸을 부드럽게 만들수있고



![7fec8377b7836af73cee84fb06df231d05535425f9421a5593](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68af53988c3ef0b109e7f832d9758fe5aa952f69991aab91e07ed193b)**5**



컬러 변화를 줄수도 있음
가장 많이 쓰는게 노랑-빨강-검정으로 변화하는 불똥이겠지?





![7eec8275b48069f43dee84e6478377730ab15cd61d36fbe02a6be7903ec77a](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68ab06fd2a7cc2cf8a2aba8fca620a976a2e8cd394286ca)**6**





![7fee8175b4836af73cec87e444826a2d07344fce5c54a0662c1ee94dc1](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68af53988c3ef0b109e7f832d9758fe5aa803a7c458a676c40f31a90e)**7**



**Size over Lifetime**을 통해 객체가 지속시간동안 보여질 크기 그래프를 잡을수있음
**Separate Axes**를 체크하면 **#1**에서 알려줫던것처럼 오브젝트의 XYZ크기를 따로 잡을수있게됨
역삼각형모양으로 두개를 잡아서 랜덤성을 부여해도 좋겠지





![7eec8277b78169f43cec87e658d62d3bc864214a7a59bb92d4048d](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68ab06fd2a7cc2cf8a2aba8a8a277ae76f4b8903915783f)**8**





![7cef8277b6836af53fec84e444826a2df78f559717afa8d9265c3e90bc](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68af53988c3ef0b109e7f832d9758fe5aae57f39e5247a71d3a3aa1f1)**9**



**Roation over Lifetime**에 그냥 수치만 입력해서 사라질때까지 계속 회전하게 할수도 있지만
위처럼 그래프를 잡아서 가감속을 넣을수 있음

너무 1차원적인 기능들이라 크게 설명할건 없으니 넘어가고





------





![7fec8377b78169f43dee84e64480756e33d25765ed2344e9d9b845e4b7df37](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68af53988c3ef0b109e7f832d9758fe5aff05f5cbddf0add4b3c31663)**10**





![7cef8377b7816bf53fed85e7478276731d852151a44b8c8f3b3a3471a1](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68af53988c3ef0b109e7f832d9758fe5aa153a3c9541dbb094d3dea05)**11**



움직임을 담당하는 이 **Velocity over Lifetime** 기능과 바로 밑에있는 **Limit Velocity over Lifetime**를 설명하는것으로 마무리 하려고함
이번 글에 이어서 다음 **Renderer**관련된 가이드가 초보자용 마지막 글이 될듯





------




**Linear**
**#1**에서 설정했던 **S****tart Speed**가 그저 '밀고 당기는 힘'이었다면
여기에 입력하는 수치는 말그대로 XYZ방향으로 움직이게 만드는거라 훨씬 직관적인 움직임을 만들어 낼수있음
이것도 마찬가지로 역삼각형 모양을 눌러서 그래프 형태로 바꾸거나 값을 두개입력해서 랜덤값을 부여하는게 가능함



![7eec8275b78369f43dee84e7449f233442367e0162c9612d52ae23aa](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68ab06fd2a7cc2cf8a2aba8ada62ef824a5b8ce3967c553)**12**





![7fec8277b6806bf73dee84fb06df231db3f73616e69419f5d7](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68af53988c3ef0b109e7f832d9758fe5af857a1cb39b5ce8a2f360006)**13**





![7eec8374b68069f53fed87e658d62d3b64f814f6dafbed2396cdace6](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68ab06fd2a7cc2cf8a2aba8abf072ab20a4ba903928c074)**14**





![7cef8374b4816af73fec84e44583756f9dbed380b8b127bca703bc75938b96a3](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68af53988ae820a1b957c85239e519963ae56a9c5cb782c2b984cdb)**15**



이 그래프를 활용해서 다양한 표현이 가능한데
복잡한 움직임은 애니메이션 키로 잡는게 좋지만 간단한 애니메이션들은 이 그래프로 때워버리는게 더 편리함

**Space**
여기서 설정한 움직임이 부모 영향을 받을꺼냐는 선택지임
**Local**은 부모의 방향에따라 이녀석의 이동 방향또한 변함 주로 총기에서 총구의 정면으로 나가야하는 탄알/파편등에 쓰이겠지?
**World**는 부모 방향에 상관없이 여기서 설정한 값대로 이동함 무조건 위쪽으로 움직여야하는 불꽃이나 먼지들은 당연하게도 World를 쓰게된다

**Orbital**
각 방향 축을 기준으로 돌리는 옵션이라고 생각하면됨
옥수수에 막대를 꼽아서 막대를 돌린다고 생각하면 편함 그러면 중심축은 가만히 있는데 그 축에서 멀리 떨어져있을수록 운동량이 많아지고
축을 기준으로 돌리기때문에 되돌아오는 움직임을 만들수 있음



![7eec8275b7836af53cee84e658d62d3b5715d6cdf22d9a126c63fce1](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68ab06fd2a7cc2cf8a2aba8aafe70a974f9e89c39c4fb30)**16**





![79eb8670b39c28a8699fe8b115ef0465063269](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68af53988c3ef0b109e7f832d9758fe5aaa53f3cd7f08c4cdfa2a93a8)**17**



방사형태의 연출에 Z축 궤도값을 주면 이렇게 날아갔다가 다시 뭉치는 움직임을 잡을수있고



![7ee98374b1836af53fed98b21fd70403d6d75681a5d79205636b](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68ab06fd2a7cc2cf8a2aba8aef220ad2ff7ef9a395c0775)**18**





![79ee8472b6836af43fee84fb06df231d25ddf275ac91e6e812](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68af53988c3ef0b109e7f832d9758fe5aaa5ff49ebf69b6f52fdbd7d6)**19**



**#3**에서 다뤗던 기울기값 0의 **Cone**모양은 이렇게 Y축 회전값을 그래프작업없이 깔끔하게 넣을수있음
여기에 **Trails**만 달아도



![7cea8377b5876bf537e998b21fd704030cf260953d74a4035aa5](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68ab06fd2a7cc2cf8a2aba8faf725fb20a2e8c9395cf9a5)**20**



이런 이펙트로 조합해 낼수가 있게됨
다른 기능들과 **동일하게 역삼각형 눌러서 Curve를 줄수있어서 변칙적인 회전값을 주는것도 가능함**

**Offest**
위가 막대꼽은 옥수수라면 이거는 그 옥수수의 크기를 해당 방향으로 늘릴때쓰는 옵션임
대부분의 이펙트가 0.0.0좌표로 중심에 놓고 작업하게 되는데 이 옵션을쓰면 그걸 벗어나는 움직임을 가지기때문에
아무래도 안쓰게 되는 옵션중 하나

**Redial**
중요한 옵션으로 오브젝트들을 이동방향 기준으로 방사형으로 더 퍼지게 만들거나 모이게 만들어준다



![79ee8275b1806bf23ceb85e745827669abc90116800ef466bbccf2c55d43931fec](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68ab06fd2a7cc2cf8a2aba8a7a226fd71f6bc9e3989c6ba)**21**





![7eef8374b48069f43dec87e74783777320f32463b21286509269682b65](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68af53988c3ef0b109e7f832d9758fe5aa902a3caaa8a746f680944a4)**22**



**#3**에서 다뤘던 방사형 이펙트를 **Shape** 형태와 상관없이 만들수 있게 해주는 항목임

**Speed Modifier**
이 기능은 오로지 **Velocity over Lifetime**에 입련해둔 수치만 영향을 주는 옵션으로 마이너스 값을 주면 여기에 입력한 모든수치가 반대로 적용된다



![79ee8272b6866bf43aed85e742826a3acc18165d88eb3912af208e78880a1a](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68ab06fd2a7cc2cf8a2aba8fcfe26f076f1e89b393b748c)**23**







![79ee8275b1806bf23ced85e1458577693d5f06a0921feb74221a9741d9609d](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68af53988c3ef0b109e7f832d9758fe5aac55a19b87e076edcf14dd6f)**24**



**Curver**값을 줘서 움직임을 멈추게 할수도 빠르게 할수도 있기때문에 가감속 효과를 이걸로 때우기도함
포탈같은곳의 파티클을 만들때 쓰면 이쁜 외곽선이 만들어지겠지?





------





![7cef8377b7816bf53fed85e7478276731d852151a44b8c8f3b3a3471a1](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68af53988c3ef0b109e7f832d9758fe5aa153a3c9541dbb094d3dea05)**25**

마지막으로 **Limit Velocity over Lifetime**은
해당 파티클 시스템의 속도에 제한을 둬서 가감속 연출을 좀 더 디테일하게 잡을수 있게끔 해주는 기능임
위에 **Speed Modifier**로 낼수있는 느낌은 한계가 있기 때문에 주로 탄환이나 피격이펙트들을 표현할때 반드시 쓰게된다

**Speed**
속도 영향받을 범위값으로 수치가 높을수록 감속영향이 덜해짐
위에있는 **SeparateAxes**를 체크하게되면 다른 기능들처럼 XYZ방향으로 눈에 안보이는 한계점을 주무를 수 있음
밑에 달린 **Dampen**값이 높을수록 속도가 멈추는 타이밍이 빨라지고 입력되어 있지 않다면 아무런 영향도 안줌





![7fe98372b6806bf23cee84e4449f2334058205c50dbe615611d165e6abf2ca](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68ab06fd2a7cc2cf8a2aba8aff270fc21f3bf9a39ff0d39)**26**



여기까지 알게된 기능들만 가지고도 충분히 유니티 파티클의 모든 작업물을 따라할수있음

**Drag**
가감속이 아니라 시작 속도값에 제한을 주는 기능임
하위 **Multiply by Size**를 체크해주면 기본 옵션에 추가로 파티클 크기가 클수록 속도가 많이 줄게되고
**Multiply by Velocity**를 체크해주면 속도가 빠를수록 속도가 많이 줄게된다



![79ee8272b6806af53aed85e158d62d3b4ce407c2d84e19df4ae11116](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef277912fcf01bd39791008f861004eba68ab06fd2a7cc2cf8a2aba8fffe77f125f1b8ca3926080a)**27**



이렇게 작은 개체가 더 앞으로날아가고 최대/최소속도를 알맞게 제한해주는 기능이라
샷건이펙트나 피가 튀길때 쓰면 안성맞춤임





------




여태까지 설명한것들을 기본적으로 활용할줄 알아야
설명을 미뤄둔 **Collision / SubEmitter / Noise / Trails / CustomData**들을 가지고 더 이쁜 이펙트들을 만들수 있다
