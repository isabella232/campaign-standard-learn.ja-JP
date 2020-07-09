---
title: コントロールパネル
description: コントロールパネルでは、インスタンスと許可リストのIPアドレス別に、SFTPストレージを監視および管理できます。
feature: Control Panel
topics: Control Panel
kt: 4696
doc-type: feature video
activity: use
team: PM
translation-type: tm+mt
source-git-commit: db20c4e6aeb10dc04a6c4556fefaa8cd18366c44
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 6%

---


# [!UICONTROL Control Panel] {#control-panel}

>[!NOTE]
>
>Adobe Campaignマニュアルでは、「[!UICONTROL whitelist]」および「[!UICONTROL blacklist]」という用語は「[!UICONTROL allow list]」および「」[!UICONTROL block list]に置き換えられました。 これらの用語の一部は、製品のUI、オプション名、内部コード、チュートリアルビデオに残っている場合があります。 これらは、今後のコントロールパネルのリリースで置き換えられる予定です。

を [!UICONTROL Control Panel] 使用すると、Adobe Campaign管理者は、主要なアセットを監視し、インスタンスまたは [!UICONTROL allow list] IPアドレスごとのSFTPストレージの管理などの管理タスクを実行できます。

## アクセス [!UICONTROL Control Panel]

コントロールパネルにアクセスするには、Experience Cloudホームに移動します。 [https://experiencecloud.adobe.com](https://experiencecloud.adobe.com):

* **[!UICONTROL Experience Cloud Home]** > **[!UICONTROL Quick Access]**

   または
* **[!UICONTROL Experience Cloud Home]**  > [!UICONTROL Solution picker]: **キャンペーン** / **[!UICONTROL Control Panel]カード&#x200B;**

   または

* URLから直接： [https://experience.adobe.com/#/controlpanel](https://experience.adobe.com/#/controlpanel)

## 前提条件

開始する前に、次の前提条件を満たします。

### 確認 [!DNL IMS Org ID]

君のことを知る必要がある [!DNL IMS org ID]。 次のビデオでは、インスタンスの参照場所を説明し [!DNL IMS org ID]ます。

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)
*チェック[!DNL IMS Org ID]（00:26分）*

### 管理者権限

にアクセスするには、管理者権限が必要で [!UICONTROL Control Panel]す。
次のビデオでは、キャンペーンインスタンスに管理者を追加する方法を説明します

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)
*製品プロファイル「[!UICONTROL Administrators]」に管理者を追加して使用できるようにする方法[!UICONTROL Control Panel]（01:03分）*

## コントロールパネルのチュートリアル

* **SFTPサーバーの管理**

   *サーバーの容量、許可リストのIPアドレスを監視し、SSHキーを追加する方法を説明します。*

   * [サーバの容量の監視、IPアドレスの一覧表示、SSHキーの追加を許可](/help/administrating/control-panel/monitoring-server-capacity-allow-listing-adding-ssh-key.md)
   * [SSHキーの生成](/help/administrating/control-panel/generate-ssh-key.md)
   * [SFTPサーバーへの接続](/help/administrating/control-panel/connect-to-sftp-server.md)
* **[サブドメインの委任](/help/administrating/control-panel/subdomain-delegation.md)**

   *サブドメインをAdobe Campaignに完全に委任する方法を学びます*
* **[SSL証明書の追加](/help/administrating/control-panel/adding-ssl-certificates.md)**

   *サブドメインを保護するためにSSL証明書を追加する方法について説明します。*
* **[SSL証明書の管理](/help/administrating/control-panel/managing-ssl-certificates.md)**

   *サブドメインのSSL証明書のステータスを表示し、更新を要求する方法について説明します。*
* **[Google TXT レコード管理](/help/administrating/control-panel/google-txt-record-management.md)**

   *キャンペーンコントロールパネルを使用してGMAILアドレスに電子メールを送信するために使用するすべてのサブドメインに、Google TXTサイト検証レコードを追加する方法を説明します。*

* **GPGキー管理**

   *送信データの暗号化用に指定したキャンペーンインスタンスに公開鍵と秘密鍵のペアを生成してインストールする方法、および受信データの復号化用にキャンペーンインスタンスに公開鍵を読み込んでインストールする方法を説明します。*

   * [データ暗号化用のGPGキーの生成とインストール](./gpg-key-management/generating-and-installing-gpg-keys-for-data-encryption.md)
   * [GPGキーを使用したデータの暗号化](./gpg-key-management/using-a-gpg-key-to-encrypt-data.md)
   * [データの復号化](./gpg-key-management/decrypting-data.md)

* **[トラブル・シューティング](/help/administrating/control-panel/trouble-shooting.md)**

   *コントロールパネルのトラブルシューティング方法を理解する*

## その他のリソース

* [コントロールパネルヘルプセンター](https://docs.adobe.com/content/help/ja-JP/control-panel/using/control-panel-home.html)

