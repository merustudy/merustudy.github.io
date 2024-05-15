---
layout: default
title: Build
nav_order: 81
parent: Basic(Unity)
grand_parent: Unity
---

# Build

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

## STEP 1. Build Test

### Step 1-1. Debuging

* Logcat 
  * [유니티 로그캣(logcat)을 이용한 안드로이드 디버깅 방법](https://blockdmask.tistory.com/587)
* 개발자설정
  * [유니티 각개격파_007_휴대폰 연결하는 방법](https://fiftiesstudy.tistory.com/246)



### Step 1-2. Trouble Shooting

* (로딩 오류 발생) 어드레서블 오류
  * 에디터에서는 문제가 없지만, 모바일 빌드 후 addressable에서 sprite 파일들을 2배로 보내줌 
  * [SOL URL](https://forum.unity.com/threads/addressables-loadresourcelocationsasync-will-give-me-2-times-the-assets-that-i-have.738317/)


<br>

## STEP 2. 최적화
### Step 2-0. 프로파일러
* About Profiler
  * [유니티 프로파일러(Profiler)를 이용해 성능 개선하기](https://dev-nicitis.tistory.com/7)
  * [유니티 최적화_프로파일러](https://coderzero.tistory.com/entry/%EC%9C%A0%EB%8B%88%ED%8B%B0-%EC%B5%9C%EC%A0%81%ED%99%94-%ED%94%84%EB%A1%9C%ED%8C%8C%EC%9D%BC%EB%9F%AC)
  * [유니티 - 프로파일링을 통한 최적화](https://rito15.github.io/posts/unity-opt-profiling/)   
  * [유니티 프로파일러 기록 제한 늘리기](https://wlsdn629.tistory.com/entry/%EC%9C%A0%EB%8B%88%ED%8B%B0-%ED%94%84%EB%A1%9C%ED%8C%8C%EC%9D%BC%EB%9F%AC-%EC%A0%9C%ED%95%9C-%EB%8A%98%EB%A6%AC%EA%B8%B0#google_vignette)
  
* Connect Profiler to Mobile
  * [(UnityEngine) Unity Profiler Manual](https://walll4542.wixsite.com/watchthis/post/unity-profiler-manual)
  * [unity study #6 - 유니티 프로파일러](https://velog.io/@sb8929/Unity-Profiling)
  * [Unity Android 모바일로 Unity Profiler 사용하기](https://dallcom-forever2620.tistory.com/19)
  
* Profiler를 통한 개선
  * [퍼포먼스 스파이크 현상](https://howudong.tistory.com/180)

### Step 2-1. Reference Stie
* [(Unity) 유니티 최적화 방법들](https://happysalmon.tistory.com/12)
* [유니티 공식 유튜브_모바일 게임 성능 최적화 - 1편](https://dev-junwoo.tistory.com/79)
* [유니티 공식 유튜브_모바일 게임 성능 최적화 - 2편](https://dev-junwoo.tistory.com/84#Light-)
* [유니티 프레임 설정하는 방법(최적화)](https://swfa.tistory.com/170)



<br>



# STEP 3. 실제 적용

### STPE 3-0. Setting

* [프레임 유지 및 드랍의 Vsync 옵션](https://cru6548.tistory.com/12)

* [Unity 프레임 고정](https://young-94.tistory.com/97#google_vignette)

  

### Step 3-1. Code(GC)

* 코루틴 최적화
  * [C#, Unity - 코루틴 Yield 최적화 하기(+IEqualityComparer)](https://velog.io/@livelyjuseok/C-Unity-%EC%BD%94%EB%A3%A8%ED%8B%B4-Yield-%EC%B5%9C%EC%A0%81%ED%99%94-%ED%95%98%EA%B8%B0IEqualityComparer)



<br>



### Step 3-2. Asset

* 에셋 관련
  * 텍스쳐
    * Read/Write enabled 플래그 비활성화 (기본 비활성화)
    * 밉맵
  * 모델
    * Read/Write enabled 플래그 비활성화(기본 활성화)
    * 애니메이션화되지 않는 모델의 리그를 비활성화
    * 애니메이션화(스켈레톤 리그) 되는 모델에 게임 오브젝트 최적화 옵션 활성화(Optimize Game Objects 활성화)
      * [유니티 - 모델 트랜스폼 구조 최적화하기](https://rito15.github.io/posts/unity-optimize-model-transform/)
  
  
