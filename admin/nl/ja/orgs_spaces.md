---



copyright:

  years: 2015, 2016



---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# 組織およびスペースの管理
{: #orgsspacesusers}
*最終更新日: 2016 年 5 月 16 日*

アカウント所有者は、**「アカウントとサポート」**アイコン ![「アカウントとサポート」アイコン](../admin/images/account_support.svg) &gt; **「組織の管理」**ページと進むことによって、組織を管理できます。組織管理者も、「組織の管理」ページを使用して、自分が管理者として設定されている組織を管理できます。
{:shortdesc}

管理タスクには、以下のものがあります。

* 組織またはスペースの作成
* 組織の名前変更
* 既存の組織またはスペースの削除
* アカウントまたは組織に追加されたチーム・メンバーのリスト表示
* 割り当て量の管理または表示
* カスタム・ドメインの管理

## 組織
{: #orginfo}

組織は複数の地域にまたがることができ、以下の項目によって定義されます。

<dl>
<dt>チーム・メンバー</dt>
<dd>組織とスペースの基本的なアクセス権限を付与された役割です。
組織内のスペースに対するその他のアクセス権を付与されるためには、
ユーザーは組織に割り当てられる必要があります。詳しくは、『[ユーザーと役割 (Users
and roles)](users_roles.html#userrolesinfo)』を参照してください。</dd>
<dt>ドメイン</dt>
<dd>組織に割り振られるインターネットへの経路を提供します。
経路にはサブドメインとドメインがあります。サブドメインは通常アプリケーション名です。
ドメインは、システム・ドメイン、またはアプリケーション用に登録した
カスタム・ドメインの場合があります。『[カスタム・ドメインの管理](orgs_spaces.html#managedomains)』を参照してください。<br/>
<p>**注**: カスタム・ドメインを追加する場合、そのカスタム・ドメインが {{site.data.keyword.Bluemix_notm}} システム・ドメインを指すように解決されるよう、DNS サーバーを構成する必要があります。この方法では、{{site.data.keyword.Bluemix_notm}}
はカスタム・ドメインの要求を受け取ると、ご使用のアプリケーションに適切に経路指定することができます。
</p></dd>
<dt>割り当て量</dt>
<dd>組織による使用に割り振ることが可能なサービス数およびメモリー容量を含む、組織のリソース限度を示します。割り当て量は、組織の作成時に割り当てられます。組織のスペースにおけるアプリケーションまたはサービスはすべて、
割り当て量の使用に寄与します。「従量課金 (PAYG)」プランまたは「サブスクリプション」プランの場合、組織のニーズの変化に応じて、Cloud Foundry アプリケーションおよびコンテナーの割り当て量を調整できます。『[割り当て量の管理](orgs_spaces.html#managequota)』を参照してください。</dd>
</dl>

{{site.data.keyword.Bluemix_notm}} では、以下に示すように、組織を使用することで、チーム・メンバー間のコラボレーションを可能にし、プロジェクト・リソースの論理的なグループ化を促進できます。

<ul>
<li>スペース、アプリケーション、サービス、ドメイン、経路、およびチーム・メンバーをまとめて、組織内でグループ化できます。</li>
<li>スペースおよび組織へのアクセス権限を、ユーザー・ベースで管理することができます。</li>
</ul>

組織を作成する際は、
組織名は {{site.data.keyword.Bluemix_notm}} で固有にする必要があります。
組織名が別の {{site.data.keyword.Bluemix_notm}} Public ユーザー、Dedicated ユーザー、または Local ユーザーで既に使用されている場合、新しい名前を指定しなければなりません。組織を作成すると作成者には自動的に*組織管理者*許可が割り当てられ、この許可により、組織名の編集、チーム・メンバーの追加、組織内でのスペースの作成または削除が可能になります。

組織を削除するには、[{{site.data.keyword.Bluemix_notm}} サポート](http://ibm.biz/bluemixsupport){: new_window}に連絡する必要があります。サポート・チームに組織の削除を要請すると、その組織内のすべてのスペース、アプリケーション、およびサービスが削除されます。

組織のチーム・メンバーには、以下の[ユーザー役割](users_roles.html#userrolesinfo)を割り当てることができます。

<ul>
<li>組織管理者</li>
<li>組織請求管理者</li>
<li>組織監査員</li>
</ul>

<!-- Add info on Manage infrastructure option under a space -->

## スペース
{: #spaceinfo}

1 つの組織内で複数のスペースを使用して、アプリケーション、サービス、およびチーム・メンバーのセットをグループ化できます。スペースは {{site.data.keyword.Bluemix_notm}} の特定の地域と結合されます。

組織にチーム・メンバーを追加した後、それらのメンバーにスペースに対する許可を付与できます。組織と同様に、スペースでも、チーム・メンバーに割り当てることができる、特定の許可を持つ[ユーザー役割](users_roles.html#userrolesinfo)があります。

<ul>
<li>スペース管理者</li>
<li>スペース開発者</li>
<li>スペース監査員</li>
</ul>

**注**: チーム・メンバーには、スペースでの許可のうち少なくとも 1 つが割り当てられていなければなりません。

## 組織およびスペースの作成
{: #createorg}

「従量課金 (PAYG)」アカウントを持つアカウント所有者のみが組織を作成できます。組織を作成するには、以下の手順を実行します。

1. **「アカウントとサポート」**アイコン ![「アカウントとサポート」アイコン](../admin/images/account_support.svg) &gt; **「組織の管理」**ページと進みます。
2. **「新規組織の追加」**をクリックします。
3. 組織名を入力します。
4. **「追加」**をクリックします。

組織内にスペースを作成できます。例えば、開発環境として *dev* スペース、テスト環境として *test* スペース、実稼働環境として *production* スペースを作成できます。その後、各スペースにアプリを関連付けることができます。スペースを作成するには、以下の手順を実行します。

1. **「アカウントとサポート」**アイコン ![「アカウントとサポート」アイコン](../admin/images/account_support.svg) &gt; **「組織の管理」**ページと進みます。
2. スペースを追加する組織を特定し、**「詳細の表示」**を選択します。
3. **「編集」**をクリックします。
4. **「スペースの追加」**をクリックします。
5. スペース名を入力します。
6. **「追加」**をクリックします。


## 組織の名前変更
{: #orgrename}

組織を名前変更するには、以下の手順を実行します。

1. **「アカウントとサポート」**アイコン ![「アカウントとサポート」アイコン](../admin/images/account_support.svg) &gt; **「組織の管理」**ページと進みます。
2. 編集する組織を特定し、**「詳細の表示」**を選択します。
3. **「編集」**を選択します。
4. 組織のタイトルに対して**「編集」**を選択します。
5. 新しい組織名を入力します。
6. **「保存」**をクリックします。

## 既存の組織またはスペースの削除
{: #deleteorgs}

組織を削除するには、アカウント所有者は [{{site.data.keyword.Bluemix_notm}} サポート](http://ibm.biz/bluemixsupport){: new_window}に連絡する必要があります。 

**注**: 削除操作は元に戻せません。組織を削除すると、その組織に関連付けられたすべてのアプリケーションとサービスが失われます。

スペースの削除は、**「組織の管理」**ページから次のようにして行うことができます。

1. **「アカウントとサポート」**アイコン ![「アカウントとサポート」アイコン](../admin/images/account_support.svg) &gt; **「組織の管理」**ページと進みます。
2. 編集する組織を特定し、**「詳細の表示」**を選択します。
3. 削除するスペースを特定し、**「編集」**を選択します。
4. **「スペースの削除」**をクリックします。

## メンバーのリスト
{: #listmembers}

特定の組織のメンバーをリストするには、次の手順を実行します。

1. **「アカウントとサポート」**アイコン ![「アカウントとサポート」アイコン](../admin/images/account_support.svg) &gt; **「組織の管理」**と進みます。
2. メンバーを表示したい組織を特定し、**「詳細の表示」**をクリックします。
3. **「編集」**をクリックします。
4. **「ユーザー」**タブで組織のメンバーとメンバーの役割を確認できます。


特定のスペースのメンバーをリストするには、次の手順を実行します。

1. **「アカウントとサポート」**アイコン ![「アカウントとサポート」アイコン](../admin/images/account_support.svg) &gt; **「組織の管理」**ページと進みます。
2. メンバーを表示したい組織を特定し、**「詳細の表示」**をクリックします。
3. メンバーを表示したいスペースを特定し、**「編集」**をクリックします。
4. **「ユーザー」**タブで、スペースのメンバーとメンバーの役割を確認できます。

## 割り当て量の管理
{: #managequota}

アカウント所有者または組織管理者は、組織に割り当てられた割り当て量および使用された割り当て量を表示できます。割り当て量は、組織が作成されたときに割り当てられた、組織でのリソース限度を表します。組織のスペースにおけるアプリケーションまたはサービスはすべて、
割り当て量の使用に寄与します。

組織の割り当て量を表示するには、以下の手順を実行します。

1. **「アカウントとサポート」**アイコン ![「アカウントとサポート」アイコン](../admin/images/account_support.svg) &gt; **「組織の管理」**ページと進みます。
2. 割り当て量を表示したい組織を特定し、**「詳細の表示」**をクリックします。
3. **「編集」**をクリックします。
4. **「割り当て量」**タブを選択します。

組織の割り当て量を更新するには、サポート・チケットをオープンする必要があります。サポート・チケットのオープンについて詳しくは、『[お客様サポートの利用](../support/index.html#contacting-support)』を参照してください。コンテナーの割り当て量について詳しくは、コンテナーに関する説明資料の『[割り当て量](../containers/container_creating_ov.html#container_quota)』を参照してください。

## ドメインの管理
{: #managedomains}

アカウント所有者または組織管理者は、システム・ドメインを表示でき、また、組織内と組織のスペース内で作成されたアプリケーション用のカスタム・ドメインを追加することができます。スペース管理者は、スペースの**「ドメイン」**タブで、スペースに割り当てられたドメインの読み取り専用リストを確認できます。 

1. **「アカウントとサポート」**アイコン ![「アカウントとサポート」アイコン](../admin/images/account_support.svg) &gt; **「組織の管理」**ページと進みます。
2. ドメインを表示または編集したい組織を特定します。
3. その組織に対して**「詳細の表示」**を選択します。
4. **「編集」**をクリックします。
5. **「ドメイン」**をクリックします。

カスタム・ドメインを追加する場合は、
DNS サーバーを構成してカスタム・ドメインを解決し、
{{site.data.keyword.Bluemix_notm}}
システム・ドメインを指すようにする必要があります。この方法では、{{site.data.keyword.Bluemix_notm}}
はカスタム・ドメインの要求を受け取ると、ご使用のアプリケーションに適切に経路指定することができます。
システム・ドメインはスペースで常に使用可能であり、カスタム・ドメインもまたスペースに割り振ることができます。スペース内に作成されたアプリケーションは、そのスペースにリストされたドメインをどれでも使用できます。カスタム・ドメインの作成と使用について詳しくは、『[カスタム・ドメインの作成と使用](../manageapps/updapps.html#domain)』を参照してください。
