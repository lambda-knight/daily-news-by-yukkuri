---
title: "【AI・量子・セキュリティ】数学の難問とモデル蒸留／光量子部品へ1億ドル／Microsoft 974件修正 2026/09/10"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# 【AI・量子・セキュリティ】数学の難問とモデル蒸留／光量子部品へ1億ドル／Microsoft 974件修正 2026/09/10

**2026-09-10 / 生成AIニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-09-10-ai/ai_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-09-10-ai)

---

## 概要

2026年9月10日の生成AI・量子コンピュータ・セキュリティニュース。OpenAIの数学的成果主張と功績帰属、中国AI企業6社へのモデル蒸留勧告、Apple Watchの常時聞き取り、PsiQuantumの1億ドル助成、Microsoftの974件の修正、Cisco Secure FMCのCVE-2026-20079を解説します。

出演: ずんだもん、四国めたん（VOICEVOX）

#生成AI #量子コンピュータ #セキュリティ #OpenAI #PsiQuantum #Microsoft #Cisco

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>生成AI・量子・セキュリティニュース（2026年9月10日）</h1>
<p><strong>キーワード:</strong> 中国AI企業の蒸留勧告 / ナビエ・ストークス問題の功績論争 / アップルの常時リスニング / サイクアンタムのチップス法助成 / シスコFMCの認証バイパス / クロームV8ゼロデイ</p>
<h2>オープニング：2026年9月10日 — 生成AI・量子・セキュリティニュース</h2>
<ul>
<li>2026年9月10日、生成AI・量子コンピュータ・セキュリティのニュースをまとめてお届けする。</li>
<li>生成AIは3本。米当局が中国のAI企業6社を「フロンティアモデルの大規模な蒸留」で名指しした合同勧告、OpenAIによるナビエ・ストークス問題の「解決」主張と功績をめぐる論争、アップルの新型ウォッチの常時リスニング機能とプライバシー。</li>
<li>量子コンピュータは、米商務省がサイクアンタムなど3社と結んだチップス法の助成契約。</li>
<li>セキュリティは2本。シスコのファイアウォール管理製品で最大深刻度の認証バイパスが実際に悪用された件と、クロームのV8エンジンで2026年7件目となる悪用済みゼロデイ。</li>
<li>通底するのは、フロンティアAIの成果と模倣の線引き、そして「3月や8月に公表済みだった脆弱性が、実際の悪用確認で一気に優先度を上げた」構図。</li>
</ul>
<h2>生成AIと社会：中国AI企業6社へのモデル蒸留勧告</h2>
<ul>
<li>2026年9月8日、米国のNSA・CISA・FBIが合同のサイバーセキュリティ勧告（AA26-251A）を公表した。</li>
<li>中国拠点のAI企業6社、すなわちディープシーク、ムーンショットAI、アリババ、ミニマックス、ステップファン、ゼットエーアイが、少なくとも2024年後半以降、米国のフロンティアAIモデルから数百万回のやり取りを通じて数十億トークン規模の出力を組織的に抽出してきた、と指摘している。</li>
<li>標的とされたのは、アンスロピックのクロード、OpenAIのGPT、グーグルのジェミニ、xAIのグロックの各系列。</li>
<li>手口は、不正アカウントや共有アカウント、クラウドサービス、集約業者、「中継ステーション」型プロキシに要求を分散させて、地理的制限や利用上限、検知を回避するというもの。思考連鎖の推論過程を引き出す抽出、遮断されたときの経路の自動切り替え、防御策の有無を見分ける品質評価の仕組みも使われていたとする。</li>
<li>当局は、規模と洗練度から中国政府が把握しているとみられ、6社にとって蒸留は補助的な道具ではなく製品開発の中心的な手法だと評価している。米国と同盟国に影響し得る軍事・サイバー能力の強化にもつながるとする。</li>
<li>推奨されている対策は、異常なプロンプト・アカウント・挙動の検知、契約額と実際の利用量の比率の監視、蒸留が疑われる相手への出力品質の抑制、提供各社をまたいだ情報共有。CVE番号を伴う脆弱性の話ではなく、正規APIの使われ方そのものへの警告という点が特徴。</li>
</ul>
<h2>生成AI：OpenAIの数学的成果主張と功績の帰属</h2>
<ul>
<li>OpenAIは2026年9月8日、社内のAIシステムが、なめらかな外力を加えた場合にナビエ・ストークス方程式の解が有限時間で特異点を生じることを示す証明を作り、クレイ数学研究所のミレニアム懸賞問題の一つを解決したと主張した。</li>
<li>ここでの特異点とは、有限の時間で流速が上限なく発散する破綻のことで、現実の流体には起こらない挙動を指す。</li>
<li>同社の説明では、最大およそ1万体のAIエージェントをほぼ並行して動かし、約88時間で証明に到達した。作業は9月1日に、バックマスター氏とアルペーゲ氏に関する噂を聞いて始めたという。100万ドルの賞金は請求しない意向を示している。</li>
<li>これに対し、ニューヨーク大学のバックマスター教授とアンスロピック研究者のアルペーゲ氏は9月7日、アンスロピックのクロードとOpenAIのコーデックスを使って約1年かけて取り組み、8月15日に突破、8月22日に形式検証を終えたとして、多孔質媒体、ブシネスク近似、3次元オイラーでの有限時間爆発という3件の関連結果と形式化を公開した。</li>
<li>バックマスター氏は、OpenAIからアンスロピック所属の共著者の名前を外すよう圧力を受けたと述べ、OpenAIの証明はまだ公開も査読もされておらず自分は見ていない、としている。</li>
<li>争点は、フロンティアの研究室が提供するツールを使って未公表の研究を進めるとき、その成果と優先権が守られるのかという、AI支援研究の信頼の問題に及んでいる。</li>
</ul>
<h2>生成AIとプライバシー：Apple Watchの常時聞き取り</h2>
<ul>
<li>アップルは9月9日の発表イベントで、新型のアップルウォッチであるシリーズ12とウルトラ4に、直前の発話を文字起こしする機能や、周囲の会話を要約する「インテリジェント」なリスニング機能を載せると発表した。</li>
<li>同じイベントでは、約2000ドルの折りたたみ式アイフォーンや、写真がAIで加工されたかを利用者が確かめられる新機能も公開された。</li>
<li>アップルは、生の音声は保存しないと説明している。ただし、常に録音され得ると分かっている状況で人がどう振る舞うか、同意やプライバシーをどう考えるか、という問いは残る。</li>
<li>Wiredなどは、プライバシー保護の作り込みがあっても、機器が周囲の音を聞き取って要約するという機能の性質そのものは変わらない、と指摘している。</li>
<li>論点は、「技術は常に聞いている」ことを当たり前にしていく方向で、消費者向け機器のリスニング機能がまた一段普及することにある。</li>
</ul>
<h2>量子コンピュータ：PsiQuantum、光量子部品の量産へ1億ドル</h2>
<ul>
<li>2026年9月8日、米商務省が、半導体関連の産業政策法であるチップス法に基づく助成の最終契約を量子コンピュータ企業3社と結んだ。総額は最大3億ドルで、光方式のサイクアンタム、イオントラップ方式のクオンティニュアム、超伝導方式のリゲッティという異なる3方式に配分される。</li>
<li>サイクアンタムの助成は1億ドルで、2026年5月の基本合意に続くもの。国内の半導体プロセス開発、光部品の量産性の向上、誤り耐性型量子コンピュータ向けの国内サプライチェーンの強化に充てるとしている。</li>
<li>具体的には、低損失の光スイッチに使うチタン酸バリウムの薄膜を、カリフォルニア州サンタクララの拠点で分子線エピタキシー装置を用いて300ミリウエハーで量産することを加速する。単一光子検出器や先端実装技術の開発・製造も対象。</li>
<li>位置づけとしては、基礎研究への資金ではなく、極低温、実装、制御エレクトロニクス、光学、製造の再現性といった「スケールの壁」に狙いを定めた投資。前日に伝えたデンマークの動きが財団による製造基盤への投資だったのに対し、今回は米政府の産業政策として量子の製造を国内に囲い込む動きにあたる。</li>
</ul>
<h2>セキュリティ：Cisco Secure FMCのCVE-2026-20079が悪用中</h2>
<ul>
<li>シスコの「Secure Firewall Management Center」ソフト、いわゆるFMCのウェブ管理画面に、認証を回避できる脆弱性CVE-2026-20079が見つかっている。CVSSは最大の10.0。</li>
<li>認証されていない遠隔の攻撃者が、細工したHTTPリクエストを送るだけで認証を回避し、機器上でスクリプトやコマンドをroot権限で実行できる。原因は、起動時に作られる不適切なシステムプロセスが別の認証経路を生んでしまうこと。</li>
<li>時系列では、シスコは2026年3月にこの脆弱性を公表して修正を出したが、当時は悪用の痕跡はないとしていた。9月9日に勧告を更新し、2026年8月に実際の悪用を把握したと確認した。シスコのタロスは、複数の攻撃グループがウェブシェル、Java製のコマンド実行ツール、認証情報の窃取にこの欠陥を使っているとしている。</li>
<li>7月29日に公表された固定認証情報の脆弱性CVE-2026-20316、CVSSは5.3、とも痕跡が共通する。CISAは9月9日にCVE-2026-20079を悪用確認済みの脆弱性カタログに追加し、米連邦機関に9月12日までの対処を義務付けた。回避策はなく、最新版へのアップグレードが対策。</li>
<li>影響としては、FMCは複数のファイアウォールを一括管理する要のシステムで、乗っ取られるとセキュリティポリシー、認証情報、構成、つながった機器まで攻撃者の管理下に入る。</li>
</ul>
<h2>セキュリティ：Chrome V8のCVE-2026-87491が悪用中</h2>
<ul>
<li>グーグルは2026年9月8日公開の安定版でクローム153系を出し、230件の脆弱性を修正した。うちCVE-2026-87491は、すでに実環境で悪用されているゼロデイ。</li>
<li>対象はクロームのジャバスクリプトとWebAssemblyのエンジンであるV8の境界外書き込みの欠陥で、深刻度は「中」。細工したウェブページを開かせることで、サンドボックス内で任意コードを実行できる。ただし機器を完全に乗っ取るには、サンドボックスからの脱出が別途必要になる。</li>
<li>グーグルは「悪用が実環境に存在することを把握している」とだけ述べ、攻撃者や手口は明かしていない。</li>
<li>報告は2026年8月6日、ソウル大学のコンプセック研究所のジヒョン・ジョン氏によるもので、報奨金は2500ドル。これは2026年に入ってグーグルが修正した、実際に悪用されたクロームのゼロデイの7件目にあたる。</li>
<li>修正版はクローム153.0.8010.36系。すぐに更新して再起動するのが対策になる。</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>6社の蒸留勧告とOpenAIのナビエ・ストークス主張は、切り口は違うが、どちらもフロンティアAIをめぐる「誰の成果か」「どこまで模倣・抽出が許されるか」という線引きの問題に触れている。</li>
<li>アップルのリスニング機能は、AIが生活に入り込むときのプライバシーの慣れをどこに置くか、という話。</li>
<li>量子は、サイクアンタムへの1億ドルを含む3社との契約で、実用化競争が製造とサプライチェーンの国内化という産業政策の段階に入ったことを示した。</li>
<li>セキュリティは、シスコのFMCもクロームのV8も、3月や8月に公表されていた話が、実際の悪用の確認で優先度が跳ね上がったパターン。境界機器とブラウザという、多くの人が通る入口が同時に狙われている。</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://www.cisa.gov/news-events/cybersecurity-advisories/aa26-251a">CISA: China-Based AI Companies Conducting Industrial-Scale Distillation Campaigns Against U.S. AI Companies (AA26-251A)</a></li>
<li><a href="https://www.nsa.gov/Press-Room/Press-Releases-Statements/Press-Release-View/Article/4592113/nsa-and-others-warn-china-based-ai-companies-are-distilling-us-frontier-ai-mode/">NSA Press Release: NSA and Others Warn China-Based AI Companies are Distilling U.S. Frontier AI Models</a></li>
<li><a href="https://thehackernews.com/2026/09/us-agencies-accuse-china-ai-firms.html">The Hacker News: U.S. Agencies Accuse China AI Firms of Distilling Claude, GPT, Gemini, and Grok</a></li>
<li><a href="https://openai.com/index/navier-stokes-solution/">OpenAI: On the Navier–Stokes Millennium Prize Problem</a></li>
<li><a href="https://www.axios.com/2026/09/08/openai-math-solution-navier-stokes-credit">Axios: OpenAI's historic math solution overshadowed by credit controversy</a></li>
<li><a href="https://www.cnn.com/2026/09/09/business/openai-millennium-problems-navier-stokes-hnk">CNN: OpenAI says it has solved one of math's "Millennium Problems"</a></li>
<li><a href="https://techcrunch.com/">TechCrunch: Apple Watch's new AI features are normalizing the idea that technology is always listening</a></li>
<li><a href="https://www.wired.com/story/apple-watch-listening-features-privacy/">Wired: Apple Doesn't Want You to Worry About the New Apple Watch's Listening Features</a></li>
<li><a href="https://thequantuminsider.com/2026/09/08/psiquantum-finalizes-100m-us-government-award-quantum-computing-rd/">The Quantum Insider: PsiQuantum Finalizes $100 Million Award with the U.S. Department of Commerce</a></li>
<li><a href="https://www.eweek.com/news/quantum-computing-awards-300m/">eWeek: US Puts Up to $300M Into Three Quantum Architectures</a></li>
<li><a href="https://sec.cloudapps.cisco.com/security/center/content/CiscoSecurityAdvisory/cisco-sa-onprem-fmc-authbypass-5JPp45V2">Cisco Security Advisory: cisco-sa-onprem-fmc-authbypass-5JPp45V2 (CVE-2026-20079)</a></li>
<li><a href="https://blog.talosintelligence.com/fmc-ongoing-exploitation/">Cisco Talos: Active exploitation of Cisco Secure Firewall Management Center vulnerabilities</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/cisco-confirms-cve-2026-20079-secure-fmc-flaw-exploited-in-attacks/">BleepingComputer: Cisco confirms CVE-2026-20079 Secure FMC flaw exploited in attacks</a></li>
<li><a href="https://thehackernews.com/2026/09/chrome-v8-zero-day-exploited-in-wild.html">The Hacker News: Chrome V8 Zero-Day Exploited in the Wild Enables Code Execution Inside Sandbox</a></li>
<li><a href="https://www.helpnetsecurity.com/2026/09/09/google-chrome-cve-2026-87491-zero-day-flaw/">Help Net Security: Google fixes yet another actively exploited Chrome zero-day (CVE-2026-87491)</a></li>
</ul>

</details>

---

[← 2026-09-10 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
