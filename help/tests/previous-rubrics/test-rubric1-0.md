---
description: adobe experience platform監査人試験に関する情報
seo-description: adobe experience platform監査人試験に関する情報
seo-title: テストルーブリック 0.0.8
title: テストルーブリック 0.0.8
uuid: c62b7169-a650-4650-876f-c254eb57cb25
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '2008'
ht-degree: 90%

---


# テストルーブリック 0.0.8 {#test-rubric}

## テストルーブリック 0.0.8

<!-- Note to writer: Please review the tables on this page for formatting and accuracy. Compare to original file.-->

![](assets/space.png)

## アラート {#alerts}

このリファレンスでは、テストに関して表示されるAdobe Experience Platform監査人の警告について詳しく説明します。

アラートは、認識する必要があるが、スコアには影響しない問題を示します。

<table id="table_031432C9BB804A6F90E7FF572739E169"> 
  <thead> 
   <tr> 
    <th colname="col1" class="entry"> テスト </th> 
    <th colname="col2" class="entry"> 条件 </th> 
    <th colname="col3" class="entry"> 推奨 </th> 
   </tr>
  </thead>
  <tbody> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud - 正しいコンバージョンタグが実装されている</b> </p> <p>重み付け：0 </p> </td> 
    <td colname="col2"> <p>正しいコンバージョンタグが使用されているかどうかを確認します。 </p> <p> <p>警告：非推奨の TubeMogul コンバージョンタグを使用すると、データが失われる可能性があります。 </p> </p> </td> 
    <td colname="col3"> <p>コンバージョンピクセルを新しい Advertising Cloud 画像専用コンバージョンタグにアップグレードします。 </p> <p>これはAdobe Experience Platform LaunchのAdvertising Cloud拡張で最も簡単に実現できます。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud - 画像専用タグ</b> </p> <p>重み付け：0 </p> </td> 
    <td colname="col2"> <p>Advertising Cloud の画像ピクセル形式は、次の推奨形式のいずれかと一致する必要があります。 </p> <p> 
      <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
       <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph">http(s)://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
       <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph">http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
       <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph">http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
      </ul> </p> </td> 
    <td colname="col3"> <p>Advertising Cloud の全機能を活用できるよう、Advertising Cloud のピクセルを新しい Advertising Cloud の画像専用タグにアップグレードします。 </p> <p>これは、Platform Launch用のAdvertising Cloud拡張機能を使用すると、最も簡単に実行できます。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud - セグメントピクセルの DSP 同期が有効になっている</b> </p> <p>重み付け：0 </p> </td> 
    <td colname="col2"> <p>TubeMogul セグメントピクセルに DSP 同期設定が含まれているかどうかを確認し、その設定をピクセルに追加することをお勧めします。 </p> <p>DSP Syncing 設定は、クエリ文字列パラメーターを使用して決定されるので、 </p> <p>タグが<span class="codeph"> （"https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> または <span class="codeph"> "http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> または <span class="codeph"> "http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?"</span>、 </p> <p>およびタグに URL パラメーター <span class="codeph"> "sid=" が含まれる）</span>に対して実行される場合、 </p> <p>URL パラメーター <span class="codeph"> "cs=0"</span> または<span class="codeph"> "cs=1"</span> が存在するかどうかを確認します。存在しない場合は、オーディエンスの一致率を向上させるために、これらのピクセルに <span class="codeph"> "cs=1"</span> を追加することをお勧めします。 </p> </td> 
    <td colname="col3"> <p> DSP 同期を実行できるよう、URL パラメーター <span class="codeph"> "cs=1"</span> を Advertising Cloud ピクセルに追加します。これにより、オーディエンスの一致率が向上します。 </p> <p>これは、Platform Launch用のAdvertising Cloud拡張機能を使用すると、最も簡単に実行できます。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM - pageBottom コールバックの配置</b> </p> <p>重み付け：0 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external">追加情報</a> </p> 
     <!--
       TEa9df69942f404055a64262889c8b21d3 
     --> </td> 
    <td colname="col2"> <p> Dynamic Tag Management には、<span class="codeph">_satellite.pageBottom()</span> 関数が必要です。 </p> <p>ベストプラクティスとして、このタグを<span class="codeph"> &lt;body&gt;</span> 内の<i>最後</i>のタグにすることをお勧めします。<span class="codeph">&lt;body&gt;</span> タグ内にある場合でも、機能する可能性はありますが、ベストプラクティスではないので、正しく機能しない場合や、予期しない結果や望ましくない結果が生じる場合があります。 </p> </td> 
    <td colname="col3"> <p>DTM が適切に機能するよう、<span class="codeph">&lt;/body&gt;</span> 終了タグの直前にインラインスクリプトを追加します。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Experience Cloud ID サービス - 1 つの AdobeOrg のみを使用する</b> </p> <p>重み付け：0 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/id-service/using/intro/id-request.html" format="html" scope="external">追加情報</a> </p> </td> 
    <td colname="col2"> <p>通常の MCID 実装では、単一の AdobeOrg を使用する必要があります。 </p> </td> 
    <td colname="col3"> <p>この実装に複数の AdobeOrg ID が存在することを検証します。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Target - mboxDefault 内のコンテンツ</b> </p> <p>重み付け：0 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/target/using/implement-target/client-side/functions-overview/mboxcreate-atjs.html" format="html" scope="external">追加情報</a> </p> </td> 
    <td colname="col2"> <p> at.js を使用する場合は、mboxDefault 内にコンテンツが存在する必要があります。 </p> </td> 
    <td colname="col3"> <p>コンテンツが使用可能であることを確認します。 </p> </td> 
   </tr> 
  </tbody> 
</table>

![](assets/space.png)

## 設定 {#configuration}

このリファレンスでは、Platform Auditorが設定で実行するテストの詳細について説明します。

Platform Auditorは、タグを他のルールおよび推奨されるベストプラクティスと比較して評価します。

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
    <td colname="col1"> <p><b>Advertising Cloud - コンバージョン名は英数字のみを使用している</b> </p> <p>重み付け：3 </p> </td> 
    <td colname="col2"> <p><span class="codeph"> ev_conversion_property_name</span> パラメーターには、「<span class="codeph"> ev_transid</span>」パラメーター （<span class="codeph"> ev_transid</span> 値には、テキスト値または数値を含めることができます）以外の数値と 10 進数のみを含める必要があります） </p> <p><span class="codeph">ev_</span> で始まる URL パラメーターを含む、<span class="codeph">everesttech.net</span> ピクセルを探します。 </p> <p>例： </p> <p><span class="codeph">http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47</span> </p> </td> 
    <td colname="col3"> <p> トランザクションプロパティのパラメーターには、数値と小数値のみを含めてください。 </p> <p> <p>警告： その他の値タイプは、データが失われる原因となる場合があります。 </p> </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud - コンバージョン名は URL で使用できる文字のみを使用している</b> </p> <p>重み付け：3 </p> </td> 
    <td colname="col2"> <p> コンバージョンプロパティ名に、アンパサンドや疑問符を含めることはできません。 </p> <p> 例： </p> <p><span class="codeph">http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
    <td colname="col3"> <p>トランザクションプロパティのパラメーターに、エンコードされていないアンパサンドや疑問符が含まれていないことを確認してください。これらがあると、URL 形式が壊れます。 </p> <p> <p>警告：プロパティパラメーターにエンコードされていないアンパサンドまたは疑問符（例：<span class="codeph"> ev_formComplete?=1</span> または <span class="codeph"> ev_formComplete&amp;Submit=1</span>）が含まれる場合、データが失われる可能性があります。 </p> </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud - トランザクション ID が正しく実装されている</b> </p> <p>重み付け：1 </p> </td> 
    <td colname="col2"> <p> プロパティ名 <span class="codeph"> ev_transid=</span> を空にすることはできません。 </p> <p>例： </p> <p><span class="codeph">http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
    <td colname="col3"> <p>プロパティ名 <span class="codeph"> ev_transid=</span> には、値（<span class="codeph"> ev_transid=</span>）を含める必要があります。値が指定されていない場合、トランザクションデータが失われる可能性があります。<span class="codeph"> ev_transid=</span> に値を割り当てるか、ピクセルからパラメーターを削除します。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analytics - DOM でインスタンス化されている</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/analytics/implementation/home.html" format="html" scope="external">追加情報</a> </p> </td> 
    <td colname="col2"> <p> Adobe Analytics コードがインストールされていないか、実行に失敗します。Web ページで解析コードが見つからない場合は、0 を返します。 </p> </td> 
    <td colname="col3"> <p>ページで Analytics タグが実装され、後続のスクリプトアクティビティによってブロックされていないことを確認します。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analytics - インスタンス化は 1 回のみ</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/analytics/implementation/home.html" format="https" scope="external">追加情報</a> </p> </td> 
    <td colname="col2"> <p> Adobe Analytics コードがページで複数回検出されました。Web ページで解析コードが見つからない場合は、0 を返します。 </p> </td> 
    <td colname="col3"> <p>ページ上の Analytics タグが 1 つだけであることを確認します。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analytics - 最新バージョン</b> </p> <p>重み付け：3 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/analytics/implementation/appmeasurement-updates.html" format="https" scope="external">追加情報</a> </p> </td> 
    <td colname="col2"> <p> ページで Analytics コードライブラリの最新バージョンが実行されていません。Experience Cloud テクノロジーの土台となるコードライブラリは、パフォーマンスの向上を活用し、最新の機能を提供できるよう、常に更新および調整されています。Web ページで解析コードが見つからない場合は、0 を返します。 </p> </td>       
    <td colname="col3"> <p>最新バージョンの Analytics ライブラリをインストールしてください。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM - 自己ホストされている</b> </p> <p>重み付け：4 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/dtm/using/client-side/client-side-information.html" format="html" scope="external">追加情報</a> </p> </td> 
    <td colname="col2"> <p> DTM ライブラリは、アドビの Akamai インスタンス上（<span class="filepath">assets.adobedtm.com</span>）でホストされています。 </p> <p> DTM の読み込みには、キャッシュ制御を通じた Web サイトのパフォーマンスの制御、サードパーティスクリプトの依存関係の軽減、および公開プロセスの制御の向上を提供する自己ホスト型アプローチが推奨されます。DTM ライブラリは、お客様自身の Web ホスティングまたは CDN を使用してホストおよび管理できます。 </p> </td> 
    <td colname="col3"> <p>ページに DTM を読み込む場合は、自己ホスト型アプローチを推奨します。Akamai CDN 経由の DTM ホスティングはほとんどの場合において機能しますが、自己ホスティングを使用すると、ページのパフォーマンスが向上します。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM - DOM Ready となった後、サードパーティタグが非同期に読み込まれる</b> </p> <p>重み付け：3 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/dtm/using/resources/load-order.html" format="html" scope="external">追加情報</a> </p> </td> 
    <td colname="col2"> <p>優れたユーザーエクスペリエンスと正確なデータ収集のバランスをとるため、DOM Ready 時にサードパーティタグをトリガーする必要があります。これにより、サイトの機能に影響を与えずに、これらのトラッキングスクリプトを確実に実行することができます。 </p> </td> 
    <td colname="col3"> <p>サードパーティのピクセルを実行するすべてのルールを DOM Ready 時に実行するように調整することで、この問題を解決します。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Experience Cloud ID サービス - 最新バージョン</b> </p> <p>重み付け：2 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/dtm/using/tools/macid.html" format="html" scope="external">追加情報</a> </p> </td> 
    <td colname="col2"> <p> 訪問者 ID サービスコードライブラリ（<span class="codeph"> visitorAPI.js</span>）の最新バージョンがページで実行されていません。Experience Cloud テクノロジーの土台となるコードライブラリは、パフォーマンスの向上を活用し、最新の機能を提供できるよう、常に更新および調整されています。 </p> </td> 
    <td colname="col3"> <p>最新バージョンの訪問者 ID サービスライブラリをインストールしてください。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Target - 最新バージョン</b> </p> <p>重み付け：2 </p> <p><a href="https://marketing.adobe.com/resources/help/ja_JP/dtm/target/" format="html" scope="external">追加情報</a> </p> </td> 
    <td colname="col2"> <p> Target コードライブラリの最新バージョンがページで実行されていません。Experience Cloud テクノロジーの土台となるコードライブラリは、パフォーマンスの向上を活用し、最新の機能を提供できるよう、常に更新および調整されています。 </p> </td> 
    <td colname="col3"> <p>最新バージョンの Target ライブラリをインストールしてください。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Target - mboxDefault は mboxCreate よりも優先される</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/target/using/implement-target/client-side/functions-overview/mboxcreate-atjs.html" format="html" scope="external">追加情報</a> </p> </td> 
    <td colname="col2"> <p><span class="codeph"> mboxCreate</span> の適切な使用方法は次のようになります。 </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;! -顧客コンテンツ--&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
    <td colname="col3"> <p><span class="codeph"> mboxCreate()</span> を呼び出す前に、必ず<span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;/div&gt;</span> タグを含めてください。at.js による追加はおこなわれません。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Target - 有効な DOCTYPE</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/target/using/implement-target/client-side/functions-overview/mboxcreate-atjs.html" format="html" scope="external">追加情報</a> </p> </td> 
    <td colname="col2"> <p> 無効な DOCTYPE が検出されました。このシナリオでは、mbox は起動されません。 </p> <p>at.js の場合、DOCTYPE は標準モードである必要があります。そうしないと、Target は動作しません。 </p> </td> 
    <td colname="col3"> <p>ページ上の DOCTYPE を更新します。 </p> </td> 
   </tr> 
  </tbody> 
</table>

![](assets/space.png)

## タグの整合性 {#tag-consistency}

タグの一貫性のためにPlatform Auditorが実行するテストについて詳しく説明します。

Platform Auditorは、タグがURL間で一貫しているかどうかを評価します。

<table id="table_4F9ED873BAF741D19BFB0F297B3A1FDB"> 
  <thead> 
   <tr> 
    <th colname="col1" class="entry"> テスト </th> 
    <th colname="col2" class="entry"> 条件 </th> 
    <th colname="col3" class="entry"> 推奨 </th> 
   </tr>
  </thead>
  <tbody> 
   <tr> 
    <td colname="col1"> <p><b>Analytics - コードバージョンが一貫している</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/analytics/implementation/home.html" format="html" scope="external">追加情報</a> </p> </td> 
    <td colname="col2"> <p> 複数のバージョンの Analytics コードが見つかりました。 </p> </td> 
    <td colname="col3"> <p>Analytics のすべてのインスタンスを最新のバージョンに置き換えてください。 </p> </td> 
   </tr> 
  </tbody> 
</table>

![](assets/space.png)

## タグの有無 {#tag-presence}

このリファレンスでは、Platform Auditorがタグを配置するために実行するテストについて詳しく説明します。

Platform Auditorは、タグが存在するかどうか、およびタグがページコード内の適切な場所にあるかどうかを評価します。

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
    <td colname="col3"> <p>Platform Launch用のAdvertising Cloud拡張機能を使用して、Advertising Cloudタグを実装します。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud - セグメントピクセルが実装されている</b> </p> <p>重み付け：5 </p> </td> 
    <td colname="col2"> <p> Advertising Cloud セグメントピクセルを新しい Advertising Cloud の画像専用コンバージョンタグにアップグレードしてください。非推奨の AMO セグメントタグを使用すると、データが失われる可能性があります。 </p> </td> 
    <td colname="col3"> <p>Platform Launch用のAdvertising Cloud拡張機能を使用して、Advertising Cloudセグメントピクセルを実装します。 </p> </td> 
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
    <td colname="col1"> <p><b>DTM - &lt;body&gt; 内に pageBottom コールバックが存在する</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external">追加情報</a> </p> </td> 
    <td colname="col2"> <p> Dynamic Tag Management で必要な<span class="codeph"> _satellite.pageBottom()</span> コールバックが、<span class="codeph"> &lt;body&gt;</span> 内で見つかりませんでした。 </p> <p>このテストは、<span class="codeph">pageBottom </span>コールがページで見つからない、または <span class="codeph"> &lt;head&gt;</span> タグ内（または他の予期しない場所）にある場合に失敗します。<span class="codeph">pageBottom</span> が <span class="codeph">&lt;body&gt;</span> タグ内で見つかった場合にのみ合格となります。ページ上にない場合は機能せず、他の 2 つの <span class="codeph">pageBottom</span> テストも失敗します。 </p> </td> 
    <td colname="col3"> <p>DTM が適切に機能するよう、<span class="codeph">&lt;/body&gt;</span> 終了タグの直前にインラインスクリプトを追加します。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM - pageBottom タグが実行された</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external">追加情報</a> </p> </td> 
    <td colname="col2"> <p> DTM <span class="codeph">pageBottom</span> タグが検出されませんでした。 </p> <p><span class="codeph"> if (false) {_satellite.pageBottom()}</span> と似た結果になる <span class="codeph"> if</span> ステートメント内で呼び出しが行われた場合に発生する可能性がありますしたがって、タグが存在し、正しく配置されている場合でも、タグは起動しない可能性があります。 </p> </td> 
    <td colname="col3"> <p>各ページに DTM <span class="codeph">pageBottom</span> 呼び出しをインストールします。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Experience Cloud ID サービス - Cookie の有無</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/dtm/using/tools/macid.html" format="html" scope="external">追加情報</a> </p> </td> 
    <td colname="col2"> <p> <span class="codeph">AMCV_</span> cookie が見つかりませんでした。訪問者オブジェクトは、<span class="codeph">VisitorAPI.js</span> コードからインスタンス化する必要があります。 </p> </td> 
    <td colname="col3"> <p> DTM 実装の場合は、AdobeOrg ID が MCID ツールに正しく入力されていることを確認します。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Experience Cloud ID サービス - MID 値が存在する</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/id-service/using/intro/cookies.html" format="html" scope="external">追加情報</a> </p> </td> 
    <td colname="col2"> <p> <span class="codeph">AMCV_</span> cookie に MID 値が見つかりませんでした。 </p> </td> 
    <td colname="col3"> <p>もう一度テストして、MCID API の遅延時間を確認してください。問題が解決しない場合は、アドビカスタマーケアにお問い合わせください。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Experience Cloud ID サービス - インストールが必要です</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/id-service/using/intro/overview.html" format="html" scope="external">追加情報</a> </p> </td> 
    <td colname="col2"> <p> Experience Cloud ID サービスコードが見つかりませんでした。ECID は、Experience Cloud ソリューションから最大限の価値を引き出すために強く推奨され、EC ソリューション全体の ID 管理にとって重要です。 </p> </td> 
    <td colname="col3"> <p>最新バージョンの MCID をインストールしてください。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Target - &lt;head&gt; でライブラリが読み込まれました</b> </p> <p>重み付け：4 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/target/using/implement-target/implementing-target.html" format="html" scope="external">追加情報</a> </p> 
     <!--
       TE61c380082a4b4706b28a84aa047599a7 
     --> </td> 
    <td colname="col2"> <p> Target ライブラリは、<span class="codeph">&lt;head&gt;</span> タグに読み込まれます。 </p> </td> 
    <td colname="col3"> <p> Target ライブラリが <span class="codeph">&lt;head&gt;</span> タグに読み込まれていることを確認してください。 </p> </td> 
   </tr> 
  </tbody> 
</table>
