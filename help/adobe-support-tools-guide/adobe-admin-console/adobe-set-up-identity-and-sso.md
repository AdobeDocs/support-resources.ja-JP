---
title: IDとシングルサインオンの設定
description: Adobe ID、Enterprise ID、Federated IDを使用して、Adobe Admin ConsoleでユーザーIDとシングルサインオン（SSO）を設定する方法について説明します。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 0c2992946f1cdbbcfb44a2baf37888bd05b2253b
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 1%

---

# IDとシングルサインオンの設定

**適用先：** Enterprise

Adobe Admin ConsoleでIDを設定する方法を説明します。 Adobe ID、Enterprise ID、Federated IDを比較し、Adobe アプリケーションへの安全なアクセスのためにシングルサインオン（SSO）を設定します。

IDを設定し、シングルサインオン（SSO）を設定して、従業員が既存の組織資格情報を使用して[ ログイン ](https://adminconsole.adobe.com/settings/)できるようにします。

ここでは、[IDとSSOの設定（YouTube） ](https://youtu.be/V57lU4zaSBs)方法に関するビデオチュートリアルを紹介します。

## 主な用語と概念

### ディレクトリ

Admin Consoleのディレクトリは、ユーザーや認証などのポリシーなどのリソースを保持するエンティティです。 これらのディレクトリは、LDAPまたはActive Directoryに似ています。

### ID プロバイダー（IdP）

ID プロバイダー（IdP）とは、次のような組織のID プロバイダーです。

- Active Directory
- Microsoft Azure
- Ping
- Okta
- InCommon
- シボレス

### 関連するペルソナ

| 役割 | 社会的責任 |
|------|----------------|
| システム管理者 | IdP ディレクトリマネージャーおよびDNS マネージャーと連携して、Admin ConsoleでIDを設定します。 |
| DNS マネージャー | DNS トークンを更新して、ドメインの所有権を検証します。 |
| ID プロバイダー（IdP） ディレクトリマネージャー | IdP ポータルと関連するコネクタを処理します。 |

### Adobe ID

エンドユーザーが作成、所有、管理します。 Adobeが認証を実行し、エンドユーザーがIDを管理します。 [ ストレージモデル ](https://helpx.adobe.com/enterprise/using/storage-for-business.html)に応じて、ユーザーまたは企業はファイルとデータを引き続き管理できます。

エンタープライズストレージモデルに更新された組織の場合、アセットとデータは組織によって管理されます。 更新されていない組織の場合、個人はAdobe ID アセットを所有および管理します。

### Enterprise ID

組織で作成、所有、管理されます。 AdobeはEnterprise IDをホストし、認証を実行しますが、Enterprise IDは組織で管理されます。 管理者がEnterprise IDを作成し、ユーザーに発行します。 管理者は、アカウントを引き継ぐか、Enterprise IDを削除して関連データへのアクセスを完全にブロックすることで、製品およびサービスへのアクセスを取り消すことができます。 詳しくは、[こちら](https://helpx.adobe.com/enterprise/using/setup-enterprise-id.html)をクリックしてください。

### Federated ID

組織によって作成および所有され、フェデレーションを介してエンタープライズディレクトリにリンクされています。 組織は資格情報を管理し、SAML2 ID プロバイダー（IdP）を介したシングルサインオンを処理します。

Federated IDが推奨される要件とシナリオを以下に示します。

- 組織のエンタープライズディレクトリに基づいてユーザーをプロビジョニングする場合。
- ユーザーの認証を管理する場合。
- ユーザーが利用できるアプリやサービスを厳密に制御する必要がある場合。

## シングルサインオンなしでIDを設定

組織が他のアプリケーションでSSOを現在使用していない場合は、Adobe IDまたはEnterprise IDを使用できます。

## Adobe IDの使用

Adobeでは、すべての組織を[ エンタープライズ ストレージ モデル ](https://helpx.adobe.com/enterprise/using/storage-for-business.html)に更新しています。 これにより、ユーザーのアセットとデータをより詳細に制御できるようになります。

Admin Consoleにユーザー[を追加する](https://helpx.adobe.com/jp/enterprise/using/users.html)を開始します。

## Enterprise IDでIDを設定する

SSOを使用せずにユーザーのデータをより詳細に制御する場合は、Enterprise ID ディレクトリを設定できます。 管理者のみがEnterprise IDを作成し、ユーザーに発行します。

Enterprise ID ディレクトリを作成するための要件と手順については、[Enterprise IDを使用した組織の設定](https://helpx.adobe.com/enterprise/using/setup-enterprise-id.html)を参照してください。

## シングルサインオンでのIDの設定

SSOを使用するには、Federated ID アカウントでユーザーIDを設定する必要があります。

Federated IDは、次の場合に推奨されます。

- 利用者が利用できるアプリやサービスを厳密に制御する必要があります。
- ユーザーの認証を管理する必要があります。
- 組織のエンタープライズディレクトリに基づいてユーザーをプロビジョニングする場合。

## 新しいSSO統合の設定

Microsoft Azure AD、Googleなどの一般的なID プロバイダーを使用するか、その他のSAML ベースのIdPを使用して、組織とAdobe製品の間でSSOを設定できます。

**Azure AD** （推奨） - [Azure AD コネクタを使用したSSOとユーザー同期の設定](https://helpx.adobe.com/enterprise/using/sso-setup-azure.html)

**その他のSAML IdP** - [他のSAML プロバイダーとのSSOの設定](https://helpx.adobe.com/enterprise/using/create-directory.html)

**Google** （推奨） - [Google コネクタを使用したSSOとユーザー同期の設定](https://helpx.adobe.com/enterprise/using/setup-sso-google.html)

## 既存のSSO設定の管理

組織とAdobe間でSSOを設定した後は、次の手順を使用して設定を管理および変更します。

ドメインとディレクトリの管理方法について説明します。

- [ ユーザーの管理](https://helpx.adobe.com/jp/enterprise/using/users.html)および[ グループ ](https://helpx.adobe.com/enterprise/using/user-groups..html)
- [ ドメインをディレクトリ ](https://helpx.adobe.com/enterprise/using/add-domains-directories.html#link-domains-to-directoies)にリンクして、ユーザーによるアプリ、サービス、設定へのアクセスを制御します
- [別の組織によって要求されたドメインを使用するようにディレクトリの信頼](https://helpx.adobe.com/enterprise/using/directory-trust.html)を管理する

ID プロバイダーを変更する方法について説明します。

- [ ユーザーの作業を中断せずにIdP](https://helpx.adobe.com/enterprise/using/migrate-authentication-provider.html)を変更する
- [ ディレクトリ間でドメインを移動](https://helpx.adobe.com/enterprise/using/manage-domains-directories.html#move-domains-across-directories)
- [ レガシーディレクトリユーザーの削除](https://helpx.adobe.com/enterprise/using/manage-directory-users.html)
- [古い/要求されていないドメインと空のディレクトリを削除](https://helpx.adobe.com/enterprise/using/manage-domains-directories.html#delete)

## エラーとよくある質問

SSOの設定と管理時のよくある質問とエラーの解決策：

### Azure AD - FAQとトラブルシューティング

#### よくある質問（FAQ）

- [Azure AD コネクタに関するFAQ](https://helpx.adobe.com/enterprise/using/azure-ad-connector-faq.html)
- [ ディレクトリとドメインを削除する方法](https://helpx.adobe.com/enterprise/using/sso-setup-azure.html#Deletedirectoriesandremovedomains)

#### トラブルシューティング

- [ ユーザーがアクセスを拒否しました](https://helpx.adobe.com/enterprise/using/sso-setup-azure.html#sync-issues)
- [同期の問題](https://helpx.adobe.com/enterprise/using/sso-setup-azure.html#sync-issues)

### その他のSAML IdP - FAQとトラブルシューティング

#### よくある質問（FAQ）

[SAML統合に関するFAQ](https://helpx.adobe.com/enterprise/using/sso-faq.html)

#### トラブルシューティング

- [一般的なSSOのトラブルシューティング ](https://helpx.adobe.com/enterprise/kb/tshoot-fed-id.html)
- [ 「アクセスが拒否されました」エラー](https://helpx.adobe.com/enterprise/kb/tshoot-fed-id.html#Error_Access_Denied_logging_in)
- [ 「別のユーザーが現在ログインしています」エラー](https://helpx.adobe.com/enterprise/kb/tshoot-fed-id.html#ErrorAnotheruseriscurrentlyloggedin)
- [SAML トレースを実行](https://helpx.adobe.com/enterprise/kb/perform-a-saml-trace.html)

### Google – よくある質問

- [Google コネクタに関するFAQ](https://helpx.adobe.com/enterprise/using/google-federation-faq.html)
- [ ディレクトリとドメインを削除する方法](https://helpx.adobe.com/enterprise/using/setup-sso-google.html#Deletedirectoriesandremovedomains)

## 会話に参加

共同作業、質問、他の管理者とのチャットを行うには、[ エンタープライズ版およびグループ版コミュニティ ](https://www.adobe.com/go/entcom)を利用してください。

## 法務とプライバシー

- [法的通知](https://helpx.adobe.com/legal/legal-notices.html)
- [ オンラインプライバシーポリシー](https://www.adobe.com/jp/privacy.html)
