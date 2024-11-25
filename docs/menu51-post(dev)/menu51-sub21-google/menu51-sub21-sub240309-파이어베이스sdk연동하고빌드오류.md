---
layout: default
title: 240309_파이어베이스sdk연동하고빌드오류
nav_order: 240309
parent: P(Google)
grand_parent: Post(Dev)
---

# 240309_파이어베이스sdk연동하고빌드오류

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

https://gall.dcinside.com/mgallery/board/view/?id=game_dev&no=154565



빌드 오류는 Gradle build faild 입니다



현재 유니티 버전은 2023.3.0b10이고 파이어베이스 sdk버전은 11.7.0 입니다



첫번째 오류 내용입니다



![a04424ad2c06782ab47e5a67ee91766dc28ff1ecd0acc5c1bf13d0c752d1d221dba88755c22e8b0f8d80ef491c1e](https://dcimg1.dcinside.com/viewimage.php?id=2abcdd23dad63db0&no=24b0d769e1d32ca73ce982fa11d02831d33053808284030ab34aa303b8a35c7f3508e8254dfecbcbe53097c8f4873a3c816f8a4ad70ed1526100085b72e86395a93a62)





두번째 오류 내용입니다



![a04424ad2c06782ab47e5a67ee91766dc28ff1ecd0acc5c1bf13d0c65bd1de213474a314cc619b7857a628b56357](https://dcimg1.dcinside.com/viewimage.php?id=2abcdd23dad63db0&no=24b0d769e1d32ca73ce982fa11d02831d33053808284030ab34aa303b8a35c7f3508e8254dfecbcbe53097c8f4873a3c816f8a4ad70ed15568530f5d21ba639530d1a6)







3일동안 이 문제 때문에 골머리를 썩히고 있습니다 제발 도와주십쇼 형님들 ㅠㅠ

단순히 감성팔이가 아닌 사례금 8만원 또한 드리겠습니다

제발 도와주세요!!! 8개월 동안 인디겜을 만들면서 그 동안의 시간이 수포로 날라가게 생겼습니다...









\-----------------------------------------------------------------------------------------------------------------



라라루라님이 해결해주셨습니다!

build setting할 때 xNet framework로 세팅되어 있는 상태에서

안드로이드 빌드를 할 경우 유니티에서 그에 맞는 Manifest와 custom gradle파일을 새로 만들게 됩니다

이런 파일들은 Assets -> Plugins -> Android안에 저장 되는데

여기에 저장된 위 파일들이 유니티에서 default로 설정된 gradle파일과 충돌하게됩니다

위 경로에 있는 파일들을 모두 지워주고

Publishing setting에서 Build탭에 체크된 항목들을 모두 제거해주고 빌드하닌까 성공했습니다

(빌드 도중에도 위 경로에 파일이 생성될 수 있는데 반드시 위 경로에 해당 파일들을 계속 지워주셔야되요)



- [화면 캡처 2024-03-09 234914.png](https://image.dcinside.com/download.php?no=24b0d769e1d32ca73ce982fa11d02831d33053808284030ab34aa303b8a35c7f3508e8254dfecbcba36ccca3f58d373ff8c283a41aa6196e244a29b20921b5&f_no=화면+캡처+2024-03-09+234914.png)
- [화면 캡처 2024-03-09 235018.png](https://image.dcinside.com/download.php?no=24b0d769e1d32ca73ce982fa11d02831d33053808284030ab34aa303b8a35c7f3508e8254dfecbcba36ccca3f58d373ff8c283a313f51e68771829b20921b5&f_no=화면+캡처+2024-03-09+235018.png)

## 

전체 댓글 *14*개

등록순

[본문 보기](https://gall.dcinside.com/mgallery/board/view/?id=game_dev&no=154565#container) **댓글닫기** 새로고침

- *라라루라* ![갤로그로 이동합니다.](https://nstatic.dcinside.com/dc/w/images/fix_nik.gif)

  구글 미트 링크 같은 거 함 주실래요? 함 아예 봐드릴게용

  03.10 00:03:38

  삭제

- - *글쓴 ㅇㅇ*(118.218)

    죄송합니다... 구글 미트를 사용해본 적이 없네요... 지금 한번 해보겠습니다

    03.10 00:05:53

    삭제

  - *라라루라* ![갤로그로 이동합니다.](https://nstatic.dcinside.com/dc/w/images/fix_nik.gif)

    화상 회의에 참여하려면 다음 링크를 클릭하세요. https://meet.google.com/ndq-quvr-kdn
    휴대전화로 참여하려면 +1 513-816-0844번호로 전화를 걸고 다음 PIN을 입력하세요. 202 242 385#
    이 링크 들어오세용

    03.10 00:07:39

    삭제

  - *라라루라* ![갤로그로 이동합니다.](https://nstatic.dcinside.com/dc/w/images/fix_nik.gif)

    갑자기 10분 정도 말씀 없으시면 해드릴 수 있는 게 없을 것 같아요...

    03.10 00:35:04

    삭제

  - *라라루라* ![갤로그로 이동합니다.](https://nstatic.dcinside.com/dc/w/images/fix_nik.gif)

    혹시 모르니 Unity 끈 상태에서 사용자 이름 내에서 존재하는 gradle cache 파일 삭제 해보시고 AppData 의 LocalLow 에 존재하는 해당 패키지 이름을 폴더 째로 삭제 시도 추천드립니다.

    03.10 00:35:51

    삭제

  - *글쓴 ㅇㅇ*(118.218)

    아 저 계속 기다리고 있었습니다! 알려주신 방법은 제가 이미 해봤는데 안돼네요 ㅠㅠ 도와주셔서 감사합니다

    03.10 00:36:47

    삭제

  - *라라루라* ![갤로그로 이동합니다.](https://nstatic.dcinside.com/dc/w/images/fix_nik.gif)

    혹시 사용하시는 미팅 툴 있으신가요? 제가 그쪽에 접속하거나 아예 통화로 하는 게 나을 것 같네요

    03.10 00:39:20

    삭제

  - 이 댓글은 게시물 작성자가 삭제하였습니다.

   

- *ㅇㅇ*(61.254)

  gradle 버전 낮아서 생긴 문제여서 유니티 버전 낮은건줄 알았는데 23버전쓰고 있네. 커스텀 gradle 버전 쓰고 있거나 런쳐 파일 건드린 적 없음?

  03.10 00:38:25

  삭제

- - *글쓴 ㅇㅇ*(118.218)

    문제 해결하려고 건드렸다가 프로젝트를 다시 만들긴 했습니다

    03.10 00:39:40

    삭제

  - *ㅇㅇ*(61.254)

    2023.3 버전은 기본적으로 제공되는 gradle 버전이 8.4인데 7.2로 인식하고 있는건 wrapper나 launcher 매니페스트나 external tool인가 어디선가 gradle 버전 바꿔놓은게 적용이 안된거 같은데 위에서 도와줬는데 해결 안 되면 gradle 빌드 버전 적용되는거 확인해봐

    03.10 00:48:23

    삭제

  - *글쓴 ㅇㅇ*(118.218)

    문제 해결되었습니다! 조언 주셔서 감사합니다

    03.10 03:23:43

    삭제

- *길가는인붕이*(211.229)

  지옥길에 들어선것을 환영한다...
  파베 sdk가 버그가 많기로 유명하고, 너무 커서 다른 sdk들과 충돌이 잘 남.
  난 2년 서비스 하고 짜증나서 파베는 떼버렸음.
  특히 광고 sdk들과 충돌이 너무 많이 나는데, 잘 찾아보면 맞는 버전 궁합이 있을 것 같긴한데, 그거 찾는게 1주씩 걸리기 예사임.
  (sdk들 마다 최근 2년간 버전이 6개 정도씩 있다고 하면, sdk를 6개 정도 쓴다면 6^6 만큼의 경우의 수가 생기고, 그걸 또 안드로이드와 ios 양쪽에서 빌드 성공해야 하는데다, 이렇게 맞춰놓은 궁합이 유니티 버전 오르면 또 다시 찾아야 한다는게...)

  03.10 11:03:17

  삭제

- - *ㅇㅇ\*1**(180.230)

    파베 안쓰면 백엔드서비스로 뭐씀
