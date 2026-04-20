---
title: '[!UICONTROL &#x200B; セキュリティパッチ &#x200B;]の取得方法と適用方法'
description: この記事では、リリースされた[!UICONTROL &#x200B; セキュリティパッチ &#x200B;]を取得および適用する方法について説明しますが、手順は利用できません。
exl-id: 6764d60e-5088-4a85-90fa-4372570b065b
source-git-commit: 90775dd524d52669067794469efdd5462af53fc0
workflow-type: tm+mt
source-wordcount: '530'
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

古いバージョンのAdobe Commerce（2.4.4）を使用している場合は、延長サポートが自動的に受け取られます。 利用可能な最新のセキュリティパッチを適用するには、次のいずれかのバージョンがサポートされていない必要があります。

2.4.4 - 2.4.4-p11

サポートされていないバージョン（2.3.x、2.4.0～2.4.3）はサポート対象外であり、最新のセキュリティ修正を利用するには、まずサポート対象バージョンにアップグレードする必要があります。

拡張サポートがない場合は、サポートにパッチを共有するようにリクエストすることはできますが、適用する際に発生する可能性のある問題やエラーを解決することはできません。

### ケース II:

分離されたパッチは例外的な場合にのみ提供され、セキュリティ修正を実装する好ましい方法ではありません。

分離されたパッチファイル/ホットフィックスがリリースノートに記載されていない場合：

* **クラウド：**

1. 一部の[!UICONTROL &#x200B; セキュリティパッチ &#x200B;]は、最新バージョンのCloud Tools Suite （ECE Tools）に含まれたり、リリースされたりする可能性があります。Cloud Patches for Commerceの下で、[&#x200B; リリースノート &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite)を確認してください。リリースにセキュリティ修正が記載されている場合は、パッケージをそのバージョンにアップグレードしてください。
1. リリースノートにセキュリティ修正が記載されていない場合は、引き続きお読みください。

* **クラウド インフラストラクチャまたはオンプレミス：**

* 分離されたパッチファイル/ホットフィックスが使用できない場合は、[&#x200B; クラウドインフラストラクチャ上のAdobe Commerce バージョン &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version) 2.4.Xを最新のパッチバージョン 2.4.X-pYにアップグレードします。
* 分離されたパッチファイル/ホットフィックスが使用できない場合は、[Adobe Commerce版オンプレミス &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade) 2.4.Xを最新のパッチバージョン 2.4.X-pYにアップグレードします。

## 関連トピックス

* Commerce Cloud Tools Suite[の](https://experienceleague.adobe.com/ja/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite) リリースノート（*Adobe Commerce on Cloud Infrastructure ガイド*）を参照してください。
* [Adobe Commerce on Cloud Infrastructure ガイド &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version)の「*Adobe Commerce バージョンをアップグレードする*」を参照してください。
