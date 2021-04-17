---
title: イベントの設定
description: 「イベントがユーザーが開始したアクションを定義し、アプリ内メッセージを表示するトリガーを定義する方法を理解します。 」
feature: アプリ内
topics: Mobile
kt: 2548
thumbnail: 26245.jpg
doc-type: feature video
activity: use
team: TM
exl-id: 2c7937f4-b0da-46e5-934e-c660012c2c6f
role: Business Practitioner, Developer
level: Beginner, Intermediate
translation-type: tm+mt
source-git-commit: 5d2bc8bd3a3a0fdb5e2f1ef75af2ab60b8f6abc8
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 3%

---

# 設定 [!UICONTROL Events] {#configuring-events}

[!UICONTROL In-App]メッセージを設定する場合は、メッセージを表示するユーザー開始アクショントリガーを定義する必要があります。 これらのアクションは[!UICONTROL events]と呼ばれます。 [!UICONTROL events]の3つのカテゴリを利用できます。[!UICONTROL Mobile Application events]、[!UICONTROL Life Cycle events]、および[!UICONTROL Analytics events]。

## [!UICONTROL Mobile Application Events] {#mobile-application-events}

[!UICONTROL Mobile Application events] は、モバイルア [!UICONTROL custom events] プリケーションに実装されるものです。

次に例を示します。

* 顧客が品目を閲覧しました
* 顧客が買い物かごに品目を追加
* 買い物かごの放棄
* 顧客が何かを購入した

Adobe Campaignで[!UICONTROL events]を設定する必要があります。 次のビデオでは、この方法について説明します。

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12)

## [!UICONTROL Life Cycle events]  {#life-cycle-events}

[!UICONTROL Lifecycle events] は標準です [!UICONTROL events]。次の[!UICONTROL events]を利用できます。

* [!UICONTROL launched]
* [!UICONTROL upgraded]
* [!UICONTROL crashed]

使用例としては、アップグレード後に新機能を紹介するメッセージや、イベントのプロモーションなどがあります。

>[!NOTE]
>
>[!UICONTROL Lifecycle module]は、モバイルアプリケーションで設定する必要があります。 [アプリにライフサイクルを追加する方法](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle)について詳しくは、こちらを参照してください

## [!UICONTROL Analytics Events] {#analytics-events}

モバイルアプリで実装されるカテゴリに応じて、以下の3つの実装がサポートされます。

* Adobe Analytics
* [!UICONTROL Context data]
* [!UICONTROL View state]

>[!NOTE]
>
>[!UICONTROL Analytics events] Adobe Analyticsのライセンスが必要です。[[!DNL Analytics] 拡張子を](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#configure-analytics-extension-in-launch)設定し、[AnalyticsをApp](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#add-analytics-to-your-app)に追加すると、これらのイベントはACSの[!UICONTROL In-App]設定で使用できるようになります。

## その他のリソース

* [ライフサイクル指標の有効化（ドキュメント）](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
