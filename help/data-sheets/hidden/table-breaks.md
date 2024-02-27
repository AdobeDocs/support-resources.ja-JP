---
title: 表の区切り
description: 異なる表の改行のテスト
hide: true
hidefromtoc: true
source-git-commit: cd9f841a3f720ee366b33f3a78f7ca731c0b865a
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 12%

---

# 表の区切り

## を使用した標準的な Markdown テーブル `<br>`

**固定`Green<br>Red<br>Blue`**

|  | 数値 | 色 |
|---|---|---|
| 十安屋 | 17 | 緑<br>赤<br>青 |
| 茉莉亜 | 23 | イエロー<br>茶色 |

{style="table-layout:fixed"}

**自動`Green<br>Red<br>Blue`**

|  | 数値 | 色 |
|---|---|---|
| 十安屋 | 17 | 緑<br>赤<br>青 |
| 茉莉亜 | 23 | イエロー<br>茶色 |

{style="table-layout:auto"}

## 重複を含む Markdown テーブル `<br>`s

**固定`Green<br><br>Red<br><br>Blue`**

|  | 数値 | 色 |
|---|---|---|
| 十安屋 | 17 | 緑<br><br>赤<br><br>青 |
| 茉莉亜 | 23 | イエロー<br><br>茶色 |

{style="table-layout:fixed"}

**自動`Green<br><br>Red<br><br>Blue`**

|  | 数値 | 色 |
|---|---|---|
| 十安屋 | 17 | 緑<br><br>赤<br><br>青 |
| 茉莉亜 | 23 | イエロー<br><br>茶色 |

{style="table-layout:auto"}

## を使用した Markdown テーブル `<p>`

**固定`Green<p>Red<p>Blue`**

|  | 数値 | 色 |
|---|---|---|
| 十安屋 | 17 | グリーン<p>赤<p>青 |
| 茉莉亜 | 23 | 黄色<p>茶色 |

{style="table-layout:fixed"}

**自動`Green<p>Red<p>Blue`**

|  | 数値 | 色 |
|---|---|---|
| 十安屋 | 17 | グリーン<p>赤<p>青 |
| 茉莉亜 | 23 | 黄色<p>茶色 |

{style="table-layout:auto"}

|  | 数値 | 色 |
|---|---|---|
| 十安屋 | 17 | これが色です **緑** これは、前の段落の区切りをテストする問題や手段として、別の行に折り返すことを意図しています。 <p>これが色です **赤** これは、前の段落の区切りをテストする問題や手段として、別の行に折り返すことを意図しています。 <p>これが色です **青** これは、前の段落の区切りをテストする問題や手段として、別の行に折り返すことを意図しています。 |
| 茉莉亜 | 23 | 黄色<p>茶色 |

{style="table-layout:fixed"}

|  | 数値 | 色 |
|---|---|---|
| 十安屋 | 17 | これが色です **緑** これは、前の段落の区切りをテストする問題や手段として、別の行に折り返すことを意図しています。 <p>これが色です **赤** これは、前の段落の区切りをテストする問題や手段として、別の行に折り返すことを意図しています。 <p>これが色です **青** これは、前の段落の区切りをテストする問題や手段として、別の行に折り返すことを意図しています。 |
| 茉莉亜 | 23 | 黄色<p>茶色 |

{style="table-layout:auto"}
