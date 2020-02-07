---
description: Auditorがテスト用に表示するアラートの詳細については、このリファレンスを参照してください。
seo-description: Auditorがテスト用に表示するアラートの詳細については、このリファレンスを参照してください。
seo-title: アラート
title: アラート
uuid: 8f05b3c1-2427-4691-a88f-1de98f120a02
translation-type: tm+mt
source-git-commit: 762ff31ca4d5ed69d1b813589e419c51a40d5920

---


# アラート{#alerts}

Auditorがテスト用に表示するアラートの詳細については、このリファレンスを参照してください。

アラートは、認識する必要があるが、スコアには影響しない問題を示します。 これらは、お客様の実装に適用されない場合があるベストプラクティスの推奨事項です。

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
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud — 正しいコンバージョンタグが実装されている</b> </p> <p>重み：0 </p> </td> 
   <td colname="col2"> <p>正しいコンバージョンタグが使用されているかどうかを確認します。 </p> <p> <p>警告： 非推奨のTubeMogulコンバージョンタグを使用すると、データが失われる可能性があります。 </p> </p> </td> 
   <td colname="col3"> <p>コンバージョンピクセルを新しいAdvertising cloud画像のみのコンバージョンタグにアップグレードします。 </p> <p>これは、Advertising Cloud Launch Extensionを使用して、最も簡単に実行できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud — 正しいJSタグの使用</b> </p> <p>重み：0 </p> </td> 
   <td colname="col2"> <p>Advertising cloudでは、最新のJavaScriptタグを使用する必要があります。 </p> </td> 
   <td colname="col3"> <p>Advertising Cloud javaScriptを最新バージョンにアップグレードします。 廃止されたJavaScriptバージョンを使用すると、機能が失われる可能性があります。 </p> <p>これは、Advertising Cloud Launch Extensionを使用すると、より簡単に実行できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud — 画像のみのタグ</b> </p> <p>重み：0 </p> </td> 
   <td colname="col2"> <p>Advertising cloudの画像ピクセル形式は、次の推奨形式のいずれかに一致する必要があります。 </p> <p> 
     <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
      <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph"> http(s)://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph"> http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph"> http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
     </ul> </p> </td> 
   <td colname="col3"> <p>Advertising cloudのピクセルを新しいAdvertising cloudの画像のみのタグにアップグレードすると、Advertising cloudの全機能を確実に活用できます。 </p> <p>これは、Advertising Cloud Launch Extensionを使用して、最も簡単に実行できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud — セグメントピクセルのDSP同期が有効</b> </p> <p>重み：0 </p> </td> 
   <td colname="col2"> <p>TubeMogulセグメントピクセルにDSP同期設定が含まれているかどうかを確認し、その設定をピクセルに追加することをお勧めします。 </p> <p>DSP Syncing設定は、クエリ文字列パラメータを使用して決定されるので、 </p> <p>タグが(<span class="codeph"> "https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> OR <span class="codeph"> "http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> OR <span class="codeph"> "http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?"</span> </p> <p>ANDタグにはURLパラメータ「sid=」 <span class="codeph"> が含まれます)。</span> </p> <p>次に、URLパラメータ <span class="codeph"> "cs=0</span> "または<span class="codeph"> "cs=1"が存在するかどうかを確認し、オーディエンスの一致率を向上させるために、これらのピクセルに"</span> cs=1 <span class="codeph"></span> "を追加することをお勧めしません。 </p> </td> 
   <td colname="col3"> <p> DSP同期が発生するように、URLパラ <span class="codeph"> メーター「cs=1</span> 」をAdvertising cloudピクセルに追加します。これにより、オーディエンスの一致率が向上します。 </p> <p>これは、Advertising Cloud Launch Extensionを使用すると、最も簡単に実行できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      CAce6db25bc8c443409f0fcc5ac9d622c3 
    </draft-comment> <p><b>DTM - pageBottomコールバックの配置</b> </p> <p>重み：0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> 追加情報</a> </p> 
    <draft-comment>
      TEa9df69942f404055a64262889c8b21d3 
    </draft-comment> </td> 
   <td colname="col2"> <p>Dynamic Tag Managementには_satellite.pageBottom() <span class="codeph"> 関数が必要です</span> 。 DTMの正しい機能を確保するために、&lt;/body&gt; <span class="codeph"> タグの直前にインラインスクリプトを追加します</span> 。 </p> <p> <p>注意：&lt;body&gt;内の最後のタグはタグにす <i>る</i> ことをお勧め <span class="codeph"> します</span>。 &lt;body&gt;タグ内に見つかった場合、機能する可能性がありますが <span class="codeph"></span> 、ベストプラクティスではないので、機能が正しくない場合や、予期しない結果や望ましくない結果が生じる場合があります。 </p> </p> </td> 
   <td colname="col3"> <p>DTMの正しい機能を確保するために、&lt;/body&gt; <span class="codeph"> タグの直前にインラインスクリプトを追加します</span> 。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM — 自己ホスト型</b> </p> <p>重み：0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/deployment.html" format="html" scope="external"> 追加情報</a> </p> </td> 
   <td colname="col2"> <p> DTMライブラリは、AdobeのAkamaiインスタンス上の <span class="filepath"> assets.adobedtm.comでホストされています</span>。 </p> <p> DTMの読み込みには自己ホスト型アプローチが推奨されます。これは、キャッシュ制御によるWebサイトのパフォーマンスの制御、サードパーティスクリプトの依存関係の軽減、および公開プロセスの制御の強化を実現するためです。 DTMライブラリは、独自のWebホスティングまたはCDNを使用してホストおよび管理できます。 </p> </td> 
   <td colname="col3"> <p>ページにDTMを読み込む場合は、自己ホスト型が推奨される方法です。 Akamai CDN経由のDTMホスティングはほとんどの場合機能しますが、自己ホスティングはページのパフォーマンスを向上させます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Experience Cloud IDサービス — 1つのAdobeOrgのみを使用</b> </p> <p>重み：0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid_id_request.html" format="html" scope="external"> 追加情報</a> </p> </td> 
   <td colname="col2"> <p>通常のMCID実装では、1つのAdobeOrgを使用する必要があります。 </p> </td> 
   <td colname="col3"> <p>この実装に複数のAdobeOrg IDが存在することを検証します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch - pageBottomコールバックの配置</b> </p> <p>重み：0 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> 追加情報</a> </p> 
    <draft-comment>
      TE48c499b022f545c5bccc6f8bde169685 
    </draft-comment> </td> 
   <td colname="col2"> <p>同期的にデプロイされている場 <span class="codeph"> 合、Launch </span>には、ページの本文の最後にpageBottomコールバック関数を定義する必要があります。 </p> <p> <p>注意：&lt;body&gt;内の最後のタグはタグにす <i>る</i> ことをお勧め <span class="codeph"> します</span>。 &lt;body&gt;タグ内に見つかった場合、機能する可能性がありますが <span class="codeph"></span> 、ベストプラクティスではないので、機能が正しくない場合や、予期しない結果や望ましくない結果が生じる場合があります。 </p> </p> </td> 
   <td colname="col3"> <p>起動には、同期 <span class="codeph"> デプロイメントの場合は</span> _satellite.pageBottom()関数が必要です。 起動機能が正しく動作するように、&lt;/body&gt; <span class="codeph"> タグの直前にインラインスクリプトを追加します</span> 。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>起動 — 自己ホスト</b> </p> <p>重み：0 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Launchの概要</a> </p> <p><a href="https://docs.adobelaunch.com/client-side-information/asynchronous-deployment" format="https" scope="external"> 非同期展開の開始</a> </p> </td> 
   <td colname="col2"> <p>起動ライブラリは、AdobeのAkamaiインスタンス( <span class="filepath"> assets.adobedtm.com)でホストされています</span>。 </p> <p>「起動」の読み込みでは、自己ホスト型が推奨されるアプローチです。これは、キャッシュ制御によるWebサイトのパフォーマンスの制御、サードパーティスクリプトの依存関係の低減、および公開プロセスの制御の強化を実現するためです。 起動ライブラリは、独自のWebホスティングまたはCDNを使用してホストおよび管理できます。 </p> </td> 
   <td colname="col3"> <p>Akamai CDNを使用した「開始」ホスティングはほとんどの場合機能しますが、ページのパフォーマンスを向上させるための最初のステップとして自己ホストを実装することをお勧めします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>起動 — 非同期で導入する必要がある</b> </p> <p>重み：0 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> 追加情報</a> </p> </td> 
   <td colname="col2"> <p>最適なパフォーマンスを得るには、起動を非同期に展開する必要があります。 </p> </td> 
   <td colname="col3"> <p>非同期起動機能が正しく動作するように、インラインスクリプトにasyncパラメーターを含めます </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Target - mboxDefault内のコンテンツ</b> </p> <p>重み：0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> 追加情報</a> </p> </td> 
   <td colname="col2"> <p> at.jsを使用する場合は、mboxDefaultにコンテンツが存在する必要があります。 </p> </td> 
   <td colname="col3"> <p>コンテンツが使用可能であることを確認します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

