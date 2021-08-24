---
title: Android™アプリでのプッシュ通知の概要
description: このチュートリアルでは、プッシュ通知を Adobe Campaign から送信し、Android™ アプリで受信する手順について説明します。
feature: プッシュ
kt: 3846
doc-type: tutorial
activity: use
team: TM
exl-id: 8dd772b2-b082-4e1e-842d-c5d6bcec564c
source-git-commit: 481cbdcc9ac7446cc36fbff6e3d6e43fe333d30b
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 60%

---

# Android™アプリでのプッシュ通知の概要

Adobe Campaignでは、iOSおよびAndroid™のモバイルデバイスにパーソナライズおよびセグメント化されたプッシュ通知を送信できます。
これらのメッセージは、Experience CloudMobile SDK V4またはExperience PlatformSDKを使用して、Adobe Campaignで設定したモバイルアプリケーションで受信されます。
このチュートリアルでは、プッシュ通知を Adobe Campaign から送信し、Android™ アプリで受信する手順について説明します。

## 前提条件

* Adobe Campaign Standard 拡張機能を使用して起動プロパティを設定する必要があります。以下のオンラインヘルプに従ってください。
   * [ビデオチュートリアル](https://video.tv.adobe.com/v/26224?quality=12)
   * [ドキュメント](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.html?lang=en)

* 対応するプロパティの Adobe Campaign Standard でのステータスが設定済みになっていることを確認します。
* [アクティブな Google Firebase アカウントを持っている](https://firebase.google.com)
* [最新バージョンのAndroid™ Studioがインストールされています](https://developer.android.com/studio)

## チュートリアルの手順

* [手順1 - Android™アプリを作成する](/help/tutorial-push-notifications-android/create-android-app.md)
* [手順 2 - Mobile SDK の統合](/help/tutorial-push-notifications-android/integrating-with-mobile-sdk.md)
* [手順 3 - モバイルアプリに拡張機能を登録](/help/tutorial-push-notifications-android/register-mobile-extensions.md)
* [手順 4 - プッシュ識別情報の設定](/help/tutorial-push-notifications-android/set-push-identifier.md)
* [手順 5 - 通知の伝達](/help/tutorial-push-notifications-android/propagate-notification.md)
* [手順 6 - プッシュ通知を送信](/help/tutorial-push-notifications-android/send-push-notification.md)
