---
title: Adobe Commerceの MySQL のサポート終了通知とデータベース互換性ガイダンス
description: この記事では、MySQL のサポート終了のタイムラインと、サポートされているAdobe Commerce バージョンのデータベース互換性ガイダンスについて説明します。
solution: Commerce
source-git-commit: 2198e1882260ca17b8b99f7ed6d415791ec0d177
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# Adobe Commerceの MySQL のサポート終了通知とデータベース互換性ガイダンス

この記事では、MySQL のサポート終了（EOS）と、サポートされているAdobe Commerce版とのデータベースの互換性に関する重要な情報を提供します。
Adobeでは、マーチャントにこの発表を確認し、プラットフォームの安定性を維持し、サポート要件に引き続き準拠するために対策を講じることを強くお勧めします。
詳しくは、[MariaDB のアップグレードの前提条件 &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/maintenance/mariadb-upgrade) と [&#x200B; システム要件 &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/system-requirements) を参照してください。

## MySQL 8.0 のサポート終了（EOS）

MySQL 8.0 は、2026 年 4 月 30 日（PT）にサポート終了（EOS）となります。
この日以降、次のAdobe Commerce バージョンでは、MySQL 8.0 以降にリリースされた MySQL バージョンをサポートまたはサポートしなくなります。

* Adobe Commerce 2.4.7
* Adobe Commerce 2.4.6
* Adobe Commerce 2.4.5

Adobeは、これらのAdobe Commerce リリースの新しい MySQL メジャーバージョンを検証したり、サポートを提供したりしません。

## オンプレミス環境のお客様に必須のアクション

次のバージョンを実行しているAdobe Commerceのオンプレミス インストールでは、データベース サーバを互換性のある MariaDB バージョンに移行することを強くお勧めします。

* 2.4.5
* 2.4.6
* 2.4.7

MariaDB はこれらのリリースで完全にサポートされており、今後の推奨データベースプラットフォームです。

* 2.4.5
* 2.4.6
* 2.4.7

データベース・サーバを互換性のある MariaDB バージョンに移行することを強くお勧めします。
MariaDB はこれらのAdobe Commerceバージョンで完全にサポートされており、推奨されるデータベースプラットフォームです。

## Adobe Commerce 2.4.8 および 2.4.9 での MySQL のサポート

Adobe Commerce 2.4.8 および 2.4.9 は、MySQL をサポートする最新のAdobe Commerce バージョンです。

対象となるバージョンは次のとおりです。
* MySQL 8.4 は、Adobe Commerceでサポートされている最終的な MySQL バージョンです。
* 8.4 以降にリリースされた MySQL バージョンは、Adobe Commerceで認定またはサポートされません。

## 今後の方向性：デフォルトのデータベースプラットフォームとしての MariaDB

今後も、Adobe Commerceは引き続き、デフォルトの推奨データベースプラットフォームとして MariaDB をサポートします。

Adobeでは、長期的な互換性とサポートの連携を維持するために、次のお客様が MariaDB への移行を計画し始めることを強くお勧めします。
* Adobe Commerce 2.4.8 および 2.4.9 のすべてのオンプレミスのお客様
* サポートされている以前のAdobe Commerce バージョンを使用しているお客様
