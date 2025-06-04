---
title: '"系统代理下为什么无法ping通"'
date: 2025-06-04 10:10:33
categories: [随笔, 技术]
tags: [Hexo, 博客]
---
The ping command was sent from the network layer.
• layer：网络层（Layer 3）
• Protocol ：ICMP
• function：Test whether the target IP can be reached, and measure the delay and packet loss

代理软件是在应用层接受连接：
ping命令(使用的是ICMP协议，在网络层)无法使用代理
但是，如果开启了tun模式，这时候代理软件作用于网络层，模拟一个虚拟网络接口用于接收请求，这时ping命令会走向代理。
