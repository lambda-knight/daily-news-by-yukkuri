---
title: "免許証1億5300万件流出、パスキー39攻撃手法【セキュリティ 2026/09/05】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# 免許証1億5300万件流出、パスキー39攻撃手法【セキュリティ 2026/09/05】

**2026-09-05 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-09-05-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-09-05-security)

---

## 概要

本人確認企業からの運転免許証画像流出、マイクロソフト398件修正、クロームの悪用済みゼロデイ、病院の多要素認証未導入など7件を解説します。

▼ 今日のトピック
・運転免許証1億5300万件超の流出
・マイクロソフト月例更新398件
・クロームとクラウドストライクのゼロデイ
・シトリックス機器の実攻撃
・パスキー周辺を突く39の手法

▼ 参考記事・ソース
（各記事の媒体名・URLは本編Markdown末尾の参考ソースを参照）

#セキュリティ #脆弱性 #パスキー #サイバー攻撃 #ずんだもん

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年9月5日）</h1>
<p><strong>キーワード:</strong> 運転免許証1.5億件流出 / Microsoft8月398件パッチ / Chrome V8ゼロデイ / CrowdStrike FalconFlank / 仏病院GDPR罰金 / Citrix NetScaler悪用開始 / パスキー39攻撃手法</p>
<h2>オープニング：2026年9月5日 — セキュリティニュース</h2>
<ul>
<li>本日は7本。ダークウェブで1億5300万件超の運転免許証画像が販売されFBIが捜査に入った事件、Microsoftが8月の月例更新で398件の脆弱性を一括修正した件、Google Chromeの実行エンジンV8の悪用済みゼロデイ、匿名研究者が公開したCrowdStrike Falconセンサーの権限昇格ゼロデイ「FalconFlank」、フランスの病院がGDPR違反で50万ユーロの制裁金を科された件、Citrix NetScalerの認証バイパスが実際の攻撃で使われ始めた件、そしてパスキー認証を回避する39の新手法をまとめた研究を扱う。</li>
<li>共通するのは「本人確認」と「認証」という守りの根幹そのものが狙われている点だ。身分証の画像、パスワードの次に来るはずだったパスキー、企業の入り口を守るVPN機器、それぞれが突破されつつある。聞き終えたときに、自分の身分証データや職場の認証方式がどこまで守られているか考えられる構成にする。</li>
</ul>
<h2>運転免許証1億5300万件超がダークウェブで販売、FBIが捜査開始</h2>
<ul>
<li>ブライアン・クレブス氏（Krebs on Security）は2026年9月1日、ダークウェブの「Exploit」フォーラムで新サービス「Nexus」が米国・カナダの運転免許証画像1億5300万件以上を販売していると報じた。運営者は「1年以上継続してデータを抜き取っている」と説明し、24時間で約40万件が新規追加されていた。免許証以外にも身分証1000万件以上、旅行書類・国際IDが300万件以上、医療カードが57万9000件以上含まれていた。</li>
<li>流出源として名指しされたのはルイジアナ州ニューオーリンズを拠点とする本人確認企業IDScan.netで、ハーツ、ターゲット、フェデックスなど500社以上が顧客とされる。クレブス氏本人の免許証もNexusに掲載されており、タイムスタンプが2025年6月にハーツでレンタカーを借りた際の身分確認と一致した。研究者ザック・エドワーズ氏はラスベガスのDEFCON参加時に立ち寄った大麻販売店での本人確認、別の研究者ラリー・ボールドウィン氏はハーツの利用日がタイムスタンプと一致すると証言している。</li>
<li>FBIニューオーリンズ支局は9月1日に正式捜査を開始し、複数のFBI幹部がクレブス氏と電話会議を行った。Nexusのサイトは9月2日午前8時56分に閉鎖された。IDScan.netは調査中とだけ回答している。証人保護対象者や家庭内暴力の被害者にとっては、顔認識と組み合わせれば居場所特定につながる恐れがあり、身分確認のために提出した写真がどこに保管され誰がアクセスできるかを一般の消費者が把握しにくい構造が問題の核心になっている。</li>
</ul>
<h2>Microsoft、8月の月例更新で398件の脆弱性を一括修正、悪用中のゼロデイも</h2>
<ul>
<li>Microsoftは2026年8月11日、Windowsおよび対応ソフトウェア向けに398件の脆弱性を修正する月例セキュリティ更新を公開した。うち42件が「重大」評価。修正の中には、公開時点で既に悪用が確認されていた権限昇格の欠陥「CVE-2026-68820」(CVSS7.0)が含まれる。afd.sysというWindowsソケット接続に関わるコンポーネントの脆弱性で、唯一の実悪用済みゼロデイだった。</li>
<li>ほかに、事前に詳細が公開済みだった脆弱性としてWindows User Profile Service内の権限昇格「CVE-2026-62832」があり、過去に報告された「LegacyHive」という手法との関連が指摘されている。今回の398件という規模は、直近の7月更新で570件超という記録的な件数を修正した流れに続くもので、6月は約200件だった。件数が短期間で急増している背景には、AIによる脆弱性発見の効率化があるとみられる一方、AIが生成した修正パッチ自体は「半分以上の確率で失敗する」との報告もある。</li>
<li>一般の利用者にとっては、月次更新の適用を後回しにしないことが唯一の直接的な対策になる。企業側は、実際に悪用が確認された脆弱性を最優先で当てたうえで、公開済みだが悪用未確認の脆弱性についても攻撃者が詳細情報を利用しやすい状態にあることを踏まえ、優先度を落とさず対応する必要がある。</li>
</ul>
<h2>Google Chrome、実行エンジンV8の悪用済みゼロデイを緊急修正</h2>
<ul>
<li>Googleは2026年9月4日、Chromeブラウザの脆弱性12件を修正する更新を公開した。うち1件「CVE-2026-85046」(CVSS8.8)は、JavaScriptとWebAssemblyを処理する実行エンジンV8内の型混同バグで、既に実際の攻撃で悪用が確認されている。研究者サルバトーレ・グリツィア氏(Serotav)が2026年8月4日に発見・報告した。</li>
<li>技術的には「PACKED_ELEMENTS配列がPACKED_SMI_ELEMENTSマップを受け取ってしまう」不具合で、これを突かれるとJavaScriptヒープ上の任意のメモリを読み書きでき、ブラウザのサンドボックスを越えてコードを実行される恐れがある。対象はChrome152.0.7977.82より前のバージョンで、Windows・macOS向けは152.0.7977.82/.83、Linux向けは152.0.7977.82で修正済み。Googleは悪用の詳細を、大多数の利用者が更新を終えるまで非公開にしている。</li>
<li>Chromeは2026年に入ってから既に6件のアクティブに悪用されたゼロデイに対処しており、ブラウザという最も日常的に使うソフトが年間を通じて攻撃対象になり続けている。自動更新を有効にしたうえで、ブラウザを開きっぱなしにせず定期的に再起動して更新を反映させることが、利用者にできる実質的な防御になる。</li>
</ul>
<h2>CrowdStrikeのセキュリティ製品自体に権限昇格ゼロデイ「FalconFlank」</h2>
<ul>
<li>ハンドル名「Nightmare Eclipse」を名乗る匿名の研究者が2026年9月4日、CrowdStrike Falconセンサーの権限昇格ゼロデイ「FalconFlank」を公開した。対象はWindows11(25H2)およびWindows Server2025の最新版。Falconセンサーが持つ「Officeマクロの疑わしい挙動を検出して削除する」機能を悪用することで、SYSTEM権限のコマンドプロンプトを起動できるという。</li>
<li>皮肉なのは、悪用されたのがマルウェア対策のために組み込まれた保護機能そのものである点だ。CrowdStrikeは調査中と説明し、当面の緩和策として「Microsoft Office File Suspicious Macro Removal」ポリシーの無効化を推奨、代わりにOfficeファイル向けのクラウド型マルウェア対策設定で保護を継続するよう案内している。技術的な詳細はCrowdStrikeの顧客専用サポートポータルでのみ公開されており、一般には限定的にしか共有されていない。</li>
<li>同じ研究者は同じ週にカスペルスキー製品の「HardBreacher」、アバスト製品の「PrettyPrague」、エヌビディア製品の「GreenSection」という別のゼロデインを次々と公開しており、セキュリティ製品やドライバそのものが持つ強い権限が、まとめて攻撃対象として調べ上げられている状況がうかがえる。防御ソフトを入れているから安全、とは言い切れない状態が続いている。</li>
</ul>
<h2>フランスの病院、GDPR違反で50万ユーロの制裁金、原因は多要素認証の未導入</h2>
<ul>
<li>フランスの個人情報保護機関CNILは、サンテティエンヌの私立病院オピタル・プリヴェ・ド・ラ・ロワール(HPL、ラムゼイ・サンテ系列、職員650人・医師180人・病床333)に対し、GDPR第32条・第34条違反を理由に50万ユーロ(約8900万円)の制裁金を科した。侵害は2025年夏に発生し、患者52万4867人分、付き添い人など関係者20万2246人分、合計72万7000人以上のデータが流出した。</li>
<li>侵害の起点は医師1人分のアカウントが乗っ取られたことで、実行者は「Marak」と名乗る未成年のハッカーとされる。CNILが問題視したのは、VPNや多要素認証が導入されていなかったこと、アクセス制御が不十分だったこと、侵入をリアルタイムで検知する監視体制が欠けていたこと、そして被害者への通知が不十分だったことの4点だ。</li>
<li>医療機関は患者の病歴や連絡先という機微な情報を大量に扱う一方、現場のIT予算や人員は限られがちで、今回のように基本的な多要素認証すら導入されていないケースが珍しくない。50万ユーロという金額自体は大企業への制裁金と比べて大きくないが、72万人超という被害規模と「基本対策の欠如」という指摘は、同規模の医療機関にも共通しうる弱点として受け止める必要がある。</li>
</ul>
<h2>Citrix NetScalerの認証バイパス、公表から2週間で実際の攻撃に悪用開始</h2>
<ul>
<li>Citrixが2026年8月19日に公式セキュリティ情報(CTX696939)で対応を発表していたNetScaler ADC・NetScaler Gatewayの認証バイパス脆弱性「CVE-2026-19490」(Critical)について、脆弱性情報企業Previdianは2026年9月3日、オーストラリア・米国・ドイツの3つの異なるIPアドレスから実際の攻撃パターンに一致するリクエストを検知したと明らかにした。SSL VPN、ICAプロキシ、CVPN、RDPプロキシとしてAAA仮想サーバーやゲートウェイに設定された機器が対象になる。</li>
<li>Shadowserverの追跡によれば、インターネットに露出しているNetScaler ADCは2万2000台以上、Gatewayは約1700台にのぼる。公表から攻撃開始までおよそ2週間というスピードは、パッチ情報の公開が同時に攻撃者への設計図にもなっている現実を示している。</li>
<li>Citrixは利用者に対し、セキュリティベースラインを確認したうえで影響を受けるアプライアンスを速やかにアップグレードするよう呼びかけている。VPN機器は社外から社内ネットワークへの入り口という性質上、突破されると被害が組織全体に広がりやすく、パッチ公開から攻撃開始までの短い猶予期間にどれだけ早く対応できるかが被害の有無を左右する。</li>
</ul>
<h2>パスキー認証を崩す39の手法、暗号自体でなく周辺の仕組みが標的に</h2>
<ul>
<li>セキュリティ企業Tokenの研究チームは2026年9月4日、パスワードに代わる認証方式として普及が進むパスキーについて、認証の暗号技術そのものではなく周辺の仕組みを突く39種類の攻撃手法を整理して公表した。手法は大きく、認証時の確認画面を偽装する攻撃、複数端末間の同期・共有機能を狙う攻撃、そして新規登録・アカウント復旧の手続きを悪用する攻撃の3系統に分類される。</li>
<li>確認画面を狙う手法にはパスキー要求を大量に送りつける「プロンプト・フラッディング」や、認証情報の入力インターフェースを偽装する手口が含まれる。同期・共有を狙う手法には、AppleやGoogleのアカウント自体を乗っ取ってクラウド復旧機能ごと奪う手口や、BitwardenやKeePassXCなどパスワード管理ソフトのエクスポート機能を悪用してパスキーを窃取する手口が挙げられている。登録・復旧を狙う手法では、正規の登録手続きに見せかけた偽の登録画面や、サポート窓口を騙して復旧手続きを乗っ取る手口が報告された。</li>
<li>セキュリティ企業SpecterOpsの研究では、マルウェアが秘密鍵そのものを盗み出さなくても、正規のWebAuthn基盤から署名済みの認証情報を横取りできることが実証されている。パスキーはフィッシングによるパスワード窃取という従来型の攻撃には強いが、「暗号は破られていないのに認証は突破される」という39通りの抜け道が並んだことは、パスキーを導入すれば認証が万全になるわけではなく、周辺の運用や復旧手続きまで含めた設計が問われる段階に入ったことを示している。</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>7件を貫くテーマは「本人確認・認証の突破」だ。運転免許証の画像そのものが1億5300万件単位で流出し、パスキーという次世代認証も39通りの回避策が見つかり、企業の入り口となるVPN機器やブラウザ、さらにはセキュリティ製品自体まで攻撃対象になっている。</li>
<li>個人にできることは、身分証を提出する相手を選び、ブラウザとOSの自動更新を止めないこと。企業・組織にとっては、月例パッチを速やかに当てること、VPN機器やセキュリティ製品であっても無条件に信頼せず多要素認証と監視体制を整えることが、フランスの病院の事例が示す教訓になる。</li>
<li>CrowdStrikeやNetScalerのように「守るための製品・機器」自体が突破口になる事例が続いており、対策ソフトを導入した時点で安心とせず、継続的な検証が必要な段階に入っている。</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://krebsonsecurity.com/2026/09/fbi-probes-service-selling-153m-drivers-licenses/">Krebs on Security: FBI Probes Service Selling 153M+ Drivers Licenses</a></li>
<li><a href="https://krebsonsecurity.com/2026/08/microsoft-plugs-nearly-400-security-holes/">Krebs on Security: Microsoft Plugs Nearly 400 Security Holes</a></li>
<li><a href="https://thehackernews.com/2026/09/google-releases-chrome-update-to-patch.html">The Hacker News: Google Releases Chrome Update to Patch Actively Exploited V8 Zero-Day</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/new-crowdstrike-falconflank-zero-day-grants-system-privileges/">BleepingComputer: New CrowdStrike 'FalconFlank' zero-day grants SYSTEM privileges</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/french-hospital-fined-500-000-after-breach-exposes-data-of-727-000/">BleepingComputer: French hospital fined €500,000 after breach exposes data of 727,000</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/hackers-target-critical-citrix-netscaler-auth-bypass-in-attacks/">BleepingComputer: Critical Citrix NetScaler auth bypass now leveraged in attacks</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/39-new-methods-that-compromise-passkey-authentication/">BleepingComputer: 39 New Methods That Compromise Passkey Authentication</a></li>
</ul>

</details>

---

[← 2026-09-05 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
