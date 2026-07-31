---
title: "2万4000台の管理口が露出、医療データ126万人流出【2026/07/30】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# 2万4000台の管理口が露出、医療データ126万人流出【2026/07/30】

**2026-07-30 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-07-30-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-07-30-security)

---

## 概要

サーバーBMC、医療請求委託先、FastJson、VeloCloud、20万台規模のDysphoriaを、対象者と実務対策に分けて解説します。

▼ 今日のトピック
・2万4000台超のBMCがパスワードハッシュを漏えい
・MCBS侵害が126万人に影響
・FastJsonとVeloCloudの悪用中ゼロデイ
・世界約20万台のDysphoriaボットネット

▼ 参考記事
https://www.bleepingcomputer.com/
https://www.bleepingcomputer.com/tag/mcbs/
https://www.bleepingcomputer.com/news/security/
https://www.bleepingcomputer.com/news/security/new-dysphoria-ddos-botnet-spreads-to-200k-devices-worldwide/

#セキュリティ #脆弱性 #情報漏洩 #DDoS #ゆっくり解説 #ずんだもん

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年7月30日）</h1>
<p><strong>キーワード:</strong> BMC / 医療データ / FastJson / VeloCloud / Dysphoria / DDoS</p>
<h2>オープニング：2026年7月30日 — セキュリティニュース</h2>
<p>直近の専門報道から、古い管理機能、医療委託先、開発ライブラリ、ネットワーク管理装置、家庭用ルーターという五つの入口を選んだ。共通点は、利用者の目に触れにくい「裏側」の資産が侵入口になっていることだ。</p>
<h2>2万4000台超のサーバー管理機能がパスワードハッシュを漏えい</h2>
<p>7月28日、インターネットへ露出した2万4000台超のサーバーBMCが、約20年前から知られる弱点により認証用パスワードハッシュを漏らしていると報じられた。BMCは本体OSが停止していても電源やコンソールを遠隔管理できるため、一般の業務画面より強い権限を持つ。</p>
<p>管理者はBMCを公開インターネットから隔離し、管理ネットワークやVPN経由に限定する必要がある。パッチだけでなく、既定・再利用パスワードの変更、アクセスログ、外部検索で自社装置が見えていないかを確認したい。</p>
<h2>医療請求会社MCBSの侵害、126万人に影響</h2>
<p>医療請求会社Medical Computer Business Servicesは、2025年のネットワーク侵害で126万人の機微情報が露出したと7月28日に公表した。医療機関そのものではなく請求処理の委託先が、多数の患者データを集中して扱うサプライチェーン上の弱点になった。</p>
<p>対象者は通知の真偽を公式窓口で確認し、医療保険明細、身に覚えのない請求、信用情報を継続監視する。組織側には、委託先へ渡す項目と保存期間を減らし、契約終了後の削除証明まで確認する課題がある。</p>
<h2>FastJsonのゼロデイ、操作不要で遠隔コード実行</h2>
<p>7月27日、オープンソースのJavaライブラリFastJsonの未修正脆弱性が米企業への攻撃で悪用され、認証や利用者操作なしに遠隔コード実行へ至ると報じられた。ライブラリはアプリの奥に組み込まれるため、製品名だけの資産台帳では影響を見落としやすい。</p>
<p>開発・運用担当は依存関係表からFastJsonの使用箇所と外部入力経路を特定し、提供元の更新、回避策、侵害痕跡を確認する。通信遮断だけで済ませず、不審な子プロセス、作成ファイル、外向き通信を調べる必要がある。</p>
<h2>VeloCloud Orchestratorの最重要ゼロデイ</h2>
<p>Aristaは7月27日、オンプレミス版VeloCloud Orchestratorで攻撃に悪用されている最重要のコマンドインジェクション脆弱性を修正した。広域ネットワークを統括する装置が侵害されると、単一端末ではなく拠点間通信の設定と認証情報へ影響が及ぶ。</p>
<p>対象はオンプレミス展開であり、クラウド利用者と混同せず公式情報で版と構成を照合する。更新後も管理画面の外部公開、管理者ログイン、設定変更履歴、生成されたアカウントを点検する。</p>
<h2>20万台規模のDysphoriaボットネット</h2>
<p>7月27日、Dysphoriaが世界約20万台のルーター、カメラ、IoT機器を侵害し、DDoS攻撃と通信中継に使っていると報じられた。イーサリアムENSとソラナSNSから指令先情報を取得し、遮断を難しくする。7月14日から20日の監視では1日最大74万回の応答が観測された。</p>
<p>感染は弱いTelnet・SSH認証情報と既知脆弱性を利用する。利用者は既定管理者パスワードを変更し、ファームウェアを更新し、不要な遠隔管理とUPnPを止める。古く更新不能な機器は交換も含めて判断する。</p>
<h2>まとめ</h2>
<p>今日の五件は「画面に警告が出ない資産」を棚卸しする重要性を示す。BMC、委託先、依存ライブラリ、管理装置、IoT機器について、存在、公開範囲、更新責任、ログの所在を答えられる状態が防御の出発点になる。</p>
<h2>参考ソース</h2>
<ul>
<li><a href="https://www.bleepingcomputer.com/">BleepingComputer: 24,000 exposed server BMCs</a></li>
<li><a href="https://www.bleepingcomputer.com/tag/mcbs/">BleepingComputer: MCBS breach affects 1.26 million people</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/">BleepingComputer: FastJson RCE zero-day</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/">BleepingComputer: VeloCloud Orchestrator zero-day</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/new-dysphoria-ddos-botnet-spreads-to-200k-devices-worldwide/">BleepingComputer: Dysphoria botnet</a></li>
</ul>

</details>

---

[← 2026-07-30 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
