---
description: Auditorが実行するテストの詳細については、このリファレンスを参照してください。
seo-description: Auditorが実行するテストの詳細については、このリファレンスを参照してください。
seo-title: テストリファレンス
title: テストリファレンス
uuid: f1d0769e-a2bd-4cec-acd1-146793644895
translation-type: tm+mt
source-git-commit: 0c116f699b697ad010ee074ac67159a49ec09ccd

---


# テストリファレンス{#test-reference}

Auditorが実行するテストの詳細については、このリファレンスを参照してください。

**現在のテストルーブリックバージョン：** 1.0.5

各テストは重み付けされます。 テストスコアは、割り当てられた重みと同じです。 体重5のテストに合格すると、5ポイントを受け取ります。

* 0:注意が必要な問題に関する警告を受け取りますが、スコアには影響しません。
* 1:最適化を推奨します。 データの正確性に影響を与えません。
* 2:このテストに失敗すると、Experience cloudの最新の機能および修正にアクセスできなくなります。
* 3:効率を確認し、実装がベストプラクティスに従っているかどうかをテストします。
* 4:失敗は、信頼性の低いデータを収集している可能性があることを意味します。
* 5:失敗は、データが失われる可能性があることを意味します。

テストは合格/不合格です。 テスト条件に対するコンプライアンスや非コンプライアンスをテストするので、部分的なコンプライアンスに対する部分的なスコアはありません。 例えば、テストでアドビソリューションの最新バージョンを確認し、1つ遅れているバージョンがある場合、以前のバージョンが5つである場合と同じスコアが得られます。 最新バージョンにはパフォーマンスの改善とバグの修正が含まれているので、最新バージョンを使用することをお勧めします。

レベル 4 または 5 の結果を修正することを&#x200B;**強くお勧めします**。

レベル 1 から 3 の結果を修正することを&#x200B;**お勧めします**。

## AuditorはどのAdobeテクノロジーを採用していますか。 {#section-52833b71c05448aaae508e6070a387f5}

* Advertising Cloud DSP
* Advertising cloud検索
* Analytics
* DTM
* Experience Cloud IDサービス（旧称Marketing Cloud IDサービス）
* Target

次のアドビソリューションは、現在、テストルーブラリックには含まれていません。 これらのソリューションのサポートは、今後の更新に備えて計画されています。

* Advertising Cloud Creative
* Audience Manager
* Campaign
* Launch

## テストカテゴリ {#section-630181db21ef4eec9ce6a13a0482bb55}

このテストリファレンスでは、テストを次のカテゴリに分けています。