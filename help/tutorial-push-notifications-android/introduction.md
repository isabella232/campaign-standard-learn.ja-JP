---
title: Android アプリでプッシュ通知を使用する前に
description: このチュートリアルでは、Adobe Campaign からプッシュ通知を送信し、Android アプリでこれらの通知を受信する手順について説明します。
feature: Push
topics: Mobile
kt: 3846
doc-type: tutorial
activity: use
team: TM
translation-type: ht
source-git-commit: 8b968e15b78655ff9ae49f812f10683201559722
workflow-type: ht
source-wordcount: '200'
ht-degree: 100%

---


# Android アプリでプッシュ通知を使用する前に

Adobe Campaign では、iOS および Android モバイルデバイスにパーソナライズおよびセグメント化されたプッシュ通知を送信できます。
これらのメッセージは、Experience Cloud Mobile SDK V4 または Experience Platform SDK を利用して、Adobe Campaign で設定したモバイルアプリケーションで受信されます。
このチュートリアルでは、Adobe Campaign からプッシュ通知を送信し、Android アプリでこれらの通知を受信する手順について説明します。

## 前提条件

* Adobe Campaign Standard 拡張機能を使用して起動プロパティを設定する必要があります。以下のオンラインヘルプに従ってください。
   * [ビデオチュートリアル](https://video.tv.adobe.com/v/26224?quality=12)
   * [ドキュメント](https://docs.adobe.com/content/help/ja-JP/campaign-learn/campaign-standard-tutorials/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.html)

* 対応するプロパティの Adobe Campaign Standard でのステータスが設定済みになっていることを確認します。
* [アクティブな Google Firebase アカウントを持っている](https://firebase.google.com)
* [インストールされた Android Studio の最新バージョン](https://developer.android.com/studio)

## チュートリアルの手順

* [手順 1 - Android アプリを作成](/help/tutorial-push-notifications-android/create-android-app.md)
* [手順 2 - モバイル SDK を統合](/help/tutorial-push-notifications-android/integrating-with-mobile-sdk.md)
* [手順 3 - モバイルアプリに拡張機能を登録](/help/tutorial-push-notifications-android/register-mobile-extensions.md)
* [手順 4 - プッシュ識別子を設定](/help/tutorial-push-notifications-android/set-push-identifier.md)
* [手順 5 - 通知を反映](/help/tutorial-push-notifications-android/propagate-notification.md)
* [手順 6 - プッシュ通知を送信](/help/tutorial-push-notifications-android/send-push-notification.md)
