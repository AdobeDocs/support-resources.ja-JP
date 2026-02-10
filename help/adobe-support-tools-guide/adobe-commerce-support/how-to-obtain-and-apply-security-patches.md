---
title: '[!UICONTROL &#x200B; セキュリティパッチ &#x200B;] の取得および適用方法'
description: この記事では、リリース済みの [!UICONTROL &#x200B; セキュリティパッチ &#x200B;] を取得して適用する方法について説明しますが、説明は入手できません。
source-git-commit: 93ee9bd110930e244befca682fadd3edc24d138a
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# [!UICONTROL &#x200B; セキュリティパッチ &#x200B;] の取得および適用方法

>[!NOTE]
>オンプレミスインストールを使用していて、[!DNL CVS] や GitHub などのバージョン管理システムを使用してコードを管理していない場合は、web ホストがパッチの適用を支援できる可能性があります。 お気軽にお問い合わせください。

この記事では、リリース済みの [!UICONTROL &#x200B; セキュリティパッチ &#x200B;] を取得して適用する方法について説明しますが、説明は入手できません。

## 影響を受ける製品とバージョン

Adobe Commerce オンプレミスおよびクラウドインフラストラクチャ – すべてのサポート対象バージョン


## 原因

ほとんどの [!UICONTROL &#x200B; セキュリティパッチ &#x200B;] は、適用するための独立したパッチやホットフィックスがない状態でリリースされており、[!UICONTROL &#x200B; セキュリティパッチ &#x200B;] リリースにアップグレードする必要があります。

## ソリューション


### ケース I:

* [&#x200B; リリースノート &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-on-cloud/user-guide/release-notes/cloud-tools-suite) に孤立したパッチファイル/ホットフィックスが記載されている場合は、[https://account.magento.com](https://account.magento.com/downloads/view/) のダウンロードセクションからファイルをダウンロードします。 共有アクセスユーザーには、まずアカウント所有者/ライセンス所有者からダウンロード権限が付与されている必要があります。

**注意事項：**

古いバージョンのAdobe Commerce（2.4.4）を使用している場合は、自動で拡張サポートを受けることができます。 使用可能な最新のセキュリティパッチを適用するには、お使いのバージョンが次のサポートされていないバージョンのいずれかである必要があります。

2.4.4 - 2.4.4-p11

サポートされていないバージョン（2.3.x、2.4.0～2.4.3）はサポート対象外です。最新のセキュリティ修正を利用するには、まずサポートされているバージョンにアップグレードする必要があります。

拡張サポートを受けていない場合、パッチの共有をサポートに依頼することもできますが、パッチの適用時に発生する可能性のある問題やエラーは解決できません。

### ケース II:

独立したパッチは例外的な場合にのみ提供され、セキュリティ修正を実装するための推奨された形式ではありません。

分離されたパッチファイル/ホットフィックスがリリースノートに記載されていない場合：

* **Cloud:**

1. 一部の [!UICONTROL &#x200B; セキュリティパッチ &#x200B;] は、最新バージョンの Cloud Tools Suite （ECE Tools）のCommerce用クラウドパッチの下に含まれているか、リリースされている可能性があります。[&#x200B; リリースノート &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite) を確認し、リリースにセキュリティ修正が記載されている場合は、パッケージをそのバージョンにアップグレードします。
1. リリースノートにセキュリティ修正についての記載がない場合は、引き続きお読みください。

* **クラウドインフラストラクチャまたはオンプレミス：**

* 分離されたパッチファイルまたはホットフィックスが入手できない場合は、[&#x200B; クラウドインフラストラクチャー上のAdobe Commerce 2.4.X を &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version) 最新のパッチバージョン 2.4.X-pY にアップグレードしてください。
* 分離されたパッチファイルまたはホットフィックスが入手できない場合は、[Adobe Commerce バージョン On-Premise](https://experienceleague.adobe.com/ja/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade) 2.4.X を最新のパッチバージョン 2.4.X-pY にアップグレードしてください。

## 関連資料

* [2&rbrace;Cloud Infrastructure ガイドのCommerce Cloud Adobe Commerce ツールスイートのリリースノート &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite) を参照してください *。*
* [2&rbrace;Cloud Infrastructure ガイドのAdobe Commerce Adobe Commerce バージョンのアップグレード &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version) を参照してください **
