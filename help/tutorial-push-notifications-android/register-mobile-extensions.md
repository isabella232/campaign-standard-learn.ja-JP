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
source-git-commit: a2f194821a9ce06272eaed979ee2d8c62cccac2b
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# 手順3 — モバイルアプリに拡張機能を登録する

この部分では、ユーザープロファイル、ID、ライフサイクル、シグナル拡張を登録するコードを追加します。 これらの拡張は、の一部で [[!UICONTROL Mobile Core Extensions]](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core)す。 また、以下のコードに示すように、Adobe Campaign Standard拡張を登録する必要があります。

プロジェクトを [!DNL Android] studioで開きます。 MainApp内のコード全体を削除します。ただし、パッケージ文の最初の行は **除きます**。

次のコードをMainAppに貼り付けます。

```java{.line-numbers}
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

32行目で、プロパティの環境ファイルIDを指定する必要があります[!UICONTROL  Launch] 。 これには、プロパティ [!UICONTROL environment tab] のからアクセスでき [!UICONTROL Launch] ます。

![launch-id](assets/launch-id-property.PNG)
