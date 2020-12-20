---
title: 手順 5 - 通知を反映
description: この部分では、Android Notification Manager.Firebaseを使用して、Adobe Campaignから受信したメッセージを伝播します。
feature: Push
topics: Mobile
kt: 4829
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 13b4f1d395dfe53f9fc5263e7b06be700e30b986
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 3%

---

# 追加通知を送信するサービス

この部分では、[!DNL Android Notification Manager]を使用して、Adobe Campaignから受信したメッセージを伝播します。 [!DNL Notification manager] は、発生したイベントをユーザーに通知するために使用します。次のようにして、バックグラウンドで何かが起きたことをユーザーに伝えます。

* 開始 [!DNL Android Studio]
* *[!DNL ACSPushTutorial]*&#x200B;プロジェクトを開く
* プロジェクト構造を展開する
* パッケージフォルダー([!DNL com.example.acspushtutorial])と[!DNL New ->Java Class]を右クリック
* このクラスに&#x200B;*[!DNL MyService]*&#x200B;という名前を付け、[!DNL FirebaseMessagingService]を拡張していることを確認します。
* このクラスに&#x200B;*[!DNL sendNotification]*&#x200B;メソッドを作成します。 このメソッドでは、[!DNL NotificationCompat.Builder]オブジェクトを使用して通知のコンテンツとチャネルを設定する必要があります。 通知を表示するには、[!DNL NotificationManagerCompat.notify()]を呼び出し、通知と[!DNL NotificationCompat.Builder.build()]の結果の一意のIDを渡します。

<!--
Removed `{.line-numbers}` below
-->

```java
package com.example.pushmessaging;
import android.app.NotificationChannel;
import android.app.NotificationManager;
import android.app.PendingIntent;
import android.content.Context;
import android.content.Intent;
import android.media.RingtoneManager;
import android.net.Uri;
import android.os.Build;
import android.util.Log;

import androidx.core.app.NotificationCompat;

import com.google.firebase.messaging.FirebaseMessagingService;
import com.google.firebase.messaging.RemoteMessage;

import java.util.Map;

public class MyService extends FirebaseMessagingService {
@Override
public void onMessageReceived(RemoteMessage remoteMessage)
{
Map<String,String> data  = remoteMessage.getData();
Log.d("data payload: ", data.toString());
sendNotification(remoteMessage);
}


private void sendNotification(RemoteMessage message) {
Intent intent = new Intent(this, MainActivity.class);
intent.addFlags(Intent.FLAG_ACTIVITY_CLEAR_TOP);
PendingIntent pendingIntent = PendingIntent.getActivity(this, 0 /* Request code */, intent, PendingIntent.FLAG_ONE_SHOT);

String channelId = "0";
Uri defaultSoundUri = RingtoneManager.getDefaultUri(RingtoneManager.TYPE_NOTIFICATION);
NotificationCompat.Builder notificationBuilder =
        new NotificationCompat.Builder(this, channelId)
                .setSmallIcon(R.drawable.ic_launcher_background)
                .setContentTitle("Message from AEM")
                .setContentText(message.getData().get("body"))
                .setAutoCancel(true)
                .setSound(defaultSoundUri)
                .setContentIntent(pendingIntent);

NotificationManager notificationManager =
        (NotificationManager) getSystemService(Context.NOTIFICATION_SERVICE);

// Since android Oreo notification channel is needed.
if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.O) {
    NotificationChannel channel = new NotificationChannel(channelId,
            "Channel human readable title",
            NotificationManager.IMPORTANCE_DEFAULT);
    notificationManager.createNotificationChannel(channel);
}

notificationManager.notify(0 /* ID of notification */, notificationBuilder.build());
}
}
```

## 修正 [!DNL AndroidManifest.xml]

&lt;追加a0/>に対して作成されたサービス。 [!DNL AndroidManifest.xml]最終的な[!DNL AndroidManifest.xml]は次のようになります。

<!--
Removed `{.line-numbers}` below
-->

```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.pushmessaging">

    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />

    <application
        android:name=".MainApp"
        android:allowBackup="true"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/AppTheme">
        <service
            android:name=".MyService"
            android:exported="false">
            <intent-filter>
                <action android:name="com.google.firebase.MESSAGING_EVENT" />
            </intent-filter>
        </service>

        <activity android:name=".MainActivity">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>
```

## アプリの実行

ツールバーまたは[!DNL Run]メニューの&#x200B;**緑色の矢印**&#x200B;をクリックして、アプリを実行します。
