---
title: "398件の更新と顔画像900万件露出｜セキュリティ6選【2026/08/25】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# 398件の更新と顔画像900万件露出｜セキュリティ6選【2026/08/25】

**2026-08-25 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-25-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-25-security)

---

## 概要

マイクロソフトの398件修正、スノーフレーク利用165組織超への恐喝、認証基盤と家庭用ルーターの欠陥、子ども・顔画像のプライバシー問題を具体策まで解説します。

▼ 今日のトピック
・マイクロソフトが少なくとも398件を修正
・スノーフレーク利用組織165社超への侵入と恐喝
・キークロークとケイリックス製ルーターの重大欠陥
・ティックトックの4億ドル和解
・クラリティチェックの顔画像900万件超露出

▼ 参考記事・ソース
https://krebsonsecurity.com/2026/08/microsoft-plugs-nearly-400-security-holes/
https://krebsonsecurity.com/2026/08/canadian-man-pleads-guilty-in-snowflake-extortions/
https://thehackernews.com/2026/08/critical-keycloak-password-reset-flaw.html
https://www.bleepingcomputer.com/news/security/unpatched-calix-flaw-lets-hackers-bypass-nat-to-expose-internal-devices/
https://www.bleepingcomputer.com/news/legal/tiktok-reaches-400m-settlement-with-us-over-coppa-violations/
https://www.wired.com/story/reverse-lookup-service-exposed-millions-of-photos-of-peoples-faces/

#セキュリティ #サイバー攻撃 #脆弱性 #情報漏洩 #ゆっくり解説 #ずんだもん

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年8月25日）</h1>
<p><strong>キーワード:</strong> Microsoft更新398件 / Snowflake恐喝165組織 / Keycloak認証回避 / Calixルーター / TikTok和解4億ドル / 顔画像900万件</p>
<h2>オープニング：2026年8月25日 — セキュリティニュース</h2>
<ul>
<li>大規模更新、クラウド恐喝、認証基盤、家庭用ルーター、子どもの個人情報、顔画像検索の6本を扱う。</li>
</ul>
<h2>Microsoft、398件を修正　悪用中の脆弱性も含む</h2>
<ul>
<li>Microsoftは8月の月例更新でWindowsと対応製品の脆弱性少なくとも398件を修正した。</li>
<li>Krebs on Securityによると、1件はすでに悪用され、別の2件は更新前に詳細が公開されていた。</li>
<li>利用者は再起動を含む更新完了を確認し、組織は悪用中の問題を優先して展開する必要がある。</li>
</ul>
<h2>Snowflake恐喝、26歳被告が165組織超への侵入を認める</h2>
<ul>
<li>カナダ人コナー・ライリー・モウカ被告は、Snowflake利用組織165社超への侵入と恐喝に関する罪を認めた。</li>
<li>同被告は1億人超のAT&amp;T顧客の通話・SMS履歴を盗んだことも認めたとKrebs on Securityが報じた。</li>
<li>クラウド自体の破壊より、盗まれた認証情報と多要素認証の不足が連鎖被害を広げた事件である。</li>
</ul>
<h2>Keycloak、認証なしでアカウントを奪える重大欠陥</h2>
<ul>
<li>Red HatとKeycloakは、パスワード再設定を強制して任意アカウントを奪えるCVE-2026-18963を修正した。</li>
<li>CVSS評価は9.1で、攻撃者は事前ログインなしに遠隔から悪用できるとされる。</li>
<li>Keycloakを組織の共通ログインに使う場合、一つの欠陥が多数サービスへの入口になるため更新を急ぐ必要がある。</li>
</ul>
<h2>Calix家庭用ルーター、NATを越えて内部機器を公開</h2>
<ul>
<li>Calix GS7 XGSのGS5239XGには、認証なしの遠隔攻撃者がポート転送規則を作れる未修正欠陥がある。</li>
<li>悪用されると、通常はNATの内側にあるカメラや保存装置などがインターネットへ露出し得る。</li>
<li>利用者は通信事業者の案内を確認し、管理画面の公開状況と見覚えのない転送規則を点検する。</li>
</ul>
<h2>TikTok、米国の子どもプライバシー訴訟で4億ドル和解</h2>
<ul>
<li>米司法省はTikTok、ByteDanceなどがCOPPAに違反したとする2024年訴訟で4億ドルの和解を発表した。</li>
<li>報道では3億ドルを直ちに支払い、過去の同意命令を無効にする命令が出た場合に追加1億ドルを支払う。</li>
<li>年齢確認、保護者同意、削除という運用を実際に機能させる責任が、罰金額として示された。</li>
</ul>
<h2>逆画像検索ClarityCheck、顔画像900万件超を露出</h2>
<ul>
<li>WIREDによると、人探しサービスClarityCheckが逆画像検索に用いる900万件超の画像を公開状態にしていた。</li>
<li>同社は検索を「private and secure」と宣伝していたが、顔写真そのものを含むデータベースの保護が伴っていなかった。</li>
<li>顔はパスワードのように交換できないため、サービス選定では検索結果だけでなく保存期間と削除方法も重要になる。</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>今日の6本は、更新の遅れ、認証情報の再利用、共通ログイン、家庭機器、年齢確認、顔データという異なる入口を示した。</li>
<li>個人はOS・ルーター更新と多要素認証、組織は認証基盤と保存データの範囲を優先して見直したい。</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://krebsonsecurity.com/2026/08/microsoft-plugs-nearly-400-security-holes/">Krebs on Security: Microsoft Plugs Nearly 400 Security Holes</a></li>
<li><a href="https://krebsonsecurity.com/2026/08/canadian-man-pleads-guilty-in-snowflake-extortions/">Krebs on Security: Canadian Man Pleads Guilty in Snowflake Extortions</a></li>
<li><a href="https://thehackernews.com/2026/08/critical-keycloak-password-reset-flaw.html">The Hacker News: Critical Keycloak Password Reset Flaw</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/unpatched-calix-flaw-lets-hackers-bypass-nat-to-expose-internal-devices/">BleepingComputer: Unpatched Calix flaw</a></li>
<li><a href="https://www.bleepingcomputer.com/news/legal/tiktok-reaches-400m-settlement-with-us-over-coppa-violations/">BleepingComputer: TikTok reaches $400M settlement</a></li>
<li><a href="https://www.wired.com/story/reverse-lookup-service-exposed-millions-of-photos-of-peoples-faces/">WIRED: Reverse-Lookup Service Exposed Millions of Photos</a></li>
</ul>

</details>

---

[← 2026-08-25 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
