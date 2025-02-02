---
title: swan.setClipboardData
header: develop
nav: api
sidebar: swan-setClipboardData
---

 

**解释**：设置系统剪贴板的内容

**百度APP中扫码体验：**

<img src="https://b.bdstatic.com/miniapp/assets/images/doc_demo/clipboardData.png"  class="demo-qrcode-image" />


**方法参数**：Object object

**`object`参数说明**：

|参数名 |类型  |必填 | 默认值 |说明|
|---- | ---- | ---- | ----|----|
|data  |  String  |是  | | 需要设置的内容|
|success |Function  |  否  | | 接口调用成功的回调函数|
|fail  | Function  |  否  | | 接口调用失败的回调函数|
|complete   | Function   | 否  | | 接口调用结束的回调函数（调用成功、失败都会执行）|

**示例**：
<a href="swanide://fragment/6fec884cc46de9ec15292cbd1da569701569485595295" title="在开发者工具中预览效果" target="_self">在开发者工具中预览效果</a>

* 在 js 文件中

```js

    swan.setClipboardData({
        data: 'xxxxxx',
        success: res => {
            swan.showToast({
                title: '设置成功'
            });
        },
        fail: err => {
            swan.showToast({
                title: '设置失败'
            });
            console.log('setClipboardData fail', err);
        }
    });
               
```
 
#### 错误码
* Andriod

|错误码|说明|
|--|--|
|202|解析失败，请检查参数是否正确      |

* iOS

|错误码|说明|
|--|--|
|202|解析失败，请检查参数是否正确      |

