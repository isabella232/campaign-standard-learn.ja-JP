---
title: 手順1 - Androidアプリを作成し、Firebase Cloud Messagingを使用するように設定する
description: この部分では、Adobe Campaign Standardから送られる [!DNL Android] App to receive [!UICONTROL Push notifications] を作成します。 プッシュ通知を受け取るには、アプリをGoogleの [!DNL Firebase Cloud Service]に登録する必要があります。
feature: Push
topics: Mobile
kt: 4825
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: cdd78e97f2769503d3d4f26933ccc7f35e9b20b9
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 2%

---


# 手順1 - [!DNL Android]アプリを作成し、[!DNL Firebase Cloud Messaging]を使用するように設定する

この部分では、[!DNL Android]アプリを作成して、Adobe Campaign Standardから送信された[!UICONTROL Push notifications]を受信します。 プッシュ通知を受け取るには、アプリをGoogleの[!DNL Firebase Cloud Service]に登録する必要があります。

1. [!DNL Firebase]アカウントにログインします。

   [!DNL Firebase] は、高品質のアプリをすばやく開発できるGoogleのモバイルプラットフォームです。[!DNL Firebase]アカウントをお持ちでない場合は、[をここから1つ作成してください。](https://firebase.google.com)

2. 開始 [!DNL Android Studio]
3. **[!UICONTROL File]**/**[!UICONTROL New]**/**[!UICONTROL New Project]をクリックします。**
4. 「**[!UICONTROL Empty Activity]**」を選択し、「**[!UICONTROL Next]」をクリックします。**

   ![android-project](assets/android-project.PNG)

5. プロジェクトに意味のある名前を付けます。

   このデモの目的で、プロジェクトの名前を&#x200B;*[!DNL ACSPushTutorial]*&#x200B;にしました。

   ![android-project-configuration](assets/android-project-configuration.PNG)

6. デフォルトのパッケージ名をそのまま使用し、**[!DNL Finish]**&#x200B;をクリックしてプロジェクトを作成します。
7. プロジェクト構造は、次のスクリーンショットのようになります

   ![android-project-structure](assets/android-project-structure.PNG)

8. クリック **[!UICONTROL Tools]** > **[!UICONTROL Firebase].** (これにより、プロジェクトがに追加され [!DNL Firebase]ます)
9. 「**[!UICONTROL Set up Firebase Cloud Messaging]」をクリックします。**

   ![firebaseの設定](assets/android-project-firebase-messaging.PNG)

10. 「**[!UICONTROL Connect to Firebase]」をクリックします。**
11. アプリケーションがFirebaseに接続されたら、**[!UICONTROL Add FCM to your app]をクリックします。**
12. 「**[!UICONTROL Accept Changes]」をクリックします。**

   アプリにFCMを追加する場合、ウィザードでプロジェクトに変更を加えるための権限が必要です。

   ![[!DNL add-fcm-to-your-app]](assets/firebase-add-fcm-to-app.PNG)

アプリケーションとFirebaseの統合に成功したら、次のようなメッセージが表示されます。

![[!DNL fcm-successfull]](assets/android-firebase-success.PNG)

[プロジェクトがコンソールに表示されていることを確認 [!DNL Firebase ]します](https://console.firebase.google.com/)

## [!UICONTROL Push Channel]設定を構成

1. [!DNL Firebase]コンソールにログイン
2. **[!UICONTROL ACSPushTutorial]**&#x200B;プロジェクトを開きます。
3. **歯車アイコン**&#x200B;をクリックし、プロジェクト設定を開きます

   ![project-settings](assets/firebase-project-settings.PNG)

4. **[!UICONTROL Cloud Messaging]**&#x200B;タブにタブ移動します。
5. サーバーキーをコピーします

   ![サーバーキー](assets/firebase-server-key.PNG)

6. Adobe Campaign Standardインスタンスにログインします
7. **[!UICONTROL Adobe Campaign]**/**[!UICONTROL Administration]**/**[!UICONTROL Channels]**/**[!UICONTROL Mobile App]をクリックします。**
8. 適切な&#x200B;**[!UICONTROL Mobile Application Property]を選択します。**
9. **[!UICONTROL Push Channel settings]**&#x200B;セクションの&#x200B;**[!DNL Android]アイコン**&#x200B;をクリックします。
10. サーバーキーをサーバーキーフィールドに貼り付けます。

うまくいけばSUCCESSメッセージが表示されます。

![push-チャネル設定](assets/push-channel-settings.PNG)

要約すると、[!DNL Android App]を作成し、[!DNL Android App]を[!DNL Firebase]に接続しました。 次に、[!DNL Android]アプリのサーバーキーをAdobe Campaign Standardのモバイルアプリに貼り付けて、[!DNL Android App]とAdobe Campaignしてモバイルアプリを接続しました。
