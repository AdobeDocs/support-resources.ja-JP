---
title: '[!UICONTROL  セキュリティパッチ ]の取得方法と適用方法'
description: この記事では、リリースされた[!UICONTROL  セキュリティパッチ ]を取得および適用する方法について説明しますが、手順は利用できません。
exl-id: 6764d60e-5088-4a85-90fa-4372570b065b
source-git-commit: eee15976f3dd402e84774ec5b769d952259c8dff
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 0%

---

# [!UICONTROL  セキュリティパッチを取得して適用する方法]

>[!NOTE]
>オンプレミスのインストールがあり、[!DNL CVS]やGitHubなどのバージョン管理システムを使用してコードを管理していない場合、web ホストがパッチの適用を支援できる可能性があります。 アドビの担当者にご連絡いただき、サポートを受けることができます。

この記事では、リリースされた[!UICONTROL  セキュリティパッチ ]を取得および適用する方法について説明しますが、手順は利用できません。

## 影響を受ける製品とバージョン

Adobe Commerce オンプレミスおよびクラウドインフラストラクチャ – すべてのサポート対象バージョン


## 原因

ほとんどの[!UICONTROL  セキュリティパッチ ]は、適用する個別のパッチやホットフィックスなしでリリースされ、[!UICONTROL  セキュリティパッチ ] リリースへのアップグレードが必要です。

Adobe Commerceのセキュリティ情報の場合、Adobeでは、個別の物理パッチやホットフィックスファイルのみが提供されます。このファイルは、情報リリースの一部として明示的に公開または言及されている場合にのみ提供されます。 掲示板に個別のパッチ/ホットフィックスパッケージが含まれていない（または参照されていない）場合、事実の後に生成して提供することはできません。

これは、セキュリティ修正プログラムがサポートされているセキュリティリリース（パッチリリースなど）の一部として開発、テスト、および一緒に出荷され、不完全なカバレッジやリグレッションのリスクを冒すことなく、個別のCVE パッチファイルに完全に分離または分離するように設計されていないためです。

サポートされている修正パスは、引き続きバージョン行に対して公式のセキュリティアップデートを適用します（または修正が含まれるバージョンにアップグレードします）。

## ソリューション


### ケース I:

* 個別のパッチファイル/ホットフィックスが[ リリースノート ](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/release-notes/cloud-tools-suite)に記載されている場合は、[https://account.magento.com](https://account.magento.com/downloads/view/)のダウンロードセクションからファイルをダウンロードしてください。 共有アクセスユーザーには、まずアカウント所有者またはライセンス所有者からダウンロード権限を付与する必要があります。

**注意事項：**

古いバージョンのAdobe Commerce（2.4.4）を使用している場合は、延長サポートが自動的に受け取られます。 利用可能な最新のセキュリティパッチを適用するには、次のいずれかのバージョンがサポートされていない必要があります。

2.4.4 - 2.4.4-p11

サポートされていないバージョン（2.3.x、2.4.0～2.4.3）はサポート対象外であり、最新のセキュリティ修正を利用するには、まずサポート対象バージョンにアップグレードする必要があります。

拡張サポートがない場合は、サポートにパッチを共有するようにリクエストすることはできますが、適用する際に発生する可能性のある問題やエラーを解決することはできません。

### ケース II:

分離されたパッチは例外的な場合にのみ提供され、セキュリティ修正を実装する好ましい方法ではありません。

分離されたパッチファイル/ホットフィックスがリリースノートに記載されていない場合：

* **クラウド：**

1. 一部の[!UICONTROL  セキュリティパッチ ]は、最新バージョンのCloud Tools Suite （ECE Tools）に含まれたり、リリースされたりする可能性があります。Cloud Patches for Commerceの下で、[ リリースノート ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite)を確認してください。リリースにセキュリティ修正が記載されている場合は、パッケージをそのバージョンにアップグレードしてください。
1. リリースノートにセキュリティ修正が記載されていない場合は、引き続きお読みください。

* **クラウド インフラストラクチャまたはオンプレミス：**

* 分離されたパッチファイル/ホットフィックスが使用できない場合は、[ クラウドインフラストラクチャ上のAdobe Commerce バージョン ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version) 2.4.Xを最新のパッチバージョン 2.4.X-pYにアップグレードします。
* 分離されたパッチファイル/ホットフィックスが使用できない場合は、[Adobe Commerce版オンプレミス ](https://experienceleague.adobe.com/en/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade) 2.4.Xを最新のパッチバージョン 2.4.X-pYにアップグレードします。

## 関連トピックス

* Commerce Cloud Tools Suite[の](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite) リリースノート（*Adobe Commerce on Cloud Infrastructure ガイド*）を参照してください。
* [Adobe Commerce on Cloud Infrastructure ガイド ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version)の「*Adobe Commerce バージョンをアップグレードする*」を参照してください。
