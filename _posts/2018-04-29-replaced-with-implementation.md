---
layout: post
title: "Configuration 'compile'is obsolete and has been replaced with 'implementation'."
description: 
categories: [Android]
tags: [Android]
redirect_from:
  - /2018/04/29/
---

# 2 Warnings

```
1. Configuration 'compile'is obsolete and has been replaced with 'implementation'.
2. Configuration 'debugCompile' is obsolete and has been replaced with 'debugImplementation' and 'debugApi'.	
```

## 재현

```groovy
  dependencies {
    classpath 'com.android.tools.build:gradle:3.1.1'
  }
```

gradle 3.0.x는 구버전이다. gradle 3.1.x는 신버전이다. 신버전으로 하고 빌드하면 2개의 경고 메시지가 나타난다.

## 원인

```groovy
dependencies {
  implementation fileTree(dir: 'libs', include: ['*.jar'])

  // Support
  implementation "com.android.support:appcompat-v7:$rootProject.support_lib_version"
  implementation "com.android.support:support-v4:$rootProject.support_lib_version"
  implementation "com.android.support:design:$rootProject.support_lib_version"
}
```

Gradle 3.1.1 버전의 버그다. 

Gradle의 최근(?) 버전은 dependencies 선언시 compile 대신 implementation 또는 api를 권한다. 2018/04/29 기준으로 최신버전은 3.1.1이다. 이 버전은 implementation을 compile로 인식을 한다.

수정되어야 할 버그다

## 해결

Gradle 버전을 3.0.x 로 떨어뜨린다. (3.1.2 버전에서 수정되기를 바란다.)