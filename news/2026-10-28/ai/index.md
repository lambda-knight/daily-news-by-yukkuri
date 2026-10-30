---
title: "Volt Typhoon、8時間で消える中継網でゼロデイを隠す ほか今週のセキュリティ 2026/10/28"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# Volt Typhoon、8時間で消える中継網でゼロデイを隠す ほか今週のセキュリティ 2026/10/28

**2026-10-28 / 生成AIニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-10-28-ai/ai_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-10-28-ai)

---

## 概要

短縮回。中国系とされるVolt Typhoonが、8時間で消える使い捨て中継網「Silent Train」の陰で管理基盤のゼロデイを使っていた件と、ソネット・ぷららの会員情報流出などの最近のインシデントを、ずんだもんと四国めたんが解説します。

▼ 今日のトピック
・Volt Typhoon、使い捨て中継網「Silent Train」でゼロデイ攻撃を隠す
・最近のインシデント一覧（ソニーネットワークコミュニケーションズ、韓国の大信証券ほか、Virtualine押収）

▼ 参考記事・ソース
・BleepingComputer「Volt Typhoon hides zero-day attacks using 'Silent Train' framework」 https://www.bleepingcomputer.com/news/security/volt-typhoon-hides-zero-day-attacks-using-silent-train-framework/
・BleepingComputer「Sony ISP subsidiary data breach exposes 2.5 million customer records」 https://www.bleepingcomputer.com/news/security/sony-isp-subsidiary-data-breach-exposes-25-million-customer-records/
・TechCrunch「South Korea's financial industry hit by fresh wave of cyberattacks」 https://techcrunch.com/2026/10/28/south-koreas-financial-industry-hit-by-fresh-wave-of-cyberattacks/
・BleepingComputer「Police seize Virtualine bulletproof service tied to ransomware, cybercrime」 https://www.bleepingcomputer.com/news/security/police-seize-virtualine-bulletproof-service-tied-to-ransowmare-cybercrime/

#生成AI #LLM #AI #人工知能 #ゆっくり解説 #ずんだもん #四国めたん #AIニュース

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>生成AI・量子・セキュリティニュース（2026年10月28日）</h1>
<p><strong>キーワード:</strong> GPT-4oと抗てんかん薬の訴訟 / Anthropic上場後の支配構造 / IBMのメートル級L-coupler / Volt Typhoonの「Silent Train」</p>
<h2>オープニング：2026年10月28日 — 生成AI・量子・セキュリティニュース</h2>
<ul>
<li>今日は短縮回として、セキュリティの2本だけを扱います。</li>
<li>セキュリティでは、中国系とされるVolt Typhoonが使い捨ての中継網でゼロデイ攻撃を隠した手口と、直近のインシデント一覧を扱います。</li>
</ul>
<h2>セキュリティ：Volt Typhoon、使い捨て中継網「Silent Train」でゼロデイ攻撃を隠す</h2>
<ul>
<li>LumenのBlack Lotus Labsは10月28日、中国の国家支援とされるVolt Typhoonが3年にわたって使ってきた中継網「Silent Train」の報告を出しました（BleepingComputer、10月28日）。</li>
<li>確認されたゼロデイは、VeloCloud Orchestrator（CVE-2026-16812）、Cisco Catalyst SD-WAN（CVE-2026-20127）、N-able N-central（CVE-2025-8875、CVE-2025-8876）、Versa Director（CVE-2024-39717）で、いずれもネットワークの管理基盤です。</li>
<li>攻撃は米国外の仮想サーバーから、乗っ取ったIntelbras製モデム（国外）とNetgear Orbi（米国内）を経由して始めます。1回の作業は通常8時間未満で、終わると鍵や設定、道具をすべて消します。</li>
<li>2025年初めからは、使い捨ての中継に加えて、乗っ取った企業のシステムを1〜3か月保持する混合型になりました。管理基盤を握ると、その先の顧客の網にも入れます。</li>
<li>標的は通信、政府、防衛、教育、電力などで、カリフォルニア、テキサス、ハワイが多く、インド太平洋を意識した可能性があるとしています。FBIが以前の「KV-Botnet」を壊したことが、この方式に移った一因とされます。</li>
<li>推奨策は、管理画面をインターネットから遮断し、修正を急ぎ、ログを長く保存して、普段と違う管理操作を監視することです。</li>
</ul>
<h2>セキュリティ：最近のインシデント一覧</h2>
<ul>
<li>ソニーネットワークコミュニケーションズ（10月27日公表／会員データベースへの不正アクセス）：10月19日に侵入され、4日後に検知。So-net会員214万1986件と、NTTドコモから受託するplala（Sコース）44万3495件の計258万5481件で、氏名、電話番号、メールアドレス、生年月日などが漏れた。5万4401件はメールのパスワードも流出。決済情報は含まれず、悪用は未確認</li>
<li>韓国の大信証券ほか（10月28日報道／サイバー攻撃）：大信証券で顧客3万8490人の氏名、メールアドレス、携帯電話番号が流出。未来アセット系の資産運用会社と暗号資産取引所Bithumbも別々の事案を報告したが、顧客データの流出は未確認。金融委員会は民間のIT基盤数十件を点検する。9月の攻撃は、中国拠点とみられる人物がAIの侵入試験ツール「Artex」を使ったとCrowdStrikeが分析</li>
<li>防弾ホスティング「Virtualine」（10月28日に押収発表／犯罪基盤の摘発）：FBIが主ドメインを押収し、オランダ警察はリンブルフ州で数十台の物理サーバーを押収、3000超の利用者のデータを回収した。資金の約5％はランサムウェア集団、約44％はロシアの薬物市場からとTRMが分析。逮捕者は報じられていない</li>
<li>対策：ISPの会員情報が漏れた後は、事業者を名乗るメールや偽サイトに注意し、同じパスワードを使い回しているサービスはすべて変更してください。</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>Volt Typhoonは、8時間で消える中継網の陰で、管理基盤のゼロデイを使っていました。</li>
<li>ソネット・ぷららの会員258万件の流出、韓国の証券会社の流出、犯罪者向けサーバー貸し業者Virtualineの押収が続きました。</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/volt-typhoon-hides-zero-day-attacks-using-silent-train-framework/">BleepingComputer: Volt Typhoon hides zero-day attacks using 'Silent Train' framework</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/sony-isp-subsidiary-data-breach-exposes-25-million-customer-records/">BleepingComputer: Sony ISP subsidiary data breach exposes 2.5 million customer records</a></li>
<li><a href="https://techcrunch.com/2026/10/28/south-koreas-financial-industry-hit-by-fresh-wave-of-cyberattacks/">TechCrunch: South Korea's financial industry hit by fresh wave of cyberattacks</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/police-seize-virtualine-bulletproof-service-tied-to-ransowmare-cybercrime/">BleepingComputer: Police seize Virtualine bulletproof service tied to ransomware, cybercrime</a></li>
</ul>

</details>

---

[← 2026-10-28 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
