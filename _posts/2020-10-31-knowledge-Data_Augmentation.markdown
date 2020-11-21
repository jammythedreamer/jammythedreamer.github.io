---
layout: post
title:  "Data Augmentation"
subtitle:   "Data Augmentation"
categories: knowledge 
tags: Term machine-learning
comments: true
---

## 개요
> `Data Augmentation`에 대해 알아본다.

### Data Augmentation이란?

`Augmentation`은 '증가','증대' 라는 뜻을 가지고 있다.
그 말 그대로 `Data Augmentation`(이하 DA)은 Data를 증대하는 것이다.
ML에서 DA를 하는 이유는 한 마디로 하면 '성능향상'에 있다.

학습을 위해서는 많은 양의 데이터가 필요하고, 여러 Processing을 통한 DA로 
Data를 보충시켜준다.

일반적으로 사용되는 Processing은 다음과 같다.

1. flip
2. crop
3. gray scale
4. rotate
5. shift
6. rescale
7. shear
8. stretch

추가적으로
- [Cutout]()
- [Mixup]()
- [CutMix]()
- [AugMix]()

와 같은 방법들도 있다.