---
layout: default
title: 220407_후기여러가지뇌피셜및뻘팁공유
nav_order: 220407
parent: P(Business)
grand_parent: Post(Dev)


---

# 여러가지 뇌피셜 및 뻘팁 공유

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

* https://gall.dcinside.com/mgallery/board/view/?id=game_dev&no=92025

다들 개발 열심히 하고 있음? ㅋㅋ

오랜만에 글 쓰는 것 같네





![25b8d122e0c007f420afd8b236ef203eebc4c793dadc12cc](https://dcimg1.dcinside.com/viewimage.php?id=2abcdd23dad63db0&no=24b0d769e1d32ca73ceb80fa11d02831059536d4b68a267ab9cc7d54528ce77dfd85c3bab7900d3d36f67a9f3f652949d25dd20169f183b5215bc6d8ed0705cf2893)







작년에 골드 렌더 매니저 출시하고 나서 열심히 운영하고 업데이트 개발도 하고 있음.

요즘은 해외 출시 준비를 달리고 있다.



**[다운로드 링크](https://play.google.com/store/apps/details?id=com.quaintree.goldlendermanager)**







문서 작업하면서 정리하다가 공유하면 괜찮을 것 같아서 공유하려고 함.

뭐 대부분 아는 사람도 있을 거고 어려운 내용은 아니라서 필요한 사람만 보면 될 듯



**1. 보안 관련**

**
**

**메모리 변조 방지 및 탐지 Anti-Cheat ToolKit**

https://assetstore.unity.com/packages/tools/utilities/anti-cheat-toolkit-2021-202695



많이들 사용하는 강력한 툴이다.

Cheat-Detector로 치팅 유저의 정보를 서버로 전송하고 강종 시키거나 세이브 데이터 삭제 등을 할 수 있음.

처벌 방식은 뭐 본인이 원하는 대로 하면 됨.



RandomizeCryptoKey 함수를 잘 사용하면 좋다.



곧 에셋 스토어 봄 세일이니까 장만하는 것을 추천









**루팅 탐지 참고글**

https://lhamed.github.io/57th-post/



예전에 신입 때는 안드로이드 네이티브로 jar 파일 플러그인 만들고 똥꼬쇼 했는데, 지금은 유니티에서 바로 됨.

보통 게임 가디언같은 툴은 루팅 환경에서 작동하기 때문에

루팅 기기 체크해서 게임 실행 막으면 치팅 유저가 대부분 줄어든다.





가상 머신을 이용해서 시도하는 경우는 위의 Cheat-Detector로 또 걸러주자









**시간 제어**

이거는 뭐 Playfab 쓰면 서버에서 받으면 되고,

서버가 없으면 **'유니티 인터넷 시간 가져오기'** 로 검색해서 찾아서 쓰자.



시간 관련 컨텐츠에서 흔히 시도 하는 치팅 방식이 기기의 로컬 시간을 변경하는 건데,

게임 시작 시 인터넷 시간을 가져온 후 DateTime 의 AddSeconds 함수에

Time.realtimeSinceStartup을 넣으면 현재 시간을 가져 올 수 있다.

불안하면 필요할 때 갱신 해도 됨.









**스토어가 아닌 유출된 APK에 대한 팁**

일단 출시하면 각종 사이트에 우리의 게임 APK가 널부러져 있다.

간혹 Mod APK도 있는데 확인은 안 해봄 ㅋㅋ



유니티에서 Application.installerName을 호출 했을 때, 구글 스토어에서 받았다면 "com.android.vending"을 뱉는다.

조건문으로 체크해서 값이 다르면 Application.Quit() 으로 강종 해주자





구글 플레이 로그인 시에 구글 스토어가 아니면 로그인하지 못하게 하는 기능이 개발자 콘솔에 있다.

그냥 체크만 하면 되었던 걸로 기억함. 체크해주자.









**게스트 로그인**

내가 알기론 애플은 게스트 로그인이 필수지만, 구글은 필수가 아니다.



게스트 로그인은 좋은 기능이지만, 주로 치팅 유저들의 창구로 악용된다 ㅋㅋ



그래서 기능은 있지만 AOS에서는 제거했고, 에디터나 IOS 환경에서만 나오게 변경했음.



구글 플레이 품질 체크리스트를 확인 하면 게스트 로그인이 필수라는 이야기는 없다.

1.5의 필수 사항에 로그인 거부에 대한 이야기가 있지만,

예외 사항에서 보듯 서버에서 정보를 받는 경우라면 없어도 될 것 같다.



품질 체크리스트



https://developers.google.com/games/services/checklist?hl=ko









**2. 무료 소스**

**
**

**NHN이 제공 하는 게임 기반용 무료 코드**

https://github.com/nhn/gpm.unity



웹뷰, 통신 프레임워크, 무한 스크롤 등 좋은 기능이 많다









**NGUI Tween을 uGUI로 구현한 무료 코드**

https://github.com/tomtc123/ugui-Tween-Tool



DoTween이라는 저렴하고 강력한 도구가 있긴 하지만 NGUI Tween 익숙하다면 이것도 쓸만함.

Deprecated 된 기능이 있는데 RichText 관련이라 딱히 사용은 안 해서 적당히 주석 처리해서 쓰면 됨









**플랫포머 기능 참고용 코드**

https://github.com/akashenen/2d-platformer-controller



플랫 포머에 있는 많은 기능들이 구현되어 있다.

나도 아직 코드 읽어보진 않았는데 괜찮을 것 같아서 공유해봄.



참고로 난 던전 서커스 이후로 플랫 포머 만들 생각 싹 사라짐 ㅋㅋㅋ











**슬더스 맵 구현 코드**

https://github.com/silverua/slay-the-spire-map-in-unity



이거도 사실 읽어보진 않음 ㅋㅋ 참고용으로 좋을 것 같다.



DoTween이 있어야 작동하는 것으로 보임.









**3. 마케팅**



나도 마케팅은 아직 초보긴 하지만 그래도 참고할 만한 정보들이다.

특정 국가를 타겟으로 잡고 마케팅을 진행하도록 하자.



간혹 보면 인도, 파키스탄, 동남아 이런 국가에 뿌리는 사람들 있는데, 허공에 돈 뿌리지 말자.



**마케팅 티어 정보**

https://phillipoh.tistory.com/33







**CPA 참고용 정보**

https://www.i-boss.co.kr/ab-6141-55967







**LTV 계산 및 정보**

https://brunch.co.kr/@parkkyunga/8







**분기 기준 국가 및 플랫폼 별 광고 eCPM 정보**

https://appodeal.com/blog/mobile-ecpm-report-app-ad-monetization-worldwide-performance/









**4. 빌드 검토 관련**



이거는 진짜 뇌피셜인데 빌드 검토를 빠르게 하는(?) 팁임.

일단 대부분 시도했을 때 한 번 빼고는 잘 작동했었다.



일단 기본은 관리형 게시임.



내부테스트 빌드로 먼저 올려서 간단하게 테스트 하고,

일정 시간이 지나면 사전 출시 보고서가 도착함.

대략 6~8시간 정도였던 듯?



그 상태에서 빌드 승급으로 프로덕션 올려버리면 1시간 이내에 검토 통과하더라.

이거는 뭐 뇌피셜 팁이라 혹시 궁금하면 해봐

검토 오래 걸린 경우는 딱 한 번이었음



\--------------------------------------------------------------------------------------------------









어쩌다 보니 인디 개발 시작한 지 2년이 되어버렸는데 ㅋㅋ

그래도 회사에서 작업하는 것보다 맘도 편하고 재미도 있다.



아직 많이 부족하지만, 지난 2년 동안 정말 많이 성장한 것 같다.

당장은 차기 프로젝트 시작 할 수는 없지만,

앞으로 더 잘 만들 수 있겠다는 자신감은 생긴 것 같음.



다들 잘 되길 바라고 조금이라도 도움이 되었으면 좋겠다.

건강 잘 챙기고 좋은 하루 돼라~
