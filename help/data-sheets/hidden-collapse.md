---
title: セクションを折りたたむバグ
description: UGP-13446 の折りたたみ可能なセクションが、ページのタブが埋め込まれていることが原因でレンダリングされない
hide: true
hidefromtoc: true
source-git-commit: f2d8eb9125df5f542c1ed075348586965f4adaad
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 7%

---

# 折りたたみ可能なセクション

<http://jira.corp.adobe.com/browse/UGP-13446> UGP-13446 の折りたたみ可能なセクションが、ページのタブが埋め込まれていることが原因でレンダリングされない

## 例

最初はページ タブあり、2 番目はなし

### オプション 2：ページタブの使用

+++ 6.5.18.0 の手動ホットフィックスのインストール - 6.5.22.0

**手順 1：ホットフィックスパッケージをダウンロードして抽出する**

- Adobe ソフトウェア配布ポータルから [6.5.18.0 - 6.5.22](https://www.adobe.com) のホットフィックスをダウンロードします
- ローカルで抽出

**手順 2：正しいバージョンフォルダーに移動する**

- 環境にインストールされているサービスパックのバージョンに応じて、一致するフォルダーに移動します。

  サービスパック 20 の例のフォルダーは次のとおりです。

  ```
  <extracted-hotfix>/SP20/
  ```

**手順 3：デプロイメントディレクトリを見つける**

- JEE 上のAEM Forms サーバーで、次の場所に移動します。

  ```
  [AEM installation directory]/deploy
  ```

  例：`adobe/adobe-experience-manager-forms/deploy`



**手順 4:EAR ファイルを更新して置き換える**

>[!BEGINTABS]

>[!TAB JBoss]

1. `adobe-core-jboss.ear` を開き、`adminui.war` を

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adminui.war
   ```

   例：`adobe-xxe-configuration-hotfix/SP20/jboss/adminui.war`

1. `adobe-core-jboss.ear` 内で、`lib/` フォルダーに移動し、`adobe-uisupport.jar` を次のように置き換えます。

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   例：`adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. 耳を救ってください。 変更が正しく保存されていることを確認します。


1. `adobe-edcserver-jboss.ear` を

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adobe-edcserver-jboss.ear
   ```

   例：`adobe-xxe-configuration-hotfix/SP20/jboss/adobe-edcserver-jboss.ear`

1. `adobe-forms-jboss.ear` を

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adobe-forms-jboss.ear
   ```

   例：`adobe-xxe-configuration-hotfix/SP20/jboss/adobe-forms-jboss.ear`



>[!TAB WebLogic]

1. `adobe-core-weblogic.ear` を開き、`adminui.war` を

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adminui.war
   ```

   例：`adobe-xxe-configuration-hotfix/SP20/weblogic/adminui.war`

1. `adobe-core-weblogic.ear` 内で、`adobe-uisupport.jar` を次のように置き換えます。

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   例：`adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. 耳を救ってください。 変更が正しく保存されていることを確認します。


1. `adobe-edcserver-weblogic.ear` を

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adobe-edcserver-weblogic.ear
   ```

   例：`adobe-xxe-configuration-hotfix/SP20/weblogic/adobe-edcserver-weblogic.ear`

1. `adobe-forms-weblogic.ear` を

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adobe-forms-weblogic.ear
   ```

   例：`adobe-xxe-configuration-hotfix/SP20/weblogic/adobe-forms-weblogic.ear`

>[!TAB WebSphere]

1. `adobe-core-websphere.ear` を開き、`adminui.war` を

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adminui.war
   ```

   例：`adobe-xxe-configuration-hotfix/SP20/websphere/adminui.war`

1. `adobe-core-websphere.ear` 内で、`adobe-uisupport.jar` を次のように置き換えます。

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   例：`adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. 耳を救ってください。 変更が正しく保存されていることを確認します。


1. `adobe-edcserver-websphere.ear` を

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adobe-edcserver-websphere.ear
   ```

   例：`adobe-xxe-configuration-hotfix/SP20/websphere/adobe-edcserver-websphere.ear`

1. `adobe-forms-websphere.ear` を

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adobe-forms-websphere.ear
   ```

   例：`adobe-xxe-configuration-hotfix/SP20/websphere/adobe-forms-websphere.ear`

>[!ENDTABS]



**手順 5:`adobe-rightsmanagement-<appserver>-dsc.jar` ファイルを** で更新

```
adobe-xxe-configuration-hotfix/SP[version]/<appserver>/adobe-rightsmanagement-<appserver>-dsc.jar
```

例：`adobe-xxe-configuration-hotfix/SP20/jboss/adobe-rightsmanagement-jboss-dsc.jar`

**手順 6:WebSphere および WebLogic での Document Security の追加設定**:

Document Security （旧称Rights Management）を使用している場合は、AEM Forms サーバーを起動する前に、次の Java システムプロパティ（JVM 引数）を設定します。

```
-Dcom.adobe.forms.jee.services.allowDoctypeDeclaration=true
```


**手順 7:Configuration Manager を再実行する**

- Configuration Manager を起動して更新された EAR を再デプロイし、ホットフィックスを適用します。

+++

### オプション 2：ページタブなし

+++ 6.5.18.0 の手動ホットフィックスのインストール - 6.5.22.0

**手順 1：ホットフィックスパッケージをダウンロードして抽出する**

- Adobe ソフトウェア配布ポータルから [6.5.18.0 - 6.5.22](https://www.adobe.com) のホットフィックスをダウンロードします
- ローカルで抽出

**手順 2：正しいバージョンフォルダーに移動する**

- 環境にインストールされているサービスパックのバージョンに応じて、一致するフォルダーに移動します。

  サービスパック 20 の例のフォルダーは次のとおりです。

  ```
  <extracted-hotfix>/SP20/
  ```

**手順 3：デプロイメントディレクトリを見つける**

- JEE 上のAEM Forms サーバーで、次の場所に移動します。

  ```
  [AEM installation directory]/deploy
  ```

  例：`adobe/adobe-experience-manager-forms/deploy`



**手順 4:EAR ファイルを更新して置き換える**

削除されたページ タブ

**手順 5:`adobe-rightsmanagement-<appserver>-dsc.jar` ファイルを** で更新

```
adobe-xxe-configuration-hotfix/SP[version]/<appserver>/adobe-rightsmanagement-<appserver>-dsc.jar
```

例：`adobe-xxe-configuration-hotfix/SP20/jboss/adobe-rightsmanagement-jboss-dsc.jar`

**手順 6:WebSphere および WebLogic での Document Security の追加設定**:

Document Security （旧称Rights Management）を使用している場合は、AEM Forms サーバーを起動する前に、次の Java システムプロパティ（JVM 引数）を設定します。

```
-Dcom.adobe.forms.jee.services.allowDoctypeDeclaration=true
```


**手順 7:Configuration Manager を再実行する**

- Configuration Manager を起動して更新された EAR を再デプロイし、ホットフィックスを適用します。

+++

フィン
