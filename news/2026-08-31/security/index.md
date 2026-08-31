---
title: "Claude乗っ取り・870万人流出・ゾンビカード【セキュリティ 2026/08/31】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# Claude乗っ取り・870万人流出・ゾンビカード【セキュリティ 2026/08/31】

**2026-08-31 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-31-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-31-security)

---

## 概要

ログイン済みセッションの窃取、空港予約情報の流出、WordPress脆弱性、期限切れVisaカードの悪用など7件を、仕組みと対策まで解説します。

▼ 今日のトピック
・Claudeのログインセッション窃取
・マンチェスター空港グループ870万人分の流出
・WordPress人気プラグイン3種の脆弱性
・TerminalFixと偽CAPTCHA
・スマートテレビの住宅用プロキシ化
・期限切れVisaのゾンビカード攻撃
・Braveの無料メールエイリアス

▼ 参考記事・ソース
・BleepingComputer「Claude sessions hijacked」 https://www.bleepingcomputer.com/news/artificial-intelligence/anthropic-warns-infostealer-malware-is-hijacking-claude-sessions-to-drain-usage/
・BleepingComputer「Manchester Airports hack」 https://www.bleepingcomputer.com/news/security/fulcrumsec-claims-manchester-airports-hack-theft-of-86-gb-of-data/
・The Hacker News「Critical WordPress flaws」 https://thehackernews.com/2026/08/five-critical-wordpress-plugin-and.html
・The Hacker News「TerminalFix」 https://thehackernews.com/2026/08/terminalfix-uses-fake-cloudflare.html
・Krebs on Security「LG to Ban Residential Proxies」 https://krebsonsecurity.com/2026/07/lg-to-ban-residential-proxies-from-smart-tv-apps/
・The Hacker News「Zombie Card Attack」 https://thehackernews.com/2026/08/zombie-card-attack-can-revive-expired.html
・BleepingComputer「Brave email aliases」 https://www.bleepingcomputer.com/news/security/brave-browser-adds-email-aliases-to-help-users-evade-tracking/

#セキュリティ #サイバー攻撃 #情報漏洩 #WordPress #Claude #ゆっくり解説 #ずんだもん

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年8月31日）</h1>
<p><strong>キーワード:</strong> Claudeセッション窃取 / マンチェスター空港870万件 / WordPress3プラグイン脆弱性 / TerminalFix / スマートTV代理サーバー / ゾンビカード攻撃</p>
<h2>オープニング：2026年8月31日 — セキュリティニュース</h2>
<ul>
<li>本日は7本。情報窃取マルウェアがブラウザ内のログイン済みセッションを盗んでClaudeを無断利用させている件、マンチェスター空港グループで約870万人分の予約情報が流出した件、WordPressの人気プラグイン3種（TranslatePress・Pods・WPMU DEV Dashboard）の乗っ取り級脆弱性、偽CAPTCHAでPowerShell/ターミナルにコマンドを貼らせる「TerminalFix」、スマートテレビやストリーミング端末が住宅用プロキシと広告詐欺に悪用されLGがアプリ排除を表明した件、期限切れVisaカードをタッチ決済で復活させる「ゾンビカード」攻撃、Braveブラウザの無料の使い捨てメールアドレス機能を扱う。</li>
<li>共通軸は「盗まれるのはパスワードではなく、ログイン済みの状態やチェックの前提そのもの」。</li>
</ul>
<h2>情報窃取マルウェア、Claudeのログインセッションを盗んで無断利用</h2>
<ul>
<li>Anthropicは2026年8月30日、一部のClaude利用者に対し、PC上の情報窃取マルウェアが「ログイン中のアクティブなセッション」を盗み、攻撃者がアカウントにアクセスして利用枠を消費していると警告した。</li>
<li>悪用されたのはVidar、LummaC2、StealC、RedLine、Acreed、Atomic Stealer（AMOS）など既知のインフォスティーラー。多くは海賊版ソフトや偽アプリのダウンロードで侵入し、ブラウザに保存されたパスワード・Cookie・認証情報をまとめて窃取する。パスワード自体ではなく認証済みブラウザセッションが標的。</li>
<li>Anthropicは「使っていないのに利用上限が回復してまた減っていたなら、これが原因の可能性が高い」と説明。対応として該当セッションの無効化、保存済み支払い方法の削除、不正利用分の返金を実施。ただし「サインアウトは盗まれたセッションを止めるが、マルウェア自体は消えない」とし、資格情報の変更・セッション無効化に加え端末のマルウェア駆除を求めている。</li>
</ul>
<h2>マンチェスター空港グループに侵入、870万人分の予約情報が流出</h2>
<ul>
<li>マンチェスター空港グループ（MAG）は2026年8月27日、データ侵害を公表。対象はマンチェスター、ロンドン・スタンステッド、イースト・ミッドランズの3空港で、全体で約870万人の顧客が影響を受けたとされる。</li>
<li>侵入経路は、Webサイトのクライアント側JavaScriptに露出していたメール配信サービスIterableのAPI認証情報。恐喝グループ「FulcrumSec」が約86GBの窃取を主張した。</li>
<li>MAGの当初説明は、駐車場・ラウンジ・ファストトラック予約およびWi-Fi登録のメールアドレス、電話番号、車両ナンバー、郵便番号。だが公開されたサンプルには予約番号、購入履歴、価格、割引、駐車日時、IPアドレス、端末情報が含まれ、2026年のこれからの旅程が約20万件あった。MAGは身代金を拒否し、運航・航空保安への影響はないとした。連絡先と旅程がそろうため、空港を装うフィッシングのリスクが高い。</li>
</ul>
<h2>WordPressの人気プラグイン3種に「乗っ取り級」の脆弱性</h2>
<ul>
<li>WordfenceとPatchstackが2026年8月29日、WordPressプラグイン・テーマの重大脆弱性を複数公表。ここでは直近未報道の3件を扱う（AvadaとGiveWPは既報）。</li>
<li>翻訳プラグイン「TranslatePress」（CVE-2026-19632、CVSS 9.8、40万サイト超、3.3.1以前）は管理者のパスワード再設定URLが露出し、アカウント乗っ取りが可能。カスタム項目プラグイン「Pods」（CVE-2026-19598、CVSS 9.8、10万サイト超、3.3.9以前）は認証なしの攻撃者が管理者へ権限昇格できる。</li>
<li>開発者向け「WPMU DEV Dashboard」（CVE-2026-76581、CVSS 9.8、5.0.1以前）はHub SSO有効時に認証を回避され管理者権限・サイト乗っ取りに至る。いずれも「認証不要で管理者」に到達する攻撃難度の低い欠陥で、最新版への更新と不要なSSO連携の無効化が要点。</li>
</ul>
<h2>偽CAPTCHAでターミナルにコマンドを貼らせる「TerminalFix」</h2>
<ul>
<li>Microsoftは2026年8月28日、ソーシャルエンジニアリング型攻撃「ClickFix」の新型「TerminalFix」を公表。改ざんサイトが偽のCloudflare CAPTCHAを表示し、利用者に悪意あるコマンドをコピーして実行させる。</li>
<li>従来はWindowsの「ファイル名を指定して実行」に貼らせていたが、TerminalFixはWindows TerminalやPowerShellに貼らせる。長く複雑なコマンドでも実行が成功しやすくなる。</li>
<li>実行されるのはPython製のリバーストンネル型バックドア（client.py）。gitnow[.]dev:443へ暗号化WebSocketで接続し、任意のTCP通信の中継と社内ネットワーク偵察を可能にする。正規バイナリと不正DLLのサイドローディング、レジストリRunキーやスケジュールタスクでの永続化、PNG画像に隠した次段ペイロードの取得も確認された。対策は「サイトの指示で端末にコマンドを貼らない」、企業ではAppLockerによるPowerShell実行制限とスクリプトブロックログの有効化。</li>
</ul>
<h2>スマートテレビが知らぬ間に「代理サーバー」に、LGがアプリ排除へ</h2>
<ul>
<li>LG Electronics USAは2026年7月21日、スマートテレビを常時稼働の住宅用プロキシ（代理サーバー）ノードに変えるアプリを、webOSストアから排除する方針を表明した。</li>
<li>セキュリティ企業Spurの調査で、LGのwebOSアプリの42%、Samsung Tizenでも25%超が住宅用プロキシSDKを含んでいた。市場を主導していたのはBright Data。プロキシノードは第三者の通信を利用者のテレビ経由で送出し、外部からは家庭の回線から通信が出ているように見える。</li>
<li>テレビ所有者側の害は帯域の消費、プロキシ利用を禁じるISPによる回線停止、犯罪通信の踏み台化。関連する別分析では、「一度払えば見放題」をうたう格安ストリーミング端末が、裏で回線を貸し出すだけでなく、スマホになりすましてAI生成サイトの広告を不正クリックし広告ネットワークや通販事業者を詐取していた。LGは開発者に機能削除を求め、非対応アプリは停止する。出所不明の端末・アプリを入れないことが家庭の対策。</li>
</ul>
<h2>期限切れのVisaカードを「ゾンビ化」してタッチ決済、研究者が実証</h2>
<ul>
<li>マサチューセッツ大学アマースト校の研究者（Raja Hasnain Anwar、Gerard DeCunha、Muhammad Taqi Raza）が、期限切れのVisa非接触カードを店頭決済で復活させる攻撃「Zombie Card」を実証。第35回USENIX Security（2026年8月12〜14日、ボルチモア）で発表した。</li>
<li>EMV非接触決済では有効期限の確認は端末側のポリシーチェックであり、カードの暗号署名には束縛されていない。VisaのKernel 3では両者の一致が必須でなく、端末が検証するfDDA署名は有効期限フィールド（5F24）を含まない。攻撃者は端末が読む日付だけを未来の値に書き換え、Track 2は改変しないため、署名も発行者の暗号文も有効なまま通過する。</li>
<li>攻撃には期限切れの実物カード（または持続的なNFC近接）とカード・端末間の中継装置が必要で、同一のプライマリ口座番号で口座が開いたままであること、発行銀行が認可時に独自に期限を再確認しないことが条件。研究者は2025年5月と同年12月にVisaと銀行へ報告したが、2026年8月20日時点でVisa・EMVCo・各カードブランド・端末ベンダーから対策案は公表されていない。更新カード受領後は古いカードを確実に破棄し、明細を頻繁に確認する。</li>
</ul>
<h2>Braveブラウザ、使い捨てメールアドレス機能を無料で追加</h2>
<ul>
<li>Braveは2026年8月29日公開のバージョン1.94で「Email Aliases」を追加。サービス登録時に使い捨てのメールアドレスを生成し、受信メールは本来のアドレスへ転送しつつ、サイト側には本アドレスを隠す。</li>
<li>無料で5個まで（上限を外す有料版を予定）。Braveアカウントを作り本来のアドレスを登録する。認証はパスワードをサーバーへ送らないOPAQUE（RFC 9807）を使用し、転送後のメールは数秒でBraveのサーバーから削除される。全対応OSで利用可。</li>
<li>効果はサイトをまたぐ同一人物の名寄せの阻止、流出後の迷惑・フィッシングメールの遮断。信頼度の読めない相手にはエイリアスを渡す運用にすると、当日から防御を一段上げられる。</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>7本のうちClaudeのセッション盗難とマンチェスター空港はすでに盗まれたインシデント、WordPress3種と「ゾンビカード」は仕組みの前提が崩れる脆弱性、TerminalFixは人をだます手口、スマートテレビは所有者が知らぬ間に加害インフラにされる構図。</li>
<li>共通軸は「ログイン済みの状態やチェックの前提が奪われる」こと。手元の対策は、海賊版に手を出さない、WordPressプラグインとBraveを更新する、更新後の古いカードを確実に破棄する、サイトの指示で端末にコマンドを貼らない。</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li>BleepingComputer「Anthropic warns infostealer malware is hijacking Claude sessions to drain usage」 https://www.bleepingcomputer.com/news/artificial-intelligence/anthropic-warns-infostealer-malware-is-hijacking-claude-sessions-to-drain-usage/</li>
<li>BleepingComputer「FulcrumSec claims Manchester Airports hack, theft of 86 GB of data」 https://www.bleepingcomputer.com/news/security/fulcrumsec-claims-manchester-airports-hack-theft-of-86-gb-of-data/</li>
<li>The Hacker News「Five Critical WordPress Plugin and Theme Flaws Enable Site Takeover or RCE」 https://thehackernews.com/2026/08/five-critical-wordpress-plugin-and.html</li>
<li>The Hacker News「TerminalFix Uses Fake Cloudflare CAPTCHAs to Deploy Reverse-Tunnel Backdoor」 https://thehackernews.com/2026/08/terminalfix-uses-fake-cloudflare.html</li>
<li>Krebs on Security「LG to Ban Residential Proxies from Smart TV Apps」 https://krebsonsecurity.com/2026/07/lg-to-ban-residential-proxies-from-smart-tv-apps/</li>
<li>Krebs on Security「Read This Before You Buy That TV Streaming Stick」 https://krebsonsecurity.com/2026/07/read-this-before-you-buy-that-tv-streaming-stick/</li>
<li>The Hacker News「Zombie Card Attack Can Revive Expired Visa Cards for Contactless Payments」 https://thehackernews.com/2026/08/zombie-card-attack-can-revive-expired.html</li>
<li>BleepingComputer「Brave browser adds email aliases to help users evade tracking」 https://www.bleepingcomputer.com/news/security/brave-browser-adds-email-aliases-to-help-users-evade-tracking/</li>
</ul>

</details>

---

[← 2026-08-31 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
