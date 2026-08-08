---
title: "800個の偽npm・Mac窃取・18年越しLinux欠陥【2026/08/08】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# 800個の偽npm・Mac窃取・18年越しLinux欠陥【2026/08/08】

**2026-08-08 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-08-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-08-security)

---

## 概要

約800個の悪性npmパッケージ、Macを狙うClickFix、私物電話へのボイスフィッシング、WordPress全版の認証前XSS、18年越しのLinux欠陥など、実務と生活に直結する8件を解説します。

▼ 今日のトピック
・約800個の悪性npmパッケージ
・Mac向けClickFixとキーチェーン窃取
・UNC6671の電話フィッシング
・WordPressのCVE-2026-64638
・Linux SCTPのroot化・コンテナ脱出
・NATを操るNatJack
・Metabase SQL注入ゼロデイ
・医療ソフト委託先侵害で380万人へ影響

▼ 参考記事・ソース
・The Hacker News「Nearly 800 Malicious npm Packages」 https://thehackernews.com/2026/08/nearly-800-malicious-npm-packages.html
・The Hacker News「ClickFix macOS Stealer」 https://thehackernews.com/2026/08/clickfix-attacks-deliver-macos-stealer.html
・The Hacker News「Linux SCTP Flaw」 https://thehackernews.com/2026/08/18-year-old-linux-sctp-flaw-could-let.html
・Bleeping Computer「Metabase SQLi zero-day」 https://www.bleepingcomputer.com/news/security/framework-tally-disclose-metabase-data-theft-attacks/

#セキュリティ #サイバー攻撃 #脆弱性 #WordPress #Linux #ゆっくり解説 #ずんだもん

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>800個の偽npmから電話フィッシング、18年越しLinux欠陥まで（2026年8月8日）</h1>
<p><strong>キーワード:</strong> npm / ClickFix / ボイスフィッシング / WordPress / Linux SCTP / NatJack</p>
<h2>オープニング：2026年8月8日 — セキュリティニュース</h2>
<p>2026年8月8日のセキュリティニュース。今回は「信頼している入口が攻撃経路へ反転する」を軸に、開発部品、偽の修復手順、電話、ウェブ管理画面、OS、家庭や企業のルーター、業務分析基盤、委託先の個人情報を扱う。</p>
<h2>約800個の悪性npmパッケージ、Windows・Mac・Linuxを横断攻撃</h2>
<ul>
<li>npmレジストリで約800個の悪性パッケージが公開され、Windows、Mac、Linuxで動く遠隔操作型マルウェアと情報窃取型マルウェアを配布した</li>
<li>パッケージ名は生成AI由来らしい不自然な名前や、正規名の入力ミスを狙うタイポスクワッティングを使う。個々の名前を覚えるより、依存追加時の出所確認が重要</li>
<li>開発者は公開者、初回公開日、ダウンロード数、更新履歴、インストール時スクリプトを確認し、ロックファイルと社内許可リスト、隔離環境で被害の連鎖を抑える</li>
</ul>
<h2>Macを狙うClickFix、偽の修復コマンドで暗号資産とキーチェーンを窃取</h2>
<ul>
<li>偽のエラー修復画面が利用者にターミナル操作を促し、Go言語製のMac向け情報窃取マルウェアを導入するClickFix攻撃が確認された</li>
<li>マルウェアは暗号資産、ブラウザー保存パスワード、AppleのiCloudキーチェーン、キャッシュ済み認証情報を狙い、CPUの種類に合う実行ファイルを選ぶ</li>
<li>ウェブページやサポート担当を名乗る相手からコマンド貼り付けを求められても実行しない。実行した場合は端末隔離、認証情報の別端末からの変更、暗号資産ウォレットの確認が必要</li>
</ul>
<h2>私物電話へのボイスフィッシング、SaaSの財務メールを狙うUNC6671</h2>
<ul>
<li>UNC6671と呼ばれる恐喝グループは、金融、プライベートエクイティ、専門サービス企業の従業員へ私物電話で連絡し、ITヘルプデスクを装った</li>
<li>「必須で緊急のセキュリティ移行」を口実に、クラウドサービスの認証情報を奪い、給与や財務フローに関わる人物とメールを探す</li>
<li>社員教育だけでなく、ヘルプデスクが本人確認に使わない情報と、緊急変更を依頼する正式経路を明文化する。管理者は新規端末登録、転送規則、金融語句の大量検索を監視する</li>
</ul>
<h2>WordPress全版に認証前XSS、管理者の操作と連鎖しコード実行へ</h2>
<ul>
<li>WordPressのログイン画面に、認証前でも到達できる反射型クロスサイトスクリプティング脆弱性CVE-2026-64638が修正された。深刻度は10点中8.9</li>
<li>単独で即サーバー乗っ取りではないが、ログイン済み管理者が攻撃者のページを操作すると、PHPコード実行へつながる連鎖が実証された</li>
<li>管理者は本体を公式修正版へ更新し、管理画面を開いた状態で未知のリンクを踏まない。ウェブ防御機器だけに頼らず、管理者セッション、追加された管理者、改変ファイルも点検する</li>
</ul>
<h2>18年前からあるLinux SCTP欠陥、ローカルroot化とコンテナ脱出</h2>
<ul>
<li>LinuxのSCTPネットワークコードに2008年から存在する解放後使用の欠陥が見つかり、ローカル利用者によるroot権限取得とコンテナからホストへの脱出が実証された</li>
<li>修正は安定版カーネル7.1.6、6.18.42、6.12.101、6.6.148で提供された。SCTPは通信事業や高可用性システムで使われる一方、一般端末では不要な場合もある</li>
<li>管理者はカーネルの版だけでなくSCTPがロード・到達可能か、信頼できない利用者がコンテナ内で使えるかを確認し、更新まで不要な機能を無効化する</li>
</ul>
<h2>NatJack、NATの状態を操りTCP乗っ取りとDNS偽装</h2>
<ul>
<li>ブラックハットUSA 2026で、NATの接続状態を操作してTCPセッション乗っ取り、DNS応答偽装、変換済みポートの露出、NATテーブル枯渇を起こすNatJackという攻撃クラスが発表された</li>
<li>Windowsを含む独立した複数実装で同種の挙動が確認され、特定ベンダー一社の単純なバグではなく、状態管理の前提を突く研究として重要</li>
<li>NATは内部端末を自動的に安全にする防火壁ではない。ルーター更新、不要なポート転送の削除、暗号化DNSやTLSの証明書警告を無視しない運用、異常な接続数の監視を組み合わせる</li>
</ul>
<h2>MetabaseのSQL注入ゼロデイ、FrameworkとTallyで顧客データ窃取</h2>
<ul>
<li>業務データ分析ソフトMetabaseの重大なSQL注入脆弱性が、修正前のゼロデイ攻撃で悪用され、FrameworkとTallyの顧客環境からデータが盗まれた</li>
<li>SQL注入は、入力欄などを通じてデータベース命令を不正に差し込む攻撃。分析基盤は複数の業務データへ横断接続するため、一度の侵入で影響範囲が広がりやすい</li>
<li>利用組織は修正版適用だけでなく、Metabaseの外部公開、サービスアカウント権限、実行済みクエリ、大量エクスポートを調査し、必要なら接続資格情報をローテーションする</li>
</ul>
<h2>医療ソフト委託先の侵害、380万人へ波及</h2>
<ul>
<li>医療ソフト企業Unlimited Technology Systemsは、2025年10月に起きた侵害で380万人を超える個人が影響を受けたと報告した</li>
<li>発生から公表規模が見えるまで時間がかかるのは、顧客企業と委託先をまたぐデータ特定・通知が複雑なため。委託は責任やリスクの消滅を意味しない</li>
<li>利用者は正式通知の内容を確認し、通知を装う詐欺に注意する。組織は委託先へ保管データの最小化、削除期限、事故通知期限、再委託先の可視化を契約で求める</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>今回の共通点は、正規の開発レジストリ、修復案内、ヘルプデスク、ログイン画面、OS機能、NAT、分析基盤、委託先という「信頼される入口」が攻撃の足場になったこと</li>
<li>個人はコマンド貼り付けと電話の緊急要求を止まり、公式窓口で確認する。開発者は依存部品、管理者は資産・権限・ログ、経営側は委託契約を点検する</li>
<li>更新は入口を閉じる作業であり、過去の侵入を消すものではない。パッチ適用と同時に、セッション、管理者追加、クエリ、データ取得、資格情報を調査する</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://thehackernews.com/2026/08/nearly-800-malicious-npm-packages.html">The Hacker News: Nearly 800 Malicious npm Packages</a></li>
<li><a href="https://thehackernews.com/2026/08/clickfix-attacks-deliver-macos-stealer.html">The Hacker News: ClickFix Attacks Deliver macOS Stealer</a></li>
<li><a href="https://thehackernews.com/2026/08/unc6671-vishing-attacks-target-personal.html">The Hacker News: UNC6671 Vishing Attacks</a></li>
<li><a href="https://thehackernews.com/2026/08/new-wordpress-pre-auth-xss-could-lead.html">The Hacker News: WordPress Pre-Auth XSS</a></li>
<li><a href="https://thehackernews.com/2026/08/18-year-old-linux-sctp-flaw-could-let.html">The Hacker News: 18-Year-Old Linux SCTP Flaw</a></li>
<li><a href="https://thehackernews.com/2026/08/new-natjack-attacks-hijack-tcp-sessions.html">The Hacker News: NatJack Attacks</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/framework-tally-disclose-metabase-data-theft-attacks/">Bleeping Computer: Metabase SQLi zero-day</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/unlimited-technology-systems-breach-impacts-38-million-people/">Bleeping Computer: Unlimited Technology Systems breach</a></li>
</ul>

</details>

---

[← 2026-08-08 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
