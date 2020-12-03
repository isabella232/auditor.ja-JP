---
description: このリファレンスでは、Adobe Experience Platform Auditor のテストで表示されるアラートの詳細を提供します。
seo-description: このリファレンスでは、Adobe Experience Platform Auditor のテストで表示されるアラートの詳細を提供します。
seo-title: アラート
title: アラート
uuid: 8f05b3c1-2427-4691-a88f-1de98f120a02
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# アラート {#alerts}

このリファレンスでは、Adobe Experience Platform Auditor のテストで表示されるアラートの詳細を提供します。

アラートは、認識する必要があるが、スコアには影響しない問題を示します。これらは、ベストプラクティスの推奨事項ですが、お客様の実装に適用されない場合があります。

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
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - 正しいコンバージョンタグが実装されている</b> </p> <p>重み付け：0 </p> </td> 
   <td colname="col2"> <p>正しいコンバージョンタグが使用されているかどうかを確認します。 </p> <p> <p>警告：非推奨の TubeMogul コンバージョンタグを使用すると、データが失われる可能性があります。 </p> </p> </td> 
   <td colname="col3"> <p>コンバージョンピクセルを新しい Advertising Cloud 画像専用コンバージョンタグにアップグレードします。 </p> <p>Experience Platform Launch 用 Advertising Cloud 拡張機能を使用すると、最も容易にこれを実施できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - 正しい JS タグを使用している</b> </p> <p>重み付け：0 </p> </td> 
   <td colname="col2"> <p>Advertising Cloud では、最新の JavaScript タグを使用する必要があります。 </p> </td> 
   <td colname="col3"> <p>Advertising Cloud JavaScript を最新バージョンにアップグレードします。非推奨の JavaScript バージョンを使用すると、機能が失われる可能性があります。 </p> <p>Platform Launch 用 Advertising Cloud 拡張機能を使用すると、より容易に実施できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - 画像専用タグ</b> </p> <p>重み付け：0 </p> </td> 
   <td colname="col2"> <p>Advertising Cloud の画像ピクセル形式は、次の推奨形式のいずれかと一致する必要があります。 </p> <p> 
     <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
      <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph">http(s)://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph">http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph">http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
     </ul> </p> </td> 
   <td colname="col3"> <p>Advertising Cloud の全機能を活用できるよう、Advertising Cloud のピクセルを新しい Advertising Cloud の画像専用タグにアップグレードします。 </p> <p>Platform Launch 用 Advertising Cloud 拡張機能を使用すると、最も容易にこれを実施できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - セグメントピクセルの DSP 同期が有効になっている</b> </p> <p>重み付け：0 </p> </td> 
   <td colname="col2"> <p>TubeMogul セグメントピクセルに DSP 同期設定が含まれているかどうかを確認し、その設定をピクセルに追加することをお勧めします。 </p> <p>DSP Syncing 設定は、クエリ文字列パラメーターを使用して決定されるので、 </p> <p>タグが<span class="codeph"> （"https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> または <span class="codeph"> "http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> または <span class="codeph"> "http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?"</span>、 </p> <p>およびタグに URL パラメーター <span class="codeph"> "sid=" が含まれる）</span>に対して実行される場合、 </p> <p>URL パラメーター <span class="codeph"> "cs=0"</span> または<span class="codeph"> "cs=1"</span> が存在するかどうかを確認します。存在しない場合は、オーディエンスの一致率を向上させるために、これらのピクセルに <span class="codeph"> "cs=1"</span> を追加することをお勧めします。 </p> </td> 
   <td colname="col3"> <p> DSP 同期を実行できるよう、URL パラメーター <span class="codeph"> "cs=1"</span> を Advertising Cloud ピクセルに追加します。これにより、オーディエンスの一致率が向上します。 </p> <p>Platform Launch 用 Advertising Cloud 拡張機能を使用すると、最も容易にこれを実施できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      CAce6db25bc8c443409f0fcc5ac9d622c3 
    --> <p><b>DTM - pageBottom コールバックの配置</b> </p> <p>重み付け：0 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external">追加情報</a> </p> 
    <!--
      TEa9df69942f404055a64262889c8b21d3 
    --> </td> 
   <td colname="col2"> <p>Dynamic Tag Management には、<span class="codeph">_satellite.pageBottom()</span> 関数が必要です。DTM が適切に機能するよう、<span class="codeph">&lt;/body&gt;</span> 終了タグの直前にインラインスクリプトを追加します。 </p> <p> <p>注意：ベストプラクティスは、このタグを<span class="codeph"> &lt;body&gt;</span> 内の<i>最後</i>のタグにすることです。<span class="codeph">&lt;body&gt;</span> タグ内にある場合でも、機能する可能性はありますが、ベストプラクティスではないので、正しく機能しない場合や、予期しない結果や望ましくない結果が生じる場合があります。 </p> </p> </td> 
   <td colname="col3"> <p>DTM が適切に機能するよう、<span class="codeph">&lt;/body&gt;</span> 終了タグの直前にインラインスクリプトを追加します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM - 自己ホストされている</b> </p> <p>重み付け：0 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/dtm/using/client-side/client-side-information.html" format="html" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p> DTM ライブラリは、アドビの Akamai インスタンス上（<span class="filepath">assets.adobedtm.com</span>）でホストされています。 </p> <p> DTM の読み込みには、キャッシュ制御を通じた Web サイトのパフォーマンスの制御、サードパーティスクリプトの依存関係の軽減、および公開プロセスの制御の向上を提供する自己ホスト型アプローチが推奨されます。DTM ライブラリは、お客様自身の Web ホスティングまたは CDN を使用してホストおよび管理できます。 </p> </td> 
   <td colname="col3"> <p>ページに DTM を読み込む場合は、自己ホスト型アプローチを推奨します。Akamai CDN 経由の DTM ホスティングはほとんどの場合において機能しますが、自己ホスティングを使用すると、ページのパフォーマンスが向上します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Experience Cloud ID サービス - 1 つの AdobeOrg のみを使用する</b> </p> <p>重み付け：0 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/id-service/using/intro/id-request.html" format="html" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p>通常の MCID 実装では、単一の AdobeOrg を使用する必要があります。 </p> </td> 
   <td colname="col3"> <p>この実装に複数の AdobeOrg ID が存在することを検証します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch - pageBottom コールバックの配置</b> </p> <p>重み付け：0 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/launch/using/intro/get-started/quick-start.html" format="https" scope="external">追加情報</a> </p> 
    <!--
      TE48c499b022f545c5bccc6f8bde169685 
    --> </td> 
   <td colname="col2"> <p>同時にデプロイした場合、Platform Launch では、ページ本文の最後で <span class="codeph">pageBottom</span> コールバック関数を定義する必要があります。 </p> <p> <p>注意：ベストプラクティスは、このタグを<span class="codeph"> &lt;body&gt;</span> 内の<i>最後</i>のタグにすることです。<span class="codeph">&lt;body&gt;</span> タグ内にある場合でも、機能する可能性はありますが、ベストプラクティスではないので、正しく機能しない場合や、予期しない結果や望ましくない結果が生じる場合があります。 </p> </p> </td> 
   <td colname="col3"> <p>Platform Launch で同期デプロイメントを実行するには、<span class="codeph">_satellite.pageBottom()</span> 関数が必要です。Platform Launch が適切に機能するよう、<span class="codeph">&lt;/body&gt;</span> 終了タグの直前にインラインスクリプトを追加します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - 自己ホストされている</b> </p> <p>重み付け：0 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/launch/using/intro/get-started/quick-start.html" format="https" scope="external">Adobe Experience Platform Launch の概要</a> </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/launch/using/reference/client-side-info/asynchronous-deployment.html" format="https" scope="external">Platform Launch の非同期デプロイメント</a> </p> </td> 
   <td colname="col2"> <p>Platform Launch ライブラリは、アドビの Akamai インスタンス上（<span class="filepath">assets.adobedtm.com</span>）でホストされています。 </p> <p>Platform Launch の読み込みには、キャッシュ制御を通じた Web サイトのパフォーマンスの制御、サードパーティスクリプトの依存関係の軽減、および公開プロセスの制御の向上を提供する自己ホスト型アプローチが推奨されます。Platform Launch ライブラリは、お客様自身の Web ホスティングまたは CDN を使用してホストおよび管理できます。 </p> </td> 
   <td colname="col3"> <p>Akamai CDN 経由の Platform Launch ホスティングはほとんどの場合において機能しますが、最初のステップとして自己ホスティングを使用すると、ページのパフォーマンスが向上します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - 非同期的にデプロイする必要がある</b> </p> <p>重み付け：0 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/launch/using/intro/get-started/quick-start.html" format="https" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p>最適なパフォーマンスを得るには、Platform Launch を非同期的にデプロイする必要があります。 </p> </td> 
   <td colname="col3"> <p>非同期的な Platform Launch 機能が正しく動作するように、インラインスクリプトに async パラメーターを含めます </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target - mboxDefault 内のコンテンツ</b> </p> <p>重み付け：0 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/target/using/implement-target/implementing-target.html" format="html" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p> at.js を使用する場合は、mboxDefault 内にコンテンツが存在する必要があります。 </p> </td> 
   <td colname="col3"> <p>コンテンツが使用可能であることを確認します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

