---
title: 外部シグナルアクティビティ — パラメーターを使用したワークフローの呼び出し
description: より複雑なカスタマージャーニーをサポートしながら、問題の監視と対応を改善するために、別のワークフローから開始する方法を説明します。
feature: 実行アクティビティ
kt: 2750
thumbnail: 27249
doc-type: feature video
activity: use
team: TM
exl-id: d3996185-681c-4906-85f0-0543ab767519
role: User, Developer
level: Experienced
source-git-commit: 2be2719ddd84490b796d9abc6300376fa896ff0c
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 9%

---

# [!UICONTROL External Signal activity ] — パラメーターを使用したワークフローの呼び出し

[!UICONTROL External Signal activity]は、同じカスタマージャーニーの一部である様々なプロセスを様々なワークフローに編成するために使用します。 このアクティビティでは、あるワークフローを別のワークフローから起動できるので、さらに複雑なカスタマージャーニーをサポートできる一方、問題が発生した場合の監視と対応を改善することができます。

ACS 19.2では、[!UICONTROL External Signal activity]はワークフローを呼び出すだけでなく、ワークフローにパラメーター（ターゲットにするオーディエンス名、インポートするファイル名、メッセージコンテンツの一部など）を渡すこともできます。 を、別のワークフローまたはREST API呼び出しからワークフローに追加して、外部システムと統合します。

また、この機能に対してテストを実行できる新しい&#x200B;**テスト**&#x200B;アクティビティも含まれます。

次のビデオでは、以下をおこなうために必要な設定手順を説明します。

1. **外部シス** テム（CRMなど）から外部パラメーターを受け取る。

   * 外部シグナルアクティビティのパラメーターを宣言する
   * API呼び出しを設定して、外部シグナルアクティビティワークフローのパラメーターとトリガーを定義します。 API呼び出しの設定方法について詳しくは、[シグナルアクティビティのトリガー](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#triggering-a-signal-activity)を参照してください。

1. **外部パラメーター（イベント変数）を使用したワークフローのカスタマイズ** :

   ワークフローがトリガーされると、パラメーターがワークフローのイベント変数に取り込まれ、ワークフロー内で使用できます。 イベント変数を使用してカスタマイズ可能なすべてのアクティビティについては、[ドキュメント](https://helpx.adobe.com/campaign/standard/automating/using/calling-a-workflow-with-external-parameters.html)を参照してください。

   * テストアクティビティの設定（19.2新機能）
   * オーディエンス読み取りと電子メール配信アクティビティの設定

1. **外部パラメーターを使用し** てワークフローを呼び出すための終了アクティビティの設定

>[!VIDEO](https://video.tv.adobe.com/v/27249/?quality=12)

## その他のリソース

* [外部シグナル（ドキュメント）](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/calling-workflow-external-parameters/calling-a-workflow-with-external-parameters.html)
