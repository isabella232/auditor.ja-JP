---
description: Adobe Experience Platform監査人に新しい監査を作成
seo-description: Adobe Experience Platform監査人に新しい監査を作成
seo-title: Adobe Experience Platform監査人に新しい監査を作成
title: Adobe Experience Platform監査人に新しい監査を作成
uuid: bd6798bb-3fab-4091-9e07-d3d1e5fdd087
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 73%

---


# 新しい監査の作成 {#create-a-new-audit}

>[!NOTE]
>
>ユーザーは、一度に 1 件のみを監査を実行できます。実行中の監査と同じ設定で監査を開始しようとすると、エラーが発生します。現在実行中の監査をキャンセルして新しい監査を作成する場合は、エラーメッセージ内のリンクを使用できます。

希望する場合は、ページ下部のリンクを使用して、ObservePoint を使用して無償の完全機能体験版アカウントにアクセスします。

1. Auditor リストで、 **[!UICONTROL New Audit]** をクリックします。

   [!DNL New Audit] 画面が表示されます。

   ![](assets/config.png)

1. （必須）監査に名前を付けます。

   名前は 250 文字以内にする必要があります。
1. （必須）開始 URL を指定します。

   開始 URL を指定する場合は、プロトコルが必要です。開始 URL は、監査がクロールを開始するページです。開始した後、Adobe Experience Platform監査人は、開始URLから始まるリンクに従って、最大500ページまでクロールします。 詳しくは、[Include フィルターと Exclude フィルター](../create-audit/filters.md)を参照してください。開始 URL は 250 文字以内にする必要があります。

   >[!NOTE]
   >
   >500 ページのスキャンを完了するまでに最大 48 時間かかる場合があります。

1. この監査に関する通知用に、1 つ以上の電子メールアドレスを指定します。

   複数のアドレスをコンマで区切って指定できます。要求者にはデフォルトで通知が送信されます。電子メールアドレスは、リアルタイムで検証されます。無効なアドレスを入力すると、画面に通知が表示されます。

   各電子メールの長さは、ドメインの末尾（例：.com）を含めて 250 文字以下に制限されます。

1. Specify [!UICONTROL Include Filters].

   このフィールドには、正確な URL、URL の一部または正規表現を含めることができます。このフィールドは、すべての URL で一致させる条件に使用します。Any crawled URLs that do not match the [!UICONTROL Include Filter] criteria are not included in the audit results.

   監査でスキャンするディレクトリを入力できます。また、1 つのドメインで監査を開始し、別のドメインで監査を終了する必要がある、クロスドメイン監査や自己参照監査を実行することもできます。これをおこなうには、トラバースするドメインを入力します。複雑な URL パターンの場合は、正規表現を使用します。

   >[!NOTE]
   >
   >フィルターーにページを含めても、開始URLに接続されていない場合、またはPlatform Auditorがそのページに到達する前に500ページをスキャンする場合、ページはスキャンされず、テスト結果に含まれません。

   Include フィルターは 1 行につき 1,000 文字までに制限されます。

   詳しくは、[Include リスト](../create-audit/filters.md)を参照してください。
1. Exclude フィルターを指定します。

   The [!UICONTROL Exclude List] prevents URLs from being audited. Use exact URLs, partial URLs, or regular expressions, just as you would in the [!UICONTROL Include List].

   一般的な例として、監査にユーザーセッションがある場合にログアウトリンクを除外する場合があります（例：`/logout`。文字列 `/logout` を含む任意の URL を示します）。

   Exclude フィルターは 1 行につき 1,000 文字までに制限されます。

   詳しくは、[Exclude リスト](../create-audit/filters.md)を参照してください。
1. （オプション）必要に応じて、Include フィルターと Exclude フィルター、および URL をテストできます。

   フィルターと URL を入力し、 **[!UICONTROL Apply]** をクリックしてテストを実行します。

   ![](assets/test-advanced-filters.png)

1. **[!UICONTROL Run Report]** をクリックします。
