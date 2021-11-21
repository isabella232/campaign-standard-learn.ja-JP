---
title: アプリ内メッセージの概要
description: モバイルアプリケーション内での顧客のリアルタイム動作に応じて、コンテキスト上関連のアプリ内メッセージをユーザーに表示する方法を説明します。
feature: In App
kt: 1911
doc-type: feature video
activity: use
team: TM
exl-id: c51716eb-7239-4fc0-9ccf-9f5f0a5fae65
role: User
level: Beginner
source-git-commit: 30e8e10575aad4dcf2b0473cdd9fd6d5fc2815f4
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 12%

---

# の概要 [!UICONTROL In-App] メッセージ {#introduction}

この [!UICONTROL In-App Messaging] channel を使用すると、モバイルアプリケーション内でユーザーがアクティブな場合にメッセージを表示できます。 このチャネルを使用するには、モバイルアプリケーションがと統合されている必要があります [!UICONTROL Adobe Experience Platform SDK].

このチュートリアルでは、モバイルプロパティを設定するために必要な手順、 [!UICONTROL Launch] の拡張 [!UICONTROL In-App Messaging] チャネルと、準備、カスタマイズ、送信の方法 [!UICONTROL In-App] Adobe Campaign Standardのメッセージ。 このリンクから、ハイライト表示された各トピックのビデオチュートリアルに進みます。

## 前提条件 {#prerequisites}

1. 次にアクセスできることを確認します： **[!UICONTROL In-App]** チャネル。 これらのチャネルにアクセスできない場合は、アカウントチームにお問い合わせください。
1. を確認します。 **ユーザー** 必要な **権限** Adobe Campaign Standardおよび [!UICONTROL Launch].

   1. Adobe Campaign Standardで、IMS ユーザーが [!UICONTROL Standard User] および [!UICONTROL Administrator] グループ。

      この手順を使用すると、ユーザーはAdobe Campaign Standardにログインし、Experience PlatformSDK モバイルアプリページに移動して、で作成したモバイルアプリのプロパティを表示できます。 [!UICONTROL Launch].

   1. In [!UICONTROL Launch]を使用する場合、IMS ユーザーが [!UICONTROL Launch] 製品プロファイル。 この手順では、にログインできます。 [!UICONTROL Launch] をクリックして、プロパティを作成および表示します。 製品プロファイルには、会社やプロパティに対する権限は設定されていませんが、ユーザーは引き続きログインできます。

1. Adobe Experience Platform Launch:

   1. モバイルプロパティを作成し、モバイルアプリにExperience PlatformSDK を実装することで、モバイルアプリを作成します。
   1. のインストール **Adobe Campaign Standard** モバイルアプリケーション用の拡張機能。

拡張機能について詳しくは、 [AdobeLaunch でのCampaign Standard拡張機能の設定](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard) 」を参照してください。

## 設定の手順 [!UICONTROL In-App] メッセージ {#steps-to-set-up}

1. [Adobe Experience Platform SDK を使用したモバイルアプリの設定](/help/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.md).
1. [イベントの設定](/help/communication-channels/mobile/in-app/configure-events.md).

## 作成、管理、公開 [!UICONTROL In-App] 配信 {#create-manage-publish}

アプリ内配信は、 **[!UICONTROL Create an In-App Message]** カードをホームページから [!UICONTROL Marketing Activities]または、 [ワークフロー内でのアプリ内配信の作成](/help/communication-channels/mobile/in-app/in-app-activity.md).

配信を設定する際に、異なる配信テンプレートから選択して、次の 3 つのオプションでユーザーをターゲティングできます。

1. [**アプリ内メッセージのブロードキャスト**](/help/communication-channels/mobile/in-app/broadcast-in-app-message.md) モバイルアプリのすべてのユーザーをターゲットに設定します。

   このメッセージタイプでは、Adobe Campaignにプロファイルが存在しない場合でも、モバイルアプリケーションのすべてのユーザー（現在のユーザーも将来のユーザーも含む）にメッセージを送信できます。 したがって、ユーザープロファイルがAdobe Campaignに存在するとは限らないので、メッセージをカスタマイズする場合はパーソナライゼーションはできません。

1. すべてのユーザーをモバイルアプリのプロファイルに基づいてターゲット設定します。

   このメッセージタイプでは、Adobe Campaignにモバイルプロファイルを持つモバイルアプリの既知のユーザーや匿名ユーザーすべてをターゲットにすることができます。 このメッセージタイプは、個人情報も機密性も含まない属性のみを使用してパーソナライズできるので、Mobile SDK と Adobe Campaign のアプリ内メッセージングサービスの間にセキュリティで保護されたハンドシェイクは必要ありません。したがって、パーソナライゼーション戦略は、ユーザーがデバイスとやり取りする際に学んだことに基づいています。 例えば、1 週間に 5 回以上アプリを起動したすべてのユーザーをターゲットに設定します。

1. [**Campaign プロファイルに基づいたターゲットユーザー**](/help/communication-channels/mobile/in-app/target-users-based-on-campaign-profile.md).

   このメッセージタイプでは、モバイルアプリケーションを購読しているAdobe Campaignプロファイル（CRM プロファイル）をターゲットにすることができます。 Adobe Campaignで使用可能なすべてのプロファイル属性を使用して、メッセージをパーソナライズできます。 個人情報と機密情報を含むメッセージを承認されたユーザーのみが使用するようにするには、Mobile SDK と Campaign のアプリ内メッセージサービスの間に安全なハンドシェイクが必要です。

このテンプレートは、電子メールやプッシュなどの他のチャネルのユーザーを既にターゲットにしているクロスチャネルオーケストレーションの使用例をサポートするのに役立ちます。 その後、応答に基づいて、アプリ内メッセージで顧客を惹きつける必要があります。

## アプリ内配信のレポート {#report}

配信が公開されると、次の操作が可能になります [アプリ内配信のレポート](/help/communication-channels/mobile/in-app/in-app-reporting.md).

## その他のリソース

* [アプリ内レポート](https://experienceleague.adobe.com/docs/campaign-standard/using/reporting/list-of-reports/in-app-report.html?lang=en)
* [モバイルプロパティの設定](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property)
* [Adobe Experience Platform SDK を使用したモバイルアプリケーションの設定](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/configuring-channels/configuring-a-mobile-application.html?lang=en)
* [アプリ内メッセージの準備と送信](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/in-app-messaging/preparing-and-sending-an-in-app-message.html?lang=en)
* [アプリ内メッセージのカスタマイズ](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/in-app-messaging/customizing-an-in-app-message.html?lang=en)
* [ワークフロー内でのアプリ内メッセージの送信](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/channel-activities/in-app-delivery.html?lang=en)
* [ライフサイクル指標の有効化](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
