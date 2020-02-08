---
description: このリファレンスでは、Auditorがタグ配置に対して実行するテストに関する詳細を提供します。
seo-description: このリファレンスでは、Auditorがタグ配置に対して実行するテストに関する詳細を提供します。
seo-title: タグ配置
title: タグ配置
uuid: 91aa355b-7022-431c-9837-e108b5ce604d
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# タグ配置

このリファレンスでは、Auditorがタグ配置に対して実行するテストに関する詳細を提供します。

Auditorは、タグが存在するかどうか、およびタグがページコード内の適切な場所にあるかどうかを評価します。

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
   <td colname="col1"> <p><b>Analytics - DOMに読み込まれました</b> </p> <p>重み：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/" format="https" scope="external"> 追加情報</a> </p> </td> 
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
   <td colname="col2"> <p> DTMタグが検 <code> pageBottom</code> 出されませんでした。 </p> <p>これは、呼び出しが、と類似した結果になる文 <code> if</code> 内にある場合に発生する可能性がありま <code> if (false) {_satellite.pageBottom()}</code>す。 したがって、タグが存在し、正しく配置されている場合でも、タグは起動しない可能性があります。 </p> </td> 
   <td colname="col3"> <p>各ページにDTM呼び出し <code> pageBottom</code> をインストールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud IDサービス — コードの存在</b> </p> <p>重み：5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/overview.html" format="html" scope="external"> 追加情報</a> </p> </td> 
   <td colname="col2"> <p>Experience Cloud IDサービスコードが見つかりませんでした。 Experience Cloud ID(MCID)は、Experience cloudソリューションから最大限の価値を引き出すために強くお勧めし、Experience cloudソリューション全体のID管理にとって重要です。 </p> </td> 
   <td colname="col3"> <p> 最新バージョンのMCIDをインストールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud IDサービス — cookieの存在</b> </p> <p>重み：5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/implementation-guides.html" format="html" scope="external"> 追加情報</a> </p> </td> 
   <td colname="col2"> <p> AMCV_ <span class="codeph"> cookieが見つかり</span> ませんでした。 訪問者オブジェクトは、VisitorAPI.jsコードからインスタンス化 <span class="codeph"> する必要があり</span> ます。 </p> </td> 
   <td colname="col3"> <p> DTM実装の場合は、AdobeOrg IDがMCIDツールに正しく入力されていることを確認します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud IDサービス — MID値が存在する</b> </p> <p>重み：5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/cookies.html" format="html" scope="external"> 追加情報</a> </p> </td> 
   <td colname="col2"> <p> MID値がAMCV_cookieに見つかりま <span class="codeph"> せんでした</span> 。 </p> </td> 
   <td colname="col3"> <p>もう一度テストして、MCID APIの待ち時間を確認します。 問題が解決しない場合は、アドビカスタマーケアにお問い合わせください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b> 起動 — ライブラリが読み込まれました</b> </p> <p>重み：5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> 追加情報</a> </p> </td> 
   <td colname="col2"> <p> グローバル_satelliteオブジェクトがDOMに見つかりませんでした。 起動がインストールされていないか、実行に失敗しています。 </p> </td> 
   <td colname="col3"> <p>起動ライブラリがページに実装され、後続のスクリプトアクティビティによってブロックされていないことを確認します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>起動 — 複数の埋め込みスクリプトがない</b> </p> <p>重み：5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> 追加情報</a> </p> </td> 
   <td colname="col2"> <p>ページに複数の埋め込みスクリプトを読み込まないでください。 実稼働サイトでは、起動ライブラリを1つだけ読み込む必要があります。 </p> </td> 
   <td colname="col3"> <p>本番用ライブラリのみがページに読み込まれていることを確認します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>起動 — pageBottomコールバックが&lt;body&gt;に存在します</b> </p> <p>重み：5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> 追加情報</a> </p> </td> 
   <td colname="col2"> <p> _satellite. <span class="codeph"> pageBottom()コールバックが、Launchに必要なペ</span> ージの <span class="codeph"></span> &lt;body&gt;内で見つかりませんでした。 </p> <p>このテストは、 <span class="codeph"> pageBottom呼び出し </span>がページ上で見つからない場合、または&lt; <span class="codeph"></span> head&gt;タグ（または他の予期しない場所）にある場合に失敗します。 pageBottomが&lt;body&gt;タグ内で見つか <span class="codeph"> った場合</span> にのみ渡 <span class="codeph"> されます</span> 。 ページ上にない場合は、機能せず、他の2つのpageBottomテストも <span class="codeph"> 失敗します</span> 。 </p> </td> 
   <td colname="col3"> <p>起動機能が正しく動作するように、&lt;/body&gt; <span class="codeph"> タグの直前にインラインスクリプトを追加します</span> 。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch — 非同期でデプロイする場合、pageBottomコールバックは存在しない</b> </p> <p>重み：5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> 追加情報</a> </p> </td> 
   <td colname="col2"> <p>_satellite. <span class="codeph"> pageBottom()コールバックがページで見つかりましたが</span> 、Launchが非同期でデプロイされている場合は、このようにはなりません。 </p> </td> 
   <td colname="col3"> <p>_satellite.pageBottom()<span class="codeph"></span> スクリプトを削除して、正しい起動機能を有効にします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Target — コード配置</b> </p> <p>重み：5 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> 追加情報</a> </p> </td> 
   <td colname="col2"> <p>Targetは、DOMで定義する必要があります。 </p> </td> 
   <td colname="col3"> <p>最新バージョンのTarget(at.js)をインストールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> ターゲット — ライブラリが&lt;head&gt;に読み込まれました</b> </p> <p>重み：4 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> 追加情報</a> </p> </td> 
   <td colname="col2"> <p> Targetライブラリは、 <span class="codeph"> &lt;head&gt;タグに読み込まれます</span> 。 </p> </td> 
   <td colname="col3"> <p> Targetライブラリが&lt;head&gt;タグに読み込まれていることを確 <span class="codeph"> 認します</span> 。 </p> </td> 
  </tr> 
 </tbody> 
</table>
