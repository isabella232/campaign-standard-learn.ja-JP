---
title: Campaign コントロールパネルの撮影の問題
description: このCampaign コントロールパネルでは、インスタンスと許可リストのIPアドレス別に、SFTPストレージを監視および管理できます。
feature: Control Panel
topics: null
kt: 2938
doc-type: article
activity: use
team: PM
translation-type: tm+mt
source-git-commit: b277b1ad17d9c03b307f8483d776b796e6c0cbef
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 1%

---


# [!UICONTROLCampaign コントロールパネル}のキャプチャ中にエラーが発生しました

Campaign コントロールパネルを使用する際の問題のトラブルシューティング方法を説明します。

## ログインとホームページ

ログインとホームページで発生する問題。

### 症状： Adobe Experience Cloudにログインできない

**操作方法：**
ユーザーは、 [!DNL IMS Org ID] (xxx)を探す必要があります。 管理者は、管理する各インスタンス [!UICONTROL product profile] に対して、ユーザ [!DNL “Campaign-xxx-Admins”] をに追加する必要があります。 ユーザーがすべてのインスタンスの管理者である場合、として自分自身を追加する必要がある場合があり *[!UICONTROL user]*&#x200B;ます。

### 症状： アクセス [!UICONTROL Adobe Experience Cloud Home] するリンクは、ユーザー [!UICONTROL Control Panel] に表示されません

**原因：**
ユーザーは、 [!UICONTROL product profile] `Campaign-xxx-Administrators/Admin`

**操作方法：**
管理者は、管理する各インスタンス [!UICONTROL product profile] に対して、ユーザ *[!DNL Campaign-xxx-Admins]* をに追加する必要があります。 ユーザーがすべてのインスタンスの管理者である場合、として自分自身を追加する必要がある場合があり *[!UICONTROL user]*&#x200B;ます。

### 症状： インスタンスが [!UICONTROL Control Panel]

**原因：**
見つからないインスタンスの *[!UICONTROL user]* 製品プロファイルとして追加され `!DNL Campaign-xxx-Administrators/Admin` る可能性が高いユーザー

**操作方法：**
管理者は、管理する各インスタンスに対して、ユーザーを製品プロファイル `Campaign-xxx-Admins` に追加する必要があります。 ユーザーがすべてのインスタンスの管理者である場合、として自分自身を追加する必要がある場合があり *[!UICONTROL user]*&#x200B;ます。

### 役立つビデオ

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)
*チェック[!DNL IMS Org ID]（00:26分）*

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)
*管理者をAdd To Add[!UICONTROL product profile]to Be Use *[!DNL administrators]*[!UICONTROL Control Panel]（01:03分）*

### 便利なドキュメント

* [Folio Builder [!UICONTROL Control Panel]](https://helpx.adobe.com/campaign/kb/control-panel-overview.html)
* [次に対する権限の管理 [!UICONTROL Control Panel]](https://helpx.adobe.com/campaign/kb/control-panel-access.html)

## SFTPサーバー（クライアントまたはAPI）への接続の確立

SFTPサーバーに接続するには、次の環境が必要です。

* [!UICONTROL allow listing] SFTPサーバーに接続するIPアドレス
* Adobe Campaignに登録する必要がある秘密鍵と公開鍵のペア
* SFTPサーバーに直接接続する場合は、SFTPクライアントソフトウェアも必要です

### 便利なドキュメント

* [SFTP サーバーへのログイン](https://helpx.adobe.com/campaign/kb/control-panel-sftp.html#LoggingintoyourSFTPserver)

