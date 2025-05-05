---
title: テーブル
description: Markdown テーブルとHTMLテーブルの操作。
hide: true
hidefromtoc: true
exl-id: 5ce746fc-6835-4bee-85c5-5ad5176baca0
source-git-commit: 6893d1e41c3899c3ab6a9b02b305161eb3f7e049
workflow-type: tm+mt
source-wordcount: '1421'
ht-degree: 17%

---

# テーブル

マットがここに何度も何度もいた – 

EDS

標準 Markdown は、基本的なテーブルのみをサポートします。 AdobeDocs Markdown の場合は、次のオプションがあります。

* Markdown の基本テーブル
* HTMLテーブル
* 段落区切り（`<p>`）、改行（`<br>`）、基本リスト（`<ul>`、`<ol>`）用の Markdown テーブルで、HTMLの構文が制限されています。

## HTMLテーブルから Markdown テーブルへの変換

場合によっては、HTMLテーブルを Markdown テーブルまたは Markdown テキストに変換する必要があります。 場合によっては、外観を改善したり、検証エラーを解決したり、今後の編集を容易にする必要があります。

残念ながら、HTMLテーブルをうまく変換するツールは 1 つもありません。 通常、いくつかのツールを組み合わせて、適切な Markdown テーブルを組み合わせます。

| ツール | 機能 |
|--- |--- |
| [Markdown テーブルジェネレーター ](https://www.tablesgenerator.com/markdown_tables) | 最初から Markdown テーブルを作成するのに適しています。 |
| [ 高度なテーブルコンバーター ](https://tableconvert.com/html-to-markdown) | テーブルを任意の形式から任意の形式に変換します。 <p>**注意：** 変換すると、リンクと画像が統合されます。 |
| [ 基本テーブル html/Markdown コンバーター ](https://jmalarcon.github.io/markdowntables/) | 簡易HTMLコンバータ <p>**注意：** 変換すると、リンクと画像が統合されます。 |
| [ テーブル以外のHTML/Markdown コンバーター ](https://codebeautify.org/html-to-markdown) | HTMLテーブルをテーブル以外のマークダウン構文に変換します。 リンク、画像、その他のフラット化された項目をコピーするには、上記のツールと組み合わせて使用します。 |

## Markdown の基本テーブル

* テーブルのプロパティを決定する 2 行目に、少なくとも 3 つのハイフンを追加してください。 例：3 列の表の `|--- |--- |--- |`。
* Markdown テーブルには、ヘッダー行とボディ行が少なくとも 1 つずつ必要です。 1 行または 1 セルのマークダウンテーブルは作成できません（代わりにHTMLを使用してください）。
* 各行のパイプ（&vert;）文字の数が同じであることを確認します。 テーブルのセルにパイプ文字を含める必要がある場合は、先頭にバックスラッシュ（`\|`）を付けるか、HTML図形コード（`&vert;`）を使用してエスケープします。
* テーブルでのコードブロックの使用には注意が必要です。 インラインコードブロックは、過度な列幅を引き起こす可能性があります。
* テーブルのレンダリング方法を変更するには、「自動」または「固定」を指定します。 [ テーブルのレンダリング方法の変更 ](#table-rendering) を参照してください。

## ボーナスHTMLを使用した Markdown テーブルの作成

移行を容易にするために、Markdown テーブルを拡張して、Markdown テーブル内のHTMLの段落区切り（`<p>`）、改行（`<br>`）、基本的なHTMLリスト（`<ul>` と `<ol>`）をサポートしました。

**改行とリストを含む Markdown テーブル**

```
| Header 1 | Header 2 | Header 3 |
|--- |--- |--- |
| Normal row | row 1 column 2 | row 1 column 3 |
| Line break | first line in cell<br>second line in cell | row 1 column 3 |
| Bullet list | Bullet list:<ul><li>Item 1</li><li>Item 2</li><li>Item 3</li></ul> | row 2 column 3 |
| Bullet list with line break | Bullet list:<ul><li>Item 1</li><li>Item 2</li><li>Item 3</li></ul><br>This is a new line after the bullet list | row 2 column 3 |
```

**例**

| ヘッダー 1 | ヘッダー 2 | ヘッダー 3 |
|--- |--- |--- |
| 通常の行 | row 1 column 2 | row 1 column 3 |
| 改行 | セルの 1 行目 <br> セルの 2 行目 | row 1 column 3 |
| 箇条書き | 箇条書き：<ul><li>項目 1</li><li>項目 2</li><li>項目 3</li></ul> | row 2 column 3 |
| 行区切り付き箇条書き | 箇条書き：<ul><li>項目 1</li><li>項目 2</li><li>項目 3</li></ul><br> これは箇条書きの後の新しい行です | row 2 column 3 |

>[!IMPORTANT]
>
>ネイティブテーブルでHTMLを使用する場合は、適切なHTML構文を使用していることを確認してください。 HTMLの構文に誤りがあると、検証エラーが発生し、そのエラーは理解しにくくなります。 作業内容を再確認してください。

## HTMLテーブルの操作

移行ツールは、元のテーブルからできるだけ多くの書式設定を保持しようとしました。 このHTML構文の大部分は無視されますが、一部の構文では検証エラーが発生します。

**移行されたHTMLテーブルのサンプル**

```
<table> 
 <tbody>
  <tr>
   <th>Property</th> 
   <th>Type</th> 
   <th>Value Description</th> 
  </tr>
  <tr>
   <td>badgingPath</td> 
   <td>String[]</td> 
   <td><p><i>(Required)</i> A multi-value string of badge images up to the number of badgingLevels. The badge image paths must be ordered so the first is awarded to the highest expert. If there are less badges than indicated by badgingLevels, the last badge in the array fills out the rest of the array. Example entry:</p><p> <code>/etc/community/badging/images/expert-badge/jcr:content/expert.png</code></p></td> 
  </tr>
  <tr>
   <td>badgingLevels</td> 
   <td>Long</td> 
   <td><i><p>(Optional)</i> Specifies the levels of expertise to be awarded. For example, if there should be an <code>expert </code>and an <code>almost expert</code> (two badges), then the value should be set to 2. The badgingLevel should correspond with the number of expert-related badge images listed for the badgingPath property. Default is 1.</p></td> 
  </tr>
  <tr>
   <td>badgingType</td> 
   <td>String</td> 
   <td><p><i>(Required)</i> Identifies the scoring engine as either "basic" or "advanced". Set to "advanced" else the default is "basic".</p></td> 
  </tr>
 </tbody>
</table>
```

**レンダリング**

<table> 
 <tbody>
  <tr>
   <th>プロパティ</th> 
   <th>タイプ</th> 
   <th>値の説明</th> 
  </tr>
  <tr>
   <td>badgingPath</td> 
   <td>String[]</td> 
   <td><p><i> （必須） </i> バッジ画像の複数値の文字列（最大バッジレベル数）。 バッジ画像のパスは、最初のパスが最高のエキスパートに授与されるように並べ替える必要があります。 バッジの数が badgingLevels で示される数よりも少ない場合は、配列の最後のバッジが配列の残りの部分を補完します。 エントリの例：</p><p> <code>/etc/community/badging/images/expert-badge/jcr:content/expert.png</code></p></td> 
  </tr>
  <tr>
   <td>バッジのレベル</td> 
   <td>Long</td> 
   <td><p><i> （任意） </i> 付与する専門知識のレベルを指定します。 例えば、<code>expert </code> と <code>almost expert</code> （2 つのバッジ）が存在する必要がある場合、値は 2 に設定する必要があります。 バッジレベルは、badgingPath プロパティにリストされているエキスパート関連のバッジ画像の数と対応する必要があります。 初期設定は 1 です。</p></td> 
  </tr>
  <tr>
   <td>badgingType</td> 
   <td>文字列</td> 
   <td><p><i> （必須） </i> スコアリングエンジンを「基本」または「詳細」として識別します。 「詳細」に設定します。設定しない場合、デフォルトは「基本」になります。</p></td> 
  </tr>
 </tbody>
</table>

**HTMLテーブルを使用するタイミング**

* 列のバランスを取る。
* テーブルのヘッダーを削除するには（Markdown テーブルにはヘッダー行が必要です）。
* 1 行テーブルのボーダーを削除する（`<tr style="border: 0;">`）。
* 列または行の範囲を追加するには、次の手順を実行します。
* 表のセル内の文字を位置合わせするには

**HTMLテーブルを使用する場合のメモ**

* HTMLテーブルで Markdown 構文を使用しないでください。 例えば、HTMLテーブルに `[!NOTE]` を追加すると、（`[!NOTE]`）のようにレンダリングされます。 代わりに、メモや画像などにHTMLの構文を使用します。

  Loc タグは、ページがレンダリングされる前に UICONTROL タグと DNL タグが削除されるので、このルールの例外です。

* テーブルでは、すべてのHTML構文がサポートされているわけではありません。 幅、高さ、色、その他のHTMLの構文要素は、EXL でレンダリングする場合、無視されます。 これらの値は、検証エラーが発生しない限り、のままにすることができます。
* テキストを揃えるには、HTMLで `align: "left|center|right"` を使用します。 例えば、テーブルセルのコンテンツを中央揃えにするには、`<td align="center">` を使用します。
* HTMLテーブルにネストしたテーブルを含めることはできません。

>[!TIP]
>
>1 行のHTMLテーブルの罫線をオフにする場合は、次の構文を使用します。
>
>```
><table>
><tr style="border: 0;">
>```

## テーブルのレンダリング方法の指定 {#table-rendering}

テーブルは 2 つの方法でレンダリングできます。

* **固定** （現在はデフォルト） – テーブルをレンダリングするためのカスタムルールを含みます（画像付きのHTMLテーブルなど）。 テーブルは、スクロールのない全幅としてレンダリングされるので、テキストが重なってしまうことがあります。
* **自動** - Git 固有の Markdown （GFM）と似ています。 テーブルはスクロールできるので、テキストは重なり合いません。

ほとんどの場合、テーブルは同じ外観でレンダリングされます。 ただし、テーブルに重複するテキストが含まれている場合は、`auto` タグを適用する必要があります。 また、画像カードを含むHTMLテーブルが適切にレンダリングされない場合は、`fixed` タグを適用することをお勧めします。

デフォルトを `fixed` から `auto` に変更することを検討しています。

## Markdown テーブルの編集

ネイティブ Markdown テーブルのレンダリング方法を指定する場合は、テーブルの後に次の構文行のいずれかを追加し、前後に空白行を追加します。

* `{style="table-layout:auto"}`
* `{style="table-layout:fixed"}`

![ テーブルのレンダリング ](assets/table-render.png)

### HTMLテーブルの編集

HTMLテーブルのレンダリング方法を指定する場合は、テーブルの最初の行に次の構文行のいずれかを使用します。

* `<table style="table-layout:auto">`
* `<table style="table-layout:fixed">`

```
<table style="table-layout:fixed">
  <tr>
    <th>Month</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>January</td>
    <td>$100</td>
  </tr>
</table>
```

### 自動または固定を使用するタイミング

**重なり合うテキスト**

`fixed` （デフォルト）が選択されている場合、長いコードブロックまたはテキストを含むテーブルで、テキストが重なり合う場合は、`auto` を使用します。

*固定（デフォルト）*

| インサイト指標 | 説明 | ID クエリーパラメーター |
| ---- | ---- | ---- |
| **timeseries.data.collection.validation.category.type.count** | 1 つのデータセットまたはすべてのデータセットに対する無効な「タイプ」メッセージの合計数。 | データセット ID |
| **timeseries.data.collection.validation.category.range.count** | 1 つのデータセットまたはすべてのデータセットに対する無効な「範囲」メッセージの合計数。 | データセット ID |
| **timeseries.data.collection.validation.category.format.count** | 1 つのデータセットまたはすべてのデータセットに対する無効な「形式」メッセージの合計数。 | データセット ID |
| **timeseries.data.collection.validation.category.pattern.count** | 1 つのデータセットまたはすべてのデータセットに対する無効な「パターン」メッセージの合計数。 | データセット ID |
| **timeseries.data.collection.validation.category.presence.count** | 1 つのデータセットまたはすべてのデータセットに対する無効な「存在」メッセージの合計数。 | データセット ID |
| **timeseries.data.collection.validation.category.enum.count** | 1 つのデータセットまたはすべてのデータセットに対する無効な「enum」メッセージの合計数。 | データセット ID |

{style="table-layout:fixed"}

*自動*

| インサイト指標 | 説明 | ID クエリーパラメーター |
| ---- | ---- | ---- |
| **timeseries.data.collection.validation.category.type.count** | 1 つのデータセットまたはすべてのデータセットに対する無効な「タイプ」メッセージの合計数。 | データセット ID |
| **timeseries.data.collection.validation.category.range.count** | 1 つのデータセットまたはすべてのデータセットに対する無効な「範囲」メッセージの合計数。 | データセット ID |
| **timeseries.data.collection.validation.category.format.count** | 1 つのデータセットまたはすべてのデータセットに対する無効な「形式」メッセージの合計数。 | データセット ID |
| **timeseries.data.collection.validation.category.pattern.count** | 1 つのデータセットまたはすべてのデータセットに対する無効な「パターン」メッセージの合計数。 | データセット ID |
| **timeseries.data.collection.validation.category.presence.count** | 1 つのデータセットまたはすべてのデータセットに対する無効な「存在」メッセージの合計数。 | データセット ID |
| **timeseries.data.collection.validation.category.enum.count** | 1 つのデータセットまたはすべてのデータセットに対する無効な「enum」メッセージの合計数。 | データセット ID |

{style="table-layout:auto"}

**画像のバランスが取れたHTML テーブル**

`fixed` を使用すると、バランスのとれたイメージが必要なHTML・テーブルで、「`auto`」を選択するとバランスが崩れます。 この例では、画像のサイズは同じですが、中央の列のテキストが多くなります。

*自動*

<table style="table-layout:auto">
<tr>
  <td>
    <a href="note-test.md">
    <img alt="リード" src="assets/leads-home.png"/>
    </a>
    <div>
    <a href="note-test.md"><strong>Adobeリードのワークフロー </strong></a>
    </div>
    <em> リードライターのメイン編集ワークフロー </em>
    <br>
  </td>
  <td>
    <a href="syntax-style-guide.md">
      <img alt="低頻度" src="assets/infrequent.png">
    </a>
    <div>
    <a href="syntax-style-guide.md"><strong> 頻度の低いユーザーのワークフロー </strong></a>
    </div>
    <em> 主筆ではないのですか？ 投稿を行う最も簡単な方法を学びます。 主筆じゃないのか？ 投稿を行う最も簡単な方法を学びます。 主筆じゃないのか？ 投稿を行う最も簡単な方法を学びます。 主筆じゃないのか？ 投稿を行う最も簡単な方法を学びます。 主筆じゃないのか？ 投稿を行う最も簡単な方法を学びます。 主筆じゃないのか？ コントリビューションを行う最も簡単な方法を説明します。</em>
    <br>
  </td>
  <td>
    <a href="note-test.md">
      <img alt="検証" src="assets/validation.png">
    </a>
    <div>
    <a href="note-test.md"><strong> 検証 </strong></a>
    </div>
    <em> 検証エラーの解決方法を説明します。</em>
    <br>
  </td>
</tr>
</table>

*固定（複数の方法で）*

<table style="table-layout:fixed">
<tr>
  <td>
    <a href="note-test.md">
    <img alt="リード" src="assets/leads-home.png"/>
    </a>
    <div>
    <a href="note-test.md"><strong>Adobeリードのワークフロー </strong></a>
    </div>
    <em> リードライターのメイン編集ワークフロー </em>
    <br>
  </td>
  <td>
    <a href="syntax-style-guide.md">
      <img alt="低頻度" src="assets/infrequent.png">
    </a>
    <div>
    <a href="syntax-style-guide.md"><strong> 頻度の低いユーザーのワークフロー </strong></a>
    </div>
    <em> 主筆ではないのですか？ 投稿を行う最も簡単な方法を学びます。 主筆じゃないのか？ 投稿を行う最も簡単な方法を学びます。 主筆じゃないのか？ 投稿を行う最も簡単な方法を学びます。 主筆じゃないのか？ 投稿を行う最も簡単な方法を学びます。 主筆じゃないのか？ 投稿を行う最も簡単な方法を学びます。 主筆じゃないのか？ コントリビューションを行う最も簡単な方法を説明します。</em>
    <br>
  </td>
  <td>
    <a href="note-test.md">
      <img alt="検証" src="assets/validation.png">
    </a>
    <div>
    <a href="note-test.md"><strong> 検証 </strong></a>
    </div>
    <em> 検証エラーの解決方法を説明します。</em>
    <br>
  </td>
</tr>
</table>
