---
title: swan.getSwanId
header: develop
nav: api
sidebar: userinfo_swan-getSwanId
---

 
**解释**：获取 swanid，swanid 长度不超过 100 个字符。

**方法参数**：Object object

**`object`参数说明**：

|参数名 |类型  |必填 | 默认值 |说明|
|---- | ---- | ---- | ----|----|
|success |Function  |  否 | |  接口调用成功的回调函数|
|fail  |  Function |   否 | |  接口调用失败的回调函数|
|complete |   Function |   否  | | 接口调用结束的回调函数（调用成功、失败都会执行）|

**success返回参数说明**：

|参数  |类型|说明 |
|---- | ---- |---- |
|errno  | String  |errno|
|data  | Object  |{swanid}|

<!-- **data 返回参数说明**

|参数  |类型|说明 |
|---- | ---- |---- |
|swanid|string|由 cuid 生成|
|swanid_signature|string|对 swanid 进行校验| -->
<!-- |swanid_old|string
|swanid_old_signature |string        -->

**示例**：

<a href="swanide://fragment/c9e65c8a95454a6246328f88f54205d61558336445340" title="在开发者工具中预览效果" target="_self">在开发者工具中预览效果</a>

* 在 swan 文件中

```html
<view class="wrap">
    <button type="primary" bindtap="getSwanId">getSwanId</button>
</view>
```

* 在 js 文件中

```js
Page({
    getSwanId() {
        swan.getSwanId({
            success: res => {
                console.log('getSwanId success', res);
            },
            fail: err => {
                console.log('getSwanId fail', err);
            }
        });
    }
});
```
* 在 css 文件中

```css
.wrap {
    padding: 50rpx 30rpx;
}
```
 

#### 错误码
* Andriod

|错误码|说明|
|--|--|
|201|解析失败，请检查调起协议是否合法|
|1001|执行失败|
|10001|内部错误|
|10002|网络无连接|

* iOS

|错误码|说明|
|--|--|
|202|解析失败，请检查参数是否正确      |
|10001|内部错误    |
|10002|网络无连接|
|10004|用户拒绝(user not login)|
|10005|系统拒绝|


