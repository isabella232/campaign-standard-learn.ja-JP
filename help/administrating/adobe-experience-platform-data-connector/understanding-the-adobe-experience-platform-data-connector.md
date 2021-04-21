---
title: Adobe Experience Platform コネクタについて
description: Adobe Experience PlatformData Connectorは、XTKデータ(キャンペーンで取り込まれたデータ)をAdobe Experience Platformのエクスペリエンスデータモデル(XDM)データにマッピングすることで、既存のお客様がAdobe Experience Platformでデータを利用できるようにします。
feature: Adobe Experience Platform Data Connector
kt: 2826
thumbnail: 27304.jpg
doc-type: feature video
activity: understand
team: TM
exl-id: 686961f9-5374-4cc6-8b36-7ee0584ea720
translation-type: tm+mt
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 11%

---

# Adobe Experience Platformについて[!UICONTROL Data Connector]

>[!NOTE]
>
>この機能は現在ベータ版であり、予告なく頻繁に更新や変更が行われる場合があります。
>
>この機能を実装する予定の場合は、[!UICONTROL Adobe Customer Support]にお問い合わせください。

## 概要

Adobe Experience Platform[!UICONTROL Data Connector]は、XTKデータ(Adobe Campaignで取り込まれたデータ)をAdobe Experience Platformの[!DNL Experience Data Model] (XDM)データにマッピングすることで、既存のお客様がAdobe Experience Platformでデータを入手できるように支援します。

コネクタは単方向であり、データをAdobe Campaign StandardからAdobe Experience Platformに送信します。 データはAdobe Experience PlatformからAdobe Campaign Standardに送られません。

Adobe Experience Platform[!UICONTROL Data Connector]は、Adobe Campaign Standard[!UICONTROL custom resources]を理解し、お客様の全体的なデータスキーマがAdobe Experience Platform内でどのように行われるべきかを理解しているデータエンジニアを対象としています。

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12)

*このビデオでは、Adobe Experience Platformの概要を説明 [!UICONTROL Data Connector] する（09:35分）*

>[!NOTE]
>
>[!UICONTROL subscription events]の既製の転送はサポートされていません。 [!UICONTROL subscription events]を転送するには、対応するXDMとデータセットをAdobe Experience Platform上に作成し、これらのデータに対するカスタムデータマッピングを設定します。
>
>既存の[!UICONTROL experience events]はAdobe Experience Platformに取り込めませんが、継続中の生成[!UICONTROL experience events]はAdobe Experience Platformにストリーミングされます。

## データマッピングを実行するための主な手順

次のチュートリアルでは、Campaign StandardとAdobe Experience Platformの間のデータマッピングを実行する主な手順を説明します。

1. [カスタムリソースのマッピング](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [エクスペリエンスイベントのマッピング](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [シードテーブルデータのマッピング](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [データ・マッピングの変更](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [データ取得ジョブのステータスの確認](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

## その他のリソース

* [Adobe Experience Platform Data Connector について](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-about-data-connector.html)
* [エクスペリエンスデータモデルの概要](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-data-model-overview.html)
* [マッピング定義](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-definition.html)
* [マッピングのアクティベーション](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-activation.html)
* [API によるデータ取得トリガー](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-triggering-data-ingestion.html)
