---
title: '[!UICONTROL &#x200B; セキュリティパッチ &#x200B;]の取得方法と適用方法'
description: この記事では、リリースされた[!UICONTROL &#x200B; セキュリティパッチ &#x200B;]を取得および適用する方法について説明しますが、手順は利用できません。
exl-id: 6764d60e-5088-4a85-90fa-4372570b065b
source-git-commit: 9a4d96e06b949e4c229fdf0f084810b27bf8b346
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 0%

---

# [!UICONTROL &#x200B; セキュリティパッチを取得して適用する方法]

>[!NOTE]
>オンプレミスのインストールがあり、[!DNL CVS]やGitHubなどのバージョン管理システムを使用してコードを管理していない場合、web ホストがパッチの適用を支援できる可能性があります。 アドビの担当者にご連絡いただき、サポートを受けることができます。

この記事では、リリースされた[!UICONTROL &#x200B; セキュリティパッチ &#x200B;]を取得および適用する方法について説明しますが、手順は利用できません。

## 影響を受ける製品とバージョン

Adobe Commerce オンプレミスおよびクラウドインフラストラクチャ – すべてのサポート対象バージョン


## 原因

Adobe Commerce セキュリティ情報の場合、Adobeは、そのアーティファクトが情報の一部として明示的にリリースされた場合にのみ、個別の個別のパッチファイルまたはホットフィックスを提供します。 独立したパッチまたはホットフィックスが公開済みまたは掲示板で参照されていない場合、Adobeは後で個別のスタンドアロンパッチを作成しません。

これは、該当するバージョン行でサポートされているセキュリティリリースの一部として、セキュリティ修正が組み込まれ、検証され、同時にリリースされるためです。

したがって、サポートされる修正パスは、影響を受けるバージョン行に対して公式のセキュリティアップデートを適用するか、既に修正が含まれているバージョンにアップグレードすることです。

## ソリューション


### ケース I:

* 個別のパッチファイル/ホットフィックスが[&#x200B; リリースノート &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-on-cloud/user-guide/release-notes/cloud-tools-suite)に記載されている場合は、[https://account.magento.com](https://account.magento.com/downloads/view/)のダウンロードセクションからファイルをダウンロードしてください。 共有アクセスユーザーには、まずアカウント所有者またはライセンス所有者からダウンロード権限を付与する必要があります。

**注意事項：**

* Adobe Commerce 2.4.6は、2027年8月30日まで延長サポートで引き続きサポートされます。

* Adobe Commerce 2.4.5は、2026年8月11日まで延長サポートの対象となります。 この日付以降、Adobeでは2027年5月31日までのセキュリティフィックスのみが提供されます。

* Adobe Commerce 2.4.4は、拡張サポートの対象ではなくなりました。 Adobeでは、2027年5月31日（PT）までのセキュリティフィックスのみが提供されます。

* Adobe Commerce 2.4.4および2.4.5の場合、Adobeはセキュリティパッチファイルのみを提供します。 これらの更新には次は含まれません。

   * Adobe Commerce サポートまたはエンジニアリングサポート
   * 品質パッチ
   * プラットフォームまたはオペレーティングシステムの依存関係の更新

サポートされていないバージョン（2.3.xおよび2.4.0～2.4.3）は、サポート対象外です。 サポートされているバージョンにアップグレードすると、最新のセキュリティ修正を受け取ることができます。

### ケース II:

分離されたパッチは、例外的な場合にのみ提供され、セキュリティ修正を実装するための好ましい方法ではありません。

独立したパッチファイルまたはホットフィックスがリリースノートに記載されていない場合は、次のガイドラインに従ってください。

>[!IMPORTANT]
>
>セキュリティ上の問題について、分離されたパッチファイルまたはホットフィックスが明示的にリリースされていない場合は、影響を受けるリリースラインの最新のパッチバージョンに完全なAdobe Commerce アプリケーションをアップグレードします。

**クラウド：**

1. 一部の[!UICONTROL &#x200B; セキュリティパッチ &#x200B;]は、最新バージョンのCloud Tools Suite （ECE Tools）に含まれたり、リリースされたりする可能性があります。Cloud Patches for Commerceの下で、[&#x200B; リリースノート &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite)を確認してください。リリースにセキュリティ修正が記載されている場合は、パッケージをそのバージョンにアップグレードしてください。
1. リリースノートにセキュリティ修正が記載されていない場合は、引き続きお読みください。

**クラウド インフラストラクチャまたはオンプレミス：**

* 分離されたパッチファイル/ホットフィックスが使用できない場合は、[&#x200B; クラウドインフラストラクチャ上のAdobe Commerce バージョン &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version) 2.4.Xを最新のパッチバージョン 2.4.X-pYにアップグレードします。
* 分離されたパッチファイル/ホットフィックスが使用できない場合は、[Adobe Commerce版オンプレミス &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade) 2.4.Xを最新のパッチバージョン 2.4.X-pYにアップグレードします。

## 関連トピックス

* Commerce Cloud Tools Suite[&#128279;](https://experienceleague.adobe.com/ja/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite)の リリースノート（*Adobe Commerce on Cloud Infrastructure ガイド*）を参照してください。
* *Adobe Commerce on Cloud Infrastructure ガイド*&#x200B;の「[Adobe Commerce バージョンをアップグレードする](https://experienceleague.adobe.com/ja/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version)」を参照してください。
