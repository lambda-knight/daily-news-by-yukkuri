---
title: "セキュリティニュース 2026-08-23"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# セキュリティニュース 2026-08-23

**2026-08-23 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-23-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-23-security)

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年8月23日）</h1>
<p><strong>キーワード:</strong> Entra ID誤報訂正 / NetScaler認証なしRCE / 車載Android詐欺網 / Defender純正ドライバ悪用 / TikTok400億円和解 / Snowflake恐喝有罪</p>
<h2>オープニング：2026年8月23日 — セキュリティニュース</h2>
<ul>
<li>本日はマイクロソフトのEntra ID脆弱性を巡る「悪用済み」表記の訂正騒動、NetScalerの認証なしリモートコード実行に発展しうる脆弱性、車載Android端末を狙う広告詐欺マルウェア、Windows Defenderの純正ドライバを悪用してセキュリティソフトを消す手口、TikTokの児童プライバシー訴訟400億円和解、Snowflake恐喝事件の実行役の有罪答弁、Microsoft Teamsを悪用した新型フィッシング、CISA自身の認証情報漏えいから得た教訓まで8本を取り上げる</li>
</ul>
<h2>マイクロソフトのEntra ID脆弱性、「悪用済み」表記が誤りだったと訂正</h2>
<ul>
<li>The Hacker Newsの報道によると、マイクロソフトが公開したセキュリティ情報で、法人向け認証基盤「Entra ID」の脆弱性（深刻度10.0、最高値）について、当初「Exploitability Assessment（悪用可能性評価）」欄が「悪用あり（Exploited: Yes）」と表示されていた</li>
<li>2026年8月21日、同社は取材を受けて表記を「悪用なし（Exploited: No）」に訂正し、「この脆弱性は悪用されていない」と説明を追加した</li>
<li>「深刻度は最高点なのに、悪用の有無の表示が途中で変わったのだ？」という点が今回の教訓で、脆弱性情報の一次発表であっても即座に鵜呑みにせず、修正・訂正の有無を追って確認する必要があることを示す事例。企業のセキュリティ担当者はパッチ適用の優先順位を、深刻度スコアと実際の悪用状況の両方で判断する必要がある</li>
</ul>
<h2>NetScaler ADC/Gatewayに認証なしリモートコード実行につながる脆弱性、watchTowrが詳細分析を公表</h2>
<ul>
<li>JPCERT/CCは2026年8月15日、Citrix NetScaler ADCおよびNetScaler Gatewayに関する注意喚起（JPCERT-AT-2026-0024）を公開した。セキュリティ企業watchTowr Labsが8月14日、この脆弱性（CVE-2026-8452）の詳細分析を公表したことを受けたもの</li>
<li>CVE-2026-8452は2026年6月30日に「サービス運用妨害（DoS）や不審な動作につながる脆弱性」として公表されていたが、watchTowrの分析により、NetScaler ADC・GatewayをSAMLのSP（サービスプロバイダ）またはIdP（認証基盤）として構成している場合、認証なしでリモートコード実行に至る可能性があることが判明した</li>
<li>「最初はDoSとしか説明されていなかったのだ？」という点が今回の核心で、公表当初は影響度が低く見えた脆弱性が、後の詳細分析でリモートコード実行にまで発展しうると判明した。SAML連携でNetScalerを使う組織はパッチ適用状況を再確認する必要がある</li>
</ul>
<h2>車載Android端末に広告詐欺マルウェア、内蔵アップデーターを悪用し感染拡大</h2>
<ul>
<li>The Hacker NewsとBleeping Computerの報道によると、セキュリティ企業Kaspersky（カスペルスキー）が2026年6月、Android搭載の車載ヘッドユニット（カーナビ・車載情報システム）向けファームウェアを開発するDoFun製の端末を狙う新しいマルウェアを発見した</li>
<li>このマルウェアは端末に標準搭載されているアップデート機能を通じて拡散し、多段階のダウンローダーを使って広告詐欺やプロキシボットネット（感染端末を中継役として悪用する仕組み）を構築する</li>
<li>「カーナビのアップデート機能が攻撃の入口になっているのだ？」という点が今回の特徴で、正規のソフトウェア更新の仕組みそのものが悪用されている。車のインフォテインメントシステムも、スマホやパソコンと同様にマルウェア感染の対象になり得ることを示す事例</li>
</ul>
<h2>Windows Defenderの純正ドライバが「武器化」、脆弱性なしでセキュリティソフトを削除可能に</h2>
<ul>
<li>The Hacker Newsの報道によると、セキュリティ企業Check Point Researchが、Windows Defenderに標準搭載されている正規の署名付きドライバ「BTR.sys（Boot Time Removal Tool）」を悪用し、Windows 7からWindows 11 25H2まで幅広いバージョンで、起動時にカーネルレベルのファイル・レジストリ操作を行う手法を公表した</li>
<li>この手法は既知の脆弱性を突くものではなく、外部から持ち込んだ不正なドライバも使わない。マイクロソフト純正の正規ドライバが本来持つ機能をそのまま悪用する点が特徴</li>
<li>「脆弱性ではなく正規の機能が悪用されているのだ？」という点が対策を難しくしている理由で、脆弱性のようにパッチ一つで塞げる問題ではない。セキュリティソフトの起動前後の動作を監視する仕組みの重要性が改めて浮き彫りになった</li>
</ul>
<h2>TikTok、児童プライバシー訴訟で400億円規模の和解に合意</h2>
<ul>
<li>The Hacker Newsの報道によると、米司法省は、ByteDance傘下のTikTokが2024年に提起された児童プライバシー法違反の訴訟について、4億ドル（日本円で約590億円相当）の支払いで和解することに合意したと発表した</li>
<li>和解金のうち3億ドルは即座に支払われ、残る1億ドルは、TikTokに対して以前出されていた同意判決（コンセントディクリー）を取り消す命令が確定した時点で支払われる</li>
<li>「和解金の支払いに条件が付いているのだ？」という点が今回の構造で、単純な罰金ではなく、過去の法的措置の扱いと支払いが連動している。未成年者のデータ収集を巡る規制強化の流れの中で、プラットフォーム企業への追及が続いていることを示す事例</li>
</ul>
<h2>Snowflake恐喝事件、実行役のカナダ人男性が有罪を認める　AT&amp;T顧客1億人超のデータも窃取</h2>
<ul>
<li>Krebs on Securityの報道によると、2024年に「最も影響の大きいサイバー犯罪者の一人」と評されたカナダ・オンタリオ州キッチナー在住の26歳男性コナー・ライリー・モウカ被告が、クラウドデータ保管サービスSnowflakeを利用していた165組織超への不正アクセス・恐喝の共謀・コンピュータ詐欺の罪を認めた</li>
<li>同被告は、AT&amp;Tの顧客1億人超の通話・テキストメッセージの履歴記録を盗み出したことも認めている</li>
<li>「一人の実行役が165組織以上を狙えてしまったのだ？」という点が今回の教訓で、クラウドサービス側の多要素認証未設定など基本的な設定不備が、大規模被害につながった事例として記録される。有罪答弁により今後は量刑が焦点になる</li>
</ul>
<h2>Microsoft Teamsを悪用した新型フィッシング「SynkLoader」、偽ロック画面で認証情報を窃取</h2>
<ul>
<li>Bleeping Computerの報道によると、これまで確認されていなかったマルウェア「SynkLoader」が、Microsoft Teamsを使ったフィッシングキャンペーンで配布されていることが判明した</li>
<li>攻撃者は偽の画面ロック（ロック画面）を表示させ、被害者がパスワードを入力する動作を誘導することで認証情報を窃取する仕組みになっている</li>
<li>「見慣れたロック画面のふりをして騙すのだ？」という点が今回の手口で、業務でTeamsを日常的に使う環境ほど、届いたメッセージやリンクを反射的に信じてしまいやすい。心当たりのないリンクからのログイン画面には注意が必要</li>
</ul>
<h2>CISA自身の認証情報漏えい、半年間気づかれなかった経緯から得た教訓</h2>
<ul>
<li>Krebs on Securityの報道によると、米サイバーセキュリティ・インフラセキュリティ庁（CISA）は、委託先の契約企業がAWS GovCloudの鍵を含む複数の内部認証情報を、公開状態のGitHubリポジトリに約半年間放置していた事案について、事後検証（ポストモーテム）を公表した</li>
<li>この漏えいは、Krebs on Securityからの通知によって初めて明らかになったもので、CISAの初動対応にあった課題を専門家が分析している</li>
<li>「防御を担う機関自身の情報が半年も気づかれなかったのだ？」という点が今回の教訓で、政府機関であっても委託先の管理体制次第で長期間の漏えいが起こり得る。すべてのセキュリティチームが自組織の外部委託先の管理体制を点検すべき事例として位置づけられている</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>本日は「正規の仕組み・機能がそのまま悪用される」パターン（Defenderドライバ、車載アップデーター、NetScalerのSAML連携）と、「公表内容が後から訂正・詳細化される」パターン（Entra ID、NetScaler）が目立った一日だった</li>
<li>個人・組織の両方に共通する教訓は、脆弱性情報や悪用状況の一次発表を鵜呑みにせず、訂正や続報を追い続けることと、委託先を含めた認証情報の管理体制を定期的に点検することの2点</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://thehackernews.com/2026/08/microsoft-entra-id-flaw-cvss-100.html">Microsoft Patches Severe Entra ID Flaw (CVSS 10.0) Allowing Remote Code Execution - The Hacker News</a></li>
<li><a href="https://www.jpcert.or.jp/at/2026/at260024.html">注意喚起: NetScaler ADCおよびNetScaler Gatewayにおけるリモートコード実行につながる脆弱性（CVE-2026-8452）に関する注意喚起 - JPCERT/CC</a></li>
<li><a href="https://thehackernews.com/2026/08/android-car-malware-spreads-through.html">Android Car Malware Spreads Through Built-In Updaters for Ad Fraud, Proxy Botnet - The Hacker News</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/hackers-infect-android-car-head-units-with-proxy-botnet-malware/">Hackers infect Android car head units with proxy botnet malware - Bleeping Computer</a></li>
<li><a href="https://thehackernews.com/2026/08/microsoft-defenders-own-driver-can-be.html">Microsoft Defender's Own Driver Can Be Weaponized to Delete Security Software at Boot - The Hacker News</a></li>
<li><a href="https://thehackernews.com/2026/08/tiktok-agrees-to-400-million-settlement.html">TikTok Agrees to $400 Million Settlement in U.S. Child Privacy Lawsuit - The Hacker News</a></li>
<li><a href="https://krebsonsecurity.com/2026/08/canadian-man-pleads-guilty-in-snowflake-extortions/">Canadian Man Pleads Guilty in Snowflake Extortions - Krebs on Security</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/new-synkloader-malware-pushed-in-microsoft-teams-phishing-campaign/">New SynkLoader malware pushed in Microsoft Teams phishing campaign - Bleeping Computer</a></li>
<li><a href="https://krebsonsecurity.com/2026/07/lessons-learned-from-cisas-recent-github-leak/">Lessons Learned from CISA's Recent GitHub Leak - Krebs on Security</a></li>
</ul>

</details>

---

[← 2026-08-23 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
