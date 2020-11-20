---
description: このリファレンスでは、Adobe Experience Platform Auditor がタグの有無を確認するために実行するテストの詳細を説明します。
seo-description: このリファレンスでは、Adobe Experience Platform Auditor がタグの有無を確認するために実行するテストの詳細を説明します。
seo-title: テストリファレンス
title: テストリファレンス
uuid: f1d0769e-a2bd-4cec-acd1-146793644895
translation-type: ht
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: ht
source-wordcount: '293'
ht-degree: 100%

---


# テストリファレンス {#test-reference}

このリファレンスでは、Adobe Experience Platform Auditor がタグの有無を確認するために実行するテストの詳細を説明します。

**現在のテストルーブリックバージョン：** 1.0.5

各テストは重み付けされます。テストスコアは、割り当てられた重み付けと同じになります。重み付けが 5 のテストに合格すると、5 ポイントを獲得します。

* 0：認識する必要があるが、スコアには影響しない問題を警告します。
* 1：最適化を推奨します。データの正確性には影響しません。
* 2：このテストで不合格となると、Experience Cloud の最新の機能や修正にアクセスできなくなります。
* 3：効率をテストするとともに、実装がベストプラクティスに従っているかどうかをテストします。
* 4：不合格の場合、信頼できないデータを収集する可能性があります。
* 5：不合格の場合、データが失われる可能性があります。

テストは合格または不合格のいずれかになります。テスト条件に対する準拠または違反をテストするので、一部準拠している場合でも部分的にスコアが提供されるわけではありません。例えば、テストでアドビソリューションの最新バージョンを確認し、1 つ前のバージョンを使用していることがわかった場合、5 つ前のバージョンを使用している場合と同じスコアが付けられます。最新バージョンにはパフォーマンスの改善とバグの修正が含まれているので、最新バージョンを使用することをお勧めします。

レベル 4 または 5 の結果を修正することを&#x200B;**強くお勧めします**。

レベル 1 から 3 の結果を修正することを&#x200B;**お勧めします**。

## Platform Auditor はどのアドビテクノロジーを採用していますか。 {#section-52833b71c05448aaae508e6070a387f5}

* Advertising Cloud DSP
* Advertising Cloud 検索
* Analytics
* DTM
* Experience Cloud ID サービス（旧称 Marketing Cloud ID サービス）
* Target

次のアドビソリューションは現在、テストルーブリックには含まれていません。これらのソリューションのサポートは、今後のアップデートで予定されています。

* Advertising Cloud Creative
* Audience Manager
* Campaign
* Adobe Experience Platform Launch
