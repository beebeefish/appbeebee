---
post: true
date: 2024-04-11
cover: https://jjaw.cn/assets/attach-siQjoJy5.gif
coveross: https://github.com/handyplus/appbeebee/assets/59829816/7fa2e845-25ea-4db0-9281-bf237a6e7b72
categories:
    - 服务端插件
tags:
    - 测试标签
title: KnapsackToGo4:强大的跨服数据同步插件第4代。
description: KTG4是基于bukkitAPI的我的世界服务器跨服同步插件，可在多个服务器之间同步玩家数据，支持多种同步方式。以轻松的完成多服务器之间的数据同步。未来将支持minecraft其他服务端Fabric，forge，sponge，Folia。
---

# KnapsackToGo4
KTG4是基于bukkitAPI的我的世界服务器跨服同步插件，全称KnapsackToGo4。
强大的跨服数据同步插件第4代。
可在多个服务器之间同步玩家数据，支持多种同步方式。
使用KnapsackToGo4可以轻松的完成多服务器之间的数据同步。
未来将支持minecraft其他服务端Fabric，forge，sponge，Folia。

互动教程：[https://jjaw.cn/2024/2/23/KnapsackToGo4/](https://jjaw.cn/2024/2/23/KnapsackToGo4/)



### KnapsackToGo4的演示
<img src="https://jjaw.cn/assets/attach-siQjoJy5.gif">
使用KnapsackToGo4可以轻松的完成多服务器之间的数据同步。KnapsackToGo4比KnapsackToGo2更稳定，更轻量，解决了死锁的问题，拥有更多同步方式和更强大的扩展性。

## 功能介绍

### 内置数据序列化
- #### yaml (默认)
> bukkit内置的序列化方式，最古老、最稳妥、兼容性最好的方式。几乎所有版本都支持。
- [x] 物品栏
- [x] 装备栏
- [x] 末影箱
- [x] 饱食度
- [x] 生命值
- [x] 最大生命值
- [x] 进度
- [x] 经验值
- [x] 药水效果
- [x] 位置
- [ ] 成书和书与笔中的特殊字符 （直接报错,bukkil里yaml问题，请反馈给服务端，建议禁用成书和书与笔）

### 内置的数据存储方式
- #### File (默认)
> 使用文件来完成数据同步，需要同步的服务器设置相同文件夹。

- #### Sqlite
> 使用Sqlite数据库完成同步，Sqlite是一个文件数据库，需要同步的服务器设置同一个.db文件。性能比文件夹好。

- #### Mysql
> 使用Mysql数据库完成同步，Mysql是一个网络数据库，需要同步的服务器连接到同一个数据库。

::: important 提醒
使用Mysql同步数据，如果玩家数量很多，需要自己使用数据库管理软件立索引，否则会性能降低。
:::






### KnapsackToGo4通过扩展可以支持MOD数据同步

#### ktg4作者编写的扩展下载列表
[KnapsackToGo4Plugin](https://gitee.com/jja8/KnapsackToGo4Plugin/)

#### NMSserialize
NMSserialize是KnapsackToGo4的数据序列化扩展，
NMSserialize主要是针对MOD服务器开发的，目前只提供1.12.2，1.16.5和1.18.2这几个MOD较多的版本。

##### 支持情况
- [x] 物品栏
- [x] 装备栏
- [x] 末影箱
- [x] 饱食度
- [x] 生命值
- [x] 最大生命值
- [x] 进度
- [x] 经验值
- [x] 药水效果
- [x] 位置
- [x] 统计数据
- [x] 成书和书与笔中的特殊字符
- [x] 玩家对象上的自定义数据 (mod和插件数据)
- [x] 特殊物品
- [x] 饰品栏

以上是已知，全部完美同步列表。

::: tip 小知识
NMSserialize使用，NMS序列化，直接调用核心序列化玩家数据，可以完美存储几乎所有的数据包括MOD的数据。缺点是必须同步全部数据。
:::

::: important 提醒
如果的服务端是纯净服务端不推荐使用NMSserialize，NMSserialize更新较慢，当你要升级服务器到最新版本时NMSserialize可能还没更新。
:::


### KnapsackToGo4如何保证数据安全
KnapsackToGo4使用的独占锁的方式，当玩家在一个服务器中的时其他服务器无法读取。
<Demo title="效果演示">

![Alt text](https://jjaw.cn/assets/2-uIT2UWZN.gif)

</Demo>


### 为什么写这款插件
> KnapsackToGo2插件已经有很多服务器在使用了，并且功能也挺完善。 但是仍然存在一些问题，例如：服务器崩溃后玩家再次进入服务器就需要等待许久。 
> 我自己对KnapsackToGo2也是不意的， 在开发完KnapsackToGo2之后我又继续开发了许多插件，也学习到了很多编程经验，我感觉我的编程技术有了很大的进步。 
> 在总结了前几代插件的毛病和逻辑上的问题后，我想到了种新的方案。于是我决定重新编写了一个更好的KnapsackToGo4。 
> 这次全新的KnapsackToGo4是在总结了前面所有经验后完全重新编写的，运行逻辑也是最合理符合直觉的。

> ps： 为什么新一代叫KnapsackToGo4而不是KnapsackToGo3呢? 因为KnapsackToGo3在很久之前就写完了，但是因为问题太多所以就弃坑了。


## 下载订阅

### PlugClub / 插件实验室
<img src="https://jjaw.cn/assets/3-lKqtphOi.webp">
加入我们的插件社区，交流和插件的使用方法，反馈遇到的问题，获得最新动态。

qq群：820131534 (已满)

因为qq群满了，所以现在有了qq频道: [https://pd.qq.com/s/113phvpau](https://pd.qq.com/s/113phvpau)
