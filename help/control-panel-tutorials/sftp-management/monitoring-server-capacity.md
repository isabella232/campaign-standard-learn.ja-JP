---
title: サーバ容量の監視
description: Campaign コントロールパネルでは、インスタンスごとに SFTP ストレージを監視および管理し、許可リストに IP アドレスを追加できます。
feature: SFTP Management
topics: Control Panel
audience: administrator
kt: 6239
thumbnail: 27270.jpg
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 8e6298c9d6fc7989b5296dc0fbea2ebeffc337a6
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 82%

---


# サーバ容量の監視

このCampaign コントロールパネルを使用すると、SFTPストレージをインスタンスごとに監視および管理できます。

## [!UICONTROL Control Panel] のサブドメイン管理へのアクセス

[!UICONTROL Control Panel] のサブドメイン管理にアクセスするには、次のいずれかの手順に従います。

* [Experience Cloud ホーム](https://experience.adobe.com/#/home)／[!UICONTROL Solution picker]：[!UICONTROL Campaign]／**[!UICONTROL Control Panel]** カード／**[!UICONTROL Subdomains & Certificates]** カード

   または
* URL から直接アクセス：[https://experience.adobe.com/jp/#/controlpanel/domain](https://experience.adobe.com/#/controlpanel/domain)

## サーバー容量の監視、[!UICONTROL allow list] への IP アドレスの追加、SSH 鍵の追加

このビデオでは、SFTPサーバーへのアクセス方法 [!UICONTROL Adobe Campaign Control Panel] と、SFTPサーバーのストレージを監視できる場所を説明します。

>[!VIDEO](https://video.tv.adobe.com/v/27270?quality=12)

### インターフェイスの説明

**インスタンス**：管理者権限を持つインスタンスのみが表示されます。

**ジョブのログ**：[!UICONTROL Control Panel] 内で実行されたジョブのみが表示されます。[!UICONTROL Control Panel] の外部で実行されたジョブは含まれません（例えば、実行中のワークフローなど）。

ログには、組織の管理者が実行するジョブのみが含まれます。複数の組織がある場合、ジョブのログにその他の組織のログは表示されません。

**「ストレージ」タブ**：ヘッダーには、最も頻繁に使用されるサーバーの上位 3 つが表示されます。3 台以上のサーバーがある場合は、「[!UICONTROL Storage]」タブに残りのサーバーが表示されます。

**警告メッセージ**：

* オレンジ - サーバーの使用率が 80％
* 赤 - サーバーの使用率が 90％

## その他のリソース

* [SSH 鍵の生成](./generate-ssh-key.md)
