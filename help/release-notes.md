---
description: Adobe Experience Platform Auditor リリースノート
seo-description: Adobe Experience Platform Auditor Release Notes
seo-title: Adobe Experience Platform Auditor release notes
title: Adobe Experience Platform Auditor リリースノート
uuid: 2e1eb2de-f162-45af-a9b0-15dbdac5531d
exl-id: 7c8c55ed-6211-446b-9182-2e9b49dd117d
source-git-commit: 286a857b2ff08345499edca2e0eb6b35ecf02332
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 100%

---

# Adobe Experience Platform Auditor リリースノート{#auditor-release-notes}

## 2019年2月05日（PT） {#section-f73142fd7c85492a806c7fc19a33a525}

**機能強化**

1 回にスキャンできる最大ページ数が 100 から 500 に増えました。

>[!NOTE]
>
>この増加に伴い、スキャンの完了に要する時間が長くなります。500 ページのスキャンを完了するまでに最大 48 時間かかる場合があります。

## 2018年11月2日 {#section-542a32872efa445dab688285bf87964b}

**新機能**

現在実行中の監査を Platform Auditor ページやカード表示から、または新しい監査の作成時にキャンセルできるようになりました。

## 2018年6月4日 {#section-0747f36a1f4f46638b2c6bf182de9864}

**新機能**

* 完了した監査をリスト表示、タイル表示、監査の詳細表示から削除できるようになりました。
* 監査設定が XLSX ダウンロードの一部として含まれるようになりました
* PDF レポートにルーブリックバージョンの追跡を追加しました
* 監査で単一ページのみをスキャンする場合のメッセージングを改善しました
* Excel のダウンロードページから完全なレポートを閲覧するためのリンクを追加しました

**バグの修正**

ユーザーが IMS 組織の管理者である場合は、シェルに「管理」リンクが表示されていることを確認します

## 2018年5月17日（PT） {#section-b72792e4e6ad4bd9910f48767704e204}

**新機能**

* 新しい監査設定に正規表現のテストと検証を追加しました

   正規表現の値は入力時に検証されるので、Include フィルターまたは Exclude フィルターをさらに容易に入力することができます。
* 監査レポートを PDF 形式でダウンロードする機能を追加しました。
* 完了した監査の監査設定に、テストルーブリックのバージョン番号が追加されました。

## 初回リリース（2018 年 3 月 23 日（PT）） {#section-dcc4cd58353b48369d1e994a05a71a29}

>[!NOTE]
>
>Platform Auditor へのアクセスは、ローリング方式で許可されます。2018 年 4 月末までに、すべてのお客様がアクセスできるようになります。

 Platform Auditor は、Adobe Experience Cloud の実装に関する評価をおこないます。Platform Auditor は、アドビ製品単体で、または複数のアドビ製品をまとめてさらに活用できるよう支援します。

Platform Auditor を使用すると、次のことができます。

* **スキャン**：アドビのテクノロジー用に、100 の Web ページを一度にスキャンします。必要に応じて、ページを含めたり除外したりするには、フィルター詳細設定を使用します。一度に 1 件の監査を実行できます。回数に制限はありません。

* **理解**：タグの有無、設定、一貫性に基づいてアドビの実装を評価するレポートを受け取ります。

* **改善**：アドビへの投資を最大限活用できるよう、実装をアップグレードする方法についてのレコメンデーションを提供します。Platform Auditor は、実装をどのように改善できるかを指摘し、問題が見つかった Web ページや修正方法に関するガイダンスを正確に示します。

お客様が自分たちの実装をトラブルシューティングおよび修正できるようにすることで、Platform Auditor は実装タグ、ひいてはデータをより細かく制御できるようにします。これにより、実装タグに関する質問をカスタマーケアに問い合わせる必要が減ります。

Platform Auditor は、Adobe と ObservePoint によって共同で開発されました。Platform Auditor ユーザーは、追加費用なしで、ObservePoint の制限付き機能を使用できます。Platform Auditor を使用するには、ObservePoint からのコミュニケーションをオプトインする必要があります。
