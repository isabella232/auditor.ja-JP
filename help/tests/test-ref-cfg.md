---
description: このリファレンスでは、Adobe Experience Platform監査が設定で実行するテストの詳細について説明します。
seo-description: このリファレンスでは、Adobe Experience Platform監査が設定で実行するテストの詳細について説明します。
seo-title: 設定
title: 設定
uuid: d40d815c-edfe-48b9-921f-cea1b0b54a0a
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 89%

---


# 設定

このリファレンスでは、Adobe Experience Platform監査が設定で実行するテストの詳細について説明します。

構成テストでは、実装内の特定の設定や値、または競合の可能性をスキャンします。Platform Auditorは、タグを他のルールおよび推奨されるベストプラクティスと比較して評価します。

<table id="table_A8A1FC360482447185C8460A18426638"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> テスト </th> 
   <th colname="col2" class="entry"> 条件 </th> 
   <th colname="col3" class="entry"> 推奨 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - コンバージョン名は英数字のみを使用している</b> </p> <p>重み付け：3 </p> </td> 
   <td colname="col2"> <p><span class="codeph"> ev_conversion_property_name</span> パラメーターには、「<span class="codeph"> ev_transid</span>」パラメーター （<span class="codeph"> ev_transid</span> 値には、テキスト値または数値を含めることができます）以外の数値と 10 進数のみを含める必要があります） </p> <p><span class="codeph">ev_</span> で始まる URL パラメーターを含む、<span class="codeph">everesttech.net</span> ピクセルを探します。 </p> <p>例： </p> <p><span class="codeph">http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47 </span> </p> </td> 
   <td colname="col3"> <p> トランザクションプロパティのパラメーターには、数値と小数値のみを含めてください。 </p> <p> <p>警告： その他の値タイプは、データが失われる原因となる場合があります。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - コンバージョン名は URL で使用できる文字のみを使用している</b> </p> <p>重み付け：3 </p> </td> 
   <td colname="col2"> <p> コンバージョンプロパティ名に、アンパサンドや疑問符を含めることはできません。 </p> <p> 例： </p> <p><span class="codeph">http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>トランザクションプロパティのパラメーターに、エンコードされていないアンパサンドや疑問符が含まれていないことを確認してください。これらがあると、URL 形式が壊れます。 </p> <p> <p>警告：プロパティパラメーターにエンコードされていないアンパサンドまたは疑問符（例：<span class="codeph"> ev_formComplete?=1</span> または <span class="codeph"> ev_formComplete&amp;Submit=1</span>）が含まれる場合、データが失われる可能性があります。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - トランザクション ID が正しく実装されている</b> </p> <p>重み付け：1 </p> </td> 
   <td colname="col2"> <p> プロパティ名 <span class="codeph"> ev_transid=</span> を空にすることはできません。 </p> <p>例： </p> <p> <span class="codeph">http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>プロパティ名 <span class="codeph"> ev_transid=</span> には、値（<span class="codeph"> ev_transid=</span>）を含める必要があります。値が指定されていない場合、トランザクションデータが失われる可能性があります。<span class="codeph"> ev_transid=</span> に値を割り当てるか、ピクセルからパラメーターを削除します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics - DOM でインスタンス化されている</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/analytics/implementation/home.html" format="html" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p> Adobe Analytics コードがインストールされていないか、実行に失敗します。Web ページで解析コードが見つからない場合は、0 を返します。 </p> </td> 
   <td colname="col3"> <p>ページで Analytics タグが実装され、後続のスクリプトアクティビティによってブロックされていないことを確認します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics - インスタンス化は 1 回のみ</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/analytics/implementation/home.html" format="https" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p> Adobe Analytics コードがページで複数回検出されました。Web ページで解析コードが見つからない場合は、0 を返します。 </p> </td> 
   <td colname="col3"> <p>ページ上の Analytics タグが 1 つだけであることを確認します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics - 最新バージョン</b> </p> <p>重み付け：3 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/analytics/implementation/appmeasurement-updates.html" format="https" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p> ページで Analytics コードライブラリの最新バージョンが実行されていません。Experience Cloud テクノロジーの土台となるコードライブラリは、パフォーマンスの向上を活用し、最新の機能を提供できるよう、常に更新および調整されています。Web ページで解析コードが見つからない場合は、0 を返します。 </p> </td> 
   <td colname="col3"> <p>最新バージョンの Analytics ライブラリをインストールしてください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM - DOM Ready となった後、サードパーティタグが非同期に読み込まれる</b> </p> <p>重み付け：3 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/dtm/using/resources/load-order.html" format="html" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p>優れたユーザーエクスペリエンスと正確なデータ収集のバランスをとるため、DOM Ready 時にサードパーティタグをトリガーする必要があります。これにより、サイトの機能に影響を与えずに、これらのトラッキングスクリプトを確実に実行することができます。 </p> </td> 
   <td colname="col3"> <p>サードパーティのピクセルを実行するすべてのルールを DOM Ready 時に実行するように調整することで、この問題を解決します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Experience Cloud ID サービス - 最新バージョン</b> </p> <p>重み付け：2 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/dtm/using/tools/macid.html" format="html" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p> 訪問者 ID サービスコードライブラリ（<span class="codeph"> visitorAPI.js</span>）の最新バージョンがページで実行されていません。Experience Cloud テクノロジーの土台となるコードライブラリは、パフォーマンスの向上を活用し、最新の機能を提供できるよう、常に更新および調整されています。 </p> </td> 
   <td colname="col3"> <p>最新バージョンの訪問者 ID サービスライブラリをインストールしてください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - 最新バージョン</b> </p> <p>重み付け：2 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/launch/using/intro/get-started/quick-start.html" format="https" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p>これらのページでは、プラットフォーム起動コードライブラリ（タービン）の最新バージョンが実行されていません。 Experience Cloud テクノロジーの土台となるコードライブラリは、パフォーマンスの向上を活用し、最新の機能を提供できるよう、常に更新および調整されています。 </p> </td> 
   <td colname="col3"> <p> プラットフォーム起動ライブラリを再構築して発行することで、プラットフォーム起動ライブラリを更新します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target - 最新バージョン</b> </p> <p>重み付け：2 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/dtm/implementing/target/update-target-tool.html" format="html" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p> Target コードライブラリの最新バージョンがページで実行されていません。Experience Cloud テクノロジーの土台となるコードライブラリは、パフォーマンスの向上を活用し、最新の機能を提供できるよう、常に更新および調整されています。 </p> </td> 
   <td colname="col3"> <p>最新バージョンの Target ライブラリをインストールしてください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target - mboxDefault は mboxCreate よりも優先される</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/target/using/implement-target/client-side/mbox-implement/mbox-download.html" format="html" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> mboxCreate</span> の適切な使用方法は次のようになります。 </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;! -顧客コンテンツ--&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
   <td colname="col3"> <p><span class="codeph"> mboxCreate()</span> を呼び出す前に、必ず<span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;/div&gt;</span> タグを含めてください。at.js による追加はおこなわれません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target - 有効な DOCTYPE</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/help/ja-JP/target/using/implement-target/client-side/faq-at-js/target-atjs-faq.html#what-html-doctype-does-atjs-require" format="html" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p> 無効な DOCTYPE が検出されました。このシナリオでは、mbox は起動されません。 </p> <p>at.js の場合、DOCTYPE は標準モードである必要があります。そうしないと、Target は動作しません。 </p> </td> 
   <td colname="col3"> <p>ページ上の DOCTYPE を更新します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

