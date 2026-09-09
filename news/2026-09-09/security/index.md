---
title: "Microsoft過去最多974件修正、WeChat着信ワーム、ChatGPT経由のGmail流出｜セキュリティニュース 2026/09/09"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# Microsoft過去最多974件修正、WeChat着信ワーム、ChatGPT経由のGmail流出｜セキュリティニュース 2026/09/09

**2026-09-09 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-09-09-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-09-09-security)

---

## 概要

Microsoftの月例更新974件と悪用済みゼロデイ2件、F5 BIG-IPへのルートキット、フロリダ州DMV侵害の主張、WeChatのゼロクリックワーム、ChatGPTの隠し指示によるGmailデータ送信、1億5300万件超の身分証画像販売、TeamPCP逮捕、NetScalerの認証不要RCEを解説します。

個人はAIアシスタントに接続する外部サービスの権限を絞り、身分証画像を預けるサービスを見直してください。組織はMicrosoftの悪用済み脆弱性と、インターネット公開されたF5・NetScaler境界機器を優先して更新・調査する必要があります。

#セキュリティ #サイバー攻撃 #Microsoft #WeChat #ChatGPT #脆弱性 #ずんだもん

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年9月9日）</h1>
<p><strong>キーワード:</strong> Microsoft9月パッチ974件 / F5 BIG-IPルートキット795台 / ShinyHunters フロリダDMV / WeChatゼロクリックワーム / ChatGPT Gmail窃取 / 運転免許証1.53億件販売 / TeamPCP豪州逮捕 / NetScaler認証不要RCE</p>
<h2>オープニング：2026年9月9日 — セキュリティニュース</h2>
<ul>
<li>本日は8本。まずMicrosoftが9月のパッチ火曜日で過去最多となる974件の脆弱性を修正し、悪用済みゼロデイ2件も含まれていた件。次に9月7日の回で伝えたAdobe CommerceのStyleSmugglerと同じ構図の被害として、F5 BIG-IP APM機器がLinuxルートキットで侵害され795台が脆弱なまま残っている件、9月7日・8日の回で扱った窃取グループShinyHuntersがフロリダ州DMVのシステム「DAVID」から20万件超を盗んだと主張している件、WeChatが着信だけでアカウントを乗っ取られるゼロクリックワームを抱えていた件を扱う。</li>
<li>後半は、ChatGPTに仕込まれた隠し指示でGmailのデータが社外アカウントへ流出する欠陥、ダークウェブで運転免許証など1億5300万件超の身分証画像が売られていた事件とFBIの捜査、9月8日の回で「Recon」フレームワーク利用者として触れたサプライチェーン攻撃集団TeamPCPの豪州での逮捕、認証なしでリモートコード実行できるNetScaler ADC/Gatewayの脆弱性を取り上げる。</li>
<li>今日の軸は「窃取グループが同じ手口を異なる標的に使い回している」ことと、「AI関連の製品・エージェント自体が新しい攻撃対象になっている」ことだ。</li>
</ul>
<h2>Microsoft、9月版パッチで974件を修正 悪用済みゼロデイ2件</h2>
<ul>
<li>Microsoftは2026年9月8日（現地時間）、月例のセキュリティ更新「9月のパッチ火曜日」で自社製品の脆弱性974件を修正した。他社由来の25件を合わせると999件で、単月の修正件数としては過去最多となり、これまで最多だった2026年7月の570件を大きく上回った。深刻度が最上位の「Critical」は110件超で、種類別ではリモートコード実行、権限昇格、情報漏えいの3種で全体の約9割を占める。製品別ではWindowsが723件、Officeが111件、SQL Serverが62件、開発ツールが22件だった。</li>
<li>実際に悪用が確認されているゼロデイは2件で、いずれもCVSSスコア7.8のローカル権限昇格の欠陥だ。一つは「CVE-2026-81963」で、Windows Update Stackのリンク解決処理の不備を突いてローカルの攻撃者がシステム権限を奪える。報告者はエアバス・ヘリコプターズのRomain Deperne氏とMicrosoftの脅威インテリジェンスセンター（MSTIC）。もう一つは「CVE-2026-85880」で、Windowsのプロセス間通信機構ALPCのヒープバッファオーバーフローを使って同じくシステム権限を得られる。報告者はセキュリティ企業のVolexityとProofpoint。Microsoftは悪用の規模や攻撃者は明らかにしていない。</li>
<li>Krebs on Securityによれば、AdobeやCisco、Google、Mozilla、OracleなどもAIを使った脆弱性発見でパッチの量とペースを増やしている。ただしTenableのSatnam Narang氏は「AIによる脆弱性発見は干し草の山を大きくしているだけで、組織に影響する『針』を増やしているわけではない」と述べ、FortraのTyler Reguly氏は、月ごとに大量の修正をテストして展開する体制が追いつかない組織が増えると警告している。件数の多さそのものが今回の特徴で、110件超のCriticalとゼロデイ2件から優先して適用しないと運用が回らなくなる規模だ。</li>
</ul>
<h2>F5 BIG-IP APM機器にLinuxルートキット、795台が脆弱なまま公開</h2>
<ul>
<li>セキュリティ企業SophosとESETは2026年9月、F5のBIG-IP APM（Access Policy Manager、社内システムへのリモートアクセスを認証で制御するゲートウェイ機能）機器を狙うLinux向けルートキットを分析して公表した。侵入経路は2025年に公表済みの重大なリモートコード実行の欠陥「CVE-2025-53521」で、これを足がかりに第2段階のペイロードとしてルートキットを送り込む。ESETは同一のマルウェアを「PoisonedRefresh」として別途特定している。</li>
<li>ルートキットはApacheの実行ファイルにインストーラーとして感染し、<code>__libc_start_main</code>を横取りしてApache Portable Runtimeのモジュール読み込み処理をフックする。これにより、正規のPHPスクリプトの中にウェブシェルをディスクへ書かずメモリ上だけに注入する。文字列はRC4で隠蔽され、特殊な形式のリクエストを受け取ると復号してPHPの<code>eval()</code>で実行し、SELinuxの設定も書き換えてBIG-IPのアップグレードをまたいで居座る。</li>
<li>2026年9月7日時点で、CVE-2025-53521に脆弱な状態のままインターネットに公開されているBIG-IP APM機器が795台確認されている。F5は2026年3月にこの脆弱性の深刻度区分を見直しているが、修正済みバージョンへの更新が済んでいない機器が攻撃対象として残り続けている。</li>
</ul>
<h2>ShinyHunters、フロリダ州DMV「DAVID」から20万件超を窃取と主張</h2>
<ul>
<li>窃取・恐喝グループShinyHuntersは2026年9月7日夜、フロリダ州の運転免許証管理システム「DAVID」を侵害し、20万件超のドライバー記録を盗んだとデータリークサイトで主張した。9月7日の回で伝えたMetabaseの脆弱性悪用や9月8日の回で伝えたMathspace（108万人流出）と同じグループとみられ、標的を教育機関から州政府システムへ広げた形になる。</li>
<li>グループの主張によれば、パスワードリセット機能の欠陥を突いてDMV職員やFBI捜査官を含む複数アカウントを侵害し、2026年9月3日から情報の持ち出しを始めたという。盗まれたと主張されているのは氏名・住所・社会保障番号・生年月日、運転免許証番号と発行・失効日、車両登録情報、保険情報、過去の車両情報、駐車許可証などだ。</li>
<li>ShinyHuntersは現在はアクセスを失っており、フロリダ州側が脆弱性を修正中だとも主張している。フロリダDMVからの公式コメントは記事公開時点で出ていない。同様のパスワードリセットを狙った社会工学的な手口は他州のDMVでも報告されており、公的機関の窓口業務システムが狙われる構図が続いている。</li>
</ul>
<h2>WeChatにゼロクリックワーム、着信だけでアカウント乗っ取り</h2>
<ul>
<li>セキュリティ企業Calif（キャリフ）は2026年9月8日、中国のメッセージアプリWeChatに、着信を受けるだけでアカウントを乗っ取られるゼロクリックのワームを実証したと公表した。対象者が電話に出る必要はなく、着信中に自動で実行される。攻撃者はあらかじめ対象者のWeChat連絡先に登録されている必要があるが、実証では3台の試験端末の間で乗っ取りが自動的に連鎖して広がることを確認したという。</li>
<li>検証されたのはiOS 26.6とAndroidの複数バージョンで、HarmonyOSやWindows・Mac・Linux向けクライアントでの検証結果は公表されていない。CalifはWeChatの運営元Tencentへ2026年7月に報告した。</li>
<li>Tencentは2026年8月21日にAndroid版8.0.77、iOS版8.0.76を公開し、8月28日にはサーバー側でも通信経路を遮断する対応を完了、全利用者に軽減策が行き渡ったと説明している。CVE番号や正式なセキュリティ勧告はまだ出ていない。実際の被害報告は今のところない。WeChatは中国語圏を中心に世界で広く使われており、着信だけで連鎖する仕組みは影響範囲が読みにくい。</li>
</ul>
<h2>ChatGPTの欠陥、隠し指示でGmailデータを社外へ送信</h2>
<ul>
<li>セキュリティ企業Check Point Researchは2026年9月8日、ChatGPTの会話の中に仕込まれた隠し指示によって、利用者に見える通常の回答と並行して、接続済みのGmailアカウントからデータを抜き出し別のChatGPTアカウントへ送る欠陥があったと報告した。ChatGPTの「Thinking mode」が二つの処理の流れを並行して進められる性質を悪用し、利用者からは通常の応答しか見えない裏側でデータが持ち出される。</li>
<li>抜け道に使われたのは、OpenAIがパッケージのキャッシュ管理に使っていたJFrog Artifactoryの内部サービスだ。本来は許可されていないはずの通信チャネルとして、異なる利用者のアカウント間でメタデータのプロパティ情報をやり取りできてしまう状態になっていた。攻撃者はペーストしたプロンプト、共有した会話、カスタムGPTに埋め込んだ非表示の指示のいずれからでもこの仕込みを起動できる。</li>
<li>Check Pointは2026年6月にOpenAIへ報告し、OpenAIは該当の内部サービスをオフラインにして対処した。利用者側の操作は不要という。OpenAIは2026年2月にも同じ箇所で見つかった別の抜け道（DNSを使う手口）を修正済みで、同一の仕組みが繰り返し悪用経路として見つかっている形だ。AIアシスタントに外部サービスを接続する際は、見えない処理が並行して走り得ることを前提に権限範囲を絞る必要がある。</li>
</ul>
<h2>ダークウェブで運転免許証1億5300万件超が販売、FBIが捜査</h2>
<ul>
<li>セキュリティ記者Brian Krebs氏は2026年9月1日、米国・カナダの運転免許証のデジタル画像1億5300万件超をロシア系ダークウェブフォーラム「Exploit」で販売する新サービス「Nexus」を報じた。あわせて身分証1000万件超、渡航書類300万件超、医療カード57万9000件超も扱われており、赤外線・紫外線スキャン画像を含む複数形式で提供されていたという。</li>
<li>画像の出どころとみられるのは、ルイジアナ州ニューオーリンズの本人確認企業idscan.netだ。月2100万件超の認証処理を行っており、顧客にはHertz、Target、大麻販売チェーンPlanet13などが含まれる。Krebs氏自身の画像や、大麻店Planet13の来店日時・レンタカー利用時間帯と一致する画像が確認できたと、複数の被害者への取材で裏付けている。</li>
<li>報道を受けてFBIニューオーリンズ支局がidscan.netのデータ流出について正式に捜査を開始し、サイバー部門の上級責任者も加わっているという。Nexusは2026年9月2日、報道の翌日にダークウェブから削除された。本人確認サービスは運転免許証の原本画像をそのまま保持していることが多く、そこが一括して破られると偽造・なりすましの材料が大量に出回ることになる。</li>
</ul>
<h2>サプライチェーン攻撃集団「TeamPCP」、豪州で2人逮捕</h2>
<ul>
<li>オーストラリア連邦警察（AFP)は2026年8月27日、西オーストラリア州パースに住む23歳の男2人（Ruben Ian Thomson容疑者、Michael Gaebler容疑者）を、サプライチェーン攻撃集団「TeamPCP」のメンバーとして逮捕したと発表した。9月8日の回でGoogleの「Recon」フレームワークの利用者として触れたUNC6780(別名TeamPCP)と同じグループで、逮捕は摘発の続報にあたる。</li>
<li>AFPによれば、TeamPCPは2025年後半から活動し、自己増殖型ワーム「Shai-Hulud」を使って数百のオープンソースソフトウェアツールに悪意あるコードを埋め込み、GitHub上で少なくとも3800件のコードリポジトリを侵害した。認証情報管理ツールLiteLLMを狙った攻撃では2500超の組織からクラウドの鍵を窃取したとされ、BMW、Audi、Honda、Mercedes-Benz、Volvo、Toyotaなど自動車大手を含む「数千の世界中の企業」から詐欺的な被害を得たという。</li>
<li>両容疑者は計14件のサイバー犯罪容疑で起訴され、2026年9月18日に法廷に再出廷する予定。オープンソースの依存パッケージに悪意あるコードを混入させる手口は摘発が難しいとされてきたが、今回は実行者の身元特定と逮捕まで到達した数少ない事例になる。</li>
</ul>
<h2>NetScaler ADC/Gatewayに認証不要RCEの脆弱性、CVSS重大</h2>
<ul>
<li>watchTowr Labsは2026年8月14日、Citrix NetScaler ADCとNetScaler Gatewayのヒープベースのバッファオーバーフローの脆弱性「CVE-2026-8452」について詳細分析を公表した。JPCERT/CCも2026年8月15日付でこの内容を注意喚起している。もともとは2026年6月30日に「サービス運用妨害（DoS）につながる不審な挙動」として公表されていた欠陥だが、watchTowrの分析でSAMLのサービスプロバイダーまたはIDプロバイダーとして構成されている場合、認証なしでリモートコード実行やウェブシェル設置に発展し得ることが判明した。</li>
<li>影響を受けるのは、NetScaler ADC/Gatewayの14.1-72.61より前のバージョン、13.1-63.18より前のバージョン、FIPS対応版の14.1-72.61 FIPSより前のバージョン、FIPS・NDcPP対応版の13.1-37.272より前のバージョンと幅広い。NetScaler製品は社内外の境界に置くリモートアクセス機器として使われることが多く、9月6日の回で扱ったFortinet製VPN機器の認証情報漏えいと同様、境界機器の欠陥がそのまま社内侵入の入り口になり得る。</li>
<li>対策は修正済みバージョンへのアップグレードで、JPCERT/CCは十分なテストを経たうえでの適用を促している。当初「DoSのみ」として公表された欠陥が、後の詳細分析でリモートコード実行につながると判明する例は珍しくなく、深刻度が低いと見なされた脆弱性でも修正を後回しにしない姿勢が必要になる。</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>8件を貫く一つ目の軸は、既知の窃取グループが手口を変えず標的だけを広げていることだ。ShinyHuntersはMetabase・Mathspaceに続いてフロリダ州DMVを狙い、TeamPCPはGoogleのRecon利用者として名前が挙がった直後に逮捕者が出た。同じ名前が複数の事件で繰り返し登場する。</li>
<li>二つ目の軸は、AI関連の製品・サービス自体が新しい攻撃対象になっていることだ。ChatGPTの隠し指示によるGmail窃取は、AIアシスタントに外部サービスをつなぐ設計そのものの危うさを示し、WeChatのゼロクリックワームは着信という日常的な操作が起点になる怖さを示した。</li>
<li>個人にできることは、身分証を求めるサービスにはできるだけ複製画像を残さないこと、AIアシスタントに接続する外部サービスの権限を必要最小限にすること。組織は、境界機器（NetScaler、F5など）の脆弱性を「DoSのみ」といった当初の評価だけで軽視せず、パッチ適用の優先順位を深刻度と公開状況の両方で見直す必要がある。</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://krebsonsecurity.com/2026/09/microsoft-plugs-nearly-1000-security-holes/">Krebs on Security: Microsoft Plugs Nearly 1,000 Security Holes</a></li>
<li><a href="https://thehackernews.com/2026/09/microsoft-patches-record-974-flaws.html">The Hacker News: Microsoft Patches Record 974 Flaws, Including Two Exploited Windows Zero-Days</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/hackers-breach-f5-big-ip-apm-devices-to-deploy-linux-rootkit/">Bleeping Computer: Hackers breach F5 BIG-IP APM devices to deploy Linux rootkit</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/shinyhunters-hackers-claim-breach-of-florida-david-dmv-database/">Bleeping Computer: ShinyHunters hackers claim breach of Florida "DAVID" DMV database</a></li>
<li><a href="https://thehackernews.com/2026/09/wechat-zero-click-worm-took-over.html">The Hacker News: WeChat Zero-Click Worm Took Over Accounts on iPhone and Android via Incoming Calls</a></li>
<li><a href="https://thehackernews.com/2026/09/chatgpt-flaw-let-planted-prompt-send.html">The Hacker News: ChatGPT Flaw Let a Planted Prompt Send a Victim's Gmail Data to Another Account</a></li>
<li><a href="https://krebsonsecurity.com/2026/09/fbi-probes-service-selling-153m-drivers-licenses/">Krebs on Security: FBI Probes Service Selling 153M+ Drivers Licenses</a></li>
<li><a href="https://krebsonsecurity.com/2026/08/two-alleged-teampcp-hackers-arrested-in-australia/">Krebs on Security: Two Alleged 'TeamPCP' Hackers Arrested in Australia</a></li>
<li><a href="https://www.jpcert.or.jp/at/2026/at260024.html">JPCERT/CC: NetScaler ADCおよびNetScaler Gatewayにおけるリモートコード実行につながる脆弱性（CVE-2026-8452）に関する注意喚起</a></li>
</ul>

</details>

---

[← 2026-09-09 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
