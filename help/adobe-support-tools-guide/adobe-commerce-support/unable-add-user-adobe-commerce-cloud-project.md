---
title: Adobe Commerce クラウドプロジェクトにユーザーを追加できない
description: ここでは、Adobe Commerce クラウドプロジェクトにユーザーを追加できない場合の解決策を説明します。
feature: Cloud, Paas
solution: Commerce
feature-set: Commerce
role: Developer
exl-id: 2dc52d5e-0930-48c4-986e-ce3f9f6f8221
source-git-commit: 755c6dc9cff041b9ca9183fbecde21f90fbaee1a
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 1%

---

# Adobe Commerce クラウドプロジェクトにユーザーを追加できない

この記事では、クラウドプロジェクトにユーザーを追加しようとして、*ユーザー XXX が存在しません* というエラーが発生して追加できない場合の解決策を説明します。

## 影響を受ける製品とバージョン

* クラウドインフラストラクチャー上のAdobe Commerce[ サポート対象のすべてのバージョン ](https://magento.com/sites/default/files/magento-software-lifecycle-policy.pdf)

## 問題

ここでは、Adobe Commerce クラウドプロジェクトにユーザーを追加できない場合の解決策を説明します。

## 原因

ユーザーをユーザーとしてプロジェクトに追加するには、まずユーザーのアカウントを [0}https://accounts.magento.cloud} で作成し、Adobe SSO にリンクしている必要があります。 ](https://accounts.magento.cloud)ユーザーがAdobe アカウントを持っていて、Commerce（magento.com）アカウントを持っていない場合は、まず作成する必要があります。

## ソリューション

1. [https://accounts.magento.cloud](https://accounts.magento.cloud) でログインするようにユーザーに依頼します。 ユーザーは、同じメールアドレスを使用して既にAdobeに登録されている必要があります。
   >[!NOTE]
   >[https://account.adobe.com](https://account.adobe.com) でアカウントを作成または持っていることが、ユーザーが [https://accounts.magento.cloud](https://accounts.magento.cloud) でアカウントを持っていることを自動的に意味しているわけではありません。 最初に [Commerce アカウントを作成 ](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account) する必要があります。

1. ユーザーが既にAdobe アカウントを持っていて、ログインできない場合は、[ 問題の理由 ](https://experienceleague.adobe.com/home#support) を [!UICONTROL User Management] に設定して、*サポートリクエスト* を送信するように依頼します。

1. ユーザーが [https://accounts.magento.cloud](https://accounts.magento.cloud) に正常にログインしたら、ユーザーをプロジェクトに追加できます。 詳しい手順については、Cloud Infrastructure ガイドの [ ユーザーの追加とアクセスの管理 ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/project/user-access#add-users-and-manage-access) を参照してください。Commerce

## 関連資料：

* Commerce on Cloud Infrastructure ガイドの [ ユーザーアクセスの管理 ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html)。
* [Adobe Commerce サポートまたは Cloud アカウントにログインできない ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-to-log-in-to-support-or-cloud-project.html)
