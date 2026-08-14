---
title: "160万件漏洩、SAPは修正3日で悪用【セキュリティ 2026/08/15】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# 160万件漏洩、SAPは修正3日で悪用【セキュリティ 2026/08/15】

**2026-08-15 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-15-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-15-security)

---

## 概要

RingCentralの160万アカウント漏洩、Shellから89GB窃取という主張、SAP Commerce Cloud、macOS遠隔操作、Metabase SQL注入、Commerzbank不正送金、Appleのスパイウェア通知を具体策まで解説します。

▼ 今日の対策
・委託先を含む認証情報の失効と多要素認証
・SAP、macOS、Metabaseの修正版適用
・Apple Threat Notification受信時の専門支援

#セキュリティ #脆弱性 #情報漏洩 #マルウェア #サイバー攻撃 #ずんだもん

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年8月15日）</h1>
<p><strong>キーワード:</strong> RingCentral情報漏洩 / Shell・Clopランサム / SAP Commerce Cloud / macOS画面共有 / Metabase脆弱性 / Commerzbank詐欺摘発 / 傭兵スパイウェア</p>
<h2>オープニング：2026年8月15日 — セキュリティニュース</h2>
<p>本日は、通信大手RingCentralの情報漏洩、石油大手シェルへのランサムウェア恐喝、SAP Commerce Cloudの実悪用、macOS画面共有機能を悪用した暗号資産マイニング、JPCERT/CCが警告するMetabaseの脆弱性、欧州での3000万ユーロ銀行詐欺の摘発、そしてアップルの傭兵スパイウェア通知の7件を扱う。情報漏洩と実悪用が続く一方で、摘発と防御通知という「押し返す」動きも同時に出た一日だった。</p>
<h2>RingCentral、160万アカウントの情報が漏洩</h2>
<ul>
<li>ビジネス通話大手RingCentralで、恐喝グループShinyHuntersが2026年7月に同社へ侵入し、160万アカウント分の個人情報を盗んだことが、漏洩通知サービスHave I Been Pwnedへの登録で判明した。</li>
<li>漏洩範囲は氏名・連絡先など個人情報とみられ、ShinyHuntersは過去にもSalesforceの顧客データを狙った大規模恐喝キャンペーンで知られるグループ。</li>
<li>ビジネス通話サービスは企業の内線・会議録音など機微情報を扱うため、利用企業側もRingCentral経由で連絡先やアカウント情報が流出していないか確認が必要になる。</li>
</ul>
<h2>石油大手シェル、ランサム集団Clopの「89GB窃取」主張を調査</h2>
<ul>
<li>石油大手シェルが、ランサムウェア集団Clopが「89GBのデータを盗んだ」と主張したことを受け、セキュリティ上のインシデントを調査していると公表した。</li>
<li>現時点でシェルは侵入経路や漏洩内容を確定していないが、エネルギー企業への攻撃は供給網全体への影響も懸念され、確認結果次第で対応範囲が広がる可能性がある。</li>
<li>石油元売りの経営基盤には給油・物流を支えるIT基盤も含まれ、恐喝の標的が業種を問わず広がっていることを示す事例でもある。</li>
</ul>
<h2>SAP Commerce Cloudの最高深刻度の脆弱性、パッチ公開3日で実悪用</h2>
<ul>
<li>SAP Commerce Cloudの最高深刻度（リモートコード実行）の脆弱性が、パッチ公開からわずか3日で攻撃に悪用され始めたと、脅威インテリジェンス企業Defusedが報告した。</li>
<li>ECサイト基盤として広く使われる製品であり、パッチが出ていても適用が追いつかない企業が先に狙われる典型的な構図が今回も繰り返された。</li>
<li>企業側は「パッチが存在する」ではなく「自社環境に適用済みか」を数日単位で確認する体制が求められる。</li>
</ul>
<h2>macOSの画面共有機能の脆弱性、暗号資産マイニングに悪用</h2>
<ul>
<li>オランダ国家サイバーセキュリティセンター（NCSC）が、macOSの画面共有機能にある認証バイパスの脆弱性について、実証コード公開後に攻撃者がモネロ（Monero）採掘マルウェアの配布に悪用していると警告した。</li>
<li>認証を回避して外部から画面共有機能へアクセスできる欠陥で、侵入後にCPU・GPUリソースを暗号資産マイニングに転用される被害が確認されている。</li>
<li>個人のMacユーザーにとっても、動作が急に重くなる・ファンが高回転になるといった症状が侵入の兆候になり得るため、システム更新の適用が対策の第一歩になる。</li>
</ul>
<h2>MetabaseのダッシュボードツールにSQLインジェクションの脆弱性、JPCERT/CCが注意喚起</h2>
<ul>
<li>JPCERT/CCは、データ可視化ツール「Metabase」にSQLインジェクションの脆弱性（CVE-2026-72898）が存在すると発表し、注意喚起を出した。</li>
<li>悪用されると、遠隔の第三者が認証なしで細工したリクエストを送信し、Metabaseが接続するデータベースへ不正なSQLクエリを実行、管理者権限を取得できる可能性がある。</li>
<li>社内の売上・利用状況ダッシュボードなどにMetabaseを使う企業は、公開元の修正版情報を確認し、優先度高く更新する必要がある。</li>
</ul>
<h2>欧州の銀行詐欺、3000万ユーロ規模の犯行で7人摘発</h2>
<ul>
<li>ブラジルで4人、欧州で3人が、決済サービス提供業者の脆弱性を悪用してコメルツ銀行(Commerzbank)顧客の口座から不正に資金を引き出したとして逮捕・起訴された。</li>
<li>被害額は3000万ユーロ規模とされ、国際共同捜査によって実行役の摘発にまでこぎつけた事例。</li>
<li>銀行本体ではなく決済を仲介するサービス提供業者側の脆弱性が起点になっており、金融機関は自社システムだけでなく委託先のセキュリティ水準まで含めた点検が必要になる。</li>
</ul>
<h2>アップル、傭兵スパイウェア攻撃の新たな「脅威通知」を送信</h2>
<ul>
<li>アップルが、iPhoneユーザー向けに「傭兵スパイウェア攻撃を検知した」とする新しい脅威通知（Threat Notification）の送付を開始したことが確認された。</li>
<li>対象は主にジャーナリスト・人権活動家・政府関係者など標的型監視の対象になりやすい利用者とみられ、国家が関与するとされる高度なスパイウェアの検知に基づく通知。</li>
<li>通知を受け取った場合はアップルが提供するロックダウンモードの利用や、専門家への相談が推奨されており、一般利用者が受け取る可能性は低いが、身に覚えのある対象者は放置せず対応することが重要になる。</li>
</ul>
<h2>まとめ</h2>
<p>情報漏洩、ランサム恐喝、実悪用される脆弱性という「攻められる側」の話題が続く一方、金融詐欺の摘発とアップルの脅威通知という「押し返す・知らせる」動きも同じ日に並んだ。委託先経由の被害（RingCentral・Commerzbank）と、パッチ公開直後の実悪用（SAP・macOS）が今回も繰り返されており、自社環境だけでなく取引先・パッチ適用速度の点検が引き続き実務上の優先課題になる。</p>
<h2>参考ソース</h2>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/ringcentral-data-breach-exposed-info-of-16-million-accounts/">Bleeping Computer: RingCentral data breach exposed info of 1.6 million accounts</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/shell-investigates-potential-incident-after-clop-data-theft-claims/">Bleeping Computer: Shell investigates 'potential incident' after Clop data theft claims</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/max-severity-sap-commerce-cloud-flaw-now-targeted-in-attacks/">Bleeping Computer: Max severity SAP Commerce Cloud flaw now targeted in attacks</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/hackers-exploit-macos-screen-sharing-flaw-to-deploy-monero-miner/">Bleeping Computer: Hackers exploit macOS Screen Sharing flaw to deploy Monero miner</a></li>
<li><a href="https://www.jpcert.or.jp/at/2026/at260023.html">JPCERT/CC: MetabaseのSQLインジェクションの脆弱性（CVE-2026-72898）に関する注意喚起</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/hackers-arrested-over-30m-bank-fraud-exploiting-service-provider-flaw/">Bleeping Computer: Hackers arrested over €30M bank fraud exploiting service provider flaw</a></li>
<li><a href="https://www.bleepingcomputer.com/news/apple/apple-sends-new-threat-notification-alerts-over-mercenary-spyware-attacks/">Bleeping Computer: Apple sends new 'Threat Notification' alerts over mercenary spyware attacks</a></li>
</ul>

</details>

---

[← 2026-08-15 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
