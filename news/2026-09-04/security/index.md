---
title: "裁判所の封印記録も流出？供給網攻撃と重大脆弱性7選【2026/09/04】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# 裁判所の封印記録も流出？供給網攻撃と重大脆弱性7選【2026/09/04】

**2026-09-04 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-09-04-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-09-04-security)

---

## 概要

裁判所バックアップ侵害、供給網攻撃の容疑者逮捕、シスコとHPEの重大脆弱性、開発環境乗っ取りなど7件を対策まで解説します。

▼ 今日のトピック
・米裁判所システム侵害と社会保障番号流出の恐れ
・供給網攻撃シャイフルードの容疑者2人を逮捕
・シスコ・ネクサス9000とIOS XRの重大欠陥
・クラウド開発環境コーダーのレジストリ乗っ取り
・セルビア学生運動メンバーへのペガサス感染
・HPEアルーバOSの重大バッファオーバーフロー
・46カ国601件へ広がった遠隔管理ソフト誘導型フィッシング

▼ 参考記事・ソース
・The Hacker News「裁判所ソフト侵害」 https://thehackernews.com/2026/09/thomson-reuters-court-software-breach.html
・Krebs on Security「TeamPCP容疑者を逮捕」 https://krebsonsecurity.com/2026/08/two-alleged-teampcp-hackers-arrested-in-australia/
・The Hacker News「Cisco Nexus 9000の重大欠陥」 https://thehackernews.com/2026/09/critical-cisco-nexus-9000-flaw-lets.html
・BleepingComputer「Coderレジストリ侵害」 https://www.bleepingcomputer.com/news/security/coders-registry-infrastructure-compromised-to-push-malicious-modules/
・The Hacker News「Pegasusゼロクリック感染」 https://thehackernews.com/2026/09/pegasus-zero-click-spyware-exploit.html
・BleepingComputer「HPE ArubaOS-CXの欠陥」 https://www.bleepingcomputer.com/news/security/hpe-patches-critical-arubaos-cx-remote-code-execution-flaw/
・The Hacker News「46カ国に広がるRMMフィッシング」 https://thehackernews.com/2026/09/us-becomes-top-target-in-rmm-phishing.html

#サイバーセキュリティ #情報漏洩 #脆弱性 #フィッシング #ゆっくり解説 #ずんだもん

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年9月4日）</h1>
<p><strong>キーワード:</strong> 米国裁判所システム侵害 / TeamPCP逮捕 / Cisco Nexus 9000重大欠陥 / Coderレジストリ改ざん / Pegasusセルビア学生 / HPE ArubaOS-CX / RMMフィッシング46カ国</p>
<h2>オープニング：2026年9月4日 — セキュリティニュース</h2>
<ul>
<li>本日は7本。トムソン・ロイター傘下の裁判所システム「C-Track」から社会保障番号や封印記録まで流出した侵害、供給網攻撃「Shai-Hulud」を主導したとされるTeamPCPの2容疑者がオーストラリアで逮捕された件、Cisco Nexus 9000スイッチとIOS XRの重大脆弱性、クラウド開発環境「Coder」のレジストリがCloudflareの経路ごと乗っ取られ資格情報窃取ツールを配布した件、セルビアの学生運動メンバーのiPhoneがPegasusスパイウェアに感染した件、HPEのネットワークOS「ArubaOS-CX」の認証不要バッファオーバーフロー、そしてカナダ発と見られていたRMMフィッシングが46カ国に広がっていた件を扱う。</li>
<li>共通するのは「本来は守り役のはずの基盤が突破口になった」点だ。裁判所のバックアップ、開発環境のレジストリ、通信キャリアのメッセージ経路、ネットワーク機器そのものが攻撃の通り道になっている。聞き終えたときに、自分や職場が信頼している基盤のどこを点検すべきか考えられる構成にする。</li>
</ul>
<h2>米裁判所システム「C-Track」侵害、社会保障番号や封印記録も流出の恐れ</h2>
<ul>
<li>トムソン・ロイター傘下ウェスト・パブリッシングは2026年9月2日、裁判所向けケース管理プラットフォーム「C-Track」のバックアップデータに第三者が不正アクセスしたと公表した。侵害は2026年3月1日から6月29日の間に起きており、発見は6月30日。北米で今も刑事捜査が続いている。</li>
<li>影響を受けたのはアラバマ、ケンタッキー、モンタナ、ネバダ、ニューハンプシャー、ノースダコタ、オハイオ（10地区）、ペンシルベニア（4機関）、サウスカロライナ、テネシー、ワイオミングの各州裁判所と米領バージン諸島、カナダ・オンタリオ州の裁判所を含む計24の裁判所機関。流出した恐れがあるのは氏名、社会保障番号、運転免許証番号、生年月日、医療情報、健康保険情報、事件番号、当事者の住所・電話番号、起訴・審理内容に加え、非公開扱いの封印記録も含まれる。</li>
<li>会社側は「現時点で不正利用や詐欺の証拠は確認していない」としつつ、米国ではエクスペリアン、カナダではトランスユニオンによる12カ月分の信用監視を提供し、専用ダイヤル（1-833-918-5294）を設けた。裁判所が扱う社会保障番号や封印記録は本来もっとも厳重に守られるべき情報であり、バックアップ基盤という「表に出にくい保管場所」が破られた点が今回の核心になる。</li>
</ul>
<h2>供給網攻撃「Shai-Hulud」の主導格、TeamPCPの2容疑者をオーストラリアで逮捕</h2>
<ul>
<li>オーストラリア連邦警察（AFP）は、史上最長規模とされるソフトウェア供給網攻撃を続けてきた集団「TeamPCP」の関与を疑われる西オーストラリア州の男性2人を逮捕したと発表した。主要容疑者はコテスロー在住のルーベン・イアン・トムソン容疑者（23）で保釈は却下され、共犯とされるマイケル・ゲーブラー容疑者（23）も身柄を拘束された。両容疑者は9月18日にパース治安判事裁判所に出廷し、あわせて14件のサイバー犯罪容疑に問われる。</li>
<li>TeamPCPは固定的な組織ではなく「個々に技能を持つ者の緩やかな共同体」で、Matrixのチャットサーバー「Cybercats」を介してFulcrumsecやxpl0itrsなど他の犯罪グループと連携していた。開発者環境を狙う自己増殖型ワーム「Shai-Hulud」を中心に、オープンソースツール数百点への不正コード混入、3月のLiteLLM侵害では2500超の組織のクラウド認証情報を窃取、5月にはGitHubで3800以上のリポジトリを侵害したと主張していた。影響先にはノボノルディスク、データブローカーのレクシスネクシス、BMW・アウディ・ホンダ・メルセデスベンツ・ボルボ・トヨタなど自動車大手も含まれる。</li>
<li>トムソン容疑者はTeamPCPの活動全体で得た報酬を約2万ドルと供述し、反省の弁はないものの覚醒剤や幻覚剤への依存を認めている。捜査は複数のサイバー犯罪フォーラムやメールアドレス、HackerOne上の旧ハンドル名「Deadcatx3」など断片的なデジタルの痕跡をつなぎ合わせて本人特定に至った。セキュリティ研究者チャーリー・エリクセン氏は「大規模言語モデルが攻撃者の知識不足を補い、運用面で杜撰な人物でも大きな被害を出せるようになっている」と指摘した。高度な技術と杜撰なOPSEC（運用上の秘匿対策）が同居する典型例で、逮捕は供給網攻撃の抑止力になり得るが、Shai-Huludの活動自体が終息したとは限らない。</li>
</ul>
<h2>Cisco Nexus 9000に致命的欠陥、IOS XR全111リリースにも波及</h2>
<ul>
<li>シスコは2026年9月2日、Nexus 9000シリーズスイッチにCVSS9.8の脆弱性「CVE-2026-20212」を公表した。TCPポート43210と43211が制限なしにIPアドレスへ紐付いており、既定のレイヤー3 VRFインスタンス経由で到達できる。細工したデータを送ると認証なしでroot権限のコードが実行され、S1HALプロセスの停止やデバイス自体の再起動も引き起こせる。対象は10.3(1)から10.6(3s)までの45リリースにまたがり、N9K-C9804やN9K-C9808を含む10機種が影響を受ける。</li>
<li>同日、IOS XR向けにも7件のCVEをまとめた「アンブレラ」修正がまとめて公開された。うち2件はCVSS9.8で、メモリ安全性に関わる「CVE-2026-20274」と認証欠落を含むアクセス制御の欠陥「CVE-2026-20275」。残り5件もCVSS8.2から8.8にのぼる。IOS XRは設定内容に関わらず全111リリースが対象となる規模の大きさが特徴だ。</li>
<li>パッチ状況は複雑で、即座に適用できる完全な修正版はまだなく、14リリースでのみSMU（ソフトウェア保守更新）が利用可能、4リリースは準備中、残る93リリースはアップグレード後に別途SMUを当てる必要がある。SMUが不要になる次期リリースは26.2.2と26.3.1が予定されている。管理者はまず自分の使うリリースがどの段階にあるかを確認し、暫定策としてポート43210・43211への到達をファイアウォールで遮断するなど、パッチ待ちの間の防御を先に固める必要がある。</li>
</ul>
<h2>クラウド開発環境「Coder」のレジストリがCloudflare経由で乗っ取られる</h2>
<ul>
<li>開発者向けセキュアクラウド開発環境を提供するCoder社は、自社レジストリ「registry.coder.com」がある種の経路乗っ取りを受け、悪意あるTerraformモジュールを配布されたと明らかにした。同社の顧客にはドロップボックス、パランティア、スクエア、メルセデス・ベンツ、KKR、EnBW、米政府機関、防衛関連企業が含まれる。</li>
<li>攻撃者はCoderのCloudflareインフラへ不正にアクセスし、レジストリのプールへ未許可のIPアドレスを追加した。この結果、一部利用者のリクエストがCloudflareによって攻撃者のサーバーへ誤って中継され、悪意あるファイルが配信された。配布されたモジュールは情報窃取ツールとして機能し、プロビジョナー環境変数、クラウド・AIツーリングのAPIキー、CI/CD認証情報、設定ファイルのシークレット、端末履歴、ユーザーのOIDCトークン、SSH鍵、認証トークン、Coderデータベースのパスワードまで探索し、集めた情報を「coder-infra[.]com」へ送信していた。</li>
<li>悪意あるファイルが配信されたのは2026年8月31日07時35分から21時45分（協定世界時）の間。Coderはバージョン2.37.0、2.36.4、2.35.7、2.34.9への更新を呼びかけ、利用者にはファイアウォールやDNSのログでcoder-infra[.]comへの通信履歴がないか確認するよう求めている。開発環境そのものを配るインフラが、CDNの経路操作という一段外側の攻撃で汚された点が今回の教訓になる。</li>
</ul>
<h2>セルビア学生運動メンバーのiPhoneにPegasusスパイウェア、iMessageゼロクリックで感染</h2>
<ul>
<li>カナダのCitizen LabはSHARE Foundationと共同で、セルビアの学生抗議運動メンバーが所有するiPhoneがNSOグループのPegasusスパイウェアに感染していたと報告した。分析の結果「iMessageのゼロクリック悪用を用いた感染を確認した」とし、2025年12月から2026年1月にかけて高い確度を示す感染の痕跡が見つかった。悪用されたのはアップルが2025年4月リリースのiOS18.4.1で修正済みの欠陥とみられる。</li>
<li>SHARE Foundationによると、2026年年初以降セルビア国内で少なくとも14人が高度なスパイウェアの標的になっており、対象は学生運動メンバーのほか活動家、野党議員、地方議員にまで及ぶ。感染が確認された時期は同国の3月29日の地方選挙と重なる。別の学生運動メンバーは警察の取り調べ中に端末を押収された後、新型のAndroid向けスパイウェア「NoviSpy」に感染していたことも判明した。</li>
<li>アムネスティ・インターナショナルのセキュリティラボ責任者ドンチャ・オ・キアーバル氏は「セルビア当局による、拘束中の侵襲的なAndroidスパイウェア展開が続いている」と述べ、新型スパイウェアは検知回避を狙って新規に構築されたものだと指摘した。別の端末からも同じ系統のスパイウェアが検出されたほか、被害者間の私信アプリViberでのやり取りが親政権系メディア「Informer TV」で公開される事態も起きている。ゼロクリック攻撃は利用者の操作なしで成立するため、OSを最新版に保つことだけが唯一の直接的な防御線になる。</li>
</ul>
<h2>HPE製ネットワークOS「ArubaOS-CX」に認証不要の重大バッファオーバーフロー</h2>
<ul>
<li>ヒューレット・パッカード・エンタープライズ（HPE）は、企業向けスイッチで使われるネットワークOS「ArubaOS-CX」に「Critical」評価の脆弱性「CVE-2026-73749」を含む修正をリリースした。認証を経ていない遠隔の攻撃者が特別に細工したパケットを脆弱なデーモンプロセスへ送るだけで、通常より高い権限でコードを実行できるバッファオーバーフローの欠陥だ。</li>
<li>影響を受けるのはバージョン10.18.0001以前、10.17.1021以前、10.16.1051以前、10.13.1180以前、10.10.1180以前で、それぞれ10.18.1002以上、10.17.1030以上、10.16.1060以上、10.13.1190以上、10.10.1181以上への更新で修正される。同時に、CVE-2026-73750からCVE-2026-73782まで10件以上の追加脆弱性も公表されており、認証要件や攻撃条件はそれぞれ異なる。</li>
<li>公表時点で悪用や実証コードの公開は確認されていないが、認証不要でパケットを送るだけという攻撃条件の低さは、境界に置かれるスイッチ機器では特に危険だ。管理者は自社の稼働バージョンを確認し、優先度を上げて修正版へ移行するとともに、管理インターフェースを不要な外部公開から切り離す対応をあわせて検討したい。</li>
</ul>
<h2>カナダの税金フォームを装ったRMMフィッシング、実は46カ国601件に拡大</h2>
<ul>
<li>ANY.RUNの研究チームは、当初カナダ歳入庁（CRA）の税務フォームを装ったフィッシングとして報告されていた攻撃が、実際には46カ国にまたがる広範なキャンペーンの一部だったと明らかにした。確認された事案は601件に及び、地理的な標的として米国が全体の約45%を占めて最大となり、教育、技術、政府機関が主な対象業種だった。</li>
<li>手口はCRA税務フォームに加え、UPSの配送通知、Adobeファイル共有、税務通知、米社会保障局を装った文書、請求書など複数の偽装文書を使い分け、被害者を誘導して正規のリモート監視・管理（RMM）ソフトウェアをインストールさせるというもの。一度RMMを入れさせれば、遠隔操作ツールとして正規に扱われるため検知を避けやすい。</li>
<li>研究チームはインフラの急速な使い捨てぶりも確認しており、425件のフィッシングキットURL・240件のホストのうち94%が観測されたのはわずか1日だけだった。ホスティングにはVercel、GitHub Pages、Netlify、Amazon S3など正規のクラウドサービスが多用されている。一方で共通の画像リソースや「secure.html」からZIPファイルへ誘導する配信構造など、日々変わるドメインを越えて使い回されている部品を手がかりに、研究チームは日単位で切り替わる攻撃群を一つのキャンペーンとして関連付けることに成功した。正規サービスを土台にした使い捨てインフラは、ドメイン名や新しさだけで安全を判断できないことを改めて示している。</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>7件の舞台は、裁判所のバックアップ、供給網ワームの捜査、ネットワーク機器の設定不備、開発環境のCDN経路、スマートフォンのメッセージアプリ、企業向けスイッチ、そしてRMMソフトの信頼と、それぞれ異なる。しかし共通しているのは「本来は守りの側にあるはずの基盤」が突破口になった点だ。</li>
<li>個人にできることは、iPhoneやAndroidを常に最新OSへ保つこと、見知らぬ添付ファイルやリンクからソフトを入れないことに尽きる。開発者や管理者は、CDN経由の配信元検証、CoderやCisco・HPE製品のバージョン確認と更新、RMMソフトの導入経路の見直しを優先したい。</li>
<li>TeamPCPの逮捕は供給網攻撃への一つの区切りだが、Shai-Hulud型の手口自体が消えたわけではない。裁判所システムのように「バックアップだから安全」と思われがちな場所ほど、実際には点検が手薄になりやすいという教訓を持ち帰りたい。</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://thehackernews.com/2026/09/thomson-reuters-court-software-breach.html">The Hacker News: Thomson Reuters Court Software Breach May Have Exposed SSNs and Sealed Data</a></li>
<li><a href="https://krebsonsecurity.com/2026/08/two-alleged-teampcp-hackers-arrested-in-australia/">Krebs on Security: Two Alleged 'TeamPCP' Hackers Arrested in Australia</a></li>
<li><a href="https://thehackernews.com/2026/09/critical-cisco-nexus-9000-flaw-lets.html">The Hacker News: Critical Cisco Nexus 9000 Flaw Lets Unauthenticated Remote Attackers Run Code as Root</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/coders-registry-infrastructure-compromised-to-push-malicious-modules/">BleepingComputer: Coder's registry infrastructure compromised to push malicious modules</a></li>
<li><a href="https://thehackernews.com/2026/09/pegasus-zero-click-spyware-exploit.html">The Hacker News: Pegasus Zero-Click Spyware Exploit Infects Serbian Student Movement Member's iPhone</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/hpe-patches-critical-arubaos-cx-remote-code-execution-flaw/">BleepingComputer: HPE patches critical ArubaOS-CX remote code execution flaw</a></li>
<li><a href="https://thehackernews.com/2026/09/us-becomes-top-target-in-rmm-phishing.html">The Hacker News: US Becomes Top Target in RMM Phishing Campaign Spanning 46 Countries</a></li>
</ul>

</details>

---

[← 2026-09-04 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
