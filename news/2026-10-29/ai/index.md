---
title: "Mistral、1兆パラメータの防御用モデルを公開 Redditはログイン前提へ ほか今週のAI業界まとめ 2026/10/29"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# Mistral、1兆パラメータの防御用モデルを公開 Redditはログイン前提へ ほか今週のAI業界まとめ 2026/10/29

**2026-10-29 / 生成AIニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-10-29-ai/ai_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-10-29-ai)

---

## 概要

Mistralはサイバー防御向けの巨大モデルの重みを公開し、RedditはAI検索で流入が減るなかログイン前提へ移ります。IBMの正方格子機での論理量子ビット3個のテレポーテーション、CiscoのVPNを落とすゼロデイ、委託先から入られたインシデントまで、ずんだもんと四国めたんが解説します。

▼ 今日のトピック
・Mistral、1兆パラメータの「Mistral Large 4」の重みを公開、狙いはサイバー防御
・AI検索で流入が細ったReddit、「ログイン前提」へ
・シドニー大、IBMの正方格子機で論理量子ビット3個のテレポーテーション
・Cisco、ファイアウォールのSSL VPNを再起動させるゼロデイ「CVE-2026-76418」
・最近のインシデント一覧（Binance、Polymarket、日本航空、ソニーネットワークコミュニケーションズ）

▼ 参考記事・ソース
・TechCrunch「Mistral releases weights for its trillion-parameter AI model, targeting cybersecurity」 https://techcrunch.com/2026/10/29/mistral-releases-weights-for-its-trillion-parameter-ai-model-targeting-cybersecurity/
・TechCrunch「As search traffic dries up, Reddit announces it's shifting to a logged-in experience」 https://techcrunch.com/2026/10/29/as-search-traffic-dries-up-reddit-announces-its-shifting-to-a-logged-in-experience/
・Quantum Computing Report「University of Sydney Demonstrates Multi-Qubit Logical Entanglement and 170-Round Stability on IBM Square-Lattice Nighthawk r2 Processor」 https://quantumcomputingreport.com/university-of-sydney-demonstrates-multi-qubit-logical-entanglement-and-170-round-stability-on-ibm-square-lattice-nighthawk-r2-processor/
・BleepingComputer「New Cisco firewall zero-day exploited to crash SSL VPN devices」 https://www.bleepingcomputer.com/news/security/cisco-warns-of-firewall-zero-day-exploited-to-crash-ssl-vpn-devices/
・BleepingComputer「Binance probes potential $5.8 billion crypto-theft hack」 https://www.bleepingcomputer.com/news/security/binance-probes-potential-58-billion-crypto-theft-hack/
・BleepingComputer「Polymarket halts trading after crypto-draining script breach, $2.5M traced」 https://www.bleepingcomputer.com/news/security/polymarket-halts-trading-after-crypto-draining-script-breach-25m-traced/
・BleepingComputer「Japan Airlines suffers third-party data breach exposing passenger info」 https://www.bleepingcomputer.com/news/security/japan-airlines-suffers-third-party-data-breach-exposing-passenger-info/
・BleepingComputer「Sony ISP subsidiary data breach exposes 2.5 million customer records」 https://www.bleepingcomputer.com/news/security/sony-isp-subsidiary-data-breach-exposes-25-million-customer-records/

#生成AI #ChatGPT #Claude #LLM #AI #人工知能 #ゆっくり解説 #ずんだもん #四国めたん #Mistral #量子コンピュータ #セキュリティ #AI最新情報 #AIニュース

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>生成AI・量子・セキュリティニュース（2026年10月29日）</h1>
<p><strong>キーワード:</strong> 1兆パラメータの防御用オープンモデル / AI検索に客を奪われたRedditのログイン化 / IBMの正方格子機で論理量子ビットの量子もつれ / CiscoのVPNを落とすゼロデイ / 暗号資産と航空会社のインシデント</p>
<h2>オープニング：2026年10月29日 — 生成AI・量子・セキュリティニュース</h2>
<ul>
<li>今日の軸は「開くか、閉じるか」です。Mistralは1兆パラメータ級のモデルの重みを公開し、Redditは逆に、ログインしないと読めない方向へ舵を切りました。</li>
<li>量子では、シドニー大学がIBMの正方格子のプロセッサーで、3つの論理量子ビットにまたがるテレポーテーションまで実行しました。</li>
<li>セキュリティでは、CiscoのファイアウォールのSSL VPNを再起動させるゼロデイと、Binance、Polymarket、日本航空、フランスのENGIEのインシデントを扱います。</li>
</ul>
<h2>生成AIとセキュリティ：Mistral、1兆パラメータの「Mistral Large 4」の重みを公開、狙いはサイバー防御</h2>
<ul>
<li>フランスのMistral AIは10月29日、今月発表した1兆パラメータ級のモデル「Mistral Large 4（ML4）」、愛称「Le Chonk」の重みを公開しました。Hugging FaceとMistralのAPIで入手できます（TechCrunch、10月29日）。</li>
<li>Mistralは、企業と政府に向けた「最先端の主権的なサイバー防御能力」をうたい、コードやITインフラ全体の脅威の検知、分析、対応に使えるとしています。</li>
<li>性能は、中国のオープンウェイトの有力モデル「GLM-5.3」と同等で、1つの作業に使うトークンは47％少ないと主張しています。Artificial Analysisの「Coding Agent Index」では、エージェント型のコーディングでほかのオープンモデルをすべて上回るとしています。</li>
<li>科学担当副社長のピエール・ストック氏は、大きなセキュリティ事故にその場で、しかも自社の設備の中で対応できると説明しました。攻撃側もAIを使うのだから、同じ能力を誰にでも早く届けるべきだという立場です。</li>
<li>同氏は「重みが公開されているので、定義上、誰にも止められないアクセスだ」と述べました。暴走するエージェントの危険は認めつつ、「人を怖がらせたくはない」と話しています。</li>
<li>CEOのアルチュール・メンシュ氏は、AIは「支配ではなく力を与える道具であるべきだ」と述べました。Mistralは、OpenAIやAnthropicといった閉じたモデルの企業が投じる計算資源と資金の「ほんの一部」で最先端の性能を出したと主張しています。</li>
</ul>
<h2>生成AIと社会：AI検索で流入が細ったReddit、「ログイン前提」へ</h2>
<ul>
<li>Redditは10月29日の第3四半期の決算説明会で、サイトを主に「ログインして使う体験」へ移す方針を明らかにしました（TechCrunch、10月29日）。</li>
<li>背景は検索からの流入の減少です。AIの要約が答えを出してしまい、Googleの検索結果からサイトへ人が来なくなっています。10月は検索からの流入が、週平均で100万人以上減りました。</li>
<li>米国の1日あたりの利用者は、第2四半期の5320万人から第3四半期は5070万人に減りました。世界全体は1億3030万人で横ばいでした。Redditは、この流れが続けば来期の利用者が「10％台前半」減りうると警告しています。</li>
<li>一方で業績は好調です。売上高は前年同期比53％増の8億9500万ドル、純利益は74％増の2億8300万ドル。AI企業へのデータ提供を含む広告以外の収入は、35％増の4800万ドルでした。</li>
<li>狙いは、AIによる無断の収集からデータを守り、モデル開発企業とのライセンス契約を増やし、ログインした利用者の行動から広告の精度を上げることです。匿名性は保つとし、「シークレットモード」を作り直しています。</li>
<li>第4四半期に米国外の一部の市場で試験を始めます。CEOのスティーブ・ハフマン氏は、開かれたインターネットに人生を形づくられた自分にとって「大きな変化だ」と書きつつ、「正しい次の一歩だ」としました。</li>
</ul>
<h2>量子コンピュータ：シドニー大、IBMの正方格子機で論理量子ビット3個のテレポーテーション</h2>
<ul>
<li>シドニー大学の研究チームは、IBMの120量子ビットのプロセッサー「ibm_phoenix」で、表面符号の論理量子ビットを使った複数の実験を行い、arXivに論文を出しました（arXiv:2610.32347、Quantum Computing Report、10月28日）。</li>
<li>このプロセッサーは、隣どうしを直接つなぐ正方格子の「Nighthawk r2」です。以前の六角形を崩した「ヘビーヘックス」配線では、表面符号に補助の量子ビットや符号の改変が必要でした。</li>
<li>距離3と距離5の表面符号で、1ラウンドあたりの記憶の誤りを1％未満に抑えました。格子手術（パッチの結合と分割）で作った論理ベル状態の忠実度は93％超です。</li>
<li>3つの論理量子ビットにまたがる状態とゲートのテレポーテーションでは、過程の忠実度が78〜93％でした。</li>
<li>170ラウンドの長時間試験では、5000万回の実行で失敗は8回、誤りの確率は約2×10⁻⁷でした。データとアンシラの役割を毎ラウンド入れ替える「歩く」回路で、全量子ビットを2ラウンドごとに測定・初期化し、計算に使わない準位への漏れを掃除しています。</li>
<li>記憶を保つ段階から、複数のパッチで論理演算をする段階に進んだ実証です。課題として、密な格子でのクロストーク、途中測定と同時に2量子ビットゲートの精度を保つこと、1マイクロ秒未満で応答する復号器が挙げられています。</li>
</ul>
<h2>セキュリティ：Cisco、ファイアウォールのSSL VPNを再起動させるゼロデイ「CVE-2026-76418」</h2>
<ul>
<li>Ciscoは10月29日、ファイアウォールの「ASA」と「Threat Defense（FTD）」のソフトウェアにある、悪用が確認された高深刻度の脆弱性CVE-2026-76418を公表しました（BleepingComputer、10月29日）。</li>
<li>対象は、設定に「webvpn」があり、SSL VPNをどこかのインターフェースで有効にした機器です。トンネルグループで二次認証を設定していると、論理の誤りが起きます。</li>
<li>認証なしの遠隔の攻撃者が、SSLのリモートアクセスVPNへの接続時に細工した要求を送ると、機器が予期せず再起動します。Ciscoの対応チームは今月、実際の悪用を把握しましたが、攻撃者や被害組織、侵害の痕跡は示していません。</li>
<li>完全な回避策はなく、修正版への更新を強く勧めています。すぐに更新できない場合は、既定や独自のトンネルグループで二次認証を無効にする手があります。</li>
<li>Shadowserverは、インターネットから見えるCisco ASAのSSL VPN機器を5万1000台超追跡しています。8月にもASAとFTDのサービス妨害のゼロデイ（CVE-2026-20349）が悪用されており、米CISAは2021年11月以降、Ciscoの欠陥101件を「悪用済み」に登録しています。</li>
</ul>
<h2>セキュリティ：最近のインシデント一覧</h2>
<ul>
<li>Binance（10月29日／不正送金の疑いを調査中）：ホットウォレット「Binance 14」から64種類のトークン約25億3000万ドルが動いたと報じられた。Arkham Intelligenceは関連する55のアドレスの保有額を計58億ドルと集計したが、盗難額は未確定。Tetherは15億6700万ドル超のUSDT、Circleは8億ドル超のUSDCを凍結。Binanceは利用者の資金は「完全に安全」としている</li>
<li>Polymarket（10月29日／外部ツール経由の不正スクリプト）：サイト計測サービスDebugBearが侵害され、配信されたJavaScriptがログイン中のセッションを乗っ取って持ち高を売却し、資産を攻撃者の財布へ送った。攻撃者の財布へ約250万ドルが流れたと追跡され、取引は約1時間止まった。Polymarketは被害を全額補償するとしている</li>
<li>日本航空（10月28日公表／予約システム委託先への不正アクセス）：予約・発券・搭乗手続きに使うAmadeusのシステムに、2023年8月10日から2026年9月23日まで不正アクセスがあった。約9万2000人の予約番号・氏名・便などが見られ、うち約2000人は旅券番号や電話番号も流出。カード番号とパスワードは含まれず、悪用は確認されていない</li>
<li>ENGIE（10月27日報道／取引先の販促基盤への不正アクセス）：フランスのエネルギー大手。取引先が顧客の勧誘や料金プランの販促に使うマーケティング基盤が侵害され、フランス国内の顧客の氏名、住所、メールアドレス、電話番号、供給地点の識別番号、顧客番号、契約番号が見られた。件数は非公表。社内のITシステムは侵害されておらず、銀行情報は含まれないとしている。犯行声明は出ていない</li>
<li>対策：取引所や航空会社、電力会社そのものではなく、計測ツールや予約システム、販促基盤といった外部の仕組みが入り口になりました。流出したメールアドレスを使ったフィッシングに注意し、パスワードを変えてください。</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>Mistralは1兆パラメータ級の防御用モデルの重みを公開し、Redditは検索流入の減少を受けてログイン前提へ移ります。情報を開く側と閉じる側に分かれた1日でした。</li>
<li>シドニー大学は、IBMの正方格子機で3つの論理量子ビットのテレポーテーションと、5000万回で8回という長時間の安定性を示しました。</li>
<li>Ciscoのファイアウォールには、VPNを落とすゼロデイが見つかりました。インシデントでは、委託先の計測ツールや予約システムが入り口になる事件が続きました。</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://techcrunch.com/2026/10/29/mistral-releases-weights-for-its-trillion-parameter-ai-model-targeting-cybersecurity/">TechCrunch: Mistral releases weights for its trillion-parameter AI model, targeting cybersecurity</a></li>
<li><a href="https://techcrunch.com/2026/10/29/as-search-traffic-dries-up-reddit-announces-its-shifting-to-a-logged-in-experience/">TechCrunch: As search traffic dries up, Reddit announces it's shifting to a logged-in experience</a></li>
<li><a href="https://quantumcomputingreport.com/university-of-sydney-demonstrates-multi-qubit-logical-entanglement-and-170-round-stability-on-ibm-square-lattice-nighthawk-r2-processor/">Quantum Computing Report: University of Sydney Demonstrates Multi-Qubit Logical Entanglement and 170-Round Stability on IBM Square-Lattice Nighthawk r2 Processor</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/cisco-warns-of-firewall-zero-day-exploited-to-crash-ssl-vpn-devices/">BleepingComputer: New Cisco firewall zero-day exploited to crash SSL VPN devices</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/binance-probes-potential-58-billion-crypto-theft-hack/">BleepingComputer: Binance probes potential $5.8 billion crypto-theft hack</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/polymarket-halts-trading-after-crypto-draining-script-breach-25m-traced/">BleepingComputer: Polymarket halts trading after crypto-draining script breach, $2.5M traced</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/japan-airlines-suffers-third-party-data-breach-exposing-passenger-info/">BleepingComputer: Japan Airlines suffers third-party data breach exposing passenger info</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/energy-giant-engie-discloses-data-breach-affecting-customers/">BleepingComputer: Energy giant ENGIE discloses data breach affecting customers</a></li>
</ul>

</details>

---

[← 2026-10-29 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
