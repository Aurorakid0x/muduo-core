# muduo-core

> **本项目目前只在[知识星球](https://programmercarl.com/other/kstar.html)答疑并维护**。

[知识星球](https://programmercarl.com/other/kstar.html)再添 CPP项目专栏， 关于网络库，知名的就是陈硕的muduo

之前也有不少录友，自己做一个muduo写到简历上。

这次 我们从 面试的角度带大家速成muduo，**【项目细节】【项目面试常见问题汇总】【拓展出的基础知识汇总】【测试相关问题】【简历写法】** 都给大家安排的明明白白。

## 为什么要做 muduo？

*  通过学习muduo网络库源码，一定程度上提升了linux网络编程能力;
*  熟悉了网络编程及其下的线程池，缓冲区等设计，学习了多线程编程;
*  通过深入了解muduo网络库源码，对经典的五种IO模型及Reactor模型有了更深的认识
*  掌握基于事件驱动和事件回调的epoll+线程池面向对象编程。

## 参考书籍

* 陈硕（官方）：https://github.com/chenshuo/muduo/
* 《Linux多线程服务器编程-使用 muduo C++网络库》-陈硕
* 《Linux高性能服务器编程》-游双

## 项目专栏目录

* muduo网络库项目前言
    * 为什么要做 muduo？
    * 所需要的基础知识
    * 参考书籍
* 框架梳理
* 并发框架
    * Channel
        * Channel类重要的成员变量：
        * Channel类重要的成员方法
    * Poller
        * Poller/EpollPoller概述
        * Poller/EpollPoller的重要成员变量：
        * EpollPoller给外部提供的最重要的方法：
    * EventLoop
        * EventLoop概述：
        * One Loop Per Thread 含义介绍
        * 全局概览Poller、Channel和EventLoop在整个Multi-Reactor通信架构中的角色
        * EventLoop重要方法 EventLoop:loop()：
    * Acceptor
        * Acceptor封装的重要成员变量
        * Acceptor封装的重要成员方法
    * tcpconnection
        * TcpConnection的重要变量
        * TcpConnection的重要成员方法：
    * socket
    * buffer
        * 重要的成员方法：
* 项目介绍
    * 简单介绍一下你的项目
* 项目面试常见问题汇总
    * 项目中的难点？
        * 如果TcpConnection中有正在发送的数据，怎么保证在触发TcpConnection关闭机制后，能先让TcpConnection先把数据发送完再释放TcpConnection对象的资源？
    * 项目中遇到的困难？是如何解决的？
        * 怎么保证一个线程只有一个EventLoop对象
        * 怎么保证不该跨线程调用的函数不会跨线程调用
    * 项目当中有什么亮点
        * Channel的tie _ 涉及到的精妙之处
* 项目细节
    * 日志系统
        * 异步日志流程
        * 开启异步日志
        * 把日志写入缓冲区
    * 缓存机制
        * Buffer数据结构
        * 把socket上的数据写入Input Buffer
        * 把用户数据通过output buffer发送给对方
    * muduo定时器实现思路
* 项目拓展出的基础知识汇总
    * IO多路复用
        * 说一下什么是ET，什么是LT，有什么区别？
        * 为什么ET模式不可以文件描述符阻塞，而LT模式可以呢？
        * 你用了epoll，说一下为什么用epoll，还有其他多路复用方式吗？区别是什么？
    * 并发模型
        * reactor、proactor模型的区别？
        * reactor模式中，各个模式的区别？
    * 测试相关问题
* 简历写法 & 面试技巧
    * 本项目简历写法
    * 通用简历写法
    * 面试技巧
        * 八股
        * 算法
        * 实习
        * 项目



## 简历写法

为了避免[知识星球](https://programmercarl.com/other/kstar.html)里大家学习这个项目写简历重复，本项目专栏提供了三种简历写法：

![](https://file1.kamacoder.com/i/algo/20240904205019.png)

## 本项目常见问题

面试中，面试官最喜欢问的就是项目难点，以及这个难点你是如何解决的。

专栏里都给出明确的例子：

![](https://file1.kamacoder.com/i/algo/20240904204734.png)

## 项目亮点以及项目细节

为了更好的掌握这个项目，亮点和细节都给大家讲清楚：

![](https://file1.kamacoder.com/i/algo/20240904204822.png)

## 项目拓展出的基础知识

在做做项目的时候，最好的方式就是 理论基础知识和项目实战相结合。

面试官也喜欢在 项目中问基础知识（八股文），本专栏也给出muduo可以拓展哪些基础知识

![](https://file1.kamacoder.com/i/algo/20240904204936.png)

## 项目专栏部分截图

![](https://file1.kamacoder.com/i/algo/20240904204906.png)

![](https://file1.kamacoder.com/i/algo/20240904205923.png)

## 突击来用

如果大家面试在即，实在没时间做项目了，可以直接按照专栏给出的【简历写法】，写到简历上，然后把项目专栏里的面试问题，都认真背一背就好了，基本覆盖 绝大多数 RPC项目问题。

## 答疑

本项目在[知识星球](https://programmercarl.com/other/kstar.html)里为 文字专栏形式，大家不用担心，看不懂，星球里每个项目有专属答疑群，任何问题都可以在群里问，都会得到解答：

![](https://file1.kamacoder.com/i/web/2025-09-26_11-30-13.jpg)


## 获取本项目专栏

**本文档仅为星球内部专享，大家可以加入[知识星球](https://programmercarl.com/other/kstar.html)里获取，在星球置顶**


