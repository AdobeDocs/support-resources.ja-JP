---
title: Adobe Admin Console ユーザー
description: Adobe Admin Consoleにおけるユーザー管理戦略の策定：管理者とエンドユーザーの追加、ユーザー管理方法の選択、ライセンスの割り当て
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: d92f4190b68a480409f4126a877de3469ed836f0
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 4%

---

# Adobe Admin Console ユーザー

エンタープライズおよびチームに適用されます。

何らかの課題に直面していませんか？ 問題を選択して解決策を表示します。

- [管理者の役割の管理](https://helpx.adobe.com/jp/enterprise/using/admin-roles.html)
- [&#x200B; ダウンロードとインストールの問題](https://helpx.adobe.com/download-install.html)
- [Enterprise ID ユーザーパスワードのリセット &#x200B;](https://helpx.adobe.com/enterprise/kb/enterprise-id-faq.html#faq)
- [Federated ID エラーの解決](https://helpx.adobe.com/enterprise/kb/tshoot-fed-id.html)
- [&#x200B; ユーザーの削除または削除されたユーザーの復元](https://helpx.adobe.com/enterprise/using/manage-directory-users.html)

**Adobe Admin Console - ユーザー** — [YouTubeを視聴](https://youtu.be/w8b36YX2TEM)

## Adobe Admin Consoleにユーザーを追加する理由

>[!NOTE]
>
>Adobe Admin Consoleの管理者は、[ID タイプ &#x200B;](https://helpx.adobe.com/jp/enterprise/using/identity.html)と[IDを設定](https://helpx.adobe.com/jp/enterprise/using/set-up-identity.html)した後、次の作業としてユーザーをAdmin Consoleに追加します。

Adobe enterpriseとteamsは、次の2種類のユーザーを広く定義しています。

### 管理者（管理者）

エンタープライズ版またはグループ版の管理者は、Admin Consoleで管理タスクを実行します。 管理者を追加すると、Adobe製品へのアクセス、使用、その他の管理タスクをきめ細かく管理できる、柔軟な管理階層を定義できます。

すべての管理者をAdmin Consoleに追加する必要があります。 管理者権限を追加する場合は、管理者権限は[管理者ロール &#x200B;](https://helpx.adobe.com/jp/enterprise/using/admin-roles.html)に基づきます。

### エンドユーザー

エンドユーザーとは、組織または教育機関がAdobeとの契約の一環として取得したAdobeの製品およびサービスを使用する組織または教育機関のユーザーです。

## ユーザー管理戦略の決定

要件に応じて、*個別に* ユーザーを追加、削除、更新するか、使用可能な&#x200B;*バルクアップロード方法*&#x200B;のいずれかを使用します。 ユーザー管理を計画する際は、次のマトリックスを参考にしてください。

>[!NOTE]
>
>Adobeのエンタープライズ版またはグループ版をご利用の場合は、Admin Consoleでのユーザー管理を開始する前に、この表を参照することをお勧めします。 既存顧客は、特に、あるID タイプから別のID タイプに移行する予定がある場合に、これを使用できます（[ID タイプの編集](https://helpx.adobe.com/enterprise/using/switch-user-identity.html)を参照）。

<table>
<thead>
<tr>
<th scope="col"></th>
<th scope="col"><strong>個人向け（Admin Console）</strong></th>
<th scope="col"><strong>CSV一括アップロード（Admin Console）</strong></th>
<th scope="col"><strong>Azure/Googleとのコネクタ</strong></th>
<th scope="col"><strong>ユーザー同期ツール</strong></th>
<th scope="col"><strong>ユーザー管理REST API</strong></th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>適用先</strong></th>
<td colspan="2">Adobe teamsとエンタープライズ版のお客様</td>
<td colspan="3">Adobe エンタープライズ版のお客様</td>
</tr>
<tr>
<th scope="row"><strong>説明</strong></th>
<td>Admin Consoleでユーザーを個別に管理します。</td>
<td>Admin ConsoleでCSV ファイルをアップロードしたユーザーを管理します。</td>
<td>既存のAzure AD ポータルまたはGoogle フェデレーションに基づいて、ユーザー（およびグループ）を管理します。</td>
<td colspan="2">組織のLDAPに基づいてユーザー（およびグループ）を管理します。</td>
</tr>
<tr>
<th scope="row"><strong>ユーザーの追加</strong></th>
<td><strong>Admin Console</strong>の「<strong> ユーザー</strong>」タブ。 <a href="https://helpx.adobe.com/jp/enterprise/using/manage-users-individually.html#add-users">詳細情報</a></td>
<td><strong>Admin Console</strong>で<strong>Add users by CSV</strong>を使用します。 <a href="https://helpx.adobe.com/enterprise/using/bulk-upload-users.html">詳細情報</a>。<em> （デフォルトのCSV テンプレートを使用） </em></td>
<td><a href="https://helpx.adobe.com/enterprise/using/sso-setup-azure.html">Azure</a>または<a href="https://helpx.adobe.com/enterprise/using/setup-sso-google.html">Google</a>にユーザーを追加します。 <strong>Admin Console</strong>経由で送信できます。</td>
<td colspan="2">ユーザーは、組織のLDAPに追加する必要があります。</td>
</tr>
<tr>
<th scope="row"><strong>ユーザーの削除</strong></th>
<td><strong>Admin Console</strong>でユーザーを選択して削除します。 <a href="https://helpx.adobe.com/enterprise/using/manage-users-individually.html#remove-users">詳細情報</a></td>
<td><strong>Admin Console</strong>の「<strong> ユーザー</strong>」タブで「<strong> ユーザーをCSV</strong>で削除」を選択します。 <a href="https://helpx.adobe.com/enterprise/using/bulk-upload-users.html#remove-users">詳細情報</a>。<em> （デフォルトのCSV テンプレートを使用） </em></td>
<td><a href="https://helpx.adobe.com/enterprise/using/sso-setup-azure.html">Google</a>または<a href="https://helpx.adobe.com/enterprise/using/setup-sso-google.html">Azure</a>でユーザーを削除する必要があります。</td>
<td colspan="2">ユーザー情報が同期していることを確認します。 <strong>注意：</strong>組織のLDAPに含まれていないユーザーがAdmin Consoleから削除されます。</td>
</tr>
<tr>
<th scope="row"><strong>ユーザーの詳細を編集</strong></th>
<td>Admin Consoleでユーザーを選択し、<strong> ユーザーの詳細を編集</strong>します。 <a href="https://helpx.adobe.com/enterprise/using/manage-users-individually.html#edit-user-details">詳細情報</a></td>
<td><strong>Admin Console</strong>の「<strong> ユーザー</strong>」タブで「<strong> ユーザーの詳細をCSV</strong>で編集」を選択します。 <a href="https://helpx.adobe.com/enterprise/using/bulk-upload-users.html#edit-user-details">詳細情報</a>。<em> （デフォルトのCSV テンプレートを使用） </em></td>
<td>すべてのユーザー情報は、<a href="https://helpx.adobe.com/enterprise/using/sso-setup-azure.html">Azure</a>または<a href="https://helpx.adobe.com/enterprise/using/setup-sso-google.html">Google</a>で変更する必要があります。</td>
<td colspan="2">ユーザー情報が同期していることを確認します。</td>
</tr>
<tr>
<th scope="row"><strong>サポートされているID タイプ</strong></th>
<td colspan="2">すべて</td>
<td>Federated ID</td>
<td colspan="2">Federated IDとEnterprise ID</td>
</tr>
<tr>
<th scope="row"><strong>最大操作ごとの更新</strong></th>
<td>10</td>
<td>25,000 （<em>5,000、最適なパフォーマンス </em>）</td>
<td colspan="3">無制限（組織のLDAPへのマップ）</td>
</tr>
<tr>
<th scope="row"><strong>要件定義</strong></th>
<td>Adobe Admin Console</td>
<td>Microsoft Excelを使用した.csv ファイル形式の作成と更新</td>
<td>Azure ADまたはGoogle フェデレーションを設定する必要があります</td>

<td>
  <ul>
    <li>macOS ターミナルまたはWindows コマンドプロンプト</li>
    <li>LDAPについて</li>
  </ul>
</td>

<td>REST APIを使用するためのプログラミング言語（Pythonなど）の実用的な知識</td>
</tr>
<tr>
<th scope="row"><strong>詳細情報</strong></th>
<td><a href="https://helpx.adobe.com/jp/enterprise/using/manage-users-individually.html">個々のユーザーの管理</a></td>

<td>
  <ul>
    <li>
      <a href="https://helpx.adobe.com/enterprise/using/bulk-upload-users.html">
        ユーザーの管理| CSVの一括アップロード
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/enterprise/kb/troubleshoot-bulk-user-csv-upload.html">
        ユーザーのCSVの一括アップロードのトラブルシューティング
      </a>
    </li>
  </ul>
</td>

<td>
  <ul>
    <li>
      <a href="https://helpx.adobe.com/enterprise/using/sso-setup-azure.html">
        Azure AD コネクタ
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/enterprise/using/setup-sso-google.html">
        Google フェデレーションコネクタ
      </a>
    </li>
  </ul>
</td>

<td>
  <ul>
    <li>
      <a href="https://adobe-apiplatform.github.io/user-sync.py/en/">
        ユーザー同期について
      </a>
    </li>
    <li>
      <a href="https://github.com/adobe-apiplatform/user-sync.py">
        Git リポジトリ
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/enterprise/using/user-sync.html">
        ステップバイステップガイド
      </a>
    </li>
  </ul>
</td>
<td><a href="https://developer.adobe.com/umapi/">UMAPIについて</a></td>
</tr>
</tbody>
</table>

## 次の手順

### パッケージの作成

ユーザーを追加すると、指定したアプリやサービスを割り当てる準備が整います。

ライセンス方法に基づいて、エンドユーザーにライセンスを割り当てます。

- **ユーザー指定ライセンス：**&#x200B;これらのユーザーを&#x200B;**製品** （[&#x200B; グループ版](https://helpx.adobe.com/enterprise/using/assign-licenses-to-teams-users.html)）または&#x200B;**製品プロファイル** （[&#x200B; エンタープライズ版](https://helpx.adobe.com/jp/enterprise/using/manage-product-profiles.html)）に追加して、Adobe製品とサービスの使用権限を付与します。 詳しくは、[&#x200B; ユーザー指定ライセンスパッケージを作成](https://helpx.adobe.com/enterprise/using/create-nul-packages.html)する方法と[製品プロファイル &#x200B;](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html#create-product-profile)を参照してください。
- **共有デバイスライセンス :** [追加されたユーザー](https://helpx.adobe.com/enterprise/using/sdl-deployment-guide.html#add-users-admin-console)は、**組織ユーザーのみがアクセスできる構成済みの共有デバイスを使用できます**。 詳しくは、[SDL パッケージの作成](https://helpx.adobe.com/enterprise/using/create-sdl-packages.html)を参照してください。

### パッケージのデプロイ

パッケージを作成したら、次のいずれかの方法を使用してクライアントマシンにデプロイします。

- クライアントマシンに移動し、パッケージファイル（WindowsまたはmacOS）をダブルクリックします。
- Windows コマンドプロンプトまたはmacOS ターミナルを使用します。
- サードパーティ製ツールの使用：
   - [Microsoft Intune](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-ms-intune.html)
   - [Microsoft System Center Configuration Manager （SCCM） &#x200B;](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-sccm.html)
   - [Apple リモート デスクトップ （ARD） &#x200B;](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-ard.html)
   - [JAMF Pro](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-jamf-pro.html)
   - [&#x200B; ムンキ &#x200B;](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-munki.html)

## 関連トピックス

- [&#x200B; ユーザーの管理|個別](https://helpx.adobe.com/jp/enterprise/using/manage-users-individually.html)
- [&#x200B; ユーザーの管理| CSVの一括アップロード &#x200B;](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html)
- [&#x200B; ディレクトリユーザーの管理](https://helpx.adobe.com/enterprise/using/manage-directory-users.html)
- [Admin Console](https://helpx.adobe.com/jp/enterprise/using/admin-console.html)
- [製品プロファイルへのユーザーの割り当て（企業および機関向け） &#x200B;](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html#assign-users)
- [&#x200B; グループ ユーザーへのライセンスの割り当て](https://helpx.adobe.com/enterprise/using/assign-licenses-to-teams-users.html)
- [&#x200B; ビジネスストレージモデル &#x200B;](https://helpx.adobe.com/enterprise/kb/business-storage-model-introduction.html)