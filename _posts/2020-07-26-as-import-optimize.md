---
layout: post
title: "코드리포멧 할때 Import 최적화도 하기"
categories: [Android]
tags: [Android]




---

# Import Optimize

정확히 기억나지 않지만, 아주 오래전에 코드 리포멧(⌥, ⌘ + L) 하면 자동으로 Import 최적화가 됐었다. 그러나 최근에는 그렇지 않아서 클래스 상단에 사용하지 않는 `import` 에 포커싱하고 ⌥ + Enter 하여 Import 최적화를 진행했다. 불편하게 사용하고 있다가 다시금 알게 되어 기록한다.

### 코드 리포멧(⌥, ⌘ + L) 할 때 Import 최적화 진행하게 하기

- Android Studio에서 클래스 파일 하나를 연다.
- (새로운)코드 리포멧(⇧,⌥, ⌘ + L) 한다.
- 창이 하나 뜬다. Optimize imports를 Check on 한다.
- 이제 코드 리포멧(⌥, ⌘ + L) 하면 자동으로 Import 최적화가 된다.

해피코딩하자.