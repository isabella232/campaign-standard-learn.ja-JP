---
title: 手順3 — モバイルアプリに拡張機能を登録する
description: この部分では、UserProfile、Identity、Lifecycle、Signalの拡張を登録するコードを追加します。
feature: Push
topics: Mobile
kt: 4827
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 13b4f1d395dfe53f9fc5263e7b06be700e30b986
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# 手順3 — モバイルアプリに拡張機能を登録する

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
