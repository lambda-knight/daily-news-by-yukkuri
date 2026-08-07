---
title: "1億人の通信履歴と570万ドル流出、便利な基盤の死角【2026/08/07】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# 1億人の通信履歴と570万ドル流出、便利な基盤の死角【2026/08/07】

**2026-08-07 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-07-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-07-security)

---

## 概要

Snowflake恐喝事件の有罪答弁から、KVM・Cisco・水道PLC・暗号資産・iCloud・子ども用GPS時計まで、今日確認すべき対策を解説します。

▼ 今日のトピック
・165組織超への侵入とAT&T顧客1億人超の通信履歴
・CVE-2026-64561とCiscoの深刻度9.8脆弱性
・外部露出したRockwell PLC 4,407台
・弱い乱数による暗号資産570万ドル以上の流出
・iCloud Private Relayと子ども用GPS時計のプライバシー

▼ 参考記事・ソース
・Krebs on Security https://krebsonsecurity.com/2026/08/canadian-man-pleads-guilty-in-snowflake-extortions/
・The Hacker News https://thehackernews.com/2026/08/cryptojs-weak-rng-behind-57-million-in.html
・WIRED https://www.wired.com/story/hackers-stalked-me-by-hijacking-a-smartwatch-for-kids/

#サイバーセキュリティ #情報漏洩 #脆弱性 #CVE #セキュリティニュース #ずんだもん #ゆっくり解説

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>Snowflake恐喝の有罪答弁から子ども用GPS時計まで（2026年8月7日）</h1>
<p><strong>キーワード:</strong> Snowflake / KVM / Cisco IOS XE / Rockwell PLC / CryptoJS / iCloud Private Relay</p>
<h2>オープニング：2026年8月7日 — セキュリティニュース</h2>
<p>2026年8月7日のセキュリティニュース。今日は「攻撃後の責任追及」「仮想化の境界」「ネットワーク機器と公共設備」「弱い乱数」「プライバシー機能の例外」「子どもの位置情報」をつなぎ、利用者と管理者が今確認すべきことを整理する。</p>
<h2>Snowflake恐喝事件、165組織超への侵入で26歳被告が有罪答弁</h2>
<ul>
<li>カナダ人のコナー・ライリー・ムーカ被告（26歳）が、クラウドデータ基盤Snowflakeを利用する165以上の組織への侵入・恐喝に関し、コンピューター詐欺と共謀を認めた</li>
<li>被告はAT&amp;T顧客1億人超の通話・テキスト履歴記録を盗んだことも認めた。本文内容ではなく通信履歴でも、人間関係や行動の推測につながる</li>
<li>企業はクラウド事業者任せにせず、多要素認証、使われていない認証情報の失効、異常な大量取得の監視を点検する必要がある</li>
</ul>
<h2>仮想マシンの壁を越える「Zapscape」——CVE-2026-64561</h2>
<ul>
<li>LinuxカーネルのKVMに、入れ子型仮想化の内側のゲストからホスト側でコードを実行しうる脆弱性CVE-2026-64561が報告された</li>
<li>攻撃には内側の仮想マシンでカーネル権限が必要で、入れ子型仮想化を信頼できない利用者へ公開する構成が主なリスクになる</li>
<li>管理者は影響するKVM/x86構成と修正版を確認し、更新まで入れ子型仮想化の公開範囲を狭める。一般利用者が直ちに端末を初期化する話ではない</li>
</ul>
<h2>CiscoがSD-WANとIOS XEの12件を修正——深刻度9.8が3件</h2>
<ul>
<li>CiscoはCatalyst SD-WANとIOS XEの計12件を修正し、このうち3件はCVSS 9.8。CVSSは脆弱性の深刻度を10点満点で示す指標で、9.8は極めて重大な区分</li>
<li>Catalyst SD-WANは設定にかかわらず影響し、IOS XEは自律型またはコントローラー型で動作する場合が対象と報じられた</li>
<li>管理者は製品名だけでなく、稼働モードとバージョンを資産台帳で照合して更新する。外部公開された管理画面の制限とログ確認も必要</li>
</ul>
<h2>水道攻撃都市にも露出、Rockwell製PLC 4,407台がネットから見える状態</h2>
<ul>
<li>8月3日の調査でRockwell Automation製PLCが世界で4,407台、うち米国で2,844台インターネットから確認された</li>
<li>最近水道施設へのサイバー攻撃があった都市では22台が見つかり、19台は同じ携帯通信事業者網を使っていた。ただし調査者は侵害を確認していない</li>
<li>PLCはポンプや設備を制御する産業用コンピューター。インターネットから見えることと乗っ取られたことは別だが、不要な直接公開を止め、認証・遠隔保守経路を棚卸しすべき</li>
</ul>
<h2>弱い乱数で暗号資産570万ドル以上流出——CryptoJSの12年前の設計</h2>
<ul>
<li>CryptoJSの<code>WordArray.random()</code>が十分に予測困難な乱数を作れず、五つの暗号資産ウォレットアプリの復旧フレーズ生成に影響した</li>
<li>オンチェーン分析では5月下旬以降の二度の資金移動で、被害下限は570万ドル。古い共通ライブラリの設計が複数アプリへ伝播した例</li>
<li>対象アプリの利用者は公式告知を確認し、影響する方法で作った復旧フレーズなら、安全な実装で新しいウォレットを作って資産を移す。復旧フレーズを第三者サイトへ入力してはならない</li>
</ul>
<h2>iCloud Private Relayの迂回で本来隠すIPアドレスが露出</h2>
<ul>
<li>Safari通信を二段階の中継に通すiCloud Private Relayについて、WebKitのプロキシ迂回により実IPアドレスが露出しうる問題が報告された</li>
<li>IPアドレスは正確な住所そのものではないが、利用回線やおおよその地域、複数アクセスの関連づけに使われる可能性がある</li>
<li>利用者はAppleの更新情報を確認し、OSとSafariを最新にする。Private Relayだけを匿名性の絶対保証と考えず、高い秘匿性が必要な作業では脅威モデルを見直す</li>
</ul>
<h2>子ども用GPSスマートウォッチ、遠隔追跡と盗聴につながる脆弱性</h2>
<ul>
<li>WIRED記者が子ども向けGPSスマートウォッチの脆弱性を使った実験で追跡・盗聴され、GPS機器の供給網全体の弱さが問題になった</li>
<li>家族の安心のための位置情報・通話機能が、認証や更新が弱いと第三者の監視手段へ反転する。価格や見た目だけでは安全性を判断できない</li>
<li>保護者はメーカーの更新提供期間、脆弱性窓口、アカウントの多要素認証、位置履歴の削除方法を確認する。不明なら常時装着や不要機能を見直す</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>今回の共通点は「便利な共有基盤」が被害の増幅器にもなること。クラウド、仮想化、ルーター、産業機器、暗号ライブラリ、プライバシー中継、GPS端末で同じ構図が見える</li>
<li>個人は公式更新、復旧フレーズの再生成判断、子ども端末の権限確認を行い、組織は多要素認証、資産台帳、外部公開範囲、異常な大量取得の監視を優先する</li>
<li>「露出」と「侵害」、「可能性」と「確認済み被害」を区別し、過度に恐れず、対象製品・構成・バージョンを確かめて対処する</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://krebsonsecurity.com/2026/08/canadian-man-pleads-guilty-in-snowflake-extortions/">Krebs on Security: Canadian Man Pleads Guilty in Snowflake Extortions</a></li>
<li><a href="https://thehackernews.com/2026/08/new-zapscape-kvm-flaw-could-let.html">The Hacker News: Zapscape KVM Flaw</a></li>
<li><a href="https://thehackernews.com/2026/08/cisco-patches-12-sd-wan-and-ios-xe.html">The Hacker News: Cisco SD-WAN and IOS XE Flaws</a></li>
<li><a href="https://thehackernews.com/2026/08/over-4400-rockwell-plcs-exposed-online.html">The Hacker News: Rockwell PLC Exposure</a></li>
<li><a href="https://thehackernews.com/2026/08/cryptojs-weak-rng-behind-57-million-in.html">The Hacker News: CryptoJS Weak RNG</a></li>
<li><a href="https://thehackernews.com/2026/08/webkit-proxy-bypasses-can-expose-real.html">The Hacker News: iCloud Private Relay IP Exposure</a></li>
<li><a href="https://www.wired.com/story/hackers-stalked-me-by-hijacking-a-smartwatch-for-kids/">WIRED: Hackers Stalked Me by Hijacking a Smartwatch for Kids</a></li>
</ul>

</details>

---

[← 2026-08-07 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
