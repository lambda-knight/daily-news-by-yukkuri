---
title: "NetScaler認証突破とCVSS 10.0、家庭ルーターも踏み台に【2026/08/16】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# NetScaler認証突破とCVSS 10.0、家庭ルーターも踏み台に【2026/08/16】

**2026-08-16 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-16-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-16-security)

---

## 概要

2026年8月16日のセキュリティニュースを、技術者と一般利用者の両方に向けて解説します。

▼ 主なトピック
・NetScaler ADC/GatewayのCVE-2026-8452：SAML構成で認証なしコード実行の恐れ
・Adobe ColdFusionなど：CVSS 10.0を含む重大欠陥3件
・Linuxボットネット「Evooo1Bot」：家庭用ルーターをSOCKS5中継ノード化
・硬貨サイズの装置と60秒未満の物理アクセスで旅客機へ影響する研究
・AIとの20回未満のやり取りで発見されたZoomの修正済みバグ
・米税関国境警備局職員による内部データベースの私的濫用疑惑
・広告追跡業者を可視化する無料サービス「DecryptAds」

境界機器はパッチ適用とSAML構成の棚卸し、家庭ではルーター管理画面の外部公開停止、初期パスワード変更、ファームウェア更新が具体策です。

#セキュリティ #脆弱性 #NetScaler #ColdFusion #ボットネット #情報漏洩

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年8月16日）</h1>
<p><strong>キーワード:</strong> NetScaler脆弱性 / Adobe ColdFusion / Evooo1Botボットネット / Boeing737ハッキング / Zoom画面共有 / CBP職員の私的監視 / DecryptAds</p>
<h2>オープニング：2026年8月16日 — セキュリティニュース</h2>
<p>本日は、Citrix NetScalerの認証なしリモートコード実行、Adobeが公開したCVSS満点の脆弱性3件、家庭用ルーターを乗っ取るボットネット「Evooo1Bot」、硬貨サイズの装置で旅客機を乗っ取れるという研究報告、AIが20回未満のやり取りで見つけたZoomの乗っ取りバグ、米税関職員による内部データベースの私的濫用、そして自分を追跡する広告業者を調べられる新サービスの7件を扱う。境界機器の脆弱性と、内部関係者・製造現場側のリスクが同時に目立つ一日だった。</p>
<h2>NetScaler ADC/Gatewayに認証不要のリモートコード実行、SAML構成が標的</h2>
<ul>
<li>watchTowr Labsが2026年8月14日、Citrix NetScaler ADCとNetScaler Gatewayに関する脆弱性（CVE-2026-8452）の詳細分析を公開した。JPCERT/CCも同月15日付で注意喚起を出している。</li>
<li>Citrixは当初、この脆弱性を2026年6月30日公開のサービス運用妨害（DoS）に関連するものとして扱っていたが、watchTowrの分析により、NetScalerをSAMLのSPまたはIdPとして構成している場合、認証なしでリモートコード実行につながる可能性が明らかになった。</li>
<li>企業のリモートアクセスの入り口にあたる機器のため、SAML連携でNetScalerを使う組織は影響範囲の特定とパッチ適用状況の確認を急ぐ必要がある。</li>
</ul>
<h2>Adobe、ColdFusion・Campaign ClassicにCVSS満点10.0の脆弱性3件を修正</h2>
<ul>
<li>Adobeが、ColdFusion・Commerce・Campaign Classicに影響する複数の重大な脆弱性を修正する更新を公開した。悪用されると任意コード実行や権限昇格につながる恐れがある。</li>
<li>最も深刻なCVE-2026-48362（CVSS 10.0）はColdFusionのOSコマンドインジェクションで、認証なしにサーバー側で任意のOSコマンドを実行できる可能性がある。他にも満点評価の欠陥が含まれる。</li>
<li>ColdFusionは古くから企業の業務システムで使われ続けており、更新が後回しにされやすい製品でもあるため、稼働中のサーバーの棚卸しと優先適用が求められる。</li>
</ul>
<h2>Linuxボットネット「Evooo1Bot」、家庭用ルーターをSOCKS5中継ノード化</h2>
<ul>
<li>Mirai系列の新型モジュール式Linuxボットネット「Evooo1Bot」が、インターネットに露出したゲートウェイ機器を狙い、感染機器をSOCKS5トラフィック中継ノードに変える活動が確認された。</li>
<li>中継ノード化されたルーターは、攻撃者が別の攻撃の踏み台として通信を経由させる「プロキシ網」の一部として悪用される。持ち主が気づかないまま自宅の回線が犯罪インフラの一部になる。</li>
<li>家庭用ルーターの管理画面を外部に公開しない設定、初期パスワードの変更、ファームウェア更新が引き続き基本対策になる。</li>
</ul>
<h2>硬貨サイズの装置で60秒以内にボーイング737の自動操縦を乗っ取れると報告</h2>
<ul>
<li>セキュリティ研究者が、機体外部のハッチを開けて硬貨サイズの装置を接続するだけで、60秒足らずのうちに自動操縦の操作や飛行計画の改ざんが可能だったと報告した。</li>
<li>航空機の物理的なアクセスポイントに対する検証で、従来はサイバー攻撃というと機内Wi-Fiやネットワーク経由の侵入が想定されてきたが、機体外部への短時間の物理接触だけで重大な影響を及ぼせる点が新しい。</li>
<li>航空業界にとっては、駐機中の機体周辺の物理的な警備・監視体制の見直しが必要になる事例で、乗客が直接できる対策はないが、業界全体の安全確保の課題として扱われている。</li>
</ul>
<h2>AIが20回未満のやり取りで発見、ZoomのバグでAI通話参加者の端末を乗っ取り可能に</h2>
<ul>
<li>研究者らが、公開されているAIツールに指示を出す形で、Zoom通話中に他の参加者の端末を乗っ取れる画面共有機能のバグを発見した。修正は既に完了している。</li>
<li>従来は人手による地道な解析が必要だった脆弱性発見の作業を、AIへの20回に満たないプロンプトのやり取りだけで到達できたと報告されている点が注目されている。</li>
<li>修正済みのため一般利用者が今すぐ対応することはないが、脆弱性発見そのものがAIによって高速化しつつあることを示す事例で、開発側の脆弱性対応スピードも合わせて問われることになる。</li>
</ul>
<h2>米税関国境警備局(CBP)職員、内部データベースで元恋人や同僚を私的に追跡</h2>
<ul>
<li>WIREDが入手した記録により、CBP（税関国境警備局）職員が業務用の内部データベースを私的に悪用し、恋愛対象や同僚の携帯電話を追跡していたとする数百件の疑惑が明らかになった。</li>
<li>本来は入出国管理や捜査目的で使われるべきデータベースへのアクセス権限が、職員個人の私的な動機で乱用されていたとされる内容で、監督・監査体制の不備が背景にあるとみられる。</li>
<li>政府機関が保有する強力な追跡権限は、外部からの攻撃だけでなく、権限を持つ内部関係者による濫用も同時に警戒する必要があることを示す事例。</li>
</ul>
<h2>自分を追跡する広告業者を洗い出せる無料サービス「DecryptAds」が登場</h2>
<ul>
<li>誰が自分のWebサイト閲覧やアプリ利用データを収集しているかを特定するのは難しく、これまでは広告テック企業側に情報が囲い込まれてきた。</li>
<li>新しい無料サービス「DecryptAds」は、この広告テック関連データを収集・照合し、自分を追跡している業者の情報を簡単に調べられるようにするものとして紹介されている。</li>
<li>一般利用者が自分自身のデータの流れを可視化できる数少ない手段であり、プライバシー対策の第一歩として、まず自分がどの業者に追跡されているかを知りたい人に向く。</li>
</ul>
<h2>まとめ</h2>
<p>境界機器（NetScaler）とレガシー業務システム（ColdFusion）という「守りの要」の脆弱性、家庭用ルーターの乗っ取りという身近な被害、そして物理接触・AI活用という新しい攻撃手法の広がりが同時に報告された一日だった。加えて、CBP職員の事例は「外部の攻撃者」だけでなく「権限を持つ内部関係者」もリスク源であることを改めて示しており、監査体制の点検が組織側の課題として残る。</p>
<h2>参考ソース</h2>
<ul>
<li><a href="https://www.jpcert.or.jp/at/2026/at260024.html">JPCERT/CC: NetScaler ADCおよびNetScaler Gatewayにおけるリモートコード実行につながる脆弱性（CVE-2026-8452）に関する注意喚起</a></li>
<li><a href="https://thehackernews.com/2026/08/adobe-patches-three-cvss-100-coldfusion.html">The Hacker News: Adobe Patches Three CVSS 10.0 ColdFusion and Campaign Classic Flaws</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/new-evooo1bot-linux-botnet-turns-routers-into-traffic-relay-nodes/">Bleeping Computer: New Evooo1Bot Linux botnet turns routers into traffic relay nodes</a></li>
<li><a href="https://www.wired.com/story/this-coin-sized-device-can-hack-a-boeing-737/">WIRED: This Coin-Sized Device Can Hack a Boeing 737</a></li>
<li><a href="https://www.wired.com/story/a-zoom-screen-sharing-bug-let-anyone-take-over-other-devices-on-a-call/">WIRED: A Zoom Screen-Sharing Bug Let Anyone Take Over Other Devices on a Call</a></li>
<li><a href="https://www.wired.com/story/cbp-workers-allegedly-used-government-databases-to-spy-on-exes-crushes-and-colleagues/">WIRED: CBP Workers Allegedly Used Government Databases to Spy on Exes, Crushes, and Colleagues</a></li>
<li><a href="https://krebsonsecurity.com/2026/08/whos-tracking-you-use-this-new-service-to-find-out/">Krebs on Security: Who's Tracking You? Use This New Service to Find Out</a></li>
</ul>

</details>

---

[← 2026-08-16 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
