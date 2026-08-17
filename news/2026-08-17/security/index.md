---
title: "北朝鮮系ラザルスのゼロデイ攻撃、AI機材強盗まで【2026/08/17】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# 北朝鮮系ラザルスのゼロデイ攻撃、AI機材強盗まで【2026/08/17】

**2026-08-17 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-17-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-17-security)

---

## 概要

2026年8月17日のセキュリティニュースを、技術者と一般利用者の両方に向けて解説します。

▼ 主なトピック
・北朝鮮系ハッカー「Lazarus」：Windowsゼロデイで防衛・航空宇宙企業にバックドア
・VMware vCenterのCVE-2026-59310：パッチ公開直後から実悪用、持続的アクセスの手口
・マイクロソフト2026年8月月例更新：398件の脆弱性を修正、1件は実悪用済み
・AI開発ツール「LiteLLM」の不正パッケージ：PyPI公開40分で2,100超組織に影響のおそれ
・Chrome向け無料VPN拡張737件：正規サービスへのなりすましも確認
・暗号化メッセージアプリ「Threema」：大規模DDoS攻撃で通信障害
・AI用サーバー機材を狙う貨物強盗の暴力化（カリフォルニア州）

企業はvCenterとマイクロソフト製品のパッチ適用状況を優先確認し、個人は無料VPN拡張機能の開発元確認とWindows Updateの即時適用が具体策です。

#セキュリティ #脆弱性 #Lazarus #VMware #マイクロソフト #LiteLLM

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年8月17日）</h1>
<p><strong>キーワード:</strong> Lazarus / VMware vCenter / マイクロソフト月例更新 / LiteLLM / Chrome VPN拡張 / Threema DDoS / AIハードウェア強盗</p>
<h2>オープニング：2026年8月17日 — セキュリティニュース</h2>
<p>本日は、北朝鮮系ハッカー集団「Lazarus」によるWindowsゼロデイ悪用、仮想化基盤VMware vCenterの脆弱性の実悪用、マイクロソフトの2026年8月月例更新で398件の脆弱性が修正された件、AI開発でよく使われるツール「LiteLLM」の不正パッケージ問題、無料VPNを装うChrome拡張機能737件、暗号化メッセージアプリ「Threema」への大規模DDoS攻撃、そしてAI用サーバー機材を狙う貨物強盗の暴力化という7件を扱う。国家の関与が疑われる攻撃と、身近なアプリ・機材を狙う実利目的の犯罪が同時に目立つ一日だった。</p>
<h2>北朝鮮系ハッカー「ラザルス」、Windowsゼロデイで防衛・航空宇宙業界にバックドア設置</h2>
<ul>
<li>セキュリティ企業Check Point Researchが、北朝鮮の関与が指摘されるハッカー集団「Lazarus Group」が、マイクロソフトが修正したばかりのWindowsの脆弱性をパッチ公開前（ゼロデイ）の段階で悪用し、これまで確認されたことのない新型バックドアを設置していたと報告した。</li>
<li>標的はフランス・ドイツ・ブラジル・インドの防衛産業・航空宇宙関連企業で、偽の求人情報でやり取りに誘い込む「Operation Dream Job」という長年続く諜報活動キャンペーンの一環とされる。</li>
<li>一般利用者が直接狙われるものではないが、国家が関与するとされるハッカー集団が「まだ世に知られていない攻撃手法」を使い続けている実例で、防衛・航空関連企業は求人メールを装った接触への警戒が引き続き必要になる。</li>
</ul>
<h2>VMware vCenterの脆弱性CVE-2026-59310が実悪用、侵入後も居座り続ける手口</h2>
<ul>
<li>企業のサーバー仮想化基盤として広く使われるBroadcom VMware vCenterに、ネットワーク経由でアクセスできる攻撃者が任意のコードを実行できる脆弱性（CVE-2026-59310、CVSS評価9.8＝ほぼ最高値）が見つかり、パッチ公開後まもなく実際の攻撃で悪用されていることが、セキュリティ企業QUIRSOの調査で確認された。</li>
<li>「ディレクトリトラバーサル」と呼ばれる、本来アクセスできないはずのファイル領域へ不正に入り込む手口が使われている。vCenterは仮想サーバーを大量にまとめて管理する司令塔にあたるため、乗っ取られると社内の多数のサーバーへ被害が波及しうる。</li>
<li>「持続的なリモートアクセス」の確保が狙いとされ、侵入後も気づかれずに居座り続けられる点が企業にとって特に危険。vCenterを運用する企業はパッチ適用状況の緊急確認が必要になる。</li>
</ul>
<h2>マイクロソフト、2026年8月の月例更新で398件の脆弱性を修正</h2>
<ul>
<li>マイクロソフトが2026年8月の月例セキュリティ更新（いわゆるパッチチューズデー）で、Windowsおよび関連製品の少なくとも398件の脆弱性を修正した。このうち1件はすでに実際の攻撃で悪用されており、2件は更新公開前から情報が公表されていた。</li>
<li>JPCERT/CCも同時期に日本国内向けの注意喚起を公開し、脆弱性を悪用されるとリモートから任意のコードを実行されたり、ローカルの利用者によって権限を昇格されたりする可能性があるとしている。</li>
<li>「毎月大量に脆弱性が出るのは異常では」と感じるかもしれないが、これは月例更新として定例化された仕組みであり、家庭のパソコンでもWindows Updateを放置せず適用することが最も基本的な自衛策になる。</li>
</ul>
<h2>AI開発ツール「LiteLLM」の不正パッケージ、2100以上の組織に影響のおそれ</h2>
<ul>
<li>AIモデルを共通の形式で呼び出すために広く使われる開発ツール「LiteLLM」について、悪意あるコードを仕込んだ偽の配布パッケージがソフトウェア配布サイトPyPI上に約40分間だけ公開されていたことが分かった。短時間の公開でも、この間にダウンロードした開発者の環境からクラウドの認証キーやSSH鍵、データベースのパスワードなどが盗まれた可能性がある。</li>
<li>脅威情報企業CloudSEKが、攻撃者が盗み出したとみられる約43万4千件のファイルからなるデータを入手し分析した結果、2100を超える組織が情報漏洩の影響を受けた可能性があると報告した。</li>
<li>「つまりどういうこと？」と言えば、AI開発の裏側で使われる部品（ライブラリ）が一瞬でも汚染されると、それを取り込んだ企業のシステム全体の鍵が盗まれかねないということ。ソフトウェア部品を丸ごと信頼して使う開発現場のリスクが改めて示された。</li>
</ul>
<h2>Chrome向け無料VPN拡張機能737件が通信を密かに中継</h2>
<ul>
<li>ブラウザ拡張機能を調べたセキュリティ研究者が、無料のVPN・プロキシをうたうChrome拡張機能737件が、利用者の通信を勝手に別の中継網（プロキシ基盤）経由で流していたことを発見した。主にロシア語圏で、規制で塞がれたサービスへアクセスしたい利用者を狙ったものとみられる。</li>
<li>これらの拡張機能は少なくとも40のChromeウェブストア開発者アカウントから公開され、合計7万5486件インストールされていた。このうち274件は、実在する66種類の正規サービスになりすましていたことも確認された。</li>
<li>「VPNを入れたつもりが、逆に自分の通信を他人に覗かれる・利用される」という典型的な落とし穴。無料VPN拡張機能を入れている人は、開発元の実在性やレビューを確認し、身に覚えのない拡張機能は削除することが対策になる。</li>
</ul>
<h2>暗号化メッセージアプリ「Threema」、大規模DDoS攻撃で通信障害</h2>
<ul>
<li>プライバシー重視の暗号化メッセージアプリとして知られる「Threema」が今週、複数の大規模なDDoS（分散型サービス妨害）攻撃を受け、通信に深刻な障害が発生した。DDoS攻撃とは、大量のアクセスを一斉に送りつけてサーバーをパンクさせ、サービスを使えなくする攻撃手法。</li>
<li>Threemaは通話やメッセージ内容の秘匿性を重視して使われることが多いアプリで、内容そのものが盗まれたわけではないが、サービスが使えなくなること自体が利用者にとっての実害になる。</li>
<li>「なぜ暗号化アプリが狙われるのか」という点では、内容を盗む代わりに「使えなくすること」自体を目的にした妨害攻撃であり、通信の秘匿性と可用性（使い続けられること）は別の課題であることを示す事例。</li>
</ul>
<h2>AI用サーバー機材の争奪戦、貨物強盗が暴力化</h2>
<ul>
<li>WIREDの報道によると、カリフォルニア州で発生した2件の事件で、データセンター向けのサーバーなどAI関連機材を積んだ貨物を狙う強盗が、これまでにない暴力的な手口を伴って発生したという。専門家は「これまで見た中で最悪」と評している。</li>
<li>犯罪組織がAI用の高性能サーバー機材を物流の段階から狙うようになっている背景には、需要増と品薄によりこうした機材自体が高値で転売できる「実物資産」になっていることがあるとみられる。</li>
<li>サイバー攻撃だけでなく、AIブームが物理的な犯罪の形も変えつつあるという事例で、データセンター事業者や物流事業者にとっては、輸送経路や積み荷情報の管理強化が新たな課題になる。</li>
</ul>
<h2>まとめ</h2>
<p>国家の関与が疑われるLazarusのゼロデイ攻撃と、vCenterやマイクロソフト月例更新のような企業インフラの脆弱性対応が並ぶ一方、LiteLLMの不正パッケージやChromeの偽VPN拡張機能のように、開発者やごく普通の利用者が日常的に使う「部品」「便利ツール」が汚染されるケースも相次いだ。加えてThreemaへの妨害攻撃、AI機材を狙う貨物強盗の暴力化は、サイバー空間と物理空間の両方でAI関連の資産・インフラが攻撃対象として狙われやすくなっていることを示している。</p>
<h2>参考ソース</h2>
<ul>
<li><a href="https://thehackernews.com/2026/08/lazarus-exploits-windows-zero-day-to.html">The Hacker News: Lazarus Exploits Windows Zero-Day to Gain SYSTEM Access and Deploy Backdoor</a></li>
<li><a href="https://thehackernews.com/2026/08/attackers-exploit-vmware-vcenter.html">The Hacker News: Attackers Exploit VMware vCenter Vulnerability to Gain Persistent Remote Access</a></li>
<li><a href="https://krebsonsecurity.com/2026/08/microsoft-plugs-nearly-400-security-holes/">Krebs on Security: Microsoft Plugs Nearly 400 Security Holes</a></li>
<li><a href="https://www.jpcert.or.jp/at/2026/at260022.html">JPCERT/CC: 2026年8月マイクロソフトセキュリティ更新プログラムに関する注意喚起</a></li>
<li><a href="https://thehackernews.com/2026/08/malicious-litellm-releases-tied-to.html">The Hacker News: Malicious LiteLLM Releases Tied to Trivy Hack May Have Exposed 2,100+ Organizations</a></li>
<li><a href="https://thehackernews.com/2026/08/737-chrome-vpn-extensions-caught.html">The Hacker News: 737 Chrome VPN Extensions Caught Routing Traffic Through Proxies</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/large-scale-ddos-attacks-disrupted-threema-secure-messaging-service/">Bleeping Computer: Large-scale DDoS attacks disrupted Threema secure messaging service</a></li>
<li><a href="https://www.wired.com/story/the-worst-ive-ever-seen-cargo-thieves-are-turning-violent-in-pursuit-of-ai-hardware/">WIRED: 'The Worst I've Ever Seen': Cargo Thefts Have Turned Violent in Pursuit of AI Hardware</a></li>
</ul>

</details>

---

[← 2026-08-17 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
