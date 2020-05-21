---
title: 外部シグナルアクティビティ — パラメータを使用してワークフローを呼び出します。
description: 外部信号アクティビティは、同じ顧客の遍歴の一部である異なるプロセスを別々のワークフローに編成および調整するために使用します。 ワークフローを別のワークフローから開始でき、より複雑な顧客の遍歴をサポートしながら、問題が発生した場合の監視と対応を改善できます。
feature: External Signal Activity
topics: Workflows
kt: 2750
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 556bff4c94e16d3a94561dee1ccb311bc003b631
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 0%

---


# [!UICONTROL External Signal activity ]— パラメーターを使用してワークフローを呼び出す

は、同じ顧客の遍歴の一部である異なるプロセスを別々のワークフローに編成および調整するために使用します。 [!UICONTROL External Signal activity] ワークフローを別のワークフローから開始でき、より複雑な顧客の遍歴をサポートし、問題が発生した場合の監視と対応を改善できます。

ACS 19.2では、ワークフローを呼び出すだけでなく、オーディエンスにパラメータ(ターゲットに対するワークフロー名、インポートするファイル名、メッセージコンテンツの一部など)を渡すこともできます。 [!UICONTROL External Signal activity] を別のワークフローまたはREST API呼び出しから取得して、外部システムと統合できます。

また、この機能に対してテストを実行できる新しい **Test** アクティビティも追加されました。

次のビデオでは、次の操作に必要な設定手順を説明します。

1. **コンテンツ管理システム** (CRM)など、外部システムから外部パラメーターを受け取ります。
   * 外部シグナルアクティビティでパラメータを宣言する
   * API呼び出しを設定して、パラメーターを定義し、ワークフローの外部シグナルアクティビティをトリガーします。 API呼び出しの設定方法について詳しくは、「シグナルアクティビティの [トリガー](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#triggering-a-signal-activity)」を参照してください。

1. **外部パラメーターを使用したワークフローのカスタマイズ** (イベント変数):
ワークフローがトリガーされると、パラメーターはワークフローのイベント変数に取り込まれ、ワークフロー内で使用できます。 イベント変数を使用してカスタマイズ可能なすべてのアクティビティについては、 [ドキュメント](https://helpx.adobe.com/campaign/standard/automating/using/calling-a-workflow-with-external-parameters.html) を参照してください。

   * テストアクティビティの設定（19.2で導入された新機能）
   * 読み取りオーディエンスと電子メール配信アクティビティの設定

1. **外部パラメーターを使用してワークフローを呼び出す** 、エンドアクティビティの設定

>[!VIDEO](https://video.tv.adobe.com/v/27249/?quality=12)

## その他のリソース

* [外部シグナル（ドキュメント）](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/data-management-activities/external-api.html)
