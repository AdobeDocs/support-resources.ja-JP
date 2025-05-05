---
title: Self Service Excellence Collaborative Documentation Syntax and Formatting Guide
description: Markdown のスタイル設定の基本的な概要
mini-toc-levels: 1
hide: true
hidefromtoc: true
exl-id: 9f15436b-156a-4c07-bfaf-8557cd948197
source-git-commit: 0c01084577891a2869a2f5538381ca952514ff9c
workflow-type: tm+mt
source-wordcount: '4305'
ht-degree: 13%

---

# Markdown 構文スタイルガイド

このページでは、マークダウン（.md）形式を使用したデジタルエクスペリエンスドキュメントのオーサリング用のマークダウンコンポーネントについて説明します。 このページには、Adobe社員の詳細が含まれます。

EDS

参照：[Adobe.com](https://www.adobe.com){rel=nofollow}

<!--
* You can [view a basic sample file](sample.md) or [view a sample file with advanced syntax examples](sample-full.md)
-->

>[!TIP]
>
>この [AdobeDocs Markdown ビデオ ](https://video.tv.adobe.com/v/26165) をご覧ください。

ほとんどの場合、テキストの書式設定には、Git に特化した標準の Markdown （GFM）構文に従います。 ただし、一部の構文（水平線など）はサポートされておらず、ドキュメントのニーズに合わせて様々な方法で Markdown を拡張しました。

## 基本的なテキストフォーマット

段落には、Markdown での特別な構文は必要ありません。 各段落の間に空白行を追加します。

テキストを **太字** 形式にするには、次の 2 つのアスタリスクで囲みます。

```
This text is **bold**.
```

テキストを&#x200B;*斜体*&#x200B;にするには、1 つのアスタリスクで囲みます。

```
This text is *italic*.
```

テキストを太字と斜体 ***の両方の形式にするには*** 次の 3 つのアスタリスクで囲みます。

```
This is text is both ***bold and italic***.
```

Markdown の書式設定文字を無視するには、文字の前に `\` を使用します。

`This is not \*italicized\* type.`

レンダリング済み：これは\*italicized\* タイプではありません。

## バッジ

処理中。 Loc を待っています。

<!--

See the [dev version of this article](https://experienceleague-dev.corp.adobe.com/docs/authoring-guide-exl/using/markdown/syntax-style-guide.html#badges) for an example. Or [this one](https://experienceleague-dev.corp.adobe.com/docs/internal-test/test/badge.html).

There are two ways to create badges:

* **Metadata badge** - Specify the badge information in metadata so that the badge appears above the title in the article. This is especially useful for adding a badge to all articles in a guide or repo via the TOC.md or metadata.me files.
* **Inline badge** - Specify the badge information on its own line or in a heading, table, or other page element.

![badge examples](assets/badge-examples.png)

**Badge syntax**

*Metadata*: `badge: "Beta Content" type="Informative" url="https://www.example.com" tooltip="Go to example.com"`

*Inline*: `[!BADGE Beta Content]{type=Informative url="https://www.example.com" tooltip="Go to example.com"}`

**Examples**

```
|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off his horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|
```

**Rendered**

|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off his horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|

**More details**

* Only the badge label is required. The `type`, `url`, and `tooltip` parameters are optional. The `type` parameter determines the color. The `url` parameter lets users click the badge to open an article. The `tooltip` parameter displays the tooltip text on mouseover.
* If you want multiple badges to appear at the top of the page, use different badge names. For example, you can create badge names such as `badgeBeta` or `badgeWeb`. Example:

  ```
  badge1: "Beta"
  badge2: "Campaign Web"
  ```

* For metadata badges, make sure that all values are wrapped in quotes. For inline badges, make sure that `url` and `tooltip` are wrapped in quotes.
* Valid type values include *Informative* (default, blue), *Positive* (green), *Negative* (red), *Neutral* (dark gray), and *Caution* (yellow). 

-->

## Blockquote

オーサリングシステムでは、ブロッククォート構文（行の先頭に `>` る）を使用して、ヒント、メモ、ビデオのカスタムマークダウン拡張機能を識別します。 段落の前に `>` 文字を追加することで、実際の引用ブロックを作成できます。

>これは引用ブロックです。

```
>This is a blockquote quotation.
```

## コードブロック （インライン）{#code-block}

**用途**

文のインラインのコードをレンダリングするために使用します。 完全なコードブロックを必要としない cookie 名、ファイル名、値またはコマンドを呼び出すのに最適です。

としてレンダリングされたのコードブロック内のコンテンツは、ローカライズされていません。 （このルールの唯一の例外は `` と `` の構文です。これは、公開のためのパッケージ化の際に削除されます）。

検証してはいけないサンプル URL のコードブロックも使用します：`https://www.example.com`

**構文**

コードブロックでは、ハイライト表示するコード要素を囲むために、バッククォートを 1 つ使用します。

```
This is `inline code` within a paragraph of text.
```

**例**

This is `inline code` within a paragraph of text.

>[!TIP]
>
>また、テキストを 3 つのバッククォート（&grave;&grave;&grave;）で囲んで、インラインコードブロックを作成することもできます。 これは、インラインコードブロック内でバックティック文字を参照する必要がある場合に特に便利です。 例：
>
>&grave;&grave;&grave;`Use a back tick (`&grave;`) for formatting`&grave;&grave;&grave;&grave;

## コードブロック（囲み）

**用途**

コードブロックを使用して、コード構文を表示します。 囲みコードブロックでは、3 つのバッククォートを使用して、ハイライト表示するコード要素を囲みます。 囲みコードブロックの上下に空白行を追加します。

コードブロックはローカライズされません。

>[!TIP]
>
>囲みコードブロックを作成する際は、言語を指定します。 言語を指定すると、その言語に固有の構文をハイライト表示でき、ユーザーに **コピー** ボタンが表示されます。 言語を指定すると、行番号を表示することもできます。

**構文**

コード行の前後に 3 つのバッククォート（&grave;&grave;&grave;）を使用します。 開くティックと閉じるティックが同じ数のスペースにインデントされていることを確認します。 最適なレンダリングを行うには、コード言語を指定します。

&grave;&grave;&grave;grave;`javascript`

**例**

```javascript
var visitor = Visitor.getInstance("INSERT-MARKETING-CLOUD-ORGANIZATION ID-HERE", {
     trackingServer: "INSERT-TRACKING-SERVER-HERE", // same as s.trackingServer
     trackingServerSecure: "INSERT-SECURE-TRACKING-SERVER-HERE", // same as s.trackingServerSecure

     // To enable CNAME support, add the following configuration variables
     // If you are not using CNAME, DO NOT include these variables
     marketingCloudServer: "INSERT-TRACKING-SERVER-HERE",
     marketingCloudServerSecure: "INSERT-SECURE-TRACKING-SERVER-HERE" // same as s.trackingServerSecure
});
```

### コードブロックの構文のハイライト表示

Experience League では、コードブロックの構文のハイライト表示をサポートします。構文が適切にハイライト表示されるように、最初のバックティックの後に `java` などの言語を指定します。有効な言語のリストについては、[https://prismjs.com](https://prismjs.com/#supported-languages) を参照してください。抜けている言語がある場合は、Jira チケットを起票してください。

### コードブロック内の行番号付け

行番号付けを有効にするには、言語の後に `{line-numbers="true"}` を追加します。

行番号（&grave;&grave;&grave;`html {line-numbers="true"}`）を使用する例：

```html {line-numbers="true"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>

</body>
</html>
```

**行番号付けの開始 _**

1 以外の番号から番号付けを開始するには、行番号構文の後に `start-number="n"` を追加します。

新しい開始行（&grave;&grave;&grave;`html {line-numbers="true" start-line="7"}`）を使用する例：

```html {line-numbers="true" start-line="7"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>
<p>My second paragraph.</p>

</body>
</html>
```

### コードブロック内の行のハイライト表示

コードブロック内の行をハイライト表示するには、行番号構文の後に `highlight="n"` を追加します。`11-13, 16` を指定すると、11 行目から 13 行目と 16 行目がハイライト表示されます。

行のハイライト表示（&grave;&grave;&grave;`html {line-numbers="true" start-line="7" highlight="11-13, 16"}`）を使用する例：

```html {line-numbers="true" start-line="7" highlight="11-13, 16"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>
<p>My second paragraph.</p>

</body>
</html>
```

### コードブロックの変数の書式設定

`<i>italic</i>` などの変数の構文は、コードブロックではサポートされていません。 可変テキストを指定するには、山かっこ `< >` を使用する方法があります。

## 折りたたみ可能なセクション

デフォルトで非表示になっている折りたたみ可能なセクション（**アコーディオン** とも呼ばれます）を作成できます。 ユーザーはタイトルをクリックして、セクションを展開または折りたたむことができます。

折りたたみ可能なテキストを使用して、FAQ ページを整理したり、ネストされたリストで複雑な手順を整理したりするなど、複雑なコンテンツを簡略化できます。 例えば、サブステップのセットを表示する代わりに、サブステップを「詳細を表示」セクションに折りたたむことができます。

**構文**

```
+++See details
This is text inside a collapsible section.

* Bullet one
* Bullet two
* Bullet three

+++
```

**例**

+++詳細を表示
これは、折りたたみ可能なセクション内のテキストです。

* 箇条書き 1
* 箇条書き 2
* 箇条書き 3

+++

**メモ**

+++* 折りたたみ可能なセクションは、折りたたみ可能なセクション内にネストしないでください。 ネストされた折りたたみ可能なセクションが正しくレンダリングされない。 ただし、検証が失敗するわけではなく、ネストされたセクションの `` 構文が表示されます。
* 折りたたみ可能なセクション内の箇条書きリストやコードブロックなど、項目の上下に空白行を必ず追加してください。追加しないと、検証エラーが発生します。
* 折りたたみ可能なセクション内に見出しを追加することはできますが、お勧めしません。
* [ アコーディオンは、デスクトップ上の複雑なコンテンツに対する答えであるとは限りません ](https://www.nngroup.com/articles/accordions-complex-content/)
* 折りたたみ可能なセクションの欠点の 1 つは、**ページ内で検索** （Ctrl/Cmd+F）で折りたたまれたテキストが無視されることです。 これは Safari では当てはまりますが、Chromeでは当てはまりません。「ページで検索」は、Chromeで折りたたまれたテキストを検出します。
* 折りたたみ可能なセクションを使用した [ メンテナンス更新 ](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html?lang=ja) ページの例。

## コメントと備考

コメントは、レンダリングされたヘルプ システムには表示されません。 コメントを使用して、自分自身または他のライターにメモを残します。 テキストのドラフトセクションにコメントを使用することもできます。

コメントの場合、ヘルプシステムではレンダリングされませんが、GitHub.comで Markdown ファイルを編集するユーザーには表示されることに注意してください。 コメントに機密情報を含めないでください。

```
<!-- standard comment code -->

DO NOT USE the following:
<!--> bad comment syntax <-->
```

ドキュメントを編集していない限り、この下のテキストは表示されません（「You can&#39;t see me」）。

<!--
You can't see me (unless you're editing in Git).
-->

**注意：** 公開ヘルプ記事にコメント（注釈）が表示されません。 ただし、ユーザーが表示および編集できる、公開用 Markdown ファイル内にはコメントが表示されます。

>[!IMPORTANT]
>
>箇条書きなどのブロックコンポーネント内、特にネストされた箇条書きには、コメントを追加しないでください。 コメントを使用すると、箇条書きのレンダリング方法を変更することができます。
>
>TOC.md ファイルで、TOC リストの途中の行をコメントアウトしないでください。 これにより、目次リストが分割され、検証エラーが発生する可能性があります。 代わりに、目次のコメントをファイルの末尾に移動します。

## コンテキストヘルプ

作成者は製品チームと協力して、Experience CloudまたはExperience Platformの製品 UI にヘルプポップオーバーを追加できます。 例：

```markdown
>[!CONTEXTUALHELP]
>id="platform_destinations_activate_mandatorykey_4"
>title="About mandatory attributes"
>abstract="Select the XDM schema attributes that all exported profiles should include. Profiles without the mandatory key are not exported to the destination. Not selecting a mandatory key exports all qualified profiles regardless of their attributes."
>additional-url="http://www.adobe.com/go/destinations-mandatory-attributes-en" text="Learn more in documentation"
```

## 定義リスト

定義リストの場合、標準の Markdown 構文はまだサポートされていません。 代わりに、次のような手動による書式設定を使用します。

```
**Frog** - An amphibious green creature. Likes flies.
```

レンダリング：

**カエル** – 水陸両用の緑の生き物。 ハエが好き。

<!--
A definition list is a Markdown extension that supports the Definition List component in AEM. A definition list consists of a term and its definition.

**When to use**

Using a definition list is optional. To define lists of features or options, you can use either the definition list syntax or use basic Markdown formatting, such as applying bold to option names.

**Syntax**

```
Frog
: An amphibious green creature. Likes flies.

Cat
: A less amphibious creature than frogs.
```

**Example**

Frog
: An amphibious green creature. Likes flies.

Cat
: A less amphibious creature than frogs.
-->

## ファイルのダウンロード

.zip またはその他のダウンロード可能なファイルをアセットディレクトリにアップロードし、そこにリンクします。 .zip ファイルの場合は、リンクをクリックするとファイルがダウンロードされます。 ブラウザーで開くことができるファイルタイプ（PDFや PNG など）の場合は、リンクをクリックすると新しいタブが開きます。 そのようなファイルについては、それらを圧縮するか、リンクを右クリックしてダウンロードする手順を提供することを検討してください。

`Download` &lbrack;`download-test.zip`&rbrack;`(assets/download-test.zip)`

レンダリング：

ダウンロード [ テスト zip をダウンロード ](assets/download-test.zip)

>[!NOTE]
>
>ダウンロードファイルと画像の最大ファイルサイズは 100 MB です。 github.comの制限です。 git.corp.adobe.comの上限はより大きい（250 MB）が、github.com ミラーにファイルをコピーできる必要がある。

## 見出し {#headings}

Markdown では、シャープ記号（`#`）を使用して見出しレベルを識別します。 最初のレベル（`#`）は記事のタイトルで、これもメタデータヘッダーで指定されます。同じにします。 2 番目のレベル（`##`）は、ミニ目次に含めるページの主な見出しを表します。 AEM（chl-author）での記述に慣れている場合、レベル 2 の見出し（`##`）はAEMの「見出し 1」コンポーネントにマッピングされます。

見出しの最大文字数：69 文字（英語）/120 文字（LOC）。

```
# This is level 1 (article title)

## This is level 2
   
### This is level 3
```

**見出しのベストプラクティス**

* 各記事で、レベル 1 の見出し（`#`）がメタデータの後の空白行の後に続くことを確認します。
* レベル 2 （`##`）からレベル 4 （`####`）にジャンプするなど、レベルをスキップしないでください。
* 各見出しに空白行 *before* と *after* を含めます。
* 見出しに数字が含まれる場合は、数字で始まらない明示的な見出し ID （`## Release notes for 2016 {#release-notes-2016}` など）を指定します。
* 3 つの見出しレベルのみを推奨します。 現時点では、レベル 4 以降が適切にレンダリングされません。
* 見出しは右側のナビゲーションに表示され、クリックしてセクションにジャンプできます。 デフォルトでは、右側のナビゲーションに 2 つのレベルの見出しが表示されます。 レベル数を変更する場合は、`mini-toc-levels: 3` などのメタデータ `mini-toc-levels` 使用します。

**見出し ID**

見出し ID （*アンカー ID* とも呼ばれます）は、記事内のセクションへのカスタムディープリンクを作成するために使用されます。 見出し ID を指定するには、次の形式を使用します。

```
## Creating processing rules {#processing-rules}
```

見出し ID は小文字でハイフンを付ける必要があります。

見出しに見出し ID を指定しない場合、デフォルトの見出し ID は「見出し」（小文字とハイフン）です。 例えば、`## Creating widgets and Such` 見出しには `#creating-widgets-and-such` アンカーが付きます。

## HTML構文 {#html}

セキュリティやアクセシビリティなど、様々な理由により、Markdown で使用できるHTMLの構文は制限されています。 次のリストに、サポートされるHTML構文を示します。 このリストにないHTML構文は、検証エラーになります。

```html
<table>
<tbody>
<td>
<tfoot>
<thead>
<th>
<tr>
<col>
<colgroup>
<p> (paragraph break)
<ul> (unordered list / numbered list)
<ol> (ordered list / bullet list)
<li> (list item)
<br> (line break)
<b>
<caption>
<i>
<strong> (bold)
<u> (underline)
<s> (strikethrough)
<span>
<sub> (subscript)
<sup> (superscript)
<a>
<img>
<div>
<em> (emphasis, italics)
<pre> (codeblock)
<code>
<codeblock>
```

<!--
Bob: Check above no space char. (ignore the space; I can't add a codeblock inside this codeblock)
-->

HTML構文を追加する場合は、チケットをログに記録するか、SSE チームにお問い合わせください。

## 画像 {#images}

画像には `![]()` の構文を使用します。 括弧には代替テキスト `[ ]` 含まれ、括弧には画像の場所とオプションのホバーテキスト（ツールチップ）を含めることがで `( )` ます。 感嘆符は、画像とリンクを区別します。

```
![alt text](assets/logo.png "Hover text")
```

![ 代替テキスト ](assets/logo.png " ホバーテキスト ")

共有画像の場合、画像をルートアセットフォルダーに配置し、リポジトリ内の任意のファイルから機能するルートリンクを使用することができます。

```
/help/assets/imagename.png
```

### 画像のサイズ変更と整列

**画像プロパティ（右揃えの画像を含む）**![ 代替テキスト ](assets/premium.png "Premium ホバーテキスト "){align="right"}

デフォルトの画像の幅または中央を変更したり、ページビューまたはテーブルセル内で画像を右揃えにしたりするには、次のような構文を使用します。

```
![Dive image alt text](assets/maui-dive.jpg "Hover text - Maui dive width is 300 pixels and centered"){width="300" align="center"}
```

レンダリング：

ボブ – 幅= 300 ピクセル下

![ ダイビング画像の代替テキスト ](assets/maui-dive.jpg " ホバーテキスト - Maui ダイビングの幅は 300 ピクセルで中央に配置されています "){width="300" align="center"}

* 大きな画像の場合は、ページ幅に合わせて（幅 640 ピクセル以上）縮小できる大きさの画像を作成することをお勧めします。 推奨幅は 1500 ピクセルです。 2500 ピクセルまたは 500 キロバイトを超える画像を作成する必要はありません。 画像の最大ファイルサイズは 100 MB です。
* 小さな画像の場合、目的の幅をピクセル単位で使用して画像を作成するか、`{width="250"}` （ピクセル）または `{width="50%"}` （元の画像サイズではなく、表示領域の割合）などの幅パラメーターを使用します。 画像は均等に拡大/縮小されます。 画像は拡大または縮小できるので、ピクセル化に注意してください。
* 同じインターフェイスの画像がページ上で大きく表示される場合があります。これは、幅の広い画像（ツールバーなど）は縮小され、幅の狭い画像（パネルなど）は縮小されないからです。 このような場合は、視覚的な一貫性を向上させるために、幅の広い画像を縮小することを検討してください。
* ビュー領域内のイメージの位置合わせを変更できます。 `{align="center"}` または `{align="right"}` を使用します。 `valign` パラメーターはサポートされていません。

>[!NOTE]
>
>画像の最大ファイルサイズは 100 MB です。 github.comの制限です。 git.corp.adobe.comの上限はより大きい（250 MB）が、github.com ミラーにファイルをコピーできる必要がある。

### 画像リンク

ユーザーが画像をクリックして別のページにジャンプできるようにする場合は、この形式を使用します。

**構文**

```
[![image](assets/core-services_96.png)](https://www.adobe.com)
```

**例**

この画像をクリックすると、Adobeの Web サイトに移動します。

[![画像](assets/core-services_96.png)](https://www.adobe.com)

### クリックしてズームする画像

`zoomable` パラメーターを使用すると、ユーザーは画像をクリックして拡大バージョンの画像を表示できます。 ユーザーがズーム可能な画像の上にマウスポインターを置くと、ポインターは虫眼鏡になります。 クリックすると、画像がブラウザーの全幅に拡大されます。 閉じるボタンで閉じることができます。

**例**

![ マウイ島でのダイビング画像 ](/help/data-sheets/hidden/assets/maui-dive.jpg " ダイビング "){width="100" zoomable="yes"}

**構文**

```
![Diving image](/help/data-sheets/hidden/assets/maui-dive.jpg "Diving in Maui"){width="100" zoomable="yes"}
```

## リンクとクロスリファレンス {#links-and-cross-references}

外部リンクは簡単で、リンクキャプションまたは純粋な URL としてレンダリングできます。

```
[Adobe](https://www.adobe.com)
```

レンダリング：

[Adobe](https://www.adobe.com)

URL を直接テキストに追加した場合、自動的にはリンクに変換されません。 URL をリンクとして表示する場合は、構文 `< >` 追加します。 例：

```
https://www.adobe.com

<https://www.adobe.com>
```

レンダリング：

https://www.adobe.com

<https://www.adobe.com>

記事へのリンク（相互参照）はもう少し複雑になる場合があります。

**オプション 1：標準の相対リンク**

標準の相対リンクは次のようになります。

```
See [Overview example article](collaborative-doc-instructions/overview.md)
```

パス名には、ソースファイルとターゲットファイルの両方の場所を指定する必要があります。 `./` （現在のディレクトリ）、`../` （1 つ前のディレクトリ）、`../../` （2 つ前のディレクトリ）など、すべての相対リンクオペランドを使用できます。

**オプション 2：ルート相対リンク**

このタイプのリンクの利点は、ターゲットファイルのみを考慮する必要があることです。 ソースファイルの場所に関係なく、リポジトリ内の任意のソースファイルから機能します。

```
/help/using/docile-rules/introduction.md
```

**ディープリンク**

記事内の見出しにリンクするには、ターゲット見出しに明示的な見出し ID （「アンカー ID」とも呼ばれます）が必要です。 例：

`## Creating audience segments {#creating-audience-segments}`

同じページ内でこの見出しにリンクするには、見出し ID をリンクとして使用します。

`See [Creating audience segments](#creating-audience-segments)`

リポジトリ内の別の記事からこの見出しにリンクするには、リンクの末尾に見出し ID サフィックスを追加します。

`See [Audiences: Creating audience segments](audiences.md#creating-audience-segments)`

**新しいタブで開く**

別のガイドにジャンプする場合など、リンクを新しいタブで開くには、リンクの `{target="_blank"}` プロパティを使用します。

例：

`[See What's new](whats-new.md){target="_blank"}`

## メタデータ

マークダウンファイルの先頭にメタデータを追加します。 メタデータラインの次の行（および空白行）は、記事のタイトル（# タイトル）にする必要があります。

```
---
title: Title for search optimization
description: This is the article description used for search optimization. Use common search keywords and synonyms.
---

# Article title
```

## ローカリゼーションタグ：UICONTROL、DNL、DONOTLOCALIZE

マークダウンのすべてのヘルプコンテンツは、初めに機械翻訳を使用してローカライズされます。ローカライズされていないヘルプの場合は、機械翻訳のままとなります。ただし、過去にローカライズされたヘルプコンテンツの場合、そのコンテンツが人によって翻訳されている間、機械翻訳されたコンテンツがプレースホルダーとして機能します。

## その他の類似項目

記事の最後に関連リンクを表示するには、「その他の関連リンク」コンポーネントを使用します。 レンダリング時、MORELIKETHIS コンポーネントは「関連記事」としてレンダリングされます（他の言語にはローカライズされます）。

**構文**

![ 詳しくは、次の構文を参照してください ](assets/morelikethis.png)

**例**

>[!MORELIKETHIS]
>
>* [Article 1](https://helpx.adobe.com/jp/support/analytics.html)
>* [Article 2](https://helpx.adobe.com/jp/support/audience-manager.html)

## 注意/注意

Markdown を拡張して、様々なタイプのメモ（メモ、ヒント、重要、警告）を書式設定しました。

**構文**

```
>[!NOTE]
>
>This is a standard NOTE block.
```

**例**

>[!NOTE]
>
>これは標準的なメモブロックです。

**構文**

```
>[!TIP]
>
>This is a standard tip.
```

**例**

>[!TIP]
>
>これは標準的なヒントです。

**構文**

```
>[!WARNING]
>
>This is a standard warning block.
```

**例**

>[!WARNING]
>
>これは標準の警告ブロックです。

**構文**

```
>[!IMPORTANT]
>
>This is a standard important block.
```

**例**

>[!IMPORTANT]
>
>これは、標準的な重要ブロックです。

**構文**

```
>[!NOTE]
>
>This is a standard NOTE block.
>
>It includes multiple paragraphs.
```

**例**

>[!NOTE]
>
>これは標準的なメモブロックです。
>
>複数の段落が含まれます。

サポートされる新しいメモのタイプ：

>[!ADMIN]
>
>これは管理メモです。 EXL のみ。

>[!AVAILABILITY]
>
>これは、可用性に関するメモです。EXL のみ。

>[!PREREQUISITES]
>
>これは前提条件に関するメモです。EXL のみ。

>[!INFO]
>
>これは参考情報に関するメモです。EXL のみ。

>[!ERROR]
>
>これは、エラーに関するメモです。EXL のみ。

>[!SUCCESS]
>
>これは、成功に関するメモです。EXL のみ。

## 番号付きリストと箇条書き {#lists}

番号付きリストを作成するには、`1.` または `1)` で行を開始し、方法を 1 つ選択して記事内で一貫して使用します。 番号を指定する必要はありません。GitHub によって自動的に番号が振られます。

番号付きリストのすべての手順に対して、番号 `1` を使用します。

リストの前後に空白行を追加します。

**構文**

```
1. This is step 1.

1. This is the next step.

   1. This is a sub-step

   1. This is a sub-step

1. This is yet another step, the third.
```

**例**

1. This is step 1.

   1. サブステップ

   1. サブステップ

1. This is the next step.

1. This is yet another step, the third.

箇条書きを作成するには、行の先頭に `*`、`-` または `+` を使用し、方法を 1 つ選択して記事内で一貫して使用します。 （`*` と `+` などの形式が混在している場合、ファイルをチェックインすると Markdown 検証エラーが発生します）。

**ベストプラクティス：** 箇条書きには `*` を使用します。 Visual Studio Code では、箇条書きにアスタリスクが適用されるので、アスタリスクを使用して順不同のリストの作成を自動化する方が簡単です。 （TOC.md ファイルでリストにプラス記号 `+` が使用されていることに気づいたかもしれません。 それは移住からのホールドオーバーです。 有効な箇条書き文字は、記事内で一貫性がある限り機能します）。

**構文**

```
* First item in an unordered list.
* Another item.
* Here we go again.
```

**例**

* First item in an unordered list.
* Another item.
* Here we go again.

また、リストをリスト内に埋め込んだり、リスト項目間でコンテンツを追加したりすることもできます。 新しいリストが開始されないように、リスト項目間のコンテンツをインデントします。 ステップとステップの間の項目は、テキストの先頭にインデントする必要があります。つまり、番号付きリストの場合は 3 スペース、箇条書きリストの場合は 2 スペースです。

```
1. Set up your table and code blocks.
1. Perform this step.

   ![screen](assets/core-services_96.png)
   
1. Make sure that your table looks like this: 

   | Hello | World |
   |---|---|
   | How | are you? |
   
1. This is the fourth step.

   >[!NOTE]
   >
   >This is note text.
   
1. Do another step.

   This is an indented line.
```

**例**

1. Set up your table and code blocks.
1. Perform this step.

   ![screen](assets/core-services_96.png)

1. Make sure that your table looks like this:

   | Hello | World |
   |---|---|
   | How | are you? |

1. This is the fourth step.

   >[!NOTE]
   >
   >This is note text.

1. Do another step.

   これはインデントされた行です。

注意：インデントが大きすぎる場合（例えば 3 ではなく 6 スペースなど）、その行の内容はコードブロックとして扱われます。

## シェードボックス

シェードボックスは、ページの残りの部分からコンテンツの一部をオフにする場合に役立ちます。 例えば、Workfront チームは、特定の目的を達成するために、テキスト、画像およびコードサンプルを含んだ「サンプル」ボックスを追加するのが好きです。 シェードボックスは、「自分で」セクションや「ユースケース」セクション、拡張メモやヒントにも役立つ場合があります。

シェードボックスを作成するには、セクションの先頭に `>[!BEGINSHADEBOX]` を追加し、最後に `>[!ENDSHADEBOX]` を追加します。 これらの開始タグと終了タグの間のコンテンツはすべて、グレーの背景になります。 `BEGINSHADEBOX` にラベルを追加する（`>[!BEGINSHADEBOX "Use Case]` など）のは、太字のシェードボックスのタイトルを作成するオプションの方法です。 また、次の行に太字や見出しを追加することもできます。

例：

>[!BEGINSHADEBOX]

**HTMLテーブルのボーダーの削除**

HTMLテーブルを使用してバランスの取れたデザインを作成しても、コンテンツをテーブルのように表示したくない場合があります。 1 行のHTMLテーブルのボーダーをオフにするには、次の構文を使用します。

```
<table>
<tr style="border: 0;">
```

>[!NOTE]
>
>使い過ぎないように。 通常のテーブルの場合、コンテンツ全体で一貫したデザインを維持したいと考えています。

![ テーブルのヒント ](assets/table-no-border.png)

3 列の表では、`<td align="center">` と `<td align="right">` を追加して、セルの内容をビュー領域に均等に配置することもできます。 そうでなかったら、君に言っただろうに。

これがシェードボックスの最後の行です。

>[!ENDSHADEBOX]

## スニペット （次を含む）

リポジトリ内の記事間でテキストを共有するには、リポジト `help` フォルダーに `_includes` フォルダーを作成します。 この `_includes` フォルダーには、リポジトリ内の他のファイルから参照（含める）できる.md ファイルを含めることができます。 さらに、このリポジトリの `snippets.md` ファイルには、リポジトリ内の任意のファイルから参照できる Head2 アンカーを含めることができます。

snippets.md ファイルの H2 への参照：`{{id-name}}`

インクルード ファイルの参照：`{{$include /help/_includes/filename.md}}`

## テーブル

テーブルは、Markdown で問題になる可能性があります。 以前のオーサリングシステムからテーブルを移行する場合、単純なテーブル（セルごとに 1 行）はネイティブの Markdown テーブルとしてフォーマットされます（推奨）。 より高度なテーブルはHTMLとしてフォーマットされます。

>[!TIP]
>
>[Markdown テーブル ](https://video.tv.adobe.com/v/26220) ビデオを視聴

多くの場合、Markdown ではネイティブテーブルの方が適切に表示されます。 列は、内容に応じてサイズが変更されます。 HTMLテーブルは、同じ幅の列でレンダリングされます。

デフォルトでは、Markdown はセル内の複数の行またはリストをサポートしていません。 ただし、Markdown テーブルを拡張して、セル内に複数行（`<p>` または `<br>` を使用）または基本リスト（`<ul><li>` などを使用）を許可するようにしました。

>[!IMPORTANT]
>
>これらのHTMLコードを Markdown テーブルに追加する場合は注意が必要です。 構文が正しくない場合は、問題を正確に説明しない、わかりにくい検証エラーが発生します。 HTMLの構文が適切な形式であることを確認します。

iframes、セル範囲、埋め込みテーブルなど、どのテーブルでも使用できません。

ネイティブの Markdown テーブルでは許可されません：ネストされたリストまたは複雑なリスト。

[ テーブル ](tables.md) を参照してください。

**構文**

```
| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | row 1 column 2 | row 1 column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

**例**

| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | row 1 column 2 | row 1 column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |

単純なテーブルならば、Markdown でも十分に記述できます。しかし、1 つのセルに複数の段落やリストを含むような複雑なテーブルは記述できません。このようなコンテンツを記述したい場合は、見出しとテキストを使用するなど、別の書式を使用することをお勧めします。

**段落区切りとリストを含む Markdown テーブル**

```
| Header | Another header | Yet another header |
|------------|----------|----------------|
| row 1 | first paragraph in cell<p>second paragraph in cell(`<p>`)<br>line break (`br`) | row 1 column 3 |
| row 2 | bullet list<ul><li>item 1</li><li>item 2</li><li>item 3</li></ul> | row 2 column 3 |
```

**例**

| Header | Another header | Yet another header |
|------------|----------|----------------|
| row 1 | セル内の最初の段落<p>セル区切り（`br`） `<p>`2 番目 <br> 段落 | row 1 column 3 |
| row 2 | 箇条書き<ul><li>項目 1</li><li>項目 2</li><li>項目 3</li></ul> | row 2 column 3 |

**改行とフェイクリストを含む Markdown テーブル**

手動の箇条書きで対処します。

```
| Color | Things to Do |
|--- |--- |
| Red | * Read <br> * Write <br> * Study |
| Blue | * Swim <br> * Run <br> * Lift <br> **Note**: Remember to train smart.|
```

**例**

| カラー | やること |
|--- |--- |
| 赤 | *読み取り <br> *書き込み <br> *試験 |
| 青 | *泳ぐ <br>*走る <br> *持ち上げる <br> **メモ**：スマートなトレーニングを忘れずに。 |


## タブ

タブは、セクションの上部にあるクリック可能な領域で、異なるコンテンツを表示します。 タブをクリックすると、タブの内容が表示され、他のタブの内容は非表示になります。

タブセットを作成するには、タブセットの先頭に `>[!BEGINTABS]` を追加し、最後のタブの後に `>[!ENDTABS]` を追加します。 各タブセクション `>[!TAB <tab title>]` タグを追加し、その下に各タブのコンテンツを追加します。

**タブ構文**

```
>[!BEGINTABS]

>[!TAB iOS]

This content appears in the iOS tab.

>[!TAB Android]

This content appears in the Android tab.

>[!TAB Windows]

This content appears in the Windows tab.

>[!TAB MacOS]

This content appears in the MacOS tab.

>[!TAB Linux]

This content appears in the Linux tab.

>[!ENDTABS]
```

**レンダリング**

>[!BEGINTABS]

>[!TAB iOS]

このコンテンツは「iOS」タブに表示されます。

>[!TAB Android]

このコンテンツは「Android」タブに表示されます。

>[!TAB Windows]

このコンテンツは「Windows」タブに表示されます。

>[!TAB MacOS]

このコンテンツは「MacOS」タブに表示されます。

>[!TAB Linux]

この内容は、「Linux」タブに表示されます。

>[!ENDTABS]

**タブメモ**

* ユーザーがページ内検索（Ctrl + F/Cmd + F）を使用して、表示されないタブ内のコンテンツを見つけることはできません。
* タブタイトルがユーザーのブラウザーのページビュー幅を超えている場合は、水平スクロールバーが表示されます。
* タブタイトルの書式は設定できません。 追加する構文は、タイトルの一部として渡されます。 例えば、`>[!TAB **iOS**]` は `**iOS**` と表示されます。
* 1 つのページに複数のタブセットを作成できますが、別のタブセット内にタブセットをネストすることはできません。
* タブセットには影の背景が適用されるので、ユーザーはタブコンテンツと他のコンテンツを区別することができます。

## テキストのハイライト表示

Workfront チームは、今後の機能のプレビューを示すために黄色のハイライト表示を使用できるようにするよう求めました。仕組みを以下に示します。

例：

```
This entire paragraph should NOT be highlighted. <span class="preview"> This word is **bold** inside a highlighted sentence.</span> And this is just the last sentence.
```

レンダリング：

この段落全体をハイライト表示しないでください。<span class="preview"> この単語はハイライトされた文内で&#x200B;**太字**&#x200B;になっています。</span> これは最後の文にすぎません。

原則として、`<span class="preview">` を使用して段落内の段落やテキストをハイライト表示し、複数の段落やコンポーネントに `<div class="preview">` を使用します。

>[!NOTE]
>
>メモやテーブルなどの特定のページ要素のハイライト表示の改善に取り組んでいます。 不適切なレンダリングが表示された場合は、JIRA のバグを自由に記録してください。 処理中。
>
>VSC プレビューでは、ハイライト表示はまだサポートされていません。

## ビデオ

ビデオが Markdown でネイティブにレンダリングされない。 ビデオをインラインで表示するには、コンポーネントインジケーターの `[!VIDEO]` を使用し、URL を使用します。

**構文**

```
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

**例**

>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)

## その他のマークダウン構文情報

### 拡張マークダウンコンポーネント

共通の Markdown に含まれない項目をサポートするには、Markdown を拡張する必要があります。

特殊コンポーネントは、角括弧と感嘆符に、ブロックの種類の参照を加えたものを使用して、ブロック引用を含む形式で宣言されます。 メモの宣言方法の例を以下に示します。

```
>[!NOTE]
>
>This is a note.
```

* メモ（注意、重要、ヒント、注意、警告を含む）
* 埋め込みビデオ
* その他の関連リソース（関連記事）
* ローカライゼーション用の様々な UI タグ
* 見出し、画像およびコードブロックのコンポーネントプロパティ
* 折りたたみ可能なセクション
* テキストのハイライト表示
* ページタブ

メモなどの段落ベースのコンポーネントをまとめるには、各行の先頭に Markdown のブロッククォート（`>`）を使用します。 プレビューを改善するには、ブロック引用符記号のみを持つセクションの開始の直後に行を追加します（`>`）。 セクションを終了するには、空白行を追加します。

コンポーネント内でサブコンポーネントを使用する必要がある場合は、そのサブコンポーネントセクションに追加レベルのブロック引用（`>  >`）を追加します。 例えば、DONOTLOCALIZE セクション内の NOTE は `>  >` で始める必要があります。

場合によっては、見出しなどの Markdown 要素の特定の設定をサポートする必要があります。 デフォルトの設定を変更する必要がある場合は、コンポーネントの後に `{# }` るフランス語の中括弧でパラメーターを追加します。

### 空白行

空白の行を含むテキストの壁に呼吸室を追加できます。 空白行を追加する回避策として、`<br>&nbsp;` を使用します。

例：これは本当に長いテキストである可能性があるものの最初の文です。 この段落と次の段落の間に空行を入れましょう。

<br> 

ここではあまり印象に残らないかもしれませんが、ページが混み過ぎていると感じたら、空白の行を試してみてください。

### 「エスケープ」する文字 {#characters-to-escape}

複数の文字（`# { } [ ] < > * + - . !`）には、見出し、画像、リストおよびその他のコンポーネントを作成するために、Markdown またはHTMLで特別な意味があります。 これらの文字を使用すると、レンダリング エンジンはコードを追加していると判断します。 ただし、場合によっては、これらの文字をテキストに表示する必要があります。 それには、文字を「エスケープ」する必要があります。 最も簡単なエスケープ方法は、文字の前にバックスラッシュ（`\`）を付けることです。 たとえば、`#` 文字を使用して行を開始し、見出しとして解釈しないようにする場合は、次のように入力します `\#`

`\# This is not a heading`

**レンダリング済み：**

\#これは見出しではありません

バックスラッシュは、`# { } [ ] * + - . !` の文字でのみ機能します。 山かっこ（`<yourname>` など）などの文字をエスケープする必要がある場合は、テキストをバッククォートで囲んでインラインコードブロックを適用するか、文字の代わりにHTMLエンティティコードを使用します。 一般的なHTMLコードの例：

* `&lt;` （&lt;）
* `&gt;` （>）
* `&amp;` （&amp;）
* `&Hat;` （^）
* `&mdash;` （–）
* `&ndash;` （–）

HTMLエンティティの完全なリストは、[Freeformatter web サイト ](https://www.freeformatter.com/html-entities.html) で入手できます。 これにより、すべての特殊文字を検索できます。

>[!NOTE]
>
>「ファイル/名前を付けて保存を選択」などのチェーンステップの場合は、`>` の文字は他の文字の隣にないので、エスケープする必要はありません。 `<filename>` などの変数の場合、コードブロックコードまたは文字 `backticks` （`&lt;filename&gt;`）を使用して山括弧をエスケープします。

コードブロックでHTMLエンティティを使用する場合、エンティティテキストは特殊文字に変換されません。 例えば、コードブロックで `&gt;`、「>」ではなく「`&gt;`」と表示されます。

バッククォート（&grave;）をエスケープするには、`&grave;` を使用するか、インラインコードブロックを囲む 3 つのバッククォート内にバッククォートを挿入します。

### サポートされていない項目

サポートする予定のない Git 風味の Markdown アイテムがいくつかあります。 使用するプレビューツールにより、これらの機能の一部が有効になる場合がありますが、それに依存しているわけではありません。

**タスクリスト**

サポートなし

```
* [x] Set up Jersey Shore recording
* [x] Buy donuts with sprinkles
* [x] Take nap
* [ ] Wash ferret
```

**絵文字**

サポートなし

```
:bowtie:
```

**罫線（横）**

サポートなし

```
***
```

**ブロック引用**

次に説明するように、ブロッククォート（行の先頭に `>`）を使用して、メモやビデオなどの拡張 Markdown 構文を示します。 ただし、`>` の構文を使用してブロック引用セクションを作成することもできます。

>[!NOTE]
>
>インデントが大きすぎると（例えば、3 つではなく 6 つのスペースが含まれるなど）、コンテンツはブロック引用符で囲まれてレンダリングされます。 コンテンツが誤ってブロッククォートとしてレンダリングされるのを防ぐために、適切な量のインデントを使用します。
