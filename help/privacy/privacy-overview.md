---
title: Adobe Campaign Standard(ACS)とのプライバシー要求 — 概要
description: このチュートリアルでは、Adobe Campaign Standard(ACS)インターフェイスを介したプライバシーの作成リクエストについて説明します。
feature: GDPR, CCAP
topic: Privacy
kt: 1480
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 556bff4c94e16d3a94561dee1ccb311bc003b631
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 24%

---


# Adobe Campaign Standardユーザーインターフェイスでのプライバシー要求

Adobe Campaignオファーデータは、GDPR(General Data Protection Regulation)やCCPA(California Consumer Privacy Act)などのプライバシー行為に従って、PIIデータのプライバシーアクセスおよび削除の要求を実行する3つの方法を制御します。

* **プライバシーコアサービスの統合を使用：すべてのExperience Cloudソリューション** に送信される [!UICONTROL Privacy Service] プライバシー要求は、専用のワークフローを介してキャンペーンによって自動的に処理されます。プライバシーコアサービスからプライバシーリクエストを作成する方法については、[Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html)を参照してください

* **API経由：** Adobe Campaignは、RESTを使用したプライバシーリクエストの自動処理を可能にするAPIを提供します

* **Adobe Campaignインターフェイスを介して：各プライバシー要求** に対して、データコントローラーはAdobe Campaignに新しいプライバシー要求を作成します

>[!NOTE]
>
> **ACS 19.4での変更：**
> 
> [Privacy Service統合](https://adobe.io/apis/cloudplatform/gdpr.html)は、すべてのアクセス要求と削除要求に使用する必要がある方法です。 19.4 以降、アクセス要求および削除要求に対する Campaign API およびインターフェイスの使用は廃止されます。廃止および削除された機能のCampaign Standardについて詳しくは、[このページ](https://helpx.adobe.com/jp/campaign/kb/acs-deprecated-and-removed-features.html)を参照してください。
>
>**個人情報の販売のオプトアウト（CCPA）**
>
>19.4 以降、Campaign インターフェイスおよび API で、「CCPA オプトアウト」フィールドが標準で提供されます。19.3の場合、この情報を活用するには、Adobe Campaign Standardでこのフィールドを作成する必要があります。 詳しくは、[詳細なドキュメント](https://helpx.adobe.com/jp/campaign/kb/acs-privacy.html#ccpa)を参照してください。
>
> バージョンを確認するには、インターフェイスの右上にある ? アイコンをクリックし、「バージョン情報」を選択します。

## ビデオTutorials

### プライバシーリクエストの前提条件

1. [名前空間の作成](/help/privacy/namespaces-for-privacy-requests.md)
1. [カスタムリソースの変更](/help/privacy/custom-resources-for-privacy-requests.md)

### Adobe Campaignのユーザーインターフェイスを通じて、プライバシーリクエストを作成、追跡、実行します。

* [Adobe Campaignユーザーインターフェイスを使用したプライバシーリクエストの作成と追跡](/help/privacy/create-and-track-privacy-requests.md)
* [プライバシー要求の実行](/help/privacy/execute-privacy-requests.md)

## その他のリソース

* [Adobe Campaign の一般的なプライバシーガイドライン](https://helpx.adobe.com/jp/campaign/kb/campaign-privacy-overview.html)
* [ACS の CCPA](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ccpa)
* [Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html)
* [Adobe Campaign StandardREST APIドキュメント](https://final-docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#privacy-management)
