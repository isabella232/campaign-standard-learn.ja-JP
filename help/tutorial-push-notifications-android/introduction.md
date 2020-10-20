---
title: Androidアプリでプッシュ通知を使用する前に
description: このチュートリアルでは、Adobe Campaign からプッシュ通知を送信し、Android アプリでこれらの通知を受信する手順について説明します。
feature: Push
topics: Mobile
kt: 3846
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 6c88336d9c02faa683973d74ec21e38622afdf3f
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 41%

---

# Androidアプリでプッシュ通知を使用する前に

Adobe Campaign では、iOS および Android モバイルデバイスにパーソナライズおよびセグメント化されたプッシュ通知を送信できます。これらのメッセージは、Experience CloudMobile SDK V4またはExperience PlatformSDKを利用して、Adobe Campaignで設定したモバイルアプリケーションで受信されます。
このチュートリアルでは、Adobe Campaign からプッシュ通知を送信し、Android アプリでこれらの通知を受信する手順について説明します。

## 前提条件

* Adobe Campaign Standard拡張機能を使用して起動プロパティを設定する必要があります。 以下のオンラインヘルプに従ってください。
   * [ビデオチュートリアル](https://video.tv.adobe.com/v/26224?quality=12&captions=jpn)
   * [ドキュメント](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.html)

* 対応するプロパティのAdobe Campaign Standardでのステータスが設定済みになっていることを確認します。
* [アクティブなGoogle Firebaseアカウントを持っている](https://firebase.google.com)
* [インストールされたAndroid Studioの最新バージョン](https://developer.android.com/studio)

## チュートリアルの手順

* [手順 1 - Android アプリを作成](/help/tutorial-push-notifications-android/create-android-app.md)
* [手順 2 - モバイル SDK を統合](/help/tutorial-push-notifications-android/integrating-with-mobile-sdk.md)
* [手順3 — モバイルアプリに拡張機能を登録する](/help/tutorial-push-notifications-android/register-mobile-extensions.md)
* [手順 4 - プッシュ識別子を設定](/help/tutorial-push-notifications-android/set-push-identifier.md)
* [手順 5 - 通知を反映](/help/tutorial-push-notifications-android/propagate-notification.md)
* [手順6 — プッシュ通知を送信する](/help/tutorial-push-notifications-android/send-push-notification.md)
