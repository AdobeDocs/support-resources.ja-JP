---
title: ' [!DNL Adobe Commerce on cloud pro infrastructure]のファクトシートの監視'
description: このドキュメントでは、Adobe Commerce インフラストラクチャの監視と通知について説明します。
exl-id: 0dd3239f-de10-48df-b3f4-ac2b8cbc6c72
TQID: https://experienceleague.adobe.com/H7CvXHTRGGHEh079EB2rOZV2yc7BoFMQgdq5-yLkjF4
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: d1c3158bb425e7966ccc5e5d79457c6b33e00063
workflow-type: tm+mt
source-wordcount: 511
ht-degree: 0%

---

# [!DNL Adobe Commerce on cloud pro infrastructure]のファクトシートの監視

このドキュメントでは、Adobe Commerce インフラストラクチャの監視と通知について説明します。

マーチャント、システムインテグレーター、Adobeの社内チームは、監視によって、サイトの空き状況やディスク容量の不足をトラブルシューティングできます。

## 問題のトラブルシューティングと解決

Adobe Commerce インスタンスには、通常、カスタムコードと設定が含まれています。 Adobeでは、カスタムコードと設定に関する問題をサポートまたは解決しません。 Adobeは、マーチャントがナレッジベースの問題をトラブルシューティングして特定し、予防と解決のために推奨されるソリューションとベストプラクティスを提供するのに役立ちます。 以下の表を使用して、何が監視され、誰が解決の責任を負うかを理解することをお勧めします。

通知がトリガーされると、Adobe Commerce サポートチームが問題をトリアージします。 トリアージの一部として、エラーログやその他のリソースが分析されます。 トリアージに基づいて、問題を解決するために、マーチャントまたはパートナー（カスタム更新の場合）またはAdobeの社内チームに対して、追加の[!DNL Zendesk] サポートチケットが作成されます。

## Adobe Commerce：デフォルトのモニタリング

以下のイベントは監視され、Adobe Commerce チームは特定された問題を解決し、報告するために必要な手順を実行します。

## サイト可用性モニタリング

| サイトの可用性 | 説明 |
|------------|------------|
| **目標の監視** | サイトの空き状況を追跡します。 |
| **上でインストルメント化** | 高[!DNL SLA]のシングル [!DNL URL]が選択されました。 |
| **説明** | サイトの可用性は、指標に設定されたしきい値にもとづいて決定されます。 チェックが10分間失敗し、進行中のアクティブなデプロイメントがない場合、サイト停止の通知がトリガーされます。 |
| **通知の受信者** | Adobeとのパートナーシップについて話します。 |
| **Adobeによるアクション** | 問題がAdobe Commerce インフラストラクチャ上にある場合のトリアージと修正を担当します。 |
| **マーチャントによるアクション** | マーチャント/パートナーによって導入された変更またはカスタムコードによって発生した場合の問題の修正を担当します。 トラブルシューティングについては、[&#x200B; サイトダウントラブルシューティング &#x200B;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/site-down-or-unresponsive/magento-site-down-troubleshooter.html)を参照してください。 |

## ディスクスペース監視

| ディスクスペース監視 | 説明 |
|------------|------------|
| **目標の監視** | ディスクスペースの使用状況を追跡します。 |
| **上でインストルメント化** | [!DNL MySQL]個のディスク パーティションとメディア ディスク パーティション。 |
| **指標** | 空きディスク領域は、ホスト上で毎分監視されます。 5%または2 GBの空き容量しか残っていない場合、警告が表示されます。 残りの空き容量に設定されているクリティカルしきい値は2%または1 GBです。 |
| **説明** | 通知は、ホストの空きディスク領域に設定されたしきい値に基づいて送信されます。 追加のディスク容量は、関連するマウント（[!DNL MySQL]またはメディア）に1回自動的に追加され、サイトの停止を防ぎ、販売者がディスク容量をクリアしたり、ディスク使用量が急速に増加する原因となるコードやログを特定して解決したりするための時間を与えます。 |
| **通知の受信者** | Adobeとのパートナーシップについて話します。 |
| **Adobeによるアクション** | サポートチケットを自動的に発行し、関連するマウント（[!DNL MySQL]またはメディア）に追加のディスクスペースが自動的に追加され、サイトの停止を防ぎます。 |
| **マーチャントによるアクション** | 継続的な警告レベルのディスク容量アラートを受け取るには、次を参照してください。 <ul><li>[[!DNL Managed alerts for Adobe Commerce]: ディスク警告アラート &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-operations/tools/managed-alerts-for-adobe-commerce/managed-alerts-for-magento-commerce-disk-warning-alert)</li><li>[[!DNL Managed alerts for Adobe Commerce]: ディスククリティカルに関する警告](https://experienceleague.adobe.com/en/docs/commerce-operations/tools/managed-alerts-for-adobe-commerce/managed-alerts-for-magento-commerce-disk-critical-alert) </li></ul> |
