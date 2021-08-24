---
title: アプリ内メッセージの概要
description: モバイルアプリケーション内での顧客のリアルタイム動作に応じて、コンテキスト上関連性の高いアプリ内メッセージをユーザーに表示する方法を説明します。
feature: アプリ内
kt: 1911
doc-type: feature video
activity: use
team: TM
exl-id: c51716eb-7239-4fc0-9ccf-9f5f0a5fae65
role: User
level: Beginner
source-git-commit: 481cbdcc9ac7446cc36fbff6e3d6e43fe333d30b
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 12%

---

# [!UICONTROL In-App]メッセージの概要 {#introduction}

[!UICONTROL In-App Messaging]チャネルを使用すると、モバイルアプリケーション内でユーザーがアクティブな場合にメッセージを表示できます。 このチャネルを使用するには、モバイルアプリケーションを[!UICONTROL Adobe Experience Platform SDK]と統合する必要があります。

このチュートリアルでは、モバイルプロパティ、[!UICONTROL In-App Messaging]チャネルの[!UICONTROL Launch]拡張機能の設定に必要な手順、Adobe Campaign Standardで[!UICONTROL In-App]メッセージを準備、カスタマイズ、送信する方法について説明します。 このリンクから、ハイライト表示された各トピックに関するビデオチュートリアルが表示されます。

## 前提条件 {#prerequisites}

1. **[!UICONTROL In-App]**&#x200B;チャネルにアクセスできることを確認します。 これらのチャネルにアクセスできない場合は、アカウントチームにお問い合わせください。
2. **ユーザー**&#x200B;がAdobe Campaign Standardおよび[!UICONTROL Launch]で必要な&#x200B;**権限**&#x200B;を持っていることを確認します。

   1. Adobe Campaign Standardで、IMSユーザーが[!UICONTROL Standard User]および[!UICONTROL Administrator]グループに属していることを確認します。\
      この手順を使用すると、ユーザーはAdobe Campaign Standardにログインし、Experience PlatformSDKモバイルアプリページに移動して、[!UICONTROL Launch]で作成したモバイルアプリのプロパティを表示できます。
   2. [!UICONTROL Launch]で、IMSユーザーが[!UICONTROL Launch]製品プロファイルに含まれていることを確認します。 この手順では、ユーザーが[!UICONTROL Launch]にログインして、プロパティを作成および表示できます。 製品プロファイルには、会社やプロパティに権限が設定されていないが、ユーザーは引き続きログインできる。

3. Adobe Experience Platform Launch:

   1. モバイルプロパティを作成し、モバイルアプリにExperience PlatformSDKを実装して、モバイルアプリを作成します。
   2. モバイルアプリケーション用の&#x200B;**Adobe Campaign Standard**&#x200B;拡張機能をインストールします。

拡張機能について詳しくは、ドキュメントの[AdobeLaunchのCampaign Standard拡張機能の設定](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard)を参照してください。

## [!UICONTROL In-App]メッセージの設定手順 {#steps-to-set-up}

1. [Adobe Experience Platform SDK を使用したモバイルアプリの設定](/help/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.md).

2. [イベントの設定](/help/communication-channels/mobile/in-app/configure-events.md)を参照してください。

## [!UICONTROL In-App]配信の作成、管理および公開 {#create-manage-publish}

ホームページから&#x200B;**[!UICONTROL Create an In-App Message]**&#x200B;カードをクリックするか、[!UICONTROL Marketing Activities]から[ワークフロー内にアプリ内配信を作成して、1回だけアプリ内配信を作成できます。](/help/communication-channels/mobile/in-app/in-app-activity.md)

配信を設定する際に、異なる配信テンプレートから選択して、3つのオプションでユーザーをターゲティングできます。

1. [**アプリ内メッセージをブロードキャ**](/help/communication-channels/mobile/in-app/broadcast-in-app-message.md) ストして、モバイルアプリのすべてのユーザーをターゲットにします。

   このメッセージタイプでは、Adobe Campaignにプロファイルが存在しない場合でも、モバイルアプリケーションのすべてのユーザー（現在のユーザーも将来のユーザーも含む）にメッセージを送信できます。 したがって、ユーザープロファイルがAdobe Campaignに存在するとは限らないので、メッセージをカスタマイズする場合はパーソナライゼーションはできません。

2. モバイルアプリプロファイルに基づいてすべてのユーザーをターゲット設定する。

このメッセージタイプでは、Adobe Campaignにモバイルプロファイルを持つモバイルアプリの既知のユーザーや匿名ユーザーをすべてターゲットにすることができます。 このメッセージタイプは、個人情報も機密性も含まない属性のみを使用してパーソナライズできるので、Mobile SDK と Adobe Campaign のアプリ内メッセージングサービスの間にセキュリティで保護されたハンドシェイクは必要ありません。したがって、パーソナライゼーション戦略は、ユーザーがデバイスとやり取りして得た情報に基づいています。 例えば、先週5回以上アプリを起動したすべてのユーザーをターゲットにします。

3. [**Campaign プロファイルに基づいたターゲットユーザー**](/help/communication-channels/mobile/in-app/target-users-based-on-campaign-profile.md).

   このメッセージタイプでは、モバイルアプリケーションを購読しているAdobe Campaignプロファイル（CRMプロファイル）をターゲットにできます。 Adobe Campaignで使用可能なすべてのプロファイル属性を使用して、メッセージをパーソナライズできます。 個人情報と機密情報を含むメッセージが権限のあるユーザーのみによって確実に使用されるようにするには、Mobile SDKとCampaignのアプリ内メッセージサービスの間で安全なハンドシェイクが必要です。

このテンプレートは、電子メールやプッシュなどの他のチャネルで既にユーザーをターゲット設定しているクロスチャネルオーケストレーションの使用例をサポートするのに役立ちます。 その後、その回答に基づいて、アプリ内メッセージを送信します。

## アプリ内配信のレポート {#report}

配信がパブリッシュされると、アプリ内配信](/help/communication-channels/mobile/in-app/in-app-reporting.md)を[レポートできます。

## その他のリソース

* [アプリ内レポート](https://experienceleague.adobe.com/docs/campaign-standard/using/reporting/list-of-reports/in-app-report.html?lang=en)
* [モバイルプロパティの設定](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property)
* [Adobe Experience Platform SDKを使用したモバイルアプリケーションの設定](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/configuring-channels/configuring-a-mobile-application.html?lang=en)
* [アプリ内メッセージの準備と送信](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/in-app-messaging/preparing-and-sending-an-in-app-message.html?lang=en)
* [アプリ内メッセージのカスタマイズ](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/in-app-messaging/customizing-an-in-app-message.html?lang=en)
* [ワークフロー内でのアプリ内メッセージの送信](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/channel-activities/in-app-delivery.html?lang=en)
* [ライフサイクル指標の有効化](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
