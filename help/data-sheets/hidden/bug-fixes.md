---
title: バグ修正（非表示）
description: 内部テスト用のテストページ
hide: true
hidefromtoc: true
source-git-commit: 3c5839d71d68232c631fb9ff5bebfa5ea864d250
workflow-type: tm+mt
source-wordcount: '1358'
ht-degree: 4%

---

# バグの修正

## インラインバッジが機能しない

これらのバッジは、箇条書き項目と同じ行に配置する必要があります。

* [[!DNL Mixpanel]](note-test.md) [!BADGE メモ]{type=Informative}
* [[!DNL Pendo]](tables.md) [!BADGE テーブル]{type=Positive}
* [[!DNL RainFocus]](syntax-style-guide.md) [!BADGE 構文スタイルガイド]{type=Positive}

## UGP-10560 — 折りたたみ可能なセクションのバッジ

+++ 以前のバージョン

### V1.16 リリース

_2023 年 2 月 14 日_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) カタログサービス API で製品ビデオがサポートされるようになりました。
![修正点](assets/package.png) 固定価格のバンドル製品がサポートされるようになりました。
![修正点](assets/package.png) 在庫切れのオプションが PDP ウィジェットに表示されるようになりました。

#### 既知の制限事項

以下の機能は、まだサポートされていません。

* 動的属性ペイロードの最大サイズは 9 MB です。
* グループの製品価格。 単純な製品価格で計算できます。
* 画像配列では、最初の画像のみに役割が含まれます。

API Mesh と Core GraphQL API を使用して、次の制限を解決できます。

* 最小広告価格
* [価格帯](https://www.adobe.com)

### V1.13 リリース

_2023年10月12日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) カタログサービスは、 `inStock` 製品バリアントのフラグ。
![新規](assets/package.png) `urlKey` および `externalId` がGraphQLスキーマに追加されました。
![新規](assets/package.png) ダウンロード可能な製品とギフトカードがサポートされるようになりました。

### V1.12 リリース

_2023年9月19日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](https://www.adobe.com).
![修正点](assets/package.png) このリリースには、サービス側のバグ修正と改善が含まれています。

### V1.11 リリース

_2023年7月18日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) カタログサービスは、 [`recommendations`](https://developer.adobe.com/commerce/services/graphql/recommendations/recommendations/) GraphQL製品Recommendationsに対するクエリ。

### V1.10 リリース

_2023年6月27日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) カタログサービス API で「関連製品」がサポートされるようになりました。

### V1.7 リリース

_2023年4月12日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) カタログサービスで、削除された製品のバリアントをクリーンアップするようになりました。
![修正点](assets/package.png) インフラストラクチャの拡張性とパフォーマンスの向上。

### V1.6 リリース

_2023年3月28日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) スウォッチを [`products`](https://developer.adobe.com/commerce/services/graphql/catalog-service/products/) クエリ。
![新規](https://www.adobe.com).

### V1.5 リリース

_2023年3月6日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) 追加済み [`categories`](https://developer.adobe.com/commerce/services/graphql/schema/catalog-service/categories/) GraphQL機能。
![修正点](assets/package.png) パフォーマンスと API の拡張性が向上しました。

### V1.4 リリース

_2023年2月7日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) インストール手順を簡単にするカタログサービスのメタパッケージを公開しました。
![修正点](assets/package.png) API の拡張性とパフォーマンスの向上。

### V1.3 リリース

_2023年1月17日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) オンボーディングエクスペリエンスをシンプル化し、改善しました。
![新規](assets/package.png) 実稼動前のテストで、新しい顧客サンドボックスエンドポイントを使用できます。
![新規](assets/package.png) 仮想製品のサポートが追加されました。
![修正点](assets/package.png) API の拡張性とパフォーマンスの向上。

### V1.1 リリース

_2022年11月18日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) カタログサービスでAdobeの [API メッシュ](https://developer.adobe.com/graphql-mesh-gateway/).
![修正点](assets/package.png) API の拡張性と全体的なパフォーマンスが向上しました。

### V1.0 リリース

_2022年10月4日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) バンドルされた製品とグループ化された製品をサポートするようになりました。
![新規](assets/package.png) B2B 表示の上書きを追加しました。 製品が検索可能になり、特定の顧客グループ用に買い物かごに追加できるようになりました。
![修正点](assets/package.png) サービスの安定性が向上し、パフォーマンスが向上しました。

### 0.3 リリース — ベータ+

_2022年9月12日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) バリエーションをサポートする画像：製品の画像は、選択したオプションに基づいて返されます。
![新規](assets/package.png) 価格サポートの役割：特定の顧客グループのメンバーのみが製品の価格を表示できます
![修正点](assets/package.png) サービスの安定性とパフォーマンスの向上
![新規](assets/package.png) 製品がカタログから削除されると、アップデートを受け取ります

### ベータリリース

_2022年8月9日（PT）_

[!BADGE サポート]{type=Informative tooltip="サポートあり"}

![新規](assets/package.png) The `products` および `refineProduct` クエリは次のデータを返します。

* 定義済み（システム）の製品属性。
* 動的な製品属性を選択し、役割でフィルターします（製品の表示ページ/製品リストページ）。
* 製品オプション。
* 製品画像を使用し、役割 (PDP/PLP) でフィルタリングします。
* シンプルな製品の特定の価格と、設定可能な製品の価格帯。
* 顧客グループの価格と価格帯。 顧客グループを持たない買い物客に対して、フォールバックのデフォルト価格が返されます。
* B2B 顧客固有の価格を使用する製品タイプ。

+++

## UGP-10565 — テキストの強調表示

前のテキスト `<div class="preview">`

<div class="preview">

### Workfrontネイティブフィールドの追加

カスタムフォームにWorkfrontネイティブフィールドを追加できます。 カスタムフォームがオブジェクトに添付されると、そのフィールドにはオブジェクトデータが入力されます。 例えば、プロジェクトに添付されたカスタムフォームの「説明」フィールドが、プロジェクトの説明を取り込みます。 （利用可能なデータがない場合、フィールドに「N/A」と表示される場合があります）。

1. 画面の左側で、を探します。 **ネイティブフィールド** をクリックし、キャンバス上のセクションにドラッグします。
1. 画面の右側で、カスタムフィールドのオプションを設定します。

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">ラベル</td> 
      <td> <p>（必須）フィールドの上に表示する説明的なラベルを入力します。 ラベルはいつでも変更できます。</p> <p><b>重要</b>：このラベルでは特殊文字を使用しないでください。 レポートでは正しく表示されません。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">名前</td> 
      <td> <p>（必須）この名前は、システムによるフィールドの識別方法です。</p><p> 初めてフィールドを設定し、ラベルを入力すると、「名前」フィールドに合わせて自動的に入力されます。 ただし、「ラベル」フィールドと「名前」フィールドは同期されません。これにより、システムで表示される名前を変更することなく、ユーザーに表示されるラベルを自由に変更できます。</p>
      <p><b>重要</b>:
      <ul> 
      <li>これは可能ですが、他のユーザーがWorkfrontでカスタムフォームを使用し始めた後は、この名前を変更しないことをお勧めします。 読み込むと、Workfrontの他の領域で参照される可能性のあるフィールドが認識されなくなります。</p> </li>
      <li> <p>各フィールド名は、組織のWorkfrontインスタンス内で一意である必要があります。 これにより、既に作成済みのものを別のカスタムフォームに再利用できます。</p> </li>
      <li><p>Workfrontの様々な領域でフィールドを使用する際にエラーが発生しないよう、カスタムフィールド名にはピリオド (.) やドット (.) を使用しないことをお勧めします。</p></td> 
     </tr> 
     <tr> 
      <td role="rowheader">手順</td> 
      <td> <p>フィールドに関する追加情報を入力します。 カスタムフォームに入力する際に、疑問符アイコンの上にマウスポインターを置くと、ここに入力した情報を含むツールヒントが表示されます。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">参照フィールド</td> 
      <td><p>（必須）Workfrontネイティブフィールドを選択します。<p><p>フォームのオブジェクトのネイティブフィールドのみを使用できます。 例えば、フォームデザイナーの上部にある「オブジェクトの種類」リストに「プロジェクト」と表示されている場合、プロジェクトのネイティブフィールドを選択できますが、タスクに固有のフィールドは選択できません。</p></td>
     </tr>
     <tr> 
      <td role="rowheader">サイズ</td> 
      <td>（オプション）必要に応じて、フィールドの表示サイズを変更します。</td> 
     </tr> 
    </tbody> 
   </table>

1. 変更を保存するには、 **適用** フォームの作成を続行するには、別のセクションに移動します。

   または

   「**保存して閉じる**」をクリックします。

</div>

ハイライト表示後のテキスト

## UGP-10566 — リンクテキストがHTMLテーブルの通常のテキストより小さい

「UGP-9780」も参照

<table style="table-layout:auto"> 
<tbody> 
<tr>
<td>に入力</td>
<td>説明</td>
<td>次の用途で使用可能： </td>
</tr>
<tr> 
    <td role="rowheader">ラベル</td> 
    <td> <p>（必須）カスタムフィールドの上に表示する説明的なラベルを入力します。 ラベルはいつでも変更できます。 詳しくは、 <a href="https://www.adobe.com" class="MCXref xref">カスタムフォームにカスタムフィールドを追加する</a> 」を参照してください。</p> <p><b>重要</b>：このラベルでは特殊文字を使用しないでください。 レポートでは正しく表示されません。</p> </td> 
    <td>
    <ul>
    <li>ラジオボタン。 詳しくは、 <a href="https://www.adobe.com">カスタムフォームにカスタムフィールドを追加する</a> 」を参照してください。 （クラスなし）</li>
    <li>チェックボックスグループ</li>
    <li>ドロップダウン</li>
    </ul></td>
</tr> 
</tbody> 
</table>

## UGP-9176 — 古いバグ

メモ（およびリスト）では、「span」タグがうまく機能していません

新しいコメント作成エクスペリエンスで使用可能な機能とオブジェクトについて詳しくは、 [新しいコメントエクスペリエンス](note-test.md).

1. 返信を追加するオブジェクトに移動します。
1. クリック **更新**」、「 **コメント** タブをクリックし、返信先のコメントまたは返信を検索します。

   または

   <span class="preview">次をクリック： **すべて** 「 」タブで、「 」をクリックします。 **コメントで返信** をクリックして「コメント」タブでコメントを開き、そのコメントに返信します。 「すべて」タブでは返信できません。</span>

1. （オプション）返信に以前の更新のテキストを含めるには、 **その他** 返信先のコメントの右上隅にあるメニューで、 **見積もりの返信**. 前の更新のテキストが入力領域に表示され、縦の灰色の線が付きます。
1. クリック **返信**.

   ![](assets/package.png)

   会話に積極的に関与しているユーザーがの下部に表示されます。 **返信を追加…** 」ボックスに追加して、不要なものを追加したり、削除したりできます。 これらのユーザーは、オブジェクトを購読しているユーザーと共に、オブジェクトに対して更新または返信がおこなわれるたびに通知を受け取ります。 さらに多くのユーザーにタグを付けて、返信に含めることもできます。  さらに多くのユーザーにタグを付けるには、 [更新時の他のユーザーへのタグ付け](note-test.md).

   >[!TIP]
   >
   >   既存の返信に返信を追加する場合は、 **返信を追加…** ボックスを使用するか、 **返信** 元のコメントに対して。 返信はスレッドの最後に追加されます。

1. 返信の入力を開始し、リッチテキストツールバーの追加のオプションを使用します。 リッチテキストなどの更新機能の使用について詳しくは、 [作業を更新](note-test.md).

1. クリック **送信** をクリックして返信を保存します。

1. （オプション） **その他** 返信先のコメントの右上隅にあるメニューを使用して、返信を管理する他のオプションを選択できます。 詳しくは、 [作業を更新](note-test.md).
