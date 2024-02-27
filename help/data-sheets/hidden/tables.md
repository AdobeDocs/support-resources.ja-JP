---
title: テーブル
description: Markdown テーブルおよびHTMLテーブルの操作
hide: true
hidefromtoc: true
source-git-commit: 3779d588f21da83928bf0c71357afa90fd5f7179
workflow-type: tm+mt
source-wordcount: '1421'
ht-degree: 18%

---

# テーブル

マットは何度もここにいた —

EDS

標準の Markdown では、基本的なテーブルのみがサポートされます。 AdobeDocs Markdown の場合は、次のオプションを使用できます。

* 基本的な Markdown テーブル
* HTMLテーブル
* 段落区切りのHTML構文が制限された Markdown テーブル (`<p>`)、改行 (`<br>`) と基本リスト (`<ul>`, `<ol>`) をクリックします。

## HTMLテーブルから Markdown テーブルへの変換

場合によっては、HTMLテーブルを Markdown テーブルや Markdown テキストに変換する必要があります。 外観の改善、検証エラーの解決、今後の編集の容易化が必要になる場合があります。

残念ながら、HTMLテーブルをうまく変換するツールを 1 つも見つけることができませんでした。 通常は、ツールの組み合わせを使用して、まともな Markdown テーブルをコブルします。

| ツール | 動作 |
|--- |--- |
| [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) | Markdown テーブルをゼロから作成する場合に適しています。 |
| [高度なテーブルコンバーター](https://tableconvert.com/html-to-markdown) | テーブルを任意の形式から任意の形式に変換します。 <p>**注意：** 変換時に、リンクと画像が統合されます。 |
| [基本テーブル html / Markdown コンバーター](https://jmalarcon.github.io/markdowntables/) | シンプルなHTML変換器 <p>**注意：** 変換時に、リンクと画像が統合されます。 |
| [非テーブルHTML/Markdown コンバーター](https://codebeautify.org/html-to-markdown) | HTMLテーブルを表以外の Markdown 構文に変換します。 上記のツールと組み合わせて、リンク、画像、および他の統合された項目をコピーする場合に使用します。 |

## 基本的な Markdown テーブル

* テーブルのプロパティを決定する 2 番目の行に、少なくとも 3 つのハイフンを追加してください。 例： `|--- |--- |--- |` 3 列のテーブルの場合。
* Markdown テーブルには、少なくとも 1 つのヘッダー行と 1 つのボディ行が必要です。 1 行または 1 セルの Markdown テーブルは作成できません ( 代わりにHTMLを使用 )。
* 各行に同じ数のパイプ ( &amp;vert; ) 文字が含まれていることを確認します。 表のセル内にパイプ文字を含める必要がある場合は、その前にバックスラッシュ (`\|`) またはHTMLエンティティコード (`&vert;`) をクリックします。
* テーブルでのコードブロックの使用には注意が必要です。 インラインコードブロックにより、列の幅が不均等になる場合があります。
* [ 自動 ] または [ 固定 ] を指定して、テーブルのレンダリング方法を変更できます。 詳しくは、 [テーブルのレンダリング方法の変更](#table-rendering).

## ボーナスHTML付き Markdown テーブルの作成

移行を容易にするために、Markdown テーブルを拡張して、HTMLの段落区切り (`<p>`)、改行 (`<br>`) と基本HTMLリスト (`<ul>` および `<ol>`) を Markdown テーブル内に追加します。

**改行とリストが含まれる Markdown テーブル**

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
| 改行 | セルの最初の行<br>セルの 2 行目 | row 1 column 3 |
| 箇条書き | 箇条書き：<ul><li>項目 1</li><li>項目 2</li><li>項目 3</li></ul> | row 2 column 3 |
| 改行付き箇条書き | 箇条書き：<ul><li>項目 1</li><li>項目 2</li><li>項目 3</li></ul><br>これは箇条書きの後の新しい行です | row 2 column 3 |

>[!IMPORTANT]
>
>ネイティブテーブルでHTMLを使用する場合は、適切なHTML構文を使用する必要があります。 HTML構文にエラーがあると、検証エラーを理解するのが困難になります。 作業内容を再度確認します。

## HTMLテーブルの操作

移行ツールは、元のテーブルの書式をできるだけ保持しようとしました。 このHTML構文のほとんどは無視されますが、一部の構文では検証エラーが発生します。

**移行済みHTML表の例**

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
   <td><p><i>（必須）</i> badgingLevels の数までのバッジ画像の複数値文字列。 バッジ画像のパスを並べ替える必要があるので、最初の画像は最も高いエキスパートに与えられます。 badgingLevels で指定した数より少ないバッジが存在する場合、配列の最後のバッジが残りの配列を補完します。 エントリの例：</p><p> <code>/etc/community/badging/images/expert-badge/jcr:content/expert.png</code></p></td> 
  </tr>
  <tr>
   <td>badgingLevels</td> 
   <td>Long</td> 
   <td><p><i>（オプション）</i> 与える専門知識のレベルを指定します。 例えば、 <code>expert </code>および <code>almost expert</code> （バッジが 2 つ）の場合、値は 2 に設定する必要があります。 badgingLevel は、badgingPath プロパティにリストされるエキスパート関連のバッジ画像の数に対応している必要があります。 初期設定は 1 です。</p></td> 
  </tr>
  <tr>
   <td>badgingType</td> 
   <td>文字列</td> 
   <td><p><i>（必須）</i> スコアリングエンジンを「基本」または「詳細」として識別します。 "advanced"に設定し、それ以外の場合、デフォルトは"basic"です。</p></td> 
  </tr>
 </tbody>
</table>

**HTML表を使用するタイミング**

* 列のバランスを取る。
* テーブルヘッダーを省略するには（Markdown テーブルにはヘッダー行が必要です）。
* 1 行のテーブルの境界線を削除するには (`<tr style="border: 0;">`) をクリックします。
* 列または行の範囲を追加するには
* テーブルのセル内でテキストを整列させるには

**HTML表の操作に関する注意**

* HTMLテーブルでは Markdown 構文を使用しないでください。 例えば、 `[!NOTE]` HTMLテーブルには、そのままレンダリングされます (`[!NOTE]`) をクリックします。 代わりに、HTML構文をメモや画像に使用します。

  Loc タグは、ページがレンダリングされる前に UICONTROL タグと DNL タグが削除されるので、このルールは例外です。

* テーブルでは、すべてのHTML構文がサポートされているわけではありません。 幅、高さ、色、およびその他のHTML構文要素は、EXL でレンダリングされると無視されます。 検証エラーが発生しない限り、これらの値はに残すことができます。
* テキストを整列させるには、 `align: "left|center|right"` HTML。 例えば、テーブルのセルの内容を中央揃えにするには、 `<td align="center">`.
* HTMLテーブルにネストされたテーブルを含めることはできません。

>[!TIP]
>
>1 行のHTMLテーブルの境界線をオフにする場合は、次の構文を使用します。
>
>```
><table>
><tr style="border: 0;">
>```

## テーブルのレンダリング方法の指定 {#table-rendering}

テーブルは次の 2 つの方法でレンダリングできます。

* **固定** （現在はデフォルト） — テーブルをレンダリングするためのカスタムルールが含まれます。画像付きのHTMLテーブルも含まれます。 表は全幅でスクロールせずにレンダリングされ、テキストが重なる場合があります。
* **自動** - Git 風の Markdown(GFM) に似ています。 テーブルをスクロールできるので、テキストは重なりません。

ほとんどの場合、テーブルは同じ外観でレンダリングされます。 ただし、テーブルに重なるテキストが含まれている場合は、 `auto` タグを使用します。 または、HTMLカード付きの画像テーブルが正しくレンダリングされない場合は、 `fixed` タグを使用します。

デフォルトを `fixed` から `auto`.

## Markdown テーブルの編集

ネイティブの Markdown テーブルのレンダリング方法を指定する場合は、テーブルの後に次の構文行を追加し、その前後に空白行を追加します。

* `{style="table-layout:auto"}`
* `{style="table-layout:fixed"}`

![table-rendering](assets/table-render.png)

### HTML表の編集

HTMLテーブルのレンダリング方法を指定する場合は、テーブルの最初の行に次の構文行の 1 つを使用します。

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

**テキストの重なり**

用途 `auto` 長いコードブロックまたはテキストを含むテーブルの場合、 `fixed` （デフォルト）が選択されています。

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

**HTMLがバランスのとれた画像のテーブル**

用途 `fixed` HTMLテーブルで、バランスの取れた画像を必要とし、 `auto` が選択されている。 この例では、画像のサイズは同じですが、中央の列の方がテキストが多くなります。

*自動*

<table style="table-layout:auto">
<tr>
  <td>
    <a href="table-breaks.md">
    <img alt="リード" src="assets/leads-home.png"/>
    </a>
    <div>
    <a href="table-breaks.md"><strong>Adobeリードのワークフロー</strong></a>
    </div>
    <em>リードライターのメイン編集ワークフロー。</em>
    <br>
  </td>
  <td>
    <a href="syntax-style-guide.md">
      <img alt="低頻度" src="assets/infrequent.png">
    </a>
    <div>
    <a href="syntax-style-guide.md"><strong>頻度の低いユーザーのワークフロー</strong></a>
    </div>
    <em>リードライターではないのか？ 投稿をおこなう最も簡単な方法を学びます。 リードライターではないのか？ 投稿をおこなう最も簡単な方法を学びます。 リードライターではないのか？ 投稿をおこなう最も簡単な方法を学びます。 リードライターではないのか？ 投稿をおこなう最も簡単な方法を学びます。 リードライターではないのか？ 投稿をおこなう最も簡単な方法を学びます。 リードライターではないのか？ 投稿をおこなう最も簡単な方法を学びます。</em>
    <br>
  </td>
  <td>
    <a href="note-test.md">
      <img alt="検証" src="assets/validation.png">
    </a>
    <div>
    <a href="note-test.md"><strong>検証</strong></a>
    </div>
    <em>検証エラーの解決方法を説明します。</em>
    <br>
  </td>
</tr>
</table>

*修正済み（複数の点で）*

<table style="table-layout:fixed">
<tr>
  <td>
    <a href="table-breaks.md">
    <img alt="リード" src="assets/leads-home.png"/>
    </a>
    <div>
    <a href="table-breaks.md"><strong>Adobeリードのワークフロー</strong></a>
    </div>
    <em>リードライターのメイン編集ワークフロー。</em>
    <br>
  </td>
  <td>
    <a href="syntax-style-guide.md">
      <img alt="低頻度" src="assets/infrequent.png">
    </a>
    <div>
    <a href="syntax-style-guide.md"><strong>頻度の低いユーザーのワークフロー</strong></a>
    </div>
    <em>リードライターではないのか？ 投稿をおこなう最も簡単な方法を学びます。 リードライターではないのか？ 投稿をおこなう最も簡単な方法を学びます。 リードライターではないのか？ 投稿をおこなう最も簡単な方法を学びます。 リードライターではないのか？ 投稿をおこなう最も簡単な方法を学びます。 リードライターではないのか？ 投稿をおこなう最も簡単な方法を学びます。 リードライターではないのか？ 投稿をおこなう最も簡単な方法を学びます。</em>
    <br>
  </td>
  <td>
    <a href="note-test.md">
      <img alt="検証" src="assets/validation.png">
    </a>
    <div>
    <a href="note-test.md"><strong>検証</strong></a>
    </div>
    <em>検証エラーの解決方法を説明します。</em>
    <br>
  </td>
</tr>
</table>
