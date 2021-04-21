---
title: 手順4 - pushidentifierの設定
description: '**pushIdentifier**は、プッシュ通知用のデバイストークンを格納する文字列です。 これは、Firebaseから送信され、MobileCore.setPushIdentifierメソッドを使用してSDKに渡されるのと同じトークンです。'
feature: プッシュ
topic: MOBILE
kt: 4828
doc-type: tutorial
activity: use
team: TM
exl-id: 08387b84-edaa-45ee-ae66-53bcbd5c7c39
translation-type: tm+mt
source-git-commit: ddbb0843ea45a83d9ab5bfa0877287f6ba7d6210
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# 手順4 - [!DNL pushidentifier]を設定する

**[!DNL pushidentifier]**&#x200B;は、[!DNL Push]通知のデバイストークンを格納する文字列です。 これは[!DNL Firebase]から送信されるのと同じトークンで、[!DNL MobileCore.setPushIdentifier]メソッドを使用してSDKに渡されます。

[!DNL Android ]studioでプロジェクトを開きます。 [!DNL MainActivity] **のコード全体を削除します。ただし、パッケージ文**&#x200B;の最初の行は除きます。

次のコードを[!DNL MainActivity]に貼り付けます。

<!--
Removed `{.line-numbers}` below
-->

```java
import androidx.annotation.NonNull;
import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.util.Log;
import android.widget.Toast;

import com.adobe.marketing.mobile.MobileCore;
import com.google.android.gms.tasks.OnCompleteListener;
import com.google.android.gms.tasks.Task;
import com.google.firebase.iid.FirebaseInstanceId;
import com.google.firebase.iid.InstanceIdResult;

public class MainActivity extends AppCompatActivity {

@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);

registerToken();
}

void registerToken() {
FirebaseInstanceId.getInstance().getInstanceId()
    .addOnCompleteListener(new OnCompleteListener<InstanceIdResult>() {
        @Override
        public void onComplete(@NonNull Task<InstanceIdResult> task) {
            if (!task.isSuccessful()) {
                Log.w("Message App", "getInstanceId failed", task.getException());
                return;
            }

// Get new Instance ID token
String token = task.getResult().getToken();

Log.d("Got token", token);

MobileCore.setPushIdentifier(token);
}
});
}

@Override
public void onResume() {
super.onResume();
MobileCore.setApplication(getApplication());
MobileCore.lifecycleStart(null);
}

@Override
public void onPause() {
super.onPause();
MobileCore.lifecyclePause();
}
}
```

## アプリのテスト

これ以上作業を行う前に、アプリをテストするのに適したタイミングです。

* 緑の矢印をクリックしてアプリを実行するか、**[!DNL Run->Run'app']**&#x200B;を選択します。
* [!DNL Android]エミュレーターが開始し、[!DNL "Hello World" ]テキストを使用して実行しているアプリが表示されます。
* [!DNL logcat]ウィンドウを開きます。 「[!DNL Got]」を検索します。 [!DNL Firebase]から受け取ったトークンが、次のようにログに書き込まれています。 「[!DNL Got token]」の後の長い文字列は、Adobe Campaignに送信される[!DNL pushidentifier ]です。

![logcatトークン](assets/logcat-got-token.PNG)

### モバイルアプリケーション購読者の確認

Adobe Campaign Standardインスタンスにログインします。
**[!UICONTROL Administration->Channels->Mobile App(AEP SDK)]**&#x200B;に移動します。 適切なモバイルアプリケーションを開きます。 [!UICONTROL Mobile Application Subscribers]タブにタブ移動します。 [!UICONTROL registration token ]が表示されます。

![モバイルアプリケーション購読者](assets/mobile-application-subscribers.PNG)

>[!NOTE]
>
>[!UICONTROL Mobile Application Subscribers]タブに登録トークンが表示されない場合は、これ以上先に進む前にSTOPを押します。
