---
title: Adobe Experience Platform コネクタについて
description: Adobe Experience Platform Data Connectorを使用すると、XTKデータ（Campaignで取り込んだデータ）をAdobe Experience PlatformのExperience Data Model(XDM)データにマッピングすることで、既存のお客様がAdobe Experience Platformでデータを利用できるようになります。
kt: 2826
thumbnail: 27304.jpg
doc-type: feature video
activity: understand
team: TM
exl-id: 686961f9-5374-4cc6-8b36-7ee0584ea720
source-git-commit: 5a2f8c9a78bf5100b272f9b4461131545b3aeb8b
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 10%

---

# Adobe Experience Platformの理解[!UICONTROL Data Connector]

>[!NOTE]
>
>この機能は現在ベータ版で、予告なく頻繁に更新および変更される可能性があります。
>
>この機能を実装する予定がある場合は、[!UICONTROL Adobe Customer Support]にお問い合わせください。

## 概要

Adobe Experience Platform [!UICONTROL Data Connector]は、既存のお客様がXTKデータ(Adobe Campaignで取り込んだデータ)をAdobe Experience Platformの[!DNL Experience Data Model](XDM)データにマッピングすることで、Adobe Experience Platformでデータを利用できるようにするのを支援します。

コネクタは一方向で、Adobe Campaign StandardからAdobe Experience Platformにデータを送信します。 データはAdobe Experience PlatformからAdobe Campaign Standardに送信されません。

Adobe Experience Platform [!UICONTROL Data Connector]は、Adobe Campaign Standard [!UICONTROL custom resources]を理解し、顧客のデータスキーマ全体をAdobe Experience Platform内に配置する方法を理解できるデータエンジニアを対象としています。

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12)

*このビデオでは、Adobe Experience Platformの概要を説 [!UICONTROL Data Connector] 明します（9:35分）*

>[!NOTE]
>
>[!UICONTROL subscription events]の標準転送はサポートされていません。 [!UICONTROL subscription events]を転送するには、対応するXDMとデータセットをAdobe Experience Platform上に作成し、これらのデータのカスタムデータマッピングを設定します。
>
>既存の[!UICONTROL experience events]はAdobe Experience Platformに取り込めませんが、継続的に生成された[!UICONTROL experience events]はAdobe Experience Platformにストリーミングされます。

## データマッピングを実行するための主な手順

次のチュートリアルでは、Adobe Experience PlatformとCampaign Standardの間でデータマッピングを実行する主な手順を説明します。

1. [カスタムリソースのマッピング](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [エクスペリエンスイベントのマッピング](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [シードテーブルデータのマッピング](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [データマッピングの変更](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [データ取得ジョブのステータスの確認](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

## その他のリソース

* [Adobe Experience Platform Data Connector について](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-about-data-connector.html)
* [エクスペリエンスデータモデルの概要](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-data-model-overview.html)
* [マッピング定義](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-definition.html)
* [マッピングのアクティベーション](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-activation.html)
* [API によるデータ取得トリガー](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-triggering-data-ingestion.html)
