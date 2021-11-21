---
title: イベントの設定
description: 「イベントが、どのユーザーが開始したアクションによって、表示するアプリ内メッセージをトリガーにするかを定義する方法を理解します。 」
feature: In App
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
source-wordcount: '213'
ht-degree: 3%

---

# 設定 [!UICONTROL Events] {#configuring-events}

を設定する際 [!UICONTROL In-App] メッセージを表示するには、メッセージを表示するユーザーが開始するアクショントリガーを定義する必要があります。 これらのアクションは、 [!UICONTROL events]. 次の 3 つのカテゴリー： [!UICONTROL events] は使用可能です。 [!UICONTROL Mobile Application events], [!UICONTROL Life Cycle events]、および [!UICONTROL Analytics events].

## [!UICONTROL Mobile Application Events] {#mobile-application-events}

[!UICONTROL Mobile Application events] が [!UICONTROL custom events] モバイルアプリケーションに実装される

以下に例を示します。

* 顧客が品目を閲覧した
* 顧客が買い物かごに品目を追加します
* 買い物かごの放棄
* 顧客が何かを購入した

これらを設定する必要があります [!UICONTROL events] Adobe Campaign 次のビデオでは、この方法を説明します。

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12)

## [!UICONTROL Life Cycle events] {#life-cycle-events}

[!UICONTROL Lifecycle events] 標準搭載 [!UICONTROL events]. 以下 [!UICONTROL events] は使用可能です。

* [!UICONTROL launched]
* [!UICONTROL upgraded]
* [!UICONTROL crashed]

使用例としては、アップグレード後に新機能を紹介するメッセージやイベントプロモーションなどがあります。

>[!NOTE]
>
>この [!UICONTROL Lifecycle module] は、モバイルアプリケーションで設定する必要があります。 詳しくは、こちらを参照してください。 [アプリにライフサイクルを追加する方法](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle)

## [!UICONTROL Analytics Events] {#analytics-events}

モバイルアプリに実装されている機能に応じて、次の 3 つのカテゴリがサポートされます。

* Adobe Analytics
* [!UICONTROL Context data]
* [!UICONTROL View state]

>[!NOTE]
>
>[!UICONTROL Analytics events] Adobe Analyticsライセンスが必要です。 次に、 [[!DNL Analytics] 拡張機能が設定されました](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#configure-analytics-extension-in-launch) とが追加されました。 [アプリに対する Analytics](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#add-analytics-to-your-app)を使用する場合、これらのイベントは [!UICONTROL In-App] ACS での設定

## その他のリソース

* [ライフサイクル指標の有効化（ドキュメント）](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
