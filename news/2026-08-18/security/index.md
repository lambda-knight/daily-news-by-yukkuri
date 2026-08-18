---
title: "ポケモンセンター漏洩とSnowflake恐喝犯有罪答弁【2026/08/18】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# ポケモンセンター漏洩とSnowflake恐喝犯有罪答弁【2026/08/18】

**2026-08-18 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-18-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-18-security)

---

## 概要

2026年8月18日のセキュリティニュースを、技術者と一般利用者の両方に向けて解説します。

▼ 主なトピック
・ポケモンセンター：委託先物流企業CEVA Logistics経由で英独顧客情報が流出、一部注文キャンセルも
・Snowflake恐喝事件：カナダ人男性が有罪を認める、AT&T顧客1億人超のデータ窃取も認定
・フランス税務当局（DGFiP）：67万8千人分のデータが流出
・GitLab：CVE-2026-19478（CVSS9.4）、未認証でも公開プロジェクトを削除可能な致命的脆弱性
・マイクロソフト：Defenderのゼロデイ「ShieldBreak」（CVE-2026-69414）への対応継続中
・Unisocモデム：VoLTEビデオ通話一本でAndroidカーネルを完全乗っ取り、修正未定
・子ども向けスマートウォッチ：WIRED記者が位置追跡・盗聴の実験対象に

委託先や部品を経由した漏洩・攻撃が目立つ一日でした。企業はGitLabとDefenderのパッチ適用状況を優先確認し、家庭ではGPS内蔵の子ども向け見守り製品の選定に注意が必要です。

#セキュリティ #脆弱性 #ポケモンセンター #Snowflake #GitLab #Unisoc

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年8月18日）</h1>
<p><strong>キーワード:</strong> ポケモンセンター漏洩 / Snowflake恐喝犯有罪答弁 / フランス税務当局漏洩 / GitLab致命的脆弱性 / ShieldBreakゼロデイ / Unisoc VoLTE / キッズ用スマートウォッチ</p>
<h2>オープニング：2026年8月18日 — セキュリティニュース</h2>
<p>本日は、任天堂系ブランド「ポケモンセンター」の委託先物流企業経由の情報漏洩、SnowflakeをめぐるAT&amp;T顧客1億件超の窃取事件でカナダ人の男が有罪を認めた件、フランス税務当局から67万8千人分のデータが盗まれた件、開発プラットフォームGitLabのCVSS9.4の致命的脆弱性、マイクロソフトが対応中のDefenderゼロデイ「ShieldBreak」、スマートフォン用チップメーカーUnisocのモデムを狙う修正未定の攻撃連鎖、そして子ども向けスマートウォッチの追跡・盗聴実験という7件を扱う。大企業・政府機関からの情報流出と、身近な製品の脆弱性が同時に並ぶ一日だった。</p>
<h2>ポケモンセンター、委託先物流企業経由で英独顧客の情報が流出</h2>
<ul>
<li>任天堂系の公式グッズ販売サイト「ポケモンセンター」が、英国とドイツの顧客に対し第三者経由のデータ漏洩を通知した。委託先の物流企業CEVA Logisticsのシステムから、顧客の個人情報と注文情報が盗まれたという。</li>
<li>漏洩を受けて一部の注文がキャンセルされたことも明らかになっている。ポケモンセンター自体のシステムが直接破られたのではなく、配送を担う外部の物流業者が侵入経路になった点が特徴。</li>
<li>「つまりどういうこと？」と言えば、自社のセキュリティを固めても、荷物を運ぶ委託先の防御が甘ければ個人情報は漏れるということ。英国・ドイツで最近ポケモンセンターに注文した人は、届いた通知メールを確認し、心当たりのない請求がないかカード明細もチェックした方がよい。</li>
</ul>
<h2>Snowflake恐喝事件、カナダ人男性が有罪を認める AT&amp;T顧客1億人超のデータ窃取も認める</h2>
<ul>
<li>2024年に「最も影響の大きいサイバー犯罪者の一人」と評されたカナダ人男性コナー・ライリー・ムッカ容疑者（26、オンタリオ州キッチナー在住）が、クラウドデータ基盤Snowflakeを利用していた165以上の組織を不正アクセス・恐喝した罪などで有罪を認めた。</li>
<li>同容疑者はあわせて、通信大手AT&amp;Tの顧客1億人以上の通話・メッセージ履歴を盗んだことも認めている。Snowflakeという一つのクラウド基盤を踏み台に、多数の企業から連鎖的にデータを盗み出す手口だった。</li>
<li>「一つのクラウドサービスが破られると、それを使う何百もの企業に被害が波及する」という、2024年当時から指摘されてきたサプライチェーン型攻撃の構図が、今回の司法手続きで改めて公式に確定した形になる。今後の量刑と、企業側のクラウド認証情報管理の見直しが焦点になる。</li>
</ul>
<h2>フランス税務当局から67万8千人分のデータが流出</h2>
<ul>
<li>フランス経済・財務省が、税務を担当する国税総局（DGFiP）のシステムに攻撃者が侵入し、67万8千人分のデータが盗まれたと発表した。</li>
<li>税務当局のデータには納税者の個人情報や所得に関する情報が含まれるとみられ、政府機関という機微な組織が狙われた事例になる。</li>
<li>「なぜ税務当局が狙われるのか」といえば、氏名・住所・所得といった質の高い個人情報がまとまって保管されているため、なりすましや標的型詐欺に悪用しやすいから。対象になった納税者への詳しい通知や、今後の不審な連絡への注意喚起が課題になる。</li>
</ul>
<h2>GitLabにCVSS9.4の致命的脆弱性、未認証でも公開プロジェクトを削除可能</h2>
<ul>
<li>開発プラットフォームGitLabが、コミュニティ版・エンタープライズ版の両方に影響する致命的な脆弱性（CVE-2026-19478、CVSS9.4）を修正する更新を公開した。特定の条件下では、ログインしていない攻撃者でも公開プロジェクトやユーザーデータを遠隔から改ざん・削除できる状態だった。</li>
<li>GraphQLと呼ばれるデータ取得の仕組みに起因する不具合で、GitLabはこの脆弱性を最も深刻な「Critical」に分類している。</li>
<li>「つまりどういうこと？」と言えば、ログインすらしていない第三者が、企業や開発者が公開しているソースコードのプロジェクトを勝手に消せてしまう可能性があったということ。GitLabのセルフホスト版を運用する企業は、更新の適用状況を優先度高く確認する必要がある。</li>
</ul>
<h2>マイクロソフト、Defenderのゼロデイ「ShieldBreak」への対応を継続中</h2>
<ul>
<li>セキュリティ研究者「Nightmare Eclipse」が先週公表したWindows Defenderのゼロデイ脆弱性「ShieldBreak」（CVE-2026-69414）について、マイクロソフトが修正パッチを準備中であることを明らかにした。</li>
<li>現時点では正式な修正プログラムは公開されておらず、対応は継続中の段階にある。</li>
<li>「パッチが出るまで何もできないのだ？」という状態そのものが、ゼロデイ対応の難しさを示している。Windows Defenderは多くの家庭用・企業用パソコンで標準的に使われているセキュリティソフトのため、修正が公開され次第、速やかな適用が必要になる。</li>
</ul>
<h2>スマホ用チップメーカーUnisocのモデムに攻撃連鎖、修正の見通し立たず</h2>
<ul>
<li>セキュリティ研究組織SSD Secure Disclosureが、通信用チップメーカーUnisocのモデムを搭載する端末で、ビデオ通話規格「VoLTE」を使ったビデオ通話一本で、Androidの中核部分（カーネル）まで完全に乗っ取れる二段階の攻撃手法を公開した。チップメーカー側からの修正はまだ提供されていない。</li>
<li>今回の手法は、2026年3月にSSDが公表したリモートコード実行の脆弱性の続き（第2段階）にあたり、複数月にわたって段階的に攻撃連鎖が明らかにされてきた経緯がある。</li>
<li>「ビデオ通話を受けるだけで乗っ取られるのだ！？」という点が最大の懸念で、利用者側の操作ミスがなくても被害が成立しうる。Unisoc製モデムを搭載したスマートフォンの利用者は、メーカーからの修正提供状況を注視する必要がある。</li>
</ul>
<h2>子ども向けスマートウォッチをハッキング、位置追跡・盗聴が可能に</h2>
<ul>
<li>米WIREDの記者が、子ども向けのピンク色のプラスチック製スマートウォッチに存在する脆弱性を通じて、セキュリティ研究者に位置を追跡され、会話を盗聴される実験を受けた。</li>
<li>WIREDは、この問題が特定の一製品だけでなく、GPS機能を搭載した子ども向けガジェット全般に共通する、脆弱なサプライチェーンの一部にすぎないと報じている。</li>
<li>「子どもの安全のために買った製品が、逆に子どもを危険にさらす」という皮肉な構図。安価なGPS内蔵の子ども向け見守り製品を使っている家庭は、メーカーの実在性やセキュリティ対応の実績を確認することが対策になる。</li>
</ul>
<h2>まとめ</h2>
<p>大企業・政府機関を巻き込む情報漏洩系のニュース（ポケモンセンター、Snowflake関連の有罪答弁、フランス税務当局）と、開発基盤・OS・通信チップ・子ども向けガジェットという幅広い製品層の脆弱性（GitLab、ShieldBreak、Unisoc、キッズ用スマートウォッチ）が同時に並んだ一日だった。委託先経由の漏洩や、通話・ビデオ通話を受けただけで被害が成立する攻撃連鎖は、利用者自身の注意だけでは防ぎきれない領域が広がっていることを示している。</p>
<h2>参考ソース</h2>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/pokemon-center-data-breach-exposes-customer-info-cancels-some-orders/">Bleeping Computer: Pokémon Center data breach exposes customer info, cancels some orders</a></li>
<li><a href="https://krebsonsecurity.com/2026/08/canadian-man-pleads-guilty-in-snowflake-extortions/">Krebs on Security: Canadian Man Pleads Guilty in Snowflake Extortions</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/french-tax-authority-data-breach-affects-678-000-individuals/">Bleeping Computer: French tax authority data breach affects 678,000 individuals</a></li>
<li><a href="https://thehackernews.com/2026/08/critical-gitlab-graphql-flaw-could-let.html">The Hacker News: Critical GitLab GraphQL Flaw Could Let Unauthenticated Attackers Delete Public Projects</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/microsoft-working-on-defender-patch-for-shieldbreak-zero-day/">Bleeping Computer: Microsoft working on Defender patch for ShieldBreak zero-day</a></li>
<li><a href="https://thehackernews.com/2026/08/unisoc-volte-video-call-exploit-chain.html">The Hacker News: Unisoc VoLTE Video Call Exploit Chain Can Give Attackers Full Android Kernel Access</a></li>
<li><a href="https://www.wired.com/story/hackers-stalked-me-by-hijacking-a-smartwatch-for-kids/">WIRED: Hackers Stalked Me by Hijacking a Smartwatch for Kids</a></li>
</ul>

</details>

---

[← 2026-08-18 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
