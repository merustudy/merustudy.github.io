---
layout: default
title: resource
nav_order: 106
parent: P(Dev)
grand_parent: Post(Dev)
---

# 파티클시스템 전용 시퀀스 텍스쳐 만들기 (포샵&에펙)

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

* https://gall.dcinside.com/mgallery/board/view/?id=198234567890&no=16&page=2




드로잉할 실력이 안된다면 돚거할 래퍼런스부터 체크
원하는 리소스 네이밍 뒤에 Sprite Animation만 붙여서 검색하면 왠만한건 다 나온다
이 게시글은 그냥 튜토리얼 목적이라 이러는거지 진짜 게임에 쓸꺼면 라이선스 잘 확인해서 사용하던지
유튜브에 에프터이펙트같은걸로 리소스 만드는 튜토리얼 따라해서 만들어 내는수밖에 없음
인디게임단에서 가장 편한건 걍 직접 그리는거지 레퍼런스 보면서 리소스 찍는건 쉽잖아?

일단 가장 만만한 번개 이펙트에 도전해보자
Lightning Sprite Animation로 검색



![7eef8174b6836af53fec84e445836a2de5aa52812f1448cc87edc2afea55](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781afc7cf51deeb5fa90b6e8e1b740494dc63cd828420f23e5349ca35afd756ef13fd2997635d28f007697)**1**



적당히 마음에 드는걸 골라보자
이왕이면 중점이 다 맞춰져서 재생되는 GIF나 영상이 나이스임
이미 다 쪼개져있는 리소스의 경우 중심점을 하나하나 맞춰줘야해서 초보자는 심하게 번거로울수있음
검색방식을 GIF로만 검색해보는것도 좋은 방법





![7fb9d37fb0d66bf36ce781b042d7206e15507c5bb47e534df7dfe54dfd4408775645994a32dfb6b5e2e9ccfb9077922b](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781afc7cf51deeb5fa90b6e8e1b74049099567ca17a536b17293aad2b25c9da67d953b887f9e84)**2**



이게 찜쪄먹기 편해보인다

에프터 이펙트를 켜자



![78eb8570b0846df020afd8b236ef203e0a7e5cda387de9](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781afc7cf51deeb5fa90b6e8e1b740494dc63cd828420f23e5349ca35afd756ea331d0a333c3a6ba5d4a37)**3**



박스친곳에 다운받은 파일을 끌어다 넣으면됨



![7cef8377b6806bf43fed87e6478377733fe57e417f42136f893330ffec8edd](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781afc7cf51deeb5fa90b6e8e1b740494dc63cd828420f23e5349ca35afd7569f13583e1d02c77350d0f45)**4**



등록한 GIF던 PNG던 영상이든 여기다가 끌어와



![7ee88373b6876bf33dea83fb06df231db85dc315a793eb107cf32c](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781afc7cf51deeb5fa90b6e8e1b740494dc63cd828420f23e5349ca35afd753cf161805220cdbcb6c6c317)**5**



저쪽창에다 우클릭해서 Knoll UnMult를 찾아서 적용하셈
Knoll UnMult 플러그인은 영상이든 뭐든 검은색을 지워주는 기능이고 이펙트 뿐만아니라 걍 존나 유용하고 좋은 기능임
따로 설치해줘야하는데 구글에 검색하면 다운로드랑 튜토리얼 널려있음 무료이고 불법도아님 국민 플러그인이라고 보면됨





![7eec8275b7816af73cec84e64783776c73a827e056e0284f255fad3a59ec78ec58](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781afc7cf51deeb5fa90b6e8e1b74049099567ca17a536b17293aad2e309cea672ce376c171385)**6**



누끼가 '딸깍'하니까 다 따졌다
위에도 언급했지만 '검은색'을 빼주는 기능이라 배경이 완전 0.0.0이 아니라면 불완전하게 적용되는데



이경우에는 Ctrl + Alt + Shift + E를 누르거나



![7ee98577b68069f520afd8b236ef203e83e4683c1f8ce3](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781afc7cf51deeb5fa90b6e8e1b740494dc63cb54447002ce63992a057f61901aa328570afa3b83e8f9fea24)**7**



이렇게 UnMult를 불러왔던 방식으로 우클릭해서 Levels를 추가해준다음



![78e98575b08669f53fed84e647827673fba30319ea91b96b3164ad0e2e63fd](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781afc7cf51deeb5fa90b6e8e1b74049099567ca17a536b17293aa84e258c0ad719668182db483)**8**



이런식으로 배경이 검은색이 될때까지 조절해주면됨
배경뿐만아니라 원본도 손상되기때문에 어차피 포토샵에서 손봐주긴 해야된다는거
뭐가됐든 완전하기만한 기능은 아니니까각종 편법 ㄱㄱ

여튼 누끼따진 상태로 돌아와서

Ctrl + M을 눌러주면 랜더링을통해 리소스로 뽑아낼수 있게됨

File - Export - Add to Render Queue순으로 해도 ok



![79ee8472b6816cf23df1c6bb11f11a3950eff2094c68245c59](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781afc7cf51deeb5fa90b6e8e1b740494dc63cd828420f23e5349ca35afd756ef132d0fd2e9b1462be4310)**9**



Quality를 눌러서 Format타입을 PNG로 변경





![7eef8472b7816cf43ded82e658c12a3a0065a37a696983b160b278](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781afc7cf51deeb5fa90b6e8e1b740494dc63cd828420f23e5349ca35afd756dab34d0aa7803be1f292015)**10**



Channels를 Alpha가 포함된걸로 바꿔주셈





![7eee8272b78369f53cee84e658c12a3a4d8bcbe982ce65a1b7b323](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781afc7cf51deeb5fa90b6e8e1b740494dc63cd828420f23e5349ca35afd7567a53f865100e3dfbc0d56de)**11**



OutputTo를 눌러서 저장할폴더 골라주고 저장을 누른다음

Render버튼 눌러주면 에프터 이펙트 관련 주제는 끝

이제 포토샵으로 갈 차례다 ㅋㅋㅋ



![78ee8575b0816df23fed87e7459f3433dc906f5d95fc89a976ff4d59](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781afc7cf51deeb5fa90b6e8e1b740494dc63cb54447002ce63992a057f61901a031d7a380f138ea506f3f97)**12**



순서대로 File - Scripts - Load Files into Srack 눌러준다





![78e98377b78169f43df1c6bb11f11a394a751acfd7495d6f63](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781afc7cf51deeb5fa90b6e8e1b740494dc63cd828420f23e5349ca35afd753af635d0775a74fde57abd4b)**13**



아까 에펙으로 랜더링했던 폴더를 찾아서 리소스 선택해준다음 열기!

여기서 중요 포인트
사실 랜더링한건 시퀀스 수가 너무 많다보니 여기서 다 불러오지말고 그냥 눈대중으로 원하는 프레임만 잡아오셈
어쨌든 파티클 시스템으로 시퀀스를 만들꺼면 홀수 프레임은 적용하기 귀찮아지니까 짝수로맞추고
대부분 2x1 / 2x2 / 2x4 / 4x4 / 4x8 이정도로만 리소스를 뽑는편임 많은 프레임을 넣을수록 해상도를 높여야하기때문에 최적화 이슈가 있거든
파티클 시스템에 넣는 텍스쳐 해상도는 256x256 안넘어가는게 좋음 256으로도 충분히 많이 뭉개짐



여튼 이 번개이펙트는 세로로 늘씬한 리소스니까 가로에 8개 세로로 2개해서 16프레임정도면 괜찮을거같음



![7be88673b4806bf73cec87e7459f3433e23a36dd55ad3a07c3bda4bd66](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781afc7cf51deeb5fa90b6e8e1b740494dc63cd828420f23e5349ca35afd756aa73ed710eb3efbe618511f)**14**



나는 이렇게 간다!







![78eb8377b6836af53fed85fb06df231d7ad3cdf6f2e42c8ece2f](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781afc7cf51deeb5fa90b6e8e1b740494dc63cb54447002ce63992a057f61901a761d53bbc870568049a88e1)**15**



그럼 이렇게 내가 엄선한 리소스들만 등록이 되고 OK버튼 누르면
이쁘게 레이어로 정리되서 들어옴

잠깐 사고가있었음
원작자녀석 배경에다 함정을 만들어놔서 완전 검은색이 아니었어 ㅋㅋㅋㅋㅋ
배경 검은색 만들고 다시 뽑음



![78e98372b4806bf53cee84e658c12a3a2f35e656c649d78281c1055c](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe98ffa1bd6253125a05cf7d4a1966d14e02bef27781afc7cf51deeb5fa90b6e8e1b740494dc63cd828420f23e5349ca35afd756aa33384714f09e29435f9cd)**16**



검은색 배경을 맨뒤에 깔아보니 누끼는 깔끔하게 따졌다
이거를 이제 파티클 시스템 전용 리소스로 정리하면됨





![78e98573b1816af73cec87e758c12a3a92e44d9ec41706bb7e3256](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc652354c6c5847274559ef581281e7e01a49f31388c6f4b1e9c)**17**



일단 불러온 리소스의 최대크기를 알아야하니까
싹다 쉬프트+클릭으로 선택해주고
Ctrl + j 을 눌러준뒤 Ctrl + e 를 눌러주면 합쳐진 레이어가 생길거임





![7ee88472b6836af53cee85fb06df231d95f4b67f98d49237011cd4](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc084f51c9ca877f7a5693feed151e2e002303735965cb0f3b)**18**



이제 합쳐진 레이어 위에다가 Ctrl + 좌클릭을 누르면 스샷처럼 전체 외곽선이 선택이되고



![7eef8472b68369f43dee84e658c12a3af3375f3feeb47792f3](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc652354c6c5847274559ef581281a29055962d2d386d3c66b12)**19**



C키를 누르거나 위 스샷모양을 눌러주면



![7fec8277b7836af73dec87e758c12a3adaff91b25af1247c6c6e9f1b](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc652354c6c5847274559ef581284f7a0354de810ff10c8fede7)**20**



이렇게 텍스처 크기에 맞춰서 해상도를 줄일수 있게됨 앤터 두번 ㄱㄱ



![79e88572b4816af53cee85fb06df231dd541c5a29225896b3c9f](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc652354c6c5847274559ef58128197602cfabf2beef21daa378)**21**



이제 불러온파일 상단바에 우클릭해서 Image Size누르면 원하는 크기로 줄일수 있음





![7fee8472b6806af73dee84e647826a2d7ce6e26d79181782132fae7f78](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc652354c6c5847274559ef581281e7e02e8d8a3e0c5ab659470)**22**



위에서 말했지만 8x2짜리256크기의 리소스를 만들어야하니까
세로 길이를 128로 맞춰줘야 겠지?
자동으로 비율이 맞춰지기때문에 45x128 해상도가 될거임
하지만 우리는 256크기의 가로칸에 정확한 비율로 8장을 배치해야 한단말이야?





![79ef8372b68069f43dee84e658c12a3aa59daaaf804dff190bc1ba](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc652354c6c5847274559ef58128492c55ac9c4f3023f62f12b6)**23**



가운데 연결고리를 클릭해서 풀어준뒤에 32로 맞춰준다음 OK누르면





![7eee8272b7836bf53fed85e444826a2d2b9e9832bfb74e076aa7795aa0](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc652354c6c5847274559ef581284c7952fcbcdb8e683c9ad8d8)**24**



딱 원하는 사이즈의 리소스가 만들어짐
이제 다왔다 ㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋ





![7cef8374b68369f53cec84e458c12a3af25edb8932ab4c4d81f7c1](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc652354c6c5847274559ef581281d7c512188f104a980ceb22f)**25**



아까 사이즈 계측용으로 통합했던 레이어는 지우거나 꺼버리고
밑에 +를 눌러서 빈 레이어를 하나 만들어주셈





![78ee8572b4816af43fec98a518d604037ef9c80c5637c5b626](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc084f51c9ca877f7a5693feed12482c010bf96f88551aea50)**26**



Ctrl + A를 눌러서 전체선택 해주고
상단메뉴에서 Edit - Stroke를 눌러주면 창이 하나 뜨게되고





![7fee8475b7806bf43dee85e758d62d3b517a99a1de4b1592835ed8cd](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d5d2d87260bf2a25baeed1017c4e41a70ab77ed00940c4b)**27**



Width를 1픽셀로 잡아주고
Color은 니가 알아보기 쉬운 컬러로 정해서 OK누르면됨





![78e98372b0836bf43fed85e458c12a3a700fed22772cd951a2d1d1](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc652354c6c5847274559ef58128437f560d93f4578811a15218)**28**



짜잔 외곽선이 생겼어요
이제





![79ef8175b4806bf73ded87fb06df231d408ed84f0bf546cf3842](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc652354c6c5847274559ef581281a7a56418341910683b2f23b)**29**



파일 이름에다 우클릭해서 Canvas Size를 눌러주자





![7cef8275b4836af53cec87e445836a2d2ca78981d2778e8034938fe5a9](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc652354c6c5847274559ef58128432b02b7397ad84a03f0a2ff)**30**



이제 Anchor을 꼭지점으로 눌러주고 저곳을 기준으로 256크기로 늘릴거임





![78e98473b1876cf33aea98a518d604031cac519b83162a7af6](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc652354c6c5847274559ef58128482907910a1844cc99727cf4)**31**



이제 설정된 박스의 간격을 딱딱 맞춰서
8x2 비율로 딱딱 맞춰서 배치하면됨... 외곽선 레이어를 Ctrl + j로 복사해서 쓰길 바람
안그럼 개 노가다가 될테니
***\***여기서 중요한건 시퀀스는 무조건 움직일 순서대로 나열해야 한다는거임 역순으로 짜도 상관없음 어차피 그래프만 뒤집으면 되니까
하지만 순서를 뒤죽박죽 해두면 이 노가다를 처음부터 다시해야니까 반드시 신경쓰기





![79ee8475b4806bf43fec84e4459f343345ad85f03208c3c70d390ffc](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc652354c6c5847274559ef581281f2c5786be0e375ffc83a524)**32**



휴 이게 제일 귀찮고 힘들었다
이제 외곽선만 있는 레이어를 모두 꺼주면





![7eef8475b78169f43ded87e64583757310bd3338b7b2595927dce96e80e9](https://dcimg4.dcinside.co.kr/viewimage.php?id=7ce48874b6866df039e78fe5&no=24b0d769e1d32ca73fe886fa1bd62531b19a96f1cd404ede18aa6cde17cb708f28f7ad1feb6c8fe4ae045a751d197edc652354c6c5847274559ef581284d7650cf483c80bbfdf87651)**33**



완성

파티클 시스템에 적용할 리소스만들기 단계가 완료되었다





https://www.youtube.com/watch?v=KTBOahrXTBE



 

![img](https://i.ytimg.com/vi/KTBOahrXTBE/maxresdefault.jpg)

**How to Convert After Effects Animations into a Spritesheet for Unity (Free and Quick)**

Do everything inside After Effects and a lightweight open source utility. No scripts, no plugins, no AE expressions. Takes literally a minute to do.GlueIt do...

www.youtube.com

이 리소스 배치를 쉽게 해주는 툴이 있는데

덧글에 제보로 알게되서 여기다가도 괜찮은 가이드 유튜브링크 남겨둠







 

![img](https://opengraph.githubassets.com/b8d3e10058a7450f672d4d003a0740f0ee091073c6fea9ba0773f471c11be135/Kavex/GlueIT)

**GitHub - Kavex/GlueIT: :art: Simple SpriteSheet Tool**

:art: Simple SpriteSheet Tool. Contribute to Kavex/GlueIT development by creating an account on GitHub.

github.com

툴 다운로드는 여기









------


원래는 파티클시스템에 적용하는 과정까지 적으려했는데
하다보니 리소스 제작만으로 너무 늘어져서 최종 리소스 뽑는 부분까지만 쓰고 다음글로 넘어감
