---
title: swan.onSocketError
header: develop
nav: api
sidebar: websocket_swan-onSocketError
---


 

**解释**：监听 WebSocket 错误

**方法参数**：Function callback


**示例**：

<a href="swanide://fragment/a22e8de4dae980a6179ade70625f9fbf1569500084816" title="在开发者工具中预览效果" target="_self">在开发者工具中预览效果</a>

* 在 js 文件中

```js
Page({
    swan.onSocketError(function (res) {
        console.log('WebSocket连接打开出错，请检查！', res);
    });

    swan.connectSocket({
        url: 'wss://xxx.websocket.org',
        header: {},
        protocols: [''],
        success: res => {
            console.log('connectSocket success', res);
        },
        fail: err => {
            console.log('connectSocket fail', err);
        }
    });
});
```


 
#### 错误码

* Andriod

|错误码|说明|
|--|--|
|0|error happen    |

* iOS

|错误码|说明|
|--|--|
||Status error,current + 当前状态|
||Excedding max concurrency + 设置的最大并发数|