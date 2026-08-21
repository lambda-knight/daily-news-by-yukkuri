---
title: "セキュリティニュース｜マイクロソフト8月定例更新398件・Rustサプライチェーン攻撃【2026/08/21】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# セキュリティニュース｜マイクロソフト8月定例更新398件・Rustサプライチェーン攻撃【2026/08/21】

**2026-08-21 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-21-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-21-security)

---

## 概要

2026年8月21日のセキュリティニュース。固有名詞、数字、当事者の声を軸に、ずんだもんと四国めたんが解説します。

▼ 今日のトピック
・マイクロソフト、8月定例更新で398件の脆弱性を修正 1件はすでに悪用済み
・開発基盤Rustのパッケージが乗っ取られ、ダウンロード2億4500万件超のクレートに攻撃コード混入
・ロシア系とみられるハッカー集団、GoogleのログインとWhatsAppの端末連携機能を悪用しアカウント乗っ取り
・AIが生成した攻撃スクリプトが米重要インフラの制御機器シーメンスS7 PLCを標的に
・メールサーバーZimbraの脆弱性が実際の攻撃で悪用される、パッチ済みでも要確認
・米CISA、AI開発基盤「MLflow」の脆弱性が実際に悪用されていると警告
・欧州でAndroidマルウェア「Manic」拡大、近くの感染端末を中継してデータを盗み出す

#ニュース #ゆっくり解説 #ずんだもん #四国めたん

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年8月21日）</h1>
<p><strong>キーワード:</strong> Microsoft8月パッチ / Rustサプライチェーン攻撃 / OAuth乗っ取り / Siemens PLC攻撃 / Zimbra実攻撃 / MLflow脆弱性</p>
<h2>オープニング：2026年8月21日 — セキュリティニュース</h2>
<ul>
<li>本日はマイクロソフトの8月定例更新398件、開発基盤Rustのサプライチェーン攻撃、ロシア系とみられるOAuth悪用によるアカウント乗っ取り、AIが生成した攻撃スクリプトが工場の制御機器を狙った件、Zimbraメールサーバーへの実攻撃、AI開発基盤MLflowの脆弱性、欧州で広がるAndroidマルウェアまで7本を取り上げる</li>
</ul>
<h2>マイクロソフト、8月定例更新で398件の脆弱性を修正 1件はすでに悪用済み</h2>
<ul>
<li>マイクロソフトは8月の月例セキュリティ更新で、Windowsおよび対応ソフトウェアの脆弱性少なくとも398件を修正した。このうち1件はすでに実際の攻撃で悪用されており、2件は更新公開前に詳細が公表されていた</li>
<li>JPCERT/CCとIPAもこの更新に合わせて注意喚起を出しており、国内の企業・個人ユーザーに適用を呼びかけている</li>
<li>更新の適用後、一部のWindows 11環境でゲームが起動しない、または動作中にクラッシュする不具合が報告されており、マイクロソフトが原因を調査中。「つまりどういうこと？」といえば、セキュリティのために更新は必要だが、副作用が出た場合はマイクロソフトの公式情報を確認しながら対応する必要があるということ</li>
</ul>
<h2>開発基盤Rustのパッケージが乗っ取られ、ダウンロード2億4500万件超のクレートに攻撃コード混入</h2>
<ul>
<li>プログラミング言語Rustの公式パッケージ管理サイト「crates.io」で、管理者アカウントが乗っ取られ、広く使われる部品「arrayref」など3つのパッケージに不正なコードが仕込まれた</li>
<li>仕込まれたコードは、プログラムを組み立てる（ビルドする）過程で外部から攻撃用プログラムを自動ダウンロードして実行する仕組みになっており、開発者のパソコンに情報を盗むマルウェアが送り込まれた</li>
<li>影響を受けたパッケージの累計ダウンロード数は2億4500万件を超える。「開発者が気づかないうちに攻撃される」という点が今回の核心で、ソフトを作る側が被害を受けると、そのソフトを使う多数の利用者にも影響が連鎖する恐れがある</li>
</ul>
<h2>ロシア系とみられるハッカー集団、GoogleのログインとWhatsAppの端末連携機能を悪用しアカウント乗っ取り</h2>
<ul>
<li>セキュリティ企業が、ロシア系とみられる3つのサイバースパイ集団が、Googleの正規ログイン機能（OAuth）とWhatsAppの「端末を連携」機能を悪用し、欧米の学術関係者・航空宇宙防衛産業・政府機関・シンクタンク関係者のアカウントを乗っ取っていたと報告した</li>
<li>攻撃者は偽サイトを使わず、正規のログイン画面やQRコード連携の仕組みそのものを悪用するため、利用者が不審に気づきにくい</li>
<li>「本物の画面を使われたら見分けがつかないのだ？」という点が今回の脅威の核心。同種の職業に就く人は、身に覚えのない連携リクエストやログイン確認を承認しないことが対策になる</li>
</ul>
<h2>AIが生成した攻撃スクリプトが米重要インフラの制御機器シーメンスS7 PLCを標的に</h2>
<ul>
<li>米政府は、人工知能（AI）が生成した攻撃スクリプトを使い、シーメンス製の産業用制御機器「S7シリーズPLC」を標的にする「アクティブな脅威」について警告を出した</li>
<li>攻撃者は正規の監視ツールを装ったAI生成スクリプトを使い、工場やインフラ設備の下調べ（偵察）と攻撃能力の開発を進めていたとされる</li>
<li>PLCは工場やプラントの機械を直接制御する装置で、電力・水道・製造業など重要インフラで広く使われている。「AIが攻撃の敷居を下げているのだ？」といえば、これまで専門知識が必要だった制御機器への攻撃準備を、AIの助けで攻撃者がより速く進められるようになっている現状を示す事例</li>
</ul>
<h2>メールサーバーZimbraの脆弱性が実際の攻撃で悪用される、パッチ済みでも要確認</h2>
<ul>
<li>企業向けメールサーバーソフト「Zimbra Collaboration」の脆弱性（CVE-2026-73570、深刻度8.9）が、実際の攻撃で悪用されていることをポーランドのCERTが確認した</li>
<li>この脆弱性はコマンドインジェクションと呼ばれる手法で、修正パッチが提供済みだったにもかかわらず、適用していない組織が攻撃を受けている</li>
<li>「パッチが出ているのに、なぜ被害が出るのだ？」という点が今回の教訓で、修正プログラムの公開と実際の適用の間には時間差があり、その隙を攻撃者が突いている。Zimbraを運用する組織は適用状況の再確認が必要</li>
</ul>
<h2>米CISA、AI開発基盤「MLflow」の脆弱性が実際に悪用されていると警告</h2>
<ul>
<li>米サイバーセキュリティ・インフラセキュリティ庁（CISA）は、AIの開発・実験管理に使われるオープンソース基盤「MLflow」の重大な脆弱性が、実際の攻撃で悪用されていると連邦機関向けに警告した</li>
<li>MLflowはAIモデルの学習過程やデータを管理するためのツールで、企業のAI開発チームで広く使われている</li>
<li>「AIを作るための道具自体が狙われているのだ？」という点が新しい構図で、AI開発ブームに伴い、AIそのものではなく、AIを開発・運用するための周辺基盤が攻撃対象として狙われ始めている</li>
</ul>
<h2>欧州でAndroidマルウェア「Manic」拡大、近くの感染端末を中継してデータを盗み出す</h2>
<ul>
<li>欧州複数国の利用者を狙う新型Androidマルウェア「Manic」が確認された。通常のネット経由でのデータ送信がブロックされた場合、近くにある別の感染端末を中継してデータを盗み出す予備手段を備えている</li>
<li>この仕組みにより、感染端末がネットワークから切り離されていても、近くの別の感染スマホ経由で情報が外部に送られる可能性がある</li>
<li>「スマホをネットから切っても安全じゃないのだ？」という点が従来のマルウェアとの違い。心当たりのないアプリのインストールを避け、不審な権限要求を許可しないことが引き続き基本的な対策になる</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>本日は開発基盤（Rust）とAI周辺基盤（MLflow）という「攻撃対象の新しい層」と、パッチ済みでも悪用が止まらないZimbraのような「対応の遅れが招く実害」が並んだ一日だった</li>
<li>個人でできる備えは、8月の更新プログラムの早期適用、身に覚えのないログイン連携リクエストを承認しないこと、心当たりのないアプリの権限要求を許可しないことの3点</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://krebsonsecurity.com/2026/08/microsoft-plugs-nearly-400-security-holes/">Microsoft Plugs Nearly 400 Security Holes - Krebs on Security</a></li>
<li><a href="https://www.bleepingcomputer.com/news/microsoft/microsoft-august-windows-updates-may-cause-gaming-issues-reboots/">Microsoft says August Windows updates may cause gaming issues - Bleeping Computer</a></li>
<li><a href="https://thehackernews.com/2026/08/rust-supply-chain-attack-puts-build.html">Rust Supply Chain Attack Puts Build-Time Malware in Crates with 245 Million Downloads - The Hacker News</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/hackers-poison-arrayref-rust-crate-to-push-infostealer-malware/">Hackers poison arrayref Rust crate to push infostealer malware - Bleeping Computer</a></li>
<li><a href="https://thehackernews.com/2026/08/suspected-russian-hackers-abuse-google.html">Suspected Russian Hackers Abuse Google OAuth and WhatsApp Linking to Hijack Accounts - The Hacker News</a></li>
<li><a href="https://thehackernews.com/2026/08/ai-generated-exploit-scripts-target.html">AI-Generated Exploit Scripts Target Siemens S7 PLCs in U.S. Critical Infrastructure - The Hacker News</a></li>
<li><a href="https://thehackernews.com/2026/08/attackers-exploit-zimbra-snmp-flaw-for.html">Attackers Exploit Zimbra SNMP Flaw for Unauthenticated Remote Code Execution - The Hacker News</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/cisa-warns-of-hackers-exploiting-critical-mlflow-vulnerability/">CISA warns of hackers exploiting critical MLflow vulnerability - Bleeping Computer</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/new-manic-android-malware-can-exfiltrate-data-through-nearby-devices/">New Manic Android malware can exfiltrate data through nearby devices - Bleeping Computer</a></li>
</ul>

</details>

---

[← 2026-08-21 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
