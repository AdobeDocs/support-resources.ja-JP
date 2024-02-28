---
title: 非表示のテストページ
description: このページは、検索や目次から非表示になります
hide: true
hidefromtoc: true
badgePremium: label="プレミアム" type="Positive" url="https://www.premium-product.com" tooltip="プレミアムのダウンロード"
badgeExam: label="試験 ADO-E903" type="neutral"
source-git-commit: 0e4881c62b518866bd39d5c3f8eef0dc6063441b
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 94%

---

# 非表示のテストページ

アクティブ化しますか？午後 3:10 頃に送信を再確認します。午後 3:30 に運用開始になりますか？

## ボタン

[ボタンのデフォルト](https://www.adobe.com/)

**[ボタンのプライマリ](https://www.adobe.com/)**

_[ボタンのセカンダリ](https://www.adobe.com/)_

**_[ボタンの第 3](https://www.adobe.com/)_**

## 問題のプレビュー

次の段落を、VSC プレビューで適切にレンダリングできません。理由はわかりません。

パスワードが [!DNL Adobe] によって管理されている場合は、[Adobe アカウントのパスワードを変更](https://helpx.adobe.com/jp/manage-account/using/change-or-reset-password.html){target="_blank"}できます。

## メモのタイプ

サポートされているすべてのメモのタイプ。

>[!NOTE]
>
>This is a standard NOTE block.

>[!TIP]
>
>This is a standard tip.

>[!IMPORTANT]
>
>これは、重要なメモです。

>[!WARNING]
>
>これは、警告です。

>[!CAUTION]
>
>これは、注意です。

>[!ADMIN]
>
>これは、管理としてレンダリングされる管理に関するメモです。EXL のみ。

>[!AVAILABILITY]
>
>これは、可用性に関するメモです。EXL のみ。

>[!PREREQUISITES]
>
>これは、前提条件に関するメモです。EXL のみ。

>[!INFO]
>
>これは、情報に関するメモです。EXL のみ。

>[!ERROR]
>
>これは、エラーに関するメモです。EXL のみ。

>[!SUCCESS]
>
>これは、成功に関するメモです。EXL のみ。

>[!MORELIKETHIS]
>
>* ページ 1
>* ページ 2

## バッジ

バッジは、コンテンツのインジケーターとして使用される、カラー表示されるラベルです。例えば、バッジを追加して記事を&#x200B;_ベータ版_&#x200B;としてマークしたり、セクションを&#x200B;_プレミアム_&#x200B;としてマークしたりできます。バッジのカラーを変更して、URL とツールチップを関連付けることができます。

[!BADGE バッジの例]

2 つのタイプがあります of それぞれ構文が異なるバッジを以下に示します。

* **メタデータ** - ページの上部付近にバッジを表示します
* **インライン** - 構文が存在するバッジを表示します

### メタデータバッジ

メタデータにバッジ構文を追加すると、記事のページタイトル（H1）の上にバッジが配置されます。

例えば、_バッジ 1_ または&#x200B;_バッジ 2_ を使用してバッジに名前を付けることができます。または、よりクリエイティブにすることもできます（名前が&#x200B;_バッジ_&#x200B;で始まる場合に限ります）。

メタデータの例：

```
badgePremium: label="Premium" type="Positive" url="https://www.premium-product.com" tooltip="Download Premium"
badgeExam: label="Exam ADO-E903" type="neutral"
```

* **badgePremium：**&#x200B;この例では、プレミアムバッジと URL およびツールチップが表示されます。

* **badgeExam：**&#x200B;この例では、試験 ID 番号が付いたダークバッジが表示されます。

#### インラインバッジ

バッジ情報を独自の行で指定するか、見出し、表またはその他のページ要素で指定します。

ベータ版のラベル、青色、URL、ツールチップを含むインラインバッジの構文を以下に示します。

`[!BADGE Beta]{type=Informative url="https://www.example.com" tooltip="Go to example.com"}`

### 使用可能なバッジのカラー

バッジは、Adobe Spectrum で定義されたカラーを使用します。

| タイプ | バッジ |
|---|---|
| 情報（デフォルト） | [!BADGE Beta]{type=Informative url="https://www.example.com"} |
| 正 | [!BADGE 新機能]{type=Positive url=&quot;https://www.example.com&quot; tooltip=&quot;Go to example.com&quot;} |
| 負 | [!BADGE 廃止済み]{type=negative tooltip=&quot;この機能は現在提供終了です&quot;} |
| 中立 | [!BADGE 多分]{type=Neutral tooltip=&quot;乗り手が馬から落ちた…&quot;} |
| 注意 | [!BADGE 注意]{type=Caution tooltip=&quot;Yellow status&quot;} |

構文の例

```
|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off the horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|
```

### バッジの要件

* メタデータで使用できるバッジは 2 つだけです。このルールは設定可能なので、例外が必要な場合はお知らせください。
* バッジラベルのみが必要です。`type`、`url`、`tooltip` パラメーターはオプションです。`type` パラメーターを使用すると、カラーが決定されます。`url` パラメーターを使用すると、ユーザーはバッジをクリックして記事またはページを開くことができます。`tooltip` パラメーターを使用すると、マウスオーバー時にツールチップテキストが表示されます。
* `TOC.md` ファイルにバッジを追加すると、ガイド内のすべての記事にバッジが表示されます。記事にジャンプするバッジの URL を指定する場合は、異なるフォルダー内の記事を考慮して、相対リンク（例：`article.md`）ではなくルートリンク（例：`/help/guide/article.md`）を使用します。
* `metadata-new.md` にバッジを追加すると、リポジトリ内のすべての記事にバッジが表示されます。
* メタデータバッジの場合は、すべての値が引用符で囲まれます。インラインバッジの場合は、`url` と `tooltip` が引用符で囲まれます。
* 有効なタイプの値には、*情報*（デフォルト、青）、*正*（緑）、*負*（赤）、*中立*（濃いグレー）、*注意*（黄）があります。
* バッジラベルは、ローカライズされています。
* 複数のメタデータバッジを指定した場合、バッジは、`badge1:` や `badgeWeb` など、バッジ名に基づいてアルファベット順に表示されます。
* URL を新しいタブで開く場合は、次の構文を使用します。

  ```
  [!BADGE Open in new tab]{type=Negative url="https://www.adobe.com newtab=true" tooltip="Open adobe.com in new tab"}
  ```

  レンダリング：

  [!BADGE 新しいタブで開く]{type=Negative url="https://www.adobe.com newtab=true" tooltip="adobe.com を新しいタブで開きます"}

## テキストのハイライト表示

Workfront チームは、今後の機能のプレビューを示すために黄色のハイライト表示を使用できるようにするよう求めました。仕組みを以下に示します。

例 1：

```
This entire paragraph should NOT be highlighted. <span class="preview"> This word is **bold** inside a highlighted sentence.</span> And this is just the last sentence.
```

レンダリング：

この段落全体をハイライト表示しないでください。<span class="preview"> この単語はハイライトされた文内で&#x200B;**太字**&#x200B;になっています。</span> これは最後の文にすぎません。

例 2：

```
Highlighting should start after this paragraph.

<div class="preview">

Start of DIV.

This is a new paragraph, then an image

![image](/help/data-sheets/assets/BusinessSupportThumbnail.png)

Last highlighted item.

</div>

Not highlighted
```

レンダリング：

この段落の後にハイライト表示を開始する必要があります。

<div class="preview">

DIV の開始。

これは新しい段落で、次に画像が続きます

![画像](/help/data-sheets/assets/BusinessSupportThumbnail.png)

最後にハイライト表示された項目。

</div>

ハイライト表示されていません

## コードブロックの構文のハイライト表示

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
