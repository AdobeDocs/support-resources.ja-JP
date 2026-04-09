---
title: IDの概要
description: 自社のID タイプ（Federated ID、Enterprise ID、Adobe ID、Personal Adobe ID）を把握して選択し、Admin Consoleでのユーザーアクセスを管理します。
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
source-git-commit: c066e95c05f8e8a0953daecda9a220268d325f98
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 5%

---


# IDの概要

エンタープライズおよびチームに適用されます。

AdobeのID管理システムは、管理者がアプリケーションやサービスに対するユーザーのアクセスを作成および管理するのに役立ちます。 Adobeでは、これらのID タイプまたはアカウントを提供して、ユーザーを認証および承認できます。

## Adobe Admin ConsoleのID タイプ

ID タイプにより、組織はユーザーのアカウントとデータをさまざまなレベルで制御できます。 ID モデルの選択は、組織がアセットを保存および共有する方法に大きな影響を与えます。 Federated IDとEnterprise ID モデルは組織で作成および管理されますが、Adobe IDは個人で作成および管理されます。

次の表に、自社に最適なID モデルを選択する方法を示します。

>[!NOTE]
>組織がAdobeのエンタープライズストレージモデルに更新されておらず、個人向けのAdobe IDをまだ使用している場合は、以下の[ID タイプの表](https://helpx.adobe.com/jp/enterprise/using/identity.html#using-personal-adobe-id)の説明を参照してください。

<table>
<thead>
<tr>
<th scope="col">ID タイプ</th>

<th scope="col" style="text-align: center;">
  <img src="./assets/federated-id.png" alt="Federated IDアイコン"><br>
  Federated ID
</th>
<th scope="col" style="text-align: center;">
  <img src="./assets/enterprise-id.png" alt="Enterprise ID"><br>
  Enterprise ID
</th>
<th scope="col" style="text-align: center;">
  <img src="./assets/adobe-id.png" alt="Adobe ID"><br>
  Adobe ID
</th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>主な製品</strong></th>
<td>組織で作成、所有、管理されます。 組織はユーザー認証情報を管理し、SAML2 ID プロバイダー（IdP）を介したシングルサインオン（SSO）を使用します。</td>
<td>組織で作成、所有、管理されます。 検証済みのドメインでユーザーアカウントを作成する独占的な権利を、組織が保持します。</td>
<td>エンドユーザーが作成、所有、管理します。 Adobeが認証を実行し、エンドユーザーがIDを管理します。 <a href="https://helpx.adobe.com/jp/enterprise/using/storage-for-business.html"> ストレージモデル </a>に応じて、ユーザーまたは企業はファイルとデータを引き続き管理できます。 Adobe ID アカウントは、未検証、公開、または信頼できるドメインで作成されます。 以下の備考セクションのポイント 2を参照のこと。</td>
</tr>
<tr>
<th scope="row"><strong>アカウントとデータの所有権</strong></th>
<td colspan="2">組織が所有し管理されている</td>
<td>企業ストレージでは組織所有、ユーザーストレージではユーザー所有</td>
</tr>
<tr>
<th scope="row"><strong>セキュリティとモニタリング</strong></th>
<td colspan="2">
  <ul>
    <li>監査ログ</li>
    <li>コンテンツログ</li>
    <li>共有制限</li>
    <li>組織の認証設定</li>
  </ul>
</td>

<td>
  <ul>
    <li>コンテンツログ</li>
    <li>共有制限</li>
    <li>パスワードポリシー</li>
  </ul>
</td>

</tr>
<tr>
<th scope="row"><strong>パスワードのリセット</strong></th>
<td colspan="2">サポートなし</td>
<td><a href="https://helpx.adobe.com/jp/manage-account/using/change-or-reset-password.html">アカウントのパスワードをリセット</a></td>
</tr>
<tr>
<th scope="row"><strong>Creative Cloud エンタープライズ版およびDocument Cloud エンタープライズ版</strong></th>
<td colspan="3">サポートあり</td>
</tr>
<tr>
<th scope="row"><strong>Creative Cloud グループ版およびDocument Cloud グループ版</strong></th>
<td colspan="2">サポートなし</td>
<td>サポートあり</td>
</tr>
<tr>
<th scope="row"><strong>Experience Cloud</strong></th>
<td colspan="3">サポートあり</td>
</tr>
<tr>
<th scope="row"><strong>おすすめ対象</strong></th>
<td>
  <ul>
    <li>すでにSSOまたはSAMLを使用中の組織</li>
    <li>既存のディレクトリサービス（例：GoogleおよびAzure AD）</li>
    <li>Adobe サービス以外のシステムと容易に統合する必要がある</li>
    <li>ドメインの所有権を証明できる</li>
  </ul>
</td>
<td>
  <ul>
    <li>ドメインの所有権を証明できる</li>
    <li>SSOは不要</li>
  </ul>
</td>
<td>
  <ul>
    <li>Creative Cloud チーム版</li>
    <li>組織は、自分が所有していないドメインを使用することを好む</li>
    <li>パブリックドメイン（Hotmail、Gmailなど）</li>
    <li>Adobe Experience Manager Mobileなどのアプリケーションにアクセス</li>
  </ul>
</td>
</tr>
<tr>
<th scope="row"><strong>基本を学ぶ</strong></th>
<td><a href="https://helpx.adobe.com/jp/enterprise/using/set-up-identity.html">IDの設定</a></td>
<td><a href="https://helpx.adobe.com/jp/enterprise/using/add-domains-directories.html#claim-domains">要求ドメイン</a></td>
<td><a href="https://helpx.adobe.com/jp/enterprise/using/users.html#add-users">ユーザーを追加</a></td>
</tr>
</tbody>
</table>

>[!NOTE]
>
>1. Creative Cloud グループ版のパスワードポリシーは、Creative Cloud グループ版のパスワードポリシーと同じです。
>1. Adobe ID ユーザーは、Adobe IDの資格情報または所有する組織の認証モデル（SSO、2FAなど）を使用して認証を行います。 このような場合、ユーザーは所有組織のSSO ページにリダイレクトされます。 認証後、ユーザーは[&#x200B; ビジネスプロファイルの選択](https://helpx.adobe.com/jp/enterprise/kb/enterprise-id-faq.html#choose-profile)が必要になる場合があります。

## Adobeの個人IDの使用

Adobeでは、すべてのチームとエンタープライズ版のお客様がAdobeのエンタープライズ版ストレージモデルを使用できるようにアップデートしています。 個人のAdobe IDを使用して、会社または学校のAdobe アプリケーションやサービスにアクセスするユーザーがいる場合は、次の表を参照してください。

### パーソナル Adobe ID

<table>
<thead>
<tr>
<th scope="col">ID タイプ</th>
</th>
<th scope="col" style="text-align: center;">
  <img src="./assets/personal-adobe-id.png" alt="Adobe ID"><br>
  パーソナル Adobe ID
</th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>主な製品</strong></th>
<td>エンドユーザーが作成、所有、管理します。 Adobeが認証を実行し、エンドユーザーがIDを管理します。</td>
</tr>
<tr>
<th scope="row"><strong>アカウントとデータの所有権</strong></th>
<td>ユーザー制御</td>
</tr>
<tr>
<th scope="row"><strong>セキュリティとモニタリング</strong></th>
<td>パスワードポリシー。 以下の注意セクションのポイント 1を参照してください。</td>
</tr>
<tr>
<th scope="row"><strong>パスワードのリセット</strong></th>
<td><a href="https://helpx.adobe.com/jp/manage-account/using/change-or-reset-password.html"> アカウントのパスワードをリセットします。</a>以下の注意セクションのポイント 2を参照してください。</td>
</tr>
<tr>
<th scope="row"><strong>Creative Cloud エンタープライズ版およびDocument Cloud エンタープライズ版</strong></th>
<td>サポートあり</td>
</tr>
<tr>
<th scope="row"><strong>Experience Cloud</strong></th>
<td>サポートあり</td>
</tr>
<tr>
<th scope="row"><strong>/に対してのみ使用可能</strong></th>
<td>
  <ul>
    <li>移行前にオンボーディングしたエンタープライズ版およびグループ版のお客様</li>
    <li>Creative Cloud チーム版</li>
    <li>ユーザーの手にコントロールを求める</li>
    <li>Digital Publishing Suiteなどのアプリケーションにアクセス</li>
    <li>ユーザーが組織から分離した後に所有するアセット</li>
  </ul>
</td>
</tr>
<tr>
<th scope="row"><strong>基本を学ぶ</strong></th>
<td><a href="https://helpx.adobe.com/jp/enterprise/using/users.html#add-users">ユーザーを追加</a></td>
</tr>
</tbody>
</table>

>[!NOTE]
>
>1. Creative Cloud グループ版のパスワードポリシーは、Creative Cloud グループ版のパスワードポリシーと同じです。
>1. [enterprise storage](https://helpx.adobe.com/jp/enterprise/using/manage-adobe-storage.html)を使用しているCreative Cloud エンタープライズ版のお客様の場合、管理者はAdobe ID ユーザーをAdmin Consoleに追加できますが、商品プロファイルに追加することはできません。 管理者は、Adobe ID ユーザーを別のID タイプに移行する必要があります。
>1. **Adobe IDのみをサポートする** Adobe ライセンス Web サイトなど、一部の製品およびサービスがあります。

## その他の関連リソース

- [IDの設定](https://helpx.adobe.com/jp/enterprise/using/set-up-identity.html)
- [&#x200B; ユーザーIDの切り替え](https://helpx.adobe.com/jp/enterprise/using/switch-user-identity.html)
- [Admin Consoleの概要](https://helpx.adobe.com/enterprise/using/admin-console-overview.html)
- [教育に関するFAQ](https://helpx.adobe.com/enterprise/using/education-faq.html)
- [&#x200B; ユーザーの追加と管理](https://helpx.adobe.com/jp/enterprise/using/users.html)