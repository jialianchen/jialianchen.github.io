---
layout: post
title: WebRTC_QOE估值研究
tags:
- 流媒体
categories: 流媒体服务
description: 一个搜集流媒体信息的大杂烩。
---

# QOE估值研究
最近在做webrtc的码率调整动态优化，准备使用drl来做。但是并没有一些idea about reward function.在sigcomm2017的Pensieve@Mao中使用的是vod的估值函数:

```
r(t) = q(b(t)) - uT(t) - n|q(b(t)) - q(b(t-1))|
means: r(t) = +bitrate - rebuffering - smoothness
```
