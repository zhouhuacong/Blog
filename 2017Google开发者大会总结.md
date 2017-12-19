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
### 3. Android studio 工具
### 4. 架构组件


## 3. AD
### 1. 移动流量的未来趋势
### 2. Google帮助提升广告

## 4. TensorFlow
### 1. 介绍性质

## 5. Google Could / PWA
### 1. 介绍性质
