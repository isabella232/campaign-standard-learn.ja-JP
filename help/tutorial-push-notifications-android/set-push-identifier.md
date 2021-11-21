---
title: 手順 4 - pushidentifier を設定する
description: '**pushIdentifier**は、プッシュ通知用のデバイストークンを含む文字列です。 これは、Firebase から送信され、 MobileCore.setPushIdentifier メソッドを使用して SDK に渡されるトークンと同じです。'
feature: Push
kt: 4828
doc-type: tutorial
activity: use
team: TM
exl-id: 08387b84-edaa-45ee-ae66-53bcbd5c7c39
source-git-commit: 5a2f8c9a78bf5100b272f9b4461131545b3aeb8b
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# 手順 4 — 設定 [!DNL pushidentifier]

この **[!DNL pushidentifier]** は、のデバイストークンを含む文字列です。 [!DNL Push] 通知。 これは次から送信されたトークンと同じです： [!DNL Firebase] を呼び出し、 [!DNL MobileCore.setPushIdentifier] メソッド。

でプロジェクトを開きます。 [!DNL Android™ ]スタジオ。 のコード全体を削除する [!DNL MainActivity] **パッケージ文の最初の行以外は**.

次のコードを [!DNL MainActivity]:

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

これで、今後に進む前にアプリをテストする良い機会になりました。

* 緑の矢印をクリックするか「 **[!DNL Run->Run'app']**.
* この [!DNL Android™] エミュレーターが起動し、アプリがで実行されていることを確認します。 [!DNL "Hello World" ]テキスト。
* を開きます。 [!DNL logcat] ウィンドウ 「[!DNL Got]&quot;. から受け取ったトークンが表示されます。 [!DNL Firebase] を次のようにログに書き込みます。 &quot;の後の長い文字列[!DNL Got token]&quot;は [!DNL pushidentifier ]Adobe Campaignに送信される

![logcat-token](assets/logcat-got-token.PNG)

### モバイルアプリケーション購読者の確認

Adobe Campaign Standardインスタンスにログインします。
移動 **[!UICONTROL Administration->Channels->Mobile App(Experience Platform SDK)]**. 適切なモバイルアプリケーションを開きます。 タブで [!UICONTROL Mobile Application Subscribers] タブをクリックします。 次のように表示されます。 [!UICONTROL registration token ]リストに表示されました。

![mobile-application-subscribers](assets/mobile-application-subscribers.PNG)

>[!NOTE]
>
>が [!UICONTROL Mobile Application Subscribers] ここで停止を押してから、続行してください。
