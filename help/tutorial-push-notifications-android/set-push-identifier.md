---
title: 手順4 - pushidentifierの設定
description: '**pushIdentifier**は、プッシュ通知用のデバイストークンを格納する文字列です。 これは、Firebaseから送信され、MobileCore.setPushIdentifierメソッドを使用してSDKに渡されるのと同じトークンです。'
feature: Push
topics: MOBILE
kt: 4828
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: bbe5f985ae791f55e94c7369fbf1aefcfd9d2b76
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# 手順4 — 設定 [!DNL pushidentifier]

は、通知 **[!DNL pushidentifier]** のデバイストークンを含む文字列 [!DNL Push] です。 これは、によって送信され [!DNL Firebase] 、メソッドを使用してSDKに渡されるのと同じトークンで [!DNL MobileCore.setPushIdentifier] す。

プロジェクトを [!DNL Android ]studioで開きます。 パッケージ文の最初の行を [!DNL MainActivity] 除く、のコード全体を削除します ****。

次のコードをに貼り付けま [!DNL MainActivity]す。

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

* 緑色の矢印をクリックするか、を選択して、アプリを実行し **[!DNL Run->Run'app']**&#x200B;ます。
* エミュレータ [!DNL Android] ーが開始し、アプリケーションが [!DNL "Hello World" ]テキストで実行されていることが確認できます。
* ウィンドウを開き [!DNL logcat] ます。 「[!DNL Got]」を検索します。 次に示すように、ログに [!DNL Firebase] 書き込まれた時点から受け取ったトークンが表示されます。 「[!DNL Got token]」の後の長い文字列は、Adobe Campaign [!DNL pushidentifier ]に送信されます。

![logcatトークン](assets/logcat-got-token.PNG)

### モバイルアプリケーション購読者の確認

Adobe Campaign Standardインスタンスにログインします。
ナビゲ **[!UICONTROL Administration->Channels->Mobile App(AEP SDK)]**&#x200B;ート 適切なモバイルアプリケーションを開きます。 Tab to the [!UICONTROL Mobile Application Subscribers] tab. リストが表示され [!UICONTROL registration token ]ます。

![モバイルアプリケーション購読者](assets/mobile-application-subscribers.PNG)

>[!NOTE]
>
>これ以上操作を行う前に、 [!UICONTROL Mobile Application Subscribers] タブ「ここで停止」に登録トークンが表示されない場合。
