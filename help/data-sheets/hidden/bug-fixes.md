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
* [AI アシスタントを使用したプッシュの生成](tables.md)
* [AI アシスタントを使用したコンテンツ実験](test-redirection.md)

>[!ENDSHADEBOX]

シェードボックスなし

**目次**

* [AI アシスタントの基本を学ぶ](note-test.md)
* **[AI アシスタントを使用したメールの生成](syntax-style-guide.md)**
* [AI アシスタントを使用した SMS の生成](test-page.md)
* [AI アシスタントを使用したプッシュの生成](tables.md)
* [AI アシスタントを使用したコンテンツ実験](test-redirection.md)


## UGP-10584 インラインバッジが機能しない

これらのバッジは、箇条書き項目と同じ行にある必要があります。

* [[!DNL Mixpanel]](note-test.md) [!BADGE &#x200B; 注 &#x200B;]{type=Informative}
* [[!DNL Pendo]](tables.md) [!BADGE &#x200B; テーブル &#x200B;]{type=Positive}
* [[!DNL RainFocus]](syntax-style-guide.md) [!BADGE &#x200B; 構文スタイルガイド &#x200B;]{type=Positive}

## UGP-10560 – 折りたたみ可能なセクションのバッジ

+++ 以前のバージョン

### V1.16 リリース

_2023 年 2 月 13 日_

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポートあり"}

![ 新規 ](assets/package.png)Catalog Service API で製品ビデオがサポートされるようになりました。
![ 修正 ](assets/package.png) 固定価格のバンドル製品がサポートされるようになりました。
![ 修正 ](assets/package.png) 在庫切れのオプションが PDP ウィジェットに表示されるようになりました。

#### 既知の制限事項

これらの機能は、まだサポートされていません。

* 動的属性ペイロードの最大サイズは 9 MB です。
* グループ製品価格。 簡単な製品価格で計算できます。
* 画像配列では、最初の画像にのみ役割が含まれます。

API メッシュとコア GraphQL API を使用すると、次の制限を解決できます。

* 広告の最低価格
* [ 階層レベルの価格 ](https://www.adobe.com)

### V1.13 リリース

_2023年10月12日（PT）_

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポートあり"}

![ 新規 ](assets/package.png) カタログサービスでは、製品バリアントの `inStock` フラグをサポートしています。
![ 新規 ](assets/package.png)`urlKey` と `externalId` がGraphQL スキーマに追加されました。
![ 新規 ](assets/package.png) ダウンロード可能な製品とギフトカードがサポートされるようになりました。

### V1.12 リリース

_2023年9月19日（PT）_

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポートあり"}

![ 新規 ](https://www.adobe.com)。
![ 修正 ](assets/package.png) このリリースには、サービス側のバグ修正と改善が含まれています。

### V1.11 リリース

_2023年7月18日（PT）_

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポートあり"}

![ 新規 ](assets/package.png) カタログサービスで、商品Recommendationsの [`recommendations`](https://developer.adobe.com/commerce/services/graphql/recommendations/recommendations/) GraphQL クエリがサポートされるようになりました。

### V1.10 リリース

_2023年6月27日（PT）_

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポートあり"}

![ 新規 ](assets/package.png)Catalog Service API で「関連製品」がサポートされるようになりました。

### V1.7 リリース

_2023年4月12日（PT）_

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポートあり"}

![ 新規 ](assets/package.png) 削除された製品のバリエーションがカタログサービスでクリーンアップされるようになりました。
![ 修正 ](assets/package.png) インフラストラクチャの拡張性とパフォーマンスの向上。

### V1.6 リリース

_2023年3月28日（PT）_

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポートあり"}

![ 新規 ](assets/package.png) [`products`](https://developer.adobe.com/commerce/services/graphql/catalog-service/products/) クエリにスウォッチを追加しました。
![ 新規 ](https://www.adobe.com)。

### V1.5 リリース

_2023年3月6日（PT）_

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポートあり"}

![ 新規 ](assets/package.png) GraphQL機能 [`categories`](https://developer.adobe.com/commerce/services/graphql/schema/catalog-service/categories/) 追加しました。
![ 修正 ](assets/package.png) パフォーマンスと API のスケーラビリティが向上しました。

### V1.4 リリース

_2023年2月7日（PT）_

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポートあり"}

![ 新規 ](assets/package.png) 公開されたカタログサービスメタパッケージで、インストール手順を簡素化します。
![ 修正 ](assets/package.png)API のスケーラビリティとパフォーマンスの改善。

### V1.3 リリース

_2023年1月17日（PT）_

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポートあり"}

![ 新機能 ](assets/package.png) オンボーディングエクスペリエンスを簡素化および改善しました。
![ 新規 ](assets/package.png) 新しい顧客サンドボックスエンドポイントは、実稼動前のテストで使用できます。
![ 新規 ](assets/package.png) 仮想製品のサポートが追加されました。
![ 修正 ](assets/package.png)API のスケーラビリティとパフォーマンスの改善。

### V1.1 リリース

_2022年11月18日（PT）_

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポートあり"}

![ 新規 ](assets/package.png) カタログサービスで、Adobeの [API メッシュ ](https://developer.adobe.com/graphql-mesh-gateway/) がサポートされるようになりました。
![ 修正 ](assets/package.png) API のスケーラビリティと全体的なパフォーマンスが向上しました。

### V1.0 リリース

_2022年10月4日（PT）_

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポートあり"}

![ 新規 ](assets/package.png) バンドルされた製品とグループ化された製品をサポートするようになりました。
![ 新規 ](assets/package.png) B2B 表示オーバーライドを追加しました。 製品が検索できるようになり、特定の顧客グループのために買い物かごに追加できるようになりました。
![ 修正 ](assets/package.png) サービスがより安定し、パフォーマンスが向上しました。

### 0.3 リリース - Beta+

_2022年9月12日（PT）_

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポートあり"}

![ 新規 ](assets/package.png) バリアント用の画像はサポートされます。製品画像は、選択したオプションに基づいて返されます
![ 新規 ](assets/package.png) 価格サポートの役割：特定の顧客グループのメンバーのみが製品の価格を表示できるようにします
![ 修正 ](assets/package.png) サービスの安定性とパフォーマンスの向上
![ 新規 ](assets/package.png) 製品がカタログから削除されると、更新が受信されます

### Beta リリース

_2022 年 8 月 9 日_

[!BADGE &#x200B; サポート対象 &#x200B;]{type=Informative tooltip="サポートあり"}

![ 新規 ](assets/package.png) `products` クエリと `refineProduct` クエリは、次のデータを返します。

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

私はこれを金曜日の午後に追加しましたが、今はPublishをクリックしませんでした。

### [!BADGE Beta]{type=Informative}

Bob

## UGP-10565 - テキストハイライト表示

`<div class="preview">` の前のテキスト

<div class="preview">

### Workfront ネイティブフィールドを追加

カスタムフォームにWorkfront ネイティブフィールドを追加できます。 カスタムフォームがオブジェクトに添付されると、フィールドはオブジェクトデータから入力されます。 例えば、プロジェクトに添付されたカスタムフォームの「説明」フィールドは、プロジェクトの説明を取り込みます。 （データが利用できない場合、フィールドには「該当なし」と表示される場合があります）。

1. 画面の左側で **ネイティブフィールド** を見つけて、キャンバス上のセクションにドラッグします。
1. 画面の右側で、カスタムフィールドのオプションを設定します。

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">ラベル</td> 
      <td> <p>（必須） フィールドの上に表示する説明ラベルを入力します。 ラベルはいつでも変更できます。</p> <p><b> 重要 </b>：このラベルでは特殊文字を使用しないでください。 レポートに正しく表示されません。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">名前</td> 
      <td> <p>（必須）この名前によって、システムによるフィールドの識別方法が決まります。</p><p> 初めてフィールドを設定する際にラベルを入力すると、それに一致するように「名前」フィールドが自動的に設定されます。 ただし、「ラベル」フィールドと「名前」フィールドは同期されません。これにより、システムに表示される名前を変更しなくても、ユーザーに表示されるラベルを自由に変更できます。</p>
      <p><b> 重要 </b>:
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

1. 変更を保存するには、「**適用**」をクリックして別のセクションに移動し、フォームの作成を続行します。

   または

   **保存して閉じる** をクリックします。

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
    <td> <p>（必須） カスタムフィールドの上に表示する説明ラベルを入力します。 ラベルはいつでも変更できます。 詳しくは、この記事の <a href="https://www.adobe.com" class="MCXref xref"> カスタムフォームへのカスタムフィールドの追加 </a> を参照してください。</p> <p><b> 重要 </b>：このラベルでは特殊文字を使用しないでください。 レポートに正しく表示されません。</p> </td> 
    <td>
    <ul>
    <li>ラジオボタン。 詳しくは、この記事の <a href="https://www.adobe.com"> カスタムフォームへのカスタムフィールドの追加 </a> を参照してください。 （クラスなし）</li>
    <li>チェックボックスグループ</li>
    <li>ドロップダウン</li>
    </ul></td>
</tr> 
</tbody> 
</table>

## UGP-9176 – 古いバグ

「span」タグは、メモ（およびリスト）ではうまく機能しません

新しいコメント機能で使用できる機能とオブジェクトについて詳しくは、「新しいコメント機能 [ を参照してください ](note-test.md)。

1. 返信を追加するオブジェクトに移動します。
1. **更新** をクリックし、オブジェクトの **コメント** タブをクリックして、返信するコメントまたは返信を見つけます

   または

   <span class="preview">[**すべて**] タブをクリックし、**[ コメントで返信**] をクリックして [ コメント ] タブでコメントを開き、返信します。 「すべて」タブでは返信できません。</span>

1. （オプション）返信に以前の更新からのテキストを含めるには、返信先のコメントの右上隅にある **詳細** メニューをクリックし、「**返信を引用**」をクリックします。 前の更新のテキストが入力領域に表示され、灰色の縦線でマークされます。
1. **返信** をクリックします。

   ![](assets/package.png)

   「**返信を追加…**」ボックスの下部で、会話に積極的に参加しているユーザーを表示し、関係がなくなったユーザーをさらに追加または削除できます。 これらのユーザーは、オブジェクトを購読しているすべてのユーザーと共に、オブジェクトに対して更新または返信が行われるたびに通知を受け取ります。 さらにユーザーにタグを付けて、返信に含めることもできます。  さらに多くのユーザーにタグを付けるには、[ 更新で他のユーザーにタグを付ける ](note-test.md) を参照してください。

   >[!TIP]
   >
   >   既存の返信に返信を追加するには、「返信を追加…**ボックスに入力を開始するか、元のコメントの** 返信 **&#x200B;**&#x200B;をクリックします。 返信がスレッドの最後に追加されます。

1. 返信の入力を開始し、リッチテキストツールバーから追加のオプションを使用します。 リッチテキストやその他の更新機能の使用について詳しくは、[ 作業の更新 ](note-test.md) を参照してください。

1. 「**送信**」をクリックして、返信を保存します。

1. （オプション）返信を管理するその他のオプションについては、返信するコメントの右上隅にある **その他** メニューをクリックします。 詳しくは、[ 作業の更新 ](note-test.md) を参照してください。


## UGP-10614 – 画像を含む問題テーブル

`{width="20"}` パラメーターが原因で、テーブルに問題が発生していると思います。

## Expert と Ultimate のSuccess Planの比較

|  | Expert Successプラン | Ultimate Successプラン |
|--- |--- |--- |
|  | Expert Success Planでは、技術的なトラブルシューティングやお客様の重要なビジネス上の課題に対するガイダンスのために&#x200B;**24時間 365 日、エキスパートケア**&#x200B;にアクセスすることができます。また、アドビのセルフガイド型リソース、限定公開のベストプラクティス、アドビのエキスパートや同業者が集うオンラインコミュニティを利用して、迅速な解決策を見つけることができます。 <p> *すべての Adobe Experience Cloud ライセンスに含まれています。* | Ultimate Success Planでは、**高パフォーマンスのデジタルエクスペリエンスを実現するための戦略的なガイダンスとプロアクティブな技術的健全性**&#x200B;を体験できます。お客様のアドビ環境は、お客様のビジネスに精通した専門家チームによってサポートされ、お客様の目標とビジネスへの影響の優先順位に合わせたロードマップの実行に重点を置いています。 |
| **サクセスチーム** | プールされたサポートエンジニアチーム | 次が含まれます。 <ul><li> 専任テクニカルアカウントマネージャー </li><li> 専任カスタマーサクセスマネージャー </li><li> 専任サポートサービスマネージャー</li><li> サクセスアクセラレータを提供するプールされたテクニカルエンジニアと戦略的専門家チーム </li><li> プールされたサポートエンジニアチーム </li></ul> |
| **プロアクティブなテクニカルサポートと運用サポート** | ![ not included icon ](../assets/Cross_red_circle.svg){width="20"} 適用外 | 次が含まれます。 <ul><li>アップグレードと移行のレビュー、リリース準備 </li><li>製品ロードマップのレビュー</li><li> 技術的および戦略的ロードマップの調整</li><li>主要なイベントの準備と計画</li><li>関連性のあるタイムリーな主主要計画</li><li>技術的なベストプラクティスと業界のガイダンス</li><li>製品チームに対する連携/代弁</li><li>主要なビジネス目標を達成するための統合された計画 - 相互アクションプラン（MAP）</li></ul> |
| **テクニカルサポート** | 次が含まれます。 <ul><li>**P1**：24 時間 365 日の問題サポート</li><li>**P2、P3、P4**：営業時間内でのサポート</li><li>標準の障害管理</li><li>プールされたエスカレーション管理</li></ul> | 次が含まれます。 <ul><li>**P1**：24 時間 365 日対応の問題サポート</li><li>**P2／P3**：平日24 時間対応の問題サポート</li><li>**P4**：営業時間内でのサポート</li><li>優先された障害管理</li><li>専任担当者によるエスカレーション管理</li></ul> |
| **サクセスアクセラレータ** | ![適用外アイコン](../assets/Cross_red_circle.svg){width="20"} 適用外 | TAM および CSM によって定期的にスケジュールされたサクセスアクセラレータ<p>*（詳しくは、「サクセスアクセラレータカタログ」を参照してください）* |
| **サポートチャネル** | オンライン, 電話, Experience League, フォーラム | パーソナライズされたオンラインポータル, 優先電話, Experience League, フォーラム |

{style="table-layout:fixed"}

## サポートアドオン

| アドオン | Expert Successプラン | Ultimate Successプラン |
|--- |--- |--- |
| **イベント管理アドオン**<br>&#x200B;主要なイベントのライフサイクル全体を管理するために必要なエンドツーエンドのリーダーシップとサポートを提供 | ![ available icon ](../assets/Plus_blue.svg){width="20"} 利用可能 | ![ available icon ](../assets/Plus_blue.svg){width="20"} 利用可能 |
| **テクニカルアカウントディレクターアドオン**<br>&#x200B;リーダーシップ管理を提供かつエグゼクティブエンゲージメントを持ち、ビジネス成果を最大化するガバナンスを実現するリードテクニカルリソース | ![ not available icon ](../assets/Cross_red_circle.svg){width="20"} 利用不可 | ![ available icon ](../assets/Plus_blue.svg){width="20"} 利用可能 |
| **アドバンスクラウドサポートアドオン**<br> Adobe Experience Manager as a Cloud Service のお客様に対するトップティアケアと価値保証 | ![ available icon ](../assets/Plus_blue.svg){width="20"} 利用可能 | ![ available icon ](../assets/Plus_blue.svg){width="20"} 利用可能 |
| **メンターセッションアドオン**<br>&#x200B;ジャストインタイムのトレーニング方法のスキルベースのラーニングを提供 | ![ available icon ](../assets/Plus_blue.svg){width="20"}  利用可能 | ![ available icon ](../assets/green_checkmark.svg){width="20"} 利用可能 |
| **Developer Boostアドオン**<br>&#x200B;お客様の開発作業を支援するフィールドエンジニアリングエキスパートへのアクセスを提供 | ![ available icon ](../assets/Plus_blue.svg){width="20"} 利用可能 | ![ included icon ](../assets/green_checkmark.svg){width="20"}  利用可能 |
| **Priority Queue Bundle アドオン**<br>&#x200B;サポートチケットを優先して対応する権利、Mentor SessionおよびDeveloper Boostをまとめたパッケージ | ![ available icon ](../assets/Plus_blue.svg){width="20"} 利用可能 | ![ included icon ](../assets/green_checkmark.svg){width="20"}  利用可能 |

{style="table-layout:fixed"}
