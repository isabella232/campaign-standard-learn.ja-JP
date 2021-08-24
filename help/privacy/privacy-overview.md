---
title: Adobe Campaign Standard（ACS）でのプライバシーリクエスト ー 概要
description: このチュートリアルでは、 Adobe Campaign Standardインターフェイスを使用したプライバシーリクエストの作成方法を説明します。
feature: プライバシーツール
kt: 1480
doc-type: feature video
activity: use
team: TM
exl-id: fb766403-694c-4a7b-b3d1-4a418df85891
source-git-commit: 481cbdcc9ac7446cc36fbff6e3d6e43fe333d30b
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 62%

---

# Adobe Campaign Standard ユーザーインターフェイスでのプライバシーリクエスト

Adobe Campaign では、GDPR（General Data Protection Regulation）や CCPA（California Consumer Privacy Act）などのプライバシー法に準拠して、PII データのプライバシーアクセスおよび削除リクエストを実行するための 3 つの方法をデータコントローラーに提供しています。

* **Privacy Core Service 統合を使用する：** [!UICONTROL Privacy Service] からすべての Experience Cloud ソリューションにプッシュされたプライバシーリクエストは、 専用のワークフローを通じて Campaign によって自動的に処理されます。Privacy Core Serviceからプライバシーリクエストを作成する方法については、[Adobe Experience Platform Privacy Service](https://www.adobe.io/apis/experienceplatform/gdpr.html)を参照してください。

* **API を使用する：** Adobe Campaign では、REST を使用したプライバシーリクエストの自動処理を可能にする API を提供しています。

* **Adobe Campaignインターフェイスを使用する：** データ管理者は、プライバシーリクエストごとにAdobe Campaignでプライバシーリクエストを作成できます

>[!NOTE]
>
> **ACS 19.4 での変更点：**
> 
> [Privacy Service 統合](https://www.adobe.io/apis/experienceplatform/gdpr.html)は、すべてのアクセスリクエストおよび削除リクエストに対して使用すべき方法です。19.4 以降、アクセスリクエストと削除リクエストに対する Campaign API およびインターフェイスの使用は非推奨（廃止予定）になりました。Campaign Standard の廃止および削除された機能の詳細については、 [こちらのページ](https://experienceleague.adobe.com/docs/campaign-standard/using/release-notes/deprecated-features.html?lang=en)を参照してください。
>
>**個人情報の販売のオプトアウト（CCPA）**
>
> CampaignインターフェイスおよびAPIに、「CCPAオプトアウト」フィールドが標準で用意されています。
>
> バージョンを確認するには、**をクリックします。**&#x200B;インターフェイスの右上にある ? アイコンをクリックし、「バージョン情報」を選択します。

## ビデオチュートリアル

### プライバシーリクエストの前提条件

1. [名前空間の作成](/help/privacy/namespaces-for-privacy-requests.md)
1. [カスタムリソースの変更](/help/privacy/custom-resources-for-privacy-requests.md)

### Adobe Campaignユーザーインターフェイスを使用したプライバシーリクエストの作成、追跡、実行

* [Adobe Campaign ユーザーインターフェイスを使用したプライバシーリクエストの作成と追跡](/help/privacy/create-and-track-privacy-requests.md)
* [プライバシーリクエストの実行](/help/privacy/execute-privacy-requests.md)

## その他のリソース

* [Adobe Campaign の一般的なプライバシーガイドライン](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/privacy/privacy-management.html?lang=en#getting-started)
* [ACS の CCPA](https://experienceleague.adobe.com/docs/campaign-standard/using/getting-started/privacy/privacy-requests.html?lang=en#privacy-requests)
* [Adobe Experience Platform Privacy Service](https://www.adobe.io/apis/experienceplatform/gdpr.html)
* [Adobe Campaign Standard REST API ドキュメント](https://final-docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#privacy-management)
