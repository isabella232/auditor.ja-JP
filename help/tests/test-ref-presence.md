---
description: このリファレンスでは、Adobe Experience Platform Auditor がタグの有無を確認するために実行するテストの詳細を説明します。
seo-description: このリファレンスでは、Adobe Experience Platform Auditor がタグの有無を確認するために実行するテストの詳細を説明します。
seo-title: タグの有無
title: タグの有無
uuid: 91aa355b-7022-431c-9837-e108b5ce604d
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '958'
ht-degree: 100%

---


# タグの有無

このリファレンスでは、Adobe Experience Platform Auditor がタグの有無を確認するために実行するテストの詳細を説明します。

Platform Auditor はタグの有無、およびタグがページコード内の適切な場所に配置されているかを評価します。

<table id="table_98A2E3F7B3154EEFA76D0CAE2FE97CAB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> テスト </th> 
   <th colname="col2" class="entry"> 条件 </th> 
   <th colname="col3" class="entry"> 推奨 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Advertising Cloud - コードの有無</b> </p> <p>重み付け：5 </p> </td> 
   <td colname="col2"> <p> Advertising Cloud タグは DOM では使用できません。 </p> </td> 
   <td colname="col3"> <p>Adobe Experience Platform Launch 用 Advertising Cloud 拡張機能を使用して、Advertising Cloud タグを実装します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Advertising Cloud - セグメントピクセルが実装されている</b> </p> <p>重み付け：5 </p> </td> 
   <td colname="col2"> <p> Advertising Cloud セグメントピクセルを新しい Advertising Cloud の画像専用コンバージョンタグにアップグレードしてください。非推奨の AMO セグメントタグを使用すると、データが失われる可能性があります。 </p> </td> 
   <td colname="col3"> <p>Platform Launch 用 Advertising Cloud 拡張機能を使用して、Advertising Cloud セグメントピクセルを実装します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Analytics - DOM に読み込まれている</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/analytics/implementation/home.html" format="https" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p> Adobe Analytics タグが検出されませんでした。 </p> </td> 
   <td colname="col3"> <p>最新バージョンの Analytics をインストールしてください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM - ライブラリが読み込まれている</b> </p> <p>重み付け：5 </p> <p>追加情報: </p> <p> 
     <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
      <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://docs.adobe.com/content/help/ja-JP/dtm/using/admin/c-troubleshooting.html" format="html" scope="external">DTM のトラブルシューティング</a> </li> 
      <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://docs.adobe.com/content/help/ja-JP/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> ヘッダーおよびフッターコードの追加</a> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p> DOM 内にグローバル _satellite オブジェクトが見つかりませんでした。Dynamic Tag Management がインストールされていないか、実行に失敗します。 </p> </td> 
   <td colname="col3"> <p>ページで DTM ライブラリが実装され、後続のスクリプトアクティビティによってブロックされていないことを確認します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM - 埋め込みコードが 1 つ</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/dtm/using/client-side/code.html" format="html" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p> 実稼動サイトでは、1 つの DTM ライブラリのみを読み込みます。 </p> </td> 
   <td colname="col3"> <p>実稼動ライブラリのみがページに読み込まれていることを確認してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM - &lt;body&gt; 内に pageBottom コールバックが存在する</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p> Dynamic Tag Management で必要な<span class="codeph"> _satellite.pageBottom()</span> コールバックが、<span class="codeph"> &lt;body&gt;</span> 内で見つかりませんでした。 </p> <p>このテストは、<span class="codeph">pageBottom </span>コールがページで見つからない、または <span class="codeph"> &lt;head&gt;</span> タグ内（または他の予期しない場所）にある場合に失敗します。<span class="codeph">pageBottom</span> が <span class="codeph">&lt;body&gt;</span> タグ内で見つかった場合にのみ合格となります。ページ上にない場合は機能せず、他の 2 つの <span class="codeph">pageBottom</span> テストも失敗します。 </p> </td> 
   <td colname="col3"> <p>DTM が適切に機能するよう、<span class="codeph">&lt;/body&gt;</span> 終了タグの直前にインラインスクリプトを追加します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM - pageBottom タグが実行された</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p> DTM <code> pageBottom</code> タグが検出されませんでした。 </p> <p><code> if (false) {_satellite.pageBottom()}</code> と似た結果になる <code> if</code> ステートメント内で呼び出しが行われた場合に発生する可能性がありますしたがって、タグが存在し、正しく配置されている場合でも、タグは起動しない可能性があります。 </p> </td> 
   <td colname="col3"> <p>各ページに DTM <code> pageBottom</code> 呼び出しをインストールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Experience Cloud ID サービス - コードの有無</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/id-service/using/intro/overview.html" format="html" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID サービスコードが見つかりませんでした。Experience Cloud ID（MCID）は、Experience Cloud ソリューションから最大限の価値を引き出すために強く推奨され、Experience Cloud ソリューション全体の ID 管理にとって重要です。 </p> </td> 
   <td colname="col3"> <p> 最新バージョンの MCID をインストールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Experience Cloud ID サービス - Cookie の有無</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/dtm/using/tools/macid.html" format="html" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">AMCV_</span> cookie が見つかりませんでした。訪問者オブジェクトは、<span class="codeph">VisitorAPI.js</span> コードからインスタンス化する必要があります。 </p> </td> 
   <td colname="col3"> <p> DTM 実装の場合は、AdobeOrg ID が MCID ツールに正しく入力されていることを確認します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Experience Cloud ID サービス - MID 値が存在する</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/id-service/using/intro/cookies.html" format="html" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">AMCV_</span> cookie に MID 値が見つかりませんでした。 </p> </td> 
   <td colname="col3"> <p>もう一度テストして、MCID API の遅延時間を確認してください。問題が解決しない場合は、アドビカスタマーケアにお問い合わせください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch - ライブラリが読み込まれている</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/launch/using/intro/get-started/quick-start.html" format="https" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p> DOM 内にグローバル _satellite オブジェクトが見つかりませんでした。Platform Launch がインストールされていないか、実行に失敗します。 </p> </td> 
   <td colname="col3"> <p>ページで Platform Launch ライブラリが実装され、後続のスクリプトアクティビティによってブロックされていないことを確認します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch - 複数の埋め込みスクリプトがない</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p>ページに複数の埋め込みスクリプトを読み込まないでください。実稼動サイトでは、1 つの Platform Launch ライブラリのみを読み込みます。 </p> </td> 
   <td colname="col3"> <p>実稼動ライブラリのみがページに読み込まれていることを確認してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch - &lt;body&gt; 内に pageBottom コールバックが存在する</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p> Platform Launch で必要な<span class="codeph"> _satellite.pageBottom()</span> コールバックが、<span class="codeph"> &lt;body&gt;</span> 内で見つかりませんでした。 </p> <p>このテストは、<span class="codeph">pageBottom </span>コールがページで見つからない、または <span class="codeph"> &lt;head&gt;</span> タグ内（または他の予期しない場所）にある場合に失敗します。<span class="codeph">pageBottom</span> が <span class="codeph">&lt;body&gt;</span> タグ内で見つかった場合にのみ合格となります。ページ上にない場合は機能せず、他の 2 つの <span class="codeph">pageBottom</span> テストも失敗します。 </p> </td> 
   <td colname="col3"> <p>Platform Launch が適切に機能するよう、<span class="codeph">&lt;/body&gt;</span> 終了タグの直前にインラインスクリプトを追加します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch - 非同期でデプロイする場合は pageBottom コールバックを使用しない</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p><span class="codeph">_satellite.pageBottom()</span> コールバックがページで見つかりました。Platform Launch が非同期でデプロイされている場合は、このようにはなりません。 </p> </td> 
   <td colname="col3"> <p><span class="codeph">_satellite.pageBottom()</span> スクリプトを削除して、正しい Platform Launch 機能を有効にします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target - コードの有無</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/target/using/implement-target/implementing-target.html" format="html" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p>Target は、DOM で定義する必要があります。 </p> </td> 
   <td colname="col3"> <p>最新バージョンの Target（at.js）をインストールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Target - &lt;head&gt; でライブラリが読み込まれました</b> </p> <p>重み付け：4 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p> Target ライブラリは、<span class="codeph">&lt;head&gt;</span> タグに読み込まれます。 </p> </td> 
   <td colname="col3"> <p> Target ライブラリが <span class="codeph">&lt;head&gt;</span> タグに読み込まれていることを確認してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>
