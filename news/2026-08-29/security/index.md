---
title: "セキュリティニュース 2026-08-29"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# セキュリティニュース 2026-08-29

**2026-08-29 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-29-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-29-security)

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年8月29日）</h1>
<p><strong>キーワード:</strong> Microsoft398件パッチ / ownCloud CVE-2023-49105 / Gitea CVE-2026-60004 / ServiceNow最大深刻度3件 / 悪性ブラウザ拡張19個 / Snowflake恐喝有罪答弁 / Metabaseゼロデイ</p>
<h2>オープニング：2026年8月29日 — セキュリティニュース</h2>
<ul>
<li>本日は、マイクロソフトが8月に修正した398件の脆弱性と実際に悪用中のゼロデイ、2023年に修正済みのownCloudの穴がフィリピンの原子力研究機関から核関連資料を盗むのに使われた件、コード管理ソフトGiteaで8000台超が未修正のまま暗号資産マイニングに悪用されている件、ServiceNowのAI基盤に見つかった認証不要の最大深刻度3件、暗号資産を盗む不正なChrome・Edge拡張機能19個、クラウド分析基盤Snowflakeを狙った大規模恐喝でカナダ人が有罪を認めた件、日本でも悪用が確認されているMetabaseのSQLインジェクションの7本を扱う。</li>
<li>通底するのは「修正が出ている、あるいはとっくに出ていた脆弱性が、更新の遅れによって現役の侵入経路になり続けている」という点。聞き終えたときに、自分の手元で後回しにしている更新はどれか、を考えられる構成にする。</li>
</ul>
<h2>マイクロソフト、8月に398件を修正 ソケットドライバのゼロデイが悪用中</h2>
<ul>
<li>マイクロソフトは2026年8月11日、自社製品の脆弱性398件を修正する月例更新を公開した。うち42件が「緊急」で、遠隔からほぼ操作なしにコンピュータを乗っ取られ得るものとされる。7月の記録的な570件、6月の約200件に続く多さで、同社はAIを使った脆弱性発見の加速が背景にあると説明している。</li>
<li>実際に攻撃で悪用が確認されているのは「CVE-2026-68820」1件。Windowsの通信処理を担うドライバ「afd.sys」の権限昇格の欠陥で、セキュリティ企業Automoxのランドン・マイルズ氏は「これは攻撃の2段目だ。まずフィッシングで低い権限の足場を作り、次にこのドライバの穴で管理者権限まで上がる」と指摘している。</li>
<li>未悪用だが公開済みの脆弱性として、Windowsユーザープロファイルサービスの権限昇格「CVE-2026-62832」なども含まれる。一方でAIによる修正には限界も報告されており、1Passwordの調査ではAIが生成したパッチが穴を塞げなかったり新たな穴を作ったりした割合が5割を超えた。SANSのエド・スカウディス氏は「一発でAIに直させようとせず、反復して試し、検証せよ」と述べている。</li>
</ul>
<h2>2023年修正のownCloudの穴、フィリピン原子力研究機関から核資料窃取に悪用</h2>
<ul>
<li>米CISA（サイバーセキュリティ・インフラ安全保障庁）は2026年8月27日、ファイル共有ソフト「ownCloud」の脆弱性「CVE-2023-49105」を、悪用が確認された脆弱性のカタログ（KEV）に追加した。深刻度スコアは9.8で、WebDAV APIの認証を回避してファイルの読み取り・改ざん・削除ができる。影響を受けるのはownCloud coreの10.6.0から10.13.0で、修正版10.13.1は2023年11月に公開されている。</li>
<li>CISAによると、中国語を使うとみられる攻撃者がこの穴を悪用し、フィリピンの原子力研究機関と、フィリピン海軍向けの造船会社を標的にした。攻撃者は約372MB・176ファイルを持ち出し、核物質の管理記録、2023〜2028年の戦略計画、研究炉の部品情報、過去の燃料在庫、職員の個人情報などが含まれていたとされる。勤怠システムの192MBのSQLデータベースや、BitLockerの復旧鍵・KeePassのパスワード管理ファイルといった認証情報も盗まれた。</li>
<li>米連邦政府機関には2026年8月30日までの修正が命じられた。3年近く前に修正版が出ている脆弱性が、更新されないまま重要施設への侵入に使われた形で、パッチ適用の遅れがそのまま国家安全保障の問題になっている。</li>
</ul>
<h2>コード管理ソフト「Gitea」、8300台超が未修正のまま実攻撃を受ける</h2>
<ul>
<li>セキュリティ監視団体Shadowserverによると、2026年8月27日時点でインターネットに露出したGiteaサーバーのうち約8393台が、実際に攻撃が続く脆弱性「CVE-2026-60004」に対して未修正のまま残っている。Giteaはソフト開発でソースコードを管理する自前設置型のサービスで、GitHubの小型版のような位置づけだ。</li>
<li>この脆弱性は差分適用用のAPIを悪用し、リポジトリに書き込み権限を持つ利用者が、GiteaのOS利用者の権限で任意のシェルコマンドを実行できるというもの。Giteaは初期設定で誰でも登録できるため、認証なしの攻撃者でもアカウントを作ってリポジトリを用意すれば悪用できる。修正版は2026年7月27日公開の1.27.1。発見はセールスフォースのシャイ・ロッド氏による。</li>
<li>現在確認されている攻撃では、未修正サーバーに暗号資産のマイニングマルウェアが送り込まれている。CISAはこの脆弱性もKEVに追加し、連邦機関に3日以内、つまり8月28日までの修正を命じた。修正版が出てから1か月経っても1万台近くが放置されている点に、更新運用の弱さが表れている。</li>
</ul>
<h2>ServiceNowのAI基盤に認証不要の最大深刻度3件</h2>
<ul>
<li>業務管理クラウド大手ServiceNowは2026年8月28日、同社のAI基盤に影響する深刻度が最大の脆弱性3件を修正した。「CVE-2026-18885」はコードインジェクションによる任意コード実行、「CVE-2026-18886」はコードインジェクションによる権限昇格、「CVE-2026-74820」はSQLインジェクションによるデータの窃取・改ざんにつながる。いずれも認証不要で、攻撃の難易度も低いとされる。</li>
<li>あわせて、基本的な権限を持つ攻撃者が遠隔でコードを実行し得るサンドボックス回避の脆弱性「CVE-2026-6876」も修正された。修正はXanadu、Yokohama、Zurichなど複数のバージョン系列で提供されている。ServiceNowはフォーチュン500級の大企業が多く使うため、影響範囲は広い。</li>
<li>ServiceNowは「現時点でServiceNow環境への悪用は確認していない」としている。ただし2年前には同社の脆弱性3件が連鎖的に悪用され実被害が出た経緯があり、自前設置型のインスタンスは直ちに修正するよう勧告されている。</li>
</ul>
<h2>暗号資産を盗むChrome・Edge拡張機能19個、8万人が導入</h2>
<ul>
<li>ソフトウェア供給網セキュリティ企業Socketは2026年8月、暗号資産の窃取機能を持つ不正なブラウザ拡張機能19個（Chrome18個、Edge1個）を発見したと公表した。「Superior」と名付けられたこの活動は2024年2月から続いており、19個の合計導入数は8万人を超える。</li>
<li>内訳は攻撃者が自作した14個と、既存の開発者から買い取った5個。買い取られた「右クリック・コピー解除＋OCR」拡張だけで8万件の導入があった。拡張は表向きは説明どおりに動きつつ、裏で攻撃者のサーバーに接続する二段構えで、暗号資産ウォレットの秘密鍵やハードウェアウォレットの復元フレーズの窃取、FacebookやLinkedInのアカウント乗っ取り、偽の更新画面を出す手口などを備える。</li>
<li>最大の危険は自動更新にある。Chromeの初期設定では拡張が自動で最新版に更新されるため、無害な状態で入れさせておき、後から悪性コードを配信できる。2年以上も検知されずに正規の拡張を買い集めていた点から、研究者は「極めて高い能力を持つ攻撃者」と評価している。導入済みの拡張は一度棚卸しし、不要なものは削除するのが現実的な対策になる。</li>
</ul>
<h2>クラウド分析基盤Snowflakeを狙った大規模恐喝、カナダ人が有罪を認める</h2>
<ul>
<li>2024年に「最も影響の大きいサイバー犯罪者の1人」と評されたカナダ・オンタリオ州キッチナー在住のコナー・ライリー・ムッカ被告（26）が、クラウド分析基盤Snowflakeを使う165以上の組織へ侵入し恐喝したなどの罪で有罪を認めた。コンピュータ詐欺、電信詐欺、重加重の個人情報窃盗、共謀の各罪で、量刑言い渡しは2026年10月27日、最低2年、最大30年の禁錮に直面する。</li>
<li>攻撃手法は高度なものではなく、多要素認証が設定されていないSnowflakeアカウントの、情報窃取マルウェアなどで盗んだログイン情報を使ってクラウド上のデータを抜き取るというものだった。標的にはAT&amp;Tの1億人超の通話・SMS記録、チケットマスター、レンディングツリー、ニーマン・マーカスなどが含まれ、恐喝で得た額は250万ドルを超える。</li>
<li>共犯者のうち米陸軍兵カメロン・ワゲニウス被告は2026年9月3日に量刑言い渡し、もう1人のジョン・エリン・ビンズ容疑者はトルコ国籍の保護で引き渡しを免れている。基本的な設定である多要素認証の欠如という穴が、通信大手を含む大規模流出に直結した事例だ。</li>
</ul>
<h2>Metabase「CVE-2026-72898」、日本でもゼロデイ悪用を確認</h2>
<ul>
<li>JPCERT/CCは、データ可視化ツール「Metabase」のSQLインジェクションの脆弱性「CVE-2026-72898」について、2026年8月6日の公表時点で既にゼロデイ攻撃が確認されていると注意喚起した。認証不要で、細工したリクエストにより内部データベースへ不正なSQLを実行され、Metabaseの管理者権限を奪われる恐れがある。</li>
<li>影響を受けるのは58.x系以降で、58.24、59.21、60.17、61.11、62.9、63.5より前のバージョン。58.xより前は影響を受けない。複数の組織が被害を公表しており、実証コードも出回っている。</li>
<li>すぐに更新できない場合の緩和策として、パスワード再設定用のエンドポイント「/api/session/reset_password」へのアクセスをネットワーク側で遮断することが挙げられている。侵害の痕跡は、このエンドポイントへのPOSTリクエスト（HTTP 400）の直後に現在ユーザー確認のGETリクエスト（HTTP 200）が続くパターン。侵害が疑われる場合はデータベースの認証情報を変更し、管理者アカウントを点検する必要がある。</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>今日の7本は、マイクロソフトの398件のように毎月出続ける修正、Giteaやownの穴のように修正版が出てもなお放置される脆弱性、ServiceNowやMetabaseのように認証不要で即侵入に使える弱点、拡張機能やSnowflakeのように利用者側の設定・運用の甘さを突く手口、と経路は違っても「更新と設定の遅れが侵入口になる」点で一致している。</li>
<li>組織にとって当面の要点は、CISAがKEVに載せたownCloudとGiteaのように悪用が確認された脆弱性を最優先で塞ぐこと、ServiceNowやMetabaseの認証不要の穴は公開即日で更新すること、Snowflakeの件が示すとおり多要素認証を全アカウントで徹底すること、そしてブラウザ拡張機能を定期的に棚卸しすることの4つになる。</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://krebsonsecurity.com/2026/08/microsoft-plugs-nearly-400-security-holes/">Krebs on Security: Microsoft Plugs Nearly 400 Security Holes</a></li>
<li><a href="https://thehackernews.com/2026/08/snowflake-github-actions-flaw-lets.html">The Hacker News: ownCloud Flaw Exploited to Steal Nuclear Records From Philippine Research Body</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/over-8-300-gitea-servers-vulnerable-to-code-execution-attacks/">BleepingComputer: Over 8,300 Gitea servers vulnerable to code execution attacks</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/servicenow-warns-of-three-max-severity-security-vulnerabilities/">BleepingComputer: ServiceNow warns of three max severity security vulnerabilities</a></li>
<li><a href="https://thehackernews.com/2026/08/19-chrome-and-edge-extensions-found.html">The Hacker News: 19 Chrome and Edge Extensions Found With Wallet-Stealing and Crypto-Draining Code</a></li>
<li><a href="https://krebsonsecurity.com/2026/08/canadian-man-pleads-guilty-in-snowflake-extortions/">Krebs on Security: Canadian Man Pleads Guilty in Snowflake Extortions</a></li>
<li><a href="https://www.jpcert.or.jp/at/2026/at260023.html">JPCERT/CC: MetabaseのSQLインジェクションの脆弱性（CVE-2026-72898）に関する注意喚起</a></li>
</ul>

</details>

---

[← 2026-08-29 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
