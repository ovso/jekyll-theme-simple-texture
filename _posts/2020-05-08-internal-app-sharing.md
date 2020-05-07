---
layout: post
title: "내부 앱 공유"
categories: [Android]
tags: [Android]
---

프로덕션 APK를 간단하게 공유하고 싶을 때가 있다. 버전코드, 버전네임, 키 싸인, 디버그 모드 등등 신경쓰고 싶지 않고 APK를 빠르게 공유하고 싶다. 그럴 때 [내부 앱 공유](https://support.google.com/googleplay/android-developer/answer/9303479?hl=ko)를 사용하면 된다.

# 권한

앱 게시가 가능한 권한을 갖고 있으면 [내부 앱 공유](https://support.google.com/googleplay/android-developer/answer/9303479?hl=ko)가 가능하다. 물론 권한만 갖고 있다고 하여 APK 파일을 업로드 할 수 있는 것은 아니다. [Play Console](https://play.google.com/apps/publish/?account=8297797920459431859)을 통해 `승인된 업로더 추가`를 진행해야 한다. `승인된 업로더 추가`가 있다면 `승인된 테스터 추가`가 있다. 불특정 다수에서 공유할 수 있는 방법도 있으니  **내부 앱 공유** 문서를 정독한다면 모든 걸 알게 된다.. :)

# 결론

기존의 베타테스트는 까다로웠고 곧바로 게시되지도 않았다. 그러나 **내부 앱 공유** 아주 빠르다. 프로덕션을 위한 테스트 또는 베타테스트 트랙과 전혀 상관없다. 모든 걸 무시(?)하고 APK가 업로드 된다. 유용하게 사용하자.