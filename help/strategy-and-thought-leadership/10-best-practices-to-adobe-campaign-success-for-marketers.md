---
title: マーケター向けAdobe Campaign成功のベストプラクティス 10 件
description: Adobe Campaignをご利用のお客様にとって、デジタル消費者の変革を解き放ち、迅速に実現し、より優れたエクスペリエンスを提供する 10 のベストプラクティスについて説明します。
doc-type: article
role: User
level: Beginner
kt: 11779
last-update-author: 20230130
source-git-commit: 26570845b0516d60d333afb8addc1de46947c88a
workflow-type: tm+mt
source-wordcount: '1279'
ht-degree: 0%

---


# の 10 のベストプラクティス [!DNL Adobe Campaign] マーケター向け成功

Christian Klimczyk は、7 年間の自称「Adobe・ナード」です [!DNL Adobe Experience Cloud] 主に専門知識 [!DNL Adobe Campaign]. 大規模な CPG 会社のAdobeプラットフォーム所有者として、クリスチャンと彼のチームは [!DNL Campaign] （すべての消費者通信およびインタラクション） ダイレクトメール、E メール、SMS/MMS をまたいで、規制要件の厳しさやマルチチャネル消費者マーケティングキャンペーンをシームレスに調整および管理します。

この記事では、Adobe Campaignの実践者がデジタル消費者の変革を解き放ち、加速し、顧客にとってより良い経験を提供するためのベストプラクティスを紹介します。


## 1.包括的なマーケティングと配信計画の策定

を成功に導くための最初の手順 [!DNL Adobe Campaign] は、あらゆる種類のマーケティングにおいて、お客様のツールと期待を理解することです。 消費者に連絡するために使用するチャネルを明確に定義し、理解し、それらのチャネルを使用するタイミングと理由を把握します。

Adobe Campaignは、通信を様々な方法で実行および調整できる柔軟なツールです。 [顧客の半分が、購入ジャーニーごとに 3～5 チャネルでエンゲージする](https://www.mckinsey.com/capabilities/operations/our-insights/redefine-the-omnichannel-approach-focus-on-what-truly-matters). そのため、これらのチャネルを事前に使用する方法を理解し、計画を立てることは、プラットフォームの可能性を最大限に高め、お客様の共感を呼ぶために重要です。

## 2.顧客データを文書化し、理解する

<!-- Sandra, this paragraph opens as if it's going to discuss the advantages of segmentation, but it left me hanging. So, I hit the Hubspot link and dug into it a bit, and it seemed to me like the juicy information is this quote: 

"A study by Hubspot revealed that 30% of the marketers who participated in it used market segmentation techniques to improve email engagement. Segmented campaigns had 14.31% higher open rates and saw 101% more clicks than non-segmented campaigns.

"Email marketers who segmented their audience before campaigning stated that the revenue generated increased to up to 760%. Targeted and segmented emails bring in 58% of all revenue." [Link](https://www.notifyvisitors.com/blog/segmentation-statistics/) 

I added that second paragraph about 760% revenue and broke up the rest of the section, touched it up to help make the Hubspot example a little more impactful. If I altered this section too much, you can reject the change. It didn't have mistakes, but it felt like it didn't tie the segment example strongly enough to the point about data design. See if this is okay...-->

以下に従う： [ハブスポット研究](https://www.linkedin.com/pulse/customer-segmentation-effective-b2b-business-industry-sabreen)のセグメント化キャンペーンでは、開封率が 14.31%高く、非セグメント化キャンペーンよりも 101%多くのクリック数が見られました。 キャンペーンの前にオーディエンスをセグメント化した電子メールマーケターは、生み出された売上高が最大 760%増加したと述べています。

Adobe Campaignでは、セグメント化をすばやく簡単に調整できます。 ただし、このプロセスを合理化し、容易にするには、キャンペーンの作成と実行を設計およびリクエストする際に、キャンペーンオペレーターとマーケティング担当者が基になるデータを文書化して理解している必要があります。 現在のデータを把握し、お客様の [!DNL Campaign] インスタンス。

キャンペーンは、それらをサポートする基になるデータ構造と同じ程度の効果を発揮します。 また、このデータ構造を把握し、ドキュメント化することは、プラットフォームの統合時や消費者データプラットフォームにジャンプする際に問題が発生した場合にも役立ちます

## 3.キャンペーンのタイミングを計画する

お客様と同じように、日課があります。 キャンペーンの送信と編成は、このリズムに対応している必要があります。 そうしないと、 [送信済みメールの 85%が開封されておらず、98%がクリックスルーを受け取っていない](https://www.validity.com/resource-center/state-of-email-2021/).

例えば、顧客が朝に電話で最良の契約をチェックしている場合、プロモーションのメールを送信することを検討します。 次のホットトレンドの夜に閲覧している場合は、無料配送のプロモコードを含むフォローアップメールを送信することを検討します。 また、 [!DNL Campaign] ：ワークフローと送信がいつ実行中かを追跡します。 複数のブランドをまたいだコミュニケーションの調整と容易化は困難な場合があります。 [E メールのリズム、ケイデンス、タイミングを把握し、常に目を通しています](https://experienceleaguecommunities.adobe.com/t5/adobe-campaign-classic-blogs/predictive-send-time-optimization-with-adobe-campaign/ba-p/561554) は、メッセージや Campaign インスタンスの全体的な安定性と強度にとって非常に役立ちます。

## 4.パーソナライゼーションを使用します。

現在、消費者は受信するメッセージにある程度のパーソナライゼーションを期待しています。 [顧客の 80%は、パーソナライズされたエクスペリエンスを提供するブランドから購入する可能性が高くなります](https://us.epsilon.com/power-of-me). 件名の名前は優れています。 ただし、パーソナライゼーションはさらに進むことができます。 閲覧した製品を含めたり、類似の製品と結び付けたり、ブランドの統合的なエクスペリエンスやルックアンドフィールを強化し続けたりできます。 各ビットがメッセージのエンゲージメントと開封率を向上させます。

## 5.クリエイティブアセットの健全な在庫を保有する

クリエイティブアセットは、効果的で油井の良いキャンペーン配信エンジンの実現に役立つガソリンです。 消費者に届くのに成功すればするほど、マーケティングプロセスを拡大し、成熟するに従って、よりクリエイティブなコンテンツが必要になります。 消費者は、これを期待しています。

チームが設定できる次の配信の速度に制限されます。 多くの場合、新しい魅力的なコンテンツが必要です。 [!DNL Adobe Campaign] では、テンプレートの設定や、これらの配信の受信および準備が簡単におこなえます。 しかし、クリエイティブの健全なパイプラインを持つことは、 [Litmus レポート](https://www.litmus.com/resources/state-of-email/)を使用している場合、マーケティング担当者の 58%が、1 つの E メールキャンペーンを作成するのに 2 週間以上かかることに注意しています。

## 6.購読と環境設定を理解し、管理する

サブスクリプション設定の管理と管理は、すぐに混乱を招き、様々なレベルのリスクが生じる可能性があります。 顧客に返信しないチャネルを介して間違ったメッセージを送信するのと同様に、10 人中 9 人の消費者は、否定的な経験を持つことで、将来的にブランドで買い物をする可能性が低くなると述べています。 大規模には、規制やコンプライアンスに関するリスクや罰金にさらされる可能性があります。

の専門家による使用を通じて、オプトインの管理と、進化し続けるこのエコシステムの育成に先立つ戦略を立てる [!DNL Adobe Campaign] および他のマーケティングテクノロジーツール 多くの場合、これはキャンペーン成功指標の 1 つです。慎重な計画をおこなうと、キャンペーン戦略が成長し成長するにつれ、貴重な配当が支払われます。

## 7.配信品質の把握と計画

_配信品質_ 神秘的で複雑な概念のように見えます。 配信品質の重要な基本ルールは、戦略的計画です。 IP アドレスのウォーミングアップと評判の構築には時間がかかります。 レピュテーションが急速に低下する可能性があるので、発生した損害を修復するのが困難です。 実際 **6 通に 1 通のメールが受信ボックスに届かない**.

配信品質の問題は、技術的な要因や、消費者がマーケティングにどのように反応するかに基づく問題が複数の要因によって発生する可能性があります。 保持 [配信品質](https://business.adobe.com/products/campaign/email-deliverability.html) キャンペーンを作成および実行する際、および遡及プロセスにおいて、健全で安定した環境を維持し、顧客に対して引き続きポジティブなエクスペリエンスを提供できます。

## 8.キャンペーン遡及プロセスの計画と開発

キャンペーンの配信と編成に忙しい状況であれば、多くの場合、達成したことを確認し、プロセスやキャンペーンのセグメント化を再評価するのに、それ以上ではなく、非常に強力です。 キャンペーン実行の規模と速度に応じて、2 ～ 4 週間ごとにキャンペーン遡及的な検証を保持します。

テンプレート化された一連の質問を作成すると、キャンペーンのリードタイム、クリエイティブ、セグメント化を他の多くのトピックの中で改善する方法に関する深く考慮深い会話が役立ちます。 以前に実行した内容を基にして学習した場合にのみ、を改善し、より速くすることができます。

## 9.テストと反復

新しいことを試すとき、初めて正しいとは限りません。 したがって、プロセスや戦術のテストや反復が重要です。 ロングショットの場合や適切な場合がある顧客のグループを試してみます。 クリエイティブを切り替えます。 新しいコールトゥアクションを試してみてください。 変化のための変更は生産的ではありませんが、多くの小さく正確な実験は、将来の大きな成果をもたらす可能性があります。

## 10.できるだけ機敏に保つ

市場は変化を続け、急速に動き続けている。 キャンペーンチームができるだけ軽く機敏になるように促すことは、お客様の期待に応え、競争を進め続ける上で重要です。

[デジタルマーケティングのリーダーの 35%は、自社の組織内で最も大きな課題が生じていると考えています](https://www.gartner.com/en/newsroom/press-releases/gartner-says-35--of-digital-marketing-leaders-believe-the-bigges). これを実現するには、いくつかのプラットフォームでのクロストレーニング、データフローや構造、その他のAdobeソリューションの理解を深め、キャンペーンのコンティンジェンシープランを作成します。 この考え方は多くの方法で実現できますが、短期的および長期的な成功を達成するには、俊敏性と計画に対する全体的なコミットメントが重要です。
