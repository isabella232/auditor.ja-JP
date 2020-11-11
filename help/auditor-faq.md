---
description: Adobe Experience Platform Auditor に関するよくある質問と回答
seo-description: Adobe Experience Platform Auditor に関するよくある質問と回答
seo-title: Adobe Experience Platform Auditor FAQ
title: Adobe Experience Platform Auditor FAQ
uuid: 4db0781a-b288-4ec2-97ff-410a8241a61d
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '990'
ht-degree: 71%

---


# Adobe Experience Platform Auditor FAQ{#auditor-faq}

この記事では、Adobe Experience Platform Auditor についてのよくある質問とその回答を紹介します。

* [Adobe Experience Platform監査人とは何ですか？](auditor-faq.md#section-c4a9bc8d8eef41598c27e0951a2518e4)
* [会社はPlatform Auditorを使用する資格があるか。](auditor-faq.md#section-f90094050d1e44929066a942833435cf)
* [Platform Auditorが評価するAdobeテクノロジはどれですか。](auditor-faq.md#section-52833b71c05448aaae508e6070a387f5)
* [監査は何件実行できますか。](auditor-faq.md#section-caac1e50ce1249aeba76308f3ef03fa0)
* [監査では、何がクロールの対象になりますか。](auditor-faq.md#section-6d068ed69ece4a1bb6d0c34454550c45)
* [監査にはどのくらいの時間がかかりますか。](auditor-faq.md#section-5086ae27ef1f4671a9d951348654633a)
* [レポートにはどのような情報が表示されますか。](auditor-faq.md#section-752d6b82f6744a3182c4ce16ea6b5d3f)
* [その情報はどの程度実用的ですか。](auditor-faq.md#section-9308c1ea882048b781087ae6d2eee9f0)
* [Platform AuditorはAdobe以外のテクノロジーを監査できますか。](auditor-faq.md#section-f6e73c56083b4815bbf901296038bcd4)
* [IP アドレスを承認してページのスキャンを許可することはできますか...](auditor-faq.md#section-011e4f54c58140ffb93bedeb0745b6cc)
* [Platform AuditorはObsemepointと同じIP範囲を使用しますか。](auditor-faq.md#section-39512b156e194787981bdd572ff5b5a9)

## Adobe Experience Platform監査人とは何ですか？ {#section-c4a9bc8d8eef41598c27e0951a2518e4}

Platform Auditorは、ObservePointと共同開発されたAdobe Experience Cloudのサービスで、デジタル実装の検証の専門家です。

Platform Auditorを使用すると、一度に最大500のWebページをスキャンし、Adobe投資を最大限に活用できるように、Adobe Experience Cloudの実装を改善する方法を示すレポートを受け取ることができます。

## Am I eligible to use Platform Auditor? {#section-f90094050d1e44929066a942833435cf}

すべてのAdobe Experience Cloudのお客様の組織は、Platform Auditor（2018年5月1日現在）に無料でアクセスできます。 各ユーザーは、機能にアクセスする前に、Adobe Experience Cloud UI の Adobe／ObservePoint の利用条件に同意する必要があります。利用条件のオプトアウトについては、担当のアカウントマネージャーにお問い合わせください。

## How do I access Platform Auditor? {#section-531ff85f94384831a89cbb4109549daf}

After logging in at [https://experiencecloud.adobe.com](https://experiencecloud.adobe.com), you can find Platform Auditor by clicking on **[!UICONTROL Activation]** in the top navigation. また、[https://auditor.adobe.com](https://auditor.adobe.com) に直接アクセスすることもできます。

## Which Adobe technologies does Platform Auditor grade? {#section-52833b71c05448aaae508e6070a387f5}

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

## 監査は何件実行できますか。 {#section-caac1e50ce1249aeba76308f3ef03fa0}

実行可能な監査の件数に制限はありません。ユーザーは、一度に 1 件のみを監査を実行できます。実行中の監査と同じ設定で監査を開始しようとすると、エラーが発生します。

## 監査では、何がクロールの対象になりますか。 {#section-6d068ed69ece4a1bb6d0c34454550c45}

ObservePoint テクノロジーでは現在、ドキュメントリンク内の URL をクロールします。ボタンや、ページネーションウィジェット、その他のページエレメント内のリンクはクロール対象外になります。

## How do I suggest new criteria for Platform Auditor tests? {#section-926e6ef9225b4f0bb19c2927d634cd77}

You can submit test suggestions via the Platform Auditor Community by clicking **[!UICONTROL Share Feedback]** on this page: [https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor](https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor)

## 監査にはどのくらいの時間がかかりますか。 {#section-5086ae27ef1f4671a9d951348654633a}

監査の完了に要する時間は、次のような要因の影響を受けます。

* ページ読み込み時間

   ObservePoint エンジンは、監査の各ページをブラウザーに読み込みます。ページの読み込みが速くなるほど、監査が早く完了します。
* 同時接続

   Platform Auditorは、各ページを1つの接続で訪問します。 完全な ObservePoint アカウントでは、一度に最大 10 個のエンジンが使用されます。
* ネットワークのサイレント状態

   各ページが読み込まれた後、監査では、7 秒間ネットワークのサイレント状態が続くのを待ってから、次のページに進みます。ページの読み込み後に発生した多数のネットワーク要求がページから送信された場合、60 秒後に待機がタイムアウトします。
* ページ再試行回数

   ページまたはタグが見つからない場合、監査はその URL を保存し、監査の後半でその URL に戻ります。監査では、エラーの原因が一時的な問題でないことをを確認するために、最大 3 回ページを訪問します。
* 処理

   監査の実行後、収集したすべてのデータを処理し、ルールを通じてフィルタリングします。スキャン自体にはあまり時間はかかりませんが、この処理時間は長くかかります。

>[!NOTE]
>
>Platform Auditorは、一度に1回のスキャンを実行します。 完全な ObservePoint アカウントでは、多数の監査を連続して実行できます。

## レポートにはどのような情報が表示されますか。 {#section-752d6b82f6744a3182c4ce16ea6b5d3f}

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

## その情報はどの程度実用的ですか。 {#section-9308c1ea882048b781087ae6d2eee9f0}

Platform Auditorでの推奨事項はすべて、DTMやターゲットなどのAdobe Experience Cloudソリューションの実装に関する問題を解決するための対策を講じることを目的としています。 この作業を容易にするため、Platform Auditorチームは、必要な作業をどこで行うかに関する非常に詳細な指示を提供するために幅広く作業を行ってきました。 スキャンされたすべての URL とテスト結果のスプレッドシートを書き出して、問題のある領域を簡単に特定できます。DTM 実装に関するレコメンデーションの例を次に示します。

<table id="table_EE67775088344BDAA5126268072D6089"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>pageBottom コールバックが続く</b> </p> <p>DTM を正しく実装するには、_satellite.pageBottom() 関数が必要です。DTM が適切に機能するよう、&lt;/body&gt; 終了タグの直前にインラインスクリプトを追加します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Can Platform Auditor audit non-Adobe technology? {#section-f6e73c56083b4815bbf901296038bcd4}

いいえ。ただし、ObservePoint のフル機能を使用すると、すべてのマーケティングタグとテクノロジーを監査および監視できます。アドビのお客様は、無料の体験版アカウントをご利用いただけます。To access your trial account visit [ObservePoint’s Platform Auditor Page](https://www.observepoint.com/adobe-auditor/?utm_source=Adobe&amp;utm_medium=Auditor&amp;utm_campaign=Premium).

## IP アドレスを承認して、ログインで保護されたページのスキャンを許可することはできますか。 {#section-011e4f54c58140ffb93bedeb0745b6cc}

この機能は現在、完全な ObservePoint 製品を使用していない限り、サポートされていません。

## Does Platform Auditor use the same IP ranges as ObservePoint? {#section-39512b156e194787981bdd572ff5b5a9}

クロールは ObservePoint によって実行されるので、同じ IP アドレスが使用されます。

詳しくは、[ObservePoint のドキュメント](https://help.observepoint.com/articles/2312494-observepoint-whitelisting-and-proxy-list)を参照してください。
