---
description: このリファレンスでは、Adobe Experience Platform Auditor がタグの整合性を確認するために実行するテストの詳細を説明します。
seo-description: このリファレンスでは、Adobe Experience Platform Auditor がタグの整合性を確認するために実行するテストの詳細を説明します。
seo-title: タグの整合性
title: タグの整合性
uuid: 16271dd6-3587-4f33-92f8-54ec4a3d6469
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 100%

---


# タグの整合性

このリファレンスでは、Adobe Experience Platform Auditor がタグの整合性を確認するために実行するテストの詳細を説明します。

Platform Auditor の整合性テストでは、スキャンされたすべてのページで矛盾を探します。これらの値や設定は、正確なデータ収集をおこなうために、サイト上のすべてのページで同じにする必要があります。

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
    <!--
      1.0.1 
    --> <p><b>Analytics - コードバージョンが一貫している</b> </p> <p>重み付け：5 </p> <p><a href="https://docs.adobe.com/content/help/ja-JP/analytics/implementation/home.html" format="html" scope="external">追加情報</a> </p> </td> 
   <td colname="col2"> <p> 複数のバージョンの Analytics コードが見つかりました。 </p> </td> 
   <td colname="col3"> <p>Analytics のすべてのインスタンスを最新のバージョンに置き換えてください。 </p> </td> 
  </tr> 
 </tbody> 
</table>
