---
title: 手順1 - Androidアプリを作成し、Firebase Cloud Messagingを使用するように設定する
description: ここではAdobe Campaign Standardから [!DNL Android] App to receive [!UICONTROL Push notifications] 作成します。 プッシュ通知を受け取るには、アプリをGoogleに登録する必要があります [!DNL Firebase Cloud Service]。
feature: Push
topics: Mobile
kt: 4825
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: afe1ae6c8d73b7b776e0eec327fa16db76c23ce1
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 2%

---


# 手順1 - [!DNL Android] アプリの作成と、 [!DNL Firebase Cloud Messaging]

この部分では、Adobe Campaign Standardから [!DNL Android][!UICONTROL Push notifications] 送信されるアプリを作成します。 プッシュ通知を受け取るには、アプリをGoogleに登録する必要があり [!DNL Firebase Cloud Service]ます。

1. アカウントにログインし [!DNL Firebase] ます。

   [!DNL Firebase] は、高品質のアプリをすばやく開発できるGoogleのモバイルプラットフォームです。 アカウントをお持ちでない場合は、ここ [!DNL Firebase] から [アカウントを作成してください](https://firebase.google.com)。

2. 起動 [!DNL Android Studio]
3. Click **[!UICONTROL File]** > **[!UICONTROL New]** > **[!UICONTROL New Project].**
4. 「**[!UICONTROL Empty Activity]**」を選択し、「**[!UICONTROL Next]」をクリックします。**

   ![android-project](assets/android-project.PNG)

5. プロジェクトに意味のある名前を付けます。

   このデモの目的で、プロジェクトの名前を *[!DNL ACSPushTutorial]*

   ![android-project-configuration](assets/android-project-configuration.PNG)

6. デフォルトのパッケージ名をそのまま使用し、をクリックし **[!DNL Finish]** てプロジェクトを作成します。
7. プロジェクト構造は、次のスクリーンショットのようになります

   ![android-project-structure](assets/android-project-structure.PNG)

8. クリック **[!UICONTROL Tools]** > **[!UICONTROL Firebase].**(これにより、プロジェクトがに追加され[!DNL Firebase]ます)
9. 「**[!UICONTROL Set up Firebase Cloud Messaging]」をクリックします。**

   ![firebaseの設定](assets/android-project-firebase-messaging.PNG)

10. 「**[!UICONTROL Connect to Firebase]」をクリックします。**
11. アプリケーションがFirebaseに接続されたら、をクリックし **[!UICONTROL Add FCM to your app]ます。**
12. 「**[!UICONTROL Accept Changes]」をクリックします。**

   アプリにFCMを追加する場合、ウィザードでプロジェクトに変更を加えるための権限が必要です。

   ![[!DNL add-fcm-to-your-app]](assets/firebase-add-fcm-to-app.PNG)

アプリケーションとFirebaseの統合に成功したら、次のようなメッセージが表示されます。

![[!DNL fcm-successfull]](assets/android-firebase-success.PNG)

[プロジェクトがコンソールに表示されていることを確認 [!DNL Firebase ]します](https://console.firebase.google.com/)

## 設定 [!UICONTROL Push Channel] を行う

1. コンソールにログイン [!DNL Firebase] する
2. プロジェクトを開き **[!UICONTROL ACSPushTutorial]** ます。
3. **歯車アイコンをクリックし** 、プロジェクト設定を開きます

   ![project-settings](assets/firebase-project-settings.PNG)

4. Tab to the **[!UICONTROL Cloud Messaging]** tab.
5. サーバーキーをコピーします

   ![サーバーキー](assets/firebase-server-key.PNG)

6. Adobe Campaign Standardインスタンスにログインします
7. Click **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile App].**
8. 適切なを選択し **[!UICONTROL Mobile Application Property]ます。**
9. セクションで **[!DNL Android]アイコン&#x200B;**をクリック&#x200B;**[!UICONTROL Push Channel settings]**します。
10. サーバーキーをサーバーキーフィールドに貼り付けます。

うまくいけばSUCCESSメッセージが表示されます。

![push-チャネル設定](assets/push-channel-settings.PNG)

要約すると、を作成し、を [!DNL Android App] 使用してに接続し [!DNL Android App] ま [!DNL Firebase]す。 次に、アプリのサーバーキーをAdobe Campaign Standardのモバイルアプリに貼り付け [!DNL Android App] て、とAdobe Campaignしてモバ [!DNL Android] イルアプリを接続しました。
