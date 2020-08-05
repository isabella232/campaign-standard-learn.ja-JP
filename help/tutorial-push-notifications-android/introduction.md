---
title: Android Appでのプッシュ通知の使用の手引き
description: Adobe Campaign では、iOS および Android モバイルデバイスにパーソナライズおよびセグメント化されたプッシュ通知を送信できます。これらのメッセージは、Experience CloudMobile SDK V4またはExperience PlatformSDKを利用して、Adobe Campaignで設定したモバイルアプリケーションで受信されます。 このチュートリアルでは、Adobe Campaignからプッシュ通知を送信し、Androidアプリでこれらの通知を受信する手順について説明します。
feature: Push
topics: Mobile
kt: 3846
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: a2f194821a9ce06272eaed979ee2d8c62cccac2b
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 14%

---

# Android Appでのプッシュ通知の使用の手引き

Adobe Campaign では、iOS および Android モバイルデバイスにパーソナライズおよびセグメント化されたプッシュ通知を送信できます。これらのメッセージは、Experience CloudMobile SDK V4またはExperience PlatformSDKを利用して、Adobe Campaignで設定したモバイルアプリケーションで受信されます。
このチュートリアルでは、Adobe Campaignからプッシュ通知を送信し、Androidアプリでこれらの通知を受信する手順について説明します。

## 前提条件

* Adobe Campaign Standard拡張機能を使用して起動プロパティを設定する必要があります。 以下のオンラインヘルプに従ってください。
   * [ビデオチュートリアル](https://video.tv.adobe.com/v/26224?quality=12&captions=jpn)
   * [ドキュメント](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.html)

* 対応するプロパティのAdobe Campaign Standardでのステータスが設定済みになっていることを確認します。
* [アクティブなGoogle Firebaseアカウントを持っている](https://firebase.google.com)
* [インストールされたAndroid Studioの最新バージョン](https://developer.android.com/studio)

## チュートリアルの手順

* [手順1 - Androidアプリを作成する](/help/tutorial-push-notifications-android/create-android-app.md)
* [手順2 — モバイルSDKの統合](/help/tutorial-push-notifications-android/integrating-with-mobile-sdk.md)
* [手順3 — モバイルアプリに拡張機能を登録する](/help/tutorial-push-notifications-android/register-mobile-extensions.md)
* [手順4 — プッシュ識別子を設定する](/help/tutorial-push-notifications-android/set-push-identifier.md)
* [手順5 — 通知の伝播](/help/tutorial-push-notifications-android/propagate-notification.md)
* [手順6 — プッシュ通知を送信する](/help/tutorial-push-notifications-android/send-push-notification.md)
