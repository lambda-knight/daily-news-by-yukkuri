---
title: "セキュリティニュース｜AWS漏洩キー9300件放置・GitLab即日悪用【2026/08/22】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# セキュリティニュース｜AWS漏洩キー9300件放置・GitLab即日悪用【2026/08/22】

**2026-08-22 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-22-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-22-security)

---

## 概要

2026年8月22日のセキュリティニュース。固有名詞、数字、当事者の声を軸に、ずんだもんと四国めたんが解説します。

▼ 今日のトピック
・公開放置されたAWSアクセスキー9300件超、今も有効なまま乗っ取り放題
・GitLabの脆弱性CVE-2026-19478、公開からわずか数日で実際の攻撃に悪用
・Ciscoの業務ソフトCrosswork・Secure Workloadに脆弱性9件、5件は最悪水準の深刻度10.0
・米CISA、ビデオ会議サーバー「TrueConf」の悪用中脆弱性に緊急パッチを命令
・偽装したnpmパッケージがAI制御のLinuxバックドア「RedC2 4.0」を配布
・顔写真検索サービスから900万枚超の顔画像データベースが露出
・Meta、女性政治家を「ヌード化」する偽アプリの広告を掲載していた
・JPCERT/CC、分析ツール「Metabase」のSQLインジェクション脆弱性に注意喚起

#ニュース #ゆっくり解説 #ずんだもん #四国めたん

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年8月22日）</h1>
<p><strong>キーワード:</strong> AWS漏洩キー放置 / GitLab即日悪用 / Cisco最悪深刻度 / TrueConf緊急パッチ / npm偽装RedC2 / 顔画像900万枚露出</p>
<h2>オープニング：2026年8月22日 — セキュリティニュース</h2>
<ul>
<li>本日は公開されたまま放置されているAWSアクセスキー9300件超、公開から数日で実攻撃に悪用されたGitLabの脆弱性、Ciscoの業務ソフトに見つかった最悪水準の脆弱性、米CISAが緊急パッチを命じたビデオ会議サーバー、開発ツールを装いAIバックドアを仕込むnpmパッケージ、顔画像900万枚超が露出した検索サービス、女性政治家の「ヌード化」偽アプリの広告掲載、Metabaseの脆弱性への注意喚起まで8本を取り上げる</li>
</ul>
<h2>公開放置されたAWSアクセスキー9300件超、今も有効なまま乗っ取り放題</h2>
<ul>
<li>2022年8月から2026年8月までの間に公開状態で見つかったAmazon Web Services（AWS）のアクセスキーのうち、9300件超が今なお有効な状態のまま放置されていることが分かった</li>
<li>アクセスキーは、プログラムやサービスがAWSへログインするための「合鍵」に相当する情報で、これが漏れると企業のクラウド環境そのものを外部から操作されかねない</li>
<li>「つまりどういうこと？」といえば、鍵が何年も前に落ちていたのに誰も気づかず、今日この瞬間もそのまま使える状態が続いているということ。開発者は自分のコードにアクセスキーを直接書き込まない、書き込んでしまった場合は速やかに無効化するという基本の徹底が今回あらためて問われている</li>
</ul>
<h2>GitLabの脆弱性CVE-2026-19478、公開からわずか数日で実際の攻撃に悪用</h2>
<ul>
<li>GitLabで新たに公表された脆弱性CVE-2026-19478（深刻度9.4）が、セキュリティ企業watchTowrの報告によると、公表からわずか数日で実際の攻撃に悪用され始めた</li>
<li>この脆弱性はコードインジェクションと呼ばれる手法で、認証を経ていない攻撃者が、外部に公開されているGitLabのプロジェクトを改ざん・削除し、データを書き換えられる場合がある</li>
<li>「認証なしでできてしまうのだ？」という点が今回の核心で、ログイン情報を盗まなくても攻撃が成立する。公開リポジトリを持つ組織は、パッチ適用状況を今すぐ確認する必要がある</li>
</ul>
<h2>Ciscoの業務ソフトCrosswork・Secure Workloadに脆弱性9件、5件は最悪水準の深刻度10.0</h2>
<ul>
<li>Ciscoは、ネットワーク管理ソフト「Crosswork」と、業務システムのセキュリティ管理ソフト「Secure Workload」に対し、9件の脆弱性を修正する更新を公開した。このうち5件は最悪水準にあたる深刻度10.0（満点）と評価されている</li>
<li>9件のうち4件は、機器の設定内容にかかわらず「Crosswork Data Gateway」「Crosswork Network Controller」「Crosswork Planning」に影響する</li>
<li>Ciscoはこの数か月、社内のセキュリティ総点検の一環として同種の修正を継続的に公開している。「満点評価が5件も同時に出るのは珍しいのだ？」といえば、それだけ根の深い設計上の問題がまとめて見つかったことを意味し、該当製品を使う企業のシステム担当者は優先度を最上位に置くべき更新といえる</li>
</ul>
<h2>米CISA、ビデオ会議サーバー「TrueConf」の悪用中脆弱性に緊急パッチを命令</h2>
<ul>
<li>米サイバーセキュリティ・インフラセキュリティ庁（CISA）は、自社運用型のビデオ会議・コミュニケーション基盤「TrueConf Server」にある2件の脆弱性が実際に悪用されていると確認し、連邦政府機関に対して優先的なパッチ適用を命じた</li>
<li>TrueConf Serverは組織が自前のサーバーで運用するビデオ会議システムで、社外に会議データを預けたくない企業・団体で使われている</li>
<li>「もう攻撃が始まっているから急げということなのだ？」という理解で正しい。CISAが緊急命令を出す脆弱性は、理論上の危険ではなく現に悪用が確認されているものに限られるため、該当システムの運用者は速やかな対応が求められる</li>
</ul>
<h2>偽装したnpmパッケージがAI制御のLinuxバックドア「RedC2 4.0」を配布</h2>
<ul>
<li>セキュリティ研究者が、カレンダーや連続記録（ストリーク）管理ツールを装った14件のnpmパッケージが、実際にはAI搭載のLinux向け不正プログラム「RedC2 4.0」を密かに配布していたと報告した</li>
<li>発見したTrend Micro傘下のTrendAIによると、パッケージが読み込まれると、内部に仕込まれた実行ファイルを取り出して実行権限を与え、バックグラウンドで動かす仕組みになっていた</li>
<li>「便利ツールのふりをして仕込まれてるのだ？」という点が今回の手口で、開発者が普段づかいのパッケージ管理サイトから何気なく取り込んだツールが、AIが制御する遠隔操作の入口になっていた。出所不明な小規模パッケージを安易に導入しないことが対策になる</li>
</ul>
<h2>顔写真検索サービスから900万枚超の顔画像データベースが露出</h2>
<ul>
<li>人物検索サービス「ClarityCheck」が提供する顔写真の逆引き検索機能で、900万枚を超える画像ファイルを含むデータベースが外部から閲覧できる状態になっていたことが判明した</li>
<li>ClarityCheckはこのサービスについて「非公開で安全」とうたっていたが、実際には保護されないまま公開されていた</li>
<li>「顔写真ってそんなに簡単に漏れるものなのだ？」といえば、本人の同意なく集められた顔写真がサービスの内部管理不備によって誰でも見られる状態になっていたということ。顔認識サービスに写真が登録されているかどうかは利用者側からは分かりにくく、事業者側の管理体制が問われる事例</li>
</ul>
<h2>Meta、女性政治家を「ヌード化」する偽アプリの広告を掲載していた</h2>
<ul>
<li>Metaが運営するSNS上で、写真から人物の服を脱がせたように加工する「ヌード化」アプリの広告が掲載されていたことが分かった。広告の一つには、著名な米政治家に酷似したディープフェイクのポルノ動画が使われていた</li>
<li>報道機関の取材を受け、Appleはこのアプリをアプリストアから削除した</li>
<li>「広告として審査を通っていたのだ？」という点が今回の問題で、悪用目的が明らかなアプリの宣伝が、大手プラットフォームの広告審査をすり抜けていた。同意のない加工画像・動画による被害は当事者の名誉やプライバシーを直接侵害するため、プラットフォーム側の審査体制の実効性が改めて問われている</li>
</ul>
<h2>JPCERT/CC、分析ツール「Metabase」のSQLインジェクション脆弱性に注意喚起</h2>
<ul>
<li>JPCERT/CCは2026年8月6日、データ分析ツール「Metabase」にSQLインジェクションの脆弱性（CVE-2026-72898）が存在すると公表されたことを受け、注意喚起を出した</li>
<li>この脆弱性が悪用されると、遠隔の第三者が認証なしで細工したリクエストを送ることで、Metabaseのアプリケーションデータベースに対して不正なSQL文を実行し、管理者権限を取得できる可能性がある</li>
<li>「社内のデータ分析ツールが乗っ取られる入口になるのだ？」という理解で正しい。Metabaseは売上や利用状況などの社内データを可視化するために広く導入されており、管理者権限を奪われると社内の分析対象データそのものが漏洩・改ざんされる恐れがある</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>本日は「何年も前から放置されていた漏洩」（AWSキー、顔画像データベース）と、「公表直後に速攻で悪用される新しい脆弱性」（GitLab、TrueConf）という対照的な2種類のリスクが並んだ一日だった</li>
<li>開発者・システム担当者への教訓は、パッチが出たら即適用すること、そしてコードや設定に鍵情報を残さないことの2点に尽きる</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/hundreds-of-leaked-aws-keys-give-full-control-over-corporate-accounts/">Hundreds of leaked AWS keys give full control over corporate accounts - Bleeping Computer</a></li>
<li><a href="https://thehackernews.com/2026/08/gitlab-cve-2026-19478-comes-under.html">GitLab CVE-2026-19478 Comes Under Active Exploitation Within Days of Disclosure - The Hacker News</a></li>
<li><a href="https://thehackernews.com/2026/08/cisco-patches-nine-crosswork-and-secure.html">Cisco Patches Nine Crosswork and Secure Workload Flaws, Five Scoring CVSS 10.0 - The Hacker News</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/cisa-orders-feds-to-patch-actively-exploited-trueconf-server-flaws/">CISA orders feds to patch actively exploited TrueConf Server flaws - Bleeping Computer</a></li>
<li><a href="https://thehackernews.com/2026/08/14-trojanized-npm-packages-drop-redc2.html">14 Trojanized npm Packages Drop RedC2 4.0 Linux Backdoor With AI-Assisted C2 - The Hacker News</a></li>
<li><a href="https://www.wired.com/story/reverse-lookup-service-exposed-millions-of-photos-of-peoples-faces/">Reverse-Lookup Service Exposed Millions of Photos of People's Faces - Wired Security</a></li>
<li><a href="https://www.wired.com/story/meta-ran-ads-for-an-app-promising-to-nudify-female-politicians/">Meta Ran Ads for an App That Promised to Nudify Female Politicians - Wired Security</a></li>
<li><a href="https://www.jpcert.or.jp/at/2026/at260023.html">注意喚起: MetabaseのSQLインジェクションの脆弱性（CVE-2026-72898）に関する注意喚起 - JPCERT/CC</a></li>
</ul>

</details>

---

[← 2026-08-22 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
