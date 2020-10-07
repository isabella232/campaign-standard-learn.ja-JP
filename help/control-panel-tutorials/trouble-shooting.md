---
title: Campaign コントロールパネルのトラブルシューティング
description: Campaign コントロールパネルでは、インスタンスごとの SFTP ストレージと許可リストの IP アドレスを監視および管理できます。
feature: Control Panel
topics: null
kt: 2938
doc-type: article
activity: use
team: PM
translation-type: tm+mt
source-git-commit: 9d71fbf2067611c2d3c088d6ed6bc02b2d3ffc1c
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 100%

---


# [!UICONTROL Control Panel] のトラブルシューティング

Campaign コントロールパネルを使用する際の問題のトラブルシューティング方法を説明します。

## ログインとホームページ

ログインとホームページで発生する問題。

### 症状：Adobe Experience Cloud にログインできない

**解決方法：**
ユーザーは、[!DNL IMS Org ID]（xxx）を探し出して示す必要があります。管理者は、管理する各インスタンスについて、ユーザーを [!UICONTROL product profile]（[!DNL “Campaign-xxx-Admins”]）に追加する必要があります。ユーザーがすべてのインスタンスの管理者であっても、場合によっては、*[!UICONTROL user]* として自分自身を追加する必要があります。

### 症状：[!UICONTROL Adobe Experience Cloud Home] の [!UICONTROL Control Panel] にアクセスするリンクがユーザーに表示されない

**原因：**
ユーザーが [!UICONTROL product profile]（`Campaign-xxx-Administrators/Admin`）に追加されない限り、リンクは表示されません。

**解決方法：**
管理者は、管理する各インスタンスについて、ユーザーを [!UICONTROL product profile]（*[!DNL Campaign-xxx-Admins]*）に追加する必要があります。ユーザーがすべてのインスタンスの管理者であっても、場合によっては、*[!UICONTROL user]* として自分自身を追加する必要があります。

### 症状： インスタンスが [!UICONTROL Control Panel] の一覧に表示されない

**原因：**
ユーザーは、見つからないインスタンスについて、製品プロファイル（`Campaign-xxx-Administrators/Admin`）に *[!UICONTROL user]* として追加される必要があると考えられます。

**解決方法：**
管理者は、管理する各インスタンスについて、ユーザーを製品プロファイル（`Campaign-xxx-Admins`）に追加する必要があります。ユーザーがすべてのインスタンスの管理者であっても、場合によっては、*[!UICONTROL user]* として自分自身を追加する必要があります。

### 参考ビデオ

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)

*[!DNL IMS Org ID]の確認（0 分 26 秒）*

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)

*[!UICONTROL product profile]の&#x200B;*[!DNL administrators]*に管理者を追加して[!UICONTROL Control Panel]を使用できるようにする方法（01:03 分）*

### 参考ドキュメント

* [[!UICONTROL Control Panel] を詳しく知る ](https://docs.adobe.com/content/help/ja-JP/control-panel/using/control-panel-home.html)
* [[!UICONTROL Control Panel] に対する権限の管理 ](https://docs.adobe.com/content/help/ja-JP/control-panel/using/control-panel-home.html)

## SFTP サーバー（クライアントまたは API）への接続の確立

SFTP サーバーに接続するには、次の環境が必要です。

* SFTP サーバーに接続する IP アドレスの [!UICONTROL allow listing]
* Adobe Campaign に登録する必要がある秘密鍵と公開鍵のペア
* SFTP サーバーに直接接続する場合は、SFTP クライアントソフトウェアも必要です

### 参考ドキュメント

* [SFTP サーバーへのログイン](https://docs.adobe.com/content/help/ja-JP/control-panel/using/control-panel-home.html#LoggingintoyourSFTPserver)

