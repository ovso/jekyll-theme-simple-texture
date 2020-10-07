---
layout: post
title: "데이터바인딩의 양방향 속성(two-way-attributes)"
categories: [Android]
tags: [Databinding]
---

# 양방향 속성(two-way-attributes)확인하기

양방향 속성은 MVVM에서 종종 유용하게 쓰인다. 그러나 우리는 어느 위젯에 어떤 속성이 있는지 잘 모른다. 아래의 표를 참고하면 된다. 링크를 따라 들어가면 프레임워크의 코드를 볼 수 있는데(.java) 살펴보면 위젯별로 모든 속성이 나와 있다.

| 클래스                                                       | 속성                                                         | 결합 어댑터                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| [`AdapterView`](https://developer.android.com/reference/android/widget/AdapterView?hl=ko) | `android:selectedItemPosition` `android:selection`           | [`AdapterViewBindingAdapter`](https://android.googlesource.com/platform/frameworks/data-binding/+/refs/heads/studio-master-dev/extensions/baseAdapters/src/main/java/androidx/databinding/adapters/AdapterViewBindingAdapter.java) |
| [`CalendarView`](https://developer.android.com/reference/android/widget/CalendarView?hl=ko) | `android:date`                                               | [`CalendarViewBindingAdapter`](https://android.googlesource.com/platform/frameworks/data-binding/+/refs/heads/studio-master-dev/extensions/baseAdapters/src/main/java/androidx/databinding/adapters/CalendarViewBindingAdapter.java) |
| [`CompoundButton`](https://developer.android.com/reference/android/widget/CompoundButton?hl=ko) | [`android:checked`](https://developer.android.com/reference/android/R.attr?hl=ko#checked) | [`CompoundButtonBindingAdapter`](https://android.googlesource.com/platform/frameworks/data-binding/+/refs/heads/studio-master-dev/extensions/baseAdapters/src/main/java/androidx/databinding/adapters/CompoundButtonBindingAdapter.java) |
| [`DatePicker`](https://developer.android.com/reference/android/widget/DatePicker?hl=ko) | `android:year` `android:month` `android:day`                 | [`DatePickerBindingAdapter`](https://android.googlesource.com/platform/frameworks/data-binding/+/refs/heads/studio-master-dev/extensions/baseAdapters/src/main/java/androidx/databinding/adapters/DatePickerBindingAdapter.java) |
| [`NumberPicker`](https://developer.android.com/reference/android/widget/NumberPicker?hl=ko) | [`android:value`](https://developer.android.com/reference/android/R.attr?hl=ko#value) | [`NumberPickerBindingAdapter`](https://android.googlesource.com/platform/frameworks/data-binding/+/refs/heads/studio-master-dev/extensions/baseAdapters/src/main/java/androidx/databinding/adapters/NumberPickerBindingAdapter.java) |
| [`RadioButton`](https://developer.android.com/reference/android/widget/RadioButton?hl=ko) | [`android:checkedButton`](https://developer.android.com/reference/android/R.attr?hl=ko#checkedButton) | [`RadioGroupBindingAdapter`](https://android.googlesource.com/platform/frameworks/data-binding/+/refs/heads/studio-master-dev/extensions/baseAdapters/src/main/java/androidx/databinding/adapters/RadioGroupBindingAdapter.java) |
| [`RatingBar`](https://developer.android.com/reference/android/widget/RatingBar?hl=ko) | [`android:rating`](https://developer.android.com/reference/android/R.attr?hl=ko#rating) | [`RatingBarBindingAdapter`](https://android.googlesource.com/platform/frameworks/data-binding/+/refs/heads/studio-master-dev/extensions/baseAdapters/src/main/java/androidx/databinding/adapters/RatingBarBindingAdapter.java) |
| [`SeekBar`](https://developer.android.com/reference/android/widget/SeekBar?hl=ko) | [`android:progress`](https://developer.android.com/reference/android/R.attr?hl=ko#progress) | [`SeekBarBindingAdapter`](https://android.googlesource.com/platform/frameworks/data-binding/+/refs/heads/studio-master-dev/extensions/baseAdapters/src/main/java/androidx/databinding/adapters/SeekBarBindingAdapter.java) |
| [`TabHost`](https://developer.android.com/reference/android/widget/TabHost?hl=ko) | `android:currentTab`                                         | [`TabHostBindingAdapter`](https://android.googlesource.com/platform/frameworks/data-binding/+/refs/heads/studio-master-dev/extensions/baseAdapters/src/main/java/androidx/databinding/adapters/TabHostBindingAdapter.java) |
| [`TextView`](https://developer.android.com/reference/android/widget/TextView?hl=ko) | [`android:text`](https://developer.android.com/reference/android/R.attr?hl=ko#text) | [`TextViewBindingAdapter`](https://android.googlesource.com/platform/frameworks/data-binding/+/refs/heads/studio-master-dev/extensions/baseAdapters/src/main/java/androidx/databinding/adapters/TextViewBindingAdapter.java) |
| [`TimePicker`](https://developer.android.com/reference/android/widget/TimePicker?hl=ko) | `android:hour` `android:minute`                              | [`TimePickerBindingAdapter`](https://android.googlesource.com/platform/frameworks/data-binding/+/refs/heads/studio-master-dev/extensions/baseAdapters/src/main/java/androidx/databinding/adapters/TimePickerBindingAdapter.java) |

[https://developer.android.com/topic/libraries/data-binding/two-way?hl=ko#two-way-attributes](https://developer.android.com/topic/libraries/data-binding/two-way?hl=ko#two-way-attributes)

