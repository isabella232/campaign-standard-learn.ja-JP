---
title: 手順 1 - Android アプリを作成し、Firebase Cloud Messaging を使用するように設定する
description: このパートでは、 [!DNL Android] 受信するアプリ [!UICONTROL Push notifications] Adobe Campaign Standardから送信済み プッシュ通知を受け取るには、アプリをGoogleに登録する必要があります [!DNL Firebase Cloud Service].
feature: Push
user: Admin
level: Experienced
jira: KT-4825
doc-type: tutorial
activity: use
team: TM
recommendations: noDisplay
exl-id: f087d9f2-cce9-4903-977f-3c5b47522c06
source-git-commit: 0ad82fb0533ed8fc2a85c2a32c7e54deef14d05a
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 3%

---

# 手順 1 — 作成 [!DNL Android] アプリケーションと使用する設定 [!DNL Firebase Cloud Messaging]

このパートでは、 [!DNL Android] 受信するアプリ [!UICONTROL Push notifications] Adobe Campaign Standardから送信済み プッシュ通知を受け取るには、アプリをGoogleに登録する必要があります [!DNL Firebase Cloud Service].

1. にログインします。 [!DNL Firebase] アカウント。

   [!DNL Firebase] は、高品質のアプリをすばやく開発するのに役立つ、Googleのモバイルプラットフォームです。 次の条件を満たさない場合、 [!DNL Firebase] アカウントを作成してください [ここから](https://firebase.google.com).

2. 開始 [!DNL Android Studio]
3. クリック **[!UICONTROL File]** > **[!UICONTROL New]** > **[!UICONTROL New Project].**
4. 「**[!UICONTROL Empty Activity]**」を選択し、「**[!UICONTROL Next]」をクリックします。**

   ![android-project](assets/android-project.PNG)

5. プロジェクトに意味のある名前を付けます。

   このデモの目的で、プロジェクトの名前をにしました。 *[!DNL ACSPushTutorial]*

   ![android-project-configuration](assets/android-project-configuration.PNG)

6. デフォルトのパッケージ名をそのまま使用し、「 **[!DNL Finish]** をクリックして、プロジェクトを作成します。
7. プロジェクト構造は、以下のスクリーンショットのようになります

   ![android-project-structure](assets/android-project-structure.PNG)

8. クリック **[!UICONTROL Tools]** > **[!UICONTROL Firebase].** ( これにより、プロジェクトが [!DNL Firebase])
9. 「**[!UICONTROL Set up Firebase Cloud Messaging]」をクリックします。**

   ![firebase を設定](assets/android-project-firebase-messaging.PNG)

10. 「**[!UICONTROL Connect to Firebase]」をクリックします。**
11. アプリが Firebase に接続されたら、 **[!UICONTROL Add FCM to your app].**
12. 「**[!UICONTROL Accept Changes]」をクリックします。**

   アプリに FCM を追加する場合、ウィザードでプロジェクトに変更を加えるための権限が必要です。

   ![[!DNL add-fcm-to-your-app]](assets/firebase-add-fcm-to-app.PNG)

アプリを Firebase と正常に統合すると、次のようなメッセージが表示されます。

![[!DNL fcm-successfull]](assets/android-firebase-success.PNG)

[プロジェクトが [!DNL Firebase ]コンソール](https://console.firebase.google.com/)

## 設定 [!UICONTROL Push Channel] 設定

1. ログイン先 [!DNL Firebase] コンソール
2. を開きます。 **[!UICONTROL ACSPushTutorial]** プロジェクト。
3. 次をクリック： **歯車アイコン** プロジェクト設定を開きます。

   ![project-settings](assets/firebase-project-settings.PNG)

4. タブで **[!UICONTROL Cloud Messaging]** タブをクリックします。
5. サーバーキーをコピーします。

   ![server-key](assets/firebase-server-key.PNG)

6. Adobe Campaign Standardインスタンスにログインします。
7. クリック **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile App].**
8. 適切な **[!UICONTROL Mobile Application Property].**
9. 次をクリック： **[!DNL Android]アイコン** （内） **[!UICONTROL Push Channel settings]** 」セクションに入力します。
10. 「サーバーキー」フィールドにサーバーキーを貼り付けます。

すべてがうまくいけば、SUCCESS メッセージが表示されます。

![push-channel-settings](assets/push-channel-settings.PNG)

要約すると、 [!DNL Android App] そして [!DNL Android App] 次を使用 [!DNL Firebase]. その後、Adobe Campaignのモバイルアプリを [!DNL Android App] 貼り付けて [!DNL Android] Adobe Campaign Standardのモバイルアプリに追加されたアプリのサーバーキー。
