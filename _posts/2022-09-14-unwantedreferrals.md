---
layout: post
permalink: /unwantedreferrals/
title: 'GA 광고 성과로 PG사 도메인이 잡힌다면?  '
date: 2022-09-14 23:58:00 +09:00
feature: '/img/posts/220914/thumbnail.png'
categories:
  - inspiration
tags:
  - 디지털마케팅
  - 구글애널리틱스4
  - GA4
  - GA4세팅

description: '구글애널리틱스4(GA4) 원치 않는 추천(unwanted referrals)'
---

### **마케터A의 사연입니다**
이번 달에 진행한 OO프로모션의 매체별 성과를 ga4에서 보려고하니, 대부분 PG사 도메인이 성과로 잡혀 정확한 성과 파악이 어렵습니다.정확한 성과 파악을 위해 PG사 도메인을 제외하고 싶은데 어떻게 할 수 있을까요?

![sum](/img/posts/220914/question.gif)

### **다케터의 답변입니다**
브라우저는 사용자가 링크를 클릭해서 웹페이지로 이동할 때 리퍼러(Referrer)라는 이름으로 클릭한 웹 페이지의 주소를 저장해요.GA에서는 리퍼러(Referrer)를 수집해 사용자가 어떤 곳에서 우리 사이트를 접속하는지 알 수 있죠.

예를 들어볼까요? 사용자가 페이스북 광고를 보고 우리 사이트에 들어왔고, 광고에 UTM을 심어뒀다면 GA 세션 소스/매체에는 facebook/display 라는 값이 찍힐거에요. ( 앱으로 들어올 경우, 매체가 referral로 노출되기도 합니다.) 사용자가 유입에 그치지 않고 구매까지 일어났다면 해당 소스/매체에 구매 전환 성과가 찍히게 될겁니다.

그런데 만약, 사용자가 구매를 하는 과정에서 PG(Payment Gateway) 도메인을 거쳐서 구매를 했다면 PG사가 referrer 값으로 찍히게 됩니다.페이스북 광고를 보고 들어왔어도, 도메인을 거쳐 구매가 발생했다면 페이스북 광고 성과가 아닌 PG사의 성과로 찍히게 되는거죠.

GA에서는 PG 도메인을 자동으로 식별해주지 않거든요. 이럴 경우 우리는 GA4의 원치 않는 추천 파악(unwanted referrers) 기능을 활용해서 PG사 도메인을 제외시킬 수 있습니다. (UA 속성의 '추천 제외 목록' 기능과 동일합니다.)


### **원치 않는 추천 (unwanted referrals) 설정 방법**
1. GA4 관리자 - 속성에 들어갑니다.
![sum](/img/posts/220914/ga4_property.jpg)

2. 속성 - 데이터 스트림을 클릭합니다.
![sum](/img/posts/220914/ga4_datastream.jpg)

3. 웹 스트림에 들어가 Google 태그 - 태그 설정 구성을 클릭합니다.
![sum](/img/posts/220914/ga4_tag.jpg)

4. 설정 - 모두 표시 클릭 후 원치 않는 추천 나열을 클릭합니다.
![sum](/img/posts/220914/ga4_unwanted.jpg)

5. 제외할 PG사 도메인을 등록합니다.
![sum](/img/posts/220914/ga4_pg.jpg)

이렇게 하면 GA4 보고서에 더 이상 PG사 도메인이 referrer에 띄지 않습니다.
