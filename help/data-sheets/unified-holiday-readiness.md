---
title: Adobe DX ソリューション統合ホリデー対応ガイド
description: AEP、AJO、CJA、Commerce、AEM、Marketo、Workfront、Campaign、Analytics および Target に対するAdobe DX Holiday Readiness は、計画、拡張、保護および最適化に役立ちます。
feature-set: Experience Cloud
feature: Support
solution: Experience Cloud, Experience Platform, Journey Optimizer, Customer Journey Analytics, Commerce, Experience Manager, Workfront, Campaign, Analytics, Target, Marketo Engage
role: Developer, Admin, Leader, User
index: true
source-git-commit: 542f9696ed2cc71b23cfc3cc4fd410af5c8f7f73
workflow-type: tm+mt
source-wordcount: '3827'
ht-degree: 2%

---

# Adobe DX ソリューション統合ホリデー対応ガイド


Adobe DX ソリューション統合休日対応ガイドは、事後対応型の問題解決ではなく、プロアクティブな計画に重点を置くことで、休日時期に備えることができます。 インスタンスの準備が整い、潜在的な問題を発生前に最小限に抑えるための実用的な手順を説明します。 Adobeのチームは、技術的な専門知識、幅広い能力、実証済みの手法を駆使して、技術的および戦略的な両方で適切なレベルのサポートとガイダンスを提供し、お客様のビジネスの準備を整えます。

次のベストプラクティスに従って、Adobe デジタルエクスペリエンスソリューションの回復力と安全性を確保し、ピーク時のホリデートラフィックに対応できるようにします。

* トラフィックの増加に備えて計画します。
* ピークウィンドウ中に大きな変更を行わないようにします。ホリデーシーズンの前または後に更新をスケジュールします。
* ダッシュボードとアラートを使用してパフォーマンスを監視し、ボトルネックを早期に検出します。
* 認定されたサポート担当者が最新であることを確認します。
* 可能な限り、事前に [Adobe サポートにお問い合わせください &#x200B;](https://experienceleague.adobe.com/ja/docs/learning-manager/using/faq/how-to-submit-support-ticket)。

Adobeのソリューションに固有の、休日への対応に関する推奨事項については、次の節を参照してください。

* [Adobe Experience Platform](#aep)
* [Adobe Journey Optimizer](#ajo)
* [Adobe Customer Journey Analytics](#cja)
* [Adobe Commerce](#commerce)
* [Adobe Experience Manager](#aem)
* [AdobeMarketo](#marketo)
* [Adobe Workfront](#workfront)
* [Adobe Campaign](#campaign)
* [Adobe Analytics](#analytics)
* [Adobe Target](#target)

>[!NOTE]
>
>各セクションをクリックして展開します。


## Adobe Experience Platform（AEP）の休日への対応ガイド {#aep}

+++**クリックして、Adobe Experience Platform（AEP）の休日に対する準備状況の推奨事項を確認します。**

Adobe Experience Platform（AEP）は、リアルタイムのカスタマーエクスペリエンスを強化するうえで重要な役割を果たします。 ホリデーシーズンが近づくにつれて、AEPの実装が、トラフィックの増加、安全なデータ処理、スケーラブルな取り込みのために最適化されるようにすることが重要になります。

### 季節需要の予測

季節的なトラフィックスパイクに備えて、Adobeでは処理能力の計画とストリーミングプロファイル取り込みの監視を行うことをお勧めします。 これには、データ量の予測や、システムがスループットの向上に対処できるようにすることが含まれます。 詳しくは、[&#x200B; 処理能力と季節的なトラフィックの計画 &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/dataflows/ui/monitor-streaming-profile) を参照してください。

### スケールの準備

Adobeでは、休暇のトラフィックに対して環境の準備を確実に整えるための方法がいくつか用意されています。

* サンドボックスに割り当てられる容量を増やします。
* [&#x200B; 監視ダッシュボード &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/dataflows/ui/monitor-streaming-profile) で高スループットのデータフローを特定し、必要に応じてスロットルやフィルタリングを適用します。
* [&#x200B; ライセンスの使用と容量：ストリーミングスループットのベストプラクティス &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/landing/license/capacity#suggestions) で説明されているように、待機時間の短いユースケースにバッチ取得を使用してパフォーマンスを最適化します。

これらのプラクティスは、取り込みの信頼性を維持し、ピーク時の待ち時間を短縮するのに役立ちます。

### ベストプラクティスとガードレール

運用上の制限内に保ち、サービスの中断を避けるために、Adobeでは、次の取り込みとプロファイルガードレールを推奨します。

* [&#x200B; ストリーミングスループットのベストプラクティス &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/landing/license/capacity#suggestions)
* [&#x200B; データ取り込みのガードレール &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/ingestion/guardrails)
* [リアルタイム顧客プロファイルデータおよびセグメント化用のデフォルトガードレール](https://experienceleague.adobe.com/ja/docs/experience-platform/profile/guardrails)
* [AEP ブループリント：ガードレール &#x200B;](https://experienceleague.adobe.com/ja/docs/blueprints-learn/architecture/architecture-overview/guardrails)

### セキュリティとガバナンス

Adobeでは、特にトラフィックが多い季節やデータの機密性が高い場合に、強力なセキュリティとガバナンスのプラクティスを重視しています。

Adobe Experience Platform実装全体で顧客データを保護し、プライバシー制御を適用し、コンプライアンスを維持する方法の推奨事項については、[AEPのガバナンス、プライバシー、セキュリティ：セキュリティ &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/landing/governance-privacy-security/overview#security) を参照してください。

これらのガイドラインに従い、Adobeの公開ドキュメントを活用することで、組織はAdobe Experience Platformの回復力と安全性を確保し、ホリデーシーズンを通じて優れたカスタマーエクスペリエンスを提供する準備を整えることができます。

+++

## Adobe Journey Optimizer（AJO）の休日への対応ガイド {#ajo}

+++**クリックして、Adobe Journey Optimizer（AJO）の休日に対する準備状況の推奨事項を確認します。**


ホリデーシーズンに向けてAdobe Journey Optimizerを準備するには、イベントのスパイクとクロスチャネルの複雑さを予測し、ジャーニーと頻度のルールを設定し、データハイジーンと意思決定のロジックを確保する必要があります。 また、パフォーマンスを大規模に検証し、セキュリティと API ガードレールを適用し、ピーク後のインサイトを適用して今後のキャンペーンを調整する必要もあります。

### 需要を予測

* ホリデーシーズンの圧縮率とキャンペーン量の増加に基づき、以下を予測：
   * リアルタイムイベントとトリガージャーニーのスパイク（買い物かごの放棄、直前のオファー）
   * メッセージ飽和度のリスク（高いオプトアウト、疲労）
   * クロスチャネルの複雑さの増加（メール + プッシュ + SMS + アプリ内）
* 昨年の指標（オープン/クリック/オプトアウト率、ジャーニーエントリボリューム）を使用して、予想される負荷をモデル化し、メッセージングシステムのしきい値を設定します。
* 可能性の高い「処理の少ない時間帯」またはパフォーマンスが低い時間帯（例：週末、休日）を特定し、それに応じて送信ボリュームを計画します。

### スケールの準備

* AJOのすべてのチャネル設定（メール、プッシュ、SMS、web、アプリ内）が正しく設定されていることを確認します。 [&#x200B; チャネル設定のセットアップ &#x200B;](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/configuration/channel-surfaces) を参照してください。
* フリークエンシーキャップとキャッピングルールを設定して、メッセージ量を制御します。 [&#x200B; フリークエンシーキャップ &#x200B;](https://experienceleague.adobe.com/ja/docs/journey-optimizer-learn/tutorials/configuration/business-rules/configure-frequency-capping-rules) の記事を参照してください。
* チャネル/ジャーニーのルールセットを設定します。[&#x200B; ルールセットの操作 &#x200B;](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets) を参照してください。
* データハイジーン/リアルタイムイベントストリームおよびセグメント化フレームワークを準備します。
* 次のようなホリデーキャンペーンのターゲットオーディエンスを定義していることを確認します。
   * 価値の高い顧客
   * 常連セグメント
   * 買い物かごの放棄
   * 初めての購入者
* ホリデージャーニーのテンプレートを事前に読み込んだり準備したりします。決定ロジック（オファー/制約）を活用して、在庫、時間依存オファー、チャネルの環境設定に基づいて動的に適応できるようにします。 [&#x200B; オファーへの制約の追加 &#x200B;](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/decisioning/offer-decisioning/managing-offers-in-the-offer-library/configure-offers/add-constraints) 記事の例を参照してください。
* 技術的準備状況：API/エンドポイントの読み込み処理能力、カスタムアクションおよび外部統合のスロットル/キャッピングルールを確認します。 [&#x200B; ガードレールと制限事項 &#x200B;](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/get-started/guardrails) を参照してください。

### テストと検証

* 実験フレームワークを使用して、主な変数の変更をテストします。
   * 送信時間
   * オファータイプ
   * チャネルミックス
[AJO Experimentation Acceleratorのベストプラクティス &#x200B;](https://experienceleague.adobe.com/en/docs/experimentation-accelerator/using/get-started/experiment-accelerator-best-practices) を参照してください。
* ジャーニーのエンドツーエンドの検証を実施します。
   * イベントのトリガー
   * セグメントのエントリ
   * ジャーニーパスフロー
   * パーソナライゼーションロジック
   * オファーの制約
   * 終了条件
* キャッピングルールと競合ルールを検証します。 [ジャーニーのキャッピングと判別 &#x200B;](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/conflict-prioritization/journey-capping) に関する記事を参照してください。
* ピークの送信またはスパイクに対するストレステスト拡張ボリューム：高トリガーボリュームをシミュレートして、負荷時のシステム動作を検証します。
* 配信品質の検証：メールドメインや送信者のウォームアップ、モバイルプッシュ設定の確認、SMS/アプリ内のフォールバックチャネルの確認を行います。

### ベストプラクティス

* オムニチャネルオーケストレーションを使用します。 AJOのホリデーシーズンの例を示したブログ [&#x200B; エンゲージメントと成長のための不可欠なオムニチャネルカスタマージャーニー &#x200B;](https://business.adobe.com/blog/essential-customer-journeys-for-omnichannel-engagement) の記事を参照してください。
* 必要に応じて、リアルタイムトリガーの優先順位を付けます。 例：買い物かごの放棄、閲覧の中断、在庫アラートは、休日の買い物客がよりリアクティブなので、などです。
* セグメント化とパーソナライゼーションの活用：目的の高いセグメントをターゲットにし、過去の購入行動や好みに基づいてオファーをカスタマイズします。
* メッセージングの疲れを最小限に抑える：過度の勧誘を避けるために、制限と静かな時間を強制します。 [AJOでの毎日のフリークエンシーキャップでカスタマーエクスペリエンスを高める &#x200B;](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/elevate-customer-experience-with-daily-frequency-capping-in-ajo/ba-p/761510?profile.language=ja) のブログ投稿を参照してください。
* タイミングの問題：休暇の早い時期に（圧縮されたシーズンを考慮して）送信を計画し、チャネルをタイムゾーンとローカルオーディエンスの行動に合わせます。
* 動的/期間限定のオファーを提供して、緊急度を高めつつ、チャネル間で調整して重複と競合を回避します。
* 抑制ロジックの使用：購入したばかりのオーディエンスを抑制したり、購入後のジャーニーを適用して冗長なメッセージを回避したりします。

### セキュリティとガバナンス

* 必要なユーザーのみがジャーニーをデプロイしたり、ビジネスルールを変更したりできるように、アクセス制御と権限が設定されていることを確認します。
* API 呼び出し/接続キャッピングの監視と適用：例えば、[Capping API を参照してください。 |Adobe Journey Optimizer](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/connect-systems/external-systems/capping) 記事。
* クリーンなファーストパーティデータを使用し、適切な ID スティッチングを確保することで、メッセージングが重複したり、ミスアラインメントしたりしないように、顧客中心になるようにします。
* 特に大量のホリデー送信の場合に、配信品質ドメインが暖められ、スパム対策対策が行われていることを確認します。
* 監査ログとジャーニーの変更をピークシーズン中に頻繁に確認し、ジャーニーの誤実行やエラーを早期に検出します。

### ピーク後の学習

* ピーク読み込みの後、ジャーニーエントリ数、抑制数、オプトアウト率、配信品質指標、チャネルパフォーマンスについて確認します。
* 抑制されたセグメントをクリーンアップし、ホリデーウィンドウ用に作成されたジャーニーを一時停止または廃止して、繰り越し疲労を避けます。
* リアルタイムのパフォーマンスに関するインサイトを使用して、来年の計画を調整します（例：送信時間の調整、チャネルミックス、メッセージの量）。

季節的な需要の予測、チャネルとルールの設定、ジャーニーのパフォーマンスの検証、セキュリティとガバナンスの適用を事前に行うことで、Adobe Journey Optimizerは、ホリデーシーズン終了後も、シームレスでパーソナライズされた柔軟な顧客体験を提供できるようになります。

+++

## Customer Journey Analytics（CJA）の休日への対応ガイド {#cja}

+++**クリックして、Customer Journey Analytics（CJA）の休日に対する準備状況の推奨事項を確認します。**

Customer Journey Analyticsは 5 Ps を使用して、ホリデー/ピークシーズンへの対応を達成します。

### スケールの準備

* CJAの接続とデータビューを確認し、強化されたモニタリングとプロビジョニングが必要な接続とデータビューを確立します。
* 休日に備えてプロビジョニングで十分であることを確認し、必要に応じて重要な接続とデータビューを拡張します。 詳しくは、[&#x200B; 接続の管理 &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-connections/manage-connections) を参照してください。

### パフォーマンスの監視

* RAM （[[!UICONTROL &#x200B; レポートアクティビティマネージャー &#x200B;] 概要 &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-overview)）を活用して、アクティブなレポートリクエストとキューに登録されたレポートリクエストをリアルタイムで監視し、容量内の接続を特定して、ボトルネックを発見します。
* [&#x200B; エラーとトラブルシューティングガイド &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-workspace/workspace-faq/error-messages) および [&#x200B; 既知の制限事項 &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-workspace/workspace-faq/aw-limitations) 記事を使用して、ピーク読み込み中の待ち時間の増加を確認します。
* 管理者が、RAM を介して、長時間実行されている/ブロックされているリクエストを事前に中断またはキャンセルできるようにします。 [CJAでのレポートリクエストのキャンセル &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-cancel-requests) を参照してください。

### ベストプラクティス

* トラフィックが少ない時間帯に書き出しやレポートをスケジュールして、負荷をスムーズにし、待ち時間を最小限に抑えます。 [&#x200B; 予定レポート &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-components/scheduled-projects-manager) の記事を参照してください。
* リクエストを分割：1 日を通して異なる間隔でレポートをスケジュールします。
* パネルを減らし、セグメントを簡素化し、日付範囲を短縮し、過剰な同時ジョブを回避します。 詳しくは、[CJA Workspaceのパフォーマンスの最適化 &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-workspace/workspace-faq/optimizing-performance) を参照してください。

### トラブルシューティング

* ワークスペースエラーのトラブルシューティングを行う場合は、原因と推奨アクションについてエラーメッセージを参照し、RAM （[!UICONTROL Reporting Activity Manager]）を使用してボトルネックを解消し、同時実行を効果的に管理します。 詳しくは、[CJA Workspace エラー処理 &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-workspace/workspace-faq/error-messages) を参照してください。
* RAM （CJA[[!UICONTROL &#x200B; の &#x200B;]Reporting Activity Manager](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-overview)）を使用して、問題のあるユーザー、クエリまたはプロジェクトを特定し、必要に応じて優先順位を付けて終了またはキャンセルします。

### ピーク後の学習

* 休日/ピーク期間の後、パフォーマンスとインシデントログを確認して、提供されたベストプラクティスの影響を評価します。
* 処理に時間のかかるクエリやユーザータスクを確認し、次のシーズンに最適化できるパターンやトレンドを特定します。
* ユーザーや関係者からのフィードバックを収集し、新しく得たインサイトを使用して独自の Runbook と準備プランを更新します。
* アカウントチームを介してAdobe チームにフィードバックを提供します。

+++

## Adobe Commerce ホリデー対応ガイド {#commerce}

+++**クリックして、Adobe Commerceの休日に対する準備状況の推奨事項を確認します。**

組織のピークシーズンを確実に成功させるには、高トラフィックに対応するAdobe Commerce デジタルストアフロントの準備を行うことが不可欠です。

### 需要を予測

* ホリデーのピーク営業期間中（11 月中旬から 1 月中旬）に、Adobeでは、クラウドインフラストラクチャでホストされているすべてのAdobe Commerceのマーチャントに対して、ホリデーサージ容量のリクエストを送信して、訪問者数の増加をプロアクティブに計画することをお勧めします。 詳しくは、[&#x200B; クラウドインフラストラクチャにおけるAdobe Commerceのホリデーサージ容量リクエスト &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-knowledge-base/kb/announcements/commerce-announcements/holiday-surge-capacity-requests-for-magento-commerce-cloud) を参照してください。

### スケールの準備

Adobe Commerce（およびオプションのAdobe Experience Cloud ツール）を使用して実用的な戦略を提供し、1 年で最も忙しい時期に優れたカスタマーエクスペリエンスを計画、ピボット、提供するのに役立つ、[&#x200B; 計画とピボット：ピークシーズン 2025 への戦略的アプローチ &#x200B;](https://experienceleague.adobe.com/ja/perspectives/planning-and-pivoting-a-strategic-approach-to-peak-season-2025) ガイドの推奨事項に従ってください。

### ベストプラクティス

* Adobeのガイド [&#x200B; 高トラフィックに対応するインフラストラクチャの準備方法 – ピークシーズンの 5 Ps のパフォーマンス &#x200B;](https://business.adobe.com/blog/how-to/the-5-ps-of-peak-season-performance-a-guide-to-preparing-your-infrastructure-for-high-traffic) に従ってください。
* トラフィック量の多いインフラストラクチャを準備する方法、ダウンタイムを防ぐ方法、休日に最適なパフォーマンスを実現する方法については、[Commerce休暇に備える技術ヒント &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-knowledge-base/kb/how-to/tech-tips-for-commerce-holiday-readiness) を参照してください。

+++

## Adobe Experience Manager（AEM）の休日への対応ガイド {#aem}

+++**クリックして、Adobe Experience Manager（AEM）の休日に対する準備状況の推奨事項を確認します。**

ホリデーシーズンが近づいており、多くのAdobeのお客様にとって、これはピーク時の販売時期の開始を意味します。 皆様の成功に向けた取り組みにおいて、皆様には、今後のトラフィックの急増に備えた準備を万全に整えていただきたいと考えています。

### Adobe Experience Manager（AEM） Cloud Services

ホリデーシーズン中に最も忙しい瞬間を経験する組織の場合、ピークトラフィックに対応するためにAdobe Experience Manager サイトを最適化する方法を検討している可能性があります。 幸いにも、Adobe Experience Manager Cloud Services を使用すると、サイトは自動スケール機能を既に備えており、トラフィックが突然変更された場合でも、訪問者にシームレスなエクスペリエンスを提供できます。

#### スケールの準備

* Adobe Experience Manager Cloud Services で高トラフィックに備える方法に関する詳細なインサイトとガイダンスについては、次のリンクを参照してください。

   * [AEM as a Cloud Serviceの CDN](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/implementing/content-delivery/cdn)
   * [AEM as a Cloud Serviceのキャッシュ &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-manager-learn/cloud-service/caching/overview)

* Ultimate Success ユーザーで、最近Adobe アカウントチームとボリュームフォーキャスト情報を共有した場合は、既にビューがあるので、再度送信する必要はありません。

アドビは、ジャーニーのすべてのステップでお客様をサポートします。 ご不明な点やご不明な点がございましたら、お気軽に [&#x200B; サポートチケットを送信 &#x200B;](https://experienceleague.adobe.com/ja/docs/learning-manager/using/faq/how-to-submit-support-ticket) ください。

ホリデーシーズンにマーケティングキャンペーンを準備するには、[AEMaaCS ユーザーガイド：概要 – マーケティングキャンペーンパラメーター &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/implementing/content-delivery/caching#marketing-parameters) ドキュメントを確認してください。

#### セキュリティとガバナンス

AEM Web サイトのトラフィックセキュリティとセキュリティについては、AEM as a Cloud Service チュートリアルの [&#x200B; 概要 – AEM Web サイトの保護 &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-manager-learn/cloud-service/security/traffic-filter-and-waf-rules/overview) に関する記事を参照してください。

#### 休日のメンテナンス計画

Adobeでは、重要なホリデーウィンドウ中にサービスが中断されないようにするために、メンテナンス除外期間をスケジュールしました。

* **自動更新はありません** は次の期間に行われます：
   * 2025 年 11 月 24 日～2025 年 12 月 2 日
   * 2025 年 12 月 15 日～2026 年 1 月 2 日

これにより、トラフィックが多い時間帯の安定性が確保されます。 完全なリリーススケジュールとメンテナンスウィンドウについては、[AEM リリースロードマップ &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-manager-release-information/aem-release-updates/update-releases-roadmap) を参照してください。


### Adobe Experience Manager（AEM）とAdobe Managed Services（AMS）

Adobe Managed Servicesを利用しているAEMのお客様は、CSE と事前に協力して、休日の補償ニーズを計画できます。

++++

## Adobe Marketo ホリデー対応ガイド {#marketo}

+++**クリックして、Adobe Marketoの休日への対応に関する推奨事項を確認します。**

Adobe Marketoを使用してホリデーキャンペーンを成功に導くには、メール認証の設定を検証し、データベースをクリーンアップおよび保護し、キャンペーンのロジックとスケジュールを最適化し、メールのレンダリングと配信品質を徹底的にテストして、ピーク時のパフォーマンスとエンゲージメントに対するサポートの対応を合理化する必要があります。

### スケールの準備

* SPF/DKIMの設定を確認し、すべてが正しく設定されて機能していることを確認します。 詳しくは、[&#x200B; メール配信品質の SPF とDKIMの設定 &#x200B;](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-spf-and-dkim-for-your-email-deliverability) を参照してください。
* 非アクティブまたは無効なレコードをパージして、Marketo データベースを監査およびクリーンアップします。 これにより、送信が最も販売準備完了のリードのインボックスに届く可能性が高まります。 詳しくは、[Marketo データベースのヘルスチェックとクリーンな状態の保持方法 &#x200B;](https://nation.marketo.com/t5/champion-program-blogs/marketo-database-health-check-up-amp-how-to-keep-it-clean/ba-p/323563) を参照してください。
* チームメンバーがタスクを実行するための適切な権限を持っていることを確認し、メールへの意図しないアクセスや変更を防ぎます。 **[!UICONTROL 管理者]** または **[!UICONTROL Admin Console]** 経由で変更を加えている場合でも、私たちはあなたのことをカバーしています。 [&#x200B; ユーザーの役割と権限の管理 &#x200B;](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/administration/users-and-roles/managing-user-roles-and-permissions) の記事を参照してください。
* ランチパッドの統合を確認して正しい認証を行い、使用する前に潜在的なエラーを解決します。 [Marketo デベロッパーガイド：認証 &#x200B;](https://experienceleague.adobe.com/ja/docs/marketo-developer/marketo/rest/authentication) の記事を参照してください。

### ベストプラクティス

効率化の出発点は、Marketoがキャンペーンをどのように優先し、処理するかを正確に理解することです。 これらの最適化のヒントを使用して、キャンペーンにスピードのプレゼントをしましょう。

* 緊急度の高いメールや優先度の高いメールを誤って遅延させるのを防ぐには、Marketoがキャンペーンフローのステップの処理を優先する方法を理解することが重要です。 [&#x200B; キャンペーン処理の仕組み &#x200B;](https://nation.marketo.com/t5/knowledgebase/how-campaign-processing-works/ta-p/248264) の記事を参照してください。
* スマートリストのロジックに留意すると、キャンペーンを迅速かつピーク時のパフォーマンスで実行するのに役立ちます。 [&#x200B; スマートリストのベストプラクティス &#x200B;](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/creating-a-smart-list/best-practices-for-smart-lists) の記事を参照してください。
* **[!UICONTROL ヘッドスタート]** または **[!UICONTROL 受信者のタイムゾーン]** では、送信の前にメールの作成を開始でき、遅延を減らし、高リソースのロジックを使用して適格なリードの準備時間を増やすことができます。 詳しくは、[&#x200B; メールプログラムのヘッドスタート &#x200B;](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/email-marketing/email-programs/email-program-actions/head-start-for-email-programs) および [&#x200B; 受信者のタイムゾーンでメールプログラムをスケジュールする &#x200B;](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/email-marketing/email-programs/email-program-actions/scheduling-with-recipient-time-zone/schedule-email-programs-with-recipient-time-zone) に関する記事を参照してください。
* キャンペーンがアクティブで、リードがフローを実行中に、フローステップで間違いに気がつきます。 すぐに調整して修正することは魅力的ですが、ライブ待機ステップを変更したり、フローを並べ替えたりした場合に何が起こるかを認識しておくと、後で多くの頭痛を避け、クリーンアップするのに役立ちます。 [&#x200B; メンバーの待機手順でのキャンペーンフローの編集 &#x200B;](https://nation.marketo.com/t5/knowledgebase/editing-campaign-flow-with-members-in-wait-steps/ta-p/254294) の記事を参照してください。

### テストと検証

**[!UICONTROL 送信]** をヒットする前に、メールの外観と動作が意図したとおりに動作することを確認してください。

* Marketoでは、複数の方法でメールの外観をテストし、想定通りに表示されることを確認しています。
   * **[!UICONTROL プレビュー]** 関数を使用すると、セグメント化または個々のリードでプレビューすることで、動的コンテンツとトークンが正しくレンダリングされていることを確認できます。 [&#x200B; 動的コンテンツを含むメールのプレビュー &#x200B;](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/email-marketing/general/functions-in-the-editor/preview-an-email-with-dynamic-content) 記事を参照してください。
   * テストレコードに直接メールをすばやく簡単に送信して、様々なクライアントやデバイスでメールがどのように表示されるかを確認します。 [&#x200B; スマートリストから 1 つのフローステップを実行する &#x200B;](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/using-smart-lists/run-a-single-flow-step-from-a-smart-list) の記事を参照してください。
   * [!DNL Litmus] ユーザーにとっては、アカウントを統合し、メールエディターから直接レンダリングテストを開始することが、これまで以上に簡単になりました。 [&#x200B; メールのレンダリングのテスト  [!DNL Litmus]](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/email-marketing/email-designer/test-email-rendering) の記事を参照してください。
* [!DNL SpamAssassin] と統合して、メールのコンテンツを確認し、インボックスに届く可能性または *スパム* としてマークされる可能性のスコアを割り当てるメールスパムレポート機能を確認します。 [&#x200B; メールスパムレポート &#x200B;](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/email-marketing/email-designer/spam-report) の記事を参照してください。
* [!UICONTROL &#x200B; キャンペーンキュー &#x200B;] に注目して、キャンペーンが処理され、緊急度の高い項目の優先順位が正しく設定されていることを確認します。 [&#x200B; キャンペーンは実行中ですか？記事 &#x200B;](https://nation.marketo.com/t5/knowledgebase/is-my-campaign-running/ta-p/248662)。

### サポートエクスペリエンスの効率化

問題が発生した場合は、速度が重要であり、Marketo サポートがお手伝いします。 これらの詳細をサポートケースに含めると、前後を避けて、チームがより迅速な解決に向けて取り組むのに役立ちます。 [Marketo サポートの操作のベストプラクティス &#x200B;](https://nation.marketo.com/t5/knowledgebase/best-practices-for-working-with-marketo-support/ta-p/253491) の記事を参照してください。

このガイドを使用すると、この重要な期間にエンゲージメントとコンバージョンを促進するための強力な立場から始めているので、もう少し安心できます。 賭け金は高いですが、ストレスは必要ありません。 今日から準備を始めて、ホリデーシーズンを今までで最も成功させましょう。

+++

## Adobe Workfront ホリデー対応ガイド {#workfront}

+++**クリックして、Adobe Workfrontの休日に対する準備状況の推奨事項を確認します。**

ホリデーシーズンに向けてAdobe Workfrontを準備するには、サポート連絡先を更新し、Adobeの社内スケジュールを調整し、ピークウィンドウ時の大きな変更を避け、自動化と統合をプロアクティブに監視して、スムーズに作業できるようにする必要があります。

### スケールの準備

休業期間中にスムーズにサポートを受けられるようにするため：

* 事前に認定サポート担当者を確認および更新してください。
* 重要な問題が発生した場合に、主要な関係者がサポートと共同作業できることを検証します。
* ホリデーウィンドウ中に製品またはワークフローの変更を計画する場合は、11 月中旬または 1 月上旬より前に変更をスケジュールして、最適なターンアラウンド時間を確保することを検討してください。
* 社内の休暇スケジュールをAdobeの担当者に伝え、整合性を確保します。

### テストと検証

Workfrontのリリースに関する情報を入手し、サンドボックス環境で新機能をテストします。

* [Adobe Workfront リリースの準備 &#x200B;](https://experienceleague.adobe.com/ja/docs/workfront/using/product-announcements/product-releases/release-readiness)
* [Workfront リリースノートアーカイブ &#x200B;](https://experienceleague.adobe.com/ja/docs/workfront/using/product-announcements/product-releases/product-releases)
* [2025 年第 1 四半期リリースの概要 &#x200B;](https://experienceleague.adobe.com/ja/docs/workfront/using/product-announcements/product-releases/release-25-q1/25-q1-release-overview)
* [Workfront リリースのウェビナー録画 &#x200B;](https://experienceleague.adobe.com/ja/docs/events/workfront-recordings/releases/25-1-release-webinar)

### ベストプラクティス

* プロアクティブ計画：内部タイムオフスケジュールの影響を受ける可能性のある、システムの依存関係またはスケジュールされた自動化を特定します。
* 継続的なコミュニケーション：計画されたメンテナンスや主要なイベントについては、社内チームとAdobe サポートに常に情報を提供します。
* ダッシュボードの使用：主要な統合と自動化を監視して、パフォーマンスの問題の初期兆候を把握します。
* 早期にエスカレートする：サービスの低下が予想される、または発生を確認した場合は、すぐにサポートチケットを開きます。重要になるのを待つ必要はありません。

事前に計画し、明確なコミュニケーションを維持し、問題を早期にエスカレートさせることで、組織は中断を最小限に抑え、休業期間中、Workfrontが引き続き重要なワークフローをサポートすることができます。

+++

## Adobe Campaign ホリデー対応ガイド {#campaign}

+++**クリックして、Adobe Campaignの休日に対する準備状況の推奨事項を確認します。**


Adobe Campaignを休日への備えに備えるために、チームは、配信品質の設定を事前に検証し、オーディエンスのセグメント化とメッセージ頻度を最適化し、インフラストラクチャの拡張性を確保し、季節的なボリュームとエンゲージメントのスパイクを効果的に処理するためのクロスチャネルキャンペーンオーケストレーションをテストする必要があります。

### ホリデーキャンペーンを目立たせるためのエキスパートのヒント

休暇に備えた買い物を始めるのに早すぎることがないのと同じように、ホリデーマーケティングキャンペーンを大成功に導くための計画も、早く始めるに越したことはありません。Adobe Campaignを使用すると、組織の目標を達成するキャンペーンを設計、計画、実行できます。 1 年の終わりを華麗に飾るキャンペーンを実行するためのヒントはご存知でしょうか？ 配信品質と実行のベストプラクティスについて説明し、Adobe Campaignですべてを行う方法を示すこのビデオ [&#x200B; ホリデーキャンペーンを目立たせるためのエキスパートのヒント &#x200B;](https://experienceleague.adobe.com/ja/docs/events/experience-league-live-recordings/episodes/exl-live-episode-03) を確認してください。

### 休業期間中の注意点と準備

このビデオ、[Adobe Campaign：休日への備え – 休日に向けた考慮事項と準備 &#x200B;](https://helpx.adobe.com/jp/customer-care-office-hours/campaign/campaign-holiday-readiness.html) では、次の内容を説明します。

* Campaign コミュニティへの参加
* 配信品質 – 休日以降に関する考慮事項
* Adobe Campaign Classic（ACC）およびAdobe Campaign Standard（ACS）の技術的な推奨事項

ホリデーピークシーズンに備えてAdobe Campaignを準備するには、配信品質チェックを完了し、キャンペーン設定を検証して、拡張性の高いインフラストラクチャとクロスチャネルオーケストレーションが導入され、ホリデーシーズンを通じて時間に依存する大量のキャンペーンを自信を持って実行する必要があります。

+++

## Adobe Analytics ホリデー対応ガイド {#analytics}

+++**クリックして、Adobe Analyticsの休日に対する準備状況の推奨事項を確認します。**

ホリデーシーズンが近づくと、Adobe Analyticsを使用する組織は、トラフィックのピーク時にデータの正確性、プラットフォームのパフォーマンス、レポートの信頼性を確保するために、積極的な手順を実行する必要があります。 Adobeには、チームが効果的に準備するのに役立つリソースとベストプラクティスがいくつか用意されています。

### トラフィックを予測

適切なハードウェア割り当てとシステムの応答性を確保するために、Adobeでは、事前に **ピーク時および毎日のサーバーヒット/コールボリューム** を送信することをお勧めします。

* [&#x200B; トラフィックスパイクスケジュールとハードウェア割り当てのリードタイム &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/traffic-management/t-traffic-schedule-spike#hardware-allocation-lead-times) を確認してください。大量のデータが入る時期にリアルタイムで意思決定を行うためには、データをどれだけ迅速に使用できるかを理解することが重要です。

* [Adobe Analyticsのデータ待ち時間の概要では、予期しないトラフィックスパイクやハードウェアの問題など &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics/technotes/latency)Adobe Analyticsのデータの可用性と待ち時間に与える影響を説明し、データの待ち時間を減らすために推奨される戦略を見つけます。

### ベストプラクティス

データフィードを使用して生の分析データを書き出すチームに対しては、Adobeが、フィード設定の最適化と、一般的な落とし穴の回避に関するガイダンスを提供します。

* [Adobe Analytics データフィードのベストプラクティス &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics/export/analytics-data-feed/data-feeds-best-practices)

休業期間中に迅速で信頼性の高いレポートを作成するために、Adobeでは次のことを推奨しています。

* [Analysis Workspaceのパフォーマンスの最適化 &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics/analyze/analysis-workspace/workspace-faq/optimizing-performance)
* [Report Builderのトラブルシューティングとベストプラクティス：リクエストの最適化に関する推奨事項 &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics/analyze/legacy-report-builder/troubleshoot#section_33EF919255BF46CD97105D8ACB43573F)
* [Analytics コンポーネントガイド：予定レポートキュー &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics/components/scheduled-reports-admin)

### 休日のメンテナンス計画

Adobeでは、通常、ピーク時の休憩時間に **メンテナンスを含まない時間帯** を実施して、サービスが中断されないようにします。 AdobeのリリースおよびメンテナンススケジュールをExperience Leagueでモニタリングし、Adobe アカウントチームと調整してサポート計画を立てる必要があります。

これらのガイドラインに従い、Adobeの公開ドキュメントを活用することで、Adobe Analyticsの実装が堅牢でレスポンシブ、かつホリデーシーズンの需要に対応していることを確認できます。

+++

## Adobe Target ホリデー対応ガイド {#target}

+++**クリックして、Adobe Targetの休日に対する準備状況の推奨事項を確認します。**

ホリデーシーズンにはエンゲージメントの高いチャンスが訪れるだけでなく、トラフィックサージやパーソナライゼーションシステムへの需要の増加などの課題も伴います。 この重要な期間にシームレスなエクスペリエンスを提供できるように、Adobe Targetの実装の準備が整っていることを確認するために、主要な推奨事項をまとめました。

### 需要を予測

まず、20～50% 以上のトラフィックスパイクを予測し、インフラストラクチャが負荷を処理できることを検証します。 Adobe Target、Analytics、AEPをまたいでアクティビティとデータ量を予測し、予期せぬ事態の発生を防ぎます。

また、チェックアウト、製品のお勧め、プロモーションオファーなど、ミッションクリティカルなジャーニーを特定して、パーソナライゼーションの取り組みが最も重要な部分に集中できるようにすることも重要です。

[Adobe Targetを使用した最適化のベストプラクティス &#x200B;](https://experienceleague.adobe.com/ja/docs/target-learn/tutorials/administration/strategy/target-best-practices-for-optimization) を参照してください。

### スケールの準備

* Web サイトやモバイルデバイスでのトラフィック増加に備えて計画し、Target サポートチームに対して、呼び出しがブロックされないようにサーバー容量を増やすように通知します。
* 負荷/ペンテストを行う場合は、事前に Target サポートチームにお知らせください。
* 最新バージョンの `at.js`/配信 API にアップグレードしてください。
* 重要でない変更を凍結し、フォールバックエクスペリエンスに備える。
* サポートプロセスとエスカレーションプロセスを調整し、プロアクティブなアラートを有効にします。

### テストと検証

[QA リンク &#x200B;](https://experienceleague.adobe.com/ja/docs/target/using/activities/activity-qa/activity-qa) を使用してコンテンツ配信を検証し、すべてが期待どおりに動作することを確認します。 「**[!UICONTROL オーディエンスを一致させるルールを使用してエクスペリエンスを表示]**」切替スイッチを使用して、適切なオーディエンスがテストしているアクティビティに適格であることを確認します。 **[!UICONTROL 目標指標]** の設定がアクティビティの **[!UICONTROL 目標]** に合っていることを再確認します。 万一に備えて、常にバックアップ計画を用意しておいてください。

### ベストプラクティス

実装を [Adobe Targetの制限内に保ち &#x200B;](https://experienceleague.adobe.com/ja/docs/target/using/troubleshoot/target-limits) 立ち上げる前に、事前に [GDPR および CCPA への準拠 &#x200B;](https://experienceleague.adobe.com/ja/docs/target-dev/developer/implementation/privacy/cmp-privacy-and-general-data-protection-regulation) を確認してください。 アクティブなアクティビティを 100 個未満に維持し、古いアクティビティをアーカイブして作業を効率化します。 **[!UICONTROL 自動配分]**/**[!UICONTROL 自動ターゲット]** を活用して、AI による最適化を実現します。 ロールバックプランとリアルタイム監視ダッシュボードを確立します。

### セキュリティとガバナンス

エクスペリエンスをパーソナライズする前に、GDPR および CCPA の下で同意のコンプライアンスを確認します。 個人を特定できる情報（PII）のプロファイルパラメーターへの保存を避け、顧客データを保護するための API セキュリティを検証します。

+++
