---
title: "セキュリティニュース｜SafePal、暗号資産ハードウェアウォレット利【2026/08/19】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# セキュリティニュース｜SafePal、暗号資産ハードウェアウォレット利【2026/08/19】

**2026-08-19 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-19-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-19-security)

---

## 概要

2026年8月19日のセキュリティニュース。固有名詞、数字、当事者の声を軸に、ずんだもんと四国めたんが解説します。

▼ 今日のトピック
・SafePal、暗号資産ハードウェアウォレット利用者約4万人分の個人情報が流出
・ランサム集団Clop、業務システム「Windchill」侵入専用の自作ツールを開発
・偽の開発者向け部品（RubyGems）16種、ブラウザのパスワードと暗号資産を盗む
・マイクロソフトCopilot Personal、リンクを1回クリックしただけで情報が抜き取られる脆弱性
・CISA、Windowsの脆弱性がランサムウェア集団に悪用されていると正式確認

#ニュース #ゆっくり解説 #ずんだもん #四国めたん

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年8月19日）</h1>
<p><strong>キーワード:</strong> 暗号資産ウォレット流出 / ランサムウェア / タイポスクワッティング / Copilot脆弱性 / CISA注意喚起 / AIハードウェア強奪</p>
<h2>オープニング：2026年8月19日 — セキュリティニュース</h2>
<ul>
<li>本日は暗号資産ウォレットの顧客情報流出、製造業システムを狙う自作攻撃ツール、AIアシスタントの新型脆弱性、貨物強盗の暴力化まで8本を取り上げる</li>
</ul>
<h2>SafePal、暗号資産ハードウェアウォレット利用者約4万人分の個人情報が流出</h2>
<ul>
<li>暗号資産のハードウェアウォレット大手SafePalは、注文追跡用プラグインの権限設定ミスにより、氏名・メールアドレス・配送先住所・電話番号・購入内容が外部から閲覧できる状態になっていたと発表した</li>
<li>影響を受けたのは約39,798人。SafePalは8月16日、対象顧客全員に個別メールで通知した</li>
<li>資産そのもの（秘密鍵や暗号資産）は流出していないとされるが、氏名と住所が結びつくため、フィッシング詐欺や「ウォレットを持っている人」を狙った物理的な脅迫のリスクが指摘されている</li>
</ul>
<h2>ランサム集団Clop、業務システム「Windchill」侵入専用の自作ツールを開発</h2>
<ul>
<li>ランサムウェア集団Clopに関連するとみられる攻撃者が、製品ライフサイクル管理ソフト「PTC Windchill」と「FlexPLM」を狙う専用の不正プログラム（Javaで書かれた遠隔操作用の裏口ツール）を開発していたことが判明した</li>
<li>このツールは、サーバーに保存された認証情報を自動で解読し、ファイルの一覧を調べ、盗み出す機能をあらかじめ備えていた</li>
<li>Windchillは自動車・航空機など製造業の設計データを扱うシステムで、侵入されると製品設計図や部品情報が丸ごと流出するおそれがある</li>
</ul>
<h2>偽の開発者向け部品（RubyGems）16種、ブラウザのパスワードと暗号資産を盗む</h2>
<ul>
<li>プログラム部品を配布するサイト「RubyGems」で、正規のパッケージ名によく似せた偽物16種が見つかった。「StubMaker」と呼ばれる情報窃取プログラムが仕込まれていた</li>
<li>開発者が名前を打ち間違えて偽パッケージを取り込む「タイポスクワッティング」という手口で、Windows環境でブラウザに保存されたパスワードや暗号資産ウォレットの情報を盗み出す</li>
<li>発見は8月15日。研究者チーム「OpenSourceMalware」が公表した。ソフト開発者は依存関係を追加する際にパッケージ名を必ず確認する必要がある</li>
</ul>
<h2>マイクロソフトCopilot Personal、リンクを1回クリックしただけで情報が抜き取られる脆弱性</h2>
<ul>
<li>セキュリティ企業Varonisが、個人向けAIアシスタント「Microsoft Copilot Personal」に3件の脆弱性（総称「CoSnitch」）を発見したと公表した</li>
<li>悪意のあるリンクを1回クリックするだけで、利用者のCopilotセッションが連携している他のアプリ（メールやファイルなど）から情報を静かに抜き取られる可能性がある</li>
<li>原因はCopilot自体が表示する未文書化のURLパラメータの悪用。マイクロソフトには報告済みで、AIアシスタントと外部サービスの連携部分が新たな攻撃対象になっている一例</li>
</ul>
<h2>CISA、Windowsの脆弱性がランサムウェア集団に悪用されていると正式確認</h2>
<ul>
<li>米国土安全保障省傘下のCISA（サイバーセキュリティ・インフラセキュリティ庁）は、4月に「実際に攻撃で使われている」と警告していたWindows Task Hostの脆弱性について、ランサムウェア集団による悪用も確認したと発表した</li>
<li>Windows Task Hostはタスクを管理するWindowsの基本機能で、この欠陥を突かれるとシステム内で通常より高い権限を奪われる</li>
<li>該当システムを使う企業・組織は、CISAが定める期限までの修正パッチ適用が義務付けられている</li>
</ul>
<h2>「Ransom Busters」を名乗る集団、ランサム被害者に「データ削除代行」を持ちかけ最大900万円要求</h2>
<ul>
<li>ランサムウェアの被害企業に対し、「Ransom Busters」を名乗る第三者が「盗まれたデータをランサム集団のサーバーから削除してあげる」と持ちかけ、2万～6万ドル（約290万～900万円）の支払いを要求するメールを送りつける手口が確認された</li>
<li>セキュリティ企業GuidePoint Researchは「一見すると救済のように見えるが、通常あり得ない申し出」と警告している</li>
<li>実際にデータが削除される保証はなく、二重に金を騙し取られるだけの可能性が高い。被害企業への「助けます」型の二次詐欺として要注意</li>
</ul>
<h2>LG、スマートTVアプリの「住宅用プロキシ」化を禁止へ</h2>
<ul>
<li>LGエレクトロニクスは、自社スマートTVの通信を第三者が勝手に中継させる「住宅用プロキシ」機能を持つアプリを、今後webOSストアから排除すると発表した</li>
<li>直前の調査で、LGのTVアプリストアで配信されているゲームなどのアプリのうち42%以上が、利用者のテレビ回線を無断で他人のインターネット通信の中継地点として使う仕組みを持っていたことが判明していた</li>
<li>家庭のTVが知らないうちに犯罪者の通信の隠れみのに使われる恐れがあり、利用者側でできる対策は少ないため、メーカー側の対応が焦点になっていた</li>
</ul>
<h2>AI用サーバー機材めぐる貨物強盗が暴力化——カリフォルニアで相次ぐ襲撃</h2>
<ul>
<li>データセンター向けのサーバーなどAI関連機材を積んだトラックを狙う貨物強盗事件が、カリフォルニア州で相次いで発生し、手口が急速に暴力化していると専門家が指摘している</li>
<li>直近の2件では、運転手への直接的な脅迫や実力行使を伴う事件が確認され、関係者は「これまで見た中で最悪」と証言している</li>
<li>AI開発ブームでサーバー機材の需要と単価が高騰し、換金しやすい高額商品として組織犯罪の標的になっている構図がある</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>本日は資産・機材そのものを狙う古典的な窃盗から、AIアシスタントの連携部分を突く新型攻撃、被害者につけ込む二次詐欺まで、狙われ方の多様化が目立った</li>
<li>個人でできる備えは、暗号資産関連サービスからの通知メールの確認、開発ツールのパッケージ名の再確認、知らない相手からの「復旧支援」の申し出を疑うことの3点</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://thehackernews.com/2026/08/safepal-hardware-wallet-maker-says-flaw.html">SafePal Hardware Wallet Maker Says Flaw Exposed Data of Nearly 40,000 Customers - The Hacker News</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/clop-created-custom-web-shell-for-windchill-data-theft-attacks/">Clop created custom web shell for Windchill data theft attacks - Bleeping Computer</a></li>
<li><a href="https://thehackernews.com/2026/08/16-typosquatted-rubygems-packages-steal.html">16 Typosquatted RubyGems Packages Steal Browser Credentials and Crypto Wallets - The Hacker News</a></li>
<li><a href="https://thehackernews.com/2026/08/microsoft-copilot-personal-flaws-could.html">Microsoft Copilot Personal Flaws Could Let One Click Exfiltrate Data From Connected Apps - The Hacker News</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/cisa-windows-task-host-flaw-now-exploited-by-ransomware-gangs/">CISA: Windows Task Host flaw now exploited by ransomware gangs - Bleeping Computer</a></li>
<li><a href="https://thehackernews.com/2026/08/ransom-busters-claims-it-hacked.html">Ransom Busters Claims It Hacked Ransomware Servers, Asks Victims for Up to $60,000 - The Hacker News</a></li>
<li><a href="https://krebsonsecurity.com/2026/07/lg-to-ban-residential-proxies-from-smart-tv-apps/">LG to Ban Residential Proxies from Smart TV Apps - Krebs on Security</a></li>
<li><a href="https://www.wired.com/story/the-worst-ive-ever-seen-cargo-thieves-are-turning-violent-in-pursuit-of-ai-hardware/">‘The Worst I've Ever Seen’: Cargo Thefts Have Turned Violent in Pursuit of AI Hardware - Wired Security</a></li>
</ul>

</details>

---

[← 2026-08-19 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
