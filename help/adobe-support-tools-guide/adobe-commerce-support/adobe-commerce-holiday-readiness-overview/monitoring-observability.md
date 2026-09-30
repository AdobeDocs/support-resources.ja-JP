---
title: 監視と監視
description: Adobe Commerceを利用しているマーチャントが、ホリデーシーズンなどの交通量の多いイベントに備えるためのモニタリングとオブザーバビリティに関する推奨事項。
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: 4239b8a6-e74f-567d-a7a5-b98b9ead0ea4
    internal-label: Observability
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: 3c398179-d35a-51ba-b317-6c5b95feef5e
    internal-label: Logs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 71589dd124714805fbf844540fb2d272433631ee
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 2%
---

# 監視と監視

このセクションでは、ホリデーシーズンなどのトラフィックの多いイベントに備えて、Adobe Commerce環境を監視するための技術的な推奨事項を提供します。

>[!NOTE]
>
>**（クラウドのみ）**&#x200B;とマークされた手順は、クラウドインフラストラクチャ上のCommerceに適用されます。 その他のほとんどの推奨事項は、オンプレミスのデプロイメントにも適用されます。

## New Relicによるトラフィックのモニタリング（クラウドのみ） {#monitor-traffic-with-new-relic}

Adobe Commerce on cloud infrastructureには、[!DNL New Relic] オブザーバビリティ プラットフォーム サブスクリプションが含まれており、[!DNL Fastly]件のログが[!DNL New Relic]にストリーミングされ、ほぼリアルタイムでシームレスに組み込まれます。 この統合により、トラフィックパターンと傾向をリアルタイムで監視できるため、是正措置を講じることができます。

これらのログを使用して、以下を行います。

* web リクエストの送信元の国を特定します。
* サイトをクロールしている不正なIP アドレスやユーザーエージェントを発見。
* 支払いなどの特定のエンドポイントをターゲットとする悪意のあるトラフィックを特定します。
* 顧客が使用するデバイスとブラウザーのタイプに関するレポートを作成できます。

例えば、トラフィックのソース国を監視して、プロモーションと顧客の地理的な場所を反映していることを確認します。

```sql
SELECT count(*) FROM Log
WHERE cache_status IS NOT NULL
AND project_id = '<YOUR_PROJECT_ID>'
AND (content_type LIKE 'text/html;%' or url LIKE '%graphql%' or url like '%rest%')
FACET geo_country_code
SINCE 7 days ago until today
```

このクエリをニーズに合わせて変更したり、さらにセグメント化したり、一元的に追跡するためのダッシュボードに変えたりできます。 詳しくは、[New Relic ログ管理](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/monitor/new-relic/log-management)を参照してください。

## New Relic アラートのカスタマイズ（クラウドのみ） {#customize-new-relic-alerts}

Adobe Commerceのクラウドインフラストラクチャで設定されるマネージドアラートに加えて、セールスシーズンのピーク時に、GraphQLのクエリでボットトラフィックや応答時間の増加を通知するなど、様々なアラートや通知をプラットフォームに設定できます。 組み込みアラートの完全なリストについては、[Adobe Commerceの管理アラート &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-operations/tools/managed-alerts-for-adobe-commerce/managed-alerts-for-magento-commerce)を参照してください。

[!DNL New Relic]個のアラートとAIがNRQL ベースのクエリ構造をサポートしています。 **[!UICONTROL アラートとAI]**&#x200B;の下の[!DNL New Relic] ダッシュボードからカスタムアラートを設定します。

## Apdex スコアのレビュー（クラウドのみ） {#review-apdex-score}

Apdex スコアは、web アプリケーションやサービスの応答時間に対するユーザー満足度を測定します。 [!DNL New Relic]を使用して、Adobe Commerce on cloud infrastructureのApdex スコアを確認できます。

Apdex スコアは0から1の範囲です。 スコアが0の場合は最も悪いスコアとなり、回答率の100%が&#x200B;**不満**&#x200B;でした。 スコアが1の場合は可能な限り最適なスコアとなります。つまり、応答時間の100%が&#x200B;**件の満足度**&#x200B;でした。 [!DNL New Relic]は、バックエンドのパフォーマンスを反映するApp Server スコアと、クライアント側のパフォーマンスを反映するエンド ユーザーのスコアの両方をレポートします。

Apdex スコアが0.5以下の場合、調査が保証されます。 スコアが0.4未満の場合は障害とみなされます。

[!DNL New Relic]は、Apdexと共に、クラウドインフラストラクチャ上のAdobe Commerceのパフォーマンスの問題を分析するための様々な統計情報を提供します。 手順については、[Adobe CommerceでのNew Relicを使用したパフォーマンスのトラブルシューティング &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/troubleshoot-performance-using-new-relic-on-magento-commerce)を参照してください。

## サポートインサイト（SWAT レポート）の確認 {#review-support-insights-swat-report}

環境に関する詳細なレポートを入手するには、サイト全体の分析ツール（SWAT）レポートを生成します。 SWAT ツールについて詳しくは、[&#x200B; サイト全体の分析ツール &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-operations/tools/site-wide-analysis-tool/intro)を参照してください。