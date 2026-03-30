---
title: Experience League サポートリリースノート
description: Experience League サポートに関する最新リリース情報。
feature: Release Notes
source-git-commit: 25bfd2450594c3fbb361cb80fe16e1a438f73b89
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 4%

---


# Experience League サポートリリースノート

このリリースノートには、Experience League サポートのアップデートが含まれており、次の内容が含まれています。

![新機能](../adobe-support-tools-guide/assets/new.svg)
![修正](../adobe-support-tools-guide/assets/fix.svg)修正と機能強化
![&#x200B; バグ &#x200B;](../adobe-support-tools-guide/assets/bug.svg)既知の問題

## 2026年3月30日 – Enhanced Case Form

![新規](../adobe-support-tools-guide/assets/new.svg) ケースフォームは、ユーザーが各段階で必要な情報を理解するのに役立つガイド付きフローに整理されています。

- [!UICONTROL 製品の選択]
- [!UICONTROL 問題の説明]
- [!UICONTROL &#x200B; システム情報]
- [!UICONTROL 優先度とビジネスへの影響]
- [!UICONTROL 連絡先情報と視聴者リスト &#x200B;]
- [!UICONTROL &#x200B; レビューして送信]

![新規](../adobe-support-tools-guide/assets/new.svg) **[!UICONTROL 問題の説明]**&#x200B;に基づいてタイトルを自動的に生成できるようになりました。これにより、ユーザーはケースを送信する前にタイトルを編集できます。

![新規](../adobe-support-tools-guide/assets/new.svg)さんが&#x200B;**[!UICONTROL を追加しました「問題は再現可能ですか？」トラブルシューティングの改善に役立つ]** オプション。 ユーザーが&#x200B;**[!UICONTROL Yes]**&#x200B;を選択すると、問題を再現するために実行した手順を入力するように求められます。 *No*&#x200B;が選択されている場合、ユーザーはケースの提出を進めることができます。

![新規](../adobe-support-tools-guide/assets/new.svg)環境またはインスタンスに最近変更が加えられたかどうかを示すオプションを追加しました。 **[!UICONTROL はい]**&#x200B;が選択されている場合、変更に関する追加情報を入力するように求められます。

![新規](../adobe-support-tools-guide/assets/new.svg)さんが、重要な詳細をキャプチャするために、使用権限のある製品に&#x200B;**追加の[!UICONTROL 環境コンテキスト &#x200B;] フィールド**&#x200B;を追加しました：

- **Marketo**
   - Munchkin ID
- **Adobe Target**
   - アクティビティ名
   - サイト URL （タグプロパティ名）
- **Adobe Analytics**
   - RSID
   - サイト URL （タグプロパティ名） / cURL
   - Workspace Shortlink
- **Adobe Journey Optimizer（AJO）**
   - ジャーニーID、URL/Campaign ID、URL/Channel ID、URL/Offer Decisioning IDまたはURL
   - プロファイル例
   - サンドボックス名
- **Real-Time Customer Data Platform （RTCDP）**
   - 影響を受けるコンポーネント ID （宛先ID/オーディエンス ID/データセット ID/データフローID/結合ポリシーID/スキーマ ID/Source ID/バッチ ID）
   - プロファイル例
   - サンドボックス名
- **Adobe Experience Platform（AEP）**
   - 影響を受けるコンポーネント ID （宛先ID/オーディエンス ID/データセット ID/データフローID/結合ポリシーID/スキーマ ID/Source ID/バッチ ID）
   - プロファイル例
   - サンドボックス名
- **Customer Journey Analytics （CJA）**
   - Workspace プロジェクト URL
   - 接続ID / エラーメッセージ / コード
   - データビューID

![新規](../adobe-support-tools-guide/assets/new.svg) ケース作成フローを中断せずに役立つガイダンスを表示するために、**AIを活用した[!UICONTROL &#x200B; レコメンデーションパネル]**&#x200B;を追加しました。

![新規](../adobe-support-tools-guide/assets/new.svg)入力したすべての情報の統合ビューを提供し、ユーザーが次のことを実行できるようにするために、**[!UICONTROL 概要の確認]**&#x200B;手順を追加しました。

- ケースの詳細を1か所で確認する
- 前の手順に戻って編集します
- 進捗を見失うことなく概要へ戻る

![修正](../adobe-support-tools-guide/assets/fix.svg) ケースの説明フィールドの名前を&#x200B;*[!UICONTROL に変更しました「問題を説明してください」]*&#x200B;で、わかりやすくしました。

![修正](../adobe-support-tools-guide/assets/fix.svg)完全性を確保し、送信エラーを減らすために、必須のフィールドインジケーターとしてアスタリスク （*）を追加しました。

## 2026年3月18日 – コールバック機能のリクエストの拡張

Experience Leagueでは、コールバックのリクエストオプションが提供され、画面共有機能を使用してセルフサービスのweb ミーティングスケジュールを有効にし、問題解決を迅速化できるようになりました。
- この機能は、Adobe Experience Manager、Campaign、Workfrontで利用できます。
- 顧客は都合の良いタイミングでミーティングを予約し、瞬時に招待状を受け取ることができます。
- Adobe Experience Manager P1の場合、すぐにコールバックをおこなうことで、重要な問題が発生した際のエンゲージメントを加速し、ダウンタイムとビジネスへの影響を最小限に抑えることができます。
