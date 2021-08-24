---
title: 手順4 — プッシュ識別子を設定する
description: '**pushIdentifier**は、プッシュ通知用のデバイストークンを含む文字列です。 これは、Firebaseから送信され、 MobileCore.setPushIdentifierメソッドを使用してSDKに渡されるトークンと同じです。'
feature: プッシュ
kt: 4828
doc-type: tutorial
activity: use
team: TM
exl-id: 08387b84-edaa-45ee-ae66-53bcbd5c7c39
source-git-commit: 5a2f8c9a78bf5100b272f9b4461131545b3aeb8b
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# 手順4 - [!DNL pushidentifier]を設定する

**[!DNL pushidentifier]**&#x200B;は、[!DNL Push]通知のデバイストークンを含む文字列です。 [!DNL Firebase]から送信され、[!DNL MobileCore.setPushIdentifier]メソッドを使用してSDKに渡されるトークンと同じです。

[!DNL Android™ ]スタジオでプロジェクトを開きます。 [!DNL MainActivity] **内のコード全体を削除します。ただし、パッケージステートメント**&#x200B;の最初の行は除きます。

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

今が、それ以降に進む前にアプリをテストする良い機会です。

* 緑の矢印をクリックするか、「**[!DNL Run->Run'app']**」を選択して、アプリを実行します。
* [!DNL Android™]エミュレーターが起動し、[!DNL "Hello World" ]テキストでアプリが実行されていることを確認します。
* [!DNL logcat]ウィンドウを開きます。 「[!DNL Got]」を検索します。 [!DNL Firebase]から受信したトークンが、次のようにログに書き込まれています。 「[!DNL Got token]」の後の長い文字列は、Adobe Campaignに送信される[!DNL pushidentifier ]です。

![logcatトークン](assets/logcat-got-token.PNG)

### モバイルアプリケーション購読者の確認

Adobe Campaign Standardインスタンスにログインします。
**[!UICONTROL Administration->Channels->Mobile App(Experience Platform SDK)]**&#x200B;に移動します。 適切なモバイルアプリケーションを開きます。 「[!UICONTROL Mobile Application Subscribers]」タブに移動します。 [!UICONTROL registration token ]が表示されます。

![mobile-application-subscribers](assets/mobile-application-subscribers.PNG)

>[!NOTE]
>
>[!UICONTROL Mobile Application Subscribers]タブに登録トークンが表示されない場合は、ここで停止してから先に進んでください。
