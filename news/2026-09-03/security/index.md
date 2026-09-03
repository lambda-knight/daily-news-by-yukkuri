---
title: "免許証1億5300万件とAI開発端末を狙う新攻撃【2026/09/03】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# 免許証1億5300万件とAI開発端末を狙う新攻撃【2026/09/03】

**2026-09-03 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-09-03-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-09-03-security)

---

## 概要

正規に見える本人確認、ソフト配布、広告、VPN、電話、バックアップが攻撃の入口に。個人と管理者が今すぐ取れる対策まで整理します。

▼ 今日のトピック
・運転免許証1億5300万件超を売るサービスをFBIが捜査
・悪性Git設定がAIコーディングエージェントに命令
・偽インストーラーがWindowsの更新と防御を弱体化
・Meta広告からAndroidへ入るStreamRat
・SonicWall、Switchvox、WordPressの脆弱性

▼ 参考記事・ソース
・Krebs on Security「FBI Probes Service Selling 153M+ Drivers Licenses」 https://krebsonsecurity.com/2026/09/fbi-probes-service-selling-153m-drivers-licenses/
・The Hacker News「Malicious .git Configs Can Make Claude, Codex, Cursor, and Other AI Agents Run Attacker Code」 https://thehackernews.com/2026/09/malicious-git-configs-can-make-claude.html
・The Hacker News「Fake Software Installers Disable Windows Update and Weaken Microsoft Defender」 https://thehackernews.com/2026/09/fake-software-installers-disable.html
・The Hacker News「Meta Ads Push StreamRat Android Trojan」 https://thehackernews.com/2026/09/meta-ads-push-streamrat-android-trojan.html
・The Hacker News「Attackers Exploit Two SonicWall SMA 1000 Zero-Days」 https://thehackernews.com/2026/09/attackers-exploit-two-sonicwall-sma.html
・BleepingComputer「Hackers exploit Sangoma Switchvox flaw」 https://www.bleepingcomputer.com/news/security/hackers-exploit-sangoma-switchvox-flaw-to-deploy-reverse-shells/
・BleepingComputer「WordPress backup plugin flaw exposes millions of sites」 https://www.bleepingcomputer.com/news/security/wordpress-backup-plugin-flaw-exposes-millions-of-sites-to-takeover-attacks/

#サイバーセキュリティ #情報漏洩 #脆弱性 #ゆっくり解説 #ずんだもん #四国めたん

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年9月3日）</h1>
<p><strong>キーワード:</strong> 運転免許証1億5300万件 / 悪性Git設定 / 偽インストーラー / StreamRat / SonicWallゼロデイ / Switchvox / WordPress</p>
<h2>オープニング：2026年9月3日 — セキュリティニュース</h2>
<ul>
<li>本日は7本。本人確認サービスから流出した疑いのある運転免許証画像、AIコーディングエージェントに利用者権限で命令を実行させる悪性Git設定、Windowsの更新と防御を弱める偽インストーラー、約57万アカウントに届いた広告からAndroidへ入るStreamRat、SonicWallのVPN機器で悪用された2件のゼロデイ、Sangoma SwitchvoxとWordPressバックアッププラグインの脆弱性を扱う。</li>
<li>共通するのは「正規に見える入口」だ。本人確認、ソースコード、ソフト配布、広告、VPN、電話、バックアップという信頼されやすい場所が攻撃面になった。個人と管理者が、いま止めるべき入口を具体的に整理する。</li>
</ul>
<h2>運転免許証1億5300万件超を売るサービスをFBIが捜査</h2>
<ul>
<li>Krebs on Securityは2026年9月、米国とカナダの住民の運転免許証をデジタル画像で1億5300万件超販売する新しい個人情報窃取サービスがダークウェブに現れたと報じた。掲載画像を確認した本人への取材から、ルイジアナ州を拠点とする広く使われた本人確認会社が収集した画像を吸い上げている可能性が示された。</li>
<li>米連邦捜査局のニューオーリンズ支局は、画像の出所について正式な捜査を開始した。現段階で記事が示すのは「同社が侵害元と確定した」という結論ではなく、掲載された本人への取材を根拠とする流出経路の疑いだ。</li>
<li>免許証画像は氏名、住所、生年月日、顔写真、署名などを一枚にまとめており、口座開設やアカウント回復の本人確認に悪用され得る。利用者は身に覚えのない信用照会や口座通知を監視し、本人確認事業者は画像の保存期間、外部取得、アクセス記録を点検する必要がある。</li>
</ul>
<h2>悪性Git設定がAIコーディングエージェントに利用者権限で命令</h2>
<ul>
<li>Manifold Securityは、7種類のコマンドライン型AIコーディングエージェントにまたがる8件の欠陥を公表した。細工されたリポジトリ自身のGit設定にコマンドを指定すると、Claude、Codex、Cursorなどが開発者の端末でそのコマンドを実行し得る。公表時点で4件は未修正だった。</li>
<li>問題のコマンドはエージェントの隔離環境の外で、利用者本人の権限により、承認画面なしで動くと説明されている。攻撃成立には、悪性設定を含むリポジトリがローカル環境へ届く必要があるが、届いた後は「コードをまだ実行していないから安全」という判断が通用しない。</li>
<li>知らないリポジトリをAIエージェントで開く前に、隔離した環境で設定を調べ、エージェントを最新版へ上げることが防御の中心になる。組織では、開発端末の認証情報を最小化し、リポジトリを開いただけの段階で発生する子プロセスや外向き通信も監視対象に含めたい。</li>
</ul>
<h2>偽ソフト配布サイトがWindows UpdateとDefenderを弱体化</h2>
<ul>
<li>Microsoftは、信頼されたソフト会社を装う偽ダウンロードサイトが悪性インストーラーを配る活動を確認した。主な標的は中国を拠点とする多国籍企業の業務環境と中国語利用者で、複数の組織と業種に侵害が広がった。</li>
<li>利用者が自分で検索してソフトを入れる流れを悪用し、導入後にWindows Updateを無効化し、Microsoft Defenderの防御を弱める。つまり最初の不正プログラムを入れるだけでなく、その後に修正プログラムと検知機能が働きにくい端末へ変える手口だ。</li>
<li>個人は広告枠や検索順位だけで配布元を信用せず、製品の公式サイトやOSのストアから入手する。企業は許可済み配布経路を決め、更新サービスの停止、Defender設定の変更、除外項目の追加を監視する。感染が疑われる端末は、設定を戻すだけで済ませず、ネットワークから切り離して侵入後の活動を調べる。</li>
</ul>
<h2>Meta広告からAndroidをほぼ完全操作するStreamRat</h2>
<ul>
<li>ThreatFabricは、偽のテレビ視聴サービスを宣伝するMeta広告から、Android向け銀行型トロイの木馬「StreamRat」が配られたと報告した。広告はスペイン語利用者を狙い、スペインを中心に欧州連合内の推定57万950アカウントへ到達した。</li>
<li>StreamRatは感染端末に対する、ほぼ完全な遠隔操作能力を攻撃者へ与えるとされた。動画視聴という身近な誘いと広告プラットフォームの見た目が、正規アプリだという思い込みを作る。銀行型トロイの木馬は、送金情報や認証操作を狙う不正アプリを指す。</li>
<li>Android利用者は広告先から配布されたファイルを直接入れず、公式ストアで開発者名と配布元を確かめる。アクセシビリティー、画面共有、通知閲覧など広い権限を動画アプリが求めたら中止する。すでに入れた場合は別の安全な端末から銀行や主要アカウントの認証情報を変更する。</li>
</ul>
<h2>SonicWall SMA 1000の2件のゼロデイが連鎖する恐れ</h2>
<ul>
<li>SonicWallは、SMA 1000シリーズのVPN機器で、実際の攻撃に使われた2件の脆弱性を修正した。1件は認証前に悪用できるサーバー側リクエスト偽造、CVE-2026-83548で、深刻度は最高のCVSS 10.0。社内調査で発見され、修正版が公開された。</li>
<li>サーバー側リクエスト偽造は、外部の攻撃者がVPN機器を代理にして、通常は外から届かない内部の宛先へ通信させる欠陥だ。報告では2件が攻撃の連鎖を構成する可能性があり、境界機器だからこそ一つの穴が次の操作への足場になる。</li>
<li>SMA 1000管理者は修正版を適用し、管理画面の公開範囲を絞り、更新前後のログと不審な内部向け通信を調べる。すでに悪用されたゼロデイなので、更新だけを完了扱いにせず、侵害された前提でセッション、管理者アカウント、連携資格情報も点検する。</li>
</ul>
<h2>Sangoma SwitchvoxのCVE-2026-9586が電話基盤を侵入口に</h2>
<ul>
<li>攻撃者は、Sangomaの業務用電話基盤SwitchvoxにあるCVE-2026-9586を実際に悪用している。これは認証なしで成立するSQLインジェクションで、最終的に遠隔コード実行へつながり、攻撃者はリバースシェルを設置している。</li>
<li>SQLインジェクションは、入力欄などからデータベースへの命令を混ぜる攻撃。リバースシェルは侵害された機器の側から攻撃者へ接続し、遠隔操作の通路を作る。外からの着信を受ける電話基盤が、社内ネットワークへの戻り道になる点が重い。</li>
<li>管理者はSwitchvoxの対象バージョンを確認して修正を適用し、インターネットから管理機能へ直接届かない構成にする。外向き通信、見慣れないプロセス、データベースへの異常な入力、追加アカウントを調べ、電話が動いていることだけで健全と判断しない。</li>
</ul>
<h2>WordPressバックアッププラグインの欠陥が数百万サイトに波及</h2>
<ul>
<li>WordPress向け「All-in-One WP Migration and Backup」プラグインにSQLインジェクションの脆弱性が見つかった。認証していない攻撃者でも遠隔コードを実行し、影響を受けるウェブサイトを乗っ取れる可能性があり、利用規模は数百万サイトに及ぶ。</li>
<li>バックアップ製品はサイトのファイルとデータベースを扱うため、権限が大きい。そこへ認証なしの入力経路が重なると、情報の読み出しだけでなく、サイト上で攻撃者のプログラムを動かす段階まで進み得る。</li>
<li>管理者はプラグインを修正版へ更新し、使っていなければ無効化だけでなく削除する。ウェブサーバーの新規ファイル、管理者ユーザー、予定実行、外部への通信、バックアップの取得履歴を確認する。一般利用者側の対策ではなく、サイト運営者が更新と侵害調査を担う案件だ。</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>7件の入口は、免許証による本人確認、Gitリポジトリ、ソフト配布サイト、SNS広告、VPN、業務電話、バックアップとばらばらだ。しかし、利用者や管理者が「そこは正規だろう」と信用しやすい場所を攻撃者が選んだ点は共通する。</li>
<li>個人は、免許証を使った口座・信用情報の異常通知を見張り、広告や検索結果からアプリを直接入れない。開発者は未知のリポジトリを隔離して調べ、AIエージェントへ渡す資格情報を減らす。</li>
<li>組織は、SonicWall、Switchvox、WordPressプラグインを更新し、Windows UpdateやDefenderの停止を監視する。修正の適用と侵害調査を一組にすることが、今日の7本から得られる実務上の結論だ。</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://krebsonsecurity.com/2026/09/fbi-probes-service-selling-153m-drivers-licenses/">Krebs on Security: FBI Probes Service Selling 153M+ Drivers Licenses</a></li>
<li><a href="https://thehackernews.com/2026/09/malicious-git-configs-can-make-claude.html">The Hacker News: Malicious .git Configs Can Make Claude, Codex, Cursor, and Other AI Agents Run Attacker Code</a></li>
<li><a href="https://thehackernews.com/2026/09/fake-software-installers-disable.html">The Hacker News: Fake Software Installers Disable Windows Update and Weaken Microsoft Defender</a></li>
<li><a href="https://thehackernews.com/2026/09/meta-ads-push-streamrat-android-trojan.html">The Hacker News: Meta Ads Push StreamRat Android Trojan That Can Gain Near-Complete Device Control</a></li>
<li><a href="https://thehackernews.com/2026/09/attackers-exploit-two-sonicwall-sma.html">The Hacker News: Attackers Exploit Two SonicWall SMA 1000 Zero-Days That May Form an Attack Chain</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/hackers-exploit-sangoma-switchvox-flaw-to-deploy-reverse-shells/">BleepingComputer: Hackers exploit Sangoma Switchvox flaw to deploy reverse shells</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/wordpress-backup-plugin-flaw-exposes-millions-of-sites-to-takeover-attacks/">BleepingComputer: WordPress backup plugin flaw exposes millions of sites to takeover attacks</a></li>
</ul>

</details>

---

[← 2026-09-03 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
