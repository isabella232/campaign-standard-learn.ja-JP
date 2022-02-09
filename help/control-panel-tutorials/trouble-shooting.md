---
title: Campaign コントロールパネルのトラブルシューティング
description: コントロールパネルを使用すると、インスタンスおよび許可リストの IP アドレスごとに SFTP ストレージを監視および管理できます。
feature: Control Panel
kt: 2938
doc-type: article
activity: use
team: PM
recommendations: noDisplay
exl-id: f546f791-a69b-4586-abfa-3e626b8feb17
source-git-commit: 57dbf456625d22cd2e4526d92e5a8c20a048d339
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 57%

---

# [!UICONTROL Control Panel] のトラブルシューティング

Campaign コントロールパネルを使用する際の問題のトラブルシューティング方法を説明します。

## ログインとホームページ

ログインとホームページで発生する問題。

### 症状：Adobe Experience Cloudにログインできません

**対処方法：**
ユーザーは、 [!DNL IMS Org ID] 三十 管理者はユーザーを [!UICONTROL product profile] [!DNL “Campaign-xxx-Admins”] 管理する各インスタンスに対して、 ユーザーがすべてのインスタンスの管理者である場合、自身を *[!UICONTROL user]*.

### 症状：[!UICONTROL Adobe Experience Cloud Home] の [!UICONTROL Control Panel] にアクセスするリンクがユーザーに表示されない

**原因：**
ユーザーが [!UICONTROL product profile]（`Campaign-xxx-Administrators/Admin`）に追加されない限り、リンクは表示されません。

**対処方法：**
管理者はユーザーを [!UICONTROL product profile] *[!DNL Campaign-xxx-Admins]* 管理する各インスタンスに対して、 ユーザーがすべてのインスタンスの管理者である場合、自身を *[!UICONTROL user]*.

### 症状： インスタンスが [!UICONTROL Control Panel] の一覧に表示されない

**原因：**
ほとんどの場合、ユーザーは *[!UICONTROL user]* 製品プロファイル `Campaign-xxx-Administrators/Admin` 見つからないインスタンスの

**対処方法：**
管理者は製品プロファイルにユーザーを追加する必要があります `Campaign-xxx-Admins` 管理する各インスタンスに対して、 ユーザーがすべてのインスタンスの管理者である場合、自身を *[!UICONTROL user]*.

### 役立つビデオ

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)

*[!DNL IMS Org ID] の確認（0 分 26 秒）*

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)

*[!UICONTROL product profile] の [!DNL administrators] に管理者を追加して [!UICONTROL Control Panel] を使用できるようにする方法（01:03 分）*

### 参考ドキュメント

* [[!UICONTROL Control Panel] を詳しく知る ](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=ja)
* [[!UICONTROL Control Panel] に対する権限の管理 ](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=en)

## SFTP サーバー（クライアントまたは API）への接続の確立

SFTP サーバーに接続するには、次の環境が必要です。

* SFTP サーバーに接続する IP アドレスの [!UICONTROL allow listing]
* Adobe Campaign に登録する必要がある秘密キーと公開キーのペア
* SFTP サーバーに直接接続する場合は、SFTP クライアントソフトウェアが必要です

### 参考ドキュメント {#helpful-docs}

* [SFTP サーバーへのログイン](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=en)
