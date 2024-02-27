---
title: セルフサービスエクセレンスコラボレーションドキュメントの構文と書式設定ガイド
description: Markdown のスタイル設定の基本的な概要
mini-toc-levels: 1
hide: true
hidefromtoc: true
source-git-commit: 77a5127250ffbc9d490579188e8469d4c3dac4c3
workflow-type: tm+mt
source-wordcount: '4238'
ht-degree: 13%

---

# Markdown 構文スタイルガイド

このページでは、Markdown(.md) 形式を使用した Digital Experience Technical Documentation Authoring の Markdown コンポーネントについて説明します。 このページには、Adobe従業員の詳細が含まれます。

EDS

こちらを参照してください。 [Adobe.com](https://www.adobe.com){rel=nofollow}

<!--
* You can [view a basic sample file](sample.md) or [view a sample file with advanced syntax examples](sample-full.md)
-->

>[!TIP]
>
>ご覧ください [AdobeDocs Markdown ビデオ](https://video.tv.adobe.com/v/26165).

ほとんどの場合、テキストを書式設定する際は、標準の Git 固有の Markdown(GFM) 構文に従います。 ただし、一部の構文（横線など）はサポートされておらず、ドキュメントのニーズに合わせて様々な方法で Markdown を拡張しています。

## 基本的なテキストの書式設定

Markdown では、段落を特別な構文で指定する必要はありません。 各段落の間に空白行を追加します。

テキストを次の形式に設定するには **太字**&#x200B;で囲む場合は、2 つのアスタリスクで囲みます。

```
This text is **bold**.
```

テキストを&#x200B;*斜体*&#x200B;にするには、1 つのアスタリスクで囲みます。

```
This text is *italic*.
```

テキストを両方として書式設定するには ***太字と斜体***&#x200B;次の 3 つのアスタリスクで囲みます。

```
This is text is both ***bold and italic***.
```

Markdown の書式設定文字を無視する場合は、 `\` 文字の前：

`This is not \*italicized\* type.`

レンダリング：これは斜体ではありません。

## バッジ

処理中。 ロケーションで待機中

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

## Blockquotes

オーサリングシステムはブロック引用符の構文 (`>` （行の先頭）で、ヒント、メモおよびビデオのカスタム Markdown 拡張を識別します。 実際のブロック引用符を作成するには、 `>` 文字を段落の前に配置します。

>これはブロック引用です。

```
>This is a blockquote quotation.
```

## コードブロック（行単位）{#code-block}

**使用するタイミング**

文の一部のコードをインラインでレンダリングするために使用します。 完全囲みコードブロックを必要としない cookie 名、ファイル名、値、またはコマンドを呼び出すのに最適です。

のコードブロック内のコンテンツが、そのままレンダリングされ、ローカライズされません。 ( このルールの例外は次のとおりです。 `!UICONTROL` および `!DNL` 構文（パブリッシュ用にパッケージ化中に削除されます）。

また、検証すべきでないサンプル URL には、次のコードブロックを使用します。 `https://www.example.com`

**構文**

コードブロックは、ハイライト表示するコード要素を囲むために 1 つのバッククォートを使用します。

```
This is `inline code` within a paragraph of text.
```

**例**

This is `inline code` within a paragraph of text.

>[!TIP]
>
>3 つのバッククォート (&grave;&grave;&grave;) でテキストを折り返して、インラインコードブロックを作成することもできます。 これは、インラインコードブロック内で戻り目盛り文字を参照する必要がある場合に特に便利です。 例：
>
&grave;&grave;&grave;`Use a back tick (`&grave;`) for formatting`&grave;&grave;&grave;

## コードブロック（囲み線）

**使用するタイミング**

コードブロックを使用して、コード構文を表示します。 囲みコードブロックでは、ハイライト表示するコード要素を囲むために、3 重のバッククォートを使用します。 囲みコードブロックの上と下に空白行を追加します。

コードブロックはローカライズされません。

>[!TIP]
>
囲みコードブロックを作成する際に、言語を指定します。 言語を指定すると、その言語に固有の構文のハイライト表示が可能になり、 **コピー** 」ボタンをクリックします。 言語を指定する場合は、行番号を表示することもできます。

**構文**

コード行の前後に 3 つのバッククォート (&grave;&grave;&grave;) を使用します。 開くおよび閉じるバッククォートが同じ数のスペースでインデントされていることを確認します。 最適なレンダリングをおこなうには、コード言語を指定します。

&grave;&grave;&grave;`javascript`

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

Experience League では、コードブロックの構文のハイライト表示をサポートします。構文が適切にハイライト表示されるように、最初のバックティックの後に `java` などの言語を指定します。有効な言語のリストについては、[https://prismjs.com](https://prismjs.com/#supported-languages) を参照してください。言語が不足している場合は、Jira チケットをログに記録してください。

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

### コードブロック内の変数の形式設定

変数の構文（例： ） `<i>italic</i>` は、コードブロックではサポートされていません。 可変テキストを指定する場合、山括弧を使用する方法が 1 つあります `< >`.

## 折りたたみ可能なセクション

折りたたみ可能なセクション ( **アコーディオン**) が表示されるので、この値はデフォルトで非表示になっています。 ユーザーはタイトルをクリックして、セクションを展開または折りたたむことができます。

折りたたみ可能なテキストを使用して、FAQ ページの整理や、ネストされたリストを含む複雑な手順の整理など、複雑なコンテンツを簡略化できます。 例えば、一連のサブステップを表示する代わりに、サブステップを「詳細を表示」セクションに折りたたむことができます。

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

+++詳細を見る折りたたみ可能なセクション内のテキストです。

* 箇条書き 1
* 箇条書き 2
* 箇条書き 3

+++

**メモ**

* 折りたたみ可能なセクション内で折りたたみ可能なセクションをネストしないでください。 入れ子になった折りたたみ可能なセクションが正しくレンダリングされない。 ただし、検証が失敗することはないので、ユーザーには `+++` ネストされたセクションの構文。
* 折りたたみ可能なセクション内の箇条書きリストやコードブロックなどの項目の上と下に空白行を必ず追加してください。空白行を追加しないと、検証エラーが発生します。
* 折りたたみ可能なセクション内に見出しを追加することはできますが、お勧めしません。
* [アコーディオンは、デスクトップ上の複雑なコンテンツに対する答えとは限りません](https://www.nngroup.com/articles/accordions-complex-content/)
* 折りたたみ可能なセクションの歴史的な欠点の 1 つは、 **ページ内で検索** (Ctrl/Cmd+F) 折りたたまれたテキストを無視します。 Safari では、これがまだ当てはまりますが、Chrome では当てはまりません。Chrome では、「ページで検索」を選択すると折りたたまれたテキストが検出されます。
* の例 [メンテナンスの更新](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html?lang=en) 折りたたみ可能なセクションを使用するページ。

## コメントと備考

レンダリングされたヘルプシステムにはコメントは表示されません。 コメントを使用して、自分や他の作成者にメモを残します。 注釈は、テキストの下書きセクションに対しても使用できます。

コメントの場合、ヘルプシステムではレンダリングされませんが、 GitHub.comで Markdown ファイルを編集したユーザーには表示されることに注意してください。 コメントに機密情報を含めないでください。

```
<!-- standard comment code -->

DO NOT USE the following:
<!--> bad comment syntax <-->
```

ドキュメントを編集している場合を除き、この下のテキスト (「You can&#39;t see me」) は表示されません。

<!--
You can't see me (unless you're editing in Git).
-->

**リマインダー：** コメントは、公開されるヘルプ記事には表示されません。 ただし、ユーザーが表示および編集できる、公開用 Markdown ファイル内にはコメントが表示されます。

>[!IMPORTANT]
>
箇条書きリストなどのブロックコンポーネント（特にネストされた箇条書きリスト）内にコメントを追加しないでください。 コメントは、箇条書きリストのレンダリング方法を変更できます。
>
TOC.md ファイル内で、TOC リストの中央にある行をコメントアウトしないでください。 これにより、目次リストが分割され、検証エラーが発生する場合があります。 代わりに、目次内のコメントをファイルの末尾に移動します。

## CONTEXTUALHELP

作成者は、製品チームと協力して、製品 UI またはExperience Platform製品 UI にヘルプポップオーバーを追加できます。 例：

```markdown
>[!CONTEXTUALHELP]
>id="platform_destinations_activate_mandatorykey_4"
>title="About mandatory attributes"
>abstract="Select the XDM schema attributes that all exported profiles should include. Profiles without the mandatory key are not exported to the destination. Not selecting a mandatory key exports all qualified profiles regardless of their attributes."
>additional-url="http://www.adobe.com/go/destinations-mandatory-attributes-en" text="Learn more in documentation"
```

## 定義リスト

定義リストについては、標準の Markdown 構文はまだサポートされていません。 代わりに、次のような手動の書式を使用します。

```
**Frog** - An amphibious green creature. Likes flies.
```

レンダリング：

**カエル**  — 水陸両用の緑の生き物。 ハエが好き。

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

## ファイルをダウンロード

.zip または他のダウンロード可能なファイルを assets ディレクトリにアップロードし、そのファイルにリンクします。 .zip ファイルの場合、リンクをクリックすると、ファイルがダウンロードされます。 PDFや PNG など、ブラウザーで開くことができるファイルタイプの場合は、リンクをクリックすると新しいタブが開きます。 このようなファイルの場合は、圧縮するか、リンクを右クリックしてダウンロードする手順を指定することを検討してください。

`Download` &amp;lbrack;`download-test.zip`&amp;rbrack;`(assets/download-test.zip)`

レンダリング：

ダウンロード [download-test.zip](assets/download-test.zip)

>[!NOTE]
>
ダウンロードファイルおよびダウンロード画像の最大ファイルサイズは 100 MB です。 これがgithub.comの制限です。 git.corp.adobe.comの上限は (250 MB) 高いですが、github.comミラーにファイルをコピーできる必要があります。

## 見出し {#headings}

Markdown では、シャープ記号 (`#`) を使用して見出しレベルを識別できます。 第 1 レベル (`#`) は記事のタイトルで、メタデータヘッダーでも指定されます。これらは同じにします。 2 番目のレベル (`##`) は、ミニ目次に含まれるページのメイン見出しを表します。 AEM (chl-author) での記述に慣れている場合は、レベル 2 の見出し (`##`) をAEMの「見出し 1」コンポーネントにマッピングします。

見出しの最大文字数：69 文字（英語）/120 文字 (LOC)。

```
# This is level 1 (article title)

## This is level 2
   
### This is level 3
```

**見出しのベストプラクティス**

* レベル 1 の見出し (`#`) では、各記事のメタデータの後に空白行が続きます。
* レベル 2 からジャンプする (`##`) をレベル 4 (`####`) をクリックします。
* 空白行を含める *前* および *次より後* 各見出し。
* 見出しに数字が含まれる場合は、数字で始まらない明示的な見出し ID（例： ）を指定します。 `## Release notes for 2016 {#release-notes-2016}`.
* 見出しレベルは 3 つのみにすることをお勧めします。 レベル 4 以降は、現時点では正しくレンダリングされません。
* 見出しは右側のナビゲーションに表示されるので、クリックしてセクションにジャンプできます。 デフォルトでは、右側のナビゲーションには、2 つのレベルの見出しが表示されます。 レベル数を変更する場合は、 `mini-toc-levels` メタデータ ( 例： `mini-toc-levels: 3`.

**見出し ID**

見出し ID( 別名 *アンカー ID*) は、記事内のセクションへのカスタムディープリンクを作成するために使用します。 見出し ID を指定するには、次の形式を使用します。

```
## Creating processing rules {#processing-rules}
```

見出し ID は小文字でハイフネーション処理する必要があります。

見出しの見出し ID を指定しない場合、デフォルトの見出し ID は「スラフィッド」（小文字とハイフネーションで区切られた）となります。 例えば、 `## Creating widgets and Such` 見出しには `#creating-widgets-and-such` アンカー。

## HTML構文 {#html}

セキュリティやアクセシビリティなど、様々な理由により、Markdown で使用できるHTML構文は制限されています。 次のリストは、サポートされるHTML構文を示しています。 このリストにないHTML構文は、検証エラーの原因となります。

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

このリストにHTML構文を追加する場合は、チケットをログに記録するか、SSE チームにお問い合わせください。

## 画像 {#images}

以下を使用します。 `![]()` 画像の構文。 括弧 `[ ]` 代替テキストと括弧を含める `( )` 画像の場所とオプションのホバーテキスト（ツールチップ）を含めます。 感嘆符は、画像とリンクを区別します。

```
![alt text](assets/logo.png "Hover text")
```

![代替テキスト](assets/logo.png "カーソルを合わせたテキスト")

共有画像の場合、画像をルートアセットフォルダーに配置し、リポジトリ内の任意のファイルから機能するルートリンクを使用できます。

```
/help/assets/imagename.png
```

### 画像のサイズ変更と整列

**画像のプロパティ（右揃えの画像を使用）** ![代替テキスト](assets/premium.png "Premium のホバーテキスト"){align="right"}

ページビューや表のセル内で画像のデフォルトの幅や中央揃えを変更したり、画像を右揃えにするには、次のような構文を使用します。

```
![Dive image alt text](assets/maui-dive.jpg "Hover text - Maui dive width is 300 pixels and centered"){width="300" align="center"}
```

レンダリング：

![画像の代替テキストを表示](assets/maui-dive.jpg "ホバーテキスト — Maui ダイブの幅が 300 ピクセルで、中央揃え"){width="300" align="center"}

* 大きな画像の場合は、ページの幅内（少なくとも 640 ピクセルの幅）に収まるように縮小されるほど大きい画像を作成することをお勧めします。 推奨幅は 1,500 ピクセルです。 2500 ピクセルまたは 500 キロバイトを超える画像を作成する必要はありません。 画像の最大ファイルサイズは 100 MB です。
* 小さい画像の場合は、目的の幅（ピクセル単位）を使用して画像を作成するか、次のような幅のパラメーターを使用します。 `{width="250"}` （ピクセル）または `{width="50%"}` （元の画像サイズではなく、表示領域の割合）。 画像は縦横比を保って拡大・縮小されます。 画像は拡大または縮小できるので、ピクセル化には注意が必要です。
* 場合によっては、幅の広い画像（ツールバーなど）は縮小され、狭い画像（パネルなど）は縮小されないので、同じインターフェイスの画像がページ上で不均等に見えることがあります。 その場合は、視覚的な一貫性を高めるために、より広い画像を縮小することを検討してください。
* ビュー領域内でのイメージの配置を変更できます。 次のいずれかを使用 `{align="center"}` または `{align="right"}`. The `valign` パラメーターはサポートされていません。

>[!NOTE]
>
画像の最大ファイルサイズは 100 MB です。 これがgithub.comの制限です。 git.corp.adobe.comの上限は (250 MB) 高いですが、github.comミラーにファイルをコピーできる必要があります。

### 画像リンク

ユーザーが画像をクリックして別のページにジャンプできるようにする場合は、この形式を使用します。

**構文**

```
[![image](assets/core-services_96.png)](https://www.adobe.com)
```

**例**

この画像をクリックして、AdobeWeb サイトに移動します。

[![画像](assets/core-services_96.png)](https://www.adobe.com)

<!--
### Click-to-zoom images

Use the `zoomable` parameter to allow users to click an image to view an enlarged version of the image. When the user mouses over a zoomable image, the pointer becomes a magnifying glass. When clicked, the image expands to the full width of the browser. It can be dismissed with a close button.

**Example**

![Diving image](/help/test-guide/assets/maui-dive.jpg "Diving in Maui"){width="100" zoomable="yes"}

**Syntax**

```
![Diving image](/help/test-guide/assets/maui-dive.jpg "Diving in Maui"){width="100" zoomable="yes"}
```

-->

## リンクとクロスリファレンス {#links-and-cross-references}

外部リンクは直進型で、リンクされたキャプションや純粋な URL としてレンダリングできます。

```
[Adobe](https://www.adobe.com)
```

レンダリング：

[Adobe](https://www.adobe.com)

URL をテキストに直接追加した場合、その URL は自動的にリンクに変換されません。 URL をリンクとして表示する場合は、 `< >` 構文を使用します。 例：

```
https://www.adobe.com

<https://www.adobe.com>
```

レンダリング：

https://www.adobe.com

<https://www.adobe.com>

記事へのリンク（相互参照）は、もう少し複雑になる場合があります。

**オプション 1：標準相対リンク**

標準の相対リンクは次のようになります。

```
See [Overview example article](collaborative-doc-instructions/overview.md)
```

パス名は、ソース・ファイルとターゲット・ファイルの両方の場所を考慮する必要があります。 相対リンクの演算値 ( 例： `./` （現在のディレクトリ）、 `../` （1 つのディレクトリに戻る）、および `../../` （2 つ前のディレクトリ）。

**オプション 2：ルート相対リンク**

このタイプのリンクの利点は、ターゲットファイルにのみ対応する必要があることです。 ソースファイルの場所に関係なく、リポジトリ内の任意のソースファイルから機能します。

```
/help/using/docile-rules/introduction.md
```

**ディープリンク**

記事内の見出しにリンクするには、ターゲット見出しに明示的な見出し ID（「アンカー ID」とも呼ばれる）が含まれている必要があります。 例：

`## Creating audience segments {#creating-audience-segments}`

同じページ内のこの見出しにリンクするには、見出し ID をリンクとして使用します。

`See [Creating audience segments](#creating-audience-segments)`

リポジトリ内の別の記事からこの見出しにリンクするには、リンクの末尾に見出し ID サフィックスを追加します。

`See [Audiences: Creating audience segments](audiences.md#creating-audience-segments)`

**新しいタブで開く**

別のガイドにジャンプする場合など、リンクで新しいタブを開く場合は、 `{target="_blank"}` プロパティを使用します。

例：

`[See What's new](whats-new.md){target="_blank"}`

## メタデータ

Markdown ファイルの先頭にメタデータを追加します。 メタデータ行の後の行（および空白行）は、記事のタイトル (# Title) にする必要があります。

```
---
title: Title for search optimization
description: This is the article description used for search optimization. Use common search keywords and synonyms.
---

# Article title
```

## ローカライゼーションタグ： UICONTROL、DNL、DONOTLOCALIZE

マークダウンのすべてのヘルプコンテンツは、初めに機械翻訳を使用してローカライズされます。ローカライズされていないヘルプの場合は、機械翻訳のままとなります。ただし、過去にローカライズされたヘルプコンテンツの場合、そのコンテンツが人によって翻訳されている間、機械翻訳されたコンテンツがプレースホルダーとして機能します。

## その他の類似項目

「その他の類似項目」コンポーネントを使用して、記事の最後に関連リンクを表示します。 MORELIKETHIS コンポーネントは、レンダリング時に「関連記事」としてレンダリングされます（他の言語にローカライズされます）。

**構文**

![その他の類似項目構文](assets/morelikethis.png)

**例**

>[!MORELIKETHIS]
>
* [Article 1](https://helpx.adobe.com/jp/support/analytics.html)
* [Article 2](https://helpx.adobe.com/jp/support/audience-manager.html)

## メモ/注意

Markdown を拡張して、メモ、ヒント、重要、警告など、様々なタイプのメモの形式を設定しました。

**構文**

```
>[!NOTE]
>
>This is a standard NOTE block.
```

**例**

>[!NOTE]
>
This is a standard NOTE block.

**構文**

```
>[!TIP]
>
>This is a standard tip.
```

**例**

>[!TIP]
>
This is a standard tip.

**構文**

```
>[!WARNING]
>
>This is a standard warning block.
```

**例**

>[!WARNING]
>
これは標準の警告ブロックです。

**構文**

```
>[!IMPORTANT]
>
>This is a standard important block.
```

**例**

>[!IMPORTANT]
>
これは標準的な重要なブロックです。

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
This is a standard NOTE block.
>
複数の段落が含まれます。

新しくサポートされるメモのタイプ：

>[!ADMIN]
>
これは管理メモです。 EXL のみ。

>[!AVAILABILITY]
>
これは、可用性に関するメモです。EXL のみ。

>[!PREREQUISITES]
>
これは、前提条件に関するメモです。EXL のみ。

>[!INFO]
>
これは、情報に関するメモです。EXL のみ。

>[!ERROR]
>
これは、エラーに関するメモです。EXL のみ。

>[!SUCCESS]
>
これは、成功に関するメモです。EXL のみ。

## 番号付きリストと箇条書きリスト {#lists}

番号付きリストを作成するには、行を `1.` または `1)`を使用する場合は、1 つの方法を選択し、記事内で一貫して使用してください。 番号を指定する必要はありません。GitHub によって自動的に番号が振られます。

数値を使用 `1` 番号付きリストの各ステップに対して

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

箇条書きリストを作成するには、行を `*` または `-` または `+`を使用する場合は、1 つの方法を選択し、記事内で一貫して使用してください。 ( 複数の書式を混在させる場合、 `*` および `+`を呼び出した場合、ファイルをチェックインすると、Markdown 検証エラーが表示されます )。

**ベストプラクティス：** 用途 `*` 箇条書きの場合 Visual Studio Code では、箇条書き記号にアスタリスクが適用されるので、アスタリスクを使用すると、順不同のリストを自動作成できます。 (TOC.md ファイルにプラス記号が使用されているのに気がついたかもしれません。 `+` リストの場合。 移住の妨げになります 有効な箇条書き文字は、記事内で一貫性がある限り機能します。)

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

また、リスト内にリストを埋め込んだり、リスト項目間にコンテンツを追加したりすることもできます。 リスト項目間のコンテンツのインデントを設定して、新しいリストを開始しないようにします。 ステップ間の項目は、テキストの先頭までインデントする必要があります。番号付きリストの場合は 3 つのスペース、箇条書きリストの場合は 2 つのスペースです。

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
   This is note text.

1. Do another step.

   これはインデントされた行です。

注意：3 の代わりに 6 個のスペースなど、行のインデントが行き過ぎると、その行のコンテンツはコードブロックとして扱われます。

## ボックスのシェーディング

網掛けボックスは、ページの残りの部分からコンテンツの一部をオフにする場合に便利です。 例えば、Workfrontのチームは、特定の目的を達成するために、テキスト、画像およびコードサンプルを含む「例」ボックスを追加します。 日除けボックスは、「On Your Own」セクションや「Use Case」セクション、または拡張メモやヒントにも役立ちます。

シェードボックスを作成するには、 `>[!BEGINSHADEBOX]` セクションの先頭に、および `>[!ENDSHADEBOX]` 最後に これらの開始タグと終了タグの間のコンテンツはすべて、グレーの背景になります。 ラベルの追加先 `BEGINSHADEBOX` ( 例： `>[!BEGINSHADEBOX "Use Case]` は、太字のシェードボックスのタイトルを作成するオプションの方法です。 また、次の行に太字のテキストや見出しを追加することもできます。

例：

>[!BEGINSHADEBOX]

**HTML表内の境界線の削除**

HTMLテーブルを使用してバランスの取れたデザインを作成し、コンテンツをテーブルのように見せたくない場合があります。 1 行のHTMLテーブルの境界線をオフにするには、次の構文を使用します。

```
<table>
<tr style="border: 0;">
```

>[!NOTE]
>
過剰に使用しないでください。 通常のテーブルの場合、コンテンツ間で一貫したデザインを維持する必要があります。

![表のヒント](assets/table-no-border.png)

3 列のテーブルで、 `<td align="center">` および `<td align="right">` セルの内容をビュー領域全体に均等に分布させます。 そうでなければ、私はあなたに言っていたでしょう。

これはシェードボックスの最後の線です。

>[!ENDSHADEBOX]

## スニペットと次を含む

リポジトリ内の記事間でテキストを共有するには、 `_includes` フォルダーを `help` フォルダー。 この `_includes` フォルダーには、リポジトリ内の他のファイルから参照（含める）できる.md ファイルを含めることができます。 また、 `snippets.md` このリポジトリ内のファイルには、リポジトリ内の任意のファイルから参照できる Head2 アンカーを含めることができます。

snippets.md ファイルの H2 への参照： `{{id-name}}`

インクルードファイルへの参照： `{{$include /help/_includes/filename.md}}`

## テーブル

Markdown ではテーブルに問題が生じる場合があります。 以前のオーサリングシステムからテーブルを移行する場合、単純なテーブル（セルごとに 1 行）はネイティブの Markdown テーブルとしてフォーマットされます（推奨）。 より高度なテーブルはHTML形式です。

>[!TIP]
>
次の項目を見る [Markdown の表（ビデオ）](https://video.tv.adobe.com/v/26220)

ネイティブテーブルは、Markdown の方が見た目が良くなることがよくあります。 列のサイズは内容に応じて変更されます。 HTMLテーブルは、等幅の列でレンダリングされます。

デフォルトでは、セル内の複数の行やリストは Markdown でサポートされません。 ただし、Markdown テーブルを拡張し、セル内の複数行を許可するようにしました ( `<p>` または `<br>`) または基本リスト ( `<ul><li>` など )。

>[!IMPORTANT]
>
これらのHTMLコードを Markdown テーブルに追加する場合は注意してください。 構文が正しくない場合、問題を正確に説明できない、混乱を招く検証エラーが発生します。 HTMLの構文を調べ、正しい形式であることを確認します。

どのテーブルでも使用できません： iframe、セルの範囲、埋め込みテーブル。

ネイティブの Markdown テーブル（ネストされたリストまたは複雑なリスト）では使用できません。

詳しくは、 [テーブル](tables.md)

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
| row 1 | セルの最初の段落<p>セル内の 2 番目の段落 (`<p>`)<br>改行 (`br`) | row 1 column 3 |
| row 2 | 箇条書きリスト<ul><li>項目 1</li><li>項目 2</li><li>項目 3</li></ul> | row 2 column 3 |

**改行と偽リストを含む Markdown テーブル**

手動での箇条書きに対する回避策

```
| Color | Things to Do |
|--- |--- |
| Red | * Read <br> * Write <br> * Study |
| Blue | * Swim <br> * Run <br> * Lift <br> **Note**: Remember to train smart.|
```

**例**

| Color | すべきこと |
|--- |--- |
| 赤 | *読み取り <br> *書き込み <br> *研究 |
| 青 | *泳ぐ <br> *実行 <br> *上昇率 <br> **注意**：必ずスマートトレーニングをおこなってください。 |
.32


## タブ

タブは、セクションの上部にある、様々なコンテンツを表示するクリック可能な領域です。 タブをクリックすると、タブのコンテンツが表示され、他のタブのコンテンツは非表示になります。

タブセットを作成するには、 `>[!BEGINTABS]` （タブセットの先頭）および `>[!ENDTABS]` 最後のタブの後。 追加 `>[!TAB <tab title>]` タグを追加し、その下に各タブのコンテンツを追加します。

**タブの構文**

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

この内容は、「Android」タブに表示されます。

>[!TAB Windows]

この内容は、「Windows」タブに表示されます。

>[!TAB MacOS]

このコンテンツは「MacOS」タブに表示されます。

>[!TAB Linux]

この内容は、「Linux」タブに表示されます。

>[!ENDTABS]

**タブのメモ**

* ページ内検索 (Ctrl+F/Cmd+F) を使用して、表示されないタブ内のコンテンツを検索することはできません。
* タブのタイトルがユーザーのブラウザーのページビューの幅を超えて拡張されている場合は、水平スクロールバーが表示されます。
* タブタイトルの形式を設定することはできません。 追加した構文は、タイトルの一部として渡されます。 例： `>[!TAB **iOS**]` が次のように表示されます。 `**iOS**`.
* 1 つのページに複数のタブセットを作成できますが、別のタブセット内にタブセットをネストすることはできません。
* タブセットには網掛けの背景が適用され、ユーザーがタブの内容を他の内容と区別できるようになります。

## テキストのハイライト表示

Workfront チームは、今後の機能のプレビューを示すために黄色のハイライト表示を使用できるようにするよう求めました。仕組みを以下に示します。

例：

```
This entire paragraph should NOT be highlighted. <span class="preview"> This word is **bold** inside a highlighted sentence.</span> And this is just the last sentence.
```

レンダリング：

この段落全体をハイライト表示しないでください。<span class="preview"> この単語はハイライトされた文内で&#x200B;**太字**&#x200B;になっています。</span> これは最後の文にすぎません。

原則として、 `<span class="preview">` 段落内の段落またはテキストをハイライト表示し、 `<div class="preview">` 複数の段落およびコンポーネントの場合。

>[!NOTE]
>
メモやテーブルなど、特定のページ要素のハイライト表示の改善に取り組んでいます。 不適切なレンダリングが見つかった場合は、JIRA のバグを自由にログに記録できます。 処理中。
>
VSC プレビューは、まだハイライト表示をサポートしていません。

## ビデオ

ビデオは Markdown でネイティブにレンダリングされません。 ビデオをインラインで表示するには、コンポーネントインジケーターを使用します `[!VIDEO]` そして URL を

**構文**

```
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

**例**

>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)

## 追加の Markdown の構文情報

### 拡張 Markdown コンポーネント

一般的な Markdown に含まれていない項目をサポートするには、Markdown を拡張する必要があります。

特殊コンポーネントは、ブロックの種類に対する参照と、角括弧と感嘆符を使用して、ブロックの引用符を含む内で宣言されます。 例えば、メモを宣言する方法を次に示します。

```
>[!NOTE]
>
>This is a note.
```

* メモ（注意事項）：メモ、重要、ヒント、注意、警告を含む
* 埋め込みビデオ
* その他の類似項目（関連記事）
* ローカライゼーション用の様々な UI タグ
* 見出し、画像、コードブロックのコンポーネントプロパティ
* 折りたたみ可能なセクション
* テキストのハイライト表示
* ページタブ

Markdown のブロッククォート ( `>` ) を各行の先頭に配置し、メモなどの段落ベースのコンポーネントを結び付けます。 プレビューを改善するには、ブロック引用符記号 (`>`) をクリックします。 セクションを終了するには、空白行を追加します。

コンポーネント内でサブコンポーネントを使用する必要がある場合は、ブロック引用符のレベルをさらに追加します (`>  >`) をサブコンポーネントセクションに追加します。 例えば、ローカライズ禁止セクション内のメモは、次のように始まる必要があります。 `>  >`.

見出しなど、Markdown 要素に固有の設定を使用する必要が生じる場合もあります。 デフォルト設定を変更する必要がある場合は、中括弧で囲んでパラメータを追加します。 `{# }` コンポーネントの後に。

### 空白行

空白の線を含むテキストの壁に、少しの息を入れることができます。 用途 `<br>&nbsp;` 空白行を追加する回避策として。

例：これは、本当に長いテキストになり得る最初の文です。 この段落と次の段落の間に空白行を挿入します。

<br> 

ここではあまり印象的に見えないかもしれませんが、ページが混み過ぎているように感じたときに空白行を試してみてください。

### 「エスケープ」する文字 {#characters-to-escape}

複数の文字 (`# { } [ ] < > * + - . !`) は、見出し、画像、リスト、その他のコンポーネントを作成する際に、Markdown やHTMLで特別な意味を持ちます。 これらの文字を使用すると、レンダリングエンジンはユーザーがコードを追加していると考えます。 ただし、場合によっては、これらの文字をテキストに表示する必要があります。 それには、文字を「エスケープ」する必要があります。 最も簡単なエスケープメソッドは、文字の前にバックスラッシュ (`\`) をクリックします。 例えば、行の先頭に `#` 見出しとして解釈されないように文字を入力する場合は、 `\#`:

`\# This is not a heading`

**レンダリング：**

\#これは見出しではありません

バックスラッシュは次の文字でのみ使用できます。 `# { } [ ] * + - . !`. 山括弧 ( `<yourname>`) を入力する場合は、テキストをバッククォートで囲んでインラインコードブロックを適用するか、文字の代わりにHTMLエンティティコードを使用します。 一般的なHTMLコードの例：

* `&lt;` (&lt;)
* `&gt;` (>)
* `&amp;` (&amp;)
* `&Hat;` (^)
* `&mdash;` (—)
* `&ndash;` (-)

HTMLエンティティの完全なリストは、 [Freeformatter Web サイト](https://www.freeformatter.com/html-entities.html). これにより、すべての特殊文字を検索できます。

>[!NOTE]
>
「ファイルを選択 > 名前を付けて保存」などのチェーンステップでは、 `>` 文字の隣にない文字です。 変数 ( `<filename>` 次のコードブロックを使用して、山括弧をエスケープする `backticks` または文字コード (`&lt;filename&gt;`) をクリックします。

コードブロックでHTMLエンティティを使用する場合、エンティティテキストは特殊文字に変換されません。 例： `&gt;` は、コードブロック内に「 `&gt;` &quot; &quot; > &quot;の代わりに&quot; &quot;を使用します。

バッククォート (&grave;) をエスケープするには、 `&grave;` または、インラインコードブロックをラップする 3 つのバッククォートの内側にバックティックを挿入します。

### サポートされていない項目

Git に基づいた Markdown のアイテムには、サポートする予定がないものもあります。 使用するプレビューツールによって、これらの機能の一部が有効になる場合がありますが、この機能には依存しません。

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

ブロック引用符 (`>` （行の先頭）を示し、ノートやビデオなどの拡張 Markdown 構文を示します。 ただし、 `>` 構文を使用してブロック引用セクションを作成します。

>[!NOTE]
>
3 つではなく 6 つのスペースなど、インデントが行き過ぎると、コンテンツはブロック引用符としてレンダリングされます。 適切な量のインデントを使用して、コンテンツが誤ってブロック引用としてレンダリングされるのを防ぎます。
