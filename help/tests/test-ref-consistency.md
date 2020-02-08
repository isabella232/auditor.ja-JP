---
description: このリファレンスでは、Auditorがタグの一貫性を確保するために実行するテストに関する詳細を説明します。
seo-description: このリファレンスでは、Auditorがタグの一貫性を確保するために実行するテストに関する詳細を説明します。
seo-title: タグの一貫性
title: タグの一貫性
uuid: 16271dd6-3587-4f33-92f8-54ec4a3d6469
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# タグの一貫性

このリファレンスでは、Auditorがタグの一貫性を確保するために実行するテストに関する詳細を説明します。

Auditorの整合性テストでは、スキャンされたすべてのページに一貫性がないかどうかを確認します。 これらは、正確なデータ収集を行うために、サイト上のすべてのページで同じ値または設定にする必要がある値です。

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
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics — 一貫したコードバージョン </b> </p> <p>重み：5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/choose-implementation-method.html" format="html" scope="external"> 追加情報</a> </p> </td> 
   <td colname="col2"> <p> 複数のバージョンのAnalyticsコードが見つかりました。 </p> </td> 
   <td colname="col3"> <p>Analyticsのすべてのインスタンスを現在のバージョンに置き換えます。 </p> </td> 
  </tr> 
 </tbody> 
</table>
