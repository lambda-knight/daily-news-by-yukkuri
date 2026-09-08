---
title: "Magentoゼロデイに緊急パッチ、MFA突破258組織【セキュリティ 2026/09/08】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# Magentoゼロデイに緊急パッチ、MFA突破258組織【セキュリティ 2026/09/08】

**2026-09-08 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-09-08-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-09-08-security)

---

## 概要

Magento StyleSmugglerの緊急パッチ、フィッシング代行BigBear2.0のMFA突破、Metabase経由のMathspace108万人流出、航空旅客2億2000万件露出、FreeIPAの認証なし管理者権限、GoogleのAI攻撃フレームワーク報告など8件を対策まで解説します。

▼ 今日のトピック
・Magento・Adobe Commerceゼロデイ「StyleSmuggler」に9月8日パッチ（CVE-2026-75650、CVSS10.0）
・フィッシング代行「BigBear 2.0」が多要素認証を突破、258組織で5137件の認証情報
・学習アプリMathspace、Metabaseの欠陥で108万人分流出（ShinyHunters疑い）
・航空旅客2億2000万件超、ベトナム関連の事前旅客情報データベースが露出
・FreeIPAに認証不要で管理者権限を奪う脆弱性連鎖（CVE-2026-76578、CVSS9.8）
・Google、生成AIを組み込んだ攻撃自動化フレームワーク「Recon」を報告
・Bing検索汚染「BengalSEO」がMayaBotとサポート詐欺へ誘導
・Grindr、HIV状態の広告目的共有をめぐり英国で2600万ポンドの和解

▼ 参考記事・ソース
・The Hacker News「Adobe Patches Magento Zero-Day」 https://thehackernews.com/2026/09/adobe-patches-magento-zero-day.html
・Bleeping Computer「BigBear Microsoft 365 phishing service bypassed MFA at 258 organizations」 https://www.bleepingcomputer.com/news/security/bigbear-microsoft-365-phishing-service-bypassed-mfa-at-258-organizations/
・Bleeping Computer「Mathspace discloses data breach affecting over 1 million people」 https://www.bleepingcomputer.com/news/security/mathspace-discloses-data-breach-affecting-over-1-million-people/
・Bleeping Computer「220 million traveler records exposed in Vietnam-linked APIS leak」 https://www.bleepingcomputer.com/news/security/220-million-traveler-records-exposed-in-vietnam-linked-apis-leak/
・The Hacker News「FreeIPA Flaw Chain Lets Anonymous Clients Create Reusable Administrator Credentials」 https://thehackernews.com/2026/09/freeipa-flaw-chain-lets-anonymous.html
・Bleeping Computer「Hackers build AI frameworks for widescale credential theft」 https://www.bleepingcomputer.com/news/security/hackers-build-ai-frameworks-for-widescale-credential-theft/
・The Hacker News「BengalSEO Poisons Bing Search Results」 https://thehackernews.com/2026/09/bengalseo-poisons-bing-search-results.html
・The Hacker News「Grindr to Pay £26 Million to Settle U.K. Claims Over HIV Status Data Sharing」 https://thehackernews.com/2026/09/grindr-to-pay-26-million-to-settle-uk.html

#セキュリティ #脆弱性 #フィッシング #多要素認証 #ずんだもん

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年9月8日）</h1>
<p><strong>キーワード:</strong> StyleSmugglerパッチ CVE-2026-75650 / BigBear2.0 MFA突破 258組織 / Mathspace Metabase流出108万人 / ベトナムAPIS 2億2000万件露出 / FreeIPA認証不要CVSS9.8 / Google Recon攻撃フレームワーク / TeamPCP豪州逮捕 / Grindr HIV情報和解</p>
<h2>オープニング：2026年9月8日 — セキュリティニュース</h2>
<ul>
<li>本日は8本。まず9月7日に「未修正」として伝えた通販ソフトMagento・Adobe Commerceのゼロデイ「StyleSmuggler」に、Adobeが9月8日付で緊急パッチを出した続報。次にフィッシング代行サービス「BigBear 2.0」が多要素認証を突破して258組織を侵害した件、学習アプリMathspaceが集計ソフトMetabaseの欠陥を突かれ108万人分の個人情報を流出させた件、ベトナムに関連するとみられる航空旅客情報データベースから2億2000万件超が露出していた件を扱う。</li>
<li>後半は、Linuxの認証基盤FreeIPAで認証なしに管理者権限を奪える脆弱性連鎖（CVSS9.8）、Googleが公表した生成AIを組み込んだ攻撃自動化フレームワーク「Recon」、Bingの検索結果を汚染してマルウェア「MayaBot」やサポート詐欺へ誘導する長期キャンペーン「BengalSEO」、出会い系アプリGrindrがHIV状態の広告目的共有をめぐり英国で2600万ポンドの和解に応じた件を取り上げる。</li>
<li>今日の軸は二つ。「盗んだ認証情報とセッションを使う攻撃が、AIとサービス化で量産段階に入った」こと、そして「Metabaseのように内部向けの集計ツールが、外向けの侵入口になっている」ことだ。</li>
</ul>
<h2>Magento・Adobe Commerceの緊急ゼロデイ「StyleSmuggler」、9月8日に修正パッチ</h2>
<ul>
<li>Adobeは2026年9月8日、通販サイト構築ソフトAdobe CommerceとMagento Open Sourceの最大深刻度の脆弱性「StyleSmuggler」（CVE-2026-75650、CVSSスコア10.0）に対する修正パッチを公開した。9月7日の回では、オランダのEC専門企業Sansecが「未修正のまま攻撃が始まっている」と警告した段階を伝えたが、今回その正式パッチが出た形だ。</li>
<li>影響範囲はAdobe Commerceの2.4.4から2.4.9、Magento Open Sourceの2.4.6から2.4.9で、2026年8月以前のリリースが対象になる。攻撃は9月4日22時20分（協定世界時）に最初の悪用が確認され、その約50分後にはEC開発事業者が管理するMagentoサーバーが侵害された。攻撃者はMagentoのテンプレート処理と依存性注入のコードを悪用し、ログインなしで任意のコードを実行させる。</li>
<li>侵入後は2種類の仕掛けが確認されている。一つはRust言語で書かれたLinux向けの裏口で、外部サーバーに接続して追加の命令を待つ。もう一つはPHPのウェブシェルを書き込むドロッパーだ。Sansecは、パッチ適用に加えて暗号鍵の再生成が必要だとしている。決済情報を扱うサイトは、パッチ当てだけで済ませず侵害の有無を点検する必要がある。</li>
</ul>
<h2>フィッシング代行「BigBear 2.0」、多要素認証を突破して258組織を侵害</h2>
<ul>
<li>インドのセキュリティ企業CloudSEKは、フィッシングを代行するサービス「BigBear 2.0」の管理画面に侵入して調査した結果を公表した。このサービスはEvilginx2という道具を土台に、利用者とMicrosoftの認証基盤の間に割り込む「中間者」型の仕組みで、IDとパスワードだけでなくログイン後のセッションのクッキーごと盗む。多要素認証を通したあとのセッションを乗っ取るため、認証コードやアプリ承認があっても防げない。</li>
<li>管理画面の記録では、多要素認証の突破を伴う侵害が258組織で完了しており、盗まれた認証情報は合計5137件。内訳は多要素認証を突破した完全な認証が474件、平文パスワード1032件、セッションクッキー4148件で、40カ国以上の3331個の被害IPにまたがる。少なくとも5つの攻撃グループがこの多人数向け管理画面を借りて使っていた。標的はMicrosoft 365で、Exchange Online、Teams、SharePoint、OneDrive、Entra IDが含まれる。</li>
<li>独自のJavaScriptで、パスキーにあたるFIDO2・WebAuthnの機能を無効化し、より弱い認証方式へ誘導する仕掛けも入っていた。CloudSEKは、露出したパスワードの変更とセッションの失効に加え、フィッシングに強いパスキー認証の強制、管理下の端末からのみ接続を許す条件付きアクセスの導入を挙げている。</li>
</ul>
<h2>学習アプリMathspace、Metabase経由で108万人分の個人情報が流出</h2>
<ul>
<li>オーストラリア発の数学学習プラットフォームMathspaceは2026年9月7日、社内向けの集計ソフトMetabaseの脆弱性を突かれ、1,079,819人分の個人情報が盗まれたと公表した。影響を受けたのはオーストラリアとニュージーランドの児童生徒、保護者、学校職員で、9月7日の回で扱ったMetabaseの認証なし管理者権限奪取（CVE-2026-72898）と同じ構図だ。</li>
<li>時系列では、攻撃者は8月10日に最初の侵入を果たし、8月27日にオーストラリアの集計用データベースからデータを持ち出した。9月3日に侵害を確認し、9月7日に公表している。盗まれたのは氏名などの個人情報で、学習記録、成績、パスワード、認証トークン、シングルサインオンの認証情報、API認証情報、アカウントと学校を結びつける記録は含まれないとしている。</li>
<li>攻撃はShinyHuntersと呼ばれるグループの仕業とみられている。複数の企業が使う自前運用のMetabaseを同時期に狙う手口が共通するためだ。内部の可視化ダッシュボードは、業務データベースの認証情報を持ちながらインターネットに公開されがちで、そこが侵入口になる。対象バージョンのMetabaseを外部公開している組織は、9月7日の回で伝えた通り即時の更新が要る。</li>
</ul>
<h2>航空旅客2億2000万件超、ベトナム関連の乗客情報データベースが露出</h2>
<ul>
<li>セキュリティ企業Kinryū Labsは2026年6月3日、ランサムウェアの調査中に、認証なしで読める状態のElasticsearchクラスター（「pax-info」、約107ギガバイト、29個の索引）を発見した。中身は旅客記録が210,318,069件、乗員記録が10,465,631件で、合計220,783,700件にのぼる。データはハノイのViettelに割り当てられたIP空間で運用されていたが、具体的な運用組織は特定されていない。</li>
<li>露出していた項目は、氏名、生年月日、性別、国籍、パスポートなど渡航書類の番号と有効期限、発行国、便名と搭乗日、航空会社、出発・到着・経由の空港、座席、手荷物の参照番号などだ。これは各国が入国審査前に受け取る「事前旅客情報（APIS）」に相当する。記録は2017年1月から2026年4月までの約9年分におよび、韓国・中国・カナダ・ニュージーランド国籍の旅客が含まれていた。対象の航空会社はアジア太平洋、欧州、中東にまたがる。</li>
<li>研究者は6月8日までに修復されたことを確認した。身代金の要求文やデータの売り出しは見つかっていないが、サーバーの記録がないため無断複製を完全には否定できないとしている。パスポート番号と渡航履歴がひも付いた情報は、なりすましや標的型の詐欺に使われやすい。</li>
</ul>
<h2>FreeIPAに認証不要で管理者権限を奪う脆弱性連鎖、CVSS9.8</h2>
<ul>
<li>Red Hatは2026年9月8日、Linuxのドメイン全体でログイン権限を管理する認証基盤FreeIPAに、認証なしの攻撃者が管理者権限を奪える脆弱性連鎖があると公表し、14件の勧告を出した。中心はFreeIPA側のCVE-2026-76578（CVSS9.8）と、その基盤である389 Directory ServerのCVE-2026-76560（CVSS7.5）で、別途CVE-2026-79678（CVSS8.1）も修正された。</li>
<li>攻撃は二つの欠陥の組み合わせで成立する。まずFreeIPAが、認証していない利用者にもワンタイムパスワードのトークン管理を許してしまう。次に389 Directory Serverのアクセス制御が、空のクライアント名を空の登録値と一致するものとして扱う。この結果、匿名の攻撃者が自分の好きなKerberos IDを作り、管理者グループに入り込める。</li>
<li>修正版はFreeIPA 4.13.4で、FreeIPA側の2件を直す。実際の攻撃はまだ確認されていないが、Red Hatは「まったくアクセス権のない機体」を含む初期設定の環境で再現に成功したとしている。暫定策は、ファイアウォールでLDAPのポート（389・636）へのアクセスを制限し、依存関係がないことを確認したうえで匿名のLDAP接続を無効化することだ。</li>
</ul>
<h2>Google、生成AIを組み込んだ攻撃フレームワーク「Recon」を報告</h2>
<ul>
<li>Googleの脅威情報部門（GTIG）は、攻撃者が生成AIを組み込んだ自動化の枠組みを使い始めていると報告した。露出した指令サーバー上で見つかった「Recon」というフレームワークは、偵察と認証情報の管理を自動で行い、API鍵を含む23,800件超の窃取済み秘密情報を管理していた。攻撃者は脆弱性の探索、第三者の認証情報の大量収集、通信経路の切り替え、侵害済みクラウド環境を経由した回避を、人手をほとんど介さずに回している。</li>
<li>ある事例では、AIのコーディング補助と手順書にあたる指示ファイルを使い、侵害済みのクラウド基盤に対する大規模な認証情報収集の仕組みを6時間で構築していた。ロシア拠点のグループはAIをTelegramの監視に組み込み、サプライチェーン攻撃集団UNC6780（別名TeamPCP）もこの種の自動化を使っている。Googleは自社のAI「Gemini」の悪用も早期に検知して遮断したとしている。</li>
<li>Googleが示した数字で重いのは、攻撃者がいったん正規の認証情報を手に入れると、その後の操作を防げるのは37%にとどまるという点だ。入口で止める多要素認証やパスキーの比重が、これまで以上に大きくなる。</li>
</ul>
<h2>Bing検索の結果を汚染する長期キャンペーン「BengalSEO」、マルウェアとサポート詐欺へ誘導</h2>
<ul>
<li>調査企業The DFIR Reportは2026年8月、Bingの検索結果を汚染してマルウェアやサポート詐欺へ誘導する大規模なSEO汚染作戦「BengalSEO」を公表した。インド・ラジャスタン発で少なくとも2015年から続いており、発見は2026年3月。2024年1月から2026年3月の間に84個のGitHubアカウントが使われ、囮ページには2000本以上の被リンクが張られていた。</li>
<li>手口は、「bitdefender central how to login」のような正規の検索語を狙い、囮ページを上位に押し込む。ページはgithub.io、pages.dev、sites.google.com、readthedocs.ioなど信頼されるサービスに置き、JavaScriptでHTML構造を毎回組み替えてクローラーには別ページに見せる。訪問者は振り分けシステムを通され、CloudflareのTurnstileなどで自動調査を弾いたうえで最終ページへ送られる。</li>
<li>最終ページは2系統。一つは、利用者がダウンロードしたつもりのソフトを装ったJavaScriptドロッパーで、独自マルウェア「MayaBot」（2022年から使用、wscript.exeで実行、C2と暗号資産採掘ツールXMRigを展開）を仕込む。もう一つは、Bitdefenderアカウントの不審な動きを口実に攻撃者のサポート番号へ電話させる技術サポート詐欺だ。囮ページは動画配信、ウイルス対策、税務、ギフトカードの有効化などを詐称する。対策は、公式サイトをブックマークから開き、検索経由の「ログイン方法」ページからソフトを入手しないことだ。</li>
</ul>
<h2>Grindr、HIV情報の広告目的共有をめぐり英国で2600万ポンドの和解</h2>
<ul>
<li>出会い系アプリのGrindrは、利用者のHIV状態と最終検査日を広告最適化の事業者ApptimizeとLocalyticsに共有していたとして、英国で提起された集団訴訟に2600万ポンド（約3510万ドル）で和解した。支払いは2026年12月末までに1300万ポンド、2027年3月末までに1300万ポンドの2回に分ける。訴訟には1万人超の利用者が名を連ねた。</li>
<li>問題とされたのは2020年より前、中国のKunlunが運営していた時期のデータの扱いで、機微な情報を商用・広告目的で共有した点が英国のプライバシー法に反するとされた。集団訴訟はAusten Hayes法律事務所が起こした。Grindrは「和解に責任の認定や責任の自認は含まれない」としつつ、一部の英国利用者が示した苦痛と信頼の低下は認めるとコメントしている。</li>
<li>この慣行は2018年にノルウェーの非営利団体SINTEFが指摘して停止され、ノルウェーのデータ保護当局は950万ユーロ（後に550万ユーロに減額）の制裁金を科していた。HIV状態のような情報は、いったん広告事業者の手に渡ると回収が難しい。アプリに health 関連の情報を入れる際は、それが第三者に渡り得る前提で考える必要がある。</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>8件を貫く軸は二つだ。一つは、盗んだ認証情報とセッションを使う攻撃がAIとサービス化で量産段階に入ったこと。BigBear 2.0はMFA突破を代行サービスにし、GoogleのReconはAIで偵察と認証情報管理を自動化し、BengalSEOは検索結果の汚染を10年がかりで工業化していた。正規の認証情報を握られたあとに防げる操作は37%という数字が、入口対策の重さを示す。</li>
<li>もう一つは、内部向けの道具が外向けの侵入口になっていることだ。Mathspaceの108万人流出は、集計ソフトMetabaseの認証なし管理者権限奪取が原因で、9月7日に伝えた脆弱性の具体的な被害が早くも出た形になる。FreeIPAの認証基盤も、認証なしで管理者になれる連鎖が見つかった。</li>
<li>個人の備えは、パスキーの利用、コマンドを貼り付けさせる画面を攻撃と見なすこと、健康や渡航に関わる情報は第三者に渡り得る前提で入力すること。組織は、多要素認証だけに頼らずパスキーと条件付きアクセスを重ね、インターネットに公開した管理・集計ツールを棚卸しし、依存ライブラリの取り込みに版と公開元の確認を挟むことだ。</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://thehackernews.com/2026/09/adobe-patches-magento-zero-day.html">The Hacker News: Adobe Patches Magento Zero-Day Exploited to Deploy Rust Backdoor and PHP Web Shell</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/magento-stylesmuggler-zero-day-exploited-to-deploy-linux-backdoor/">Bleeping Computer: Magento StyleSmuggler zero-day exploited to deploy Linux backdoor</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/bigbear-microsoft-365-phishing-service-bypassed-mfa-at-258-organizations/">Bleeping Computer: BigBear Microsoft 365 phishing service bypassed MFA at 258 organizations</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/mathspace-discloses-data-breach-affecting-over-1-million-people/">Bleeping Computer: Mathspace discloses data breach affecting over 1 million people</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/220-million-traveler-records-exposed-in-vietnam-linked-apis-leak/">Bleeping Computer: 220 million traveler records exposed in Vietnam-linked APIS leak</a></li>
<li><a href="https://thehackernews.com/2026/09/freeipa-flaw-chain-lets-anonymous.html">The Hacker News: FreeIPA Flaw Chain Lets Anonymous Clients Create Reusable Administrator Credentials</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/hackers-build-ai-frameworks-for-widescale-credential-theft/">Bleeping Computer: Hackers build AI frameworks for widescale credential theft</a></li>
<li><a href="https://thehackernews.com/2026/09/bengalseo-poisons-bing-search-results.html">The Hacker News: BengalSEO Poisons Bing Search Results to Deliver MayaBot and Tech Support Scams</a></li>
<li><a href="https://thehackernews.com/2026/09/grindr-to-pay-26-million-to-settle-uk.html">The Hacker News: Grindr to Pay £26 Million to Settle U.K. Claims Over HIV Status Data Sharing</a></li>
</ul>

</details>

---

[← 2026-09-08 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
