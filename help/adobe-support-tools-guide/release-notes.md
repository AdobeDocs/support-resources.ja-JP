---
title: 新しい EXL ケースフォームリリースノート
description: EXL ケースフォームの最新リリース情報です。
feature: Release Notes
source-git-commit: 421ef19ed939cd757e3182c8fa5bbda13fd7561e
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 8%

---


# 新しい EXL ケースフォームリリースノート

新しいケース作成エクスペリエンスでは、問題の解決を合理化するために設計された新しいフォームが導入されています。このフォームには、次のものが含まれます。

![新規](../adobe-support-tools-guide/assets/new.svg) - 新機能
![修正](../adobe-support-tools-guide/assets/fix.svg) - 修正点と改善点
![バグ](../adobe-support-tools-guide/assets/bug.svg) - 既知の問題

## リリース 1.0 - ケース作成フォームの強化

*2026年1月15日（PT）*

![&#x200B; 新規 &#x200B;](../adobe-support-tools-guide/assets/new.svg) ケースフォームはガイド付きフローで構成されており、各ステージで必要な情報を理解するのに役立ちます。

- [!UICONTROL &#x200B; 製品の選定 &#x200B;]
- [!UICONTROL &#x200B; 問題の詳細 &#x200B;]
- [!UICONTROL &#x200B; システム情報 &#x200B;]
- [!UICONTROL &#x200B; 影響 &#x200B;]
- [!UICONTROL &#x200B; 連絡先情報 &#x200B;]
- [!UICONTROL &#x200B; 確認して送信 &#x200B;]

![&#x200B; 新規 &#x200B;](../adobe-support-tools-guide/assets/new.svg) 実用的な詳細を取得し、トラブルシューティングを高速化するために、**新しい [!UICONTROL &#x200B; 再現する手順 &#x200B;] フィールド** を追加しました。

![&#x200B; 新規 &#x200B;](../adobe-support-tools-guide/assets/new.svg) 重要な詳細を取得する資格のある製品に **追加の [!UICONTROL &#x200B; 環境コンテキスト &#x200B;] フィールド** を追加しました。

- **Marketo**
   - Munchkin ID
- **Adobe Target**
   - アクティビティ名
   - サイト URL （タグプロパティ名）/HAR またはAssurance ログ
- **Adobe Analytics**
   - RSID
   - サイト URL （タグプロパティ名）/HAR またはAssurance ログ/cURL/デバッグログ
   - Workspace簡略リンク
- **Adobe Journey Optimizer（AJO）**
   - ジャーニー ID またはジャーニー URL
   - サンプルプロファイル
- **Real-Time Customer Data Platform（RTCDP）**
   - 影響を受けるコンポーネント ID （宛先 ID、プロファイル ID、オーディエンス ID、データセット ID、データフロー ID）
   - HAR ファイル/Assurance ログ
- **Customer Journey Analytics（CJA）**
   - Workspace プロジェクト
   - タグプロパティ名


![&#x200B; 新規 &#x200B;](../adobe-support-tools-guide/assets/new.svg) **AI 駆動の [!UICONTROL Recommendations Panel]** が追加され、ケース作成フローを中断することなく、役立つガイダンスを表示できるようになりました。

![&#x200B; 新規 &#x200B;](../adobe-support-tools-guide/assets/new.svg) 入力されたすべての情報の統合ビューを提供し、ユーザーが次のことができるようにする [!UICONTROL &#x200B; 概要のレビュー &#x200B;] 手順を追加しました。

- ケースの詳細を 1 か所でレビュー
- 前の手順に戻って編集します
- 進行状況を失わずに概要に戻る

![&#x200B; 修正 &#x200B;](../adobe-support-tools-guide/assets/fix.svg) わかりやすくするために、名前が「ケース説明」フィールドを *[!UICONTROL 「問題を説明してください」]* に変更しました。

![&#x200B; 修正 &#x200B;](../adobe-support-tools-guide/assets/fix.svg) 完全性を確保し、送信エラーを減らすために、必須フィールド指標としてアスタリスク（*）を追加しました。
