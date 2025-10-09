---
title: Adobe Success ポータルのリリースノート
description: ' [!DNL Adobe Success portal] の最新のリリース情報をご確認ください。'
feature: Release Notes
exl-id: be268e05-8298-4f21-8f2f-f66c52d76fe3
source-git-commit: 4a7f2142170b79b8024881144fa77ea4940c382c
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 36%

---

# [!DNL Adobe Success portal] リリースノート

このリリースノートには、[!DNL Adobe Success portal] の以下の更新内容が含まれています。

![新規](../adobe-success-portal/assets/new.svg) - 新機能
![修正](../adobe-success-portal/assets/fix.svg) - 修正点と改善点
![バグ](../adobe-success-portal/assets/bug.svg) - 既知の問題

## 3.0

_2025 年 10 月 9 日_

![ 新規 ](../adobe-success-portal/assets/new.svg) **[!UICONTROL アクションプラン]** モジュールにカレンダー表示を追加して、**[!UICONTROL 主要事業目標]** （KBO）にリンクされた **[!UICONTROL アクセラレーター]****[!UICONTROL アクティビティ]** のタイムラインを視覚化しました。
* アクションプラン KBO ページ、または **[!UICONTROL KBO]**/**[!UICONTROL Accelerator]**/**[!UICONTROL Activity]** 詳細ページ（KBO にリンクされている場合のみ）からカレンダーにアクセスします。
* リスト表示（デフォルト）とカレンダー表示を切り替えます。
* カレンダーには、各 KBO に対して折りたたみ可能なセクションが表示されます。
   * 青 **[!UICONTROL アクセラレータ]**
   * **[!UICONTROL アクティビティ]** が緑
* 各 **[!UICONTROL アクセラレーター]**/ **[!UICONTROL アクティビティ]** には、名前、ステータス、開始日/終了日（*Month XX*、*YYYY*）の形式で表示されます。
* イベントカードをクリックすると、イベントの詳細を含むページが開きます。 「戻る」ボタンをクリックすると、に戻ります。
* イベントは色分けされています。青色は **[!UICONTROL アクセラレーター]**、緑色は **[!UICONTROL アクティビティ]** です。 KBO を縦方向にスクロールし、週または月ごとに横方向にスクロールします。
* テキストが切り捨てられるとツールチップに完全な名前が表示され、スクロール中はタイムラインが表示されたままになります。
* デフォルトの表示は現在の週です。ナビゲーション矢印を使用して週間を移動できます。
* 月表示では、進行中の作業と予定されている作業の明確なタイムラインを提供します。

![ 修正 ](../adobe-success-portal/assets/fix.svg)**[!UICONTROL アクションプラン]** の **[!UICONTROL 主なビジネス目標]** および **[!UICONTROL アクティビティ]** ページを拡張して、完了日にツールチップを表示するようにし、タイムラインの可視性を向上させました。

![ 修正 ](../adobe-success-portal/assets/fix.svg) ナビゲーションを高速化するために、**[!UICONTROL アクションプラン]** および **[!UICONTROL 結果トラッカー]** のフィルター内に追加された検索。


![ 修正 ](../adobe-success-portal/assets/fix.svg) 簡単なコンテキストで、各検索結果にツールチップを追加しました。

![ 修正 ](../adobe-success-portal/assets/fix.svg) 調査結果と事例からダウンロードした PDF にAdobe ブランディングを追加しました。

![ 修正 ](../adobe-success-portal/assets/fix.svg) アカウントに関連付けられているすべての **[!UICONTROL 戦略的パートナー]** を、プライマリ連絡先の指標と共に表示します。

![ 修正 ](../adobe-success-portal/assets/fix.svg) **[!UICONTROL アラートとAdobeステータス]** のタイムゾーンが、ログインしたユーザーのプロファイルを正しく反映しなかった問題を修正しました。

![ 修正 ](../adobe-success-portal/assets/fix.svg) **[!UICONTROL アラートとAdobeステータス]** のフィルターが期待どおりに動作しない問題を修正しました。

![ 修正 ](../adobe-success-portal/assets/fix.svg) KBO の詳細ページと **[!UICONTROL 結果トラッカー]** ページの **[!UICONTROL ユースケース]** の並べ替えに一貫性がなかった問題を修正しました。

![ 修正 ](../adobe-success-portal/assets/fix.svg) ケースのタイトルにカーソルを合わせたときに、ケースリストページのツールチップにケース全体の名前が表示されない問題を修正しました。

![ 修正 ](../adobe-success-portal/assets/fix.svg)Safari ブラウザーで背面矢印アイコンが正しく表示されない問題を修正しました。

## 2.0

_2025年9月11日（PT）_

![新規](../adobe-success-portal/assets/new.svg)次のフィールドを&#x200B;**[!UICONTROL アクティビティの詳細]**&#x200B;ページに追加しました。

* **[!UICONTROL 優先度]**：アクティビティの優先度レベルを示します。使用可能な値は、*緊急*、*高*、*標準*、*低*、*なし*&#x200B;です。値が&#x200B;*なし*&#x200B;の場合、「**[!UICONTROL 優先度]**」フィールドはポータルの UI に表示されません。
* **[!UICONTROL アドビ所有者]**：アクティビティに対して指定されたアドビオーナーを表示します。
* **[!UICONTROL クライアント所有者]**：顧客側の所有者を表示します。
* **[!UICONTROL 次の手順]**：アクティビティに対してキャプチャされた次のアクションを表示します。
* **[!UICONTROL アドビソリューション]**：アクティビティに関連するアドビソリューションを示します。

![修正](../adobe-success-portal/assets/fix.svg) **[!UICONTROL アクションプラン]**&#x200B;内の&#x200B;**[!UICONTROL 主要ビジネス目標]**&#x200B;および&#x200B;**[!UICONTROL アクティビティ]**&#x200B;ページを拡張し、アクセラレーターとアクティビティのそれぞれの完了日を表示し、タイムラインの可視性を向上させました。

![修正](../adobe-success-portal/assets/fix.svg) **[!UICONTROL KBO の詳細]**&#x200B;ページの&#x200B;**[!UICONTROL ユースケース]**&#x200B;の表示方法を改善し、より洗練されたデザイン、優れた操作性、一貫したナビゲーションを実現しました。

![修正](../adobe-success-portal/assets/fix.svg) **Ctrl + クリック**（または Mac で **Command + クリック**）しても新しいタブでリンクが開かない問題を修正しました。
