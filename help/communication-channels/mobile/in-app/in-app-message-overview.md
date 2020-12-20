---
title: アプリ内メッセージの概要
description: Adobe Campaign Standard(ACS)のアプリ内メッセージチャネルを使用すると、モバイルアプリ内での顧客のリアルタイム動作に応じて、文脈で関連するアプリ内メッセージをユーザーに提示できます。
feature: In-App
topics: Mobile
kt: 1911
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 82fb2d39dc61a55c0aa20ca1fa215f35a7dd9088
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 12%

---


# [!UICONTROL In-App]メッセージ{#introduction}の紹介

[!UICONTROL In-App Messaging]チャネルを使用すると、モバイルアプリケーション内でユーザーがアクティブな場合にメッセージを表示できます。 このチャネルを使用するには、モバイルアプリケーションを[!UICONTROL Adobe Experience Platform SDK]と統合する必要があります。

このチュートリアルでは、モバイルプロパティの設定に必要な手順、[!UICONTROL In-App Messaging]チャネルの[!UICONTROL Launch]拡張子、およびAdobe Campaign Standardで[!UICONTROL In-App]メッセージを準備、カスタマイズ、送信する方法について説明します。 リンクからは、強調表示された各トピックのビデオチュートリアルに進むことができます。

## 前提条件 {#prerequisites}

1. **[!UICONTROL In-App]**&#x200B;チャネルにアクセスできることを確認します。 これらのチャネルにアクセスできない場合は、アカウントチームにお問い合わせください。
1. **ユーザー**&#x200B;が、Adobe Campaign Standardと[!UICONTROL Launch]で必要な&#x200B;**権限**&#x200B;を持っていることを確認します。

   1. Adobe Campaign Standardで、IMSユーザーが[!UICONTROL Standard User]および[!UICONTROL Administrator]グループに属していることを確認します。\
      この手順では、ユーザーがAdobe Campaign Standardにログインし、Experience PlatformSDKモバイルアプリページに移動して、[!UICONTROL Launch]で作成したモバイルアプリのプロパティを表示できます。
   1. [!UICONTROL Launch]で、IMSユーザーが[!UICONTROL Launch]製品プロファイルの一部であることを確認します。\
      この手順では、ユーザーが[!UICONTROL Launch]にログインして、プロパティを作成し表示できます。 [!UICONTROL Launch]の製品プロファイルについて詳しくは、[製品プロファイルの作成](https://docs.adobelaunch.com/launch-reference/administration/user-permissions#3-create-your-product-profile)を参照してください。 製品プロファイルでは、会社やプロパティに権限が設定されていないはずですが、ユーザーはログイン可能です。

1. Adobe Experience Platform Launch:

   1. モバイルプロパティを作成し、モバイルアプリをExperience PlatformSDKに実装して、モバイルアプリを作成します。
   1. モバイルアプリケーション用の&#x200B;**Adobe Campaign Standard**&#x200B;拡張機能をインストールします。

拡張機能について詳しくは、[!UICONTROL Adobe Launch ]ドキュメントの[Adobeの起動](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard)でCampaign Standard拡張機能を設定するを参照してください。

## [!UICONTROL In-App]メッセージ{#steps-to-set-up}を設定する手順

1. [Adobe Experience Platform SDK を使用したモバイルアプリの設定](/help/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.md).

1. [イベントの設定](/help/communication-channels/mobile/in-app/configure-events.md)。

## [!UICONTROL In-App]配信{#create-manage-publish}を作成、管理、および公開

ホームページの&#x200B;**[!UICONTROL Create an In-App Message]**&#x200B;カードをクリックして、[!UICONTROL Marketing Activities]から1回だけアプリ内配信を作成できます。または、[ワークフロー](/help/communication-channels/mobile/in-app/in-app-activity.md)内でアプリ内配信を作成できます。

配信を設定する場合、異なる配信テンプレートから選択してターゲットを行うには、次の3つの方法があります。

1. [**アプリ内メッセージをブロードキャストして、モバイルアプリのすべてのユーザーにターゲットします。**](/help/communication-channels/mobile/in-app/broadcast-in-app-message.md) 

   このメッセージタイプを使用すると、Adobe Campaignに既存のプロファイルがない場合でも、モバイルアプリのすべてのユーザー（現在または将来）にメッセージを送信できます。 したがって、Adobe Campaignにユーザプロファイルが必ずしも存在しないので、メッセージをカスタマイズする場合は、パーソナライゼーションは不可能です。

1. モバイルアプリのプロファイルに基づいて、すべてのユーザーをターゲットします。

   このメッセージタイプを使用すると、モバイルプロファイルをAdobe Campaignに持つモバイルアプリの既知ユーザーまたは匿名ユーザー全員をターゲットできます。 このメッセージタイプは、個人情報も機密性も含まない属性のみを使用してパーソナライズできるので、Mobile SDK と Adobe Campaign のアプリ内メッセージングサービスの間にセキュリティで保護されたハンドシェイクは必要ありません。したがって、パーソナライゼーション戦略は、ユーザーがデバイスとやり取りすることでユーザーについて学んだことに基づいています。 例えば、先週5回以上アプリを起動したすべてのユーザーにターゲットを送信します。

1. [**Campaign プロファイルに基づいたターゲットユーザー**](/help/communication-channels/mobile/in-app/target-users-based-on-campaign-profile.md).

   このメッセージタイプを使用すると、モバイルアプリケーションを購読しているターゲットAdobe Campaignプロファイル(CRMプロファイル)を使用できます。 メッセージは、使用可能なすべてのプロファイル属性を使用してAdobe Campaignでパーソナライズできますが、個人情報と機密情報を含むメッセージが権限のあるユーザーのみに使用されるように、モバイルSDKとキャンペーンのアプリ内メッセージサービスとの間で安全なハンドシェイクが必要です。

このテンプレートは、電子メールやプッシュなどの他のチャネルをターゲットにし、その応答に基づいて既にチャネルをアプリ内メッセージに関連付ける場合など、クロスユーザーオーケストレーションの使用例をサポートするのに役立ちます。

## アプリ内配信に関するレポート{#report}

配信が公開されると、[アプリ内配信](/help/communication-channels/mobile/in-app/in-app-reporting.md)に関するレポートを作成できます。

## その他のリソース

* [アプリ内レポート](https://docs.adobe.com/content/help/en/campaign-standard/using/reporting/list-of-reports/in-app-report.html)
* [モバイルプロパティの設定](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property)
* [Adobe Experience PlatformSDKを使用したモバイルアプリの設定](https://helpx.adobe.com/jp/campaign/kb/configuring-app-sdk.html)
* [アプリ内メッセージの準備と送信](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/preparing-and-sending-an-in-app-message.html)
* [アプリ内メッセージのカスタマイズ](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/customizing-an-in-app-message.html)
* [ワークフロー内でのアプリ内メッセージの送信](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/channel-activities/in-app-delivery.html)
* [ライフサイクル指標の有効化](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
