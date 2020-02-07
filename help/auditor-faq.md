---
description: 'null'
seo-description: 'null'
seo-title: Auditor FAQ
title: Auditor FAQ
uuid: 4db0781a-b288-4ec2-97ff-410a8241a61d
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Auditor FAQ{#auditor-faq}

この記事では、Adobe Experience Platform Auditorに関するよくある質問とその回答を紹介します。

* [Auditorとは](auditor-faq.md#section-c4a9bc8d8eef41598c27e0951a2518e4)
* [私の会社はAuditorを使用する資格がありますか。](auditor-faq.md#section-f90094050d1e44929066a942833435cf)
* [AuditorはどのAdobeテクノロジーを採用していますか。](auditor-faq.md#section-52833b71c05448aaae508e6070a387f5)
* [監査はいくつ実行できますか。](auditor-faq.md#section-caac1e50ce1249aeba76308f3ef03fa0)
* [監査のためにクロールされるもの](auditor-faq.md#section-6d068ed69ece4a1bb6d0c34454550c45)
* [監査にはどのくらいの時間がかかりますか。](auditor-faq.md#section-5086ae27ef1f4671a9d951348654633a)
* [レポートにはどのような情報が表示されますか。](auditor-faq.md#section-752d6b82f6744a3182c4ce16ea6b5d3f)
* [その情報はどの程度対応可能ですか。](auditor-faq.md#section-9308c1ea882048b781087ae6d2eee9f0)
* [Auditorはアドビ以外のテクノロジーを監査できますか。](auditor-faq.md#section-f6e73c56083b4815bbf901296038bcd4)
* [IPアドレスをホワイトリストに登録してページのスキャンを許可する…](auditor-faq.md#section-011e4f54c58140ffb93bedeb0745b6cc)
* [AuditorはAbservePointと同じIP範囲を使用しますか。](auditor-faq.md#section-39512b156e194787981bdd572ff5b5a9)

## Auditorとは {#section-c4a9bc8d8eef41598c27e0951a2518e4}

Auditorは、デジタル実装の検証の専門家であるObservePointと共同開発されたAdobe Experience cloudのサービスです。

Auditorを使用すると、顧客は一度に最大500のWebページをスキャンし、Adobe Experience cloudの実装を改善する方法を示すレポートを受け取って、アドビの投資を最大限に活用できます。

## Auditorを使用する資格はありますか。 {#section-f90094050d1e44929066a942833435cf}

Adobe Experience cloudのすべての顧客組織に対して、Auditorへの無料アクセスが許可されます（2018年5月1日現在）。 各ユーザーは、Adobe Experience Cloud UIのAdobe/ObservePointの利用条件に同意してから、機能にアクセスする必要があります。 利用条件のオプトアウトについては、担当のアカウントマネージャーにお問い合わせください。

## Auditorにアクセスする方法を教えてください。 {#section-531ff85f94384831a89cbb4109549daf}

[https://experiencecloud.adobe.com](https://experiencecloud.adobe.com) にログインしたら、上部のナビゲーションの「**[!UICONTROL 有効化]**」をクリックすると、Auditor を見つけることができます。また、[https://auditor.adobe.com](https://auditor.adobe.com) に直接アクセスすることもできます。

## AuditorはどのAdobeテクノロジーを採用していますか。 {#section-52833b71c05448aaae508e6070a387f5}

* Advertising Cloud DSP
* Advertising cloud検索
* Analytics
* DTM
* Experience Cloud IDサービス（旧称Marketing Cloud IDサービス）
* Target

次のアドビソリューションは、現在、テストルーブラリックには含まれていません。 これらのソリューションのサポートは、今後の更新に備えて計画されています。

* Advertising Cloud Creative
* Audience Manager
* Campaign
* Launch

## 監査はいくつ実行できますか。 {#section-caac1e50ce1249aeba76308f3ef03fa0}

実行できる監査の数に制限はありません。 ユーザーは、1回に1つの監査の実行に制限されます。 実行中の監査と同じ設定で監査を開始しようとすると、エラーが発生します。

## 監査のためにクロールされるもの {#section-6d068ed69ece4a1bb6d0c34454550c45}

現在、ObservePoint技術は、ドキュメントリンク内のURLをクロールします。 ボタン、ページネーションウィジェット、およびその他のページエレメントで見つかったリンクはクロールされません。

## Auditorテストの新しい条件を提案する方法を教えてください。 {#section-926e6ef9225b4f0bb19c2927d634cd77}

Auditor Community ページ（[https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor](https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor)）の「**[!UICONTROL Share Feedback]**」をクリックして、テストの提案を送信できます。

## 監査にはどのくらいの時間がかかりますか。 {#section-5086ae27ef1f4671a9d951348654633a}

監査の完了に要する時間には、次のような要因が多くあります。

* ページ読み込み時間

   ObservePointエンジンは、監査の各ページをブラウザに読み込みます。 ページの読み込みが速くなるほど、監査の完了が速くなります。
* 同時接続

   Adobe Auditorは、各ページを訪問する際に1つの接続を使用します。 Full ObservePointアカウントでは、一度に最大10個のエンジンが使用されます。
* ネットワークの無音

   各ページが読み込まれた後、監査は7秒のネットワークの無音状態が続くのを待ってから、次のページに進みます。 ページの読み込み後に発生した多くのネットワーク要求がページから送信された場合、60秒後に待機がタイムアウトします。
* ページ再試行回数

   ページまたはタグが見つからない場合、監査はそのURLを保存し、監査の後半に戻ります。 監査では、一時的な問題が原因でエラーが発生していないことを確認するために、最大3回ページを訪問します。
* 処理中

   監査の実行後、収集されたすべてのデータが処理され、ルールによってフィルタリングされます。 この処理時間は大きく、スキャン自体に時間がかかりません。

>[!NOTE]
>
>Adobe Auditorは、一度に1回のスキャンを実行します。 Full ObservePointアカウントは、多くの監査を連続して実行できます。

## レポートにはどのような情報が表示されますか。 {#section-752d6b82f6744a3182c4ce16ea6b5d3f}

各スキャンで、スキャンされたURL、Webページで見つかった問題、および見つかった問題の修正方法に関する推奨事項を示すレポートが生成されます。

スキャンの結果は、次の3つのカテゴリに分類されます。

* 設定
* タグの一貫性
* タグ配置

この3つのカテゴリに加えて、このレポートには、注意が必要な情報を含むアラートが表示されますが、そのためにすぐに対処する必要はありません。

次に、これらのカテゴリに含まれるレコメンデーションは、次の3つの追加カテゴリに分類されます。

* 強く推奨
* 推奨
* 合格

## その情報はどの程度対応可能ですか。 {#section-9308c1ea882048b781087ae6d2eee9f0}

Auditorを通じて提供される推奨事項は、DTMやTargetなどのAdobe Experience cloudソリューションの実装に関する問題を解決するための対策を講じることを目的としています。 これを容易にするため、Auditorチームは広範囲に作業を進め、必要な作業をどこで行うかに関する詳細な指示を行ってきました。 スキャンされたすべてのURLとテスト結果のスプレッドシートを書き出して、問題のある領域を簡単に特定できます。 DTM実装に関する推奨事項の例を次に示します。

<table id="table_EE67775088344BDAA5126268072D6089"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>pageBottomコールバックlast</b> </p> <p>DTMを正しく実装するには、_satellite.pageBottom()関数が必要です。 DTMの正しい機能を確保するために、&lt;/body&gt;タグの直前にインラインスクリプトを追加します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Auditorはアドビ以外のテクノロジーを監査できますか。 {#section-f6e73c56083b4815bbf901296038bcd4}

いいえ。ただし、ObservePointのフル機能を使用すると、すべてのマーケティングタグとテクノロジーを監査および監視できます。 アドビのお客様は、無料の体験版アカウントをご利用いただけます。 体験版アカウントにアクセスするに [は、ObservePointのAuditor Pageを参照してください](https://www.observepoint.com/adobe-auditor/?utm_source=Adobe&utm_medium=Auditor&utm_campaign=Premium)。

## ログインで保護されたページのスキャンを許可するために、IPアドレスをホワイトリストに登録できますか。 {#section-011e4f54c58140ffb93bedeb0745b6cc}

この機能は、現在、ObservePointの完全な機能を使用しない限り、サポートされていません。

## AuditorはObservePointと同じIP範囲を使用しますか。 {#section-39512b156e194787981bdd572ff5b5a9}

クロールはObservePointによって実行されるので、同じIPアドレスが使用されます。

詳しくは、ObservePointのドキ [ュメントを参照](https://help.observepoint.com/articles/2312494-observepoint-whitelisting-and-proxy-list) してください。
