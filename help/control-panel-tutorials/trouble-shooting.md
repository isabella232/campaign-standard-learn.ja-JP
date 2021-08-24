---
title: Campaign コントロールパネルのトラブルシューティング
description: 「 」Campaign コントロールパネルを使用すると、インスタンス別、およびIPアドレス別に、SFTPストレージを監許可リスト視および管理できます。
feature: コントロールパネル
kt: 2938
doc-type: article
activity: use
team: PM
exl-id: f546f791-a69b-4586-abfa-3e626b8feb17
source-git-commit: 481cbdcc9ac7446cc36fbff6e3d6e43fe333d30b
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 44%

---

# [!UICONTROL Control Panel] のトラブルシューティング

Campaign コントロールパネルを使用する際の問題のトラブルシューティング方法を説明します。

## ログインとホームページ

ログインとホームページで発生する問題。

### 症状：Adobe Experience Cloudにログインできない

**対処方法：**
ユーザーは、(xxx)を見つけ [!DNL IMS Org ID] る必要があります。管理者は、管理する各インスタンスについて、ユーザーを[!UICONTROL product profile] [!DNL “Campaign-xxx-Admins”]に追加する必要があります。 ユーザーがすべてのインスタンスの管理者である場合は、自分自身を&#x200B;*[!UICONTROL user]*&#x200B;として追加する必要があります。

### 症状：[!UICONTROL Adobe Experience Cloud Home] の [!UICONTROL Control Panel] にアクセスするリンクがユーザーに表示されない

**原因：**
ユーザーが [!UICONTROL product profile]（`Campaign-xxx-Administrators/Admin`）に追加されない限り、リンクは表示されません。

**対処方法：**
管理者は、管理する各インスタンスについ [!UICONTROL product profile] *[!DNL Campaign-xxx-Admins]* て、ユーザーをに追加する必要があります。ユーザーがすべてのインスタンスの管理者である場合は、自分自身を&#x200B;*[!UICONTROL user]*&#x200B;として追加する必要があります。

### 症状： インスタンスが [!UICONTROL Control Panel] の一覧に表示されない

**原因：**
ユーザーは、見つからないインスタンスの製品プロフ *[!UICONTROL user]* ァイルと `Campaign-xxx-Administrators/Admin` して追加される必要がある可能性が高いです

**対処方法：**
管理者は、管理する各インスタンスについて、ユーザーを製 `Campaign-xxx-Admins` 品プロファイルに追加する必要があります。ユーザーがすべてのインスタンスの管理者である場合は、自分自身を&#x200B;*[!UICONTROL user]*&#x200B;として追加する必要があります。

### 参考になるビデオ

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
* Adobe Campaignに登録する必要がある秘密鍵と公開鍵のペア
* SFTPサーバーに直接接続する場合は、SFTPクライアントソフトウェアが必要です

### 参考ドキュメント {#helpful-docs}

* [SFTP サーバーへのログイン](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=en)
