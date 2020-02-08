---
description: Auditorが設定で実行するテストの詳細については、このリファレンスを参照してください。
seo-description: Auditorが設定で実行するテストの詳細については、このリファレンスを参照してください。
seo-title: 設定
title: 設定
uuid: d40d815c-edfe-48b9-921f-cea1b0b54a0a
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# 設定

Auditorが設定で実行するテストの詳細については、このリファレンスを参照してください。

構成テストでは、実装内の特定の設定、値、または競合の可能性をスキャンします。 Auditorは、タグを他のルールおよび推奨ベストプラクティスと比較して評価します。

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
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud — コンバージョン名に使用できる文字は英数字のみです</b> </p> <p>重み：3 </p> </td> 
   <td colname="col2"> <p>ev_conversion_property_nameパ <span class="codeph"> ラメーターには、「</span> ev_transid<span class="codeph"> 」パラメーター以外の数値と10進数のみを含める必要があります(</span>ev_transid <span class="codeph"></span> 値には、テキスト値または数値を含めることができます) </p> <p>ev_で始まるURLパ <span class="codeph"> ラメーターを含むeveresttech.net</span> pixelを探 <span class="codeph"> します</span>。 </p> <p>例： </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47 </span> </p> </td> 
   <td colname="col3"> <p> トランザクションプロパティのパラメーターには、数値と10進数値のみを含めてください。 </p> <p> <p>警告： その他の値の型は、データの損失の原因となる場合があります。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud — コンバージョン名にURLセーフ文字を使用する</b> </p> <p>重み：3 </p> </td> 
   <td colname="col2"> <p> コンバージョンプロパティ名にアンパサンドや疑問符を含めることはできません。 </p> <p> 例： </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>トランザクションプロパティのパラメーターに、エンコードされていないアンパサンドや疑問符が含まれていないことを確認します。 これらはURL形式を壊します。 </p> <p> <p>警告：エンコードされていないアンパサンドまたは疑問符を含むプロパティパラメーター(例：ev_formComplete?=1 <span class="codeph"> またはev_formComplete&amp;Submit=1</span> ) <span class="codeph"></span>の場合、データが失われる可能性があります。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud — トランザクションIDが正しく実装されている</b> </p> <p>重み：1 </p> </td> 
   <td colname="col2"> <p> プロパティ名 <span class="codeph"> ev_transid=</span> を空にすることはできません。 </p> <p>例： </p> <p> <span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>プロパティ名 <span class="codeph"> ev_transid=</span> のままにして値(<span class="codeph"> ev_transid=</span>)を指定しないでください。 値を指定せずにこのままにしておくと、トランザクションデータが失われる可能性があります。 ev_transid=に値を割り当 <span class="codeph"> てるか、ピクセルからパ</span> ラメータを削除します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - DOMでインスタンス化</b> </p> <p>重み：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/impl_testing.html" format="html" scope="external"> 追加情報</a> </p> </td> 
   <td colname="col2"> <p> Adobe Analyticsコードがインストールされていないか、実行に失敗しています。 解析コードが見つからない場合は0を返します。 </p> </td> 
   <td colname="col3"> <p>Analyticsタグがページに実装され、後続のスクリプトアクティビティによってブロックされていないことを確認します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics — インスタンス化は1回のみ</b> </p> <p>重み：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/" format="https" scope="external"> 追加情報</a> </p> </td> 
   <td colname="col2"> <p> Adobe Analyticsコードがページで複数回検出されました。. 解析コードが見つからない場合は0を返します。 </p> </td> 
   <td colname="col3"> <p>ページにAnalyticsタグが1つだけ存在することを確認します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics — 最新バージョン</b> </p> <p>重み：3 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/appmeasurement/release" format="https" scope="external"> 追加情報</a> </p> </td> 
   <td colname="col2"> <p> ページでAnalyticsコードライブラリの最新バージョンが実行されていません。 Experience cloudテクノロジーを強化するコードライブラリは、パフォーマンスの向上を活用し、最新の機能を提供するために、常に更新およびツイークされています。 解析コードが見つからない場合は0を返します。 </p> </td> 
   <td colname="col3"> <p>Analyticsライブラリの最新バージョンをインストールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - DOM準備完了後にサードパーティタグが非同期に読み込まれる</b> </p> <p>重み：3 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/load_order.html" format="html" scope="external"> 追加情報</a> </p> </td> 
   <td colname="col2"> <p>ユーザーの使い勝手が良い場合と正確なデータを収集する場合のバランスをとるには、サードパーティタグをDOM ready時にトリガーする必要があります。 これにより、サイトの機能に影響を与えずに、これらのトラッキングスクリプトを確実に実行できます。 </p> </td> 
   <td colname="col3"> <p>サードパーティのピクセルを実行するすべてのルールをDOM readyで実行するように調整して、この問題を解決します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud IDサービス — 最新バージョン</b> </p> <p>重み：2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/macid.html" format="html" scope="external"> 追加情報</a> </p> </td> 
   <td colname="col2"> <p> ページで、最新バージョンの訪問者IDサービスコードライブラリvisitor <span class="codeph"> API.jsが実行されていません</span>。 Experience cloudテクノロジーを強化するコードライブラリは、パフォーマンスの向上を活用し、最新の機能を提供するために、常に更新およびツイークされています。 </p> </td> 
   <td colname="col3"> <p>訪問者IDサービスライブラリの最新バージョンをインストールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>起動 — 最新バージョン</b> </p> <p>重み：2 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> 追加情報</a> </p> </td> 
   <td colname="col2"> <p>これらのページでは、最新バージョンの起動コードライブラリ（タービン）が実行されていません。 Experience cloudテクノロジーを強化するコードライブラリは、パフォーマンスの向上を活用し、最新の機能を提供するために、常に更新およびツイークされています。 </p> </td> 
   <td colname="col3"> <p> 起動ライブラリを再構築して公開し、起動ライブラリを更新します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target — 最新バージョン</b> </p> <p>重み：2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/dtm/update-target-tool.html" format="html" scope="external"> 追加情報</a> </p> </td> 
   <td colname="col2"> <p> ページでTargetコードライブラリの最新バージョンが実行されていません。 Experience cloudテクノロジーを強化するコードライブラリは、パフォーマンスの向上を活用し、最新の機能を提供するために、常に更新およびツイークされています。 </p> </td> 
   <td colname="col3"> <p>Targetライブラリの最新バージョンをインストールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target - mboxDefaultはmboxCreateの前に配置 </b> </p> <p>重み：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> 追加情報</a> </p> </td> 
   <td colname="col2"> <p>mboxCreateの適切な使用方法は <span class="codeph"> 次のように</span> なります。 </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;! — 顧客コンテンツ —&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
   <td colname="col3"> <p>mboxCreate()を呼び出す前に、必ず <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;/div&gt;</span> タグを含めて <span class="codeph"> ください</span>。 at.jsは追加しません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>ターゲット — 有効なDOCTYPE</b> </p> <p>重み：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> 追加情報</a> </p> </td> 
   <td colname="col2"> <p> 無効なDOCTYPEが検出されました。 このシナリオでは、mboxは起動されません。 </p> <p>at.jsの場合、DOCTYPEは標準モードである必要があります。そうしないと、Targetは動作しません。 </p> </td> 
   <td colname="col3"> <p>ページ上のDOCTYPEを更新します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

