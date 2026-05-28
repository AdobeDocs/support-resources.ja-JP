---
title: Adobe DX Solutions Unified Holiday Readiness Guide
description: AEP、AJO、CJA、Commerce、AEM、Marketo、Workfront、Campaign、Analytics、Target向けのAdobe DXのホリデーシーズンの準備状況を確認し、計画、拡張、セキュリティの確保、最適化を支援します。
feature-set: Experience Cloud
feature: Support
solution: Experience Cloud, Experience Platform, Journey Optimizer, Customer Journey Analytics, Commerce, Experience Manager, Workfront, Campaign, Analytics, Target, Marketo Engage
role: Developer, Admin, Leader, User
index: true
exl-id: 7a36a281-98d0-4b1f-afc5-dbcde10fddaf
source-git-commit: bbc1d3c0a0436a36d55adac14bb354fe0ecf96da
workflow-type: tm+mt
source-wordcount: '4803'
ht-degree: 3%

---

# Adobe DX Solutions Unified Holiday Readiness Guide


Adobe DX Solutions Unified Holiday Readiness Guideでは、事後的な問題解決ではなく、積極的なプランニングに重点を置くことで、ホリデーシーズンの準備に役立ちます。 インスタンスの準備を整えるための実用的なステップを提供し、潜在的な問題が発生する前に最小限に抑えます。 Adobeチームは、技術的な専門知識、幅広い能力、適切なレベルのサポートとガイダンスを提供するための実証済みの手法など、技術的にも戦略的にも優れたサービスを提供し、ビジネスの準備を整えます。

Adobeのデジタルエクスペリエンスソリューションが、回復力と安全性を備え、ホリデートラフィックのピークに対応していることを確認するには、次のベストプラクティスに従ってください。

* トラフィックの増加に備える：
* 繁忙期における大きな変化を回避し、ホリデーシーズンの前後にアップデートをスケジュールします。
* ダッシュボードとアラートを使用して、パフォーマンスを監視し、ボトルネックを早期に検出します。
* 承認済みのサポート担当者が最新であることを確認します。
* [可能な限り、事前にAdobe サポート &#x200B;](https://experienceleague.adobe.com/ja/docs/learning-manager/using/faq/how-to-submit-support-ticket)にお問い合わせください。

Adobeのソリューション固有の休暇準備状況に関する推奨事項については、次の節を参照してください。

* [Adobe Experience Platform](#aep)
* [Adobe Journey Optimizer](#ajo)
* [Adobe Customer Journey Analytics](#cja)
* [Adobe Commerce](#commerce)
* [Adobe Experience Manager](#aem)
* [Adobe Marketo](#marketo)
* [Adobe Workfront](#workfront)
* [Adobe Campaign](#campaign)
* [Adobe Analytics](#analytics)
* [Adobe Target](#target)

>[!NOTE]
>
>各セクションをクリックして展開します。


## Adobe Experience Platform（AEP）ホリデーシーズン対応ガイド {#aep}

+++**クリックすると、Adobe Experience Platform（AEP）の休暇準備に関する推奨事項が表示されます。**

Adobe Experience Platform（AEP）は、リアルタイムの顧客体験を強化するうえで、重要な役割を果たします。 ホリデーシーズンが近づくにつれ、トラフィックの増加、安全なデータ処理、スケーラブルな取り込みのために、AEPの実装を最適化することが不可欠です。

### 季節需要の予測

季節的なトラフィックの急増に備えるために、Adobeでは、キャパシティの計画とストリーミングプロファイルの取り込みのモニタリングを推奨しています。 これには、データ量を予測し、システムがスループットの向上に対応できるようにすることも含まれます。 [&#x200B; キャパシティとシーズントラフィックのプラン &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/dataflows/ui/monitor-streaming-profile)を参照してください。

### 拡張の準備

Adobeでは、お客様の環境がホリデートラフィックに対応できるよう、いくつかの対策を用意しています。

* サンドボックスの割り当て容量を増やします。
* [監視ダッシュボード &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/dataflows/ui/monitor-streaming-profile)で高スループットデータフローを特定し、必要に応じてスロットルまたはフィルタリングを適用します。
* [&#x200B; ライセンスの使用状況と容量：ストリーミングスループットのベストプラクティス &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/landing/license/capacity#suggestions)の説明に従って、パフォーマンスを最適化するために、バッチ取り込みを低遅延のユースケースに使用します。

これらのプラクティスは、取り込みの信頼性を維持し、ピーク時の待ち時間を短縮するのに役立ちます。

### ベストプラクティスとガードレール

運用上の制限内に収まり、サービスの中断を回避するために、Adobeでは次の取り込みとプロファイルガードレールをお勧めします。

* [ストリーミングスループットのベストプラクティス](https://experienceleague.adobe.com/ja/docs/experience-platform/landing/license/capacity#suggestions)
* [データ取り込みのガードレール](https://experienceleague.adobe.com/ja/docs/experience-platform/ingestion/guardrails)
* [リアルタイム顧客プロファイルデータとセグメンテーションのデフォルトガードレール](https://experienceleague.adobe.com/ja/docs/experience-platform/profile/guardrails)
* [AEP ブループリント：ガードレール](https://experienceleague.adobe.com/ja/docs/blueprints-learn/architecture/architecture-overview/guardrails)

### セキュリティとガバナンス

Adobeでは、特にデータの機密性が高いトラフィックの多いシーズンには、強力なセキュリティとガバナンスの実践を重視しています。

AEPの実装全体で顧客データを保護し、プライバシー制御を適用し、コンプライアンスを維持する方法に関する推奨事項については、[Adobe Experience Platformのガバナンス、プライバシー、セキュリティ &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/landing/governance-privacy-security/overview#security)を参照してください。

これらのガイドラインに従い、Adobeの公開ドキュメントを活用することで、Adobe Experience Platformのレジリエンスとセキュリティを確保し、ホリデーシーズンを通じて優れた顧客体験を提供する準備を整えることができます。

+++

## Adobe Journey Optimizer（AJO）ホリデーシーズン対応ガイド {#ajo}

+++**クリックすると、Adobe Journey Optimizer（AJO）の休暇準備に関する推奨事項が表示されます。**


Adobe Adobe Journey Optimizerを活用して、ホリデーシーズンに備えるためには、イベントの急増やクロスチャネルの複雑さを予測し、ジャーニーと頻度のルールを設定して、データの健全性と意思決定ロジックを確保する必要があります。 また、大規模なパフォーマンスを検証し、セキュリティとAPIのガードレールを徹底し、ピーク後のインサイトを適用して将来のキャンペーンを洗練させる必要もあります。

### 需要の予測

* ホリデーシーズンの圧縮率とキャンペーン量の増加にもとづいて、次の要素を期待します。
   * リアルタイムのイベントとトリガージャーニーの急増（カート放棄、直前のオファー）
   * メッセージの飽和リスク（オプトアウト率の向上、顧客の疲労）
   * クロスチャネルの複雑さの向上（電子メール + プッシュ通知+ SMS + アプリ内）
* 過去1年間の指標（開封率/クリック率/オプトアウト率、ジャーニー入力量）を使用して、メッセージシステムの予想される読み込みをモデル化し、しきい値を設定します。
* 「静かな時間帯」やパフォーマンスの低い時間帯（たとえば、週末、休日）を特定し、それに応じて配信数を計画します。

### 拡張の準備

* AJOのすべてのチャネル設定が適切に設定されていることを確認します（メール、プッシュ、SMS、web、アプリ内）。 「[&#x200B; チャネル設定の設定](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/configuration/channel-surfaces)」を参照してください。
* 頻度の上限と上限のルールを設定して、メッセージボリュームを制御します。 [頻度の上限](https://experienceleague.adobe.com/ja/docs/journey-optimizer-learn/tutorials/configuration/business-rules/configure-frequency-capping-rules)の記事を参照してください。
* チャネル/ジャーニーのルールセットの設定：[&#x200B; ルールセットの操作](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets)を参照してください。
* データの健全性を保つ/リアルタイムのイベントストリームとセグメンテーションフレームワークを準備する。
* 次のようなホリデーキャンペーンのターゲットオーディエンスを定義していることを確認します。
   * 有望個客
   * 優良顧客セグメント
   * cart-abandoners
   * 初回購入者
* ホリデージャーニーのテンプレートをプリロードまたは準備し、意思決定ロジック（オファー/制約）を活用して、在庫、時間制限のあるオファー、チャネルの好みにもとづいて動的に適応させます。 [&#x200B; オファーに制約を追加](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/decisioning/offer-decisioning/managing-offers-in-the-offer-library/configure-offers/add-constraints)の記事の例を参照してください。
* 技術的準備状況：API/エンドポイントの読み込み容量、カスタムアクションおよび外部統合のスロットル/キャッピングルールを確認します。 [&#x200B; ガードレールと制限](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/get-started/guardrails)を参照してください。

### 検証

* 実験フレームワークを使用して、主要な変数の変更をテストします。
   * 送信時間
   * オファータイプ
   * チャネルミックス
[AJO Experimentation Acceleratorのベストプラクティス &#x200B;](https://experienceleague.adobe.com/ja/docs/experimentation-accelerator/using/get-started/experiment-accelerator-best-practices)を参照してください。
* エンドツーエンドのジャーニー検証の実施：
   * イベントトリガー
   * セグメント化エントリ
   * ジャーニーパスフロー
   * パーソナライゼーションロジック
   * オファーの制約
   * 出口基準
* キャッピングルールと競合ルールを確認します。 [ジャーニーの上限設定と調停](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/conflict-prioritization/journey-capping)の記事を参照してください。
* ピーク時の送信またはスパイクに対するストレステストのスケーリングされたボリューム：高トリガーボリュームをシミュレートして、負荷時のシステム動作を検証します。
* 配信品質の検証：電子メールのドメイン/送信者をウォームアップし、モバイルプッシュ設定を確認し、SMS/アプリ内のフォールバックチャネルをチェックします。

### ベストプラクティス

* オムニチャネルオーケストレーション。 AJOのホリデーシーズンの例を紹介したブログ [&#x200B; エンゲージメントと成長に不可欠なオムニチャネルカスタマージャーニー](https://business.adobe.com/jp/blog/essential-customer-journeys-for-omnichannel-engagement)の記事を参照してください。
* 必要に応じて、リアルタイムのトリガーに優先順位を付ける： 例：買い物客の反応が高いほど、カートの放棄、放棄の閲覧、在庫アラートを送信する
* セグメンテーションとパーソナライゼーションを活用する：インテントの高いセグメントをターゲットにし、過去の購買行動や嗜好にもとづいてオファーをカスタマイズします。
* メッセージの疲労を最小限に抑える：過剰な勧誘を避けるために、上限とサイレントアワーを実施します。 AJO[&#128279;](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/elevate-customer-experience-with-daily-frequency-capping-in-ajo/ba-p/761510?profile.language=ja)のブログ記事で、日次の配信頻度の上限を設定して顧客体験を向上させるを参照してください。
* タイミングが重要：プランでは、ホリデーウィンドウ（圧縮されたシーズンを考慮）で配信を早め、タイムゾーンや地域のオーディエンスの行動に合わせてチャネルを調整します。
* 動的なオファーや期間限定のオファーを提供することで、緊急性を高めつつ、チャネルをまたいで調整し、オファーの重複や競合を回避します。
* 抑制ロジックを使用する：購入したばかりのオーディエンスを抑制するか、冗長なメッセージを避けるために購入後のジャーニーを適用します。

### セキュリティとガバナンス

* アクセス制御と権限が設定されていることを確認し、必要なユーザーのみがジャーニーをデプロイしたり、ビジネスルールを変更したりできるようにします。
* API呼び出し/接続の上限を監視して適用します。例えば、[Capping API | Adobe Journey Optimizer](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/connect-systems/external-systems/capping)を参照してください。
* クリーンな1st パーティデータを使用し、適切なIDをつなぎ合わせることで、メッセージが顧客中心となり、重複や不整合を防ぎます。
* 配信品質ドメインのウォームを徹底し、特に大量のバリエーション送信に対してスパム対策を講じます。
* 監査ログとジャーニーの変更を繁忙期に頻繁に確認し、ミス実行やエラージャーニーを早期に検出します。

### ピーク後の学習

* ピーク時の読み込み後、ジャーニーのエントリ数、抑制カウント、オプトアウト率、配信品質の指標、チャネルパフォーマンスを確認します。
* 抑制されたセグメントをクリーンアップし、休暇ウィンドウ用に構築されたジャーニーを一時停止または削除して、引き継ぎの疲労を回避します。
* リアルタイムのパフォーマンスから得られるインサイトを活用して、来年の計画を改善します（例：送信時間の調整、チャネルミックス、メッセージ量）。

季節ごとの需要を先見的に予測し、チャネルやルールの設定を行い、ジャーニーのパフォーマンスを検証し、セキュリティとガバナンスを強化することで、Adobe Journey Optimizerが今年だけでなく、今年もシームレスでパーソナライズされた回復力のある顧客体験を提供できるようにします。

+++

## Customer Journey Analytics（CJA）ホリデーシーズン対応ガイド {#cja}

+++**クリックすると、Customer Journey Analytics（CJA）の休暇準備に関する推奨事項が表示されます。**

Customer Journey Analyticsでは、5P法を適用して、ホリデーシーズンやピークシーズンの準備態勢を整えます。

### 拡張の準備

* CJAの接続とデータビューを確認し、監視とプロビジョニングを強化する必要がある接続とデータビューを設定します。
* ホリデースケールにはプロビジョニングで十分であることを確認し、必要に応じてクリティカル接続とデータビューをアップスケールします。 詳しくは、[接続の管理](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-connections/manage-connections)を参照してください。

### パフォーマンスを監視

* RAM （[[!UICONTROL Reporting Activity Manager]概要](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-overview)）を活用して、アクティブなレポートリクエストとキューに入れられたレポートリクエストをリアルタイムで監視し、容量に応じた接続を特定し、ボトルネックを検出します。
* [&#x200B; エラーとトラブルシューティング ガイド &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-workspace/workspace-faq/error-messages)および[既知の制限事項](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-workspace/workspace-faq/aw-limitations)の記事を使用して、ピーク時の読み込み中に遅延が増加することを確認します。
* 管理者は、RAM経由で長時間実行またはブロックされたリクエストを先制的に一時停止またはキャンセルできます。 CJA[&#128279;](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-cancel-requests)の「 レポートのキャンセル」を参照してください。

### ベストプラクティス

* 低トラフィック期間に書き出し/レポートをスケジュールして、読み込みをスムーズにし、遅延を最小限に抑えます。 [&#x200B; スケジュール済みレポート &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-components/scheduled-projects-manager)の記事を参照してください。
* リクエストの分散：1日を通して異なる間隔でレポートをスケジュールします。
* パネルを削減し、セグメントを簡素化し、日付範囲を短縮して、過剰な同時作業を回避します。 詳しくは、[CJA Workspaceのパフォーマンスの最適化](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-workspace/workspace-faq/optimizing-performance)の記事を参照してください。

### トラブルシューティング

* ワークスペースのエラーをトラブルシューティングする場合は、原因と推奨されるアクションについてエラーメッセージを参照してください。RAM （[!UICONTROL Reporting Activity Manager]）を使用して、ボトルネックをクリアし、同時実行を効果的に管理してください。 詳しくは、[CJA Workspace エラー処理](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-workspace/workspace-faq/error-messages)を参照してください。
* RAM （[[!UICONTROL Reporting Activity Manager] in CJA](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-overview)）を使用して、問題のあるユーザー、クエリ、またはプロジェクトを特定します。必要に応じて優先順位を付け、終了/キャンセルします。

### ピーク後の学習

* ホリデーシーズン/ピーク期間の後、パフォーマンスとインシデントログを確認して、提供されたベストプラクティスの影響を評価します。
* 進行の遅いクエリやユーザータスクを確認して、来シーズンに最適化できるパターンやトレンドを特定します。
* ユーザーや関係者からフィードバックを収集し、新たに獲得したインサイトを基に、独自のランブックと準備計画を更新します。
* アカウントチームを介してAdobe チームにフィードバックを提供します。

+++

## Adobe Commerceホリデーシーズン対応ガイド {#commerce}

+++**クリックすると、Adobe Commerceの休暇準備に関する推奨事項が表示されます。**

自社の繁忙期を成功させるには、Adobe Commerceデジタルストアフロントが高トラフィックに対応できるように準備することが不可欠です。

### 需要の予測

* ホリデーシーズン（11月中旬から1月中旬）には、Adobeでは、クラウドインフラストラクチャでホストされているすべてのAdobe Commerce加盟店が、ホリデーサージキャパシティリクエストを送信することで、訪問者の増加を積極的に計画することをお勧めします。 詳しくは、[&#x200B; クラウドインフラストラクチャ上のAdobe Commerceのホリデーサージキャパシティのリクエスト &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-knowledge-base/kb/announcements/commerce-announcements/holiday-surge-capacity-requests-for-magento-commerce-cloud)を参照してください。

### 拡張の準備

「[計画と方向転換：繁忙期2025](https://experienceleague.adobe.com/ja/perspectives/planning-and-pivoting-a-strategic-approach-to-peak-season-2025)の戦略的アプローチ」の推奨事項に従います。このガイドでは、Adobe Commerce（およびオプションのAdobe Experience Cloud ツール）を使用して実用的な戦略を提供し、最も混雑する時期に優れた顧客体験を計画、方向転換、提供するのに役立ちます。

### ベストプラクティス

* Adobeのガイド [高トラフィックに対応するためのインフラストラクチャの準備方法（繁忙期のパフォーマンスの5 P） &#x200B;](https://business.adobe.com/blog/how-to/the-5-ps-of-peak-season-performance-a-guide-to-preparing-your-infrastructure-for-high-traffic)。
* Commerceの休暇期間中のインフラストラクチャを高トラフィックに備え、ダウンタイムを防ぎ、パフォーマンスを最適化する方法に関するヒントについては、[の休暇準備に関する技術のヒント &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-knowledge-base/kb/how-to/tech-tips-for-commerce-holiday-readiness)を参照してください。

+++

## Adobe Experience Manager（AEM）ホリデーシーズン対応ガイド {#aem}

+++**クリックすると、Adobe Experience Manager（AEM）の休暇準備に関する推奨事項が表示されます。**

ホリデーシーズンが急速に近づいており、多くのAdobeのお客様にとって、これは繁忙期の始まりを示しています。 お客様の成功に対する当社の取り組みとして、お客様が今後急増するトラフィックに十分に備えていることを確認したいと考えています。

### Adobe Experience Manager （AEM） Cloud Services

ホリデーシーズンに最も混雑する瞬間に遭遇した場合は、ピーク時のトラフィックに対応するために、Adobe Experience Managerサイトを最適化する方法を検討しているかもしれません。 幸いなことに、Adobe Experience Manager Cloud Servicesには自動拡張する機能が既に備わっており、トラフィックが急激に変化しても、訪問者にはシームレスな体験を提供できます。

#### 拡張の準備

* Adobe Experience Manager Cloud Servicesを使用して高トラフィックに対応するための詳細なインサイトとガイダンスについては、次のリンクを参照してください。

   * [AEM as a Cloud Service での CDN](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/implementing/content-delivery/cdn)
   * [AEM as a Cloud Serviceのキャッシュ](https://experienceleague.adobe.com/ja/docs/experience-manager-learn/cloud-service/caching/overview)

* Ultimate Successをご利用のお客様で、最近Adobe アカウントチームと配信数の予測情報を共有した場合は、既にビューがあるので、もう一度お送りいただくことについて心配する必要はありません。

私たちはあなたの旅のあらゆる段階であなたをサポートするためにここにいます。 ご質問や懸念がある場合は、[&#x200B; サポートチケットを送信してください](https://experienceleague.adobe.com/ja/docs/learning-manager/using/faq/how-to-submit-support-ticket)。

ホリデーシーズンにマーケティングキャンペーンを準備するには、[AEMaaCS ユーザーガイド：概要 – マーケティングキャンペーンパラメーター](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/implementing/content-delivery/caching#marketing-parameters)のドキュメントを参照してください。

#### セキュリティとガバナンス

AEM web サイトのトラフィックセキュリティ/保護について詳しくは、AEM as a Cloud Service チュートリアルの「[概要 – AEM web サイトの保護](https://experienceleague.adobe.com/ja/docs/experience-manager-learn/cloud-service/security/traffic-filter-and-waf-rules/overview)」を参照してください。

#### ホリデーメンテナンス計画

Adobeでは、重要な休暇期間に中断のないサービスを保証するために、メンテナンスの対象外期間を設定しています。

* **次の間に自動更新は行われません**:
   * 2025年11月24日～2025年12月2日
   * 2025年12月15日～2026年1月2日

これにより、トラフィックの多い時間帯での安定性が確保されます。 完全なリリーススケジュールとメンテナンスウィンドウについては、[AEM リリースロードマップ &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-manager-release-information/aem-release-updates/update-releases-roadmap)を参照してください。


### Adobe Experience Manager（AEM）とAdobe Managed Services（AMS）

Adobe Managed Servicesを活用しているAEMのお客様は、CSEと積極的に連携して、ホリデーシーズンのカバレッジのニーズに対応することができます。

+++

## Adobe Marketoのホリデーシーズン向けガイド {#marketo}

+++**クリックすると、Adobe Marketoの休暇準備に関する推奨事項が表示されます。**

Adobe Marketoを活用して、ホリデーキャンペーンを成功させるためには、メール認証の設定、データベースのクリーニングと保護、キャンペーンロジックとスケジューリングの最適化、メールのレンダリングと配信品質の徹底的なテスト、ピーク時のパフォーマンスとエンゲージメントを実現するためのサポート準備の合理化を実現する必要があります。

### 拡張の準備

* SPF/DKIMの設定を確認し、すべての設定が正しく動作していることを確認します。 詳しくは、「[&#x200B; メール配信のSPFとDKIMの設定](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-spf-and-dkim-for-your-email-deliverability)」を参照してください。
* 非アクティブ/無効なレコードをパージして、Marketo データベースを監査およびクリーニングします。 これにより、電子メールが最も多くのリードの受信トレイに届く可能性が高まります。 詳しくは、[Marketo データベースのヘルスチェックとクリーンを維持する方法](https://nation.marketo.com/t5/champion-program-blogs/marketo-database-health-check-up-amp-how-to-keep-it-clean/ba-p/323563)の記事を参照してください。
* チームメンバーがタスクを実行し、意図しないアクセスやメールの変更を防ぐための適切な権限を持っていることを確認します。 **[!UICONTROL 管理者]**&#x200B;または&#x200B;**[!UICONTROL Admin Console]**&#x200B;を通じて変更を行う場合でも、対応できます。 [&#x200B; ユーザーの役割と権限の管理](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/administration/users-and-roles/managing-user-roles-and-permissions)の記事を参照してください。
* Launchpadの統合を確認して、正しい認証を確認し、潜在的なエラーを使用する前に解決します。 [Marketo Developer Guide: Authentication](https://experienceleague.adobe.com/ja/docs/marketo-developer/marketo/rest/authentication)を参照してください。

### ベストプラクティス

Marketoがキャンペーンの優先順位やプロセスをどのように正確に把握することから始まります。 最適化のヒントで、キャンペーンにスピードのギフトを与えましょう。

* Marketoでキャンペーンフローの各段階の処理の優先順位を把握することは、緊急メールや優先度の高いメールを誤って配信してしまうことを防ぐために非常に重要です。 [&#x200B; キャンペーン処理の仕組み](https://nation.marketo.com/t5/knowledgebase/how-campaign-processing-works/ta-p/248264)の記事を参照してください。
* スマートリストロジックを念頭に置くことで、キャンペーンを迅速かつピーク時にパフォーマンスを確保することができます。 「[&#x200B; スマートリストのベストプラクティス &#x200B;](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/creating-a-smart-list/best-practices-for-smart-lists)」の記事を参照してください。
* **[!UICONTROL Head Start]**&#x200B;または&#x200B;**[!UICONTROL 受信者タイムゾーン]**&#x200B;は、送信前にメールの作成を開始でき、遅延を減らし、リソースロジックが高いリードの選定に追加の準備時間を提供できます。 詳しくは、[電子メールプログラムの先行スタート &#x200B;](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/email-marketing/email-programs/email-program-actions/head-start-for-email-programs)および[受信者のタイムゾーンを使用した電子メールプログラムのスケジュール &#x200B;](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/email-marketing/email-programs/email-program-actions/scheduling-with-recipient-time-zone/schedule-email-programs-with-recipient-time-zone)の記事を参照してください。
* キャンペーンがアクティブになり、リードが流入すると、フローステップの間違いに気が付きます。 迅速な調整で修正したいと考えがちですが、ライブ待機ステップを変更したり、フローを並べ替えたりすると何が起こるかを知ることで、多くの頭痛を避け、後でクリーンアップすることができます。 待機手順[&#128279;](https://nation.marketo.com/t5/knowledgebase/editing-campaign-flow-with-members-in-wait-steps/ta-p/254294)の記事の「 メンバーを含むキャンペーンフローの編集」を参照してください。

### 検証

**[!UICONTROL Send]**&#x200B;をクリックする前に、電子メールの表示とパフォーマンスが意図したとおりに行われていることを確認してください。

* Marketoでは、電子メールの外観をテストし、思い描いたとおりに表示することを確認する方法をいくつかご用意しています。
   * **[!UICONTROL Preview]**&#x200B;関数を使用して、セグメント化または個々のリードによるプレビューによって、動的コンテンツとトークンが正しくレンダリングされていることを確認します。 動的コンテンツを含むメールのプレビュー[記事](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/email-marketing/general/functions-in-the-editor/preview-an-email-with-dynamic-content)を参照してください。
   * テストレコードにダイレクトメールをすばやく簡単に送信し、様々なクライアントやデバイスでメールがどのように表示されるかを確認できます。 「[&#x200B; スマートリストから単一フローステップを実行する](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/using-smart-lists/run-a-single-flow-step-from-a-smart-list)」の記事を参照してください。
   * [!DNL Litmus] ユーザーの場合、アカウントを統合し、メールエディターから直接レンダリングテストを開始することが、これまで以上に簡単になりました。  [!DNL Litmus][&#128279;](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/email-marketing/email-designer/test-email-rendering)の記事「 メールのレンダリングをテストする」を参照してください。
* [!DNL SpamAssassin]と統合された電子メールスパムレポート機能を確認して、電子メールの内容を確認し、受信トレイに届く可能性や&#x200B;*スパム*&#x200B;としてマークされる可能性についてスコアを割り当てます。 [電子メールスパムレポート &#x200B;](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/email-marketing/email-designer/spam-report)の記事を参照してください。
* [!UICONTROL &#x200B; キャンペーンキュー]に注目して、キャンペーンが処理され、緊急度の高い項目が正しく優先順位付けされていることを確認します。 「[&#x200B; キャンペーンは実行中ですか？](https://nation.marketo.com/t5/knowledgebase/is-my-campaign-running/ta-p/248662)」を参照してください。 ガイド。

### サポートエクスペリエンスの効率化

何か問題が発生した場合は、スピードが重要です。Marketoサポートがお手伝いします。 サポートケースにこれらの詳細を含めることで、行き来を避け、迅速な解決に向けてチームが取り組めるように支援します。 Marketo サポートの利用に関する[&#x200B; ベストプラクティス &#x200B;](https://nation.marketo.com/t5/knowledgebase/best-practices-for-working-with-marketo-support/ta-p/253491)の記事を参照してください。

このガイドを活用すれば、この重要な時期に、エンゲージメントとコンバージョンを促進する優れた立場から始めることができるので、安心して休憩できます。 ストレスは大きなものですが、その必要はありません。 今日から準備を始め、このホリデーシーズンを今までで最も成功させましょう。

+++

## Adobe Workfrontホリデーシーズン対応ガイド {#workfront}

+++**クリックすると、Adobe Workfrontの休暇準備に関する推奨事項が表示されます。**

ホリデーシーズンに向けて、Adobe Adobe Workfrontを導入する際は、サポート担当者の更新、Adobeによる社内スケジュールの調整、繁忙期における大きな変化の回避、自動化や統合のプロアクティブな監視を通じて、円滑なオペレーションを実現する必要があります。

### 拡張の準備

休日の間にスムーズなサポート体験を保証するために：

* 承認済みのサポート連絡先情報を事前に確認して更新します。
* 重要な問題が発生した場合、主要な関係者がサポートに協力できることを確認します。
* ホリデーシーズン中に製品やワークフローの計画が変更される場合は、11月中旬または1月上旬以降にスケジュールを設定して、最適な納期を確保することを検討してください。
* 社内のホリデースケジュールをAdobeの連絡先に伝え、連携を確保。

### 検証

Workfront リリースに関する情報を入手し、サンドボックス環境で新機能をテストします。

* [Adobe Workfront リリースの準備](https://experienceleague.adobe.com/ja/docs/workfront/using/product-announcements/product-releases/release-readiness)
* [Workfront リリースノートのアーカイブ](https://experienceleague.adobe.com/ja/docs/workfront/using/product-announcements/product-releases/product-releases)
* [2025年第1四半期リリースの概要](https://experienceleague.adobe.com/ja/docs/workfront/using/product-announcements/product-releases/release-25-q1/25-q1-release-overview)
* [Workfront リリースウェビナーの録画](https://experienceleague.adobe.com/ja/docs/events/workfront-recordings/releases/25-1-release-webinar)

### ベストプラクティス

* プロアクティブな計画：社内の休暇スケジュールの影響を受ける可能性のあるシステムの依存関係またはスケジュールされた自動化を特定します。
* 継続的なコミュニケーション：計画されたメンテナンスや重要なイベントについて、社内の各部門やAdobeサポートに情報を提供します。
* ダッシュボードを使用する：パフォーマンスに関する問題の兆候を早期に発見するために、主要な統合と自動化をモニターします。
* 早期にエスカレーションする：サービスの低下を予測または観察する場合は、すぐにサポートチケットを発行してください。それが重要になるのを待ってはいけません。

事前に計画を立て、明確なコミュニケーションを維持し、問題を早期にエスカレーションすることで、混乱を最小限に抑え、Workfrontがホリデーシーズンを通じて重要なワークフローをサポートし続けられるようにすることができます。

+++

## Adobe Campaignホリデーシーズン対応ガイド {#campaign}

+++**クリックすると、Adobe Campaignの休暇準備に関する推奨事項が表示されます。**


Adobe Campaignがホリデーシーズンに対応できるように、配信品質の設定を積極的に検証し、オーディエンスのセグメンテーションとメッセージ頻度を最適化して、インフラストラクチャの拡張性を確保し、クロスチャネルキャンペーンのオーケストレーションをテストして、季節ごとの配信数やエンゲージメントの急増を効果的に処理する必要があります。

### ホリデーキャンペーンを際立たせるエキスパートのヒント

休暇に備えた買い物を始めるのに早すぎることがないのと同じように、ホリデーマーケティングキャンペーンを大成功に導くための計画も、早く始めるに越したことはありません。 Adobe Campaignなら、組織の休暇に関するあらゆる要望を満たすキャンペーンを設計、計画、実行できます。 しかし、今年の終わりに大きな成果をもたらすキャンペーンを実施するためのヒントを把握していますか？ このビデオ「[&#x200B; ホリデーキャンペーンを際立たせるための専門家のヒント &#x200B;](https://experienceleague.adobe.com/ja/docs/events/experience-league-live-recordings/episodes/exl-live-episode-03)」では、配信品質と実行のベストプラクティスについて説明し、Adobe Campaignですべての方法について説明しています。

### 休暇期間に関する考慮事項と準備

このビデオ、[Adobe Campaign：休暇期間の準備 – 休暇期間に関する考慮事項と準備](https://helpx.adobe.com/jp/customer-care-office-hours/campaign/campaign-holiday-readiness.html)では、次の項目について説明します。

* Campaign コミュニティのエンゲージ
* 配信品質 – 休日とそれ以降の考慮事項！
* Adobe Campaign Classic（ACC）およびAdobe Campaign Standard（ACS）に関する技術情報

Adobe Campaignをホリデーシーズンに備えるためには、配信品質チェックを確定し、キャンペーン設定を検証して、ホリデーシーズン全体を通じて、信頼性のある大量の時間的制約のあるキャンペーンを実施するための拡張可能なインフラストラクチャとクロスチャネルオーケストレーションを配置する必要があります。

+++

## Adobe Analyticsホリデーシーズン対応ガイド {#analytics}

+++**クリックすると、Adobe Analyticsの休暇準備に関する推奨事項が表示されます。**

ホリデーシーズンが近づくと、Adobe Adobe Analyticsを利用している企業は、トラフィックのピーク時におけるデータの正確性、プラットフォームのパフォーマンス、レポートの信頼性を確保するために、積極的に対策を講じる必要があります。 Adobeには、効果的に準備するのに役立つリソースとベストプラクティスがいくつか用意されています。

### トラフィックを予測

適切なハードウェア割り当てとシステムの応答性を確保するために、Adobeでは、事前に&#x200B;**ピーク時および毎日のサーバーのヒット/コールボリューム**&#x200B;を送信することをお勧めします。

* データがどれだけ迅速に利用可能になるかを理解することは、大量の期間におけるリアルタイムの意思決定に不可欠であるため、[&#x200B; トラフィックスパイクスケジュールとハードウェア割り当てリードタイム &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/traffic-management/t-traffic-schedule-spike#hardware-allocation-lead-times)を確認してください。

* 予期しないトラフィックの急増やハードウェアの問題など、Adobe Analyticsのデータ可用性と待ち時間に与える影響について、[Adobe Analytics データ待ち時間の概要](https://experienceleague.adobe.com/ja/docs/analytics/technotes/latency)で説明し、データ遅延を低減するための推奨される戦略を見つけます。

### ベストプラクティス

データフィードを使用して生の分析データを書き出す場合、Adobeは、フィード設定を最適化し、よくある落とし穴を回避するためのガイダンスを提供します。

* [Adobe Analytics データフィードのベストプラクティス](https://experienceleague.adobe.com/ja/docs/analytics/export/analytics-data-feed/data-feeds-best-practices)

休暇中に迅速かつ信頼性の高いレポートを維持するために、Adobeでは次をお勧めします。

* [Analysis Workspaceのパフォーマンスの最適化](https://experienceleague.adobe.com/ja/docs/analytics/analyze/analysis-workspace/workspace-faq/optimizing-performance)
* [Report Builderのトラブルシューティングとベストプラクティス：リクエストを最適化するための推奨事項](https://experienceleague.adobe.com/ja/docs/analytics/analyze/legacy-report-builder/troubleshoot#section_33EF919255BF46CD97105D8ACB43573F)
* [Analytics コンポーネントガイド：スケジュール済みレポートキュー](https://experienceleague.adobe.com/ja/docs/analytics/components/scheduled-reports-admin)

### ホリデーメンテナンス計画

Adobeでは、通常、休暇期間のピーク時に&#x200B;**メンテナンス除外ウィンドウ**&#x200B;を適用し、サービスの中断を防ぎます。 お客様は、Experience Leagueを通じてAdobeのリリースとメンテナンスのスケジュールを監視し、Adobe アカウントチームと連携してサポート計画を立てる必要があります。

これらのガイドラインに従い、Adobeの公開ドキュメントを活用することで、企業はAdobe Analyticsの導入を堅牢かつ迅速におこない、ホリデーシーズンの需要に応えることができます。

+++

## Adobe Targetホリデーシーズン対応ガイド {#target}

+++**クリックすると、Adobe Targetの休暇準備に関する推奨事項が表示されます。**

ホリデーシーズンは、顧客とのエンゲージメントに新たな機会をもたらします。しかし、トラフィックの急増やパーソナライゼーションシステムに対する需要の増加など、さまざまな課題も伴います。 この重要な時期にシームレスな体験を提供するために、アドビでは、Adobe Targetの導入に向けた推奨事項をまとめました。

### 需要の予測

まず、トラフィックの急増を20～50%以上予測し、インフラストラクチャが負荷に対応できるかどうかを検証します。 Adobe Target、Adobe Analytics、Adobe AEPをまたいでアクティビティとデータ量を予測し、予想外の事態を回避。

また、チェックアウト、商品レコメンデーション、プロモーションオファーなど、重要な役割を果たすジャーニーを特定することも重要です。そのため、パーソナライゼーションを推進するには、最も重要なチャネルに焦点を当てる必要があります。

Adobe Targetでの最適化については、[&#x200B; ベストプラクティス &#x200B;](https://experienceleague.adobe.com/ja/docs/target-learn/tutorials/administration/strategy/target-best-practices-for-optimization)を参照してください。

### 拡張の準備

* web サイトとモバイルデバイスでのトラフィック増加を計画し、Target サポートチームに通知して、サーバー容量を増やし、ブロックされた呼び出しを回避します。
* ロード/ペンのテストでは、Target サポートチームに事前に通知する必要があります。
* 最新の`at.js`/Delivery API バージョンにアップグレードします。
* 重要ではない変更を最小限に抑えて、フォールバックエクスペリエンスに備える：
* サポートとエスカレーションプロセスを調整し、プロアクティブなアラートを有効にします。

### 検証

[QA リンク &#x200B;](https://experienceleague.adobe.com/ja/docs/target/using/activities/activity-qa/activity-qa)を使用してコンテンツ配信を検証し、すべてが期待どおりに動作することを確認します。 「**[!UICONTROL オーディエンスルールを一致してエクスペリエンスを表示]**」トグルを使用して、テスト中のアクティビティに適したオーディエンスが適格であることを確認します。 **[!UICONTROL 目標指標]**&#x200B;の設定が、アクティビティの&#x200B;**[!UICONTROL 目標]**&#x200B;に一致していることを再確認します。 また、念のために常にバックアッププランを用意しておきます。

### ベストプラクティス

実装は、[Adobe Targetの制限](https://experienceleague.adobe.com/ja/docs/target/using/troubleshoot/target-limits)内に収め、[GDPRおよびCCPAのコンプライアンス &#x200B;](https://experienceleague.adobe.com/ja/docs/target-dev/developer/implementation/privacy/cmp-privacy-and-general-data-protection-regulation)を事前に検証してから開始してください。 作業中のアクティビティを100個未満しか管理せず、古いアクティビティをアーカイブすることで、作業を効率化します。 AI主導の最適化のために&#x200B;**[!UICONTROL 自動割り当て]**/**[!UICONTROL 自動ターゲット]**&#x200B;を活用します。 ロールバックプランとリアルタイムのモニタリングダッシュボードを確立する。

### セキュリティとガバナンス

エクスペリエンスをパーソナライズする前に、GDPRとCCPAの下で同意のコンプライアンスを確認してください。 個人情報（PII）をプロファイルパラメーターに保存することを避け、API セキュリティを検証して顧客データを保護します。

+++
