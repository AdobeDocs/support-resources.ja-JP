---
title: テーブル区切り
description: 様々なテーブル区切りのテスト
hide: true
hidefromtoc: true
exl-id: a769fcb7-f8d3-419b-bdd4-98b71bdf3b5d
source-git-commit: 972704990172c966a27744b49b9f7af5626e9f3e
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 8%

---

# テーブル区切り

あまり見えない。

## `<br>` を含む標準マークダウンテーブル

**固定`Green<br>Red<br>Blue`**

|  | 数値 | 色 |
|---|---|---|
| フアンヤ | 17 | 緑 <br> 赤 <br> 青 |
| マリア | 23 | 黄 <br> 茶 |

{style="table-layout:fixed"}

**自動`Green<br>Red<br>Blue`**

|  | 数値 | 色 |
|---|---|---|
| フアンヤ | 17 | 緑 <br> 赤 <br> 青 |
| マリア | 23 | 黄 <br> 茶 |

{style="table-layout:auto"}

## Markdown テーブル （2 つの `<br>` を含む）

**固定`Green<br><br>Red<br><br>Blue`**

|  | 数値 | 色 |
|---|---|---|
| フアンヤ | 17 | 緑 <br><br> 赤 <br><br> 青 |
| マリア | 23 | 黄 <br><br> 茶 |

{style="table-layout:fixed"}

**自動`Green<br><br>Red<br><br>Blue`**

|  | 数値 | 色 |
|---|---|---|
| フアンヤ | 17 | 緑 <br><br> 赤 <br><br> 青 |
| マリア | 23 | 黄 <br><br> 茶 |

{style="table-layout:auto"}

## `<p>` を使用した Markdown テーブル

**固定`Green<p>Red<p>Blue`**

|  | 数値 | 色 |
|---|---|---|
| フアンヤ | 17 | 緑<p>赤<p>青 |
| マリア | 23 | 黄<p>ブラウン |

{style="table-layout:fixed"}

**自動`Green<p>Red<p>Blue`**

|  | 数値 | 色 |
|---|---|---|
| フアンヤ | 17 | 緑<p>赤<p>青 |
| マリア | 23 | 黄<p>ブラウン |

{style="table-layout:auto"}

|  | 数値 | 色 |
|---|---|---|
| フアンヤ | 17 | これは色 **緑** であり、前述の段落の区切りをテストする問題や手段として、別の行に折り返すことを目的としています。 <p>これは色 **赤** であり、前述の段落の区切りをテストする問題や手段として、別の行に折り返すことを目的としています。 <p>これは色 **青** であり、前述の段落の区切りをテストする問題や手段として、別の行に折り返すことを目的としています。 |
| マリア | 23 | 黄<p>ブラウン |

{style="table-layout:fixed"}

|  | 数値 | 色 |
|---|---|---|
| フアンヤ | 17 | これは色 **緑** であり、前述の段落の区切りをテストする問題や手段として、別の行に折り返すことを目的としています。 <p>これは色 **赤** であり、前述の段落の区切りをテストする問題や手段として、別の行に折り返すことを目的としています。 <p>これは色 **青** であり、前述の段落の区切りをテストする問題や手段として、別の行に折り返すことを目的としています。 |
| マリア | 23 | 黄<p>ブラウン |

{style="table-layout:auto"}
