---
title: "セキュリティニュース 2026-08-24"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# セキュリティニュース 2026-08-24

**2026-08-24 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-24-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-24-security)

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年8月24日）</h1>
<p><strong>キーワード:</strong> マイクロソフト月例570件AI起因 / 前科者運営ゼロデイ買取企業 / スマートTVプロキシ規制 / H96ストリーミングスティック広告詐欺 / ToxicPandaアプリブロック / WordPress wp2shell / RailsActiveStorageRCE</p>
<h2>オープニング：2026年8月24日 — セキュリティニュース</h2>
<ul>
<li>本日はマイクロソフトの月例更新が570件と過去最多を更新しAIが脆弱性発見を加速させている件、前科のある陰謀論者が運営するゼロデイ買取企業の実態、韓国LGがスマートTVの不正プロキシアプリを締め出す動き、格安ストリーミングスティック「H96」が広告詐欺網の踏み台になっていた件、Android向けマルウェア「ToxicPanda」がGoogle Playを機能停止させる新手口、WordPressの2件の脆弱性を組み合わせた「wp2shell」、Ruby on RailsのActive Storageに見つかったリモートコード実行の脆弱性まで7本を取り上げる</li>
</ul>
<h2>マイクロソフト月例更新、過去最多570件を修正　AIが脆弱性発見を加速</h2>
<ul>
<li>マイクロソフトは2026年7月14日、Windowsおよび対応ソフトウェアの脆弱性少なくとも570件を修正する月例更新を公開した。これは前月の記録的な更新件数からほぼ3倍に増えた数字で、うち約60件は「緊急（Critical）」評価、ゼロデイ脆弱性も3件含まれ、うち2件はすでに悪用が確認されている</li>
<li>マイクロソフトのパヴァン・ダヴルリ執行副社長は7月9日のブログで、この急増をAIによる脆弱性発見の高速化が原因と説明した。「AIの進歩により、より多くのコードでより速く、より多くの問題を発見できるようになっている」と述べている。Microsoft Copilotのリモートコード実行脆弱性（CVSS9.6、CVE-2026-48561）も含まれ、悪意あるサイトを訪れるだけでMicrosoft Edge for AndroidがCopilotへ不正な指示を自動送信する仕組みが悪用され得る</li>
<li>「AIが攻撃と防御の両方の速度を上げているのだ？」という点が今回の核心で、セキュリティ企業Tenableの研究者は、マイクロソフトが「悪用されにくい」と評価した脆弱性14件のうち13件について、Anthropicのレッドチームが実際に攻撃コードを生成できたと指摘している。人間の判断を前提にした深刻度評価そのものが、AI時代に追いついていない実態が浮き彫りになった</li>
</ul>
<h2>前科者2人が運営するゼロデイ買取企業「IRIS C2」、政府機関に取引実績なし</h2>
<ul>
<li>Krebs on Securityの報道によると、脆弱性研究者に最大700万ドルの報酬をちらつかせてゼロデイ攻撃コードを買い取るバージニア州の企業「IRIS C2」が、極右の陰謀論者で前科者のジャック・バークマン氏とジェイコブ・ウォール氏によって運営されていることが判明した</li>
<li>両氏は過去に架空の情報機関を装い、当時のFBI長官やピート・ブティジェッジ氏らへの虚偽の性的暴行疑惑を流布した経歴があり、2020年大統領選後には有権者向けの偽ロボコール事件で複数州から起訴され、2022年には有罪答弁もしている。IRIS C2の運営会社カルベクサ・グループは連邦契約企業として登録されているが、直接の政府契約は確認されていない</li>
<li>「攻撃用ゼロデイを売買する企業の運営者が、虚偽情報の前科者なのだ？」という点が今回の警戒点で、学歴や業界経験を問わず「生の才能」を持つ若手技術者を集める採用方針を公言している。攻撃的サイバー能力を扱う企業の実態確認が、発注元・応募者双方に求められる事例</li>
</ul>
<h2>LG、不正プロキシ化するスマートTVアプリを締め出しへ　対象アプリの42%超で確認</h2>
<ul>
<li>Krebs on Securityの報道によると、家電大手LGエレクトロニクスは2026年7月、自社のスマートTV向けアプリストア「webOS」で、テレビを常時稼働の「レジデンシャルプロキシ」ノードに変える機能を組み込んだアプリを締め出す方針を明らかにした</li>
<li>セキュリティ企業Spurの調査で、LGのwebOSストアで配布されるゲームなどのアプリの42%超に、第三者が利用者のインターネット接続を経由できるプロキシSDKが組み込まれていたことが判明。パックマン風の無料ゲームアプリでは、広告視聴かプロキシ提供かを選ばせる仕組みまで確認された。Samsung TizenOS向けアプリでも4分の1超で同様の仕組みが見つかっている</li>
<li>「無料アプリの裏でテレビが他人の通信の中継地点にされていたのだ？」という点が利用者への影響で、LGは開発者に機能除去を求め、応じないアプリは強制停止すると説明した。プロキシ提供業者Bright Dataは「利用者の同意に基づく」と反論しており、正当な利用と悪用の線引きが今後の焦点になる</li>
</ul>
<h2>格安ストリーミングスティック「H96」、広告詐欺ネットワークの踏み台に</h2>
<ul>
<li>Krebs on Securityの報道によると、セキュリティ企業Bitsightの研究者ペドロ・ファレ氏が、期限切れドメインを取得して通信内容を調べたところ、中国製の格安TVボックス「H96」数万台が、実際にはサムスンやシャオミなど有名スマホを装って偽装通信を送っていたことが判明した</li>
<li>これらの端末には、中国企業「浙江豊沃IoTテクノロジー」が開発した同一の2つのアプリが搭載されており、AIが自動生成したニュース記事風サイトへ広告詐欺クリックを送り込む仕組みが確認された。広告は、スマホになりすました端末からのアクセスにしか表示されない設計になっていた</li>
<li>「動画配信を見るためのスティックが、広告詐欺の踏み台になっていたのだ？」という点が消費者への警告で、Krebs on Securityはかねてから格安TVボックスがインターネット接続を無断で又貸しする危険性を指摘しており、今回は広告詐欺への悪用という新たな側面が確認された事例</li>
</ul>
<h2>Android向けマルウェア「ToxicPanda」、VPN権限を悪用しGoogle Playを機能停止</h2>
<ul>
<li>Bleeping Computerの報道によると、Android向け銀行系マルウェア「ToxicPanda」が新たな機能を獲得し、標的アプリを349種類、遠隔操作コマンドを167種類まで拡大させたことが判明した</li>
<li>新機能では、端末に付与させたVPN権限を悪用して通信を乗っ取り、Google Playストアへのアクセスをブロックする。これにより、被害者がセキュリティアプリを新たにインストールしたり、感染に気づいたアプリを更新したりする対抗策を封じる狙いがあるとみられる</li>
<li>「感染に気づいても対策アプリを入れられなくするのだ？」という点が今回の悪質さで、正規の権限要求（VPN許可）を悪用する手口は、利用者が許可画面で内容を確認する習慣の重要性を改めて示している</li>
</ul>
<h2>WordPressの脆弱性2件の組み合わせ「wp2shell」、CISAが悪用済みと認定</h2>
<ul>
<li>IPAによると、WordPress本体に見つかった脆弱性CVE-2026-60137とCVE-2026-63030を組み合わせることで、管理者権限を必要とせず標準構成のまま遠隔でコードを実行できる問題「wp2shell」が公表された。対象はWordPress 6.8系から7.0.1までで、WordPress.orgは影響を受けるバージョン向けに自動更新を強制発動している</li>
<li>米CISAは2026年7月21日、この脆弱性を実際に悪用が確認された「KEV（Known Exploited Vulnerabilities）」カタログに追加した。実証コードもすでに公開されており、今後悪用が広がる可能性がある</li>
<li>「自動更新が有効でも安心できないのだ？」という点が注意点で、自動更新の適用状況を必ず確認し、未更新のサイトは手動で最新版へ上げる必要がある。WordPressは世界のウェブサイトの多くで使われており、影響範囲が広い</li>
</ul>
<h2>Ruby on RailsのActive Storageに認証情報窃取・RCEの脆弱性「KindaRails2Shell」</h2>
<ul>
<li>JPCERT/CCは2026年7月30日、Ruby on RailsのファイルアップロードライブラリActive Storageに関するリモートコード実行の脆弱性（CVE-2026-66066、通称「KindaRails2Shell」）に関する注意喚起を公開し、8月3日に情報を更新した</li>
<li>この脆弱性が悪用されると、遠隔の第三者が細工したファイルをアップロードすることで、サーバー上のファイルや認証情報を読み取られ、リモートコード実行に至る可能性がある</li>
<li>「ファイルアップロード機能を悪用されるとサーバーごと乗っ取られかねないのだ？」という理解で正しい。Active StorageはRailsの標準機能として広く使われており、該当バージョンを使う開発チームは修正版への更新を優先度高く扱う必要がある</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>本日は「AIが脆弱性の発見・悪用双方を加速させている」構図（マイクロソフト570件更新、Copilot RCE）と、「無料・格安の消費者向け機器が知らぬ間に悪用の踏み台になる」構図（LGスマートTV、H96ストリーミングスティック）の2種類が目立った一日だった</li>
<li>個人にとっての教訓は、無料アプリや格安デバイスの裏側にある収益モデルを疑う姿勢、組織にとっての教訓は、自動更新任せにせずKEVカタログなど実際の悪用情報を確認しながらパッチ適用の優先順位を判断することの2点</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://krebsonsecurity.com/2026/07/microsoft-patches-a-record-570-security-flaws/">Microsoft Patches a Record 570 Security Flaws - Krebs on Security</a></li>
<li><a href="https://krebsonsecurity.com/2026/07/felons-fraudsters-flog-offensive-cybersecurity-startup/">Felons, Fraudsters Flog Offensive Cybersecurity Startup - Krebs on Security</a></li>
<li><a href="https://krebsonsecurity.com/2026/07/lg-to-ban-residential-proxies-from-smart-tv-apps/">LG to Ban Residential Proxies from Smart TV Apps - Krebs on Security</a></li>
<li><a href="https://krebsonsecurity.com/2026/07/read-this-before-you-buy-that-tv-streaming-stick/">Read This Before You Buy That TV Streaming Stick - Krebs on Security</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/toxicpanda-android-malware-uses-vpn-permissions-to-block-google-play/">ToxicPanda Android malware uses VPN permissions to block Google Play - Bleeping Computer</a></li>
<li><a href="https://www.ipa.go.jp/security/security-alert/2026/alert20260722.html">WordPressの脆弱性対策について(CVE-2026-60137、CVE-2026-63030：wp2shell) - IPA</a></li>
<li><a href="https://www.jpcert.or.jp/at/2026/at260021.html">注意喚起: Ruby on RailsのActive Storageにおけるリモートコード実行につながる脆弱性（CVE-2026-66066）に関する注意喚起 - JPCERT/CC</a></li>
</ul>

</details>

---

[← 2026-08-24 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
