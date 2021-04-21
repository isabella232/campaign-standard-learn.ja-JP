---
title: 手順 3 - モバイルアプリに拡張機能を登録
description: この部分では、UserProfile、Identity、Lifecycle、Signalの拡張を登録するコードを追加します。
feature: プッシュ
kt: 4827
doc-type: tutorial
activity: use
team: TM
exl-id: d8c0d8c6-2e04-4c27-b27a-d0de79dd953b
translation-type: tm+mt
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 12%

---

# 手順 3 - モバイルアプリに拡張機能を登録

この部分では、ユーザープロファイル、ID、ライフサイクル、シグナル拡張を登録するコードを追加します。 これらの拡張子は[[!UICONTROL Mobile Core Extensions]](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core)の一部です。 また、以下のコードに示すように、Adobe Campaign Standard拡張を登録する必要があります。

[!DNL Android] studioでプロジェクトを開きます。 MainApp **内のコード全体を削除します。ただし、パッケージ文**&#x200B;の最初の行は除きます。

次のコードをMainAppに貼り付けます。

<!--
Removed `{.line-numbers}` below
-->

```java
import [!DNL android].app.Application;
import android.util.Log;

import com.adobe.marketing.mobile.AdobeCallback;
import com.adobe.marketing.mobile.Campaign;
import com.adobe.marketing.mobile.Identity;
import com.adobe.marketing.mobile.InvalidInitException;
import com.adobe.marketing.mobile.Lifecycle;
import com.adobe.marketing.mobile.LoggingMode;
import com.adobe.marketing.mobile.MobileCore;
import com.adobe.marketing.mobile.Signal;
import com.adobe.marketing.mobile.UserProfile;

public class MainApp extends Application {

@Override
public void onCreate() {
super.onCreate();

MobileCore.setApplication(this);
MobileCore.setLogLevel(LoggingMode.DEBUG);

try{
    Campaign.registerExtension();
    UserProfile.registerExtension();
    Identity.registerExtension();
    Lifecycle.registerExtension();
    Signal.registerExtension();
    MobileCore.start(new AdobeCallback () {
        @Override
        public void call(Object o) {
            MobileCore.configureWithAppID("copy your launch property id here");
        }
    });
} catch (InvalidInitException e) {
    Log.d("ACS Exception", "exception");
}
}
}
```

32行目は、[!UICONTROL  Launch]プロパティの環境ファイルIDを指定する必要があります。 これは、[!UICONTROL Launch]プロパティの[!UICONTROL environment tab]からアクセスできます。

![launch-id](assets/launch-id-property.PNG)
