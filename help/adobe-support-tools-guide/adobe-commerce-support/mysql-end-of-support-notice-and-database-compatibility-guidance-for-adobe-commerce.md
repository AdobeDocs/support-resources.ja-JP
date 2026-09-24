---
title: Adobe CommerceのMySQL サポート終了のお知らせとデータベース互換性ガイダンス
description: この記事では、サポート対象のAdobe Commerce バージョンのMySQL サポート終了タイムラインとデータベース互換性ガイダンスについて説明します。
solution: Commerce
exl-id: f4ef2b3b-316c-421e-a645-9445cdd13448
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: a4ba265c36bd4ba6c7c563879834f2c59fdc58a4
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 1%
---
# Adobe CommerceのMySQL サポート終了のお知らせとデータベース互換性ガイダンス

この記事では、サポート対象のAdobe Commerce バージョンのMySQL サポート終了（EOS）とデータベースの互換性に関する重要な情報を提供します。
Adobeでは、この発表を確認し、プラットフォームの安定性を維持し、サポート要件に準拠し続けるために行動を起こすことを販売者に強くお勧めします。
詳しくは、[MariaDB](https://experienceleague.adobe.com/ja/docs/commerce-operations/implementation-playbook/best-practices/maintenance/mariadb-upgrade)および[必要システム構成](https://experienceleague.adobe.com/ja/docs/commerce-operations/installation-guide/system-requirements)のアップグレードの前提条件を参照してください。

## MySQL 8.0 サポート終了（EOS）

MySQL 8.0は2026年4月30日にサポート終了（EOS）に達します。
この日付以降、次のAdobe Commerce バージョンは、MySQL 8.0以降にリリースされたMySQL バージョンとの互換性をサポートまたは維持しません。

* Adobe Commerce 2.4.7
* Adobe Commerce 2.4.6
* Adobe Commerce 2.4.5

Adobeでは、これらのAdobe Commerce リリースで新しいMySQL メジャーバージョンの検証やサポートを提供しません。

## オンプレミス顧客に必要なアクション

次のバージョンを実行しているAdobe Commerce オンプレミスのインストールでは、データベースサーバーを互換性のあるMariaDB バージョンに移行することを強くお勧めします。

* 2.4.5
* 2.4.6
* 2.4.7

MariaDBは、これらのリリースで完全にサポートされており、今後お勧めのデータベースプラットフォームです。

* 2.4.5
* 2.4.6
* 2.4.7

データベースサーバーを互換性のあるMariaDB バージョンに移行することを強くお勧めします。
MariaDBは、これらのAdobe Commerce版で完全にサポートされており、推奨されるデータベースプラットフォームです。

## Adobe Commerce 2.4.8および2.4.9でのMySQL サポート

Adobe Commerce 2.4.8および2.4.9は、MySQLをサポートする最後のAdobe Commerce バージョンです。

これらのバージョンの場合：
* MySQL 8.4は、Adobe CommerceでサポートされているMySQLの最終バージョンです。
* 8.4以降にリリースされたMySQL バージョンは、Adobe Commerceでは認定またはサポートされません。

## 将来の方向性：デフォルトのデータベースプラットフォームとしてのMariaDB

Adobe Commerceは今後も、デフォルトおよび推奨されるデータベースプラットフォームとしてMariaDBをサポートし続けます。

Adobeでは、以下のお客様が長期的な互換性を維持し、サポートの調整を行うために、MariaDBへの移行計画を開始することを強くお勧めします。
* Adobe Commerce 2.4.8および2.4.9 オンプレミスのすべてのお客様
* 以前のサポートされているAdobe Commerce バージョンを実行しているお客様
