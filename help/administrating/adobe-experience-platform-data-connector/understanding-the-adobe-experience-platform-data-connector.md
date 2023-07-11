---
title: Adobe Experience Platform Data Connector について
description: Adobe Experience Platform Data Connector を使用すると、既存のお客様は、XTK データ（Campaign で取り込んだデータ）をAdobe Experience Platformの Experience Data Model(XDM) データにマッピングすることで、Adobe Experience Platformでデータを利用できるようになります。
feature: People Core Service Integration
jira: KT-2826
thumbnail: 27304.jpg
role: User
level: Experienced
doc-type: feature video
activity: understand
team: TM
exl-id: 686961f9-5374-4cc6-8b36-7ee0584ea720
source-git-commit: d46e4c84a7d162085016722005cca4aadb4feb3c
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 4%

---

# Adobe Experience Platform [!UICONTROL Data Connector]

>[!NOTE]
>
>この機能はベータ版で、予告なく頻繁に更新や変更がおこなわれます。
>
>次の場所に連絡してください： [!UICONTROL Adobe Customer Support] この機能を実装する予定がある場合は、をクリックします。

## 概要

Adobe Experience Platform [!UICONTROL Data Connector] は、既存のお客様が XTK データ (Adobe Campaignで取り込まれたデータ ) をにマッピングすることで、Adobe Experience Platformでデータを利用できるようにするのに役立ちます。 [!DNL Experience Data Model] Adobe Experience Platformの (XDM) データ。

コネクタは一方向で、Adobe Campaign StandardからAdobe Experience Platformにデータを送信します。 データはAdobe Experience PlatformからAdobe Campaign Standardに送信されません。

Adobe Experience Platform [!UICONTROL Data Connector] は、Adobe Campaign Standardを理解しているデータエンジニアを対象としています [!UICONTROL custom resources] およびは、顧客の全体的なデータスキーマをAdobe Experience Platform内でどのように配置するかを理解しています。

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12&learn=on)

*このビデオでは、Adobe Experience Platform [!UICONTROL Data Connector] （09:35 分）*

>[!NOTE]
>
>の標準転送 [!UICONTROL subscription events] はサポートされていません。 転送する [!UICONTROL subscription events]を使用すると、対応する XDM とデータセットをAdobe Experience Platformで作成し、それらのデータのカスタムデータマッピングを設定できます。
>
>既存 [!UICONTROL experience events] Adobe Experience Platformに取り込むことはできませんが、継続的に生成されています [!UICONTROL experience events] はAdobe Experience Platformにストリーミングされます。

## データマッピングを実行するための主な手順

次のチュートリアルでは、Campaign StandardとAdobe Experience Platformの間でデータマッピングを実行する主な手順を説明します。

1. [カスタムリソースのマッピング](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [エクスペリエンスイベントのマッピング](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [シードテーブルデータのマッピング](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [データマッピングの変更](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [データ取り込みジョブのステータスの確認](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

