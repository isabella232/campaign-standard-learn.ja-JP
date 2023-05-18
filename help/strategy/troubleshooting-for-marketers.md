---
title: マーケター向けトラブルシューティング
description: 最も一般的なエラーを把握することで、問題をより迅速に解決し、生産性を高めることができます。 これらのトラブルシューティングのヒントは、同様のエラーが発生した場合に効果的に解決するのに役立ちます。
version: Standard
feature: Workflows
role: User
level: Beginner, Intermediate, Experienced
doc-type: Article
last-substantial-update: 2023-05-18T00:00:00Z
jira: KT-13256
thumbnail: KT-13256.jpeg
source-git-commit: f7f2b6abb26075b25a3b55e4ceed744172691ce8
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 1%

---


# マーケター向けのトラブルシューティング：5 一般的なワークフローと配信エラー

基準： [スラジパトラ](https://www.linkedin.com/in/suraj-p-51612053/){target="_blank"}（メイジャー）シニアコンサルタント

過去 5 年間、シニアエンジニア兼お客様エキスパートとしてAdobe Experience Cloud製品に関するエキスパートとして、 [メイジェール](https://www.meijer.com/){target="_blank"}は、1934 年に設立されたアメリカのスーパーセンターチェーンで、ACS との複雑でマーケティングやトランザクションのキャンペーンを実行するために設立されました。 私が取り組んだいくつかのプロジェクトには、パーソナライゼーションのオファーと注文の詳細を保存するカスタマイズされたキャンペーン、Adobe Audience Managerと統合されたプロジェクト、セグメント取り込みのための顧客インサイトが含まれます。


ACS を使用している間にエラーが発生しました。このエラーは、解決に時間がかかり、面倒になる場合があります。 最も一般的なエラーを把握することで、問題をより迅速に解決し、生産性を高めることができます。 以下に、同様のエラーが発生した場合に効果的に解決するのに役立つトラブルシューティングのヒントを示します。

## データタイプ不一致エラー

**エラーコード:**
`PGS-220000 PostgreSQL error: ERROR: operator does not exist: character varying = bigint`

**原因：**
これらのタイプのエラーは、異なるデータタイプのフィールドを使用して紐付けを試みると、ワークフローに表示されます。 例えば、文字列フィールドを持つ load file を使用してファイルをアップロードする場合、string フィールドを、データ型が int のプロファイルフィールドに紐付けしようとします。

![data-type-mismatch-error](/help/assets/kt-13256/data-type-mismatch.png)

**解決策：**
「ファイルを読み込み」アクティビティのフィールドのデータタイプを、一致するデータタイプに変更します。 「ファイル読み込み」アクティビティを開きます。 「COLUMN DEFINITION」タブに移動し、目的のフィールドのデータ型を変更します。


![data-type-mismatch-solution](/help/assets/kt-13256/data-type-mismatch-solution.png)

## 配信のパーソナライゼーションエラー

**エラーコード:**
`The schema for profiles specified in the transition ('') is not compatible with the schema defined in the delivery template ('nms:recipient'). They should be identical.`

**原因：**
このエラーは、電子メールをアドレスに送信する際に表示されますが、電子メールまたはその他の識別子は、プロファイルと紐付けされていません。 E メール通信を送信するには、E メールまたは識別子を常にプロファイルにリンクする必要があります。

次に示すように、紐付けアクティビティを使用します。

![紐付けアクティビティを含むワークフロー](/help/assets/kt-13256/del-persn-error-wf.png)

**解決策：**
共通 ID は、読み込まれたファイルと受信者テーブルから取得したものである必要があります。 この共通キーは、紐付けアクティビティ内で読み込みファイルを受信者テーブルに結合します。 ワークフロー内でこの紐付け手順が必要な受信者テーブルに存在しないレコードには、E メールが送信されない場合があります。 その際、「受信読み込みファイル」アクティビティを、プロファイルからの電子メール ID などの識別子に紐付けします。 この `nms:recipient` スキーマはプロファイルテーブルを参照し、受信レコードをプロファイルに紐付けすることで、e メールの準備中に使用できるようになります。

以下に示す紐付けアクティビティのスクリーンショットを参照してください。

![紐付けの詳細を含むワークフロー](/help/assets/kt-13256/del-persn-error-wf-solution.png)

詳細情報： [紐付け](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/data-management-activities/reconciliation.html?lang=en).

## 共通フィールドデータセットエラー

**エラーコード:**
`The document types of inbound events (''and'') are incompatible (step 'Exclusion'). Unable to perform the operation. `

**原因：**
この問題は、 **除外アクティビティ** （ACS ワークフロー内） このエラーは、ID に基づいてと除外を実行する際に、プライマリセットと除外セットに同じフィールド名がない場合に発生します。


![共通フィールドデータセットエラー](/help/assets/kt-13256/dataset-error.png)

**解決策:**

このエラーを解決する方法は 2 つあります。

1. プライマリと除外の両方で同じフィールド名を使用し、そのフィールドを ID として使用します

   あるいは

1. JOINS 除外メソッドを使用して、レコードを除外するフィールドを選択します。

![一般的なフィールドデータセットエラー — ソリューション ](/help/assets/kt-13256/dataset-error-solution.png)

## フィールド名ドロップエラー

**エラーコード:**
`XTK-170036 Unable to parse expression 'i__name'`

**原因:**

エラーポイントは **エンリッチメント活性**. 最も一般的な例を以下に示します。

![フィールド名ドロップエラー](/help/assets/kt-13256/field-name-dropped-error.png)

これは、アクティビティの式の名前を手動で編集した場合に発生します。 この図は、式が次の場所から変更されたことを示しています： `name `から `i__name`.

**解決策:**

このエラーは、次の 3 つの方法で解決できます。

1. 名前を元の式に戻します。

2. 新しい名前を使用する場合は、 **エンリッチメント活性**.

3. 何が変更されたかを覚えていない場合は、アクティビティを再作成することをお勧めします。

## 一時テーブルの削除エラー 

**エラーコード:**
`XTK-170024 The temporary schema "temp:deliveryEmail1" is not defined in the current context.`

**原因：**
これは、エンリッチメントや他のアクティビティが関わる複雑なワークフローで発生する一般的なエラーです。 ワークフローに対する複数の変更中に、一部のアクティビティワークフローが正しく保存されない可能性があります。

![一時テーブルの削除エラー ](/help/assets/kt-13256/temp-table-dropped-error.png)

**解決策：**
このエラーは多くの方法で発生する可能性があるので、簡単な修正はありません。 単純なワークフローの場合は、アクティビティを再設定する方が効果的です。 複雑なワークフローでは、ワークフローアクティビティを新しいワークフローにコピーし、保存して再実行する方が効果的です。