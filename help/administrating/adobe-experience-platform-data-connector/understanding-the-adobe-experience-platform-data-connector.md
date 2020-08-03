---
title: Adobe Experience Platformデータコネクタについて
description: Adobe Experience Platformデータコネクタは、XTKデータ(キャンペーンで取り込まれたデータ)をAdobe Experience Platform上のエクスペリエンスデータモデル(XDM)データにマッピングすることで、既存のお客様がAdobe Experience Platform上でデータを利用できるようにします。
feature: Adobe Experience Platform Data Connector
topics: ACoP
kt: 2826
doc-type: feature video
activity: understand
team: TM
translation-type: tm+mt
source-git-commit: cb5d5bc58137fd374eafe165c6ea13288a60d7db
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 5%

---


# Adobe Experience Platformについて [!UICONTROL Data Connector]

>[!NOTE]
>
>この機能は現在ベータ版であり、予告なく頻繁に更新や変更が行われる場合があります。
>
>この機能を実装する予定がある [!UICONTROL Adobe Customer Support] 場合は、ご連絡ください。

## 概要

Adobe Experience Platform [!UICONTROL Data Connector] は、XTKデータ(Adobe Campaignで取り込まれたデータ)をAdobe Experience Platform上の [!DNL Experience Data Model] (XDM)データにマッピングすることで、既存のお客様がデータをAdobe Experience Platform上で利用できるようにするのに役立ちます。

コネクタは単方向であり、データをAdobe Campaign StandardからAdobe Experience Platformに送信します。 データはAdobe Experience PlatformからAdobe Campaign Standardに送信されません。

Adobe Experience Platform [!UICONTROL Data Connector][!UICONTROL custom resources] は、Adobe Campaign Standardを理解し、お客様の全体的なデータスキーマがAdobe Experience Platform内でどのように行われるべきかを理解しているデータエンジニアを対象としています。

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12)

*このビデオでは、Adobe Experience Platformの概要を説明[!UICONTROL Data Connector]します（09:35分）。*

>[!NOTE]
>
>の既製の転送はサポートされてい [!UICONTROL subscription events] ません。 転送するに [!UICONTROL subscription events]は、Adobe Experience Platform上に対応するXDMとデータセットを作成し、これらのデータに対するカスタムデータマッピングを設定します。
>
>既存のも [!UICONTROL experience events] のはAdobe Experience Platformに取り込むことはできませんが、継続中の生成物 [!UICONTROL experience events] はAdobe Experience Platformにストリーミングされます。

## データマッピングを実行するための主な手順

次のチュートリアルでは、Campaign StandardとAdobe Experience Platformの間のデータマッピングを実行する主な手順を説明します。

1. [カスタムリソースのマッピング](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [エクスペリエンスイベントのマッピング](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [シードテーブルデータのマッピング](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [データ・マッピングの変更](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [データ取り込みジョブのステータスの確認](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

## その他のリソース

* [Adobe Experience Platform Data Connector について](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-about-data-connector.html)
* [エクスペリエンスデータモデルの概要](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-data-model-overview.html)
* [マッピング定義](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-definition.html)
* [マッピングの有効化](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-activation.html)
* [API によるデータ取り込みのトリガー](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-triggering-data-ingestion.html)
