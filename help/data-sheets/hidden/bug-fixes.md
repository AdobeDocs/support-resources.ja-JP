---
title: バグの修正（非表示）
description: 内部テスト用のテストページ
hide: true
hidefromtoc: true
exl-id: e6270f95-3550-4e35-ad4c-760584bb9b5d
source-git-commit: 0cefcf5bb4a021593a6bbe44eed0ad83e8bd259f
workflow-type: tm+mt
source-wordcount: '1926'
ht-degree: 28%

---

# バグの修正

## 自動化試験

これらのバグはすべて修正する必要があります。

## UGP-10866 リンクがシェードボックスで太字にならない

>[!BEGINSHADEBOX]

**目次**

* [AI アシスタントの基本を学ぶ](note-test.md)
* **[AI アシスタントを使用したメールの生成](syntax-style-guide.md)**
* [AI アシスタントを使用した SMS の生成](test-page.md)
* [AI アシスタントによるプッシュ生成](tables.md)
* [AI アシスタントを使用したコンテンツ実験](test-redirection.md)

>[!ENDSHADEBOX]

シェードボックスなし

**目次**

* [AI アシスタントの基本を学ぶ](note-test.md)
* **[AI アシスタントを使用したメールの生成](syntax-style-guide.md)**
* [AI アシスタントを使用した SMS の生成](test-page.md)
* [AI アシスタントによるプッシュ生成](tables.md)
* [AI アシスタントを使用したコンテンツ実験](test-redirection.md)


## UGP-10584 インラインバッジが機能しない

これらのバッジは、箇条書き項目と同じ行にある必要があります。

* [[!DNL Mixpanel]](note-test.md) [!BADGE 備考]{type=Informative}
* [[!DNL Pendo]](tables.md) [!BADGE テーブル]{type=Positive}
* [[!DNL RainFocus]](syntax-style-guide.md) [!BADGE 構文スタイルガイド]{type=Positive}

## UGP-10560 – 折りたたみ可能なセクションのバッジ

+++ 以前のバージョン

### V1.16 リリース

_2023 年 2 月 13 日（Pt）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) 製品ビデオが Catalog Service API でサポートされるようになりました。
![修正](assets/package.png) 固定価格のバンドル製品がサポートされるようになりました。
![修正](assets/package.png) 在庫切れのオプションが PDP ウィジェットに表示されるようになりました。

#### 既知の制限事項

これらの機能は、まだサポートされていません。

* 動的属性ペイロードの最大サイズは 9 MB です。
* グループ製品価格。 簡単な製品価格で計算できます。
* 画像配列では、最初の画像にのみ役割が含まれます。

API メッシュとコア GraphQL API を使用すると、次の制限を解決できます。

* 広告の最低価格
* [階層の価格](https://www.adobe.com)

### V1.13 リリース

_2023年10月12日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) カタログサービスは、 `inStock` 製品バリアントのフラグ。
![新規](assets/package.png) `urlKey` および `externalId` GraphQL スキーマに追加されました。
![新規](assets/package.png) ダウンロード可能な製品とギフトカードがサポートされるようになりました。

### V1.12 リリース

_2023年9月19日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](https://www.adobe.com).
![修正](assets/package.png) このリリースには、サービス側のバグ修正と改善が含まれています。

### V1.11 リリース

_2023年7月18日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) カタログサービスで、がサポートされるようになりました [`recommendations`](https://developer.adobe.com/commerce/services/graphql/recommendations/recommendations/) 製品RecommendationsのGraphQL クエリ。

### V1.10 リリース

_2023年6月27日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) Catalog Service API で「関連製品」がサポートされるようになりました。

### V1.7 リリース

_2023年4月12日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) 削除された製品のバリエーションをカタログサービスでクリーンアップできるようになりました。
![修正](assets/package.png) インフラストラクチャの拡張性とパフォーマンスの向上。

### V1.6 リリース

_2023年3月28日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) にスウォッチを追加しました [`products`](https://developer.adobe.com/commerce/services/graphql/catalog-service/products/) クエリ。
![新規](https://www.adobe.com).

### V1.5 リリース

_2023年3月6日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) 追加済み [`categories`](https://developer.adobe.com/commerce/services/graphql/schema/catalog-service/categories/) GraphQL機能。
![修正](assets/package.png) パフォーマンスと API のスケーラビリティの向上。

### V1.4 リリース

_2023年2月7日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) インストール手順を簡素化するためのカタログサービスメタパッケージが公開されました。
![修正](assets/package.png) API のスケーラビリティとパフォーマンスの向上。

### V1.3 リリース

_2023年1月17日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) オンボーディングエクスペリエンスを簡素化し、改善しました。
![新規](assets/package.png) 新しい顧客サンドボックスエンドポイントは、実稼動前のテストで使用できます。
![新規](assets/package.png) 仮想製品のサポートが追加されました。
![修正](assets/package.png) API のスケーラビリティとパフォーマンスの向上。

### V1.1 リリース

_2022年11月18日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) カタログサービスでAdobeがサポートされるようになりました [API メッシュ](https://developer.adobe.com/graphql-mesh-gateway/).
![修正](assets/package.png) API のスケーラビリティと全体的なパフォーマンスの向上。

### V1.0 リリース

_2022年10月4日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) バンドルされた製品とグループ化された製品をサポートするようになりました。
![新規](assets/package.png) B2B 表示の上書きを追加しました。 製品が検索できるようになり、特定の顧客グループのために買い物かごに追加できるようになりました。
![修正](assets/package.png) サービスの安定性とパフォーマンスが向上しました。

### 0.3 リリース – ベータ版+

_2022年9月12日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) バリアント型の画像のサポート：選択したオプションに基づいて製品画像が返されます
![新規](assets/package.png) 価格サポートの役割：特定の顧客グループのメンバーのみが製品の価格を表示できるようにします
![修正](assets/package.png) サービスの安定性とパフォーマンスの向上
![新規](assets/package.png) 製品がカタログから削除されると、更新が受信されます

### ベータ版リリース

_2022年8月9日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) この `products` および `refineProduct` クエリは、次のデータを返します。

* 事前定義済み（システム）製品属性。
* 製品の動的属性および役割別のフィルター（製品の表示ページ/製品のリストページ）。
* 製品オプション。
* 製品画像を役割（PDP/PLP）別にフィルタリングする方法を説明します。
* シンプルな製品の特定の価格と設定可能な製品の価格範囲。
* 顧客グループの価格と価格範囲。 顧客グループを持たない買い物客に対しては、フォールバックのデフォルト価格が返されます。
* B2B 顧客固有の価格を使用する製品タイプ。

+++

## [!BADGE 非推奨（廃止予定）]{type=negative}

上記の見出しを参照してください。 そして次のもの。

## 自動アクティブ化のテスト

金曜日の午後にこれを追加しましたが、「今すぐ公開」はクリックしませんでした。

### [!BADGE Beta]{type=Informative}

Bob

## UGP-10565 - テキストハイライト表示

前のテキスト `<div class="preview">`

<div class="preview">

### Workfront ネイティブフィールドを追加

カスタムフォームにWorkfront ネイティブフィールドを追加できます。 カスタムフォームがオブジェクトに添付されると、フィールドはオブジェクトデータから入力されます。 例えば、プロジェクトに添付されたカスタムフォームの「説明」フィールドは、プロジェクトの説明を取り込みます。 （データが利用できない場合、フィールドには「該当なし」と表示される場合があります）。

1. 画面の左側で、次を見つけます **ネイティブフィールド** キャンバス上のセクションにドラッグします。
1. 画面の右側で、カスタムフィールドのオプションを設定します。

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">ラベル</td> 
      <td> <p>（必須） フィールドの上に表示する説明ラベルを入力します。 ラベルはいつでも変更できます。</p> <p><b>重要</b>：このラベルでは特殊文字を使用しないでください。 レポートに正しく表示されません。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">名前</td> 
      <td> <p>（必須）この名前によって、システムによるフィールドの識別方法が決まります。</p><p> 初めてフィールドを設定する際にラベルを入力すると、それに一致するように「名前」フィールドが自動的に設定されます。 ただし、「ラベル」フィールドと「名前」フィールドは同期されません。これにより、システムに表示される名前を変更しなくても、ユーザーに表示されるラベルを自由に変更できます。</p>
      <p><b>重要</b>:
      <ul> 
      <li>これは可能ですが、自分や他のユーザーがWorkfrontでカスタムフォームを使用し始めた後は、この名前を変更しないことをお勧めします。 これを行うと、Workfrontの他の領域で参照される可能性のあるフィールドが認識されなくなります。</p> </li>
      <li> <p>各フィールド名は、組織のWorkfront インスタンスで一意である必要があります。 この方法では、既に作成したカスタムフォームを別のカスタムフォームで再利用できます。</p> </li>
      <li><p>Workfrontの様々な領域でフィールドを使用する際にエラーが発生しないよう、カスタムフィールド名にはピリオド/ドットを使用しないことをお勧めします。</p></td> 
     </tr> 
     <tr> 
      <td role="rowheader">手順</td> 
      <td> <p>フィールドの追加情報を入力します。 ユーザーがカスタムフォームに入力する際は、疑問符アイコンの上にマウスポインターを置くと、ここに入力した情報を含むツールヒントが表示されます。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">参照フィールド</td> 
      <td><p>（必須） Workfront ネイティブフィールドを選択します。<p><p>フォームのオブジェクト用のネイティブフィールドのみを使用できます。 例えば、フォームデザイナーの上部にある「オブジェクトタイプ」リストに「プロジェクト」と表示されている場合は、プロジェクトのネイティブフィールドを選択できますが、タスクに固有のフィールドは選択できません。</p></td>
     </tr>
     <tr> 
      <td role="rowheader">サイズ</td> 
      <td>（オプション）必要に応じてフィールドの表示サイズを変更します。</td> 
     </tr> 
    </tbody> 
   </table>

1. 変更を保存するには、をクリックします **適用** 別のセクションに移動して、フォームの作成を続行します。

   または

   「**保存して閉じる**」をクリックします。

</div>

ハイライト表示後のテキスト

## UGP-10566 - HTMLテーブルで、リンクテキストが通常のテキストよりも小さい

UGP-9780 も参照。

<table style="table-layout:auto"> 
<tbody> 
<tr>
<td>入力先</td>
<td>説明</td>
<td>利用可能 </td>
</tr>
<tr> 
    <td role="rowheader">ラベル</td> 
    <td> <p>（必須） カスタムフィールドの上に表示する説明ラベルを入力します。 ラベルはいつでも変更できます。 詳しくは、を参照してください <a href="https://www.adobe.com" class="MCXref xref">カスタムフィールドをカスタムフォームに追加する</a> この記事の内容です。</p> <p><b>重要</b>：このラベルでは特殊文字を使用しないでください。 レポートに正しく表示されません。</p> </td> 
    <td>
    <ul>
    <li>ラジオボタン。 詳しくは、を参照してください <a href="https://www.adobe.com">カスタムフィールドをカスタムフォームに追加する</a> この記事の内容です。 （クラスなし）</li>
    <li>チェックボックスグループ</li>
    <li>ドロップダウン</li>
    </ul></td>
</tr> 
</tbody> 
</table>

## UGP-9176 – 古いバグ

「span」タグは、メモ（およびリスト）ではうまく機能しません

新しいコメント機能で使用できる機能とオブジェクトについて詳しくは、を参照してください。 [新しいコメント機能](note-test.md).

1. 返信を追加するオブジェクトに移動します。
1. クリック **更新**&#x200B;を選択し、 **コメント** オブジェクトの Tab キーを押して、返信先のコメントまたは返信を検索します

   または

   <span class="preview">「」をクリックします **すべて** tab キーを押してから、 **コメントで返信** 「コメント」タブでコメントを開いて返信します。 「すべて」タブでは返信できません。</span>

1. （オプション）以前の更新のテキストを返信に含めるには、 **詳細** 返信するコメントの右上隅にあるメニューをクリックし、 **見積の返信**. 前の更新のテキストが入力領域に表示され、灰色の縦線でマークされます。
1. クリック **返信**.

   ![](assets/package.png)

   の下部に、会話に積極的に参加しているユーザーを表示できます **返信を追加…** ボックスを使用すると、関係がなくなったものをさらに追加したり、削除したりできます。 これらのユーザーは、オブジェクトを購読しているすべてのユーザーと共に、オブジェクトに対して更新または返信が行われるたびに通知を受け取ります。 さらにユーザーにタグを付けて、返信に含めることもできます。  さらに人のユーザーにタグを付けるには、以下を参照してください [の更新で他のユーザーにタグ付け](note-test.md).

   >[!TIP]
   >
   >   既存の返信に追加の返信を追加するには、フィールドに **返信を追加…** ボックスまたはクリック **返信** 元のコメント。 返信がスレッドの最後に追加されます。

1. 返信の入力を開始し、リッチテキストツールバーから追加のオプションを使用します。 リッチテキストやその他の更新機能の使用について詳しくは、を参照してください。 [作業の更新](note-test.md).

1. クリック **Submit** 返信を保存します。

1. （任意） **詳細** 返信を管理するその他のオプションについては、返信するコメントの右上隅にあるメニューを参照してください。 詳しくは、を参照してください [作業の更新](note-test.md).


## UGP-10614 – 画像を含む問題テーブル

と思う `{width="20"}` パラメーターが原因で、テーブルに問題が発生しています。

## Expert と Ultimate のサクセスプランの比較

|  | Expert サクセスプラン | Ultimate サクセスプラン |
|--- |--- |--- |
|  | Expert サクセスプランを使用すると、**24 時間 365 日、技術的なトラブルシューティングに関するエキスパートケア**&#x200B;や、重要なビジネス上の問題に関するガイダンスにアクセスすることができます。また、アドビのセルフガイド型リソース、限定公開のベストプラクティス、アドビのエキスパートや同業者のオンラインコミュニティを活用して、迅速な解決策を見つけることができます。 <p> *すべての Adobe Experience Cloud ライセンスに含まれています。* | Ultimate サクセスプランを使用すると、**高パフォーマンスのデジタルエクスペリエンスを実現するための戦略的なガイダンスとプロアクティブな技術的健全性**&#x200B;を体験できます。お客様のアドビ環境は、お客様のビジネスに精通した専門家チームによってサポートされ、お客様の目標とビジネスへの影響の優先順位に合わせたロードマップの実行に重点を置いています。 |
| **サクセスチーム** | プールされたサポートエンジニアチーム | 次が含まれます。 <ul><li> 指定テクニカルアカウントマネージャー </li><li> 指定カスタマーサクセスマネージャー </li><li> 指定サポートサービスマネージャー</li><li> サクセスアクセラレータを提供するプールされたテクニカルエンジニアと戦略的専門家チーム </li><li> プールされたサポートエンジニアチーム </li></ul> |
| **プロアクティブなテクニカルサポートと運用サポート** | ![ not included icon ](../assets/Cross_red_circle.svg){width="20"} 適用外 | 次が含まれます。 <ul><li>アップグレードと移行のレビュー、リリース準備 </li><li>製品ロードマップのレビュー</li><li> 技術的および戦略的ロードマップの調整</li><li>主なイベントの準備と計画</li><li>関連性のあるタイムリーな実施可能性の計画</li><li>技術的なベストプラクティスと業界のガイダンス</li><li>製品チームに対する支持／調整</li><li>主なビジネス目標を達成するための統合された計画 - 相互アクションプラン（MAP）</li></ul> |
| **テクニカルサポート** | 次が含まれます。 <ul><li>**P1**：24 時間 365 日対応の問題サポート</li><li>**P2、P3、P4**：営業時間サポート</li><li>標準の障害管理</li><li>プールされたエスカレーション管理</li></ul> | 次が含まれます。 <ul><li>**P1**：24 時間 365 日対応の問題サポート</li><li>**P2／P3**：24 時間平日対応の問題サポート</li><li>**P4**：営業時間サポート</li><li>優先された障害管理</li><li>専任担当者によるエスカレーション管理</li></ul> |
| **サクセスアクセラレータ** | ![適用外アイコン](../assets/Cross_red_circle.svg){width="20"} 適用外 | TAM および CSM によって定期的にスケジュールされたサクセスアクセラレータ<p>*（詳しくは、「サクセスアクセラレータカタログ」を参照してください）* |
| **サポートチャネル** | オンライン, 電話, Experience League, フォーラム | パーソナライズされたオンラインポータル, 優先電話, Experience League, フォーラム |

{style="table-layout:fixed"}

## サポートアドオン

| アドオン | Expert サクセスプラン | Ultimate サクセスプラン |
|--- |--- |--- |
| **イベント管理アドオン**<br>&#x200B;主要なイベントのライフサイクル全体を管理するために必要なエンドツーエンドのリーダーシップとサポートを提供 | ![ available icon ](../assets/Plus_blue.svg){width="20"} 利用可能 | ![ available icon ](../assets/Plus_blue.svg){width="20"} 利用可能 |
| **テクニカルアカウントディレクターアドオン**<br>&#x200B;リーダーシップ管理を提供かつエグゼクティブエンゲージメントを持ち、ビジネス成果を最大化するガバナンスを実現するリードテクニカルリソース | ![ not available icon ](../assets/Cross_red_circle.svg){width="20"} 利用不可 | ![ available icon ](../assets/Plus_blue.svg){width="20"} 利用可能 |
| **アドバンスクラウドサポートアドオン**<br> Adobe Experience Manager as a Cloud Service のお客様に対するトップティアケアと価値保証 | ![ available icon ](../assets/Plus_blue.svg){width="20"} 利用可能 | ![ available icon ](../assets/Plus_blue.svg){width="20"} 利用可能 |
| **メンターセッションアドオン**<br>&#x200B;ジャストインタイムのトレーニング方法のスキルベースのラーニングを提供 | ![ available icon ](../assets/Plus_blue.svg){width="20"}  利用可能 | ![ available icon ](../assets/green_checkmark.svg){width="20"} 利用可能 |
| **Developer Boostアドオン**<br>&#x200B;お客様の開発作業を支援するフィールドエンジニアリングエキスパートへのアクセスを提供 | ![ available icon ](../assets/Plus_blue.svg){width="20"} 利用可能 | ![ included icon ](../assets/green_checkmark.svg){width="20"}  利用可能 |
| **Priority Queue Bundle アドオン**<br>&#x200B;サポートチケットを優先して対応する権利、Mentor SessionおよびDeveloper Boostをまとめたパッケージ | ![ available icon ](../assets/Plus_blue.svg){width="20"} 利用可能 | ![ included icon ](../assets/green_checkmark.svg){width="20"}  利用可能 |

{style="table-layout:fixed"}
