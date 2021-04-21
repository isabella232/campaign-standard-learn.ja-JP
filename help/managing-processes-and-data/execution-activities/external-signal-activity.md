---
title: 外部シグナルアクティビティ — パラメータを使用してワークフローを呼び出します。
description: 複雑な顧客ジャーニーをサポートしながら、問題の監視と対応を改善するために、別のワークフローから開始する方法を説明します。
feature: 実行アクティビティ
kt: 2750
thumbnail: 27249
doc-type: feature video
activity: use
team: TM
exl-id: d3996185-681c-4906-85f0-0543ab767519
role: Business Practitioner, Developer
level: Experienced
translation-type: tm+mt
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 9%

---

# [!UICONTROL External Signal activity ] — パラメーターを使用してワークフローを呼び出す

[!UICONTROL External Signal activity]は、同じ顧客ジャーニーの一部である異なるプロセスを別のワークフローに編成および調整するために使用します。 このアクティビティでは、あるワークフローを別のワークフローから起動できるので、さらに複雑なカスタマージャーニーをサポートできる一方、問題が発生した場合の監視と対応を改善することができます。

ACS 19.2では、[!UICONTROL External Signal activity]はワークフローを呼び出すだけでなく、オーディエンスにパラメータ(ターゲットに対するワークフロー名、インポートするファイル名、メッセージコンテンツの一部など)を渡すこともできます。 を別のワークフローまたはREST API呼び出しから取得して、外部システムと統合できます。

また、この機能に対してテストを実行できる新しい&#x200B;**テスト**&#x200B;アクティビティも追加されました。

次のビデオでは、次の操作に必要な設定手順を説明します。

1. **コンテンツ管理システム(CRM)などの外部システムから外部** パラメータを受け取ります。

   * 外部シグナルアクティビティでパラメータを宣言する
   * API呼び出しを設定して、ワークフローの外部シグナルアクティビティのパラメータとトリガーを定義します。 API呼び出しの設定方法について詳しくは、[シグナルアクティビティをトリガーする](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#triggering-a-signal-activity)を参照してください。

1. **外部パラメーターを使用したワークフローのカスタマイズ** (イベント変数):

   ワークフローがトリガーされると、パラメーターはワークフローのイベント変数に取り込まれ、ワークフロー内で使用できます。 イベント変数を使用してカスタマイズできるすべてのアクティビティについては、[ドキュメント](https://helpx.adobe.com/campaign/standard/automating/using/calling-a-workflow-with-external-parameters.html)を参照してください。

   * テストアクティビティの設定（19.2で導入された新機能）
   * 読み取りオーディエンスと電子メール配信アクティビティの設定

1. **外部パラメーターを使用してワークフローを呼び出すようにエンド** アクティビティを設定

>[!VIDEO](https://video.tv.adobe.com/v/27249/?quality=12)

## その他のリソース

* [外部シグナル（ドキュメント）](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/calling-workflow-external-parameters/calling-a-workflow-with-external-parameters.html)
