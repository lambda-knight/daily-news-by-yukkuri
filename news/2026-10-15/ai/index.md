---
title: "OpenAI会議室の録音装置とAIの証拠、Chrome攻撃連鎖【2026/10/15】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# OpenAI会議室の録音装置とAIの証拠、Chrome攻撃連鎖【2026/10/15】

**2026-10-15 / 生成AIニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-10-15-ai/ai_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-10-15-ai)

---

## 概要

AIへの質問履歴が盗聴事件の証拠になり、AIエージェントは6日間でChromeの攻撃連鎖を構築。同じ技術が研究と攻撃を速める現在を、量子・セキュリティまで横断して解説します。

▼ 今日のトピック
・OpenAI役員会議室の録音装置とAIへの質問履歴
・画像生成AIの安全策とAI生成音楽の表示
・GPT-5.6 Solを使ったChromeの3段階攻撃
・Gemini 4 Argonによる量子回路の最適化
・Ciscoの悪用中ゼロデイとフィッシング基盤摘発
・北朝鮮IT労働者のラップトップファーム
・直近1週間のセキュリティインシデント5件

▼ 参考記事・ソース
・Ars Technica「Recording device hidden in toilet paper found in top-secret OpenAI meeting room」 https://arstechnica.com/tech-policy/2026/10/fbi-arrests-openai-engineer-suspected-of-planting-bug-in-conference-room/
・TechCrunch「YouTube Music launches new labels as AI-generated music floods streaming platforms」 https://techcrunch.com/2026/10/14/youtube-music-launches-new-labels-as-ai-generated-music-floods-streaming-platforms/
・The Hacker News「Researchers Used a Public OpenAI Model to Build a $250,000 Chrome Full-Chain Exploit in Six Days」 https://thehackernews.com/2026/10/researchers-used-public-openai-model-to.html
・BleepingComputer「Cisco patches new Secure Email Gateway zero-day exploited in attacks」 https://www.bleepingcomputer.com/news/security/cisco-patches-actively-exploited-secure-email-gateway-zero-day/
・BleepingComputer「Global takedown hits network behind 1 billion phishing messages」 https://www.bleepingcomputer.com/news/security/global-takedown-hits-network-behind-1-billion-phishing-messages/
・BleepingComputer「FBI raids DPRK IT worker laptop farms in Texas」 https://www.bleepingcomputer.com/news/security/fbi-raids-dprk-it-worker-laptop-farms-in-texas-us-nationals-arrested/

#生成AI #ChatGPT #量子コンピュータ #セキュリティ #AIニュース #ずんだもん #四国めたん

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>生成AI・量子・セキュリティニュース（2026年10月15日）</h1>
<p><strong>キーワード:</strong> OpenAI会議室の盗聴器 / 画像生成AIの安全策の後退 / AI生成音楽のラベル表示 / GPT-5.6 SolでのChrome攻撃連鎖 / Gemini 4 Argonの量子回路最適化 / 北朝鮮IT労働者のラップトップファーム</p>
<h2>オープニング：2026年10月15日 — 生成AI・量子・セキュリティニュース</h2>
<ul>
<li>今日の軸は、内側に入れたものが牙をむくとき、何が見張り役になるのかです。</li>
<li>生成AIでは、OpenAIの役員会議室のテレビの裏から、トイレットペーパーで包んだ録音装置が見つかり、社員の技術者が訴追されました。証拠になったのは、社内のAIツールとチャットボットへの質問履歴でした。</li>
<li>研究団体White Circleは、OpenAIとGoogleの画像生成AIが、新しい版ほど性的な画像の生成を防げていないと警告しました。音楽配信では、Deezerに届く新曲の半分超がAI生成となり、YouTube Musicが3段階のラベル表示を始めます。</li>
<li>量子では、Gemini 4 Argonが量子シミュレーション向けの部品回路の費用を100分の1以下にし、耐量子暗号ML-KEMの鍵生成には、電力などの漏れから鍵に迫る新しい攻撃が発表されました。</li>
<li>セキュリティでは、AIエージェントで作ったChromeの攻撃連鎖に25万ドルの賞金、Ciscoのメール防御装置の2か月連続のゼロデイ、10億通のフィッシングを支えた闇市場の摘発、北朝鮮のIT労働者を米国人に見せかける「ラップトップファーム」の一斉捜索、直近1週間のインシデント一覧を扱います。</li>
</ul>
<h2>生成AIとスパイ：OpenAIの役員会議室に録音装置、証拠はAIへの質問履歴</h2>
<ul>
<li>米司法省は10月13日、OpenAIの技術者アブドゥルラフマン・アルフォザン被告（35歳、サウジアラビア国籍で2020年から米永住権）を、口頭の会話を傍受する装置を使った罪で訴追しました。有罪なら最長5年の禁錮と25万ドルの罰金です。</li>
<li>FBIによると、装置はサンフランシスコの建物にある役員用会議室で、テレビ背面のUSB端子に差し込まれていました。トイレットペーパーで包んで隠してあり、9月28日ごろに設置され、2日後の9月30日に見つかりました。中身は暗号化されていました。</li>
<li>部屋は特別な許可を持つ人だけが入れる場所で、技術の進み具合、政府とのやり取り、商業提携などが話し合われていました。被告は2025年7月の入社で、この部屋への入室権限はありませんでした。</li>
<li>宣誓供述書によると、被告は8月に社内の業務用AIエージェントで、幹部会議の場所と時間を調べていました。妻に結びつくチャットボットのアカウントには、装置の固有番号を挙げて、常時録音、声に反応して録音する設定、記録カードの暗号化を尋ねる質問が残っていました。</li>
<li>装置は中国製の小型マイコンボード「Seeed XIAO ESP32-S3 Sense」でした。防犯カメラは9月だけで10日、被告が会議室の外にいる姿をとらえていました。</li>
<li>OpenAIは10月5日に室内へカメラを付け、被告がテレビの裏を確かめる姿を撮影しました。同じ日に被告が遺失物係へ届けたかばんからは、2台目の同型装置が見つかっています。会社はすぐには解雇せず、権限を少しずつ絞り、FBIの逮捕に合わせて解雇しました。</li>
<li>録音を誰に渡すつもりだったかは明らかにされておらず、検察は外国政府のために動いたとは主張していません。それでもFBIのパテル長官は、フロンティアAI企業への諜報の取り締まりを防諜の最優先課題の一つと位置づけました。</li>
</ul>
<h2>生成AIと安全策：画像生成AI、新しい版ほど「脱がせる」指示を防げない</h2>
<ul>
<li>公益法人White Circleは9月公開のプレプリントで、DALL·E 3、GoogleのNano Banana 2、OpenAIのGPT-Image-2の安全フィルターを破る攻撃手法「RISE」を示しました。人が確認した結果、性的な画像が出た割合はDALL·E 3で約13％、Nano Banana 2で10％弱、GPT-Image-2で約3％でした。</li>
<li>攻撃役は、Hugging Faceで誰でも入手できる、安全訓練を外したQwen3-32B。判定役はGemini 2.5 Flashです。1つの指示ではなく、複数の場面で使い回せる攻め方のパターンを探させました。「最先端のモデルがなくても、最先端のモデルの防御は破れる」と、Denis Shilov CEOは述べています。</li>
<li>同じ手法で新版のChatGPT Images 2.5とNano Banana 2.1を試すと、「どちらも前の版より大幅に破りやすい」結果でした。OpenAIとGoogleは、Ars Technicaの取材に回答していません。</li>
<li>White Circleは、性能を優先して安全が後回しになったか、表現できる範囲が広がったかのどちらかとみています。攻撃の仕組みは公開し、11月のNeurIPS 2026で発表する予定です。</li>
<li>背景には被害の急増があります。英国のインターネット・ウォッチ財団は、2026年上半期に法的に児童性的虐待画像にあたるAI画像を6310件確認し、昨年1年分を約40％上回ったとしています。Google共同の調査では、AIで裸の画像を作ったと認めた人の20％が「面白半分」、3分の1近くが「技術を試しただけ」と答えていました。</li>
<li>論点は外部監査です。OpenAIとAnthropicは今週、外部の評価者に厳しい秘密保持契約を求めるべきだと主張しましたが、White Circleは公表を縛る契約には署名しないとしています。</li>
</ul>
<h2>生成AIと音楽：Deezerの新曲は半分超がAI製、YouTube Musicは3段階のラベル</h2>
<ul>
<li>仏Deezerは10月14日、AI生成の曲を検索結果やおすすめから消す切り替えスイッチを年内に導入すると発表しました。オンにすると、AI生成の曲、アルバム、関連アーティストが表示されなくなります。</li>
<li>Deezerに毎日届く新曲のうち、AI生成は2025年に検出の仕組みを入れた時点で約10％でした。2026年7月には50％を超え、1日平均約9万曲に達しています。2025年のIpsosとの調査では、利用者の約45％がAI曲を除く方法を求めていました。</li>
<li>YouTube Musicも同じ日、再生画面に生成AIのラベルを付けると発表しました。音楽の提供元が「完全にAI生成」「一部AI生成」「AI不使用」の3段階で申告し、YouTube独自の検出でも補います。音程補正のオートチューンは「AI不使用」に入ります。</li>
<li>YouTubeは禁止ではなく開示を選び、AIを使っただけでは収益化の対象から外しません。一方でBandcampはAI曲を全面禁止、TIDALはAI曲の収益化を止め、Spotifyは表示を強める方針で、Apple Musicも年内のラベル導入を予定しています。</li>
<li>論点：「聴かない自由」を配るのか、「知った上で聴く」に任せるのか。各社の線引きの違いは、AI曲が売り上げの分け前をどこまで取るかの違いでもあります。</li>
</ul>
<h2>生成AIと攻撃：AIエージェントでChromeの3欠陥を連鎖、賞金25万ドル</h2>
<ul>
<li>米XBOWは10月13日、OpenAIの公開モデル「GPT-5.6 Sol」で動くAIエージェントを使い、Windows版Chromeで、ウェブページを開くだけで任意のプログラムを動かせる攻撃連鎖を作ったと発表しました。Googleは最高額の25万ドルを支払いました。</li>
<li>連鎖は3段です。JavaScriptエンジンV8の欠陥で隔離領域内のメモリを操り、アニメーションWebP画像の処理の欠陥（CVE-2026-85045）で外側のメモリに書き込み、クラッシュ報告機能Crashpadの欠陥（CVE-2026-78952）でサンドボックスの外でプログラムを起動しました。</li>
<li>作業期間は8月2日から7日までの6日間で、計算費用は推定約4万ドル。従来は4人で6〜9か月かかったとされる規模の仕事で、XBOWの最初の挑戦も約2か月かかっていました。</li>
<li>人間の研究者1人が、狙う場所を決めて作業を分け、弱い手がかりを捨て、部品の組み合わせを判断しました。最初の連鎖の1つの欠陥が既知だと指摘されると、WebPの欠陥に差し替えています。</li>
<li>Googleは3件を再現・修正し、実際の攻撃に使われた形跡はないとしています。2026年の規定で全段階をつないだ攻撃への初の支払いで、同種の賞金は年4件までです。XBOWは賞金を、同社の技術を使うNGOの防御に充てるとしています。</li>
<li>論点：低い危険度の欠陥も、つなげば高い危険度になります。防御側が同じ道具を持つまでの時間差が、今後の焦点です。利用者側の対策は、更新が出たらChromeを再起動することです。</li>
</ul>
<h2>量子コンピュータとAI：Gemini 4 Argon、量子シミュレーションの部品回路の費用を100分の1以下に</h2>
<ul>
<li>Googleは10月13日のGemini 4 Argonの公開記事で、量子計算の研究に使った成果を示しました。最近の量子シミュレーションの部品となる逆正弦（arcsin）の計算回路で、Argonが書いた実装は、既に発表されている「量子CORDIC」方式に比べて時空間コストを100分の1以下にしたとしています。</li>
<li>時空間コストは、量子ビットの数とゲート操作の数を掛け合わせた資源の量です。実装は証明支援系Leanで形式的に正しさを検証したとしており、Googleは「最適化された量子回路の標準ライブラリへの一歩」と位置づけています。</li>
<li>誤り訂正でも成果を挙げました。機械学習による誤り訂正の復号器AlphaQubitの社内版を、1つの高度に最適化されたハードウェア用プログラムに書き直し、推論の処理量をほぼ2倍にしました。量子ハードウェアの速さに、実時間で追いつくためです。</li>
<li>10月1日の発表時点では、別の部品回路で既存の最良値を数分で40％上回った例を挙げていました。今回の100倍超は、それとは別の例です。</li>
<li>論点：100分の1は1つの部品回路の結果で、量子計算全体が100倍速くなったわけではありません。ただ、量子アルゴリズムの資源見積もりは、こうした部品の積み上げで決まります。AIが回路を書き、Leanが正しさを保証する組み合わせが広がれば、実用化に必要な量子ビット数の見積もりそのものが動きます。</li>
</ul>
<h2>量子と暗号：耐量子暗号ML-KEM、鍵生成の「符号化」の段階に新たな攻撃</h2>
<ul>
<li>スイスのSEALSQは10月13日、耐量子暗号の標準ML-KEMの鍵を作る過程を狙う攻撃と対策の論文を、トルコのアンタルヤで10月11日に開かれた暗号ハードウェアの国際会議CHES 2026の併設ワークショップ「LightSec 2026」で発表したと明らかにしました。</li>
<li>論文名は「Cross-information lattice attack on ML-KEM」。鍵生成のうち符号化の段階を対象に、装置の消費電力などの漏れを事前の学習で読み取る手法と、格子の数学的な縮約を組み合わせ、どちらか一方だけより効率よく秘密に迫れるとしています。</li>
<li>ML-KEMは、量子コンピュータでも破れないように米国立標準技術研究所が2024年に標準化した鍵交換の方式です。数学的に安全でも、実装が電力や電磁波、処理時間から秘密を漏らせば破られます。</li>
<li>発表では実装上の対策も示しています。ただ、どの装置や実装で何回の測定が必要かは、発表文には書かれていません。</li>
<li>同じ週には、米国の決済団体Nachaが、2030年12月の耐量子化の期限に向けて、取引先に移行計画を確認する30以上の質問例を公開しました。標準化の次は、移行の工程と実装の品質が問われる段階に入っています。</li>
</ul>
<h2>セキュリティ：Cisco Secure Email Gateway、2か月連続でログイン不要のゼロデイ</h2>
<ul>
<li>Ciscoは10月14日、メール防御装置Secure Email Gatewayに、ログインなしで任意のファイルを書き込み、root権限でコマンドを実行される欠陥（CVE-2026-76519）があり、実際に悪用されていると公表しました。10月に悪用を把握したとしています。</li>
<li>細工した添付ファイル付きのメールを、修正前の装置に送るだけで攻撃が成立します。マルウェア対策機能の中で、添付ファイルを扱う際のパスの扱いに欠陥がありました。</li>
<li>対象は、ファイルの評判を照会する機能を有効にしてメールの方針に割り当て、検査用ツールContent Scanner Toolsが25.3.0.5525より古い装置です。修正版は25.3.0.5525以降です。</li>
<li>Ciscoはクラウド版に緩和策を入れ、侵害の恐れがある顧客には連絡しました。侵害された装置では、認証情報と暗号鍵の作り直しを勧めています。Shadowserverは、ネットに露出した装置を300台近く確認しています。</li>
<li>9月にも、メールの解析部分にログイン不要でroot権限を奪われる別のゼロデイ（CVE-2026-76461）が見つかっていました。2025年11月から悪用された最大深刻度の欠陥（CVE-2025-20393）も含め、組織のメールの入り口を守る装置が、繰り返し入り口そのものにされています。</li>
</ul>
<h2>セキュリティ：10億通のフィッシングを支えた闇市場、Microsoftと日本警察が摘発</h2>
<ul>
<li>Microsoftは10月14日、医療業界の情報共有組織Health-ISACとともに、フィッシングの道具一式を売る3つのキット「CoGUI」「Haozi」「Iron Man System」と、その基盤を売る中国語の闇市場「YAM Store」を摘発したと発表しました。米フロリダ州南部地区の連邦地裁の命令で、ドメインを差し押さえました。</li>
<li>この仕組みは、150か国の7万5000を超える組織に向けた10億通超の悪質なメッセージを支えていました。2026年初めからMicrosoftの顧客に向けた分だけで、メールとSMSで7億5000万通を超えます。</li>
<li>捜査はMicrosoftと日本の警察庁が始め、日本サイバー犯罪対策センター、Cloudflare、Proofpoint、Oracleなどが加わりました。CoGUIは米国と日本を狙い、日本企業や国際機関を装ってカード情報を盗んでいました。</li>
<li>手口は、本物の組織が手放した期限切れのドメインを買い取ってサイトを再建し、クラウドの契約を取ることでした。AIで架空の組織の資料をそろえた例もあります。偽の通知は、未払いの通行料、交通違反の罰金、配送の不具合を装っていました。</li>
<li>Microsoftは関連する2万を超えるアカウントを止め、なりすましに使われた10万のドメインを遮断しました。Iron Manには、銀行、小売、配送業者、官公庁を装う2300を超えるひな形がありました。逮捕者と被害額は公表されていません。</li>
</ul>
<h2>セキュリティ：北朝鮮IT労働者の「ラップトップファーム」、テキサスの40か所を一斉捜索</h2>
<ul>
<li>米司法省は10月14日までに、北朝鮮のIT労働者が米国人を装って米企業に雇われる仕組みについて、14人を起訴し、米国人2人を逮捕したと発表しました。FBIは9月21日から25日にかけて、テキサス州の住宅40か所を捜索し、約187台のノートPCと、遠隔で操作するための切り替え機器を押収しました。</li>
<li>「ラップトップファーム」は、企業が社員に送ったノートPCを米国内の住宅に置き、北朝鮮側の労働者が遠隔で操作する拠点です。働き手は盗んだ身分や架空の身分を使い、住宅の担い手が遠隔操作ソフトを入れ、給与を北朝鮮側の口座へ送っていました。</li>
<li>オハイオ州の起訴では、2019年から2025年7月までに米企業70社が被害を受け、北朝鮮側に約300万ドルが流れたとされます。逮捕された2人は、通信詐欺、資金洗浄、身分窃盗の罪に問われています。</li>
<li>CrowdStrikeによると、労働者は偽の盗難届で代わりのPCを送らせる、住所を次々に変える、直前の引っ越しを装う、といった手口で、PCを書類上の住所から別の場所へ回していました。</li>
<li>論点：採用面接と身分確認をすり抜けた「中の人」は、PCの配送先や機器の識別番号の使い回しといった、人事以外の記録から見つかっています。</li>
</ul>
<h2>セキュリティ：最近のインシデント一覧</h2>
<ul>
<li>Ledger（10月9日に調査開始・10月13〜14日に公表／ハードウェア財布のサプライチェーン攻撃の続報）：販売店CryptoBilisの製品に、24語の復元フレーズを読み取り、eSIMでLTE回線から送る部品が仕込まれていました。資金を失った確認例はすべて同店の製品です。インドネシア、シンガポール、タイ、フィリピン、ベトナム、マレーシア、香港の販売店に販売停止を要請しました。欧州のMediaMarktでも改造品の報告があり、同社は商品を撤去しました。</li>
<li>Anywayanyday（10月14日公表／サイバー攻撃によるサービス停止）：2008年創業のロシアの旅行予約サイト。航空券、鉄道、ホテルの新規予約を止め、サイトも停止しています。予約済みの分は有効で、個人情報が漏れた証拠はないとしています。攻撃者は不明で、再開時期も示していません。</li>
<li>アリゾナ州の裁判所（10月7日公表／フィッシングを起点とする情報窃取）：職員がメールの悪質なリンクを開いたことが発端で、9月24日に検知し約2時間で遮断しました。未納の罰金などがある約130万人の氏名と社会保障番号、保護命令約3万件、里親審査の報告書約15万件が複製されました。信用情報の凍結を呼びかけています。</li>
<li>Hirudo（10月14日報道／Android向けの銀行アプリすり替えマルウェア）：ThreatFabricが発見。少なくともインドネシアの7銀行の8アプリを、安全確認を外した改造版に入れ替え、暗証番号やSMSを盗みます。ショッピングや短編ドラマのアプリを装って広がり、攻撃者の管理画面には数千件の認証情報が残っていました。被害者数は不明です。</li>
<li>Xandr（10月12日公表／個人データの違法な処理への制裁）：ノルウェーのデータ保護庁は、Microsoft傘下の広告企業Xandrに、同庁として過去最高の9200万クローネ（約960万ドル）の制裁金を科しました。2018年7月から2020年4月まで、Grindr利用者の性的指向に関わるデータを、有効な同意を確かめずに広告の競売で扱っていました。Microsoftは対応を検討中です。</li>
<li>対策：ハードウェア財布は公式の直販で買うこと、スマホのアプリは公式ストア以外から入れないこと、勤め先や公的機関を名乗るメールのリンクは開く前に送り主を確かめることが、今週の共通の備えです。</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>OpenAIの盗聴事件では、装置を隠した人物の計画が、社内のAIエージェントとチャットボットへの質問履歴に残っていました。</li>
<li>画像生成AIは新しい版ほど安全策が破られやすく、AI生成の音楽は配信各社がラベルと除外スイッチで線を引き始めました。</li>
<li>XBOWは6日間と約4万ドルでChromeの攻撃連鎖を作り、Gemini 4 Argonは量子回路の部品の費用を100分の1以下にしました。同じAIが、攻撃にも研究にも速さをもたらしています。</li>
<li>Ciscoのメール防御装置、Ledgerの財布、テキサスのノートPCと、内側に入れたものが裏切る事例が続きました。見張り役になったのは、質問履歴、防犯カメラ、配送記録といった地味な記録でした。</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://arstechnica.com/tech-policy/2026/10/fbi-arrests-openai-engineer-suspected-of-planting-bug-in-conference-room/">Ars Technica: Recording device hidden in toilet paper found in top-secret OpenAI meeting room</a></li>
<li><a href="https://therecord.media/saudi-national-charged-with-spy-device-openai">The Record: Saudi national charged with planting spy device in OpenAI executive conference room</a></li>
<li><a href="https://arstechnica.com/tech-policy/2026/10/openai-google-pushing-new-ai-models-easily-tricked-into-making-nudes-researchers-say/">Ars Technica: OpenAI, Google pushing new AI models easily tricked into making nudes, researchers say</a></li>
<li><a href="https://techcrunch.com/2026/10/14/deezer-will-soon-let-you-filter-out-ai-generated-music/">TechCrunch: Deezer will soon let you filter out AI-generated music</a></li>
<li><a href="https://techcrunch.com/2026/10/14/youtube-music-launches-new-labels-as-ai-generated-music-floods-streaming-platforms/">TechCrunch: YouTube Music launches new labels as AI-generated music floods streaming platforms</a></li>
<li><a href="https://www.financialcontent.com/article/bizwire-2026-10-13-xbow-rewarded-for-exploit-affecting-a-billion-users">Business Wire (XBOW): XBOW Rewarded for Exploit Affecting a Billion Users</a></li>
<li><a href="https://thehackernews.com/2026/10/researchers-used-public-openai-model-to.html">The Hacker News: Researchers Used a Public OpenAI Model to Build a $250,000 Chrome Full-Chain Exploit in Six Days</a></li>
<li><a href="https://www.remio.ai/post/xbow-chrome-exploit-won-googles-250-000-bounty-but-humans-still-made-the-critica">remio: XBOW Chrome Exploit Won Google's $250,000 Bounty, but Humans Still Made the Critical Calls</a></li>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-argon/">Google: Gemini 4 Argon: Built to solve your hardest problems</a></li>
<li><a href="https://blog.google/intl/en-mena/company-news/technology/gemini-4-argon-our-next-era-of-frontier-intelligence/">Google: Gemini 4 Argon: our next era of frontier intelligence</a></li>
<li><a href="https://www.sealsq.com/investors/news-releases/sealsq-presents-peer-reviewed-research-on-attack-and-countermeasures-on-ml-kem-key-generation-at-lightsec">SEALSQ: SEALSQ Presents Peer-Reviewed Research on Attack and Countermeasures on ML-KEM Key Generation at LightSec</a></li>
<li><a href="https://www.nacha.org/news/check-your-vendors-quantum-safe-readiness-new-tool-nachas-payments-innovation-alliance">Nacha: Check Your Vendors' Quantum-Safe Readiness</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/cisco-patches-actively-exploited-secure-email-gateway-zero-day/">BleepingComputer: Cisco patches new Secure Email Gateway zero-day exploited in attacks</a></li>
<li><a href="https://thehackernews.com/2026/10/cisco-warns-of-active-attacks.html">The Hacker News: Cisco Warns of Active Attacks Exploiting New Critical Secure Email Gateway Vulnerability</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/global-takedown-hits-network-behind-1-billion-phishing-messages/">BleepingComputer: Global takedown hits network behind 1 billion phishing messages</a></li>
<li><a href="https://thehackernews.com/2026/10/microsoft-disrupts-3-phishing-kits.html">The Hacker News: Microsoft Disrupts 3 Phishing Kits Linked to Over 1 Billion Scam Messages</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/fbi-raids-dprk-it-worker-laptop-farms-in-texas-us-nationals-arrested/">BleepingComputer: FBI raids DPRK IT worker laptop farms in Texas, US nationals arrested</a></li>
<li><a href="https://therecord.media/north-korea-laptop-farms-worker-scams-doj-raids-texas">The Record: Two arrested as DOJ takes down laptop farms responsible for $3 million in North Korean revenue</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/ledger-asks-sellers-across-asia-to-halt-sales-after-supply-chain-attack/">BleepingComputer: Ledger asks sellers across Asia to halt sales after supply-chain attack</a></li>
<li><a href="https://therecord.media/russia-anywayanyday-travel-website-cyberattack">The Record: Russian travel booking platform suspends reservations after cyberattack</a></li>
<li><a href="https://therecord.media/arizona-courts-say-hackers-stole-info-on-over-1-million">The Record: Arizona courts say hackers stole info on over 1 million</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/hirudo-android-malware-replaces-banking-apps-to-evade-security-checks/">BleepingComputer: Hirudo Android malware replaces banking apps to evade security checks</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/norway-fines-microsoft-ad-firm-96-million-over-grindr-data-sharing/">BleepingComputer: Norway fines Microsoft ad firm $9.6 million over Grindr data sharing</a></li>
</ul>

</details>

---

[← 2026-10-15 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
