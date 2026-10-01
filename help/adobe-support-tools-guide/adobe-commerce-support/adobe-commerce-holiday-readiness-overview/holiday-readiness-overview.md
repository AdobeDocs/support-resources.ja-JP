---
title: Adobe Commerce holiday readiness overview
description: ホリデーシーズンなどのトラフィックの多いイベントに備えて、クラウドインフラストラクチャ環境でAdobe Commerceを準備するためのエグゼクティブレベルのガイダンス。
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
TQID: 'https://experienceleague.adobe.com/63svzoaJbKTgiO3iJR3iCyr4-slOLmt4QaVT2Y--NYI'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
    internal-label: Cloud architecture
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 7ffe3c23f94b67342f02ed655d0a1700dd8f5a02
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%
---

# Adobe Commerce holiday readiness overview

このプレイブックでは、ホリデーシーズンなど、交通量の多いイベントに備えてAdobe Commerce環境を準備するためのガイダンスを提供します。 技術的なアドバイスを、次の5つの戦略的重点分野に統合します。

- パフォーマンスの最適化
- ベストプラクティスと安定性
- 監視と監視
- スケーラビリティとキャパシティプランニング
- 運用上の準備状況

これらの重点エリアは、プラットフォームが安定し、安全で、ピーク時の負荷でもパフォーマンスを維持することを保証するのに役立ちます。

## パフォーマンスの最適化

パフォーマンスを最適化するために推奨される手順の概要を次に示します。 詳しくは、[Adobe Commerceの休暇準備状況/パフォーマンスの最適化](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/performance-optimization.md)を参照してください。

* Fastly リクエストキャッシュを最適化する：プロモーションのトラッキングパラメーターを標準化し、ランディングページがキャッシュ可能であることを確認し、PWAまたはヘッドレスストアフロントでGraphQL GETを使用して、Fastlyのキャッシュヒット率を高めます。
* Fastly IOを有効にする：Fastly画像最適化とDeep IOをオンにして、画像変換をオリジンではなくCDN エッジで実行し、画像が多いストアフロントでのページレンダリング時間を短縮します。
* L2 キャッシュを有効にする：キャッシュデータを各web ノードにローカルに保存して、Adobe Commerceのバージョンに応じて、遅延を削減し、Redis/Valkeyへのネットワーク呼び出しを減らします。 Redis キャッシュは、Adobe Commerce 2.4.9または2.4.5-p16、2.4.6-p14、2.4.7-p9、および2.4.8-p4以降のパッチリリースではサポートされていません。
* スレーブ接続を有効にする：読み込み量の多いクエリを`MYSQL_USE_SLAVE_CONNECTION`と`REDIS_USE_SLAVE_CONNECTION`または`VALKEY_USE_SLAVE_CONNECTION`のレプリカノードにルーティングして、マスターデータベースが読み込み中のボトルネックにならないようにします。
* 非同期の注文とメール処理を可能にする：キューの注文プレースメント、注文データのグリッド更新、チェックアウトメールを3つの別々の設定でバックグラウンドで実行するため、チェックアウトは高注文量でも高速に保たれます。
* インデクサーをスケジュール時に更新モードに切り替える：customer_grid インデクサーを除く、カタログの頻繁な更新中にロックを避けるために、「保存時に更新」から「クローンドリブン型スケジュール時に更新」モードにインデクサーを移動します。
* スケーリングされた（分割）アーキテクチャを検討する：チューニングとコードレベルの修正でCPUが負荷の下で最大化されたままになっている場合は、webとデータベースノードを独立してスケーリングする6 ノードのスプリットティア設定に移行します。

## ベストプラクティスと安定性

以下に、インスタンスの安定性を確保するためのベストプラクティスの概要を示します。 それぞれの手順について詳しくは、[Adobe Commerceの休暇準備/ベストプラクティスと安定性](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/best-practices-stability.md)を参照してください。

* 最新バージョンにアップグレードする：サポートされているリリースを維持して、各バージョンにAdobeのセキュリティ修正とパフォーマンスの向上を維持します。
* 最新のECE ツールと品質パッチツール（QPT）をインストールする：ECE ツールを依存関係で更新し、該当する品質パッチツールの修正がクラウドとオンプレミスの両方に適用されていることを確認します。
* ログファイルの確認とクリーニング：デバッグログを削除し、繰り返し発生するエラーを監視して、ディスクの過剰使用を防ぎ、ログの可視性を向上させます。
* ディスクサイズの増加を監視：共有ファイルとデータベースボリュームの使用率を70%未満に抑え、ストレージの増加によって障害がトリガーしないようにします。
* 低速なデータベースクエリを確認する：APM ツールとMySQLの低速クエリログを使用して、ピーク時のトラフィックで複合化する前にコストのかかるクエリを見つけて修正します。
* cron ジョブを正しく設定する：Commerceのすべての非同期処理はcronに依存するため、cronが正しいユーザーの下で毎分実行されることを確認します。
* クライアントサイドの設定を最適化する：CSS、JavaScript、HTMLの縮小とバンドルをオンにして、ストアフロントの読み込み時間を短縮します。

## 監視と監視

繁忙期にAdobe Commerce インスタンスをモニタリングする場合にお勧めの方法を以下に示します。 これらの監視および観測可能性の推奨事項の詳細な手順については、[Adobe Commerceの休暇準備状況> Monitoring and Observability](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/monitoring-observability.md)を参照してください。

* New Relicでトラフィックを監視する：New RelicにストリーミングされているFastlyのログを使用して、トラフィックの異常値、不正なIP、支払いなどのエンドポイントをターゲットにした悪意のあるリクエスト、デバイスやブラウザーのトレンドを検出します。
* New Relicアラートをカスタマイズする：Adobeのマネージドアラートに加えて、通常とは異なるトラフィックへの対応、GraphQLのクエリの遅延、エラー率の上昇などに対して、独自のNRQL ベースのアラートを設定できます。
* Apdex スコアを追跡：Apdex スコア（目標≥0.85）を確認して、バックエンドとフロントエンドの応答時間を、利用者が満足できると考える範囲に保ちます。
* サポートインサイト（SWAT レポート）を確認する：イベントのピーク前とピーク後にSWAT レポートを実行して、システムレベルのリスクと改善点を特定します。

## スケーラビリティとキャパシティプランニング

各スケーラビリティとキャパシティプランニングに関する推奨事項の詳細な手順については、[Adobe Commerceの休暇準備/スケーラビリティとキャパシティプランニング &#x200B;](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md)を参照してください。

* クラスターのアップサイズを早期に計画する：Adobe サポートから一時的なコンピューティングアップサイズをリクエストします。少なくとも10営業日前にメジャープロモーションを行います。
* Fastly オリジンのシールドを有効にする：オリジンの近くのShield POPを介してキャッシュされていないリクエストをルーティングし、オリジンのサーバーに直接ヒットするリクエストを減らします。
* 負荷とフェイルオーバーテストを実施する：主要なキャンペーンよりも負荷と復旧のシナリオを事前にテストして、規模とロールバックプランが実際に停止していることを確認します。

## 運用上の準備状況

* すべてのセキュリティパッチとパフォーマンスパッチを適用する：コードがフリーズする前にすべてのパッチを終了して、デプロイメントが後で中断されないようにします。
* 休日の前にヘルスチェックを実行する：バックアップ、クローンのヘルス、およびキャッシュのウォームアップスクリプトをテストして、負荷の下で操作がスムーズに実行されるようにします。
* モニタリングプレイブックを確立する：アラートのしきい値、エスカレーションパス、24時間週7日の連絡先を文書化して、ピーク時にチームが迅速に対応できるようにします。
* ドキュメントのロールバックプラン：バージョン管理されたロールバック戦略を準備しておくことで、不適切なデプロイメントから迅速に回復できます。