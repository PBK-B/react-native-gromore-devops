<!--
 * @Author: Bin
 * @Date: 2024-09-27
 * @FilePath: /react-native-gromore-devops/README.md
-->

# React-Native-Gromore 聚合广告

> 穿山甲 GroMore SDK 的 React Native 的实现，GroMore SDK 是一个聚合广告 SDK 现已支持穿山甲、Abmob、百度、优量汇、游可赢、快手、Mintegral、Sigmob、Unity 等广告平台的聚合对接。

react-native-gromore 文档: <https://docs.ads.zmkj6.top>


## 支持广告类型

针对使用 React Native 开发的项目，并希望与穿山甲平台对接以实现流量变现，本产品提供了一个高效的解决方案，通过安装 React Native GroMore，您可以轻松集成穿山甲平台的广告服务，并通过调用简单的 API 来实现多种广告植入形式。无论您需要以下哪种广告形式:

- 开屏广告：在应用启动时全屏展示的广告，有效抓住用户的注意力并增加品牌曝光。
- 激励视频广告：用户观看视频广告后可以获得奖励，激励用户主动观看广告，从而提升广告效果和用户留存率。
- 全屏视频广告：全屏播放的视频广告，为用户提供沉浸式的广告体验，同时也能显著提高广告的可见性。
- 信息流广告：将广告自然嵌入到应用内容流中，提供与用户内容相关的广告，增强用户体验并提高广告的点击率。
- 视频信息流广告：结合视频和信息流的广告形式，为用户带来更丰富的广告体验，并有效提升广告的互动率。
- 横幅广告：在应用界面的顶部或底部展示的横幅广告，适合于不打扰用户体验的广告展示方式。

通过这些广告形式的灵活集成，您可以优化流量变现策略，提升广告投放的效果，并为用户带来更为友好的广告体验。React Native GroMore 的集成简化了与穿山甲平台的对接过程，助力您快速实现广告收入的最大化。


## 安装

通过 `npm` 或 `yarn` 安装 `@zmide/react-native-gromore`。

```bash
npm install @zmide/react-native-gromore

# or

yarn add @zmide/react-native-gromore
```

## 初始化 SDK

在项目的 `App.tsx` 或加载首个广告前需初始化 SDK，具体调用参考代码如下：

```typescript
import React, { useEffect } from 'react';
import { RNADManager } from '@zmide/react-native-gromore';

export default function App() {
	useEffect(() => {
		// 初始化 react-native-gromore
		RNADManager.init(codes.appid)
			.then((success) => {
			console.log('RNADManager init', success);
			})
			.catch((error) => {
			console.log('RNADManager init failed', error);
			});
	}, []);
	……
}
```

## 技术分享

### 2024-07

- [React Native 新架构适配之 iOS Native Components 迁移 Fabric Native Components 指北](https://docs.ads.zmkj6.top/blogs/react-native-fabric-for-ios-v3.html)

### 2020-09

- [这可能是 React Native 对接国内社交软件分享功能最全最详细的博客了](https://bin.zmide.com/?p=669&source=docs.ads.zmkj6.top)

### 2020-03

- [手把手封装一个 React native Module 之实战封装穿山甲广告模块 android 部分之开屏广告](https://bin.zmide.com/?p=512&source=docs.ads.zmkj6.top)

- [解决 React native 封装安卓 UI 原生控件刷新无效](https://bin.zmide.com/?p=519&source=docs.ads.zmkj6.top)

### 2019-10

- [ReactNative 对接穿山甲广告之开屏广告变现](https://bin.zmide.com/?p=400&source=docs.ads.zmkj6.top)


