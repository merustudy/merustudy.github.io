---
layout: default
title: renderer
nav_order: 105
parent: P(Dev)
grand_parent: Post(Dev)
---

# 이펙트 제작 초보자용 가이드#5 

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

* https://gall.dcinside.com/mgallery/board/view/?id=198234567890&no=15&page=2




초보자용 가이드의 마지막
파티클시스템의 가장 밑에있는 **Renderer** 항목에 대해 적어둠



![78e98373b0816cf33aea85e158c12a3a99e2679e9c27bc96bf7700](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781bfcf567bc09b418a85392cba6c8ce0305b79dcdbea11309be1d68bbafaa772908b8e0c8c2822c79cdae)**1**





![79e88473b0866cf53bea82e643827073154baa99d19866511e1081327a79](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781bfcf567bc09b418a85392cba6c8ce0305b79dcdbea11309be1d68bbafaa2c275eb9dd4d7b4718b3f3c3)**2**



이번 글 내용 대부분이 **RenderMode**별로 어떤 연출이 가능한지에 대한 이야기가 될거임





------




**BillBoard**
가장 기본이되는 모드로 리소스가 정면을 바라보게 해주는 모드임
사실상 파티클에 매쉬를 쓰고싶은게 아닌이상 이 모드로 전부 표현 가능



![79ee8572b0816cf53bee84e64480756fdb62d335b7c9fc6cda76993f82b48c2a](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781bfcf567bc09b418a85392cba6c8ce0305b79dcdbea11309be1d68bbafaa77265fec664e89f640ddd7af)**3**



**RanderAlignment** 타입에 따라서 어떤걸 정면으로 바라볼꺼냐를 선택할수있는데 어차피 두종류밖에 안씀



<video autoplay="" loop="" muted="" playsinline="" onmousedown="mp4_overlay(this, 'https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781bfcf567bc09b418a85392cba6c8ce4653edf692c345ee0a0b68619731b153817d1100d624');" data-src="https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781bfcf567bc09b418a85392cba6c8ce4653edf692c345ee0a0b68619731b153817d1100d624" style="margin: 0px; padding: 0px; border: 0px; vertical-align: baseline; background: transparent; font-style: normal; max-width: 100%;"></video>

**4**



**View**가 카메라를 정면으로 쳐다보는 옵션이라 3D처럼 보이게 할수있어서 기본옵션 이기도 하고 가장 많이쓰임 

**Local**은 부모를 포함한 모든 회전값을 그대로 표현하는거라 사실상 매쉬로 플랜을 사용할바에는 이 옵션을 로컬로 잡고 쓰는편

**Stretched Billboard**



![78e98570b3876cf03beb87e6449f343329e2fca42a43d2909c64bd](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781bfcf567bc09b418a85392cba6c8ce0305b79dcdbea11309be1d68bbafaa717a0ebacd56be1c6ed1a65c)**5**



리소스들의 중점을 강제로 이동방향 앞쪽으로 변경해주는 기능이라 이미지를 늘리고 줄일 수 있게됨



<video autoplay="" loop="" muted="" playsinline="" onmousedown="mp4_overlay(this, 'https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781bfcf567bc09b418a85392cba6c8ce4653edf692c345ee0a0b6b359e61b252867b11ee3afc');" data-src="https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781bfcf567bc09b418a85392cba6c8ce4653edf692c345ee0a0b6b359e61b252867b11ee3afc" style="margin: 0px; padding: 0px; border: 0px; vertical-align: baseline; background: transparent; font-style: normal; max-width: 100%;"></video>

**6**





<video autoplay="" loop="" muted="" playsinline="" onmousedown="mp4_overlay(this, 'https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781bfcf567bc09b418a85392cba6c8ce4653edf692c345ee0a0b3d30923ae155d77c1148bd10');" data-src="https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781bfcf567bc09b418a85392cba6c8ce4653edf692c345ee0a0b3d30923ae155d77c1148bd10" style="margin: 0px; padding: 0px; border: 0px; vertical-align: baseline; background: transparent; font-style: normal; max-width: 100%;"></video>

**7**



가장 보편적인 활용방법이 저 옵션 그대로 **StartSpeed**를 0.01 / -0.01 정도로잡아주고
여기에 **3D Start Size**로 비율을 강제로 늘려주면 위처럼 중심점 기준으로 퍼트릴수가 있게됨
이거를 **Size over Lifetime**으로 작아지거나 커지게 그래프를 잡아준 결과가 위 두 짤임





<video autoplay="" loop="" muted="" playsinline="" onmousedown="mp4_overlay(this, 'https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781bfcf567bc09b418a85392cba6c8ce4653edf692c345ee0a0b6060c637e207d27d114b70fe');" data-src="https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781bfcf567bc09b418a85392cba6c8ce4653edf692c345ee0a0b6060c637e207d27d114b70fe" style="margin: 0px; padding: 0px; border: 0px; vertical-align: baseline; background: transparent; font-style: normal; max-width: 100%;"></video>

**8**



또다른 사용법은 #3에서 다룬 가감속을 넣은 방사형 이펙트에



<video autoplay="" loop="" muted="" playsinline="" onmousedown="mp4_overlay(this, 'https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781bfcf567bc09b418a85392cba6c8ce4653edf692c345ee0a0b68649031ba53812d111373ac');" data-src="https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781bfcf567bc09b418a85392cba6c8ce4653edf692c345ee0a0b68649031ba53812d111373ac" style="margin: 0px; padding: 0px; border: 0px; vertical-align: baseline; background: transparent; font-style: normal; max-width: 100%;"></video>

**9**



**Stretched Billboard**의 **SpeedScale**값을 주면 속도에 따라서 슬라임처럼 늘어졌다가 작아지게 할수있음
피격 이펙트에 쓰게되면 찰진 효과를 만들수 있겠지? 개인적으로는 그냥 동그라미보단 사각형박스로 이런 표현을 하는게 이쁘더라

 
**Horizontal Billboard**



<video autoplay="" loop="" muted="" playsinline="" onmousedown="mp4_overlay(this, 'https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781bfcf567bc09b418a85392cba6c8ce4653edf692c345ee0a0b61309233b600db2811c51f1f');" data-src="https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781bfcf567bc09b418a85392cba6c8ce4653edf692c345ee0a0b61309233b600db2811c51f1f" style="margin: 0px; padding: 0px; border: 0px; vertical-align: baseline; background: transparent; font-style: normal; max-width: 100%;"></video>

**10**



달리 설명할것도 없이 무조건 바닥을 찍음
만약 카메라 각도가 0인 프로젝트를 하고있다면 아에 보이질 않을테니 조심 ㅋㅋㅋ
솔직히 일반 **BillBoard**의 **RanderAlignment** **- Local**을 쓰고 바닥 각도를 조절하면 그만이라 자주 쓰는 모드는 아님

**Mesh**
**BillBoard**다음으로 많이 쓰게될 랜더모드
원하는 모양의 매쉬를 등록해서 파티클 시스템으로 사용할수있음

애니메이션이랑 혼합해서 작업하는 경우도 있긴한데
스킬 연출을 하게될때 바닥에서 돌이나 얼음같은거 튀어나오면 싹다 이렇게 파티클시스템에 등록해서 사용하는거임
최적화 신경 안쓰는 프로젝트면 캐릭터나 배경오브젝트 모델링을 그대로 쓰기도 하는데
왠만하면 이펙트 전용으로 폴리곤수 최대한 줄이고 언맵또한 다시 펴서 사용하기도함

예시를 남겨주고 싶은데



<video autoplay="" loop="" muted="" playsinline="" onmousedown="mp4_overlay(this, 'https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781bfcf567bc09b418a85392cba6c8ce4653edf692c345ee0a0b6a34c461b55fd57d119478b1');" data-src="https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&amp;no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781bfcf567bc09b418a85392cba6c8ce4653edf692c345ee0a0b6a34c461b55fd57d119478b1" style="margin: 0px; padding: 0px; border: 0px; vertical-align: baseline; background: transparent; font-style: normal; max-width: 100%;"></video>

**11**



보통은 이렇게 쉐이더 그래프로 제작한 머테리얼과 함께 쓰기때문에
다음 컨셉의 가이드에서 다뤄보도록 하겠음



참고로 **RenderMode**들중 **~BillBoard**로 끝나는 애들은 **size**를 아무리 키워도 카메라에 보여지는 크기에 한계가 있는데



![7ee98275b1806bf23ceb82e6449f343395d24ca8a6fd971178c5e8](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781bfcf567bc09b418a85392cba6c8ce0305b79dcdbea11309be1d68bbafaa74275fb8bd00d2b49e359093)**12**



이거 꼭 늘려놔라
에셋 불러왔을때 이상하게 보이는 요인으로 이것도 한자리 차지함





------

초보자 가이드는 마무리하고
만들고 싶은거 과정과 함께 남기도록 하겠음
