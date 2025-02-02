---
title: 信息流物料投放具体字段
header: develop
nav: serverapi
sidebar: type
---



### 1.内容型

物料为文章的详情，通过图文、视频、音频、直播等形式供用户阅读为主。

1）图文型

文章的详情，物料类型主要为图片和文字的结合。

基本字段

| **key** | **类型** | **是否必填** | **备注**  | **示例**  |
| ------------- | -------- | ------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| title   | string   | **是** | 在信息流中分发的展示标题，需要描述完整，能够明确表示小程序或内容的主要信息点，不能为纯外文，最少6个字符，最多40字符（每个汉字、外文字母、阿拉伯数字、标点符号、空格等均算1字符） | 示例豆果美食小程序：超经典的蔓越莓曲奇饼干，在家也能做 |
| body | string   | **是** | 消息体，图文内容的介绍，最多2000字符（每个汉字、外文字母、阿拉伯数字、标点符号、空格等均算1字符） | 图文的全部正文，示例豆果美食小程序：黄油化开备用，黄油化开后加入糖霜，搅拌均匀，加入蛋清，继续打匀，加入切碎的蔓越莓，继续搅拌。蔓越莓放多少根据自己的喜... |
| path | string   | **是** | 智能小程序内页链接 | /pages/index/index |
| images  | string   | **是** | 封面图片链接（JSON格式）（最多3张，单图片最大2M，JPG或PNG格式） 建议尺寸：宽>=375 & 高>=250；建议比例 宽:高=1.5:1（有助于降低不可用风险，促进分发）；最低支持尺寸：宽>=218&高>=146 | ["https://b.bdstatic.com/miniapp/resource/image/demo1.png",   "https://b.bdstatic.com/miniapp/resource/image/demo2.png"] |
| mapp_type  | string   | **是** | 资源类型（参考附录一），内容型为1000 | 内容型固定为1000   |
| mapp_sub_type | string   | **是** | 资源子类型（参考附录一），图文子类为1001   | 图文型固定为1001   |
| feed_type  | string   | **是** | feed一级分类（参考附录二）  | 例如美食（可选有限集合） |
| feed_sub_type | string   | **是** | feed二级分类（参考附录二）  | 例如甜品（可选有限集合） |
| tags | string   | 否  | 资源标签，每个标签间用英文逗号分割，填写准确详细有助于提升分发效果，最多可填10个，但同资源下所有标签的字符数总和不能超过100（每个汉字、外文字母、阿拉伯数字、标点符号、空格等均算1字符） | 示例：甜甜圈,糕点,鲍师傅,酥饼  |
| ext  | string   | 见下表 | 扩展信息（JSON格式，参考下方拓展字段）  | {"desc": "智能小程序官方示例","version": "10.7.1"}  |

拓展字段

| **key**   | **类型**   | **是否必填** | **备注**  | **示例**  |
| ------------------------------------------------------------ | ---------- | ------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| author_name  | string  | 否  | 作者名 | 张三   |
| author_portrait_url   | string  | 否  | 作者头像url  | <http://www.xxx.baidu.com/author/portrail.jpg>   |
| author_path  | string  | 否  | 作者落地页链接  | /pages/author/author  |
| author_fans_num | int  | 否  | 作者粉丝量   | 10000  |
| author_auth  | string  | 否  | 是否认证作者 | 1-是 0-否   示例：1   |
| author_publish_num | string  | 否  | 作者发文量   | 100 |
| author_ask_num  | int  | 否  | 作者提问量   | 100 |
| publish_time | string  | **是** | 内容原始发布时间   | 内容原始发布时间需在一年以内   示例：2018年9月8日   |
| img_urls  | string  | 否  | 文章所有图片url | ["<https://b.bdstatic.com/miniapp/resource/image/headImg.png>"] |
| channel_id   | int  | 否  | 频道ID | 1000   |
| channel   | string  | 否  | 频道名称  | 在小程序内所属频道名   示例：萌宠，推荐，最热等  |
| like_num  | int  | 否  | 点赞量 | 1000   |
| comment_num  | int  | 否  | 评论量 | 1000   |
| dislike_num  | int  | 否  | 踩数   | 1000   |
| collect_num  | int  | 否  | 收藏量 | 1000   |
| share_num | int  | 否  | 转发量 | 1000   |
| topic  | string  | 否  | 话题名 | 减肥日记  |
| is_quality   | string  | 否  | 是否精品内容 | 小程序内优质或者热门的内容，是为1，否为0，例如1  |
| is_interactive  | string  | 否  | 是否高互动内容  | 顶/评论/收藏/分享任一互动数据在100以上的攻略资源，是为1，否为0，例如0 |
| comment   | string  | 否  | 优质评论内容 | 智能连接人与信息、人与服务、人与万物的开放生态   |
| topic_path   | string  | 否  | 话题落地页链接  | /pages/topic/topic |
| author_[introduction](https://www.youdao.com/w/brief introduction/#keyfrom=E2Ctranslation) | string  | 否  | 作者简介  | 清华大学教授，主要研究方向。。。  |
| author_followers_num  | int  | 否  | 作者关注量   | 10000  |
| author_like_num | int  | 否  | 作者累计点赞量  | 10000  |
| author_collect_num | int  | 否  | 作者累计被收藏量   | 10000  |
| author_gender   | string  | 否  | 作者性别  | 男  |
| author_location | string  | 否  | 作者位置  | 中国   |
| author_accept_rate | string  | 否  | 作者发文采纳率  | 85%，为百分比的数值   |
| is_verified  | string  | 否  | 是否大V   | true   |
| author_level | int  | 否  | 作者等级  | 0为无等级，1为最低，数字越大等级越高 |
| author_registration_year | string  | 否  | 作者注册年限 | 8（不足一年按照1计算）   |
| content_items   | JSON array | 否  | 文章结构化内容（提交该字段有助于提升信息流对内容的理解，有益于分发），需要提供正文所有的文字和图片混排内容 按原文正文换行及图片进行item分隔 type为item类型 text-文本 image-图片 例如下面的正文区可以拆分为右侧的样例。 | [ { "type":"text", "data":"第一段文字" }, { "type":"text", "data":"第二段文字" }, { "type":"image", "data":"<http://qnwww2.autoimg.cn/newsdfs/Qu4748.jpg>" }, { "type":"text", "data":"第三段文字" }, { "type":"image", "data":"<http://qnwww2.autoimg.cn/newsdfs/Nh4020.jpg>" }, { "type":"text", "data":"第四段文字" } ] |
| ip  | string  | 否  | 需引入的热点ip资源名称（如，漫画类，综艺类等）   | 极限挑战 斗破苍穹  |

2）视频型

内容的详情，物料类型主要以视频为主，辅以部分文字的说明。

基本字段

| **key** | **类型** | **是否必填** | **备注**  | **示例**  |
| ------------- | -------- | ------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| title   | string   | **是** | 在信息流中分发的展示标题，需要描述完整，能够明确表示小程序或内容的主要信息点，不能为纯外文，最少6个字符，最多40字符（每个汉字、外文字母、阿拉伯数字、标点符号、空格等均算1字符）| 示例小红书小程序：为什么大西洋和太平洋的海水，不会融合在一起？什么原因导致的？ |
| body | string   | **是** | 消息体，视频内容的介绍，最多20000字  | 视频的详细介绍，示例小红书小程序：世界之大，可谓无奇不有，虽然现在我们人类的科学技术在不断的进步，关于很多的未解之谜都在逐步的揭开，但是在世界上依然存在着很多的未解之谜，有一些自然现象真的是无法用现有的理论来解释 |
| path | string   | **是** | 智能小程序内页链接 | /pages/index/index |
| images  | string   | **是** | 封面图片链接（JSON格式）（最多3张，单图片最大2M） 建议尺寸：宽>=375 & 高>=250；建议比例 宽:高=1.5:1  | ["https://b.bdstatic.com/miniapp/resource/image/demo1.png",   "https://b.bdstatic.com/miniapp/resource/image/demo2.png"] |
| mapp_type  | string   | **是** | 资源类型（参考附录一），内容型为1000 | 内容型固定为1000   |
| mapp_sub_type | string   | **是** | 资源子类型（参考附录一），视频子类为1002   | 视频型固定为1002   |
| feed_type  | string   | **是** | feed一级分类（参考附录二）  | 科学（可选有限集合）  |
| feed_sub_type | string   | **是** | feed二级分类（参考附录二）  | 科学（可选有限集合）  |
| tags | string   | 否  | 资源标签，英文逗号分割，填写越准确详细可能带来更好的分发效果（最多10个，总长度最多100字） | 示例：组件,接口,API   |
| ext  | string   | 见下表 | 扩展信息（JSON格式，参考下方拓展字段）  | {"desc": "智能小程序官方示例","version": "10.7.1"}  |

拓展字段

| **key**   | **类型** | **是否必填**   | **备注**   | **示例**  |
| ------------------------ | -------- | -------------------------- | ---------------------------------------------- | ------------------------------------------------------------ |
| author_name  | string   | 否 | 作者名  | 张三   |
| author_profile  | string   | 否 | 作者简介   | 搞笑视频作者 |
| author_portrait_url   | string   | 否 | 作者头像url   | <http://www.xxx.baidu.com/author/portrail.jpg>   |
| author_path  | string   | 否 | 作者落地页链接   | /pages/author/author  |
| author_fans_num | int   | 否 | 作者粉丝量 | 1000   |
| author_publish_num | int   | 否 | 作者视频发布量   | 1000   |
| author _video_views   | int   | 否 | 作者发布视频浏览量  | 1000   |
| author_followers_num  | int   | 否 | 作者关注量 | 10000  |
| author_like_num | int   | 否 | 作者页累计点赞量 | 1000   |
| author_collect_num | int   | 否 | 作者页累计收藏量 | 10000  |
| author_ask_num  | int   | 否 | 作者提问量 | 100 |
| author_auth  | int   | 否 | 是否认证作者  | 1-是 0-否   示例：1   |
| author_level | int   | 否 | 作者等级   | 0为无等级，1为最低，数字越大等级越高 |
| is_verified  | string   | 否 | 是否大V | true   |
| video_title  | string   | 否 | 片名 | 我不是药神   |
| director  | string   | 否 | 导演 | 徐峥   |
| lead_role | string   | 否 | 主演 | 徐峥 周一围 王传君 谭卓 杨新鸣 |
| presenter | string   | 否 | 主持人  | 何炅   |
| guest  | string   | 否 | 嘉宾 | 谢娜   |
| publish_time | string   | **是**   | 内容原始发布时间 | 内容原始发布时间需在一年以内   示例：2018年9月8日   |
| movie_release_time | string   | 电影上映时间   | 否   | 电影上映时的时间，建议填写，   示例：2018年9月8日   |
| video_duration  | string   | **是**   | 视频时长   | 按照00:00:00格式填写  |
| pc_url | string   | **是（和h5_url需填一种）** | 视频PC播放链接   |  |
| h5_url | string   | **是（和pc_url需填一种）** | 视频H5播放链接   |  |
| update_time  | string   | 否 | 更新时间   | 2018年9月10日 15:36:20   |
| channel_id   | int   | 否 | 频道ID  | 1002   |
| video_profile   | string   | 否 | 视频简介   | 如：XXXX是最火的综艺  |
| channel   | string   | 否 | 频道名称   | 在小程序内所属的频道名称，例如视频，最热、推荐   |
| is_pay | string   | 否 | 是否付费   | 付费   |
| play_num  | int   | 否 | 播放次数   | 1000   |
| publish_year | string   | 否 | 发行年份   | 2018年 |
| area   | string   | 否 | 地区 | 北京   |
| video_status | string   | 否 | 视频状态   | 正在热映  |
| score  | string   | 否 | 评分 | 9.3 |
| like_num  | int   | 否 | 点赞量  | 1000   |
| comment_num  | int   | 否 | 评论量  | 1000   |
| collect_num  | int   | 否 | 收藏量  | 1000   |
| dislike_num  | int   | 否 | 踩数 | 1000   |
| share_num | int   | 否 | 转发量  | 1000   |
| comment   | string   | 否 | 优质评论内容  | “你敢保证你一辈子不得病？”纯粹、直接、有力！常常感叹：电影只能是电影。但每看到这样的佳作，又感慨：电影不只是电影！由衷的希望这部电影大卖！成为话题！成为榜样！成为国产电影最该有的可能。 |
| is_exclusive | string   | 否 | 是否独播   | 是1，否0   示例：1 |
| is_quality   | string   | 否 | 是否精品内容  | 小程序内优质或者热门的内容，是为1，否为0，例如1  |
| is_interactive  | string   | 否 | 是否高互动内容   | 顶/评论/收藏/分享任一互动数据在100以上的攻略资源，是为1，否为0，例如0 |
| author_registration_year | string   | 否 | 作者注册年限  | 8（不足一年按照1计算）   |
| img_urls  | string   | 否 | 视频内多张图片url（至少3张）   JSON格式  | ["<https://b.bdstatic.com/miniapp/resource/image/headImg.png>",   "<https://b.bdstatic.com/miniapp/resource/image/headImg.png>",   "<https://b.bdstatic.com/miniapp/resource/image/headImg.png>"] |
| ip  | string   | 否 | 需引入的热点ip资源名称（如，漫画类，综艺类等） | 极限挑战 斗破苍穹  |

3）直播型

内容的详情，物料类型主要以直播的形式为主。

基本字段

| **key** | **类型** | **是否必填** | **备注**  | **示例**  |
| ------------- | -------- | ------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| title   | string   | **是** | 在信息流中分发的展示标题，需要描述完整，能够明确表示小程序或内容的主要信息点，不能为纯外文，最少6个字符，最多40字符（每个汉字、外文字母、阿拉伯数字、标点符号、空格等均算1字符） | 示例斗鱼直播：户外主播宁波小老哥：《恋爱厨房》和小姐姐一起做饭，心动的感觉！ |
| body | string   | **是** | 消息体，为小程序或内容的详细介绍，机器将参考消息体为物料打上相应分发标签 | 直播内容的介绍，示例斗鱼直播：这里有美食，有音乐，还有漂亮贤惠的小姐姐。跟着《恋爱厨房》一起感受美食的魅力。 |
| path | string   | **是** | 智能小程序内页链接 | /pages/index/index |
| images  | string   | **是** | 封面图片链接（JSON格式）（最多3张，单图片最大2M） 建议尺寸：宽>=375 & 高>=250；建议比例 宽:高=1.5:1  | ["https://b.bdstatic.com/miniapp/resource/image/demo1.png",   "https://b.bdstatic.com/miniapp/resource/image/demo2.png"] |
| mapp_type  | string   | **是** | 资源类型（参考附录一），内容型为1000 | 内容型固定为1000   |
| mapp_sub_type | string   | **是** | 资源子类型（参考附录一），直播子类为1003   | 直播型固定为1003   |
| feed_type  | string   | **是** | feed一级分类（参考附录二）  | 美食（可选有限集合）  |
| feed_sub_type | string   | **是** | feed二级分类（参考附录二）  | 美食节目（可选有限集合） |
| tags | string   | 否  | 资源标签，英文逗号分割，填写越准确详细可能带来更好的分发效果（最多10个，总长度最多100字） | 示例：组件,接口,API   |
| ext  | string   | 见下表 | 扩展信息（JSON格式，参考下方拓展字段）  | {"desc": "智能小程序官方示例","version": "10.7.1"}  |

拓展字段

| **key**   | **类型** | **是否必填** | **备注**  | **示例**  |
| ------------ | -------- | ------------ | ------------------------------------------ | ------------------ |
| source_name  | string   | **是** | 主播昵称  | 张三   |
| living_type  | string   | **是** | 直播状态  | online/offline  |
| publish_time | int   | **是** | 开播时间  | 10位时间戳，示例： |
| end_time  | int   | **是** | 关播时间  | 10位时间戳，示例： |
| session_id   | string   | **是** | 场次（请将session_id加入path拼接规则当中） | 场次 id   |

4）音频

 

| **key** | **类型** | **是否必填** | **备注**  | **示例**  |
| ------------- | -------- | ------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| title   | string   | **是** | 在信息流中分发的展示标题，需要描述完整，能够明确表示小程序或内容的主要信息点，不能为纯外文，最少6个字符，最多40字符（每个汉字、外文字母、阿拉伯数字、标点符号、空格等均算1字符） | 示例斗鱼直播：户外主播宁波小老哥：《恋爱厨房》和小姐姐一起做饭，心动的感觉！ |
| body | string   | **是** | 消息体，为小程序或内容的详细介绍，机器将参考消息体为物料打上相应分发标签 | 直播内容的介绍，示例斗鱼直播：这里有美食，有音乐，还有漂亮贤惠的小姐姐。跟着《恋爱厨房》一起感受美食的魅力。 |
| path | string   | **是** | 智能小程序内页链接 | /pages/index/index |
| images  | string   | **是** | 封面图片链接（JSON格式）（最多3张，单图片最大2M） 建议尺寸：宽>=375 & 高>=250；建议比例 宽:高=1.5:1  | ["https://b.bdstatic.com/miniapp/resource/image/demo1.png",   "https://b.bdstatic.com/miniapp/resource/image/demo2.png"] |
| mapp_type  | string   | **是** | 资源类型（参考附录一），内容型为1000 | 内容型固定为1000   |
| mapp_sub_type | string   | **是** | 资源子类型（参考附录一），直播子类为1003   | 音频型固定为1004   |
| feed_type  | string   | **是** | feed一级分类（参考附录二）  | 美食（可选有限集合）  |
| feed_sub_type | string   | **是** | feed二级分类（参考附录二）  | 美食节目（可选有限集合） |
| tags | string   | 否  | 资源标签，英文逗号分割，填写越准确详细可能带来更好的分发效果（最多10个，总长度最多100字） | 示例：组件,接口,API   |
| ext  | string   | 见下表 | 扩展信息（JSON格式，参考下方拓展字段）  | {"desc": "智能小程序官方示例","version": "10.7.1"}  |

拓展字段

| **key** | **类型**   | **备注** | **是否必填** | **示例**  |
| ---------------------- | ---------- | -------------------- | ------------ | ------------------------------------------------------------ |
| author_name   | string  | 专辑作者名  | 是  | 徐佳   |
| album_name | string  | 专辑名   | 是  | 晓说2018  |
| album_type | string  | 专辑一级分类   | 是  | 开发者平台自有一级分类，例如 历史 |
| album_sub_type   | string  | 专辑二级分类   | 是  | 开发者平台自有二级分类，例如 名人传  |
| album_update_type   | string  | 专辑更新方式   | 是  | 2代表无规律更新、1代表有规律更新、0代表无更新   例如：0   |
| album_update_frequency | int  | 专辑更新频率   | 是  | 单位：天。   例如：2   ａ．若更新方式字段传“无更新”，则专辑更新频率传0；ｂ．若更新方式字段传“有规律更新”则专辑更新字段传N（Ｎ为天数）；ｃ．若更新方式字段传“无规律更新”，专辑频率传0 |
| **publish_time** | **string** | **内容原始发布时间** | 是  | **内容原始发布时间需在一年以内**   **示例：****2018****年9月8日** |
| album_publish_time  | string  | 专辑发布时间   | 是  | 内容原始发布时间需在一年以内  ，要求为时间戳格式，例如：1553529600 |
| album_update_time   | string  | 专辑更新时间   | 是  | 最新专辑的更新时间，要求为时间戳格式，例如：1553529600 |
| chapter_publish_time   | string  | 单章发布时间   | 是  | 内容原始发布时间需在一年以内   要求为时间戳格式，例如：1553529600 |
| chapter_update_time | string  | 单章更新时间   | 是  | 最新单章的更新时间，要求为时间戳格式，例如：1553529600 |
| chapter_name  | string  | 单章名   | 是  | 单章的名称，例如 高晓松聊历史  |
| chapter_num   | int  | 章节号   | 是  | 章节所对应的序号，例如 5 |
| audio_duration   | string  | 音频时长 | 是  | 按照00:00:00格式填写  |

5）本地生活

基于地理位置信息的内容详情（没有地理位置则不用填写地域标签，此时以图文或视频的策略进行全国分发）。

基本字段

| **key** | **类型** | **是否必填** | **备注**  | **示例**  |
| ------------- | -------- | ------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| title   | string   | **是** | 在信息流中分发的展示标题，需要描述完整，能够明确表示小程序或内容的主要信息点，不能为纯外文，最少6个字符，最多40字符（每个汉字、外文字母、阿拉伯数字、标点符号、空格等均算1字符） | 示例大众点评：舌尖上的江南之江浙菜   |
| body | string   | **是** | 消息体，为小程序或内容的详细介绍，机器将参考消息体为物料打上相应分发标签 | 本地生活的详情页介绍，示例大众点评：江浙菜即浙江菜系，以杭州菜作为代表，是中国传统八大菜系之一，其地山清水秀，产物丰富，佳肴美味，古有谚语曰：“上有天堂，下有苏杭”。 |
| path | string   | **是** | 智能小程序内页链接 | /pages/index/index |
| images  | string   | **是** | 封面图片链接（JSON格式）（最多3张，单图片最大2M） 建议尺寸：宽>=375 & 高>=250；建议比例 宽:高=1.5:1  | ["https://b.bdstatic.com/miniapp/resource/image/demo1.png",   "https://b.bdstatic.com/miniapp/resource/image/demo2.png"] |
| mapp_type  | string   | **是** | 资源类型（参考附录一），内容型为1000 | 内容型固定为1000   |
| mapp_sub_type | string   | **是** | 资源子类型（参考附录一），本地生活图文子类为1007 | 本地生活型固定为1007  |
| feed_type  | string   | **是** | feed一级分类（参考附录二）  | 美食（可选有限集合）  |
| feed_sub_type | string   | **是** | feed二级分类（参考附录二）  | 苏菜（可选有限集合）  |
| tags | string   | 否  | 资源标签，英文逗号分割，填写越准确详细可能带来更好的分发效果（最多10个，总长度最多100字） | 示例：组件,接口,API   |
| ext  | string   | 见下表 | 扩展信息（JSON格式，参考下方拓展字段）  | {"desc": "智能小程序官方示例","version": "10.7.1"}  |

拓展字段

| **key** | **类型** | **是否必填** | **备注**   | **示例**  |
| ------------------- | -------- | ------------------------------------------------------------ | ---------------- | ------------------------------------------------------------ |
| author_name   | string   | 否  | 作者名  | 张三   |
| author_portrait_url | string   | 否  | 作者头像url   | <http://www.xxx.baidu.com/author/portrail.jpg>   |
| author_path   | string   | 否  | 作者落地页链接   | /pages/author/author  |
| author_fans_num  | int   | 否  | 作者粉丝量 | 10000  |
| author_auth   | string   | 否  | 是否认证作者  | 1-是 0-否   示例：1   |
| author_publish_num  | string   | 否  | 作者发文量 | 100 |
| publish_time  | string   | **是** | 内容原始发布时间 | 2018年9月8日 |
| img_urls   | string   | 否  | 文章所有图片url  | ["<https://b.bdstatic.com/miniapp/resource/image/headImg.png>"] |
| channel_id | int   | 否  | 频道ID  | 1000   |
| channel | string   | 否  | 频道名称   | 在小程序内所属频道名   示例：萌宠 |
| content_heat  | string   | **是** | 内容热度   | 98.5   |
| page_view  | int   | **是** | 内容浏览量 | 1000   |
| like_num   | int   | **是** | 内容点赞量 | 1000   |
| comment_num   | int   | **是** | 内容评论量 | 1000   |
| collect_num   | int   | **是** | 内容收藏量 | 1000   |
| share_num  | int   | **是** | 内容转发量 | 1000   |
| video_duration   | string   | 是（当资源为视频时，该字段必填）  | 视频时长   | 示例：00:00:00  |
| pc_url  | string   | 是（当资源为视频时，和h5链接必填一种）  | 视频PC链接 |  |
| h5_url  | string   | 是（当资源为视频时，和pc链接必填一种）  | 视频H5链接 |  |
| store_name | string   | 是（如一篇文章有多个店铺，可不填写） | 商铺名称   | 商铺名称， case：火烧云  |
| store_province   | string   | 是（如一篇文章有多个店铺，不属于一个省，可不填写）  | 商铺所在省 | 商铺信息：省 case：北京  |
| store_city | string   | 是（如一篇文章有多个店铺，不属于一个市，可不填写）  | 商铺所在市 | 商铺信息：市 case： 北京 |
| store_area | string   | 是（如一篇文章有多个店铺，不属于一个区，可不填写）  | 商铺所在区 | 商铺信息：区 case：海淀  |
| store_district   | string   | 是（如一篇文章有多个店铺，不属于一个商圈，可不填写）   | 商铺所在商圈  | 商铺信息：商圈 case：中关村 |
| store_type | string   | 是（如一篇文章有多个店铺，不属于一个一级类别，可不填写）  | 商铺一级类别  | 商铺一级类别： case：美食   |
| store_sub_type   | string   | 是（如一篇文章有多个店铺，不属于一个二级类别，可不填写）  | 商铺二级类别  | 商铺二级类别： case：日料   |
| store_star | string   | 是（如一篇文章有多个店铺，可不填写） | 商铺星级   | 商铺星级：5星   |
| taste_rate | string   | 否（如一篇文章有多个店铺，可不填写） | 口味评分   | 口味：7.9 |
| enviroment_rate  | string   | 否（如一篇文章有多个店铺，可不填写） | 环境评分   | 环境：8.5 |
| service_rate  | string   | 否（如一篇文章有多个店铺，可不填写） | 服务评分   | 服务：7.9 |
| leaderboard_rank | int   | 是（如一篇文章有多个店铺，可不填写） | 排行榜名次 | 排行榜名次：1   |
| ave_price  | int   | 是（如一篇文章有多个店铺，不属于一个人均消费价格段，可不填写） | 人均价格   | 人均价格：200   |
| high_comment  | string   | 否  | 优质评价内容  | 手机款式漂亮，颜色我很喜欢，系统流畅，功能齐全，物超所值  |

6）问答

文章的详情，物料类型主要为图片和文字的组合，素材落详情页内容由一个问题对应多个答案。

基本字段

| **key** | **类型** | **是否必填** | **备注**  | **示例**  |
| ------------- | -------- | ------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| title   | string   | **是** | 在信息流中分发的展示标题，需要描述完整，能够明确表示小程序或内容的主要信息点，不能为纯外文，最少6个字符，最多40字符（每个汉字、外文字母、阿拉伯数字、标点符号、空格等均算1字符） | 示例豆果美食小程序：超经典的蔓越莓曲奇饼干，在家也能做 |
| body | string   | **是** | 消息体，为小程序或内容的详细介绍，机器将参考消息体为物料打上相应分发标签 | 内容的正文简介，示例豆果美食小程序：黄油化开备用,黄油化开后加入糖霜，搅拌均匀。,加入蛋清，继续打匀。,加入切碎的蔓越莓，继续搅拌。蔓越莓放多少根据自己的喜... |
| path | string   | **是** | 智能小程序内页链接，落地页要求为一个问题对应多个答案，具体样式参考手百问答落地页，**feed****要求至少8个答案** | /pages/index/index |
| images  | string   | **是** | 封面图片链接（JSON格式）（最多3张，单图片最大2M） 建议尺寸：宽>=375 & 高>=250；建议比例 宽:高=1.5:1| ["https://b.bdstatic.com/miniapp/resource/image/demo1.png",   "https://b.bdstatic.com/miniapp/resource/image/demo2.png"   "https://b.bdstatic.com/miniapp/resource/image/demo3.png“] |
| mapp_type  | string   | **是** | 资源类型（参考附录一），内容型为1000 | 内容型固定为1000   |
| mapp_sub_type | string   | **是** | 资源子类型（参考附录一），图文子类为1001   | 问答型固定为1009   |
| feed_type  | string   | **是** | feed一级分类（参考附录二）  | 例如美食（可选有限集合） |
| feed_sub_type | string   | **是** | feed二级分类（参考附录二）  | 例如甜品（可选有限集合） |
| tags | string   | 否  | 资源标签，英文逗号分割，填写越准确详细可能带来更好的分发效果（最多10个，总长度最多100字） | 示例：甜甜圈,糕点,鲍师傅,酥饼  |
| ext  | string   | 见下表 | 扩展信息（JSON格式，参考下方拓展字段）  | {"desc": "智能小程序官方示例","version": "10.7.1"}  |

拓展字段

| **key**  | **类型** | **是否必填** | **备注** | **示例**  |
| -------------------- | -------- | ------------ | ----------------------------------------------- | ------------------------------------------------------------ |
| author_name | string   | 否  | 作者名   | 张三   |
| author_portrait_url  | string   | 否  | 作者头像url | 例如<http://www.xxx.baidu.com/author/portrail.jpg>  |
| author_path | string   | 否  | 作者落地页链接 | /pages/author/author  |
| author_fans_num   | int   | 否  | 作者粉丝量  | 10000  |
| author_auth | string   | 否  | 是否认证作者   | 1-是 0-否   示例：1   |
| comment_portrait_url | array | 是  | 讨论人头像URL   问答类型资源该字段必填，固定4条 | ["<http://www.xxx.baidu.com/author/portrail.jpg>",<br>"<http://www.xxx.baidu.com/author/portrail.jpg>",<br>"<http://www.xxx.baidu.com/author/portrail.jpg>",<br>"<http://www.xxx.baidu.com/author/portrail.jpg>"]110*110 |
| comment_author_num   | int   | 是  | 讨论人数   问答类型必填该字段 | 30  |
| publish_time   | string   | **是** | 内容发布时间   | 内容发布时间需在一年以内   示例：2018年9月8日 |
| img_urls | string   | 否  | 文章所有图片url   | ["<https://b.bdstatic.com/miniapp/resource/image/headImg.png>"] |
| channel_id  | int   | 否  | 频道ID   | 1000   |
| channel  | string   | 否  | 频道名称 | 在小程序内所属频道名   示例：萌宠 |
| like_num | int   | 否  | 点赞量   | 1000   |
| comment_num | int   | 否  | 评论量   | 例如1001  |
| dislike_num | int   | 否  | 踩数  | 1000   |
| collect_num | int   | 否  | 收藏量   | 1000   |
| share_num   | int   | 否  | 转发量   | 1000   |
| topic | string   | 否  | 话题名   | 减肥日记  |
| comment  | string   | 否  | 优质评论内容   | 智能连接人与信息、人与服务、人与万物的开放生态   |
| topic_path  | string   | 否  | 话题落地页链接 | /pages/topic/topic |

### 2.工具型

工具的详情页，主要为解决用户某个问题或需求，而提供的解决方案。

基本字段

| **key** | **类型** | **是否必填** | **备注**  | **示例**  |
| ------------- | -------- | ------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| title   | string   | **是** | 在信息流中分发的展示标题，需要描述完整，能够明确表示小程序或内容的主要信息点，不能为纯外文，最少6个字符，最多40字符（每个汉字、外文字母、阿拉伯数字、标点符号、空格等均算1字符）| 示例齐天大圣小程序：违章高发地_齐车大圣智能小程序   |
| body | string   | **是** | 消息体，为小程序或内容的详细介绍，机器将参考消息体为物料打上相应分发标签 | 工具内容的介绍，示例齐天大圣小程序：提供准确、及时的违章高发地信息，方便快捷，安全出行.。 |
| path | string   | **是** | 智能小程序内页链接 | /pages/index/index |
| images  | string   | **是** | 封面图片链接（JSON格式）（最多3张，单图片最大2M） 建议尺寸：宽>=375 & 高>=250；建议比例 宽:高=1.5:1  | ["https://b.bdstatic.com/miniapp/resource/image/demo1.png",   "https://b.bdstatic.com/miniapp/resource/image/demo2.png"] |
| mapp_type  | string   | **是** | 资源类型（参考附录一），工具型为3000 | 工具型固定为3000   |
| mapp_sub_type | string   | **是** | 资源子类型（参考附录一），依照具体子类型填写  | 根据不同子类型，填写对应的二级类型，例如金融为3001  |
| feed_type  | string   | **是** | feed一级分类（参考附录二）  | 效率（可选有限集合）  |
| feed_sub_type | string   | **是** | feed二级分类（参考附录二）  | 信息查询（可选有限集合） |
| tags | string   | 否  | 资源标签，英文逗号分割，填写越准确详细可能带来更好的分发效果（最多10个，总长度最多100字） | 示例：组件,接口,API   |
| ext  | string   | 见下表 | 扩展信息（JSON格式，参考下方拓展字段）  | {"desc": "智能小程序官方示例","version": "10.7.1"}  |

拓展字段

| **key**   | **类型** | **是否必填** | **备注**   | **示例**  |
| --------- | -------- | ------------ | ------------- | ------------------ |
| scene  | string   | 否  | 使用场景   | 车主违章  |
| function  | string   | 否  | 功能点  | 违章查询，在线缴费 |
| right_age | string   | 否  | 适用年龄/评级 | 17岁以上  |

### 3.游戏型   

游戏的详情页，提供小游戏，供开发者消遣和娱乐。

基本字段

| **key** | **类型** | **是否必填** | **备注**  | **示例**  |
| ------------- | -------- | ------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| title   | string   | **是** | 在信息流中分发的展示标题，需要描述完整，能够明确表示小程序或内容的主要信息点，不能为纯外文，最少6个字符，最多40字符（每个汉字、外文字母、阿拉伯数字、标点符号、空格等均算1字符） | 示例跳一跳小游戏：不一样的跳一跳，比比看，看谁跳的更远。无需下载，立刻玩！ |
| body | string   | **是** | 消息体，为小程序或内容的详细介绍，机器将参考消息体为物料打上相应分发标签 | 游戏的介绍，示例跳一跳小游戏：我们要指控青蛙或兔子，使它们穿梭在折盒上翻蹦。 |
| path | string   | **是** | 智能小程序内页链接 | /pages/index/index |
| images  | string   | **是** | 封面图片链接（JSON格式）（最多3张，单图片最大2M） 建议尺寸：宽>=375 & 高>=250；建议比例 宽:高=1.5:1  | ["https://b.bdstatic.com/miniapp/resource/image/demo1.png",   "https://b.bdstatic.com/miniapp/resource/image/demo2.png"] |
| mapp_type  | string   | **是** | 资源类型（参考附录一），游戏型为4000 | 游戏型固定为4000   |
| mapp_sub_type | string   | **是** | 资源子类型（参考附录一），依照具体子类型而定  | 依照具体子类型而定 |
| feed_type  | string   | **是** | feed一级分类（参考附录二）  | 游戏（可选有限集合）  |
| feed_sub_type | string   | **是** | feed二级分类（参考附录二）  | 休闲游戏（可选有限集合） |
| tags | string   | 否  | 资源标签，英文逗号分割，填写越准确详细可能带来更好的分发效果（最多10个，总长度最多100字） | 示例：组件,接口,API   |
| ext  | string   | 见下表 | 扩展信息（JSON格式，参考下方拓展字段）  | {"desc": "智能小程序官方示例","version": "10.7.1"}  |

拓展字段

| **key**   | **类型** | **是否必填** | **备注**   | **示例**   |
| --------- | -------- | ------------ | ------------- | ---------------------- |
| is_multi  | string   | 否  | 单人/多人  | 多人1，单人0   示例：1 |
| is_online | string   | 否  | 是否联机   | 是1，否0   示例：1  |
| right_age | string   | 否  | 适用年龄/评级 | 17岁以上   |
| language  | string   | 否  | 语言 | 英语 |
| game_type | string   | 否  | 游戏类型   | 动作 |

### 4.服务

商品 / 服务的详情页，主要为提供商品 / 服务，用户可享受或购买。

1）商品

商品的详情页，主要售卖相关商品。

基本字段

| **key** | **类型** | **是否必填** | **备注**  | **示例**  |
| ------------- | -------- | ------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| title   | string   | **是** | 在信息流中分发的展示标题，需要描述完整，能够明确表示小程序或内容的主要信息点，不能为纯外文，最少6个字符，最多40字符（每个汉字、外文字母、阿拉伯数字、标点符号、空格等均算1字符） | 示例超值年货节：过年啦，让年货心意比你先到家！妈妈的最爱和爸爸的心头好全都低于5折哦~ |
| body | string   | **是** | 消息体，为小程序或内容的详细介绍，机器将参考消息体为物料打上相应分发标签 | 商品内容的介绍，示例超值年货节：整合主流电商平台低价好货产品，满足购物消费需求 |
| path | string   | **是** | 智能小程序内页链接 | /pages/index/index |
| images  | string   | **是** | 封面图片链接（JSON格式）（最多3张，单图片最大2M） 建议尺寸：宽>=375 & 高>=250；建议比例 宽:高=1.5:1  | ["https://b.bdstatic.com/miniapp/resource/image/demo1.png",   "https://b.bdstatic.com/miniapp/resource/image/demo2.png"] |
| mapp_type  | string   | **是** | 资源类型（参考附录一），服务型为2000 | 服务型固定位2000   |
| mapp_sub_type | string   | **是** | 资源子类型（参考附录一），商品子类为2003   | 商品型固定位2003   |
| feed_type  | string   | **是** | feed一级分类（参考附录二）  | 服务（可选有限集合）  |
| feed_sub_type | string   | **是** | feed二级分类（参考附录二）  | 电商（可选有限集合）  |
| tags | string   | 否  | 资源标签，英文逗号分割，填写越准确详细可能带来更好的分发效果（最多10个，总长度最多100字） | 示例：组件,接口,API   |
| ext  | string   | 见下表 | 扩展信息（JSON格式，参考下方拓展字段）  | {"desc": "智能小程序官方示例","version": "10.7.1"}  |

拓展字段

| **key**   | **类型** | **是否必填** | **备注** | **示例** |
| ------------------------------------------------------------ | -------- | ------------ | ----------------------- | -------------------------------------------------------- |
| name   | string   |  | 商品名称 | Apple Iphone X |
| price  | string   |  | 价格  | 7099  |
| favorable_rate  | string   |  | 好评率   | 99%   |
| category_1   | string   |  | 商品类别（一级）  | 电子产品 |
| category_2   | string   |  | 商品类别（二级）  | 通讯  |
| category_3   | string   |  | 商品类别（三级）  | 手机  |
| brand  | string   |  | 品牌  | `Apple`  |
| model  | string   |  | 型号  | (A1865) 64GB   |
| [inventory](http://www.youdao.com/w/inventory/#keyfrom=E2Ctranslation) | int   |  | 库存（动态时时数据） | 10000 |
| is_failure   | string   |  | 是否失效（已下架/售罄） | 已下架   |
| high_comment | string   |  | 优质评价内容   | 手机款式漂亮，颜色我很喜欢，系统流畅，功能齐全，物超所值 |

2）酒店



酒店的详情页，主要介绍相关酒店，并且供用户预订。

基本字段

| **key** | **类型** | **是否必填** | **备注**  | **示例**  |
| ------------- | -------- | ------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| title   | string   | **是** | 在信息流中分发的展示标题，需要描述完整，能够明确表示小程序或内容的主要信息点，不能为纯外文，最少6个字符，最多40字符（每个汉字、外文字母、阿拉伯数字、标点符号、空格等均算1字符）| 示例同程艺龙小程序：北京上地CitiGo HOUSE欢寓酒店  |
| body | string   | **是** | 消息体，为小程序或内容的详细介绍，机器将参考消息体为物料打上相应分发标签 | 酒店的介绍，示例同城艺龙小程序：上地附近最高端实惠的三星酒店，百度、腾讯等科技园员工必选 |
| path | string   | **是** | 智能小程序内页链接 | /pages/index/index |
| images  | string   | **是** | 封面图片链接（JSON格式）（最多3张，单图片最大2M） 建议尺寸：宽>=375 & 高>=250；建议比例 宽:高=1.5:1  | ["https://b.bdstatic.com/miniapp/resource/image/demo1.png",   "https://b.bdstatic.com/miniapp/resource/image/demo2.png"] |
| mapp_type  | string   | **是** | 资源类型（参考附录一），商品型为2000 | 服务型固定为2000   |
| mapp_sub_type | string   | **是** | 资源子类型（参考附录一），酒店子类为2001   | 酒店型固定为2001   |
| feed_type  | string   | **是** | feed一级分类（参考附录二）  | 服务（可选有限集合）  |
| feed_sub_type | string   | **是** | feed二级分类（参考附录二）  | 酒店订票（可选有限集合） |
| tags | string   | 否  | 资源标签，英文逗号分割，填写越准确详细可能带来更好的分发效果（最多10个，总长度最多100字） | 示例：组件,接口,API   |
| ext  | string   | 见下表 | 扩展信息（JSON格式，参考下方拓展字段）  | {"desc": "智能小程序官方示例","version": "10.7.1"}  |

拓展字段

| **key**   | **类型** | **是否必填** | **备注**  | **示例** |
| ------------ | -------- | ------------ | ------------------------------ | -------------------------------------------------------- |
| name   | string   |  | 酒店名称  | 如家前门店  |
| location  | string   |  | 酒店地理位置信息（具体到城市） | 北京西城区  |
| score  | string   |  | 酒店评分  | 9.6   |
| price  | int   |  | 价格   | 468   |
| star_level   | string   |  | 酒店星级  | 经济型酒店  |
| is_full   | string   |  | 是否满房（动态实时数据） | 是：1，否0   示例：1 |
| high_comment | string   |  | 优质评价内容 | 住的大床房，一楼，胡同里很有接地气的感觉。刚装修的挺干净 |

3）景点



景点的详情页，主要是景点的介绍或购买。

基本字段

| **key** | **类型** | **是否必填** | **备注**  | **示例**  |
| ------------- | -------- | ------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| title   | string   | **是** | 在信息流中分发的展示标题，需要描述完整，能够明确表示小程序或内容的主要信息点，不能为纯外文，最少6个字符，最多40字符（每个汉字、外文字母、阿拉伯数字、标点符号、空格等均算1字符） | 示例携程小程序：上海野生动物园。  |
| body | string   | **是** | 消息体，为小程序或内容的详细介绍，机器将参考消息体为物料打上相应分发标签 | 景点内容的介绍，示例携程小程序：上海野生动物园，带你亲近自然，感受大熊猫的可爱憨厚 |
| path | string   | **是** | 智能小程序内页链接 | /pages/index/index |
| images  | string   | **是** | 封面图片链接（JSON格式）（最多3张，单图片最大2M） 建议尺寸：宽>=375 & 高>=250；建议比例 宽:高=1.5:1  | ["https://b.bdstatic.com/miniapp/resource/image/demo1.png",   "https://b.bdstatic.com/miniapp/resource/image/demo2.png"] |
| mapp_type  | string   | **是** | 资源类型（参考附录一）服务型为2000   | 服务型固定为2000   |
| mapp_sub_type | string   | **是** | 资源子类型（参考附录一），景点子类为2002   | 景点型固定为2002   |
| feed_type  | string   | **是** | feed一级分类（参考附录二）  | 效率（可选有限集合）  |
| feed_sub_type | string   | **是** | feed二级分类（参考附录二）  | 信息查询（可选有限集合） |
| tags | string   | 否  | 资源标签，英文逗号分割，填写越准确详细可能带来更好的分发效果（最多10个，总长度最多100字） | 示例：组件,接口,API   |
| ext  | string   | 见下表 | 扩展信息（JSON格式，参考下方拓展字段）  | {"desc": "智能小程序官方示例","version": "10.7.1"}  |

拓展字段

| **key**  | **类型** | **是否必填** | **备注**  | **示例** |
| -------------- | -------- | ------------ | ------------------------------ | -------------------------------------------------------- |
| name  | string   |  | 景点名称  | 故宫  |
| location | string   |  | 景点地理位置信息（具体到城市） | 北京市东城区   |
| score | string   |  | 景点评分  | 9.6   |
| price | string   |  | 价格   | 60元  |
| artificial_tag | string   |  | 人工tag   | 卖点或吸引点，或其他话题性tag   示例：城市观光，亲水避暑 |
| is_bookable | string   |  | 是否可预订（动态实时数据）  | 是1，否0   示例：1   |
| high_comment   | string   |  | 优质评价内容 | 中国古代宫廷建筑之精华  |

4）美食


基本字段

| **key** | **类型** | **是否必填** | **备注**  | **示例**  |
| ------------- | -------- | ------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| title   | string   | **是** | 在信息流中分发的展示标题，需要描述完整，能够明确表示小程序或内容的主要信息点，不能为纯外文，最少6个字符，最多40字符（每个汉字、外文字母、阿拉伯数字、标点符号、空格等均算1字符） | 示例大众点评小程序：舌尖上的江南之江浙菜 |
| body | string   | **是** | 消息体，为小程序或内容的详细介绍，机器将参考消息体为物料打上相应分发标签 | 美食的介绍，示例大众点评小程序：江浙菜即浙江菜系，以杭州菜作为代表，是中国传统八大菜系之一，其地山清水秀，产物丰富，佳肴美味，古有谚语曰：“上有天堂，下有苏杭”。 |
| path | string   | **是** | 智能小程序内页链接 | /pages/index/index |
| images  | string   | **是** | 封面图片链接（JSON格式）（最多3张，单图片最大2M） 建议尺寸：宽>=375 & 高>=250；建议比例 宽:高=1.5:1  | ["https://b.bdstatic.com/miniapp/resource/image/demo1.png",   "https://b.bdstatic.com/miniapp/resource/image/demo2.png"] |
| mapp_type  | string   | **是** | 资源类型（参考附录一），服务型为2000 | 服务型固定为2000   |
| mapp_sub_type | string   | **是** | 资源子类型（参考附录一），图文子类为1001   |  |
| feed_type  | string   | **是** | feed一级分类（参考附录二）  | 效率（可选有限集合）  |
| feed_sub_type | string   | **是** | feed二级分类（参考附录二）  | 信息查询（可选有限集合） |
| tags | string   | 否  | 资源标签，英文逗号分割，填写越准确详细可能带来更好的分发效果（最多10个，总长度最多100字） | 示例：组件,接口,API   |
| ext  | string   | 见下表 | 扩展信息（JSON格式，参考下方拓展字段）  | {"desc": "智能小程序官方示例","version": "10.7.1"}  |

拓展字段

| **key** | **类型** | **是否必填** | **备注**  | **示例**  |
| ---------------- | -------- | ------------ | ------------------------------ | ------------------------------------------------------------ |
| name | string   |  | 餐厅名称  | 香山饭店  |
| location   | string   |  | 餐厅地理位置信息（具体到城市） | 北京海淀  |
| favorable_rate   | string   |  | 餐厅好评率   | 99% |
| price_per_person | string   |  | 人均价格  | 600元  |
| star_level | string   |  | 星级   | 五星级 |
| artificial_tag   | string   |  | 人工tag   | 餐饮类目或者属性   示例：日料、韩餐、西餐，宴请  |
| high_comment  | string   |  | 优质评价内容 | 饭店建于1984年，位于香山公园内,饭店由美籍华人   贝聿铭设计，白墙灰瓦，建筑与周围的环境相映成趣。 |

5）医疗


基本字段

| **key** | **类型** | **是否必填** | **备注**  | **示例**  |
| ------------- | -------- | ------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| title   | string   | **是** | 在信息流中分发的展示标题，需要描述完整，能够明确表示小程序或内容的主要信息点，不能为纯外文，最少6个字符，最多40字符（每个汉字、外文字母、阿拉伯数字、标点符号、空格等均算1字符） | 示例AA医生小程序：搜索医生，对症咨询。 |
| body | string   | **是** | 消息体，为小程序或内容的详细介绍，机器将参考消息体为物料打上相应分发标签 | 示例修改为-医疗服务的介绍，示例AA医生小程序：公立医院三甲医生为您服务，每天有XXXX问题被专业医生解答。 |
| path | string   | **是** | 智能小程序内页链接 | /pages/index/index |
| images  | string   | **是** | 封面图片链接（JSON格式）（最多3张，单图片最大2M） 建议尺寸：宽>=375 & 高>=250；建议比例 宽:高=1.5:1  | ["https://b.bdstatic.com/miniapp/resource/image/demo1.png",   "https://b.bdstatic.com/miniapp/resource/image/demo2.png"] |
| mapp_type  | string   | **是** | 资源类型（参考附录一），服务型为2000 | 服务型固定为2000   |
| mapp_sub_type | string   | **是** | 资源子类型（参考附录一），医疗子类为2005   | 2005   |
| feed_type  | string   | **是** | feed一级分类（参考附录二）  | 效率（可选有限集合）  |
| feed_sub_type | string   | **是** | feed二级分类（参考附录二）  | 信息查询（可选有限集合） |
| tags | string   | 否  | 资源标签，英文逗号分割，填写越准确详细可能带来更好的分发效果（最多10个，总长度最多100字） | 示例：组件,接口,API   |
| ext  | string   | 见下表 | 扩展信息（JSON格式，参考下方拓展字段）  | {"desc": "智能小程序官方示例","version": "10.7.1"}  |

拓展字段

| **key**   | **类型** | **是否必填** | **备注**  | **示例** |
| ------------ | -------- | ------------ | ------------ | -------- |
| disease   | string   |  | 疾病   | 心脏病   |
| doctor_num   | int   |  | 医生数量  | 1000  |
| high_comment | string   |  | 优质评价内容 | 妙手回春 |

