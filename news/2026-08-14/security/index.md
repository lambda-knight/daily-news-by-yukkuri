---
title: "Snowflake恐喝犯が司法取引、AIの推論が盗まれる新脆弱性も【2026/08/14】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# Snowflake恐喝犯が司法取引、AIの推論が盗まれる新脆弱性も【2026/08/14】

**2026-08-14 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-14-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-14-security)

---

## 概要

Snowflake恐喝事件の司法取引、SharePoint認証バイパス実悪用、OpenAI・Anthropic・GoogleのAI推論漏えい、Trezorの委託先経由漏洩、子供用スマートウォッチ乗っ取り、ホワイトハウスのハックバック新方針を解説します。

▼ 参考ソース
https://krebsonsecurity.com/2026/08/canadian-man-pleads-guilty-in-snowflake-extortions/
https://thehackernews.com/2026/08/attackers-exploit-sharepoint.html
https://thehackernews.com/2026/08/openai-anthropic-google-api-flaw-let.html
https://www.bleepingcomputer.com/news/security/trezor-discloses-data-breach-affecting-nearly-14-000-customers/
https://www.wired.com/story/hackers-stalked-me-by-hijacking-a-smartwatch-for-kids/
https://www.bleepingcomputer.com/news/security/white-house-taps-security-firms-for-offensive-hack-back-operations/

#サイバーセキュリティ #脆弱性 #AIセキュリティ #情報漏洩 #情報セキュリティ #ずんだもん

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年8月14日）</h1>
<p><strong>キーワード:</strong> Snowflake恐喝 / SharePoint認証バイパス / AI推論漏えい / Trezor情報漏洩 / 子供用スマートウォッチ / ハックバック</p>
<h2>オープニング：2026年8月14日 — セキュリティニュース</h2>
<p>本日は、Snowflake恐喝事件の司法取引、SharePointの認証バイパス実悪用、生成AI推論を盗み見る脆弱性、Trezorの委託先経由データ漏洩、子供用スマートウォッチの乗っ取り、そしてホワイトハウスの「ハックバック」新方針の6件を扱う。攻撃側の摘発と新種の脆弱性、政策転換が同時に動いた一日だった。</p>
<h2>Snowflake恐喝事件、実行役のカナダ人が司法取引に応じる</h2>
<ul>
<li>カナダ・オンタリオ州キッチナー在住のコナー・ライリー・モウカ容疑者（26）が、コンピュータ詐欺および共謀の罪で有罪を認めた。</li>
<li>クラウドストレージ大手Snowflakeを使う165以上の組織へ不正侵入・恐喝を行ったとされ、2024年最も影響の大きいサイバー犯罪者の一人と評されてきた人物。</li>
<li>米AT&amp;Tの1億人超の顧客の通話・SMS履歴を盗んだことも認めており、単一の司法取引で大規模漏洩の全容が明らかになった形。</li>
</ul>
<h2>SharePoint認証バイパスCVE-2026-55040、PoC公開後に実悪用</h2>
<ul>
<li>Microsoft SharePointの認証バイパス脆弱性CVE-2026-55040（CVSS 9.1）が、2026年7月のパッチチューズデーで修正済みだったにもかかわらず、実証コード（PoC）の公開後に攻撃者による悪用が始まった。</li>
<li>弱い認証処理が原因のセキュリティ機能バイパスで、パッチ適用が遅れた環境が標的になっている。</li>
<li>修正済みでも公開直後に悪用が急増する典型例で、企業は「パッチ適用済み」を確認するだけでなく適用タイミングの速さも問われる。</li>
</ul>
<h2>AI推論を盗み見る脆弱性、OpenAI・Anthropic・Googleに共通</h2>
<ul>
<li>OpenAI、Anthropic、Googleの推論API間でやり取りされる「隠された推論」の受け渡し方式に欠陥が見つかり、研究者がセッションログから内部推論やAPIキー、パスワードなどの秘密情報を復元できた。</li>
<li>暗号化された推論オブジェクトが、あるセッションで作られたブロックを別のセッションへ再生（リプレイ)できてしまう弱点が原因。</li>
<li>生成AIの「思考過程」自体が新たな攻撃対象になりつつあることを示す事例で、開発者はAPI連携時のログ管理を見直す必要がある。</li>
</ul>
<h2>Trezor、物流委託先経由で1万4千人分のデータ漏洩</h2>
<ul>
<li>ハードウェアウォレット大手Trezorが、出荷・物流業務を委託しているShipMonkがハッキングされたことで、自社顧客約1万4千人分のデータが漏洩したと公表した。</li>
<li>直接の侵入はTrezor自身ではなく委託先経由で、サプライチェーン上の弱点が暗号資産保有者の情報流出につながった。</li>
<li>仮想通貨の資産を守るハードウェアを扱う企業でも、配送情報を扱う外部業者が最も弱い環穴になり得ることを示す。</li>
</ul>
<h2>子ども用スマートウォッチ乗っ取りで位置情報と会話を盗聴</h2>
<ul>
<li>WIRED誌の記者が使ったピンク色のプラスチック製子供用スマートウォッチについて、セキュリティ研究者が脆弱性を突いて位置情報の追跡と会話の盗聴に成功した。</li>
<li>GPS内蔵ガジェットのサプライチェーン全体に根深いセキュリティの甘さがあることの一例として報告された。</li>
<li>子供の見守りを目的とした製品が、逆に子供の居場所や会話を第三者に知られるリスクを生んでいる点が問題視されている。</li>
</ul>
<h2>ホワイトハウス、民間企業へ「ハッキングし返す」権限付与を検討</h2>
<ul>
<li>トランプ大統領が署名した覚書により、米国家調整センター（NCC）が、海外のサイバー犯罪組織を「ハックし返す」ための民間セキュリティ企業向け承認プログラムを整備するよう指示された。</li>
<li>民間企業が政府の承認を得たうえで攻撃的な対抗措置（ハックバック）を取れるようにする内容で、従来の防御中心の政策からの転換となる。</li>
<li>誤爆や第三国のインフラを巻き込むリスクなど、攻撃的サイバー対応の法的・技術的な線引きが今後の焦点になる。</li>
</ul>
<h2>まとめ</h2>
<p>司法手続きによる大物摘発、パッチ済み脆弱性の実悪用、生成AIの新しい攻撃対象、委託先経由の情報漏洩、消費者向けIoTの盗聴リスク、そして政策としての攻撃的対応という、防御と攻撃の両面が動いた一日だった。パッチ適用の速さ、委託先の管理、AIログの取り扱いが当面の実務的な優先課題になる。</p>
<h2>参考ソース</h2>
<ul>
<li><a href="https://krebsonsecurity.com/2026/08/canadian-man-pleads-guilty-in-snowflake-extortions/">Krebs on Security: Canadian Man Pleads Guilty in Snowflake Extortions</a></li>
<li><a href="https://thehackernews.com/2026/08/attackers-exploit-sharepoint.html">The Hacker News: Attackers Exploit SharePoint Authentication Bypass After Public PoC Release</a></li>
<li><a href="https://thehackernews.com/2026/08/openai-anthropic-google-api-flaw-let.html">The Hacker News: OpenAI, Anthropic, Google API Flaw Let Weaker AI Models Decode Stronger Models' Reasoning</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/trezor-discloses-data-breach-affecting-nearly-14-000-customers/">Bleeping Computer: Trezor discloses data breach affecting nearly 14,000 customers</a></li>
<li><a href="https://www.wired.com/story/hackers-stalked-me-by-hijacking-a-smartwatch-for-kids/">WIRED: Hackers Stalked Me by Hijacking a Smartwatch for Kids</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/white-house-taps-security-firms-for-offensive-hack-back-operations/">Bleeping Computer: White House taps security firms for offensive hack-back operations</a></li>
</ul>

</details>

---

[← 2026-08-14 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
