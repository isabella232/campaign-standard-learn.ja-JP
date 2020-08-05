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
ht-degree: 7%

---


# Adobe Campaign Standardユーザーインターフェイスでのプライバシー要求

Adobe Campaignオファーデータは、GDPR(General Data Protection Regulation)やCCPA(California Consumer Privacy Act)などのプライバシー行為に従って、PIIデータのプライバシーアクセスおよび削除の要求を実行する3つの方法を制御します。

* **プライバシーコアサービスの統合を使用：** からすべてのExperience Cloudソリューション [!UICONTROL Privacy Service] に送信されるプライバシー要求は、専用のワークフローを介してキャンペーンによって自動的に処理されます。 Refer to the [Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html) to learn how to create privacy requests from the Privacy Core Service

* **APIを使用：** Adobe Campaignは、RESTを使用してプライバシー要求を自動的に処理するAPIを提供します

* **Adobe Campaignインターフェイスを使用：** 各プライバシーリクエストに対して、データコントローラーはAdobe Campaignに新しいプライバシーリクエストを作成します

>[!NOTE]
>
> **ACS 19.4での変更：**
> 
> [Privacy Service統合は](https://adobe.io/apis/cloudplatform/gdpr.html) 、すべてのアクセスおよび削除リクエストに対して使用する必要がある方法です。 19.4 以降、アクセス要求および削除要求に対する Campaign API およびインターフェイスの使用は廃止されます。廃止および削除された機能のCampaign Standardについて詳しくは、 [このページを参照してください](https://helpx.adobe.com/jp/campaign/kb/acs-deprecated-and-removed-features.html)。
>
>**個人情報(CCPA)の販売のオプトアウト**
>
>19.4以降、キャンペーンインターフェイスおよびAPIでは、CCPAオプトアウトフィールドがすぐに使用できます。 19.3の場合、この情報を活用するには、Adobe Campaign Standardでこのフィールドを作成する必要があります。 詳しくは、 [詳細なドキュメント](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ccpa) を参照してください。
>
> バージョンを確認するには、 アイコンをクリックし、「バージョン情報」を選択します。

## ビデオTutorials

### プライバシーリクエストの前提条件

1. [名前空間の作成](/help/privacy/namespaces-for-privacy-requests.md)
1. [カスタムリソースの変更](/help/privacy/custom-resources-for-privacy-requests.md)

### Adobe Campaignのユーザーインターフェイスを通じて、プライバシーリクエストを作成、追跡、実行します。

* [Adobe Campaignユーザーインターフェイスを使用したプライバシーリクエストの作成と追跡](/help/privacy/create-and-track-privacy-requests.md)
* [プライバシー要求の実行](/help/privacy/execute-privacy-requests.md)

## その他のリソース

* [キャンペーンに関する一般的なプライバシーガイドライン](https://helpx.adobe.com/jp/campaign/kb/campaign-privacy-overview.html)
* [ACS用CCPA](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ccpa)
* [Adobe Experience Platformプライバシーサービス](https://adobe.io/apis/cloudplatform/gdpr.html)
* [Adobe Campaign StandardREST APIドキュメント](https://final-docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#privacy-management)
