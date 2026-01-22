---
title: 新しいExperience League ケースフォームリリースノート
description: EXL ケースフォームの最新リリース情報です。
feature: Release Notes
source-git-commit: 7bca9c4ae25c77092de6957193ceecd146d19a1a
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 8%

---


# 新しいExperience League ケースフォームリリースノート

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

![新規](../adobe-support-tools-guide/assets/new.svg) 実用的な詳細をキャプチャし、トラブルシューティングを迅速化するための **新規 [!UICONTROL 再現の手順] フィールド** を追加しました。

![新規](../adobe-support-tools-guide/assets/new.svg) 重大な詳細を取り込むために、資格のある製品の **追加の [!UICONTROL 環境コンテキスト] フィールド** を追加しました。

- **Marketo**
   - Munchkin ID
- **Adobe Target**
   - アクティビティ名
   - サイト URL （タグプロパティ名）/HAR またはAssurance ログ
- **Adobe Analytics**
   - RSID
   - サイト URL （タグプロパティ名）/HAR またはAssurance ログ/cURL/デバッグログ
   - ショートリンクワークスペース
- **Adobe Journey Optimizer（AJO）**
   - ジャーニー ID またはジャーニー URL
   - サンプルプロファイル
- **Real-Time Customer Data Platform（RTCDP）**
   - 影響を受けるコンポーネント ID （宛先 ID、プロファイル ID、オーディエンス ID、データセット ID、データフロー ID）
   - HAR ファイル/Assurance ログ
- **Customer Journey Analytics（CJA）**
   - Workspace プロジェクト
   - タグプロパティ名


![新規](../adobe-support-tools-guide/assets/new.svg) ケース作成フローを中断することなく役立つガイダンスを表示するための **AI 駆動型 [!UICONTROL Recommendationsパネル]** が追加されました。

![新規](../adobe-support-tools-guide/assets/new.svg) [!UICONTROL レビュー概要] ステップを追加して、入力したすべての情報を統合表示を提供し、ユーザーが次のことを行えるようにするようになりました。

- ケースの詳細を 1 か所で確認する
- 前の手順に戻って編集します
- 進行状況を失わずに概要に戻る

![&#x200B; 修正 &#x200B;](../adobe-support-tools-guide/assets/fix.svg) わかりやすくするために、名前が「ケース説明」フィールドを *[!UICONTROL 「問題を説明してください」]* に変更しました。

![&#x200B; 修正 &#x200B;](../adobe-support-tools-guide/assets/fix.svg) 完全性を確保し、送信エラーを減らすために、必須フィールド指標としてアスタリスク（*）を追加しました。
