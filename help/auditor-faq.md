---
description: Adobe Experience Platform Auditor に関するよくある質問と回答
seo-description: Adobe Experience Platform Auditor に関するよくある質問と回答
seo-title: Adobe Experience Platform Auditor FAQ
title: Adobe Experience Platform Auditor FAQ
uuid: 4db0781a-b288-4ec2-97ff-410a8241a61d
exl-id: 75ab4497-5822-4f64-9b6d-6cbf13687e8d
translation-type: ht
source-git-commit: 286a857b2ff08345499edca2e0eb6b35ecf02332
workflow-type: ht
source-wordcount: '990'
ht-degree: 100%

---

# Adobe Experience Platform Auditor FAQ {#auditor-faq}

この記事では、Adobe Experience Platform Auditor についてのよくある質問とその回答を紹介します。

* [Adobe Experience Platform Auditor とは何ですか。](auditor-faq.md#section-c4a9bc8d8eef41598c27e0951a2518e4)
* [私の会社は Platform Auditor を使用する資格がありますか。](auditor-faq.md#section-f90094050d1e44929066a942833435cf)
* [Platform Auditor はどのアドビテクノロジーを採用していますか。](auditor-faq.md#section-52833b71c05448aaae508e6070a387f5)
* [監査は何件実行できますか。](auditor-faq.md#section-caac1e50ce1249aeba76308f3ef03fa0)
* [監査では、何がクロールの対象になりますか。](auditor-faq.md#section-6d068ed69ece4a1bb6d0c34454550c45)
* [監査にはどのくらいの時間がかかりますか。](auditor-faq.md#section-5086ae27ef1f4671a9d951348654633a)
* [レポートにはどのような情報が表示されますか。](auditor-faq.md#section-752d6b82f6744a3182c4ce16ea6b5d3f)
* [その情報はどの程度実用的ですか。](auditor-faq.md#section-9308c1ea882048b781087ae6d2eee9f0)
* [Platform Auditor はアドビ以外のテクノロジーを監査できますか。](auditor-faq.md#section-f6e73c56083b4815bbf901296038bcd4)
* [IP アドレスを承認してページのスキャンを許可することはできますか...](auditor-faq.md#section-011e4f54c58140ffb93bedeb0745b6cc)
* [Platform Auditor は ObservePoint と同じ IP 範囲を使用しますか。](auditor-faq.md#section-39512b156e194787981bdd572ff5b5a9)

## Adobe Experience Platform Auditor とは何ですか。{#section-c4a9bc8d8eef41598c27e0951a2518e4}

Platform Auditor は、デジタル実装の検証を専門とする ObservePoint と共同開発された、Adobe Experience Cloud のサービスです。

Platform Auditor を使用すると、顧客は一度に最大 500 の Web ページをスキャンし、Adobe Experience Cloud の実装の改善方法を示すレポートを受け取って、アドビの投資を最大限に活用できます。

## 私には Platform Auditor を使用する資格はありますか。{#section-f90094050d1e44929066a942833435cf}

Adobe Experience Cloud のすべての顧客組織に対して、Platform Auditor への無料アクセスが許可されます（2018 年 5 月 1 日（PT）現在）。各ユーザーは、機能にアクセスする前に、Adobe Experience Cloud UI の Adobe／ObservePoint の利用条件に同意する必要があります。利用条件のオプトアウトについては、担当のアカウントマネージャーにお問い合わせください。

## Platform Auditor にアクセスする方法を教えてください。{#section-531ff85f94384831a89cbb4109549daf}

[https://experiencecloud.adobe.com](https://experiencecloud.adobe.com) にログインしたら、上部のナビゲーションの「**[!UICONTROL Activation]**」をクリックすると、Platform Auditor を見つけることができます。また、[https://auditor.adobe.com](https://auditor.adobe.com) に直接アクセスすることもできます。

## Platform Auditor はどのアドビテクノロジーを採用していますか。{#section-52833b71c05448aaae508e6070a387f5}

* Advertising Cloud DSP
* Advertising Cloud 検索
* Analytics
* DTM
* Experience Cloud ID サービス（旧称 Marketing Cloud ID サービス）
* Target

次のアドビソリューションは現在、テストルーブリックには含まれていません。これらのソリューションのサポートは、今後のアップデートで予定されています。

* Advertising Cloud Creative
* Audience Manager
* Campaign
* Adobe Experience Platform Launch

## 監査は何件実行できますか。{#section-caac1e50ce1249aeba76308f3ef03fa0}

実行可能な監査の件数に制限はありません。ユーザーは、一度に 1 件のみを監査を実行できます。実行中の監査と同じ設定で監査を開始しようとすると、エラーが発生します。

## 監査では、何がクロールの対象になりますか。{#section-6d068ed69ece4a1bb6d0c34454550c45}

ObservePoint テクノロジーでは現在、ドキュメントリンク内の URL をクロールします。ボタンや、ページネーションウィジェット、その他のページエレメント内のリンクはクロール対象外になります。

## Platform Auditor テストの新しい条件を提案する方法を教えてください。{#section-926e6ef9225b4f0bb19c2927d634cd77}

Platform Auditor Community ページ（[https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor](https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor)）の「**[!UICONTROL Share Feedback]**」をクリックして、テストの提案を送信できます。

## 監査にはどのくらいの時間がかかりますか。{#section-5086ae27ef1f4671a9d951348654633a}

監査の完了に要する時間は、次のような要因の影響を受けます。

* ページ読み込み時間

   ObservePoint エンジンは、監査の各ページをブラウザーに読み込みます。ページの読み込みが速くなるほど、監査が早く完了します。
* 同時接続

   Platform Auditor は、それぞれのページに訪問するのに 1 つの接続を使用します。完全な ObservePoint アカウントでは、一度に最大 10 個のエンジンが使用されます。
* ネットワークのサイレント状態

   各ページが読み込まれた後、監査では、7 秒間ネットワークのサイレント状態が続くのを待ってから、次のページに進みます。ページの読み込み後に発生した多数のネットワーク要求がページから送信された場合、60 秒後に待機がタイムアウトします。
* ページ再試行回数

   ページまたはタグが見つからない場合、監査はその URL を保存し、監査の後半でその URL に戻ります。監査では、エラーの原因が一時的な問題でないことをを確認するために、最大 3 回ページを訪問します。
* 処理

   監査の実行後、収集したすべてのデータを処理し、ルールを通じてフィルタリングします。スキャン自体にはあまり時間はかかりませんが、この処理時間は長くかかります。

>[!NOTE]
>
>Platform Auditor は、一度に 1 件のスキャンを実行します。完全な ObservePoint アカウントでは、多数の監査を連続して実行できます。

## レポートにはどのような情報が表示されますか。{#section-752d6b82f6744a3182c4ce16ea6b5d3f}

スキャンごとに、スキャンされた URL、Web ページで見つかった問題、および見つかった問題の修正方法に関する推奨事項を示すレポートが生成されます。

スキャン結果は、次の 3 つのカテゴリに分類されます。

* 設定
* タグの整合性
* タグの有無

この 3 つのカテゴリに加えて、このレポートには、注意が必要な情報を含むアラートが表示されますが、必ずしもすぐに対処する必要はありません。

これらのカテゴリに含まれるレコメンデーションは、次の 3 つの追加カテゴリに分類されます。

* 強く推奨
* 推奨
* 合格

## その情報はどの程度実用的ですか。{#section-9308c1ea882048b781087ae6d2eee9f0}

Platform Auditor を通じて提供される推奨事項は、DTM や Target などの Adobe Experience Cloud ソリューションの実装に関する問題を修正するための対応をお手伝いすることを目的としています。これを容易にするため、Platform Auditor チームは広範囲に作業を進め、何をどこでおこなうかに関する詳細な指示を提供してきました。スキャンされたすべての URL とテスト結果のスプレッドシートを書き出して、問題のある領域を簡単に特定できます。DTM 実装に関するレコメンデーションの例を次に示します。

<table id="table_EE67775088344BDAA5126268072D6089"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>pageBottom コールバックが続く</b> </p> <p>DTM を正しく実装するには、_satellite.pageBottom() 関数が必要です。DTM が適切に機能するよう、&lt;/body&gt; 終了タグの直前にインラインスクリプトを追加します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Platform Auditor はアドビ以外のテクノロジーを監査できますか。{#section-f6e73c56083b4815bbf901296038bcd4}

いいえ。ただし、ObservePoint のフル機能を使用すると、すべてのマーケティングタグとテクノロジーを監査および監視できます。アドビのお客様は、無料の体験版アカウントをご利用いただけます。体験版アカウントにアクセスするには、[ObservePoint の Platform Auditor ページ](https://www.observepoint.com/adobe-auditor/?utm_source=Adobe&amp;utm_medium=Auditor&amp;utm_campaign=Premium)を参照してください。

## IP アドレスを承認して、ログインで保護されたページのスキャンを許可することはできますか。{#section-011e4f54c58140ffb93bedeb0745b6cc}

この機能は現在、完全な ObservePoint 製品を使用していない限り、サポートされていません。

## Platform Auditor は ObservePoint と同じ IP 範囲を使用しますか。{#section-39512b156e194787981bdd572ff5b5a9}

クロールは ObservePoint によって実行されるので、同じ IP アドレスが使用されます。

詳しくは、[ObservePoint のドキュメント](https://help.observepoint.com/articles/2312494-observepoint-whitelisting-and-proxy-list)を参照してください。
