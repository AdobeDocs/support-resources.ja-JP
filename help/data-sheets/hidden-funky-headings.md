---
title: タグライブラリ
description: Granite、CQ、Sling タグライブラリを使用すると、テンプレートやコンポーネントの JSP スクリプトで使用する特定の関数にアクセスできます
contentOwner: Guillaume Carlino
products: SG_EXPERIENCEMANAGER/6.5/SITES
topic-tags: platform
content-type: reference
solution: Experience Manager, Experience Manager Sites
hide: true
hidefromtoc: true
role: Developer
source-git-commit: cc5de4831db78b9b17ca87383ff5b30a2bd581eb
workflow-type: tm+mt
source-wordcount: '2466'
ht-degree: 0%

---

# タグライブラリ{#tag-libraries}

Granite、CQ、Sling タグライブラリを使用すると、テンプレートやコンポーネントの JSP スクリプトで使用する特定の関数にアクセスできます。

## **太字の見出し**

太字の見出しです

## *斜体見出し*

これは斜体の見出しです

## Granite タグライブラリ {#granite-tag-library}

Granite タグライブラリには、便利な関数が含まれています。

Granite UI コンポーネントの jsp スクリプトを開発する場合は、スクリプトの先頭に次のコードをインクルードすることをお勧めします。

```xml
<%@include file="/libs/granite/ui/global.jsp"%>
```

グローバルはまた、Sling ライブラリを宣言しています。

```xml
<%@taglib prefix="sling" uri="https://sling.apache.org/taglibs/sling" %>
```

### &lt;ui:includeClientLib> {#ui-includeclientlib}

`<ui:includeClientLib>` タグは、AEM html クライアントライブラリをインクルードします。js、css または theme の各ライブラリを指定できます。 異なるタイプ（例：js と css）の複数のインクルードがある場合は、このタグを jsp で複数回使用します。 このタグは、` [com.adobe.granite.ui.clientlibs.HtmlLibraryManager](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/javadoc/com/adobe/granite/ui/clientlibs/HtmlLibraryManager.html)` サービスインターフェイスを囲む便利なラッパーです。

このタグの属性を以下に示します。

**categories** - クライアントライブラリのカテゴリのコンマ区切りのリスト。 指定されたカテゴリのJavaScriptおよび CSS ライブラリがすべて含まれます。 テーマ名はリクエストから抽出されます。

次と同じ：`com.adobe.granite.ui.clientlibs.HtmlLibraryManager#writeIncludes`

**theme** - クライアントライブラリのカテゴリのコンマ区切りのリスト。 指定したカテゴリの、すべてのテーマ関連ライブラリ（CSS と JS の両方）が含まれます。 テーマ名はリクエストから抽出されます。

次と同じ：`com.adobe.granite.ui.clientlibs.HtmlLibraryManager#writeThemeInclude`

**js** - クライアントライブラリのカテゴリのコンマ区切りのリスト。 指定されたカテゴリのすべてのJavaScript ライブラリが含まれます。

次と同じ：`com.adobe.granite.ui.clientlibs.HtmlLibraryManager#writeJsInclude`

**css** - クライアントライブラリのカテゴリのコンマ区切りのリスト。 指定したカテゴリの CSS ライブラリがすべて対象になります。

次と同じ：`com.adobe.granite.ui.clientlibs.HtmlLibraryManager#writeCssInclude`

**themed** - テーマの設定されたライブラリまたは設定されていないライブラリのみインクルードすることを示すフラグ。 省略すると、両方のセットがインクルードされます。 純粋な JS または CSS のインクルードにのみ適用します（カテゴリまたはテーマのインクルードには適用されません）。

`<ui:includeClientLib>` タグは jsp で次のように使用できます。

```xml
<%-- all: js + theme (theme-js + css) --%>
<ui:includeClientLib categories="cq.wcm.edit" />

<%-- only js libs --%>
<ui:includeClientLib js="cq.collab.calendar, cq.security" />

<%-- theme only (theme-js + css) --%>
<ui:includeClientLib theme="cq.collab.calendar, cq.security" />

<%-- css only --%>
<ui:includeClientLib css="cq.collab.calendar, cq.security" />
```

## CQ タグライブラリ {#cq-tag-library}

CQ タグライブラリには、便利な関数が含まれています。

スクリプトで CQ タグライブラリを使用するには、スクリプトを次のコードで開始する必要があります。

```xml
<%@taglib prefix="cq" uri="https://www.day.com/taglibs/cq/1.0" %>
```

>[!NOTE]
>
>スクリプトに `/libs/foundation/global.jsp` ファイルがインクルードされると、タグライブラリが自動的に宣言されます。

AEM コンポーネントの jsp スクリプトを開発する場合は、スクリプトの先頭に次のコードをインクルードすることをお勧めします。

```xml
<%@include file="/libs/foundation/global.jsp"%>
```

このコードは sling、cq および jstl の各タグライブラリを宣言し、[`<cq:defineObjects />`](#amp-lt-cq-defineobjects) タグで定義される、定期的に使用するスクリプトオブジェクトを公開します。 これにより、コンポーネントの jsp コードが短縮および簡素化されます。

### &lt;cq:text> {#cq-text}

`<cq:text>` タグは、JSP 内のコンポーネントテキストを出力する便利なタグです。

このタグのオプションの属性を以下に示します。

**property** – 使用するプロパティの名前。 この名前は、現在のリソースを基準とした相対名です。

**value** – 出力に使用する値。 この属性が存在する場合は、property 属性の使用が上書きされます。

**oldValue** – 差分出力に使用する値。 この属性が存在する場合は、property 属性の使用が上書きされます。

**escapeXml** – 結果の文字列内の文字 &lt;、>、&amp;、&#39;および&quot;を対応する文字エンティティコードに変換する必要があるかどうかを定義します。 デフォルト値は false です。 オプションの書式設定の後にエスケープが適用されます。

**format** - テキストの書式設定に使用するオプションの java.text 形式。

**noDiff** – 差分情報が存在する場合でも、差分出力の計算をおこないません。

**tagClass** – 空でない出力を囲む要素の CSS クラス名。 空の場合は、要素が追加されません。

**tagName** – 空でない出力を囲む要素の名前。 デフォルト値は DIV です。

**placeholder** – 編集モードで null または空のテキストに使用するデフォルト値（プレースホルダー）。 デフォルトのチェックは、オプションの書式設定とエスケープの後に実行されます。つまり、出力にそのまま書き込まれます。 デフォルト値は次のとおりです。

`<div><span class="cq-text-placeholder">&para;</span></div>`

**default** - null または空のテキストに使用するデフォルト値。 デフォルトのチェックは、オプションの書式設定とエスケープの後に実行され、そのまま出力に書き込まれます。

JSP における `<cq:text>` タグの使用例を次に示します。

```xml
<cq:text property="jcr:title" tagName="h2"/>
<cq:text property="jcr:description" tagName="p"/>

<cq:text value="<%= listItem.getTitle() %>" tagName="h4" placeholder="" />
<cq:text value="<%= listItem.getDescription() %>" tagName="p" placeholder=""/>

<cq:text property="jcr:title" value="<%= title %>" tagName="h3"/><%
    } else if (type.equals("link")) {
        %><cq:text property="jcr:title" value="<%= "\u00bb " + title %>" tagName="p" tagClass="link"/><%
    } else if (type.equals("extralarge")) {
        %><cq:text property="jcr:title" value="<%= title %>" tagName="h1"/><%
    } else {
        %><cq:text property="jcr:title" value="<%= title %>" tagName="h2"/><%

<cq:text property="jcr:description" placeholder="" tagName="small"/>

<cq:text property="tableData"
               escapeXml="false"
               placeholder="<img src=\"/libs/cq/ui/resources/0.gif\" class=\"cq-table-placeholder\" alt=\"\">"
    />

<cq:text property="text"/>

<cq:text property="image/jcr:description" placeholder="" tagName="small"/>
<cq:text property="text" tagClass="text"/>
```

### &lt;cq:setContentBundle> {#cq-setcontentbundle}

`<cq:setContentBundle>` タグは、i18n ローカリゼーションコンテキストを作成して `javax.servlet.jsp.jstl.fmt.localizationContext` 設定変数に格納します。

このタグの属性を以下に示します。

**language** - リソースバンドルを取得するロケールの言語。

**source** - ロケールの取得元。 次のいずれかの値に設定できます。

* **static** - ロケールが `language` 属性から取得されます（使用可能な場合）。それ以外の場合は、サーバーのデフォルトのロケールから取得されます。

* **page** - ロケールが現在のページまたはリソースの言語から取得されます（使用可能な場合）。取得できない場合は、`language` 属性から取得されます（使用可能な場合）。この属性からも取得できない場合は、サーバーのデフォルトのロケールから取得されます。

* **request** - ロケールがリクエストロケール（`request.getLocale()`）から取得されます。

* **auto** - ロケールが `language` 属性から取得されます（使用可能な場合）。取得できない場合は、現在のページまたはリソースの言語から取得されます（使用可能な場合）。この言語からも取得できない場合は、リクエストから取得されます。

`source` 属性が設定されていない場合：

* `language` 属性が設定されている場合は、`source` 属性のデフォルト値が`` `static` になります。

* `language` 属性が設定されていない場合は、`source` 属性のデフォルト値が `auto` になります。

「コンテンツバンドル」は、標準の JSTL `<fmt:message>` タグで使用できます。 キーによるメッセージのルックアップは、次の 2 つの方法で行います。

1. まず、レンダリングされる基になるリソースの JCR プロパティで翻訳が検索されます。 これにより、これらの値を編集するための簡単なコンポーネントダイアログボックスを定義できます。
1. キーと同じ名前のプロパティがノードに格納されていない場合は、フォールバックによってリソースバンドルが Sling のリクエストから読み込まれます（`SlingHttpServletRequest.getResourceBundle(Locale)`）。 このバンドル用の言語またはロケールは、`<cq:setContentBundle>` タグの language 属性および source 属性で定義されます。

`<cq:setContentBundle>` タグは jsp で次のように使用できます。

言語を定義するページの場合：

```xml
... %><cq:setContentBundle source="page"/><%  %>
<div class="error"><fmt:message key="Hello"/>
</div> ...
```

パーソナライズされたユーザーページの場合：

```xml
... %><cq:setContentBundle scope="request"/><% %>
<div class="error"><fmt:message key="Hello"/>
</div> ...
```

### &lt;cq:include> {#cq-include}

`<cq:include>` タグは、現在のページにリソースをインクルードします。

このタグの属性を以下に示します。

**フラッシュ**

* ターゲットを含める前に出力をフラッシュするかどうかを定義するブール値。

**パス**

* 現在のリクエスト処理に含まれるリソースオブジェクトへのパス。 このパスが相対パスの場合は、指定されたリソースがスクリプトに含まれる現在のリソースのパスに追加されます。 path と resourceType または script を指定する必要があります。

**resourceType**

* 組み込むリソースのリソースタイプ。 リソースタイプを設定する場合、パスはリソースオブジェクトへの正確なパスである必要があります。この場合、パスへのパラメーター、セレクター、拡張機能の追加はサポートされていません。
* 含めるリソースが、リソースに解決できない path 属性で指定されている場合、タグはパスとこのリソースタイプから合成リソースオブジェクトを作成する場合があります。
* path と resourceType または script を指定する必要があります。

**スクリプト**

* 含める jsp スクリプト。 path と resourceType または script を指定する必要があります。

**ignoreComponentHierarchy**

* スクリプト解決のためにコンポーネント階層を無視するかどうかを制御するブール値。 true の場合、検索パスのみが考慮されます。

**例：**

```xml
<%@taglib prefix="cq" uri="https://www.day.com/taglibs/cq/1.0" %><%
%><div class="center">
    <cq:include path="trail" resourceType="foundation/components/breadcrumb" />
    <cq:include path="title" resourceType="foundation/components/title" />
    <cq:include script="redirect.jsp"/>
    <cq:include path="par" resourceType="foundation/components/parsys" />
</div>
```

スクリプトをインクルードするには `<%@ include file="myScript.jsp" %>` と `<cq:include script="myScript.jsp" %>` のどちらを使用するべきですか？

* `<%@ include file="myScript.jsp" %>` ディレクティブは、完全なファイルを現在のファイルにインクルードすることを JSP コンパイラーに通知します。 これは、インクルードされたファイルのコンテンツが元のファイルに直接ペーストされたかのように動作します。
* `<cq:include script="myScript.jsp">` タグを使用すると、ファイルが実行時にインクルードされます。

`<cq:include>` と `<sling:include>` のどちらを使用するべきですか？

* AEM コンポーネントを開発する場合、Adobeでは `<cq:include>` を使用することをお勧めします。
* `<cq:include>` を使用すると、script 属性の使用時に、名前を指定してスクリプトファイルを直接インクルードできます。 これにより、コンポーネントとリソースタイプの継承が考慮されます。多くの場合、この方法はセレクターと拡張機能を使用する Sling のスクリプト解決を厳守するよりも簡単です。

### &lt;cq:includeClientLib> {#cq-includeclientlib}

>[!CAUTION]
>
>`<cq:includeClientLib>` AEM 5.6 以降で非推奨（廃止予定）となりました。代わりに `<ui:includeClientLib>` を使用してください。

`<cq:includeClientLib>` タグは、AEM html クライアントライブラリをインクルードします。js、css または theme の各ライブラリを指定できます。 異なるタイプ（例：js と css）の複数のインクルードがある場合は、このタグを jsp で複数回使用します。 このタグは、`com.day.cq.widget.HtmlLibraryManager` サービスインターフェイスを囲む便利なラッパーです。

このタグの属性を以下に示します。

**categories** - クライアントライブラリのカテゴリのコンマ区切りのリスト。 指定されたカテゴリのJavaScriptおよび CSS ライブラリがすべて含まれます。 テーマ名はリクエストから抽出されます。

次と同じ：`com.day.cq.widget.HtmlLibraryManager#writeIncludes`

**theme** - クライアントライブラリのカテゴリのコンマ区切りのリスト。 指定したカテゴリの、すべてのテーマ関連ライブラリ（CSS と JS の両方）が含まれます。 テーマ名はリクエストから抽出されます。

次と同じ：`com.day.cq.widget.HtmlLibraryManager#`writeThemeInclude

**js** - クライアントライブラリのカテゴリのコンマ区切りのリスト。 指定されたカテゴリのすべてのJavaScript ライブラリが含まれます。

次と同じ：`com.day.cq.widget.HtmlLibraryManager#writeJsInclude`

**css** - クライアントライブラリのカテゴリのコンマ区切りのリスト。 指定したカテゴリの CSS ライブラリがすべて対象になります。

次と同じ：`com.day.cq.widget.HtmlLibraryManager#writeCssInclude`

**themed** - テーマの設定されたライブラリまたは設定されていないライブラリのみインクルードすることを示すフラグ。 省略すると、両方のセットがインクルードされます。 純粋な JS または CSS のインクルードにのみ適用します（カテゴリまたはテーマのインクルードには適用されません）。

`<cq:includeClientLib>` タグは jsp で次のように使用できます。

```xml
<%-- all: js + theme (theme-js + css) --%>
<cq:includeClientLib categories="cq.wcm.edit" />

<%-- only js libs --%>
<cq:includeClientLib js="cq.collab.calendar, cq.security" />

<%-- theme only (theme-js + css) --%>
<cq:includeClientLib theme="cq.collab.calendar, cq.security" />

<%-- css only --%>
<cq:includeClientLib css="cq.collab.calendar, cq.security" />
```

### &lt;cq:defineObjects> {#cq-defineobjects}

`<cq:defineObjects>` タグは、定期的に使用される以下のスクリプトオブジェクトを公開します。開発者がこれらのオブジェクトを参照できます。 また、[`<sling:defineObjects>`](#amp-lt-sling-defineobjects) タグで定義するオブジェクトも公開します。

**componentContext**

* リクエストの現在のコンポーネントコンテキストオブジェクト（com.day.cq.wcm.api.components.ComponentContext インターフェイス）

**component**

* 現在のリソースの現在のAEM コンポーネントオブジェクト（com.day.cq.wcm.api.components.Component インターフェイス）

**currentDesign**

* 現在のページの現在のデザインオブジェクト（com.day.cq.wcm.api.designer.Design インターフェイス）

**currentPage**

* 現在のAEM WCM ページオブジェクト（com.day.cq.wcm.api.Page インターフェイス）。

**currentStyle**

* 現在のセルの現在のスタイルオブジェクト（com.day.cq.wcm.api.designer.Style インターフェイス）

**designer**

* デザイン情報へのアクセスに使用する designer オブジェクト（com.day.cq.wcm.api.designer.Designer インターフェイス）。

**editContext**

* AEM コンポーネントのコンテキストの編集オブジェクト（com.day.cq.wcm.api.components.EditContext インターフェイス）

**pageManager**

* ページレベルの操作用のページマネージャーオブジェクト（com.day.cq.wcm.api.PageManager インターフェイス）

**pageProperties**

* 現在のページのページプロパティオブジェクト（org.apache.sling.api.resource.ValueMap）

**プロパティ**

* 現在のリソースのプロパティオブジェクト（org.apache.sling.api.resource.ValueMap）

**resourceDesign**

* リソースページのデザインオブジェクト（com.day.cq.wcm.api.designer.Design インターフェイス）

**resourcePage**

* リソースページオブジェクト（com.day.cq.wcm.api.Page インターフェイス）。
* このタグの属性を以下に示します。

**requestName**

* sling から継承

**responseName**

* sling から継承

**resourceName**

* sling から継承

**nodeName**

* sling から継承

**logName**

* sling から継承

**resourceResolverName**

* sling から継承

**slingName**

* sling から継承

**componentContextName**

* wcm に特有

**editContextName**

* wcm に特有

**propertiesName**

* wcm に特有

**pageManagerName**

* wcm に特有

**currentPageName**

* wcm に特有

**resourcePageName**

* wcm に特有

**pagePropertiesName**

* wcm に特有

**componentName**

* wcm に特有

**designerName**

* wcm に特有

**currentDesignName**

* wcm に特有

**resourceDesignName**

* wcm に特有

**currentStyleName**

* wcm に特有

**例**

```xml
<%@page session="false" contentType="text/html; charset=utf-8" %><%
%><%@ page import="com.day.cq.wcm.api.WCMMode" %><%
%><%@taglib prefix="cq" uri="https://www.day.com/taglibs/cq/1.0" %><%
%><cq:defineObjects/>
```

>[!NOTE]
>
>スクリプトに `/libs/foundation/global.jsp` ファイルがインクルードされると、`<cq:defineObjects />` タグが自動的にインクルードされます。

### &lt;cq:requestURL> {#cq-requesturl}

`<cq:requestURL>` タグは、現在の要求の URL を JspWriter に書き込みます。 2 つのタグ（[`<cq:addParam>`](#amp-lt-cq-addparam) と [`<cq:removeParam>`](#amp-lt-cq-removeparam)）をこのタグの本体内で使用すると、現在の要求 URL を書き込む前に変更できます。

様々なパラメーターを使用して、現在のページへのリンクを作成できます。 例えば、リクエストを変換できます。

`mypage.html?mode=view&query=something` に `mypage.html?query=something` り込みます。

`addParam` または `removeParam` を使用すると、指定したパラメーターが検出された場合にのみ変更がおこなわれます。他のすべてのパラメーターには影響しません。

`<cq:requestURL>` には属性がありません。

例：

```xml
<a href="<cq:requestURL><cq:removeParam name="language"/></cq:requestURL>">remove filter</a>
```

```xml
<a title="filter results" href="<cq:requestURL><cq:addParam name="language" value="${bucket.value}"/></cq:requestURL>">${label} (${bucket.count})</a>
```

### &lt;cq:addParam> {#cq-addparam}

`<cq:addParam>` タグは、特定の名前と値を持つリクエストパラメーターを外側の [`<cq:requestURL>`](#amp-lt-cq-requesturl) タグに追加します。

このタグの属性を以下に示します。

**名前**

* 追加するパラメーターの名前

**値**

* 追加するパラメーターの値

**例：**

```xml
<a title="filter results" href="<cq:requestURL><cq:addParam name="language" value="${bucket.value}"/></cq:requestURL>">${label} (${bucket.count})</a>
```

### &lt;cq:removeParam> {#cq-removeparam}

`<cq:removeParam>` タグは、特定の名前を持つリクエストパラメーターと値を外側の [`<cq:requestURL>`](#amp-lt-cq-requesturl) タグから削除します。 値を指定しない場合、特定の名前を持つすべてのパラメーターが削除されます。

このタグの属性を以下に示します。

**名前**

* 削除するパラメーターの名前

例：

```xml
<a href="<cq:requestURL><cq:removeParam name="language"/></cq:requestURL>">remove filter</a>
```

## Sling タグライブラリ {#sling-tag-library}

Sling タグライブラリには、便利な Sling 関数が含まれています。

スクリプトで Sling タグライブラリを使用する場合、スクリプトは次のコードで開始する必要があります。

```xml
<%@ taglib prefix="sling" uri="https://sling.apache.org/taglibs/sling/1.0" %>
```

>[!NOTE]
>
>スクリプトに `/libs/foundation/global.jsp` ファイルがインクルードされると、Sling タグライブラリが自動的に宣言されます。

### &lt;sling:include> {#sling-include}

`<sling:include>` タグは、現在のページにリソースをインクルードします。

このタグの属性を以下に示します。

**フラッシュ**

* ターゲットを含める前に出力をフラッシュするかどうかを定義するブール値。

**resource**

* 現在のリクエスト処理に含まれるリソースオブジェクト。 リソースまたはパスを指定してください。 両方を指定した場合は、リソースが優先されます。

**パス**

* 現在のリクエスト処理に含まれるリソースオブジェクトへのパス。 このパスが相対パスの場合は、指定されたリソースがスクリプトに含まれる現在のリソースのパスに追加されます。 リソースまたはパスを指定してください。 両方を指定した場合は、リソースが優先されます。

**resourceType**

* 組み込むリソースのリソースタイプ。 リソースタイプを設定する場合、パスはリソースオブジェクトへの正確なパスである必要があります。この場合、パスへのパラメーター、セレクター、拡張機能の追加はサポートされていません。
* 含めるリソースが、リソースに解決できない path 属性で指定されている場合、タグはパスとこのリソースタイプから合成リソースオブジェクトを作成する場合があります。

**replaceSelectors**

* ディスパッチの際、セレクターはこの属性の値に置き換えられます。

**addSelectors**

* ディスパッチ時に、この属性の値がセレクターに追加されます。

**replaceSuffix**

* ディスパッチ時に、接尾辞はこの属性の値に置き換えられます。

>[!NOTE]
>
>`<sling:include>` タグに含まれるリソースとスクリプトの解像度は、通常の sling URL の解像度と同じです。 デフォルトでは、含まれているスクリプトにも現在のリクエストのセレクター、拡張子などが使用されます。 これらは、タグ属性を使用して変更できます。例：`replaceSelectors="foo.bar"` では、セレクターを上書きできます。

例：

```xml
<div class="item"><sling:include path="<%= pathtoinclude %>"/></div>
```

```xml
<sling:include resource="<%= par %>"/>
```

```xml
<sling:include addSelectors="spool"/>
```

```xml
<sling:include resource="<%= par %>" resourceType="<%= newType %>"/>
```

```xml
<sling:include resource="<%= par %>" resourceType="<%= newType %>"/>
```

```xml
<sling:include replaceSelectors="content" />
```

### &lt;sling:defineObjects> {#sling-defineobjects}

`<sling:defineObjects>` タグは、定期的に使用される以下のスクリプトオブジェクトを公開します。開発者がこれらのオブジェクトを参照できます。

**slingRequest**

* SlingHttpServletRequest オブジェクトは、HTTP リクエストヘッダー情報へのアクセスを提供し、標準の HttpServletRequest を拡張し、リソース、パス情報、セレクターなど、Sling 固有の要素へのアクセスを提供します。

**slingResponse**

* SlingHttpServletResponse オブジェクト。サーバーが作成した HTTP 応答へのアクセスを提供します。 これは、拡張元の HttpServletResponse と同じです。**リクエスト**
* 純粋な HttpServletRequest である標準の JSP リクエストオブジェクト。**回答**
* 純粋な HttpServletResponse である標準の JSP 応答オブジェクト。

**resourceResolver**

* 現在の ResourceResolver オブジェクト。 slingRequest.getResourceResolver （）と同じです。

。**sling**

* SlingScriptHelper オブジェクト。スクリプトの便利なメソッドを含んでおり、主に sling.include （&#39;/some/other/resource&#39;）を使用してこの応答内に他のリソースの応答（ヘッダーの HTML スニペットの埋め込みなど）を含め、Sling で使用可能な OSGi サービスを取得するための sling.getService （foo.bar.Service.class）（スクリプト言語によるクラス表記）。

**resource**

* リクエストの URL に応じて処理する現在のリソースオブジェクト。 slingRequest.getResource （）と同じです。

**currentNode**

* 現在のリソースが JCR ノードを指している場合（通常は Sling の場合）、Node オブジェクトに直接アクセスできます。 それ以外の場合、このオブジェクトは定義されません。

**log**

* スクリプト内から Sling ログシステムにログを記録するための SLF4J ロガーを提供します（例：log.info（&quot;Executing my script&quot;））。

* このタグの属性を以下に示します。

**requestName**

**responseName**

**nodeName**

l **ogName resourceResolverName**

**slingName**

**例：**

```xml
<%@page session="false" %><%
%><%@page import="com.day.cq.wcm.foundation.forms.ValidationHelper"%><%
%><%@taglib prefix="sling" uri="https://sling.apache.org/taglibs/sling/1.0" %><%
%><sling:defineObjects/>
```

## JSTL タグライブラリ {#jstl-tag-library}

[JavaServer Pages 標準タグライブラリ ](https://www.oracle.com/java/technologies/java-server-tag-library.html) には、多数の役立つ標準タグが含まれています。 次のスニペットに示すように、中心となる書式設定および機能のタグライブラリは `/libs/foundation/global.jsp` で定義されます。

### /libs/foundation/global.jspからの抜粋 {#extract-of-libs-foundation-global-jsp}

```xml
<%@taglib prefix="c" uri="https://java.sun.com/jsp/jstl/core" %>
<%@taglib prefix="fmt" uri="https://java.sun.com/jsp/jstl/fmt" %>
<%@taglib prefix="fn" uri="https://java.sun.com/jsp/jstl/functions" %>
```

前述のとおり、`/libs/foundation/global.jsp` ファイルを読み込むと、`c`、`fmt`、`fn` の各プレフィックスを使用して、これらのタグライブラリにアクセスできます。 JSTL の公式ドキュメントは [The Java™ EE 5 Tutorial - JavaServer Pages Standard Tag Library](https://docs.oracle.com/javaee/5/tutorial/doc/bnakc.html) にあります。
