---
title: Adobe Campaign Standard（ACS）でのプライバシーリクエスト ー 概要
description: チュートリアルでは、Adobe Campaign Standard（ACS）インターフェイスでプライバシリクエストを作成する方法について説明します。
feature: GDPR, CCAP
topic: Privacy
kt: 1480
doc-type: feature video
activity: use
team: TM
translation-type: ht
source-git-commit: 556bff4c94e16d3a94561dee1ccb311bc003b631
workflow-type: ht
source-wordcount: '371'
ht-degree: 100%

---


# Adobe Campaign Standard ユーザーインターフェイスでのプライバシーリクエスト

Adobe Campaign では、GDPR（General Data Protection Regulation）や CCPA（California Consumer Privacy Act）などのプライバシー法に準拠して、PII データのプライバシーアクセスおよび削除リクエストを実行するための 3 つの方法をデータコントローラーに提供しています。

* **Privacy Core Service 統合を使用する：** [!UICONTROL Privacy Service] からすべての Experience Cloud ソリューションにプッシュされたプライバシーリクエストは、 専用のワークフローを通じて Campaign によって自動的に処理されます。Privacy Core Service からプライバシーリクエストを作成する方法については、 [Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html) を参照してください。

* **API を使用する：** Adobe Campaign では、REST を使用したプライバシーリクエストの自動処理を可能にする API を提供しています。

* **Adobe Campaign インターフェイスを使用する：**&#x200B;データ管理者は、プライバシーリクエストごとに Adobe Campaign で新しいプライバシーリクエストを作成します。

>[!NOTE]
>
> **ACS 19.4 での変更点：**
> 
> [Privacy Service 統合](https://adobe.io/apis/cloudplatform/gdpr.html)は、すべてのアクセスリクエストおよび削除リクエストに対して使用すべき方法です。19.4 以降、アクセスリクエストと削除リクエストに対する Campaign API およびインターフェイスの使用は非推奨（廃止予定）になりました。Campaign Standard の廃止および削除された機能の詳細については、 [こちらのページ](https://helpx.adobe.com/jp/campaign/kb/acs-deprecated-and-removed-features.html)を参照してください。
>
>**個人情報の販売のオプトアウト（CCPA）**
>
>19.4 以降、Campaign インターフェイスおよび API で、「CCPA オプトアウト」フィールドが標準で提供されます。19.3 の場合、この情報を活用するには Adobe Campaign Standard でこのフィールドを作成する必要があります。詳しくは、 [詳細なドキュメント](https://helpx.adobe.com/jp/campaign/kb/acs-privacy.html#ccpa)を参照してください。
>
> バージョンを確認するには、インターフェイスの右上にある ? アイコンをクリックし、「バージョン情報」を選択します。

## ビデオチュートリアル

### プライバシーリクエストの前提条件

1. [名前空間の作成](/help/privacy/namespaces-for-privacy-requests.md)
1. [カスタムリソースの変更](/help/privacy/custom-resources-for-privacy-requests.md)

### Adobe Campaign ユーザーインターフェイスを通じたプライバシーリクエストの作成、追跡、実行

* [Adobe Campaign ユーザーインターフェイスを使用したプライバシーリクエストの作成と追跡](/help/privacy/create-and-track-privacy-requests.md)
* [プライバシーリクエストの実行](/help/privacy/execute-privacy-requests.md)

## その他のリソース

* [Adobe Campaign の一般的なプライバシーガイドライン](https://helpx.adobe.com/jp/campaign/kb/campaign-privacy-overview.html)
* [ACS の CCPA](https://helpx.adobe.com/jp/campaign/kb/acs-privacy.html#ccpa)
* [Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html)
* [Adobe Campaign Standard REST API ドキュメント](https://final-docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#privacy-management)
