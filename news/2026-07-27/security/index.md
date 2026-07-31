---
title: "重罪犯が運営するゼロデイ買い取りスタートアップからFBIのボットネット差し押さえまで！Steamゲーマー標的の採掘マルウェアも【2026/07/27】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# 重罪犯が運営するゼロデイ買い取りスタートアップからFBIのボットネット差し押さえまで！Steamゲーマー標的の採掘マルウェアも【2026/07/27】

**2026-07-27 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-07-27-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-07-27-security)

---

## 概要

今日のセキュリティニュース8本の前半4本は「摘発・詐欺・裏社会」の話。FBIが200万台規模のボットネットにつながる住宅用プロキシ「NetNut」を差し押さえた事件、重罪判決を受けた人物たちがゼロデイ脆弱性を1万ドルから700万ドルで買い取るスタートアップ「IRIS C2」を堂々と運営している実態、ShinyHuntersを騙るビットコイン2000ドルのセクストーション詐欺、Steamフォーラムの「修正方法」投稿でゲーマーが採掘マルウェアに感染する手口を、ずんだもんと四国めたんが解説します。後半4本は技術的な脆弱性と防御の話で、ランサムウェア集団Cl0pが製造業向けソフトPTC Windchill/FlexPLMを狙う脆弱性連鎖、ブラウザのメモリ上でマルウェアを組み立てる「SourTrade」広告キャンペーン、多くのパソコンに入っているOracle Javaの月例更新、GitHubとPyPIがサプライチェーン攻撃に導入した時間差の防御策を取り上げます。

▼ 今日のトピック
・FBIが住宅用プロキシ「NetNut」とPopaボットネットを差し押さえ
・重罪判決を受けた人物たちがゼロデイ買い取りスタートアップ「IRIS C2」を運営
・情報流出ブランドを騙るビットコイン2000ドルのセクストーション詐欺
・Steamフォーラムの「修正方法」を装った投稿でゲーマーが採掘マルウェアに感染
・ランサムウェア集団Cl0pが製造業向けソフトの脆弱性を連鎖させ二重恐喝
・ブラウザのメモリ上でマルウェアを組み立てる「SourTrade」広告キャンペーン
・多くのパソコンに入っているOracle Javaの月例更新
・GitHubとPyPIがソフトウェア部品を狙うサプライチェーン攻撃に「時間差」の防御を導入

▼ 参考記事・ソース
・Krebs on Security「FBI Seizes NetNut Proxy Platform, Popa Botnet」: https://krebsonsecurity.com/2026/07/fbi-seizes-netnut-proxy-platform-popa-botnet/
・Krebs on Security「Felons, Fraudsters Flog Offensive Cybersecurity Startup」: https://krebsonsecurity.com/2026/07/felons-fraudsters-flog-offensive-cybersecurity-startup/
・Bleeping Computer「ShinyHunters data leaks fuel $2,000 sextortion email scam」: https://www.bleepingcomputer.com/news/security/shinyhunters-data-leaks-fuel-2-000-sextortion-email-scam/
・Bleeping Computer「Steam forum ClickFix attacks infect gamers with XMRig cryptominers」: https://www.bleepingcomputer.com/news/security/steam-forum-clickfix-attacks-infect-gamers-with-xmrig-cryptominers/
・The Hacker News「Cl0p Affiliates Target Internet-Exposed PTC Windchill and FlexPLM with Unauthenticated RCE」: https://thehackernews.com/2026/07/cl0p-affiliates-target-internet-exposed.html
・Bleeping Computer「Malicious sites use JavaScript to build malware in browser memory」: https://www.bleepingcomputer.com/news/security/malicious-sites-use-javascript-to-build-malware-in-browser-memory/
・IPA「Oracle Java の脆弱性対策について(2026年7月)」: https://www.ipa.go.jp/security/security-alert/2026/0722-jre.html
・Bleeping Computer「GitHub, PyPI add time-based defenses against supply chain attacks」: https://www.bleepingcomputer.com/news/security/github-pypi-add-time-absed-defenses-against-supply-chain-attacks/

#NetNut #Popa #IRISC2 #ShinyHunters #Cl0p #SourTrade #セキュリティ #サイバーセキュリティ #ゆっくり解説 #ずんだもん #四国めたん

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>重罪犯が運営するゼロデイ買い取りスタートアップからFBIのボットネット差し押さえまで——Steamゲーマー標的の採掘マルウェアも（2026年7月27日）</h1>
<p><strong>キーワード:</strong> NetNut / Popa / IRIS C2 / ShinyHunters / Cl0p / Windchill</p>
<h2>オープニング：2026年7月27日 — セキュリティニュース</h2>
<p>今日は8本を取り上げる。前半は「摘発・詐欺・裏社会」の話で、FBIが200万台規模のボットネットにつながるプロキシサービスを差し押さえた事件、重罪判決を受けた人物たちがゼロデイ脆弱性を買い取るスタートアップを堂々と運営している実態、情報流出データを悪用したビットコイン恐喝メール、ゲーマーのフォーラムに紛れ込んだ採掘マルウェアと続く。後半は技術的な脆弱性と防御の話で、ランサムウェア集団が製造業のソフトウェアを狙う脆弱性連鎖、ブラウザのメモリ上でマルウェアを組み立てる新手口、多くのパソコンに入っているJavaの更新、そしてソフトウェア部品を汚染するサプライチェーン攻撃への新しい防御策を扱う。攻撃側もお金の流れも複雑になっているが、対策の基本は今日も変わらない。</p>
<h2>FBIが住宅用プロキシ「NetNut」とPopaボットネットを差し押さえ</h2>
<ul>
<li>FBIは2026年7月2日、住宅用プロキシ（一般家庭のネット回線を経由させて身元を隠す仕組み）サービス「NetNut」に関連する数百のドメインを差し押さえたと発表した。NetNutはナスダック上場のイスラエル企業「Alarum Technologies」が運営しており、同社の法務担当者は「調査に全面的に協力する」とコメントしている。</li>
<li>差し押さえの背景には、少なくとも200万台のデバイスが本人の同意なくマルウェアに感染させられていたとされる「Popa」ボットネットがある。スマートテレビやストリーミング機器にプロキシソフトが仕込まれ、持ち主が知らないうちに常時稼働の中継ノードにされ、大量スクレイピングや広告詐欺の踏み台に使われていた。</li>
<li>セキュリティ企業3社が6月19日にNetNutとPopaの関連を初めて報告し、その約2週間後にFBIの差し押さえが実施された。セキュリティ研究者は「NetNutは競合の『IPIDEA』が差し押さえられた後に人気が高まったサービスで、今回の措置はDDoS攻撃用ボットネットへの打撃も大きい」と評価している。</li>
</ul>
<h2>重罪判決を受けた人物たちがゼロデイ買い取りスタートアップ「IRIS C2」を運営</h2>
<ul>
<li>セキュリティ記者ブライアン・クレブス氏は、市販ソフトのゼロデイ脆弱性（修正前の未知の欠陥）を1万ドルから700万ドルで買い取ると謳うバージニア州の企業「IRIS C2」を運営しているのが、極右の陰謀論者かつ重罪判決歴のある人物2人だと報じた。買い取り額は対象・信頼性・運用価値に応じて変動するという。</li>
<li>運営者の1人ジェイコブ・ウォール氏と、法律事務所を率いるジャック・バークマン氏は、FBI元長官ロバート・ムラー氏らへの虚偽の性的暴行告発や、2020年米大統領選で郵便投票について嘘を広める大量の自動音声電話（ロボコール）を実施した過去がある。この選挙妨害でクリーブランドでは15件の重罪起訴を受け2025年に有罪判決、連邦通信委員会（FCC）からは当時最大級となる510万ドルの罰金も科されている。</li>
<li>こうした人物がゼロデイ脆弱性の買い取り市場に参入していること自体は珍しくないが、記者は「これほど公然と行う例はほとんどない」と指摘する。資金源、従業員の実在性、実際の政府契約の有無、買い取った脆弱性が悪用されないための管理体制など、不透明な点が多く残っている。</li>
</ul>
<h2>情報流出ブランドを騙るビットコイン2000ドルのセクストーション詐欺</h2>
<ul>
<li>大規模データ窃盗グループ「ShinyHunters」の名を騙り、実在の情報漏洩で流出したメールアドレス宛てに、48時間以内にビットコインで2000ドル相当を支払わなければ性的な動画を公開すると脅す「セクストーション（性的脅迫）」メールが確認された。宛先にはAmtrak、Hallmark、Substack、Betterment、CarGurus、ADT、Panera Breadなど複数の実在企業から漏れたアドレスが使われている。</li>
<li>メールは「数か月前からあなたの端末を監視しており、カメラ・マイク・キーボードにアクセスしていた」と主張するが、実際にはデバイスへの侵入は起きておらず、漏洩済みのメールアドレス一覧に機械的に送りつけているだけの手口である。Bleeping Computerが確認したところ、ShinyHunters自体はこのキャンペーンへの関与を否定しており、流出データを別の詐欺師が再利用したとみられる。</li>
<li>同様のメールが届いても、実際に端末が乗っ取られている証拠（具体的な画像・動画など）が添付されていない限り、支払いも返信もリンクのクリックもせず無視するのが最も安全な対応になる。心当たりのあるサービスから情報が漏れていないか確認する良い機会にもなる。</li>
</ul>
<h2>Steamフォーラムの「修正方法」を装った投稿でゲーマーが採掘マルウェアに感染</h2>
<ul>
<li>ゲーム配信プラットフォーム「Steam」の掲示板が、ゲームの不具合に悩むユーザーへの「解決策」を装う「ClickFix」攻撃に悪用されていることが確認された。ClickFixとは、正規の対処法のように見せかけてユーザー自身に悪意あるコマンドを実行させる社会工学的な手口を指す。</li>
<li>投稿では「msf utility PC Opt」という偽のWindows最適化ツールを名乗るPowerShellスクリプトの実行が勧められる。管理者権限で実行すると、ディスクチェックやドライバー更新を装った偽の進捗表示が出る裏で、「Advanced-Optimization」という関数が暗号資産の無断採掘マルウェア「XMRig」を静かにダウンロード・実行する仕組みになっている。</li>
<li>感染の兆候として、<code>C:\Windows\Background</code>フォルダーや「XMRig-（コンピューター名）」という名前のスケジュールされたタスクの有無を確認することが推奨されている。見つかった場合はこれらを削除したうえで、アンチウイルスソフトによる全体スキャンを行う必要がある。ゲームのトラブル解決を検索する際は、フォーラムの「解決済み」投稿でもPowerShellの実行を促す内容には注意したい。</li>
</ul>
<h2>ランサムウェア集団Cl0pが製造業向けソフトの脆弱性を連鎖させ二重恐喝</h2>
<ul>
<li>ランサムウェア集団「Cl0p」（Chubby Scorpius、FIN11などの別名でも知られる）に関連する攻撃者が、製品ライフサイクル管理ソフト「PTC Windchill」と「FlexPLM」のインターネット公開環境を狙い、データを盗んで暗号化と公開の両方で脅す「ダブルエクストーション（二重恐喝）」型の攻撃を行っていると報告された。</li>
<li>攻撃はまずFlexPLMの「WSDL」エンドポイントにある認証前の情報漏洩の欠陥を使って手がかりを得て、そこからWindchillのログイン処理にある脆弱性「CVE-2026-12569」（深刻度スコア9.3）につなげ、認証なしでコードを実行しJSP形式のウェブシェルを設置する。その後ファイルシステムを調べ上げ、設計・エンジニアリングデータを盗み出す。</li>
<li>被害は製造業、自動車、航空宇宙、小売業に及んでいる。今回の脆弱性は米国土安全保障省サイバーセキュリティ・インフラセキュリティ庁（CISA）の「悪用が確認された脆弱性」カタログにも登録済みで、該当システムをインターネットに公開しないこと、またはパッチの早期適用が推奨されている。</li>
</ul>
<h2>ブラウザのメモリ上でマルウェアを組み立てる「SourTrade」広告キャンペーン</h2>
<ul>
<li>広告セキュリティ企業Confiantは、2024年末から続く大規模な悪質広告キャンペーン「SourTrade」を分析し、暗号資産取引所「Solana」や「Luno」、株価分析サービス「TradingView」を装った偽ページで、閲覧者のブラウザ自体にマルウェアを組み立てさせる新手口を報告した。対象は12か国・25言語に及び、アジア太平洋地域とラテンアメリカが主な標的となっている。</li>
<li>仕組みはブラウザを「ローカルの組み立て工場」として悪用するもので、偽ページが「サービスワーカー」を登録し、バックグラウンドで動く「シェアードワーカー」がマルウェアの部品を組み立てるエンジンとして働く。セッションごとにパラメータをランダム化しながら、正規のプログラム実行環境「Bun」のクリーンな実行ファイルをもとに悪意あるプログラムを完成させる。</li>
<li>Confiantの研究者は「ネットワーク経由で完成したファイルそのものが送信されないため、通信内容を見張るタイプのセキュリティ対策では検出が難しい」と説明する。対策として、暗号資産関連サービスは必ず公式サイトから直接アクセスし、SNS上の広告からインストールしないことが呼びかけられている。</li>
</ul>
<h2>多くのパソコンに入っているOracle Javaの月例更新</h2>
<ul>
<li>IPA（情報処理推進機構）は7月22日、Oracleが公表したJavaの実行環境「Oracle Java SE」の月例セキュリティ更新について注意喚起した。悪用された場合、アプリケーションの異常終了や、パソコンを外部から操られてしまうといった深刻な被害につながる可能性があるとしている。</li>
<li>対象はJava SE 26.0.1、25.0.3、21.0.11、17.0.19、11.0.31、8 Update 491および8 Update 491-perfと、現在サポートされているほぼ全てのバージョン系列に及ぶ。Javaは業務システムから一般向けアプリまで幅広く組み込まれているため、自分が意識していないソフトの内部で使われている場合も多い。</li>
<li>IPAはOracle公式のJava Downloadsページから最新版へ更新するよう案内している。商用利用する組織は、更新にあたってライセンス条件の確認や有償サポートの検討も必要になる。個人利用の場合も、パソコンに入っているJavaのバージョンを一度確認しておく価値がある。</li>
</ul>
<h2>GitHubとPyPIがソフトウェア部品を狙うサプライチェーン攻撃に「時間差」の防御を導入</h2>
<ul>
<li>ソフトウェア開発の基盤である「GitHub」と、Python用ソフトウェア部品（パッケージ）の配布サイト「PyPI」が、悪意ある部品を紛れ込ませる「サプライチェーン攻撃」への対策として、新規公開直後の部品を一定期間扱わないようにする「時間差」の仕組みを導入した。</li>
<li>GitHub側は依存関係の自動更新ツール「Dependabot」に72時間（3日間）の「クールダウン期間」を設定し、公開されたばかりの新バージョンをすぐには取り込まないようにした。PyPI側はリリース公開から14日を過ぎると新しいファイルのアップロードをブロックする仕組みを導入している。ユーザー側で遅延期間を調整することも可能という。</li>
<li>記事では過去の主要被害として、人気パッケージ「chalk」や「debug」の乗っ取り、「s1ngularity」作戦、「Shai-Hulud」キャンペーン、「GhostAction」攻撃が挙げられており、合わせて数十億件規模のダウンロードに影響が及んだとされる。悪意ある部品の多くは公開から数分〜数時間で検出される実態を踏まえ、検出から実際の被害拡大までの猶予時間を稼ぐ狙いがある。</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>前半の4本——FBIによるNetNut/Popaボットネットの差し押さえ、重罪判決者が運営するゼロデイ買い取りスタートアップ、ShinyHuntersを騙るセクストーション詐欺、Steamのゲーマーを狙うClickFix採掘マルウェア——は、いずれも「誰が・どんなお金の流れで」攻撃や脅迫を成り立たせているかが見えてくる話だった。表向き合法な企業活動やゲームの相談投稿の裏に、犯罪の資金源や踏み台が隠れている。</li>
<li>後半の4本——Cl0pによる製造業ソフトの脆弱性連鎖、ブラウザ上でマルウェアを組み立てるSourTrade、Oracle Javaの月例更新、GitHub/PyPIの時間差防御——は、脆弱性の悪用スピードと、それに対抗する防御側の工夫の両方を示している。3日・14日という具体的な待ち時間を設けるだけでも被害の芽を摘める可能性がある点は覚えておきたい。</li>
<li>今日共通して言えるのは、「正規の見た目」を疑う視点の大切さだ。プロキシサービスも、脆弱性買い取り企業も、フォーラムの解決策も、公式サイトのように見えるページも、成り立ちや出どころを一歩踏み込んで確認する習慣が被害を防ぐ。</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li>Krebs on Security「FBI Seizes NetNut Proxy Platform, Popa Botnet」 https://krebsonsecurity.com/2026/07/fbi-seizes-netnut-proxy-platform-popa-botnet/</li>
<li>Krebs on Security「Felons, Fraudsters Flog Offensive Cybersecurity Startup」 https://krebsonsecurity.com/2026/07/felons-fraudsters-flog-offensive-cybersecurity-startup/</li>
<li>Bleeping Computer「ShinyHunters data leaks fuel $2,000 sextortion email scam」 https://www.bleepingcomputer.com/news/security/shinyhunters-data-leaks-fuel-2-000-sextortion-email-scam/</li>
<li>Bleeping Computer「Steam forum ClickFix attacks infect gamers with XMRig cryptominers」 https://www.bleepingcomputer.com/news/security/steam-forum-clickfix-attacks-infect-gamers-with-xmrig-cryptominers/</li>
<li>The Hacker News「Cl0p Affiliates Target Internet-Exposed PTC Windchill and FlexPLM with Unauthenticated RCE」 https://thehackernews.com/2026/07/cl0p-affiliates-target-internet-exposed.html</li>
<li>Bleeping Computer「Malicious sites use JavaScript to build malware in browser memory」 https://www.bleepingcomputer.com/news/security/malicious-sites-use-javascript-to-build-malware-in-browser-memory/</li>
<li>IPA「Oracle Java の脆弱性対策について(2026年7月)」 https://www.ipa.go.jp/security/security-alert/2026/0722-jre.html</li>
<li>Bleeping Computer「GitHub, PyPI add time-based defenses against supply chain attacks」 https://www.bleepingcomputer.com/news/security/github-pypi-add-time-absed-defenses-against-supply-chain-attacks/</li>
</ul>

</details>

---

[← 2026-07-27 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
