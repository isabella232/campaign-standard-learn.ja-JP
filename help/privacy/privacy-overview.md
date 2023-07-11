---
title: Adobe Campaign Standard（ACS）でのプライバシーリクエスト ー 概要
description: このチュートリアルでは、Adobe Campaign Standard インターフェイスを使用してプライバシーリクエストを作成する方法について説明します。
feature: Privacy Tools
jira: KT-1480
doc-type: feature video
activity: use
role: Admin
level: Advanced
team: TM
recommendations: noDisplay
exl-id: fb766403-694c-4a7b-b3d1-4a418df85891
source-git-commit: 89f520da0455da693b27c397f95cdabab4552770
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 90%

---

# Adobe Campaign Standard ユーザーインターフェイスでのプライバシーリクエスト

Adobe Campaign では、GDPR（General Data Protection Regulation）や CCPA（California Consumer Privacy Act）などのプライバシー法に準拠して、PII データのプライバシーアクセスおよび削除リクエストを実行するための 3 つの方法をデータコントローラーに提供しています。

* **Privacy Core Service 統合を使用する：** [!UICONTROL Privacy Service] からすべての Experience Cloud ソリューションにプッシュされたプライバシーリクエストは、 専用のワークフローを通じて Campaign によって自動的に処理されます。Privacy Core Service からプライバシーリクエストを作成する方法については、[Adobe Experience Platform Privacy Service](https://developer.adobe.com/apis/experienceplatform/gdpr.html) を参照してください。

* **API を使用する：** Adobe Campaign では、REST を使用したプライバシーリクエストの自動処理を可能にする API を提供しています。

* **Adobe Campaign インターフェイスを使用する：**&#x200B;データ管理者は、プライバシーリクエストごとに、対応するプライバシーリクエストを Adobe Campaign で作成します。

>[!NOTE]
>
> **ACS 19.4 での変更点：**
> 
> この [Privacy Service統合](https://developer.adobe.com/apis/experienceplatform/gdpr.html) は、すべてのアクセス要求および削除要求に使用する必要があるメソッドです。 19.4 以降、アクセスリクエストと削除リクエストに対する Campaign API およびインターフェイスの使用は非推奨（廃止予定）になりました。Campaign Standard の廃止および削除された機能の詳細については、 [こちらのページ](https://experienceleague.adobe.com/docs/campaign-standard/using/release-notes/deprecated-features.html?lang=ja)を参照してください。
>
>**個人情報の販売のオプトアウト（CCPA）**
>
> Campaign インターフェイスおよび API で、「CCPA のオプトアウト」フィールドが標準で提供されています。
>
> バージョンを確認するには、インターフェイスの右上にある **?** アイコンをクリックし、「バージョン情報」を選択します。

## ビデオチュートリアル

### プライバシーリクエストの前提条件

1. [名前空間の作成](/help/privacy/namespaces-for-privacy-requests.md)
1. [カスタムリソースの変更](/help/privacy/custom-resources-for-privacy-requests.md)

### Adobe Campaign ユーザーインターフェイスを使用したプライバシーリクエストの作成、トラッキングおよび実行

* [Adobe Campaign ユーザーインターフェイスを使用したプライバシーリクエストの作成とトラッキング](/help/privacy/create-and-track-privacy-requests.md)
* [プライバシーリクエストの実行](/help/privacy/execute-privacy-requests.md)

## その他のリソース

* [Adobe Campaign の一般的なプライバシーガイドライン](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/privacy/privacy-management.html?lang=ja#getting-started)
* [ACS の CCPA](https://experienceleague.adobe.com/docs/campaign-standard/using/getting-started/privacy/privacy-requests.html?lang=ja#privacy-requests)
* [Adobe Experience Platform Privacy Service](https://developer.adobe.com/apis/experienceplatform/gdpr.html)
* [Adobe Campaign Standard REST API ドキュメント](https://final-docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#privacy-management)
