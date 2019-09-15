[度盘更新](https://pan.baidu.com/s/1dDPd8uonkXofFcHEBTzUWA)
[酷安(弃坑)](http://www.coolapk.com/u/715204)
[阅读模式](https://github.com/nmdx/bangumi/blob/master/BiliAndroidMod.md)
[Github反馈](https://github.com/nmdx/bangumi/issues/1)
**ps.以后只更新【测版】版本，测试版本将包括以下全部实验性的功能**

[TOC]
   * [版本说明](#版本说明)
      * [5.31.0 更新记录](#5310更新记录)
      * [5.9.1版本更新记录](#591版本更新记录)
   * [代码笔记](#代码笔记)
      * [番剧缓存的版权受限](#番剧缓存的版权受限)
      * [主题代码](#主题代码)
      * [番剧详情页承包下面的广告](#番剧详情页承包下面的广告)
      * [去除会员购，游戏中心和顶栏](#去除会员购游戏中心和顶栏)
      * [动态页顶栏修改](#动态页顶栏修改)
      * [黑洞广告卡片](#黑洞广告卡片)
      * [非番剧的版权限制按钮---5.9.1版本](#非番剧的版权限制按钮---591版本)
      * [(非大会员)强制添加大会员/付费番剧缓存](#非大会员强制添加大会员付费番剧缓存)
         * [视频替换方法简介](#视频替换方法简介)
      * [升级检测屏蔽](#升级检测屏蔽)
      * [直播间右下角广告](#直播间右下角广告)
      * [投屏权限控制](#投屏权限控制)
         * [全屏三点菜单里的投屏按钮](#全屏三点菜单里的投屏按钮)
         * [视频详情页播放窗口的投屏按钮](#视频详情页播放窗口的投屏按钮)
      * [修改启动activity的bug](#修改启动activity的bug)
      * [视频详情页推荐列表广告](#视频详情页推荐列表广告)
      * [跳过流量播放检测](#跳过流量播放检测)
         * [视频和番剧播放](#视频和番剧播放)
         * [直播](#直播)
      * [签名验证](#签名验证)
      * [qq分享修复](#qq分享修复)



# 版本说明
1. 番剧页缓存限制
2. 主题限制
3. 去除主页的游戏中心,会员购以及多余顶栏
4. 微信分享修复(普通视频小程序bug已解决)
5. 跳过启动页activity(已修复后台点图标进首页问题)
6. 去升级(修改版本更新地址)，修改Android7以上的证书策略(抓包用)
7. 直播间右下角广告
8. 番剧详情页横幅广告
9. 屏蔽首页视频列表的广告(仍有占位，单列正常)
10. 屏蔽偶尔出现在视频详情页下的推荐列表广告
11. 强制开启投屏(包括版权/转载视频)

**5.9.1特别修复番剧搜索，目测应该官方原版包问题**


## 5.31.0+更新记录
19.09.14：修复缓存权限检测
19.06.27：修复分享到新版本手机qq的权限
12.04：特别版本_移除直播流量提示  
11.10：特别版本_移除番剧和普通视频的流量播放提示  
10.30：去除小米/魅族/华为等推送receiver  
10.26：强制开启详情页投屏按钮，再无需全屏【鸡肋，废弃】  
10.21：非会员可以添加大会员番剧或者霹雳布袋戏之类的到缓存列表【不能正常缓存】，然后就可以使用视频替换大法(详见后，繁琐)  
10.18：跳过投屏权限服务器验证，本地强制开启投屏按钮，理论只要服务器不封掉投屏专用的视频api就能一直用；部分视频没有投屏源无法投屏，可能是官方cdn问题，无解  
10.17：修复强制跳过启动屏后，任何时候从桌面点图标都会打开首页的问题  
10.15：终于干死了新版微信分享用的小程序，这个实在没法劫持(ﾉ｀⊿´)ﾉ   恢复之前网页分享样式  
new:屏蔽升级地址，去除直播间右下角广告

**强制跳过启动页，为什么冷启动那么慢？因为它优化的就是这么渣！启动页只是用来伪装它启动慢的事实！！**


## 5.9.1版本更新记录

new:修改非番剧的缓存限制按钮，比如电影，非大会员添加后可能无法正常开始缓存，建议分享到bilime添加缓存。

new:去除版本更新提示，简单暴力的方法：抓包后修改升级地址。。class中搜索 x/v2/version/update 定位并修改之；本次更新后，修改了Android7以上所需的证书安全配置文件，以便大家以后能够方便的使用中间人证书进行HTTPS抓包。。具体代码查看res/xml/network_security_config.xml自行谷歌学习

new:修复搜索不出番剧问题，5.9.1版本将去除播放器截图按钮(高版本设置中可自行关闭)，去除番剧的手办广告，想看广告的sorry了😂

new:修复微信分享闪退问题，通过申请微信开放平台appid，替换劫持源代码，微信支付无解，除非root破解核心

new:支持免root破解核心安装啦，在yitry修改的包(去广告大会员等侧栏，破解主题等等) 添加了离线缓存

进入大会员：个人中心点击图标 
进入免流：流量进入视频详情，点击开通免流，点击激活

港澳台番剧无解，大陆ip是无法获取到数据的。。  
可以尝试搜索up主 哔哩哔哩番剧出差，在视频详情页左上角获取av号  然后去bilime搜索

bilime是一个远古的小工具。。仅供备用
折腾，使用bilime需要先用哔哩哔哩缓存一个视频(暂停即可)，  从bilime添加的缓存任务若无法显示，请强制(停止/重新启动)哔哩哔哩


# 代码笔记

工具：`MT管理器`

## 番剧缓存的版权受限
1. 从arsc中搜索"在线"，复制结果中大概是"抱歉，该剧只可在线观看" 这句的id ( 7F090269 )
2. 3个class.dex里面有一个用16进制能搜索到该id，结果大概如下:
Lcom/bilibili/bangumi/ui/detail/BangumiDetailActivity;
3. v方法列表中继续搜索该id定位到方法
4. 打开后文本搜索该id定位到行，上面那个label_记住
5. 代码片段如下:
```
<3.修改这里  直接goto : label_114>if-eqz v0 :label_123<修改这里>
const-string/jumbo v0 "不可用"
invoke-static {v7,v0} Lbl/bhr;->b(Landroid/content/Context;Ljava/lang/String;)V
goto :label_15
iget-object v0 v7 Lcom/bilibili/bangumi/ui/detail/BangumiDetailActivity;->b:Lcom/bilibili/bangumi/api/BiliBangumiSeasonDetail;
iget-boolean v0 v0 Lcom/bilibili/bangumi/api/BiliBangumiSeasonDetail;->mDownloadable:Z
if-nez v0 :<2.记住这里>label_114<记住这里>
const v0 <1.找到这里>0x7f090269<找到这里>
```
-----------
### 新版本的服务端权限检测
核心参数npcybs区分播放/缓存请求，字符串编码参考如下，5.31.0测试，新版本若编码改变请自行解决
```
      0x6bt
      0x75t
      0x66t
      0x7ct
      0x67t
      0x76t
```
直接搜索定位，5.31.0为classes.dex中第一个结果，修改一个字符即可，比如0x76t --> 0x77t 【16进制，修改加减1即可，不要过大以免字符解码异常】

该参数服务器没有强制检测，随时凉，就看程序员工资高不高了

5.47.0貌似没有字符编码了，api应该是`http://api.bilibili.com/pgc/player/api/playurl`
自行研究附近代码，其它版本可以抓包对比在线/缓存api参数研究，目前发现问题就是在线限速严重，搭配闪飞多线程将就用用吧

## 主题代码
特么。。第一次改错了，全买了一遍

Arsc找到`%d硬币/月`的`id`，`5.9.1`为`7f1005c7`  
`classes.dex`(大概和上面是同一个class)搜索`7f1005c7`，定位到`Lbl/emq`(之类的)方法列表，字符串搜索查找`free`最后大概剩下`b`和`onClick`两个方法

1. b 代码片段:
```
iget-boolean v2 v12 Ltv/danmaku/bili/ui/theme/api/BiliSkin;->【定位】mIsFree:Z
<删除这行>if-eqz v2 :label_143<删除这行>
iget-object v0 v11 Lbl/emq$b;->q:Landroid/widget/TextView;
```
2. onclick 代码片段:
```
iget-boolean v3 v0 Ltv/danmaku/bili/ui/theme/api/BiliSkin;->【定位】mIsFree:Z
<修改这里，直接goto到label_62>if-nez v3 :label_62<修改这里>
```
一个控制显示**使用**按钮  一个控制点击跳过权限检测


## 番剧详情页承包下面的广告
`5.9.1`
1. 布局文件`res/layout/bangumi_item_detail_advertise.xml`
2. 添加`android:visibility="gone"`
3. 修改宽高为0dp
> 
android:layout_width="0dp"  
android:layout_height="0dp"

`新版(5.31.0测试)`  
番剧详情页抓包可得，在第一个class 搜索app_cover，改成别的名字，(若失败把上面的ab也改掉)  
类名`BangumiUniformSeason$OperationActivity`  
可能需要MT管理器的 *dex编辑器++* 来修改这里的数据


## 去除会员购，游戏中心和顶栏

顶栏底栏和右上角都是启动时联网控制，类似之前抓包后修改id，即可屏蔽后使用内置数据  
完整匹配加大小写搜索`abtest`，将`classes3.dex`下的`tv/danmaku/bili/ui/main2/resource/MainResourceManager$TabResponse` 中`data`改名(多次测试得出的位置)

接着修改默认顶底栏数据，完整匹配搜索**会员购**，`classes3.dex`下根据需要自行删减。。  
从`new-instance v1, Lbl/okz; `到`invoke-interface {v0, v1}, Ljava/util/List;->add(Ljava/lang/Object;)Z`为一个块


## 动态页顶栏修改

`classes4.dex`搜索代码`ceq`，`bl/ceq`方法里面第一个`b`方法,
```
const/4 v4 1 
invoke-interface {v8,v4} Ljava/util/List;->get(I)Ljava/lang/Object;
move-result-object v5
check-cast v5 Lcom/bilibili/bilibililive/followingcard/net/entity/FollowingType;
iget v5 v5 Lcom/bilibili/bilibililive/followingcard/net/entity/FollowingType;->type:I
invoke-static {v5,v1,v2,v9} Lbl/cer;->b(IJI)Lbl/cer;
move-result-object v5
invoke-interface {v8,v4} Ljava/util/List;->get(I)Ljava/lang/Object;
move-result-object v6
check-cast v6 Lcom/bilibili/bilibililive/followingcard/net/entity/FollowingType;
iget-object v6 v6 Lcom/bilibili/bilibililive/followingcard/net/entity/FollowingType;->name:Ljava/lang/String;
【invoke-virtual {v0,v5,v6} Lbl/coe;->a(Landroid/support/v4/app/Fragment;Ljava/lang/String;)V】
```
```
invoke-static {v4,v1,v2,v9} Lbl/cex;->a(ZJI)Landroid/support/v4/app/Fragment;
move-result-object v9
const/4 v1 2 
invoke-interface {v8,v1} Ljava/util/List;->get(I)Ljava/lang/Object;
move-result-object v8
check-cast v8 Lcom/bilibili/bilibililive/followingcard/net/entity/FollowingType;
iget-object v8 v8 Lcom/bilibili/bilibililive/followingcard/net/entity/FollowingType;->name:Ljava/lang/String;
【invoke-virtual {v0,v9,v8} Lbl/coe;->a(Landroid/support/v4/app/Fragment;Ljava/lang/String;)V】
```
删除这两段，就是删除动态的最后两个顶栏保留第一个视频页,如果要保留其它可酌情删除，然后因为只剩一个了，可以把顶栏直接隐藏掉：`fragment_following_home_exhibition.xml`->`tabs`下面高度改成`0dp`  
**注意：去除动态的综合页会导致动态小红点去不掉**


## 黑洞广告卡片 

*dex++编辑器* 完整匹配大小写搜索`extra` 修改第一个`classes.dex`，参考`com.bilibili.ad.adview.feed.model`，重命名`extra`


## 非番剧的版权限制按钮---5.9.1版本

1. arsc中搜索"版权受限"【title_download_forbid】和"缓存"【video_detail_download】的id，大概第二个claas.dex中可搜索到代码位置，修改绘制缓存按钮
> 
~~if-eqz v1 :label_224~~  【**删掉这行，`label_224` 下面有 `版权受限`的id**】  
iget-object v1 v7 Ltv/danmaku/bili/ui/video/section/ActionSection$ActionViewHolder;->downloadText:Landroid/widget/TextView;  
const v3 0x7f090d52 【**左边`0x7f090d52`是`缓存`的id**】

2. 这修改后按钮是变过来了，点击会提示 *版权受限*，根据以前的goto大法自行体会。。
3. 还会再提示 *无法下载*，继续goto大法


## (非大会员)强制添加大会员/付费番剧缓存
东拼西凑找到**缓存付费**四个字的转码。。。代码搜索如下定位 **注意复制换行和空格**
> 
        -0x18t
        -0x4dt
        -0x64t
        -0x16t
        -0x5et
        -0x69t
        -0x15t
        -0x4ct
        -0x69t
        -0x19t
        -0x45t
        -0x4at

代码参考：
```
.method public c(Lcom/bilibili/bangumi/api/uniform/BangumiUniformEpisode;)Z
    .registers 3
    .line 781
    iget-object v0, p0, Lcom/bilibili/bangumi/ui/detail/BangumiDetailActivity;->G:Lcom/bilibili/bangumi/api/uniform/BangumiUniformSeason;
    invoke-static {p0, v0, p1}, Lbl/bqt;->a(Landroid/content/Context;Lcom/bilibili/bangumi/api/uniform/BangumiUniformSeason;Lcom/bilibili/bangumi/api/uniform/BangumiUniformEpisode;)Z
    move-result p1
    const/16 p1, 0x1【添加这行强制true】
    if-nez p1, :cond_18
    const/16 v0, 0x24
    .line 783
    new-array v0, v0, [B
    fill-array-data v0, :array_1a
    invoke-static {v0}, Lbl/jsx;->a([B)Ljava/lang/String;
    move-result-object v0
    invoke-static {p0, v0}, Lbl/gqc;->b(Landroid/content/Context;Ljava/lang/String;)V
    :cond_18
    return p1
```
仅能够添加缓存列表，然后可用替换大法ԅ(✧_✧ԅ)

### 视频替换方法简介
1. 定位到具体番剧分集文件夹，参考路径：
`/storage/emulated/0/Android/data/tv.danmaku.bili/download/s_24596/232534/entry.json`
2. 新建文件夹(或者把一个正常的复制过来)，参考命名：`lua.flv720.bb2api.64`
3. 将自己的视频文件名修改为`0.blv`后放入文件夹，然后修改entry.json开头。参考：
> {"is_completed":true,"type_tag":"lua.flv720.bb2api.64",
4. 重启客户端进行弹幕更新


## 升级检测屏蔽

升级检测网址如下,新版app已被转码  
https://app.bilibili.com/x/v2/version/update
```
const-class v2, 【Ltv/danmaku/bili/update/BiliUpdateVerInfo】 代码搜索这句定位
代码片段：
   sget-object v2, Ljava/util/concurrent/TimeUnit;->【定位可注意下这里】SECONDS:Ljava/util/concurrent/TimeUnit;
    .line 95
    invoke-virtual {v1, v3, v4, v2}, Lbl/nou$a;->b(JLjava/util/concurrent/TimeUnit;)Lbl/nou$a;
    move-result-object v1
    const/4 v2, 0x0
    .line 96
    invoke-virtual {v1, v2}, Lbl/nou$a;->a(Z)Lbl/nou$a;
    move-result-object v1
    .line 97
    invoke-virtual {v1}, Lbl/nou$a;->c()Lbl/nou;
    move-result-object v1
    const/16 v2, 0x2c
    .line 98
    new-array v2, v2, [B
    fill-array-data v2, :array_1ba【向后寻找该混淆数组】
    invoke-static {v2}, Lbl/jsx;->a([B)Ljava/lang/String;
    move-result-object v2
    invoke-static {v2}, Lokhttp3/HttpUrl;->f(Ljava/lang/String;)Lokhttp3/HttpUrl;【定位可注意下这里】
```


## 直播间右下角广告

1. apk内xml搜索id `img_top`
2. 定位到`res/layout/bili_live_room_operation_entrance_widget.xml`
3. 修改两个`frame`宽高为`0dp`


## 投屏权限控制
### 全屏三点菜单里的投屏按钮
1. 搜索**投屏**两字的id，id标题参考`Player_option_menu_projection_screen`
2. `classes3.dex`中定位  转java源码后观察大概有2句add()方法，推测前面一行就是服务器控制的权限开关，根据之前所学，想办法跳过这两处检测即可

### 视频详情页播放窗口的投屏按钮
查询后xml搜索`ic_bplayer_remote`的id `7F080765`有两结果  
`res/layout/bangumi_activity_vertical_player.xml`  
`res/layout/bili_app_activity_vertical_player_tab_base.xml`  
修改定位id上面的android:visibility="gone"为visible  
**番剧页播放器暂时无解。还有代码查不出来。。**


## 修改启动activity的bug

即，后台时点哔哩图标会直接进入本次修改的启动activity(即首页)而无法恢复之前的页面。  
删除该activity的`android:launchMode="singleTask"`属性行即可


## 视频详情页推荐列表广告

id应该是`ad_tint_frame`，使用xml搜索  
可能是`res/layout-v17/bili_ad_feed_ad_video_v2.xml`，按照之前修改布局隐藏即可


## 跳过流量播放检测

### 视频和番剧播放
1. `classes.dex`定位下`正在使用免流`的id 后面一个位置，`5.31.0`版本为`pix->m()`方法 (非正常方法，正常需要逐步定位调用关系)
2. 思路：把免流分支(全部操作代码)提取出来直接返回即可，不知道会不会造成免流异常，需要等待哔哩卡用户测试
3. 最后xml搜索`tips_unicom`定位`res/layout/bili_app_player_network_alert.xml` 把顶层隐藏一下，这样可以偷懒很多dex代码不用再改了，不然要删除所有`Lbl/psd;->a(Landroid/view/ViewGroup; `的调用

### 直播
1. 照猫画虎，还是同样的思路，结论：
claases4.dex的`gbg->n()`方法，`:cond_d9`直接如下返回
>    :cond_d9
>    invoke-virtual {p0}, Lbl/gbg;->r()V

2. 然后修改小窗模式
按照`流量播放`的`id`一路定位到`Lbl/eyr;` 最后反查`Lbl/eyr;`  
该片段直接控制显示浮层，所以把调用eyr的直接删掉，即反查得到的`Lbl/eyu;`  
代码参考删除如下：
```
    move-result-object p1
    new-instance v0, Lbl/eyr;
    invoke-direct {v0}, Lbl/eyr;-><init>()V
    invoke-virtual {p1, v0}, Lbl/ptr$a;->a(Lbl/ptm;)Lbl/ptr$a;
```

## 签名验证
1. 旧版本可以使用MT管理器的去除签名校验工具。然后可能需要重命名`META-INF/CERT.RSA/SF`，注意保持`xxx.RSA/xxx.SF`命名一致  
2. 新版本定位到`lib/armeabi-v7a/libbili.so`，十六进制编辑，ANSI文本搜索`META` 修改两处为`METB`等等  
若只能搜索十六进制，则十六进制数值为 4D 45 54 41  任意修改即可


## qq分享修复
搜索定位
```
invoke-static {v0, v1}, Lcom/tencent/tauth/Tencent;->createInstance(Ljava/lang/String;Landroid/content/Context;)Lcom/tencent/tauth/Tencent;
```

(搜狗输入法的)qq分享代码参考-----
```
    const-string v0, "101679027"
[5.31上面这句可能需要手动添加,其他版本如果分享到qq提示了appid则直接字符串搜索替换即可]
    iget-object v1, p0, Lnq;->a:Landroid/app/Activity;

    invoke-static {v0, v1}, Lcom/tencent/tauth/Tencent;->createInstance(Ljava/lang/String;Landroid/content/Context;)Lcom/tencent/tauth/Tencent;

    move-result-object v0

    iput-object v0, p0, Lnq;->a:Lcom/tencent/tauth/Tencent;
```
-----------
appid      101683658
签名    mt默认
不满意名字图标的话可去qq互联申请。。不一定能通过


## 私人备注
IWXAPI;->registerApp 微信sdk  
小程序视频，`ShareParamMinProgram;ShareParamWebPage;`
```
    .line 159
    new-instance v0, Lcom/bilibili/socialize/share/core/shareparam/ShareParamWebPage;

    invoke-direct {v0, v1, v5, v10}, Lcom/bilibili/socialize/share/core/shareparam/ShareParamWebPage;-><init>(Ljava/lang/String;Ljava/lang/String;Ljava/lang/String;)V

    .line 160
    invoke-virtual {v0, v14}, Lcom/bilibili/socialize/share/core/shareparam/ShareParamWebPage;->a(Lcom/bilibili/socialize/share/core/shareparam/ShareImage;)V

    return-object v0
```
