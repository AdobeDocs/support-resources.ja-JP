---
title: スケーラビリティとキャパシティプランニング
description: Adobe Commerceを利用するマーチャントは、ホリデーシーズンなどの交通量の多いイベントに備えるための拡張性とキャパシティプランニングに関する推奨事項を確認できます。
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
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
source-git-commit: 71589dd124714805fbf844540fb2d272433631ee
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%
---

# スケーラビリティとキャパシティプランニング

このセクションでは、ホリデーシーズンなどのトラフィックの多いイベントに備えて、Adobe Commerce環境を拡張するための技術的な推奨事項を提供します。

>[!NOTE]
>
>**（クラウドのみ）**&#x200B;とマークされた手順は、クラウドインフラストラクチャ上のCommerceに適用されます。 その他のほとんどの推奨事項は、オンプレミスのデプロイメントにも適用されます。

## クラスターのアップサイズを早期に計画する（クラウドのみ） {#plan-cluster-upsize-early}

Commerce オンクラウドインフラストラクチャのお客様の場合、一時的なクラスターアップサイズにより、より多くのコンピューティングリソースが割り当てられ、ピークシーズンのトラフィックの急増に対応できます。 日付範囲と必要なクラスターサイズを事前にサポートチケットを発行し、現在のリソース使用量と要件について専用のアカウントマネージャーと調整します。 キャパシティが必要になる少なくとも48営業時間前にリクエストを送信します。特にホリデーシーズンは、ブラックフライデーとサイバーマンデーのキャパシティが限られているため、できるだけ早く送信します。 [一時的なアップサイズをリクエストする方法](https://experienceleague.adobe.com/ja/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/how-to-request-temporary-adobe-commerce-on-cloud-infrastructure-upsize)を参照してください。

例えば、1日のベースラインが24 コア（24 vCPU、96 GB RAM）で、96 コアに7日間のアップサイズを行うプロアーキテクチャのお客様は、リソース（96 vCPU、384 GB RAM）の約4倍を使用します。これは、約504 vCPU-days （96×7−24×7）の増分消費です。

## Fastly オリジンシールド {#fastly-origin-shielding}

Adobe Commerce [!DNL Fastly]のオリジン シールドの目的は、Adobe Commerce オリジンへのトラフィックを直接減らすことです。 リクエストを受信すると、[!DNL Fastly] エッジの場所（Point of Presence）がキャッシュされたコンテンツをチェックして配信します。 キャッシュされていない場合は、Shield POPに続いて、そこにキャッシュされているかどうかを確認します。コンテンツが別のグローバル POPからも以前にリクエストされている場合は、キャッシュされます。 最後に、Shield POPにキャッシュされていない場合は、オリジンサーバーに進むだけです。

[!DNL Fastly] オリジンのシールドは、[!DNL Fastly]設定のバックエンド設定で、Adobe Commerce管理者で有効にできます。 最高のパフォーマンスを得るには、Adobe Commerce origin データセンターに最も近いシールドの場所を選択してください。 詳しくは、[&#x200B; バックエンドとオリジンシールドの設定](https://experienceleague.adobe.com/ja/docs/commerce-on-cloud/user-guide/cdn/setup-fastly/fastly-custom-cache-configuration#configure-back-ends-and-origin-shielding)を参照してください。

デフォルトでは、[!DNL Fastly] オリジン シールドは有効になっていません。

## 負荷およびフェイルオーバーテストの実施 {#conduct-load-and-failover-tests}

主要なキャンペーンの前に読み込みテストと回復テストを実行し、スケーリング設定とロールバックプランを検証します。