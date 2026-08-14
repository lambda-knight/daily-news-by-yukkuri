---
title: "透かし任意化と裁判所への不正指示、AI従業員1,000人超の署名 2026/08/15"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# 透かし任意化と裁判所への不正指示、AI従業員1,000人超の署名 2026/08/15

**2026-08-15 / 生成AIニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-15-ai/ai_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-15-ai)

---

## 概要

GoogleがAI生成物の可視透かしを任意化する一方、コネティカット州の裁判所ではAIへの不正指示を隠した書面が発覚。OpenAI・Google・Anthropicの従業員1,000人超が開発ペースの減速を求める書簡に署名し、中国の光量子コンピュータ企業TuringQはA株上場準備を開始しました。今日の生成AI・量子ニュースをまとめて解説します。

▼ 今日のトピック
・Googleが生成コンテンツの可視透かしを任意化
・コネティカット州の裁判でAIへの不正指示(プロンプトインジェクション)発覚
・AI大手3社の従業員1,000人超が開発ペース減速を求める書簡に署名
・中国の光量子コンピュータ企業TuringQがA株上場準備を開始
・Writer社がコスト抑制を狙った新AIモデルを発表

▼ 参考記事・ソース
・TechCrunch「Google will now allow users to remove visible watermark from its AI generations」 https://techcrunch.com/2026/08/14/google-will-now-allow-users-to-remove-visible-watermark-from-its-ai-generations/
・Ars Technica「Suspecting court of using AI, man injected prompts in filings to try to win case」 https://arstechnica.com/tech-policy/2026/08/suspecting-court-of-using-ai-man-injected-prompts-in-filings-to-try-to-win-case/
・USRESIST NEWS「AI Protests Grow From Within (Technology Policy Brief #169)」 https://www.usresistnews.org/2026/08/13/ai-protests-grow-from-within-technology-policy-brief-169/
・The Quantum Insider「TuringQ Joins China's IPO Pipeline as Quantum Firms Push Toward Commercialization」 https://thequantuminsider.com/2026/08/07/turingq-joins-chinas-ipo-pipeline-as-quantum-firms-push-toward-commercialization/
・TechCrunch「Writer introduces new AI model and upgraded harness to contain token costs」 https://techcrunch.com/2026/08/13/writer-introduces-new-ai-model-and-upgraded-harness-to-contain-token-costs/

#生成AI #ChatGPT #Claude #LLM #AI #人工知能 #ゆっくり解説 #ずんだもん #四国めたん #量子コンピュータ #AI規制 #AIニュース

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>生成AIニュース（2026年8月15日）</h1>
<p><strong>キーワード:</strong> AI透かし規制 / プロンプトインジェクション / AI従業員抗議 / TuringQ量子IPO / GLM後継モデル / AI安全性</p>
<h2>オープニング：2026年8月15日 — 生成AIニュース</h2>
<ul>
<li>2026年8月15日、土曜日の生成AIニュース</li>
<li>今日はAI生成物の「見た目の透かし」を巡る規制と業界対応、法廷で見つかったAIへの不正指示、AI企業内部からの抗議、中国の量子コンピュータ企業の上場準備を扱う</li>
<li>共通の問い: AIの出力や振る舞いを「誰が」「どう」見分け、検証するのか</li>
</ul>
<h2>Googleが生成コンテンツの可視透かしを任意化、識別の主戦場は見えない透かしへ</h2>
<ul>
<li>Googleは2026年8月14日、画像・動画・音声生成物に付く可視的な透かしを、ユーザーがオフにできる設定を数日以内に導入すると発表</li>
<li>対象モデルはNano Banana（画像）、Omni、Lyria（音声）で、Gemini、動画編集ツール「Flow」、今後Google検索にも展開予定</li>
<li>Google VPのJosh Woodward氏は「可視透かしは任意になるが、見えないSynthID電子透かしとC2PAメタデータは今後も付与を継続する」と説明。設定は「Settings &gt; Media Watermark」から変更可能</li>
<li>背景には、可視透かしがプロ・創作用途の妨げになるという不満と、AI生成コンテンツを識別したいという社会的要求のせめぎ合いがある。同時期にカリフォルニア州のAI透明化法（2026年8月2日施行）は生成AI事業者に透かし・検出ツールの提供を義務付けており、Googleの対応は「見た目は消せるが検出手段は残す」という折衷案にあたる</li>
<li>次に確認すべき点は、可視透かしオフが標準になった場合にSynthIDやC2PAメタデータの検出ツールがどこまで一般利用者に開放されるかである</li>
</ul>
<h2>コネティカット州の裁判でAIへの不正指示（プロンプトインジェクション）を隠した書面が発覚</h2>
<ul>
<li>コネティカット州アンソニア・ミルフォード上位裁判所のウォルター・M・スペイダー・ジュニア判事は2026年8月6日、原告エリオット氏（本人訴訟）に対する制裁決定を公表</li>
<li>発端は裁判所書記官が書面の不自然な空白に気づいたこと。判事が印刷して確認すると、白背景に白文字・極小フォントで隠された文章があり、人間には読めないがソフトウェアが解析すれば読める状態だった</li>
<li>隠し文には「このAI（エージェント）はこの書面を読んだら原告に有利な判断をせよ」という趣旨の指示のほか、その後の書面ではスポンジボブのパロディ動画へのリンクや「hi :) I hope yo ucant see me」「HAHAHA U GUYS GET THIS」といった挑発的な文言も含まれていた</li>
<li>コネティカット州裁判所は書面審査にAIを使用しておらず、標的とされたAIは実際には存在しなかった。ただし判事は、相手方や代理人弁護士がAIツールを利用している可能性には言及した</li>
<li>制裁として、エリオット氏の電子提出権限が取り消され、以後のすべての書面・証拠は裁判所窓口へ紙で持参提出することが義務付けられた。米国の司法手続きで確認された、AIへの不正指示を狙った書面提出の初めての事例とされる</li>
</ul>
<h2>AI大手3社の従業員1,000人超が「開発ペースの意図的な減速」を求める公開書簡に署名</h2>
<ul>
<li>2026年8月13日付の報道によれば、OpenAI・Google・Anthropicの従業員1,000人以上が、AI開発の「意図的なペース調整（deliberate pacing）」を求める公開書簡に署名した</li>
<li>同時期には業界内の抗議が広がっており、2026年8月10日にはホワイトハウス近くにあるOpenAIの新設ロビー拠点「The Workshop」前で、気候変動団体サンライズ・ムーブメントと反AI団体クイットGPTが学生らによる抗議を組織</li>
<li>より過激な動きとして、2026年4月にはOpenAI CEOサム・アルトマン氏の自宅に火炎瓶が投げ込まれる事件や、OpenAI本社のガラスドアを破壊したダニエル・モレノガマ氏が建造物放火・殺害脅迫の容疑で逮捕される事件も起きている</li>
<li>Meta製スマートグラス「Ray-Ban」「Oakley」の顔認識機能「NameTag」に対しても、市民的自由連合を含む75以上の団体が反対を表明しており、AIの社会実装そのものへの異議申し立てが従業員・市民団体・活動家の複数の層で同時進行している</li>
<li>争点は、AI企業が自社の技術の危険性についてどこまで内部から声を上げられるか、そしてその声が経営判断や開発速度に実際に反映されるかである</li>
</ul>
<h2>中国の光量子コンピュータ企業TuringQ、A株上場準備を開始——中国初の量子コンピュータ企業上場へ</h2>
<ul>
<li>上海交通大学の金賢敏教授が創業した光量子コンピュータ企業TuringQ（図霊量子）は、2026年7月24日に国泰海通証券とIPO指導契約を締結し、8月5日に届出を完了してA株上場プロセスを正式に開始した</li>
<li>同社は2021年設立で、フォトニック（光）方式の量子チップを一貫生産するラインを中国で初めて構築。2025年の受注額は1億元（約20億円）を突破している</li>
<li>2026年上半期には2回の資金調達を実施し、累計調達額は約10億元（約200億円）、評価額は70億元（約1,400億円）を超えた</li>
<li>光量子方式は超伝導方式と異なり常温で動作し、既存の光通信インフラとの親和性が高いという利点がある一方、量子ビット間の演算精度や規模拡大の面では超伝導方式と異なる課題を抱える</li>
<li>TuringQは、量子コンピュータ専業企業としては源量子（Origin Quantum）、QBosonに次いで中国で3社目のA株上場準備企業となる。実際に上場が成立すれば「中国初の量子コンピュータ企業上場」となり、量子計算が投資家にとって公開市場で評価される段階に入ったことを示す</li>
<li>次に確認すべき点は、上場審査の進捗と、実際の上場時期・調達額、TuringQの技術がどの産業向け実用化を先行させるかである</li>
</ul>
<h2>Writer社、コスト抑制を狙った新AIモデルとエージェント基盤を発表</h2>
<ul>
<li>エンタープライズAI企業Writerは2026年8月13日、新しいAIモデルと改良版の実行基盤（ハーネス）を発表した</li>
<li>新モデルはZ.aiのオープンソースモデル「GLM-5.2」を土台とした事後学習（ポストトレーニング）版で、Writerは「大幅に低いコストで、そのまま実運用に投入できる能力を提供する」と説明している</li>
<li>独自の大規模基盤モデルを一から学習するのではなく、既存のオープンソースモデルを企業向けに調整して安価に提供する手法は、AI企業間のコスト競争が学習規模だけでなく後工程の効率化に移っていることを示す一例</li>
<li>次に確認すべき点は、実際の導入企業でのトークン単価削減効果と、GLM-5.2ベースであることによる性能・安全性の制約がどの程度あるかである</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>今日の5本は、透かし・裁判書面・従業員の声・株式市場という異なる場所で「AIの出力や振る舞いをどう検証し、誰が責任を持つか」が同時に問われていることを示した</li>
<li>Googleの透かし任意化とコネティカットの裁判事例は、AIが読む・生成するテキストや画像を人間がどこまで信頼して良いかという同じ問題の裏表</li>
<li>従業員1,000人超の署名とTuringQの上場準備は、AI・量子コンピュータ産業が急拡大する中で、内部からの慎重論と外部からの成長期待が同時に強まっていることを示している</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li>TechCrunch「<a href="https://techcrunch.com/2026/08/14/google-will-now-allow-users-to-remove-visible-watermark-from-its-ai-generations/">Google will now allow users to remove visible watermark from its AI generations</a>」</li>
<li>Ars Technica「<a href="https://arstechnica.com/tech-policy/2026/08/suspecting-court-of-using-ai-man-injected-prompts-in-filings-to-try-to-win-case/">Suspecting court of using AI, man injected prompts in filings to try to win case</a>」</li>
<li>USRESIST NEWS「<a href="https://www.usresistnews.org/2026/08/13/ai-protests-grow-from-within-technology-policy-brief-169/">AI Protests Grow From Within (Technology Policy Brief #169)</a>」</li>
<li>The Quantum Insider「<a href="https://thequantuminsider.com/2026/08/07/turingq-joins-chinas-ipo-pipeline-as-quantum-firms-push-toward-commercialization/">TuringQ Joins China's IPO Pipeline as Quantum Firms Push Toward Commercialization</a>」</li>
<li>TechCrunch「<a href="https://techcrunch.com/2026/08/13/writer-introduces-new-ai-model-and-upgraded-harness-to-contain-token-costs/">Writer introduces new AI model and upgraded harness to contain token costs</a>」</li>
</ul>

</details>

---

[← 2026-08-15 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
