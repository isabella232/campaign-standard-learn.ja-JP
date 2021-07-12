---
title: イベントの設定
description: 「イベントが開始したアクションによって、表示されるアプリ内メッセージがトリガーされる方法を定義する方法を理解します。 」
feature: アプリ内
kt: 2548
thumbnail: 26245.jpg
doc-type: feature video
activity: use
team: TM
exl-id: 2c7937f4-b0da-46e5-934e-c660012c2c6f
role: User, Developer
level: Beginner, Intermediate
source-git-commit: 2be2719ddd84490b796d9abc6300376fa896ff0c
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 3%

---

# 設定 [!UICONTROL Events] {#configuring-events}

[!UICONTROL In-App]メッセージを設定する場合、表示するメッセージをユーザーが開始するアクショントリガーを定義する必要があります。 これらのアクションは[!UICONTROL events]と呼ばれます。 [!UICONTROL events]の3つのカテゴリを使用できます。[!UICONTROL Mobile Application events]、[!UICONTROL Life Cycle events]、および[!UICONTROL Analytics events]。

## [!UICONTROL Mobile Application Events] {#mobile-application-events}

[!UICONTROL Mobile Application events] は、モ [!UICONTROL custom events] バイルアプリケーションに実装されるものです。

例：

* 顧客が品目を閲覧した
* 顧客が買い物かごに品目を追加
* 買い物かごの放棄
* 顧客が何かを購入した

これらの[!UICONTROL events]は、Adobe Campaignで設定する必要があります。 次のビデオでは、この方法について説明します。

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12)

## [!UICONTROL Life Cycle events] {#life-cycle-events}

[!UICONTROL Lifecycle events] は標準搭載で [!UICONTROL events]す。次の[!UICONTROL events]を使用できます。

* [!UICONTROL launched]
* [!UICONTROL upgraded]
* [!UICONTROL crashed]

使用例としては、アップグレード後の新機能を紹介するメッセージや、イベントのプロモーションなどがあります。

>[!NOTE]
>
>[!UICONTROL Lifecycle module]は、モバイルアプリケーションで設定する必要があります。 [アプリケーションにライフサイクルを追加する方法](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle)の詳細については、こちらを参照してください。

## [!UICONTROL Analytics Events] {#analytics-events}

モバイルアプリに実装されている機能に応じて、次の3つのカテゴリがサポートされます。

* Adobe Analytics
* [!UICONTROL Context data]
* [!UICONTROL View state]

>[!NOTE]
>
>[!UICONTROL Analytics events] にはAdobe Analyticsライセンスが必要です。[[!DNL Analytics] 拡張機能を設定](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#configure-analytics-extension-in-launch)し、[Analyticsをアプリ](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#add-analytics-to-your-app)に追加すると、ACSの[!UICONTROL In-App]設定でこれらのイベントを使用できるようになります。

## その他のリソース

* [ライフサイクル指標の有効化（ドキュメント）](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
