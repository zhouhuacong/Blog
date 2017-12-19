# Google 2017上海开发者大会 总结

## 1. 开幕
李飞飞: "AI没有国界, AI的福祉亦无边界"(The science of AI has no borders Neither do its benefits)

图像识别与自动驾驶已经步入正轨,未来姜维我们的生活代码巨大改变



## 2. Android

### 1. Android 0reo/兼容

#### 1. 新功能
1. 后台位置更新
2. wake locks已释放
3. 带有Google Play服务的设备,Settings.secure.ANDROID_ID根据签秘钥,每个应用返回不同的值
    所以,针对广告,需要使用Google Play servers生成的可重置的AD_ID
4. Android O访问用户账号,必须借助账号选择器activity
5. 后台处理限制
    - 应用无法注册大多数显示广播
    - 后台应用无法启动服务,使用:
        - 显示Broadcast Receiver
        - JobScheduler
        - Firebase Cloud Messaging
        - startForeground API
6. 广色域显示
7. 支持更长/更窄的屏幕
    设置最大纵横比
    ```xml
    <activity
        ...
        android:resizeableActivity="false"
        android:maxAspectRatio="1.86"
    />
    ```
8. Android Orea是根据Treble构建的, 更加方便更新Android新版本
9. 通知渠道,用户可以屏蔽行为, 面向
10. 画中画模式,指定activity中的
    ```xml
        android:supoortsPicture="true"
    ```
    ```java
        activity.enterPictureInPictureMode()
    ```
11. 字体,现在是一种res,在xml在应用之间共享
12. 自动调整字体大小的textview/自动填充EditText
    ```xml
        <TextView
            ...
            app:autoSizeTextType="uniform"
            app:autoSizePresetSizes="@array/autosize_sizes"
        />
        <EditText
            ...
            app:autofillHints="postalAddress"
        />
    ```
13. 自适应图标,Android studio支持自适应图标
14. 原生音频API -- AAudio


### 2. Flutter
1. 底层使用C/C++,接口层使用Dart语言; 可以一套代码用与Android和iOS
2. 相比React Native相比,优点是与操作系统直接使用,没有中间转化层,提高效率
3. flutter美观又表现力,UI框架提供高度的可定制性
4. 可以试用一下
### 3. Android studio 工具
1. CPU分析
    - 可以看到用户的输入操作
    - 可以看到各个方法调用CPU的消耗程度
2. 内存分析
    - 内存可以结合调用的方法和对象筛选
    
3. 网络分析
    - 网络可以预览查看请求的图片
    - 可以查看耗电状态
4. 提供apk调试
### 4. 架构组件


## 3. AD
### 1. 移动流量的新兴市场
1. 中东地区和东南亚市场增长很快
    - 70%中国开发者营收
2. 东南亚虽然信用卡普及率较低,但使用点卡和运营商代扣费进行变现,能力还是可以的
3. 东南亚成功要素
    - 本地化
    - 娱乐电竞化
4. 中东地区, 节假日频繁,
    - 斋月可以利用时间点是5月中到6月中
    - 可以对本地化语言翻译
    - 日渐开放,不需要对女性包裹头部

### 2. Google帮助提升广告
1. 节假日调整eCPM价格峰值,例如美国地区,圣诞节提前增加流量和增加用户
2. 不同文化带来不同季节趋势(沙特和阿联酋eCPM在斋月达到峰值)
3. 在淡季,可以进行格式优化(插屏广告和视频广告是很好的形式,可以再Q1淡季推出)
4. 激励视频在游戏和工具类APP中比较适合,通过观看视频获取奖励
5. 精细化运营,结合firebase
6. 如何使用机器学习提升广告收益,主要是firebase结合AI分析,可以分析出用户喜欢看什么样的广告,哪些是高价值用户,Google提供A/BTest

## 4. TensorFlow / Google Could
1. Google拥有世界上最大的流量,服务器遍布全球,并且速度快,海底光缆(洛杉矶到香港 8000万人同时HD视频)
2. Google could提供多重加密,数据安全
3. TensorFlow是开源平台,并且已经提供了vision API,其中有表情识别,人脸识别,翻译,分类,视频识别等等
4. 

## 5. Google Could / PWA
### 1. 介绍性质
