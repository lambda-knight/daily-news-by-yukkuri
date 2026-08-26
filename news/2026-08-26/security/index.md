---
title: "セキュリティニュース 2026-08-26"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# セキュリティニュース 2026-08-26

**2026-08-26 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-26-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-26-security)

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年8月26日）</h1>
<p><strong>キーワード:</strong> ノルウェー政府DDoS / Nutex Health患者情報流出 / Zimbra274台侵害 / AnonyMousKIT音声AI詐欺 / Mirage2FA4500社 / WhatsAppパスキー複数登録</p>
<h2>オープニング：2026年8月26日 — セキュリティニュース</h2>
<ul>
<li>本日はノルウェー政府基盤への3度目のDDoS攻撃、米医療運営会社Nutex Healthの情報流出、メールサーバーZimbraの実被害拡大、音声AIを使ったiPhoneパスコード詐欺、Microsoft 365を狙うMirage2FA、WhatsAppの新しい認証機能、22カ国が連携した詐欺グループ摘発の7本を扱う。</li>
</ul>
<h2>ノルウェー政府のデジタル基盤、3度目のDDoS攻撃で一部機能停止</h2>
<ul>
<li>2026年8月25日午前3時38分（中欧時間）、ノルウェーのデジタル化庁（Digdir）と運用事業者Vivictaが管理する共通デジタル基盤が大規模DDoS攻撃を受けた。</li>
<li>公的ログイン「ID-porten」や電子署名「eSignering」、行政向けフォームなどが一時完全停止し、事案発生から時間が経った後もID-portenとeSigneringは部分的にアクセスできない状態が続いている。</li>
<li>Digdirの責任者フローデ・ダニエルセン氏は、調査の結果システムへの侵入やデータ漏洩の兆候はないと説明したが、ノルウェーメディアはロシアの関与を推測しており、今回で6月・8月3日に続く3度目の攻撃となる。</li>
</ul>
<h2>医療運営会社Nutex Health、患者・従業員情報流出の可能性</h2>
<ul>
<li>米国12州で28施設を運営し、2025年売上8億7500万ドルのNutex Healthは、外部の第三者が社内サーバーから情報を持ち出したサイバー攻撃を2026年8月24日にSEC提出書類で開示した。</li>
<li>同社は患者情報、従業員情報、経営・財務情報、知的財産が流出した可能性があると述べたが、対象人数や具体的なデータ種別はまだ確定していない。</li>
<li>外部フォレンジック専門家を起用し封じ込め対策と法執行機関への通知を進めており、医療機関を狙うサイバー攻撃で患者データが人質になる構図が今回も繰り返された。</li>
</ul>
<h2>メールサーバーZimbra、274台が実際に侵害される</h2>
<ul>
<li>Zimbra Collaboration Suiteのコマンドインジェクション脆弱性CVE-2026-73570が悪用され、SNMP監視機能を有効にしたサーバーで認証なしのリモートコード実行が可能になっていたことが判明した。</li>
<li>開発元Synacorは7月20日にバージョン10.1.20でパッチを提供済みだが、ポーランドのCERT Polskaが8月19日に実際の悪用を初めて確認し、これまでに274台のインスタンスが侵害された。</li>
<li>Shadowserverの調査では約8200台が未パッチのまま残っており、米CISAは連邦機関に対し8月24日までの24時間以内緊急パッチ適用を命じた。数億人が使うメールサーバーの更新遅れが被害を広げている。</li>
</ul>
<h2>音声AIで「アップル社員」を演じる詐欺キット「AnonyMousKIT」</h2>
<ul>
<li>フィッシング代行サービス「AnonyMousKIT」は、盗まれたiPhoneのアクティベーションロックを解除するため、音声AIエージェントが「Alice from Apple Support」など5種類の人格を使い分けて被害者に電話をかける。</li>
<li>2025年8月から2026年5月の間に約200件の電話詐欺が実行され、被害者を偽のAppleページへ誘導してパスコードや認証コードを盗み、iCloudバックアップや社内情報へのアクセスにまで発展した。</li>
<li>1回の通話コストは約0.10ドルと安く、168のリセラーを通じて販売されている。人間の電話オペレーターに近い自然さを持つAI音声詐欺が、盗難端末の転売価値を高める新しい分業として広がっている。</li>
</ul>
<h2>Microsoft 365を狙う「Mirage2FA」、米欧4500社超に影響</h2>
<ul>
<li>フィッシング代行ツール「Mirage2FA」は2024年から2026年にかけて米国・EUの約4500社に影響を与え、標的にされたメールアドレスの48%が侵害された可能性があるとANY.RUNの調査が示した。</li>
<li>Microsoft 365の正規ログイン画面を模倣し二要素認証を突破したうえで、パスワードだけでなくセッションクッキーそのものを盗み、SSO連携先のサービスにも侵入できる点が特徴である。</li>
<li>被害企業の63.7%が米国、狙われた業種は技術・製造・教育が上位を占め、研究者はセッション窃取をID関連インシデントとして扱い、盗まれたトークンを即座に無効化する対応を推奨している。</li>
</ul>
<h2>WhatsApp、iOS・Androidをまたぐ複数パスキー登録に対応</h2>
<ul>
<li>Metaは2026年8月26日、WhatsAppアカウントに複数のパスキーを登録できる新機能を発表し、iPhoneとAndroidの両方を持つ利用者がフィッシング耐性の高い方式でログインできるようにした。</li>
<li>パスキー自体は2023年10月にAndroidから導入済みで、現在は10億人超が利用しているとMetaは説明している。</li>
<li>パスワードを盗まれる心配がない生体認証・端末認証ベースの仕組みが主要メッセージアプリにも広がっており、複数端末を使う利用者ほど恩恵を受けやすい。</li>
</ul>
<h2>22カ国連携の「オペレーション・ジャッカルⅣ」、西アフリカ詐欺組織を摘発</h2>
<ul>
<li>2025年11月から2026年6月にかけて実施された国際捜査「オペレーション・ジャッカルⅣ」により、22カ国の当局が263人の容疑者を特定し58人を逮捕した。</li>
<li>対象は西アフリカの犯罪シンジケート「Black Axe」が組織したロマンス詐欺、暗号資産・投資詐欺、ビジネスメール詐欺で、未成年に接触し性的画像を強要する事案も含まれていた。</li>
<li>南アフリカでは39人逮捕・銀行口座257個閉鎖・267万ドル差し押さえ、アルゼンチンで17人逮捕・196人特定と、各国の摘発規模が具体的に示された数少ない「防御側の成果」の回である。</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>今日の7本は、国家インフラへのDDoS、医療機関の情報流出、メールサーバーの実被害、音声AI詐欺、認証情報窃取、認証強化、国際摘発という一連の攻防を並べた。</li>
<li>個人はパスキーなど新しい認証手段への切り替えと、電話口で名乗る「サポート担当者」を安易に信用しないこと、組織はZimbraのようなパッチ遅延を放置しないことが当面の要点になる。</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/massive-ddos-attack-disrupts-norways-government-digital-services/">BleepingComputer: Massive DDoS attack disrupts Norway's government digital services</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/hospital-operator-nutex-health-says-data-stolen-in-cyberattack/">BleepingComputer: Hospital operator Nutex Health says data stolen in cyberattack</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/hackers-breached-over-270-zimbra-servers-in-ongoing-attacks/">BleepingComputer: Hackers breached over 270 Zimbra servers in ongoing attacks</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/anonymouskit-phaas-uses-voice-ai-agents-to-phish-iphone-passcodes/">BleepingComputer: AnonyMousKIT PhaaS uses voice AI agents to phish iPhone passcodes</a></li>
<li><a href="https://thehackernews.com/2026/08/mirage2fa-surge-hits-4500-us-and-eu.html">The Hacker News: Mirage2FA Surge Hits 4,500 US and EU Companies</a></li>
<li><a href="https://thehackernews.com/2026/08/whatsapp-adds-multiple-passkeys-for.html">The Hacker News: WhatsApp Adds Multiple Passkeys for Phishing-Resistant Sign-Ins</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/police-arrests-dozens-of-suspects-in-global-cybercrime-crackdown/">BleepingComputer: Police arrests dozens of suspects in global cybercrime crackdown</a></li>
</ul>

</details>

---

[← 2026-08-26 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
