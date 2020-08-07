---
title: コントロールパネル
description: Campaign コントロールパネルでは、インスタンスごとの SFTP ストレージと許可リストの IP アドレスを監視および管理できます。
feature: Control Panel
topics: Control Panel
kt: 4696
doc-type: feature video
activity: use
team: PM
translation-type: tm+mt
source-git-commit: 906b1d76e4723b50e2d06f6525763bbd73b98e10
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 100%

---


# [!UICONTROL Control Panel] {#control-panel}

>[!NOTE]
>
>Adobe Campaign ドキュメントでは、「[!UICONTROL whitelist]（ホワイトリスト）」および「[!UICONTROL blacklist]（ブラックリスト）」という用語は「[!UICONTROL allow list]（許可リスト）」および「[!UICONTROL block list]（ブロックリスト）」に置き換えられました。これらの用語の一部は、製品の UI、オプション名、内部コード、チュートリアルビデオに残っている場合があります。今後の Campaign コントロールパネルリリースで置き換えられる予定です。

[!UICONTROL Control Panel] を使用すると、Adobe Campaign 管理者は、主要なアセットを監視し、インスタンスごとの SFTP ストレージの管理や [!UICONTROL allow list] への IP アドレス追加などの管理タスクを実行できます。

## [!UICONTROL Control Panel] へのアクセス

Campaign コントロールパネルにアクセスするには、Experience Cloud ホーム（[https://experiencecloud.adobe.com](https://experiencecloud.adobe.com)）に移動します。

* **[!UICONTROL Experience Cloud Home]**／**[!UICONTROL Quick Access]**

   または
* **[!UICONTROL Experience Cloud Home]**／[!UICONTROL Solution picker]：**Campaign**／**[!UICONTROL Control Panel]カード&#x200B;**

   または

* URL から直接アクセス：[https://experience.adobe.com/jp/#/controlpanel](https://experience.adobe.com/jp/#/controlpanel)

## 前提条件

開始する前に、次の前提条件を満たしておく必要があります。

### [!DNL IMS Org ID] を確認

自身の [!DNL IMS org ID] を知っておく必要があります。次のビデオでは、インスタンスの [!DNL IMS org ID] の参照場所を説明します。

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)
*チェック[!DNL IMS Org ID]（00:26 分）*

### 管理者権限

[!UICONTROL Control Panel] にアクセスするには、管理者権限が必要です。
次のビデオでは、Campaign インスタンスに管理者を追加する方法を説明します

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)
*製品プロファイルの「[!UICONTROL Administrators]」に管理者を追加して[!UICONTROL Control Panel]を使用できるようにする方法（01:03 分）*

## Campaign コントロールパネルのチュートリアル

* **SFTP サーバーの管理**

   *サーバー容量の監視方法、許可リストへの IP アドレスの追加方法、および SSH 鍵の追加方法を説明します。*

   * [サーバ容量の監視、許可リストへの IP アドレスの追加、SSH 鍵の追加](/help/administrating/control-panel/monitoring-server-capacity-allow-listing-adding-ssh-key.md)
   * [SSH 鍵の生成](/help/administrating/control-panel/generate-ssh-key.md)
   * [SFTP サーバーへの接続](/help/administrating/control-panel/connect-to-sftp-server.md)
* **[サブドメインのデリゲート](/help/administrating/control-panel/subdomain-delegation.md)**

   *サブドメインを Adobe Campaign に完全にデリゲートする方法を説明します。*
* **[SSL 証明書の追加](/help/administrating/control-panel/adding-ssl-certificates.md)**

   *サブドメインを保護するために SSL 証明書を追加する方法について説明します。*

* **[Google TXT レコード管理](/help/administrating/control-panel/google-txt-record-management.md)**

   *Campaign コントロールパネルを使用して、Gmail アドレス宛ての E メール送信に使用するすべてのサブドメインに Google TXT サイト検証レコードを追加する方法を説明します。*

* **GPG キー管理**

   *送信データの暗号化用に、特定の Campaign インスタンスに公開／秘密鍵のペアを生成してインストールする方法、および受信データの復号化用に、Campaign インスタンスに公開鍵を読み込んでインストールする方法を説明します。*

   * [データ暗号化用の GPG キーの生成とインストール](./gpg-key-management/generating-and-installing-gpg-keys-for-data-encryption.md)
   * [GPG キーを使用したデータの暗号化](./gpg-key-management/using-a-gpg-key-to-encrypt-data.md)
   * [データの復号化](./gpg-key-management/decrypting-data.md)

* **[トラブルシューティング](/help/administrating/control-panel/trouble-shooting.md)**

   *Campaign コントロールパネルのトラブルシューティング方法を説明します。*

## その他のリソース

* [Campaign コントロールパネルのヘルプセンター](https://docs.adobe.com/content/help/ja-JP/control-panel/using/control-panel-home.html)

