## 基于 GoLang 编写的 IOT 物联网在线直播抓娃娃企业级项目

### 项目介绍

这是一个基于 GoLang 编写的 IOT 物联网企业级项目，主要提供的功能是：在线直播抓娃娃的一个娱乐型项目。

- 用户端

用户基于微信公众号的 H5 页面进行游戏，功能包括：画面直播、弹幕评论、基于富友支付的微信充值功能。

- 商家端

商家进行设备的管理、用户的管理、充值流水的查看、数据统计、游戏房间管理。

- 平台端

平台主要是对商家的管理，例如：创建商家、编辑商家信息。

- 设备端

一个基于安卓主板的娃娃机硬件设备，服务端通过 Mqtt 协议与安卓主板进行通信，进而控制娃娃机爪子的行为动作。

### 架构图

![image](https://images.cnblogs.com/cnblogs_com/yxhblogs/1804179/o_200711075922dollmachine.png)

### 服务介绍

- DollBarrage

通过 WebSocket 协议实现娃娃机弹幕服务，主要提供：游戏房间内评论弹幕的即时交互的功能。

- DollMerchant

基于 Gin 框架提供娃娃机商户平台 Restful Api 服务，可支持自动生成 Swagger Api 文档。

- DollMqtt

服务端通过 Mqtt 协议与娃娃机设备进行通信，从而控制娃娃机设备爪子的行为动作。

- DollPlatform

基于 Gin 框架提供娃娃机运营平台 Restful Api 服务，可支持自动生成 Swagger Api 文档。

- DollRpc

Rpc 服务，主要提供了富友支付（微信支付）的功能。

- DollUnique

主要提供了生成唯一 ID 的功能。

- DollUser

基于 Gin 框架提供微信用户端的 Restful Api 服务，可支持自动生成 Swagger Api 文档。

- DollWechat

主要提供微信菜单配置、微信授权登录、微信扫码登录并关注公众的功能。

- LiveServer

主要为娃娃机直播设备与微信用户端 H5 页面进行直播推流的一个中间服务。


### 结尾

本项目为企业级项目，仅供参考学习，目前数据库文件已经遗失。
