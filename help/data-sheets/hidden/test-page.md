---
title: テストページ（非表示）
description: 内部テスト用のテストページ
hide: true
hidefromtoc: true
source-git-commit: 8956f958d373f1c67f4ffddf48388f7611ce00ea
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 1%

---

# テストページ（非表示）

非表示のテストページ

## 画像 (EXLM-412)

### カーソルを合わせたテキストを含む画像

![alt テキスト — package.png](assets/package.png "Hover text — これは package.png です。")

### テキストを中央揃え

<p align="center">私は中心です</p>

<center>私は中心です</center>

### ズーム可能な画像

`![Dive image](assets/maui-dive.jpg "Diving in Maui"){width=100 zoomable}`

**プレーン**

![ダイブ画像](assets/maui-dive.jpg "マウイでのダイビング"){width=100 zoomable}

**注意**

>[!NOTE]
>
>次の画像をクリックすると、ダイバーが表示されます。
>
>![ダイブ画像](assets/maui-dive.jpg "マウイでのダイビング"){width=100 zoomable}

**テーブル**

|  | 数値 | 色 |
|---|---|---|
| 十安屋 | 17 | 緑<br>赤<br>青 |
| 茉莉亜 | 23 | イエロー<br>茶色 |
| Bob | 60 | 画像を見る<br>![ダイブ画像](assets/maui-dive.jpg "マウイでのダイビング"){width=100 zoomable} |

{style="table-layout:fixed"}

### 基本的な画像テスト

width=200 （以下の表と比較）

![代替テキスト](assets/maui-dive.jpg "width = 200"){width=200}

width=50%（以下の表と比較）

![代替テキスト](assets/maui-flip.jpg "幅= 50%"){width=50%}

### ラップテスト ![代替テキスト](assets/package.png "右揃えの"){align="right"}

**位置揃えなし**

![代替テキスト](assets/maui-dive.jpg "width = 100"){width=100} マウイでのクリフダイビングは、人が思うほど難しくはありません。 本当に 4 つのステップでダイビングを行い、5 つのステップで安全なダイビングを行います。 最初に、崖から強く飛び出し、すぐに腕を伸ばし、足の指を指さす。 これはカメラのポーズです。 2 つ目は、体を合理的な着陸位置に動かすことです。 パニックに見えるかもしれませんが、単に感情に基づく調整に過ぎません。 3 つ目は体を傷つけない方法でスプラッシュします 4 つ目は何百万回もやったかのように立ち上がり少し退屈しています

**右揃え**

マウイでのクリフダイビングは、人が思うほど難しくはありません。 本当に 4 つのステップでダイビングを行い、5 つのステップで安全なダイビングを行います。 最初に、崖から強く飛び出し、すぐに腕を伸ばし、足の指を指さす。 これはカメラのポーズです。 2 つ目は、体を合理的な着陸位置に動かすことです。 パニックに見えるかもしれませんが、単に感情に基づく調整に過ぎません。 3 つ目は体を傷つけない方法でスプラッシュします 4 つ目は何百万回もやったかのように立ち上がり少し退屈しています ![代替テキスト](assets/maui-dive.jpg "100 幅の右揃え"){width="100" align="right"}

**左揃え**

![代替テキスト](assets/maui-dive.jpg "100 幅の左揃え"){width="100" align="left"} マウイでのクリフダイビングは、人が思うほど難しくはありません。 本当に 4 つのステップでダイビングを行い、5 つのステップで安全なダイビングを行います。 最初に、崖から強く飛び出し、すぐに腕を伸ばし、足の指を指さす。 これはカメラのポーズです。 2 つ目は、体を合理的な着陸位置に動かすことです。 パニックに見えるかもしれませんが、単に感情に基づく調整に過ぎません。 3 つ目は体を傷つけない方法でスプラッシュします 4 つ目は何百万回もやったかのように立ち上がり少し退屈しています

**右揃えで偽装**

マウイでの崖ダイビングは難しくありません。 ![代替テキスト](assets/maui-dive.jpg "100 幅の右揃え"){width="100" align="right"}

本当に 4 つのステップでダイビングを行い、5 つのステップで安全なダイビングを行います。 最初に、崖から強く飛び出し、すぐに腕を伸ばし、足の指を指さす。 これはカメラのポーズです。 2 つ目は、体を合理的な着陸位置に動かすことです。 パニックに見えるかもしれませんが、単に感情に基づく調整に過ぎません。 3 つ目は体を傷つけない方法でスプラッシュします 4 つ目は何百万回もやったかのように立ち上がり少し退屈しています


### 画像の整列

標準

![代替テキスト](assets/package.png "アイコンのテキストにマウスポインターを置く")

下に整列

![代替テキスト](assets/package.png "align=right"){align="right"}

右揃えインライン ![代替テキスト](assets/package.png "align=right"){align="right"}

中央の幅= 250

![代替テキスト](assets/maui-dive.jpg "align=center"){align=&quot;center&quot; width=250}

### 見出しの整列

**太字の見出し** ![代替テキスト](assets/package.png "align=right"){align="right"}

上記の太字の見出しを参照してください。

### テーブル内の画像

アイコンは右揃えで、ダイビング画像は 200 ピクセルを中央に配置し、フリップ画像は右に 50%を配置します。

| <center>左 | 中央 | 右</center> |
|---|---|---|
| ![代替テキスト](assets/package.png "align=right"){align=right} | ![代替テキスト](assets/maui-dive.jpg "align=center width=200"){align="center" width="200"} | ![代替テキスト](assets/maui-flip.jpg "align=right width=50%"){align="right" width="50%"} |

## 添付ファイル (EXLM-1124)

ダウンロード [PDF](/help/data-sheets/assets/BusinessSupportDatasheet.pdf)

ダウンロード [JS](assets/main.js)

ダウンロード [CSS](assets/main.css)

ダウンロード [TXT ファイル](assets/dots.txt)

ダウンロード [XLSX ファイル](assets/4-module_version.xlsx)

ダウンロード [ZIP ファイル](assets/2-Factor-Authentication-DataSource-and-FDM.zip)
