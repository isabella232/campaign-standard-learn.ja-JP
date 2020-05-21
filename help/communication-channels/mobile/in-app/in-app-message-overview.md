---
title: アプリ内メッセージの概要
description: Adobe Campaign標準(ACS)のアプリ内メッセージチャネルを使用すると、モバイルアプリ内での顧客のリアルタイム動作に応じて、文脈で関連するアプリ内メッセージをユーザーに提示できます。
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
ht-degree: 1%

---


# メッセージの概 [!UICONTROL In-App] 要 {#introduction}

この [!UICONTROL In-App Messaging] チャネルを使用すると、モバイルアプリケーション内でユーザーがアクティブな場合にメッセージを表示できます。 このチャネルを使用するには、モバイルアプリケーションがと統合されている必要があり [!UICONTROL Adobe Experience Platform SDK]ます。

このチュートリアルでは、モバイルプロパティの設定に必要な手順、 [!UICONTROL Launch] チャネルの拡張機能の設定、およびMessage Standardでの [!UICONTROL In-App Messaging][!UICONTROL In-App] メッセージの準備、カスタマイズ、送信方法について説明します。 リンクからは、強調表示された各トピックのビデオチュートリアルに進むことができます。

## 前提条件 {#prerequisites}

1. 必ず **[!UICONTROL In-App]** チャネルにアクセスできることを確認してください。 これらのチャネルにアクセスできない場合は、アカウントチームにお問い合わせください。
1. Adobe Campaign **が** Standardおよびで必要な **権限を持っていることを確認します**[!UICONTROL Launch]。

   1. Adobe Campaign標準で、IMSユーザーが [!UICONTROL Standard User] および [!UICONTROL Administrator] グループに属していることを確認します。\
      この手順では、Adobe Campaign標準にログインし、Experience Platform SDKモバイルアプリページに移動して、で作成したモバイルアプリのプロパティを表示でき [!UICONTROL Launch]ます。
   1. で、IMSユーザー [!UICONTROL Launch]が [!UICONTROL Launch] 製品プロファイルの一部であることを確認します。\
      この手順では、ログインしてプロパティを作成し、表示 [!UICONTROL Launch] できます。 の製品プロファイルについて詳し [!UICONTROL Launch]くは、「製品プロファイルの [作成](https://docs.adobelaunch.com/launch-reference/administration/user-permissions#3-create-your-product-profile)」を参照してください。 製品プロファイルでは、会社やプロパティに権限が設定されていないはずですが、ユーザーはログイン可能です。

1. Adobe Experience Platform Launch:

   1. モバイルプロパティを作成し、モバイルアプリをExperience Platform SDKに実装して、モバイルアプリを作成します。
   1. モバイルアプリケーション用の **Adobe Campaign標準** (Standard)拡張機能をインストールします。

拡張機能について詳しくは、ドキュメントの「Adobe Launchでの [Campaign Standard拡張の](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard) 設定 [!UICONTROL Adobe Launch ]」を参照してください。

## メッセージを設定する手順 [!UICONTROL In-App] です {#steps-to-set-up}

1. [Adobe Experience Platform SDK](/help/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.md)。

1. [イベントの設定](/help/communication-channels/mobile/in-app/configure-events.md)。

## 配信の作成、管理および公開 [!UICONTROL In-App] {#create-manage-publish}

ホームページの **[!UICONTROL Create an In-App Message]** カードをクリックするか、からアプリ内配信を1回だけ作成する [!UICONTROL Marketing Activities]か、ワークフロー内でアプリ内配信を [作成できます](/help/communication-channels/mobile/in-app/in-app-activity.md)。

配信を設定する場合、異なる配信テンプレートから選択してターゲットを行うには、次の3つの方法があります。

1. [**アプリ内メッセージのターゲット&#x200B;**](/help/communication-channels/mobile/in-app/broadcast-in-app-message.md)（モバイルアプリのすべてのユーザー）へのブロードキャスト。

   このメッセージタイプを使用すると、Adobe Campaignに既存のプロファイルがない場合でも、モバイルアプリのすべてのユーザー（現在または将来）にメッセージを送信できます。 したがって、Adobe Campaignにユーザプロファイルが必ずしも存在しないので、メッセージをカスタマイズする場合は、パーソナライゼーションは不可能です。

1. モバイルアプリのプロファイルに基づいて、すべてのユーザーをターゲットします。

   このメッセージタイプを使用すると、モバイルプロファイルをAdobe Campaignに持つモバイルアプリの既知ユーザーまたは匿名ユーザー全員をターゲットできます。 このメッセージタイプは、個人属性と機密属性のみを使用してパーソナライズでき、モバイルSDKとAdobe Campaignのアプリ内メッセージサービス間の安全なハンドシェイクは必要ありません。 したがって、パーソナライゼーション戦略は、ユーザーがデバイスとやり取りすることでユーザーについて学んだことに基づいています。 例えば、先週5回以上アプリを起動したすべてのユーザーにターゲットを送信します。

1. [**キャンペーンプロファイルに基づくターゲットユーザー&#x200B;**](/help/communication-channels/mobile/in-app/target-users-based-on-campaign-profile.md)。

   このメッセージタイプを使用すると、モバイルアプリケーションを購読しているターゲットAdobe Campaignプロファイル(CRMプロファイル)を使用できます。 メッセージは、使用可能なすべてのプロファイル属性を使用してAdobe Campaignでパーソナライズできますが、個人情報と機密情報を含むメッセージが権限のあるユーザーのみに使用されるように、モバイルSDKとキャンペーンのアプリ内メッセージサービスとの間で安全なハンドシェイクが必要です。

このテンプレートは、電子メールやプッシュなどの他のチャネルをターゲットにし、その応答に基づいて既にチャネルをアプリ内メッセージに関連付ける場合など、クロスユーザーオーケストレーションの使用例をサポートするのに役立ちます。

## アプリ内配信のレポート {#report}

配信が公開されると、アプリ内配信に関する [レポートを作成できます](/help/communication-channels/mobile/in-app/in-app-reporting.md)。

## その他のリソース

* [アプリ内レポート](https://docs.adobe.com/content/help/en/campaign-standard/using/reporting/list-of-reports/in-app-report.html)
* [モバイルプロパティの設定](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property)
* [Adobe Experience Platform SDKを使用したモバイルアプリケーションの設定](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html)
* [アプリ内メッセージの準備と送信](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/preparing-and-sending-an-in-app-message.html)
* [アプリ内メッセージのカスタマイズ](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/customizing-an-in-app-message.html)
* [ワークフロー内でのアプリ内メッセージの送信](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/channel-activities/in-app-delivery.html)
* [ライフサイクル指標の有効化](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
