---
description: 'null'
seo-description: 'null'
seo-title: テストrubric 0.0.8
title: テストrubric 0.0.8
uuid: c62b7169-a650-4650-876f-c254eb57cb25
translation-type: tm+mt
source-git-commit: b56d3d2bd79c812fda6a75827d14044d9a8a3b4c

---


# テストrubric 0.0.8{#test-rubric}

## テストrubric 0.0.8

<!-- Note to writer: Please review the tables on this page for formatting and accuracy. Compare to original file.-->

![](assets/space.png)

## アラート {#alerts}

Auditorがテスト用に表示するアラートの詳細については、このリファレンスを参照してください。

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
    <td colname="col1"> <p><b>Advertising Cloud — 正しいコンバージョンタグが実装されている</b> </p> <p>重み：0 </p> </td> 
    <td colname="col2"> <p>正しいコンバージョンタグが使用されているかどうかを確認します。 </p> <p> <p>警告： 非推奨のTubeMogulコンバージョンタグを使用すると、データが失われる可能性があります。 </p> </p> </td> 
    <td colname="col3"> <p>コンバージョンピクセルを新しいAdvertising cloud画像のみのコンバージョンタグにアップグレードします。 </p> <p>これは、Advertising Cloud Launch Extensionを使用して、最も簡単に実行できます。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud — 画像のみのタグ</b> </p> <p>重み：0 </p> </td> 
    <td colname="col2"> <p>Advertising cloudの画像ピクセル形式は、次の推奨形式のいずれかに一致する必要があります。 </p> <p> 
      <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
       <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph"> http(s)://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
       <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph"> http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
       <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph"> http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
      </ul> </p> </td> 
    <td colname="col3"> <p>Advertising cloudのピクセルを新しいAdvertising cloudの画像のみのタグにアップグレードすると、Advertising cloudの全機能を確実に活用できます。 </p> <p>これは、Advertising Cloud Launch Extensionを使用して、最も簡単に実行できます。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud — セグメントピクセルのDSP同期が有効</b> </p> <p>重み：0 </p> </td> 
    <td colname="col2"> <p>TubeMogulセグメントピクセルにDSP同期設定が含まれているかどうかを確認し、その設定をピクセルに追加することをお勧めします。 </p> <p>DSP Syncing設定は、クエリ文字列パラメータを使用して決定されるので、 </p> <p>タグが(<span class="codeph"> "https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> OR <span class="codeph"> "http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> OR <span class="codeph"> "http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?"</span> </p> <p>ANDタグにはURLパラメータ「sid=」 <span class="codeph"> が含まれます)。</span> </p> <p>次に、URLパラメータ <span class="codeph"> "cs=0</span> "または<span class="codeph"> "cs=1"が存在するかどうかを確認し、オーディエンスの一致率を向上させるために、これらのピクセルに"</span> cs=1 <span class="codeph"></span> "を追加することをお勧めしません。 </p> </td> 
    <td colname="col3"> <p> DSP同期が発生するように、URLパラ <span class="codeph"> メーター「cs=1</span> 」をAdvertising cloudピクセルに追加します。これにより、オーディエンスの一致率が向上します。 </p> <p>これは、Advertising Cloud Launch Extensionを使用すると、最も簡単に実行できます。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM - pageBottomコールバックの配置</b> </p> <p>重み：0 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> 追加情報</a> </p> 
     <draft-comment>
       TEa9df69942f404055a64262889c8b21d3 
     </draft-comment> </td> 
    <td colname="col2"> <p> Dynamic Tag Managementには<span class="codeph"> _satellite.pageBottom()関数が必要です</span> 。 </p> <p>&lt;body&gt;内の最後のタグはタグにす <i>る</i> ことをお勧め <span class="codeph"> します</span>。 &lt;body&gt;タグ内に見つかった場合、機能する可能性がありますが <span class="codeph"></span> 、ベストプラクティスではないので、機能が正しくない場合や、予期しない結果や望ましくない結果が生じる場合があります。 </p> </td> 
    <td colname="col3"> <p>DTMの正しい機能を確保するために、&lt;/body&gt; <span class="codeph"> タグの直前にインラインスクリプトを追加します</span> 。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> Experience Cloud IDサービス — 1つのAdobeOrgのみを使用</b> </p> <p>重み：0 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/id-request.html" format="html" scope="external"> 追加情報</a> </p> </td> 
    <td colname="col2"> <p>通常のMCID実装では、1つのAdobeOrgを使用する必要があります。 </p> </td> 
    <td colname="col3"> <p>この実装に複数のAdobeOrg IDが存在することを検証します。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> Target - mboxDefault内のコンテンツ</b> </p> <p>重み：0 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/functions-overview/mboxcreate-atjs.html" format="html" scope="external"> 追加情報</a> </p> </td> 
    <td colname="col2"> <p> at.jsを使用する場合は、mboxDefaultにコンテンツが存在する必要があります。 </p> </td> 
    <td colname="col3"> <p>コンテンツが使用可能であることを確認します。 </p> </td> 
   </tr> 
  </tbody> 
</table>

![](assets/space.png)

## 設定 {#configuration}

Auditorが設定で実行するテストの詳細については、このリファレンスを参照してください。

Auditorは、タグを他のルールおよび推奨ベストプラクティスと比較して評価します。

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
    <td colname="col1"> <p><b>Advertising Cloud — コンバージョン名に使用できる文字は英数字のみです</b> </p> <p>重み：3 </p> </td> 
    <td colname="col2"> <p>ev_conversion_property_nameパ <span class="codeph"> ラメーターには、「</span> ev_transid<span class="codeph"> 」パラメーター以外の数値と10進数のみを含める必要があります(</span>ev_transid <span class="codeph"></span> 値には、テキスト値または数値を含めることができます) </p> <p>ev_で始まるURLパ <span class="codeph"> ラメーターを含むeveresttech.net</span> pixelを探 <span class="codeph"> します</span>。 </p> <p>例： </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47</span> </p> </td> 
    <td colname="col3"> <p> トランザクションプロパティのパラメーターには、数値と10進数値のみを含めてください。 </p> <p> <p>警告： その他の値の型は、データの損失の原因となる場合があります。 </p> </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud — コンバージョン名にURLセーフ文字を使用する</b> </p> <p>重み：3 </p> </td> 
    <td colname="col2"> <p> コンバージョンプロパティ名にアンパサンドや疑問符を含めることはできません。 </p> <p> 例： </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
    <td colname="col3"> <p>トランザクションプロパティのパラメーターに、エンコードされていないアンパサンドや疑問符が含まれていないことを確認します。 これらはURL形式を壊します。 </p> <p> <p>警告：エンコードされていないアンパサンドまたは疑問符を含むプロパティパラメーター(例：ev_formComplete?=1 <span class="codeph"> またはev_formComplete&amp;Submit=1</span> ) <span class="codeph"></span>の場合、データが失われる可能性があります。 </p> </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud — トランザクションIDが正しく実装されている</b> </p> <p>重み：1 </p> </td> 
    <td colname="col2"> <p> プロパティ名 <span class="codeph"> ev_transid=</span> を空にすることはできません。 </p> <p>例： </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
    <td colname="col3"> <p>プロパティ名 <span class="codeph"> ev_transid=</span> のままにして値(<span class="codeph"> ev_transid=</span>)を指定しないでください。 値を指定せずにこのままにしておくと、トランザクションデータが失われる可能性があります。 ev_transid=に値を割り当 <span class="codeph"> てるか、ピクセルからパ</span> ラメータを削除します。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analytics - DOMでインスタンス化</b> </p> <p>重み：5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/testing-and-validation/testing-and-validation-process/impl-validation.html" format="html" scope="external"> 追加情報</a> </p> </td> 
    <td colname="col2"> <p> Adobe Analyticsコードがインストールされていないか、実行に失敗しています。 解析コードが見つからない場合は0を返します。 </p> </td> 
    <td colname="col3"> <p>Analyticsタグがページに実装され、後続のスクリプトアクティビティによってブロックされていないことを確認します。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analytics — インスタンス化は1回のみ</b> </p> <p>重み：5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/home.html" format="https" scope="external"> 追加情報</a> </p> </td> 
    <td colname="col2"> <p> Adobe Analyticsコードがページで複数回検出されました。. 解析コードが見つからない場合は0を返します。 </p> </td> 
    <td colname="col3"> <p>ページにAnalyticsタグが1つだけ存在することを確認します。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analytics — 最新バージョン</b> </p> <p>重み：3 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/appmeasurement/release" format="https" scope="external"> 追加情報</a> </p> </td> 
    <td colname="col2"> <p> ページでAnalyticsコードライブラリの最新バージョンが実行されていません。 Experience cloudテクノロジーを強化するコードライブラリは、パフォーマンスの向上を活用し、最新の機能を提供するために、常に更新およびツイークされています。 解析コードが見つからない場合は0を返します。 </p> </td>       
    <td colname="col3"> <p>Analyticsライブラリの最新バージョンをインストールします。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM — 自己ホスト型</b> </p> <p>重み：4 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/client-side-information.html" format="html" scope="external"> 追加情報</a> </p> </td> 
    <td colname="col2"> <p> DTMライブラリは、AdobeのAkamaiインスタンス上の <span class="filepath"> assets.adobedtm.comでホストされています</span>。 </p> <p> DTMの読み込みには自己ホスト型アプローチが推奨されます。これは、キャッシュ制御によるWebサイトのパフォーマンスの制御、サードパーティスクリプトの依存関係の軽減、および公開プロセスの制御の強化を実現するためです。 DTMライブラリは、独自のWebホスティングまたはCDNを使用してホストおよび管理できます。 </p> </td> 
    <td colname="col3"> <p>ページにDTMを読み込む場合は、自己ホスト型が推奨される方法です。 Akamai CDN経由のDTMホスティングはほとんどの場合機能しますが、自己ホスティングはページのパフォーマンスを向上させます。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM - DOM準備完了後にサードパーティタグが非同期に読み込まれる</b> </p> <p>重み：3 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/resources/load-order.html" format="html" scope="external"> 追加情報</a> </p> </td> 
    <td colname="col2"> <p>ユーザーの使い勝手が良い場合と正確なデータを収集する場合のバランスをとるには、サードパーティタグをDOM ready時にトリガーする必要があります。 これにより、サイトの機能に影響を与えずに、これらのトラッキングスクリプトを確実に実行できます。 </p> </td> 
    <td colname="col3"> <p>サードパーティのピクセルを実行するすべてのルールをDOM readyで実行するように調整して、この問題を解決します。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Experience Cloud IDサービス — 最新バージョン</b> </p> <p>重み：2 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/tools/macid.html" format="html" scope="external"> 追加情報</a> </p> </td> 
    <td colname="col2"> <p> ページで、最新バージョンの訪問者IDサービスコードライブラリvisitor <span class="codeph"> API.jsが実行されていません</span>。 Experience cloudテクノロジーを強化するコードライブラリは、パフォーマンスの向上を活用し、最新の機能を提供するために、常に更新およびツイークされています。 </p> </td> 
    <td colname="col3"> <p>訪問者IDサービスライブラリの最新バージョンをインストールします。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Target — 最新バージョン</b> </p> <p>重み：2 </p> <p><a href="https://marketing.adobe.com/resources/help/en_US/dtm/target/" format="html" scope="external"> 追加情報</a> </p> </td> 
    <td colname="col2"> <p> ページでTargetコードライブラリの最新バージョンが実行されていません。 Experience cloudテクノロジーを強化するコードライブラリは、パフォーマンスの向上を活用し、最新の機能を提供するために、常に更新およびツイークされています。 </p> </td> 
    <td colname="col3"> <p>Targetライブラリの最新バージョンをインストールします。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Target - mboxDefaultはmboxCreateの前に配置 </b> </p> <p>重み：5 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/functions-overview/mboxcreate-atjs.html" format="html" scope="external"> 追加情報</a> </p> </td> 
    <td colname="col2"> <p>mboxCreateの適切な使用方法は <span class="codeph"> 次のように</span> なります。 </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;! — 顧客コンテンツ —&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
    <td colname="col3"> <p>mboxCreate()を呼び出す前に、必ず <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;/div&gt;</span> タグを含めて <span class="codeph"> ください</span>。 at.jsは追加しません。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>ターゲット — 有効なDOCTYPE</b> </p> <p>重み：5 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/functions-overview/mboxcreate-atjs.html" format="html" scope="external"> 追加情報</a> </p> </td> 
    <td colname="col2"> <p> 無効なDOCTYPEが検出されました。 このシナリオでは、mboxは起動されません。 </p> <p>at.jsの場合、DOCTYPEは標準モードである必要があります。そうしないと、Targetは動作しません。 </p> </td> 
    <td colname="col3"> <p>ページ上のDOCTYPEを更新します。 </p> </td> 
   </tr> 
  </tbody> 
</table>

![](assets/space.png)

## タグの一貫性 {#tag-consistency}

このリファレンスでは、Auditorがタグの一貫性を確保するために実行するテストに関する詳細を説明します。

Auditorは、タグがURL間で一貫しているかどうかを評価します。

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
    <td colname="col1"> <p><b>Analytics — 一貫したコードバージョン </b> </p> <p>重み：5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/choose-implementation-method.html" format="html" scope="external"> 追加情報</a> </p> </td> 
    <td colname="col2"> <p> 複数のバージョンのAnalyticsコードが見つかりました。 </p> </td> 
    <td colname="col3"> <p>Analyticsのすべてのインスタンスを現在のバージョンに置き換えます。 </p> </td> 
   </tr> 
  </tbody> 
</table>

![](assets/space.png)

## タグ配置 {#tag-presence}

このリファレンスでは、Auditorがタグ配置に対して実行するテストに関する詳細を提供します。

Auditorは、タグが存在するかどうか、およびタグがページコード内の適切な場所にあるかどうかなどを評価します。

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
    <td colname="col1"> <p><b>Advertising Cloud — コード配置</b> </p> <p>重み：5 </p> </td> 
    <td colname="col2"> <p> Advertising cloudタグはDOMでは使用できません。 </p> </td> 
    <td colname="col3"> <p>Advertising cloud起動拡張を使用して、Advertising cloudタグを実装します。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud — セグメントピクセルが実装されている</b> </p> <p>重み：5 </p> </td> 
    <td colname="col2"> <p> Advertising cloudセグメントのピクセルを新しいAdvertising cloudの画像のみのタグにアップグレードします。 非推奨のAMOセグメントタグを使用すると、データが失われる可能性があります。 </p> </td> 
    <td colname="col3"> <p>Advertising cloudの起動拡張を使用して、Advertising cloudセグメントピクセルを実装します。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analytics - DOMに読み込まれました</b> </p> <p>重み：5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/home.html" format="https" scope="external"> 追加情報</a> </p> </td> 
    <td colname="col2"> <p> Adobe Analyticsタグが検出されませんでした。 </p> </td> 
    <td colname="col3"> <p>最新バージョンのAnalyticsをインストールします。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> DTM — ライブラリ読み込み済み</b> </p> <p>重み：5 </p> <p>追加情報: </p> <p> 
      <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
       <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://docs.adobe.com/content/help/en/dtm/using/admin/c-troubleshooting.html" format="html" scope="external"> DTMのトラブルシューティング</a> </li> 
       <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> ヘッダーおよびフッターコードの追加</a> </li> 
      </ul> </p> </td> 
    <td colname="col2"> <p> グローバル_satelliteオブジェクトがDOMに見つかりませんでした。 Dynamic Tag Managementがインストールされていないか、実行に失敗しています。 </p> </td> 
    <td colname="col3"> <p>DTMライブラリがページに実装され、後続のスクリプトアクティビティによってブロックされていないことを確認します。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> DTM - 1つの埋め込みコード</b> </p> <p>重み：5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/code.html" format="html" scope="external"> 追加情報</a> </p> </td> 
    <td colname="col2"> <p> 実稼働サイトで読み込むDTMライブラリは1つだけです。 </p> </td> 
    <td colname="col3"> <p>本番用ライブラリのみがページに読み込まれていることを確認します。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM - pageBottomコールバックは&lt;body&gt;に存在します</b> </p> <p>重み：5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> 追加情報</a> </p> </td> 
    <td colname="col2"> <p> _satellite. <span class="codeph"> pageBottom()コールバックが、Dynamic Tag Managementに必要な</span> ページの <span class="codeph"></span> &lt;body&gt;内で見つかりませんでした。 </p> <p>このテストは、 <span class="codeph"> pageBottom呼び出し </span>がページ上で見つからない場合、または&lt; <span class="codeph"></span> head&gt;タグ（または他の予期しない場所）にある場合に失敗します。 pageBottomが&lt;body&gt;タグ内で見つか <span class="codeph"> った場合</span> にのみ渡 <span class="codeph"> されます</span> 。 ページ上にない場合は、機能せず、他の2つのpageBottomテストも <span class="codeph"> 失敗します</span> 。 </p> </td> 
    <td colname="col3"> <p>DTMの正しい機能を確保するために、&lt;/body&gt; <span class="codeph"> タグの直前にインラインスクリプトを追加します</span> 。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM - pageBottomタグが実行されました。</b> </p> <p>重み：5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> 追加情報</a> </p> </td> 
    <td colname="col2"> <p> DTM <span class="codeph"> pageBottomタグが検出されませ</span> ん。 </p> <p>これは、if (false) {_satellite.pageBottom()} <span class="codeph"> と同じ結果になる</span> ifステートメント内で呼び出しが行われた場合に発生する可能性があります <span class="codeph"></span>。 したがって、タグが存在し、正しく配置されている場合でも、タグは起動しない可能性があります。 </p> </td> 
    <td colname="col3"> <p>各ページにDTM <span class="codeph"> pageBottom呼び出しをインストールします</span> 。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Experience Cloud IDサービス — cookieの存在</b> </p> <p>重み：5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/implementation-guides.html" format="html" scope="external"> 追加情報</a> </p> </td> 
    <td colname="col2"> <p> AMCV_ <span class="codeph"> cookieが見つかり</span> ませんでした。 訪問者オブジェクトは、VisitorAPI.jsコードからインスタンス化 <span class="codeph"> する必要があり</span> ます。 </p> </td> 
    <td colname="col3"> <p> DTM実装の場合は、AdobeOrg IDがMCIDツールに正しく入力されていることを確認します。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Experience Cloud IDサービス — MID値が存在する</b> </p> <p>重み：5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/cookies.html" format="html" scope="external"> 追加情報</a> </p> </td> 
    <td colname="col2"> <p> AMCV_cookieにmid値が見つかりま <span class="codeph"> せんでした</span> 。 </p> </td> 
    <td colname="col3"> <p>もう一度テストして、MCID APIの待ち時間を確認します。 問題が解決しない場合は、アドビカスタマーケアにお問い合わせください。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> Experience Cloud IDサービス — インストールが必要</b> </p> <p>重み：5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/overview.html" format="html" scope="external"> 追加情報</a> </p> </td> 
    <td colname="col2"> <p> Experience Cloud IDサービスコードが見つかりませんでした。 ECIDは、Experience cloudソリューションから最大限の価値を引き出すために推奨され、ECソリューション全体のID管理にとって重要です。 </p> </td> 
    <td colname="col3"> <p>最新バージョンのMCIDをインストールしてください。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> ターゲット — ライブラリが&lt;head&gt;に読み込まれました</b> </p> <p>重み：4 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> 追加情報</a> </p> 
     <draft-comment>
       TE61c380082a4b4706b28a84aa047599a7 
     </draft-comment> </td> 
    <td colname="col2"> <p> Targetライブラリは、 <span class="codeph"> &lt;head&gt;タグに読み込まれます</span> 。 </p> </td> 
    <td colname="col3"> <p> Targetライブラリが&lt;head&gt;タグに読み込まれていることを確 <span class="codeph"> 認します</span> 。 </p> </td> 
   </tr> 
  </tbody> 
</table>
