---
title: クラウドインフラストラクチャ上のAdobe Commerceのホリデーサージキャパシティのリクエスト
description: ホリデーシーズンの繁忙期（11月中旬～1月中旬）には、Adobeでは、クラウドインフラストラクチャでホストされているすべてのAdobe Commerceマーチャントに対して、トラフィックの増加に備えることをお勧めします。
feature: Support
feature-set: Commerce
role: Admin
source-git-commit: e6ae0022bac9c91eb52c76a6b7a8d8f6c45257cb
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 0%

---

# クラウドインフラストラクチャ上のAdobe Commerceのホリデーサージキャパシティのリクエスト

ホリデーシーズンの繁忙期（11月中旬～1月中旬）には、Adobeでは、クラウドインフラストラクチャでホストされているすべてのAdobe Commerceマーチャントに対して、トラフィックの増加に備えることをお勧めします。

包括的なクロスソリューションのチェックリストと、繁忙期に向けてシステムやチームを準備するためのベストプラクティスについては、[Adobe DX Unified Holiday Readiness Guide](https://experienceleague.adobe.com/en/docs/support-resources/data-sheets/unified-holiday-readiness)を参照してください。

**トラフィックの計画と見積もり**

クラウドインフラストラクチャ [のすべてのAdobe Commerce マーチャントは、毎年の繁忙期の繁忙期の繁忙期のトラフィックを推定する方法](https://business.adobe.com/blog/how-to/the-5-ps-of-peak-season-performance-a-guide-to-preparing-your-infrastructure-for-high-traffic)に関する推奨事項を活用することをお勧めします。

推奨される見積もりが完了したら、追加のキャパシティが必要になると思われる日付をチームが特定した場合は、次の手順に進んで、サージキャパシティをリクエストする方法について説明します。

**アップサイズの履歴を表示**

**CSM （カスタマーサクセスマネージャー）**から情報をリクエストすることで、要求されたサイズ変更の履歴を表示できます。
サイズ変更リクエストごとに、次の情報を利用できます。

* **サイズ開始日**: アップサイズリクエストの日付。
* **サイズ終了日**: クラスターが前のサイズに戻された日付。
* **vCPU サイズ**: アップサイズ後のクラスターのサイズ。
* **日間の使用状況**：クラスターがアップサイズを維持した日数。
* **期間vCPU**: vCPU サイズを、使用された日数で変更しました。 （例えば、vCPU サイズ 192 x 25日は4,800になります）。

**サージキャパシティを要求しています**

ホリデーシーズン中に追加のキャパシティが必要になることが予想されるクラウドインフラストラクチャのAdobe Commerceのマーチャントは、ヘルプセンターを通じて[ サージキャパシティのサポートチケット ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/how-to/how-to-request-temporary-magento-upsize.html)を送信し、チケット内の日付と予想されるキャパシティのニーズを示す必要があります。 容量を増やすには、ライセンス済みの超過容量を使用する必要があることに注意してください。

**これらのチケットは、容量が必要な場合の48営業時間前までに提出することをお勧めします。また、ブラックフライデー/サイバーマンデー期間のリクエストは、この期間の容量が限られているため、可能な限り事前に行うことをお勧めします。**


**さらにヘルプ？**

繁忙期のトラフィックの準備に関する詳細なガイダンスが必要ですか？ アドビのクラウドインフラストラクチャを使用しているAdobe Commerceをご利用のマーチャントは、Adobeアカウントチームに連絡して、繁忙期を成功させるためのヘルプ、戦略、計画のヒントを入手できます。 また、年間を通じて戦略のヒントを得るには、[Magento ブログ ](https://magento.com/blog)を参照することをお勧めします。

## キャパシティの確認に関するリソース

サポートナレッジベース：

* [ クラウド上のAdobe CommerceのCPU割り当て計算](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/how-to/magento-commerce-cloud-cpu-allocation-calculation.html)
* [ クラウド上のAdobe Commerceにホストのインスタンスのアップサイズが必要かどうかを確認します](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/how-to/magento-commerce-cloud-check-if-upsize-for-hosts-instances-is-needed.html)
* [ クラウド上のAdobe Commerce用のホストのCPU設定を確認](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/how-to/magento-commerce-cloud-check-hosts-cpu-configuration.html)
* [ クラウド上のAdobe Commerceの停止を特定して測定する](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/how-to/how-to-identify-outages.html)
