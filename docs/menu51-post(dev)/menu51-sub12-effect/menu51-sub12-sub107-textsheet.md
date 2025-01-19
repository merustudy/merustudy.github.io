---
layout: default
title: textsheet
nav_order: 107
parent: P(Dev)
grand_parent: Post(Dev)
---

# 파티클시스템 가이드 ( Texture Sheet Animation )

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

* https://gall.dcinside.com/mgallery/board/view/?id=198234567890&no=17&page=2



https://gall.dcinside.com/mgallery/board/view/?id=198234567890

리소스 만드는법은 상단 링크 확인





------




이전 글에서 리소스는 만들었으니
이제 시퀀스 애니메이션을 파티클 시스템에 적용하는 방법을 알아보자





![79ee8372b7816cf43fed85e44482776f0c8a2ee0227544defbcbabbc4dc1d085](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc652354c6c5847274559ef581284b7f0b766ed2265ef6c43a33)**1**



우선 만들어둔 PNG를 넣어줄 머테리얼을 만들어줘야함
이 머테리얼을 어떤 속성으로 만드느냐는 그냥 개인 취향이자 최적화의 영역인데
대부분은 쉐이더그래프로 직접 짠 쉐이더들을 쓰게될거임





![78e98573b1836af73cec98a518d6040323b67187ceec13634d](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc652354c6c5847274559ef581284f2955473584570be632ee65)**2**



기초적인 가이드를 하고있는거니까 어디에든 있는 옵션으로 가자
Mobile/Particles/Additive
만들고 Select 눌러서 원하는 텍스쳐 찾아서 넣거나 드래그해서 넣어주면됨





![79ee8377b7816af73ded98a518d604032125aa0010395f033c](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc652354c6c5847274559ef581281d7f52fb755358e83000f690)**3**



파티클 시스템을 불러온다음





![79ec8275b7836bf73cec98a518d60403ba27b06e5396244bfe](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc652354c6c5847274559ef58128487f0023b4666cdfa9e41e19)**4**



머테리얼을 박아주고





![79ec8374b6836af520afd8b236ef203ea6493a3b271a11](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc652354c6c5847274559ef581281d79079c8dbc24cd8e520be6)**5**



Texture Sheet Animation을 켜주고
원래 계획한것처럼 가로 8 / 세로 2의 값을 넣어주면 세팅은 끝남







![79e88373b68669f43dee84e6478377738b5ef7cbb96780f71f41ce73cc44](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc652354c6c5847274559ef58128487f06e2db57eebe4b2f31b8)**6**



초보자 가이드 #1에서 설명했던것처럼

파티클 시스템은 무조건 정사각형을 표현하기때문에 쥰내 짜그러져서 나올텐데
3D Start Size를 체크해준다음
원하는 비율로 나올때까지 늘이고 줄여주면된다
Start Speed는 어차피 안쓰니까 0으로 만들고
Start Lifetime가 길수록 시퀀스 애니메이션의 다음프레임 교체 시기가 느려지니까 적당히 짧게 만들어주자





![79ee8477b7816af73cee85fb06df231dc049cc69c43f1fecfe9b](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc652354c6c5847274559ef581281f2d52bb1af6b0e7df6c3473)**7**



번개 특성상 이 이펙트를 켜자마자 발동되어야 하니까
Rate over Time는 없에버리고
Bursts를 추가해서 생성값을 잡아주고

Shape는 꺼두어도 좋지만 나중에 재미있게 뿌려볼수 있으니 최소값으로 냅두면됨





![7ee98274b68669f43dee84e644826a3ae60e656d5f9b8badf4a436f049bb](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d5d2d87260bf2a25baeed101290b04f24ff74e33846fea6)**8**



그러면 이렇게 깔끔한 번개효과 도출이 가능해진다
해상도가 많이 깨지긴하지?
꼬우면 해상도 크기를 512x512쓰던지 프레임수를 줄이는 방법말곤 없음

이제 여기에 바닥에 찍힐때 뿌려줄 파티클과
야매 광원효과를 올려주면



![7ee88575b4806bf73cec98b21fd70403ce73a1eeae7cb17383e3](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d5d2d87260bf2a25baeed101297b41c71ac75e5591232bf)**9**



GifCam의 한계다ㅋㅋㅋ

여튼 번개를 서브해줄 이펙트들은



![7ee98174b6836af53fed85fb06df231dfa101e2bd50cdb3e6963](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc652354c6c5847274559ef581284b290b3bdcd5633604c49072)**10**



이렇게 Sub Emiters로 같이 생성되도록 묶어놨는데
이렇게 작업해두면





![79ee8274b1816af23dee84e6448077738f3675947f0d6c5376037075d496b069](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d5d2d87260bf2a25baeed1043c4e71873a822e40aeddd24)**11**



요런 지랄을 할수가 있게됨
아까 Shape을 안꺼둔 이유임 생성범위 늘리고 여러개 생성되게 값만 추가해도 이렇게 표현할 수 있다





![7cef8374b48069f53cee85fb11d8221d7568e6ceff7aaa3f7c878f](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d5d2d87260bf2a25baeed1014c6b71874ff23b133e85681)**12**



물론 초보자 가이드#5 에서 설명해준 것처럼

![7ee88475b1836bf43ff1d1bc10f11a39de9b7d44276d42c2d5ee](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d5d2d87260bf2a25baeed101791b54176ff26b0a47b0065)**13**

Stretched Billboard를 이용해서 이런형태의 번개 이펙트도 제작 가능함
특히 Stretched Billboard를 사용하는 방식이 리소스의 중점을 처음이나 끝으로 변경 가능하기때문에
타격지점을 정확하게 만들어줄수 있는 방식인데





![79ee8174b68069f43dee87e7459f3433aff1f02189a365d1d0f53046](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc652354c6c5847274559ef581284d7805b8022ab7deefdde266)**14**



단점이 리소스를 돌려서 써야함 이 랜더모드는 텍스쳐를 항상 왼쪽이나 오른쪽으로 눕혀진 리소스들만 활용 가능하다

기존에 쓰던걸 단순하게 돌려서 사용해봤자 리소스 순서가 달라져서 위처럼 지랄떠는 느낌의 움직임으로 변해버림

처음부터 Stretched Billboard모드로 만들 생각하고 리소스를 배치해야 한다는 이야기임


어쨌든 이번 글에서 잠깐 나온 Sub Emiters로는 다양한 연출이 가능하니까 다음에 한번 다뤄보겠음
